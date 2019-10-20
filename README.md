## Reset MySQL Root Password Ubuntu
Open up terminal and execute the following commands depending on the version installed

**MYSQL-SERVER >= 5.7**

 1. sudo mysql -u root -p 
 2. USE mysql; 
 3. UPDATE user SET authentication_string=PASSWORD('YOUR_PASSWORD') WHERE User='root';
 4. UPDATE user SET plugin="mysql_native_password"; 
 5. FLUSH PRIVILEGES;
 6. quit;

**MYSQL-SERVER < 5.7**

 1. List item
 2. sudo mysql -u root -p
 3. USE mysql;
 4. UPDATE user SET password=PASSWORD('YOUR_PASSWORD') WHERE User='root';
 5. UPDATE user SET plugin="mysql_native_password";
 6. FLUSH PRIVILEGES;
 7. quit;
