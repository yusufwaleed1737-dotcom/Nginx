# AWS Route 53 Domain & Nginx Web server set up

## Steps taken:

### 1. Domain registration on AWS Route 53
- **Signed into AWS Route 53 (Set up a new account if first time)**
- **Searched for available domains** '(yusufwaleed.co.uk)'

<img width="452" height="166" alt="Image" src="https://github.com/user-attachments/assets/b56431e2-198c-4a47-b143-d7d52e3ea11b" />

- **Purchase and successfully registered the domain**

### 2. Set up EC2 instance
- **Head to EC2 console on AWS and select Launch instance**
    - **Choose instance type** '(I chose Amazon Linux)'
    - **Instance type:** 't3.micro'
- **Configure the security group to allow inbound rules:**
    - **Allow HTTP (port 80) from anywhere**
    - **Allow SSH (port 22) from your IP (for Admin access)**

### 3. Hosted Zone configuration
- **Navigated to Hosted Zones > Create Hosted Zone on AWS portal**
- **Configured DNS Records**
    - **Subdomain:** 'nginx.yusufwaleed.co.uk'
    - **Record type:** 'A'
    - **Value:** 'EC2 instance IP address'
    - **TTL:** '300s'

<img width="199" height="176" alt="Image" src="https://github.com/user-attachments/assets/51e033ea-c480-4014-964e-f15aa36f598c" />

- **Saved this**

### 4. Checking the domain
- **Tested domain** 'by navigating to nginx.yusufwaleed.co.uk'
- **Confirmed Nginx default page was showing correctly**

<img width="263" height="124" alt="Image" src="https://github.com/user-attachments/assets/557bd2fc-bf49-4b3c-bbb5-7f0e7dfd0993" />

### 5. Nginx Customisation
- **Accessed Nginx configuration file** '(From EC2 instance)
- **Used Vi editor to modify the look**
- **Saved changes and headed back to domain to confirm it looks as it should**

## Results:
Successfully purchased a custom domain from Route 53 and pointed this to an EC2 instance which was running Nginx, and personalised the content

## Set up:
- AWS Route 53 (DNS and Domain registration)
- AWS EC2 (Virtual server)
- Nginx (Web server)
- Vi editor (Configure the web server)

    