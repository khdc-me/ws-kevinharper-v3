# ws-kevinharper
Repository for my personal website.

This is the parent portal into current and previous projects. I use this site for notes, bookmarks, and documentation.

## Tech Stack:
### Infrastructure & CI:
* Vagrant
* GitHub
* GitHub Actions
* Release/Versioning
* AWS Elastic Beanstalk
1
### Software:
* Python 3.9.6
* Django 3.2.6
* gunicorn 20.1.0
* whitenoise 5.3.0
* flake8
* HTML5 + CSS3
* ES6/JavaScript

## Cloning Repository & Dev Environment Setup
### Prerequisites
You must have VirtualBox and Vagrant installed on your system. *

### Cloning Repository
1. Click green "Code" button immediately above the top-right corner of this repository.
2. Select & copy your preferred method (HTTPS, SSh, or GitHub CLI).
3. Run the copied command on your system. *

### Dev Environment Setup
1. Go into the newly created folder.
2. Run
```vagrant up```

### Using Dev Environment
1. Instance is set up with
  * Hostname: dev-kevinharper-com
  * IP: 192.168.33.10
  * Shared folder between host and guest
  * dev-kevinharper-com symbolic link in home directory
2. SSH into instance
```vagrant ssh```
3. cd into dev-kevinharper-com
  * This is a symlink to /vagrant/
  * /vagrant/ is shared with your local host directory (Any changes here will reflect in your host project files/directories)
4. Run server
```python3.9 manage.py runserver 0.0.0.0:8080```
5. From your host, you can:
  * ping \<the IP\>
  * http://\<the-IP\>:8080
  * to use the Hostname, you will likely have to update your system's hosts file

\* Note: Please refer to your OSs documentation on how to set up a git environment on your workstation/laptop. Mine always run latest Ubuntu LTS, and this is all configured out-of-the-box.
