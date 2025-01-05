# osTicketEnterprise

### Phase 1: Setup 
- Download Xampp
- Download osticket
- Configure XAMPP
- File Setup
  

## Download XAMPP
![image](https://github.com/user-attachments/assets/2ce8a5be-2062-47e2-b4d6-a388266f1ee7)

- Make sure IIS is stopped to stop port conflict
- Start Apache, MySQL and verify both services are running

# Test XAMPP - go to http://localhost
![image](https://github.com/user-attachments/assets/bd34db93-5084-489e-8fdf-a893575e2e00)

![image](https://github.com/user-attachments/assets/3bf5b460-28b2-4c73-a809-396d008d9018)

Head to localhost/phpmyadmin 
- naming the database osticket
![image](https://github.com/user-attachments/assets/a00838ea-0e5c-41d5-8566-d251aa2759fd)


- Go to User accounts and add user account, allow grant all privvileges on database osticket

![image](https://github.com/user-attachments/assets/704b5fd7-b61c-4231-b063-775bba80e797)

# Download OsTicket and File Setup 
1. Download osTicket
Go to osTicket.(https://osticket.com/download/)
![image](https://github.com/user-attachments/assets/18ad3035-9ca4-4aac-b10c-d760532126df)

For the enterprise implemetation, Select these key plugins:
  - Authentication::LDAP and AD
      - Enables integration with AD
      - Allows domain user login

  - Audit:: Audit Log
      - Tracks system changes
      - Security moniotoring
      - User activity logs

  - Authentication:: Password Policy
      - Enforce password policy    

  - Storage :: Attachments on the Filesystem
      - Local file storage
        
![image](https://github.com/user-attachments/assets/056499a5-bb61-48be-bc69-1e8f85c07642)

Extract to a temp location
![image](https://github.com/user-attachments/assets/9b326f9d-812c-4711-9d3d-90c76b038e62)


Move to C://xampp/htdocs
![image](https://github.com/user-attachments/assets/b78bc4a1-2417-4cdf-904d-995714301757)


- go to http://localhost/osticket
![image](https://github.com/user-attachments/assets/5d9f38e8-c81b-4be1-980e-1c1efb1a2dbd)


To maintain consistency between AD and osTicket systems, I'll be reusing AD admin account details.
The system email is going to be helpdesk@internalcompany.com. 
![image](https://github.com/user-attachments/assets/741e3759-d2c0-458e-a776-8fc0d075807b)

![image](https://github.com/user-attachments/assets/07353222-585e-4def-8cdc-4d993c3e2812)

Create the Admin User in phpmyadmin 

![image](https://github.com/user-attachments/assets/e52c29ed-abb5-40d7-b060-7bf6b588df78)


```sql
CREATE USER 'admin_EMO'@'localhost' IDENTIFIED BY 'ThePasswordHere';
GRANT ALL PRIVILEGES ON osticket.* TO 'admin_EMO'@'localhost';
FLUSH PRIVILEGES;

```

![image](https://github.com/user-attachments/assets/e5fbf51f-8feb-4ba8-95cb-aa4f38568e67)

Congrats! You set up the support ticket system.

![image](https://github.com/user-attachments/assets/42a7881f-a22b-4571-909e-a276cb8ac9e5)

Now lets go to the admin panel at localhost/osTicket/scp:

![image](https://github.com/user-attachments/assets/1e7500dd-0017-4a2c-8371-55663d0d0a07)


For security reasons, you should delete the setup directory since its not needed and its risky if left accessible.
Go to C:/xampp\htdocs\osTicket\setup and delete. This will stop unauthorised reconfiguration. (yeah i defo need to get good with powershell commands - im a noob still)

![image](https://github.com/user-attachments/assets/1e7fec1d-d346-4852-9d75-0d460a032e7a)


### Enterprise Integration 





