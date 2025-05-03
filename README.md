<p align="center">
<img src="https://i.imgur.com/ji8tw98.png" width="50%" height="50%"/>
</p>

<h1>Setup Domain Controller in Active Directory</h1>
<p>This tutorial shows what we need to do in order to get our AD lab started</p>
</b> 

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Setup Domain Controller in Azure</h2>
<p>
 1. Create a Resource Group
</p>
<p>
 2. Create a Virtual Network and Subnet
</p>
<p>
  3. Create the Domain Controller VM (Windows Server 2022) named “DC-1”
  <ul>
    <li>Username: <strong>labuser</strong></li>
    <li>Password: <strong>Cyberlab123!</strong></li>
  </ul>
</p>


<p><em>After VM is created, set Domain Controller’s NIC Private IP address to be static</em></p>

<p>
  4. Log into the VM and disable the Windows Firewall (for testing connectivity)
</p>
</b>

<h2>Setup Client-1 in Azure</h2>
<p>
 1. Create the Client VM (Windows 10) named “Client-1”
 <ul>
  <li>Username: <strong>labuser</strong></li>
  <li>Password: <strong>Cyberlab123!</strong></li>
 </ul>
</p>

<p>
 2. Attach it to the same region and Virtual Network as DC-1
</p>
<p>
 <em>After VM is created, set Client-1’s DNS settings to DC-1’s Private IP address</em>
</p>
<p>
 3. From the Azure Portal, restart Client-1
</p>
<p>
 4. Login to Client-1
</p>
<p>
 5. Attempt to ping DC-1’s private IP address
 <ul>
  <li>Ensure the ping succeeded</li>
 </ul>
</p>
<p>
 6. From Client-1, open PowerShell and run ipconfig /all
 <ul>
  <li>The output for the DNS settings should show DC-1’s private IP Address</li>
 </ul>
</p>
