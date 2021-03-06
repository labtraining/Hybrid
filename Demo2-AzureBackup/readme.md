# Architecting Hybrid Solutions Demo

The objective of this demo is to demonstrate Azure Backup Server (DPM) backing up a protection group of servers to the Azure backup vault.

## Prerequisites

1.  An Azure subscription

1.  A storage account in the same region as the Azure Backup Vault

1.  A few Azure VMs to act as protection group members

1.  One VM to act as the Azure Backup Server

## Preparation

1.  Log into the Azure Management Portal

1.  Create a new instance of “Backup and Site Recovery” App

    * Name it “BackupDemoVault”

1.  Once provisioned click the Backup link in the “Get Started” section

    ![image](Media/image1.png)

1.  Choose the defaults and select a Virtual Machine from the list in the “Items to backup” section

    ![image](Media/image2.png)

1.  Backup a folder on an On-Premises server by choosing Add in the Backup Items section

    ![image](Media/image3.png)

1.  Install the agent on the machine you want to protect

    ![image](Media/image4.png)

1.  Copy the Vault credentials to the machine you want to protect

1.  Click the Proceed to Registration and choose the vault credentials

1.  Configure the backup to backup the desired files/folders. In this demonstration create a folder "data" in the c-drive and add a text file called important.txt into it.

## Demonstration

The whole point about Backup is to recover. This demo will show how to use DPM to recover a file

1. From the Azure Backup Server (DPM), Choose **Recovery** (lower left). 
   
    ![image](Media/image5.png)

1. Choose **Recover to the original location**  
   
    ![image](Media/image6.png)

1. Review summary and click **Recover.** 

    ![image](Media/image8.png) 

    ![image](Media/image9.png)