<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>Enabling Log Collection for VMs and NSGs</h1>
In this tutorial, we are sharing out resources over the network and creating file shares to allow read, write, or deny access to individual users or groups. <br />


<h2>Video Demonstration</h2>

- ### [Enabling Log Collection for VMs and NSGs](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- File Folders


<h2>Operating Systems Used </h2>

- Windows 10 (21H2)


<h2>High-Level Steps</h2>

- Create a Storage Account 
- Add Microsoft Sentinel to the new workspace
- Created the geoip watchlist
- 

<h2>Actions and Observations</h2>

<p>
<img src="https://github.com/user-attachments/assets/8a55d250-cbfe-4f1a-a68c-3db3c0b5f0d1" height="80%" width="80%" />
</p>

<br />

<p>
<img src="https://github.com/user-attachments/assets/edbf06e5-2b07-400d-b2dc-6a99054021f9" height="80%" width="80%""/>
 
</p>
<p>
Create a Storage Account called 'storeccsecurity01' under the Resource Group of 'CyberCat-RG' and Region 'US East 2'.
</p>
<p>
  <img src="https://github.com/user-attachments/assets/8a814d62-4d4d-45cd-8bff-ac81ae5e3e8a" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/f022d86a-f9e8-4319-92ac-c6d20f213588" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/1d4de23f-4ac6-4080-b1bd-fec23838f12f" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/3ede9840-b620-4e78-8329-f5ca1173c586" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/a6dd917b-3d3f-454d-9bc3-7cf83efacb16" height="80%" width="80%" />

</p>
<p> I was able to enable flow logs for both NSGs</p>
<br />

<p>

<img src="https://github.com/user-attachments/assets/f15d08d3-0799-47e0-8a37-0dd68c6b608b" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/33c3d6c3-79bf-452a-8d92-ed9e0a6c3d45" height="80%" width="80%" />
 <img src="https://github.com/user-attachments/assets/adcdc9e6-4846-4883-9cd7-83174e339636" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/d00239e2-3f58-40b7-aa0c-061c81ca2988" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/ea329ffd-ee7a-42e6-88e1-bf243cf6008e" height="80%" width="80%" />
</p>
<p>
Using Linux Syslog to create a Data source for Data Collection Rules within Log Analytics Workspace.

</p>
<p>
 
  <img src="https://github.com/user-attachments/assets/6e7b0bc3-5e0c-468a-be88-2f7c22b9a7df" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/f209dfb7-7c36-48e4-8546-9cac014c7f35" height="80%" width="80%" />
</p>
<p>
  Able to set all Domain Users to read-access to permission level to read only and write-access (read/write). Able to set all Domain Admins to no-access with permission level set to read/write.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/046aa331-9381-4331-91b5-6b7fc891bb34" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/33168862-a1b4-452e-ad60-94676fd991ab" height="80%" width="80%" />
<img src="https://github.com/user-attachments/assets/9aab7331-a97f-4a20-a888-b33b30489151" height="80%" width="80%" />
</p>
<p>
  No-access permission is only for Domain Admins. Since I'm logged into my user BAT.MEX on Client-1 VM, I was denied access.
</p>
<p>
<img src="https://github.com/user-attachments/assets/bf793c39-dc7d-4979-a781-bcbe5ab16786" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/d50ac89b-dac8-4b99-85a8-02cf6c39389f" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/45351db0-8895-432b-a29c-2a6470a3f6aa" height="80%" width="80%" />
  <img src="https://github.com/user-attachments/assets/92fb840d-518c-4bab-8c2f-d91fcd3fc591" height="80%" width="80%" />
  <img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />
<img src="" height="80%" width="80%" />

</p>
<p>
  Although as a Domain user BAT.MEX, I am granted access to read-access folder, but when trying to create a txt.file, I was unable to since Domain Users are granted read-only access.
</p>
