# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: Elavarasan M
* **Register Number**: 212224040083
* **Date of Submission**: 28-02-2026

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

1. First, I logged in to the AWS Management Console and opened the Amazon EC2 dashboard. Then I navigated to the Elastic Block Store section to view the available volume types.

2. I created a new EBS volume by selecting the required volume type (gp3) and specifying the storage size. I ensured that the volume was created in the same Availability Zone as my existing EC2 instance.

3. After the volume was created, I selected the volume and attached it to my running EC2 instance as an additional device (for example, /dev/xvdf).

4. I connected to the EC2 instance using SSH. Then I checked the attached device using the lsblk command and formatted the new volume using the ext4 file system.

5. I created a directory (for example, /mnt/ebs) and mounted the formatted volume to that directory using the mount command.

6. Inside the mounted directory, I created sample files and folders to store data and verified that the files were saved successfully.

7. Finally, I rebooted the EC2 instance and checked the mounted volume again to confirm that the stored data was still available, proving that EBS provides persistent storage.



---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

![alt text](images/image-1.png)

### Screenshot 2: EBS Volume Attached to EC2

![alt text](images/image-2.png)

### Screenshot 3: Mounted Volume with Data

![alt text](images/image-3.png)

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
