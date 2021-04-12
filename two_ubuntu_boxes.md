# ASSIST 2 UBUNTU VMs TO COMMUNICATE WITH EACH OTHER

1. Make sure the memory allocation to both the VMs is appropriate enough that you can run 2 VMs at the same time.
2. Run the following commands on both the VMs:\
       1. ```sudo apt-get update```\
       2. ```sudo apt-get upgrade```
3. Generate passwordless login on each machine for the other machine.\
    1. run $ssh-keygen on machine A\
    2. Do one of the following:\
        1. copy the contents of ~/.ssh/id_rsa.pub of machine A to ~/.ssh/authorized_keys of machine B.\ 
        2. run command on machine A: ssh-copy-id <ip of machine B>\
    3. Now try logging in from machine A to machine B via SSH\
    4. Do the above steps for machine B to setup passwordless connection from machine B to machine A.
