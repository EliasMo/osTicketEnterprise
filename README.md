# osTicketEnterprise

- download Xampp
- download osticket
  

### Download XAMPP
![image](https://github.com/user-attachments/assets/2ce8a5be-2062-47e2-b4d6-a388266f1ee7)

- Make sure IIS is stopped to stop port conflict
- Start Apache, MySQL and verify both services are running

## Test XAMPP - go to http://localhost
![image](https://github.com/user-attachments/assets/bd34db93-5084-489e-8fdf-a893575e2e00)

![image](https://github.com/user-attachments/assets/3bf5b460-28b2-4c73-a809-396d008d9018)

Head to localhost/phpmyadmin 
- naming the database osticket
![image](https://github.com/user-attachments/assets/a00838ea-0e5c-41d5-8566-d251aa2759fd)


- Go to User accounts and add user account, allow grant all privvileges on database osticket

![image](https://github.com/user-attachments/assets/704b5fd7-b61c-4231-b063-775bba80e797)

### Download and File Setup 
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



