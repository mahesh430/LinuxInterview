1.How to create atatch a new volume to a aws machine ?
Ans: 1.create a volume and and attach it to a EC2 machine
     2.To confirm the presence of the block volume, run the lsblk command
     3.Mounting the newly added EBS volume,to make the block volume accessible and ready to be used, we need to mount it on the AWS instance But first, you need to
     create a partition table as shown 
      fdisk /dev/xvdf
     
