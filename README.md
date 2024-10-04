<h1>Active Directory</h1>

<h2>Description</h2>
This project demonstrates the creation and configuration of a fully functional Active Directory (AD) environment using hyper-V Manager, Windows Server 2019, and Windows 10 machines. It is designed to simulate real-world IT scenarios for learning and experimentation.
<br />
<br />

## Objectives
1. Install and configure a Windows Server 2019 Domain Controller.
2. Set up users and groups in Active Directory.
3. Configure Group Policies and organizational units (OUs).
4. Enable and configure SMB for file sharing.


## Key Skills Demonstrated
- Active Directory Setup
- Group Policy Management
- Windows Server Administration
- System Networking (NAT configuration)

## Lab Setup
- **Domain Controller**: Windows Server 2019
- **User Machines**: 2 x Windows 10 Enterprise
- **Network**: NAT with internal communication between machines.

Each VM is assigned 2GB of RAM, totaling 8GB of RAM for the entire lab. The network is set to NAT for all machines to communicate internally and share the host's internet connection.

- default switch enable for all and they all connected to it.

![image](https://github.com/user-attachments/assets/b7faa6bb-7150-409d-9248-87006e5122df)


## Domain controller installation
![image](https://github.com/user-attachments/assets/b8d8c1b3-91a6-4253-aa29-f96843077558)

allows machine to communicate on the internet 

![image](https://github.com/user-attachments/assets/965b0c93-1e55-474e-8cc3-9694fbdb4a76)

![image](https://github.com/user-attachments/assets/194548d9-5cba-4aef-a035-abb5c4f262bc)


<h3>setup static ip address</h3>

![image](https://github.com/user-attachments/assets/0b9eb1f9-e6c9-4b29-b7df-087ff1f7ee95)
![image](https://github.com/user-attachments/assets/a8aff85e-0137-4fea-8154-bcd1a53159da)

<br />
<br />

## Promoting the Server to Domain Controller

![image](https://github.com/user-attachments/assets/df63c79a-9981-45a1-9ded-ff7f52039349)

![image](https://github.com/user-attachments/assets/72d1e433-0548-4ae2-8080-61695aab1066)

![image](https://github.com/user-attachments/assets/c85cca81-bfce-45ca-bdca-b740549f7e27)

![image](https://github.com/user-attachments/assets/81ccf916-51f8-4869-a2a8-17ea8ce300f0)
![image](https://github.com/user-attachments/assets/a2253f93-f254-4334-b964-bd9617a8564d)
![image](https://github.com/user-attachments/assets/95f20952-cf92-47b4-8afb-e98b3586f7c5)
![image](https://github.com/user-attachments/assets/7db3f69f-cabd-4052-aab0-d9bda779fefc)
![image](https://github.com/user-attachments/assets/19b580b4-ac0e-4d9f-a282-250fe9c863b0)
![image](https://github.com/user-attachments/assets/65aa9476-9d57-487f-9892-1a58e522768a)
![image](https://github.com/user-attachments/assets/64a7a21b-81de-4c55-8ee1-13c62b344b3d)
![image](https://github.com/user-attachments/assets/5e85d962-b610-4d8a-881d-4389c86a4cff)
![image](https://github.com/user-attachments/assets/47057efd-e797-4d68-8bd1-5948280bbb9f)

![image](https://github.com/user-attachments/assets/8482512f-389f-4db8-a099-89c92cce8661)

<h3>server is up and it is signed in as ADHACKING</h3>

![image](https://github.com/user-attachments/assets/94ece524-2794-4407-b961-f49924fed3b6)
![image](https://github.com/user-attachments/assets/22dcf879-ae50-4d21-8638-0e6e1ef0133e)


## user machine installation


## Active directory configuration 
- 1. Opened **Active Directory Users and Computers** on the Domain Controller.
- 2. Created an organizational unit (OU) named `Groups`.
- 3. Moved default users (except Administrator and Guest) to the `Groups` OU.
- 4. Created the following user accounts:
   - **saul** (password: `Password123`)
   - **walter** (password: `Password123`)
- 5. Assigned users to appropriate OUs and applied Group Policies to enforce password complexity.

![image](https://github.com/user-attachments/assets/815ca589-661f-4c7e-bd8f-2023b44ae2bc)
![image](https://github.com/user-attachments/assets/1dc3f160-03e9-422f-806a-abd307d8de77)
![image](https://github.com/user-attachments/assets/ec3885e3-b90a-448d-9a8c-c8ac27c63596)
![image](https://github.com/user-attachments/assets/4386844e-76fd-49b2-a837-6f8a433ef5e1)

<h3> User creation </h3>

![image](https://github.com/user-attachments/assets/332899e1-b687-4358-beda-cd874af3a652)
![image](https://github.com/user-attachments/assets/cc60c922-aee0-48eb-9d13-5d579862ce9e)
![image](https://github.com/user-attachments/assets/8d3ba7ec-494b-4e48-bb88-7a11316a7d31)

<h3> Becoming a member of the domain </h3>

![image](https://github.com/user-attachments/assets/45f839aa-cc4f-408c-9c09-369cce9e0dd4)
![image](https://github.com/user-attachments/assets/ec18d779-82c4-428c-a9bb-1ed5151f853c)
![image](https://github.com/user-attachments/assets/65e0b8cb-7acb-4a59-b24d-08351a135148)

<h3> got an error </h3>

![image](https://github.com/user-attachments/assets/4b92203c-3ed6-4642-8ed5-d6895fc0832f)
<br />
<h3> will verify ip setting on machine </h3>

![image](https://github.com/user-attachments/assets/f317c3df-3c8d-4707-9a12-1f7f3be32d92)

<h3> will put the machine on the same network  </h3>

![image](https://github.com/user-attachments/assets/972d8b30-2dfd-4a46-9db4-cbd67d31ffec)

<h3> will try again </h3>

![image](https://github.com/user-attachments/assets/89a96ac9-613e-40f9-a7dd-2c62fa6f729a)

![image](https://github.com/user-attachments/assets/ef369b96-f2df-493a-a8c5-fbdf6b447011)













