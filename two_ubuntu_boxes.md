# ASSIST 2 UBUNTU VMs TO COMMUNICATE WITH EACH OTHER

1. Make sure the memory allocation to both the VMs is appropriate enough that you can run 2 VMs at the same time.
2. Run the following commands on both the VMs:
        * sudo apt-get update
        * sudo apt-get upgrade
3. Generate passwordless login on each machine for the other machine.
        * run $ssh-keygen on machine A
        * Do one of the following:
                * copy the contents of ~/.ssh/id_rsa.pub of machine A to ~/.ssh/authorized_keys of machine B. 
                * run command on machine A: ssh-copy-id <ip of machine B>
        * Now try logging in from machine A to machine B via SSH
        * Do the above steps for machine B to setup passwordless connection from machine B to machine A.
