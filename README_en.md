# Gymnasists Assistant
## Telegram chat-bot for students of Moscow State Classical School
### Installation
1. Install [Python 3.6](https://www.python.org/downloads/release/python-361/)  
2. Install several packages using [pip](https://pip.pypa.io/en/stable/installing/)
```bash
pip install bs4
pip install pyTelegramBotAPI
pip install feedParser
pip install openpyxl
pip install pymySQL
```
3. Install [MySQL Community Server](https://dev.mysql.com/downloads/mysql/) and after setting up the server complete the commands listed below
```sql
CREATE USER 'bot'@'localhost' IDENTIFIED BY 'password';
CREATE DATABASE main;
USE main;
CREATE TABLE main(chatid INT unsigned NOT NULL, status TINYINT unsigned NULL, class varchar (255) DEFAULT 0)ENGINE=InnoDB;
CREATE TABLE lost(item varchar(255) NOT NULL)ENGINE=InnoDB;
CREATE TABLE events(name varchar(255) NOT NULL, date DATE NOT NULL, desc varchar(255) NOT NULL)ENGINE=InnoDB;
```
4. Set up "config.py" file by changing "token" (insert your bot's HTTP token) and "teacher_pass" (password for entering teacher's mode) variables
5. Run "source.py"!
