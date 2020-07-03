1.How to create atatch a new volume to a aws machine 

Ans: 1.create a volume and and attach it to a EC2 machine

     2.To confirm the presence of the block volume, run the lsblk command
     
     3.Mounting the newly added EBS volume,to make the block volume accessible and ready to be used, we need to mount it on the AWS instance But first, you need to
     create a partition table using the command fdisk /dev/xvdf  ,then it will ask for partition table and enter the values accordingly.
     
     4.After creating the partition table, you need to update the kernel with the changes using the partprobe command.
        partprobe /dev/xvdf
        
     5.we need to format the partition before mounting it by using the below command
        mkfs /dev/xvdf -t ext4
        
     6.To mount the volume,  first, create a mount point. We’re using the /new_storage in this case but feel free to call it whatever you want.
        mkdir /new_storage
        
     7.Then mount the volume as shown
        mount /dev/xvdf  /new_storage
      
     
