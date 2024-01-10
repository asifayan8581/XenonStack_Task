# Xenonstack Task1

# Xenonstack-assessment

output of linux 

1. nano command ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/57163d06-a6d3-464a-81db-a858946c3e0c)
![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/fa42e8ed-c00f-4ef7-bd76-5267b8b1dc93)

2. Pasting bash file ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/1fd50de0-64ad-4466-b9ad-c4954303507b)
  ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/ead52bbd-9fb6-48a3-b5b9-17aef285f4a3)

3. epsa1--help ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/f9aa73f0-458e-4026-a340-2c3b53024ceb)
![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/128a9fa6-33e0-4786-95df-7fa0d249b6ee)

4. epsa1 cpu getinfo ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/8fadda28-40e7-4bc7-8392-32b2ac1c615f)
5. epsa1 --version ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/e792d195-8a6e-425e-9538-5c842fab39f5)
6. epsa1 memory getinfo ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/4552b57d-b92f-40c9-a4cb-ef43a2214c41)
7. epsa1 user list ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/2f4b42d0-cbd8-48c4-b148-02421778135f)
8. epsa1 user list --sudo-only ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/d030f7d6-1f0a-4a14-b7a9-24391cd9d22f)
9. epsa1 user create ![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/2b3cfd6c-1ce0-4e92-b796-16701c748e99)
![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/19dee4a9-b13d-49d4-b1a1-de7a7f826934)




ROUND 2
![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/9816c3d9-7720-43bc-8522-441399b05748)

![image](https://github.com/20BCS4485/Xenonstack-assessment/assets/99709007/b38b26ea-8130-44ac-983f-641b263af402)






 







# Xenonstack Task2
## Installation

### Prerequisites

#### 1. Install Python
Install ```python-3.7.2``` and ```python-pip```. Follow the steps from the below reference document based on your Operating System.
Reference: [https://docs.python-guide.org/starting/installation/](https://docs.python-guide.org/starting/installation/)

#### 2. Install MySQL
Install ```mysql-8.0.15```. Follow the steps form the below reference document based on your Operating System.
Reference: [https://dev.mysql.com/doc/refman/5.5/en/](https://dev.mysql.com/doc/refman/5.5/en/)
#### 3. Setup virtual environment
```bash
# Install virtual environment
sudo pip install virtualenv

# Make a directory
mkdir envs

# Create virtual environment
virtualenv ./envs/

# Activate virtual environment
source envs/bin/activate
```

#### 4. Clone git repository
```bash
git clone "https://github.com/parvsablok/Xenonstack_Task1.git"
```

#### 5. Install requirements
```bash
cd simple-django-project/
pip install -r requirements.txt
```

#### 6. Load sample data into MySQL
```bash
# open mysql bash
mysql -u <mysql-user> -p

# Give the absolute path of the file
mysql> source ~/simple-django-project/world.sql
mysql> exit;

```
#### 7. Edit project settings
```bash
# open settings file
vim panorbit/settings.py

# Edit Database configurations with your MySQL configurations.
# Search for DATABASES section.
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'world',
        'USER': '<mysql-user>',
        'PASSWORD': '<mysql-password>',
        'HOST': '<mysql-host>',
        'PORT': '<mysql-port>',
    }
}

# Edit email configurations.
# Search for email configurations
EMAIL_USE_TLS = True
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_HOST_USER = '<your-email>'
EMAIL_HOST_PASSWORD = '<your-email-password>'
EMAIL_PORT = 587

# save the file
```
#### 8. Run the server
```bash
# Make migrations
python manage.py makemigrations
python manage.py migrate

# For search feature we need to index certain tables to the haystack. For that run below command.
python manage.py rebuild_index

# Run the server
python manage.py runserver 0:8001

# your server is up on port 8001
```
Try opening [http://localhost:8001](http://localhost:8001) in the browser.
Now you are good to go.

### 9. URLs
#### Signup: [http://localhost:8001/signup](http://localhost:8001/signup)
![](https://i.imgur.com/T1KkfXi.png)
#### Login: [http://localhost:8001/login](http://localhost:8001/login)
![](https://i.imgur.com/KvyiuU6.png)
#### home for search: [http://localhost:8001/](http://localhost:8001/)
![](https://i.imgur.com/234qAiS.png)
#### country page: [http://localhost:8001/country/kenya](http://localhost:8001/country/kenya)
![](https://i.imgur.com/3zh3YKd.png)
#### Logout: [http://localhost:8001/logout](http://localhost:8001/logout)

