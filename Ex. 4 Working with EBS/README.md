# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: ________MahaJanani.R________
* **Register Number**: ____212224230147_____
* **Date of Submission**: ____27/02/26_____

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

First, I logged into the AWS Management Console and opened the EC2 Dashboard. I went to the EBS section and created a new volume by selecting General Purpose SSD (gp3) with 8 GB storage in the same Availability Zone as my EC2 instance.

After creating the volume, I attached it to my running EC2 instance as /dev/xvdf. Then I connected to the instance using SSH and verified the new disk using the lsblk command.

Next, I formatted the volume, created a directory /mnt/ebs, and mounted the volume to that directory. I confirmed the mount using the df -h command.

I created a sample file inside the mounted directory and stored some data. After that, I rebooted the EC2 instance and checked the directory again. The file and data were still available, which confirmed that EBS provides persistent storage even after instance reboot.
---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="591" height="608" alt="image" src="https://github.com/user-attachments/assets/07db9d2e-9c9b-4697-b676-6d4b4e236803" />


### Screenshot 2: EBS Volume Attached to EC2

<img width="592" height="614" alt="image" src="https://github.com/user-attachments/assets/2de37f4a-80e4-462e-9eee-dbd500fb30dd" />
<img width="960" height="1044" alt="image" src="https://github.com/user-attachments/assets/ea9e1447-8772-4fc4-b12d-6dc372df4799" />

### Screenshot 3: Mounted Volume with Data

<img width="791" height="880" alt="image" src="https://github.com/user-attachments/assets/3fdf821c-31da-4f54-81f7-c31b6616f3ed" />


<img width="799" height="820" alt="image" src="https://github.com/user-attachments/assets/5dfcdafc-3b8a-47ef-bdee-d3c1a7c828fa" />

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
