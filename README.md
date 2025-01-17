# Ansible Role: SonarQube

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

> **DEPRECATED**: This role is no longer actively maintained. It may still work, but I have marked it as 'deprecated' on Ansible Galaxy, and recommend you find a new role to replace it, or fork it and use your fork.

An Ansible Role that installs [SonarQube](http://www.sonarqube.org/) on RedHat/CentOS and Debian/Ubuntu Linux servers.

## Requirements

Requires the `unzip` utility to be installed on the server. Also, different SonarQube versions require different minimum versions of Java:

  - SonarQube 5.0-5.5 requires Java 1.7+
  - SonarQube 5.6+ requires Java 1.8+

Finally, recent versions of SonarQube also require MySQL 5.6 or later.

## Role Variables

Available variables are listed below, along with default values:

    workspace: /root

Directory where downloaded files will be temporarily stored.

    sonar_download_validate_certs: true

Controls whether to validate certificates when downloading SonarQube.

    sonar_download_url: http://dist.sonar.codehaus.org/sonarqube-4.5.4.zip
    sonar_version_directory: sonarqube-4.5.4

The URL from which SonarQube will be downloaded, and the resulting directory name (should match the download archive, without the archive extension).

    sonar_web_context: ''

The value of `sonar.web.context`. Setting this to something like `/sonar` allows you to set the context where Sonar can be accessed (e.g. `hostname/sonar` instead of `hostname`).

    sonar_mysql_username: sonar
    sonar_mysql_password: sonar
    
    sonar_mysql_host: localhost
    sonar_mysql_port: "3306"
    sonar_mysql_database: sonar
    
    sonar_mysql_allowed_hosts:
      - 127.0.0.1
      - ::1
      - localhost

JDBC settings for a connection to a MySQL database. Defaults presume the database resides on localhost and is only accessible on the SonarQube server itself.

## Dependencies

  - nholuong.java
  - nholuong.mysql

## Example Playbook

    - hosts: all
      roles:
        - nholuong.sonar

Using the defaults, you can view the SonarQube home at `http://localhost:9000/` (default System administrator credentials are `admin`/`admin`).

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟