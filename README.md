
---

# Two-Tier Flask Application with Docker Compose

## Overview

This project demonstrates deploying a **two-tier architecture** on AWS using:

* **Flask** – Application Layer
* **MySQL** – Database Layer



# ⚠ Important Note — Database Validation 

Before accessing the application, it is recommended to validate that the MySQL container is working correctly.

Enter the database container:

```bash
sudo docker exec -it <container_name> bash
```

Login to MySQL:

```bash
mysql -u root -p
```

Password:

```
test@123
```

Run:

```sql
use two_tier;
show tables;
create table messages (message varchar(255)); 
or
CREATE TABLE messages (id INT AUTO_INCREMENT PRIMARY KEY, message TEXT);

describe messages;
```

This confirms:

* Database connectivity
* Container networking
* Proper MySQL authentication
* Successful table creation

This step ensures the backend is functioning before testing the frontend.

---