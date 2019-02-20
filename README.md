# Assignment 1

WordPress Installation:
1. Install PHP
    1. [Download Visual C++ Redistributable for Visual Studio 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48145)
        1. Scroll to and click red download button
        2. Select an option according to your system and click "next"
        3. Your download will start. When finished, click it and follow its instructions
    2. [Download PHP](https://windows.php.net/download/)
        1. Click on the "Zip" link according to your system
        2. Your download will start. When finished, extract its contents into your "C:\PHP7" directory
    3. Create and configure your "php.ini" file
        1. In your "C:\PHP7" directory, create a file named "php.ini"
        2. Find a file named "php.ini-development" and copy its content into your "php.ini" file
        3. Edit "php.ini" file
            1. edit "memory_limit" from "128M" to "1G"
            2. edit "max_execution_time" to at least "90"
            3. uncomment (delete the ;) the following lines:
                - ; extension_dir = "ext"
                - ; extension=php_gd2.dll
                - ; extension=php_curl.dll
                - ; extension=php_mbstring.dll
                - ; extension=php_openssl.dll
                - ; extension=php_pdo_mysql.dll
                - ; extension=php_pdo_sqlite.dll
                - ; extension=php_sockets.dll
                - ; extension=php_mysqli.dll
    4. Add "C:\PHP7" to your Windows system path
        1. Open your "System Control Panel"
        2. Click "System"
        3. On the left side, click "Advaced system settings"
        4. By the bottom, click "Environment Variables"
        5. Under the "System variables" section find and click on the "Path" row
        6. Click "edit..." button
        7. Click "New" button and add "C:\PHP7"
        8. Lastly, click "OK" until you can exit your Control Panel
    5. Check if PHP installation is successful
        1. Open your "Command Prompt" and type "php -v"
        2. You should see your PHP version along with other data
2. Install Composer
    1. [Download Composer](https://getcomposer.org/download/)
        1. Click "Composer-Setup.exe" link and your download will start
        2. When finished, run it and follow its instructions
        3. If the install wizard asks for permission to edit your "php.ini" file, give it
        4. Check if Composer installation is successful
            1. Reopen your "Command Prompt" and type "composer"
            2. You should see a text graphic, a list of help options, and a list of commands
3. Install MySQL Server
    1. [Download MySQL Installer](https://dev.mysql.com/downloads/installer/)
        1. Scroll down to find the 16.4M version and click the "Download" button
        2. You can click login, sign up, or skip
        3. Your download will start. When finished, run it
    2. MySQL Installer
        1. Agree to permissions and its License Agreement. Click "Next"
        2. Select "Server only" and click "Next"
        3. Click "Execute" and your installation will start. When finished, click "Next" and "Next" again
        4. Then select "Standalone MySQL Server / Classic MySQL Replication" and click "Next", "Next", and "Next" again
        5. For "MySQL Root Password" use "password" and click "Next" and "Next" again
        6. Click "Execute" and, when finished, "Finished"
        7. Click "Next" and "Finish"
4. Create a database
    1. In PHP Storm, click on the "Database" tab located on the right most column of the IDE
    2. Click on the plus icon to dropdown its options
    3. Hover over "Data Source" and click "MySQL"
    4. For "User", type "root", for "Password", type "password", and for "Port", make sure it is "3306"
    5. Before clicking "Apply" or "Okay", click on "Download missing driver files"
    6. Then click "Apply" and "Okay"
    7. Enter these commands into the SQL command window
        1. CREATE DATABASE wordpress;
        2. CREATE USER 'YOURNAME'@'wordpress' IDENTIFIED WITH mysql_native_password BY 'YOURPASSWORD';
        3. GRANT ALL PRIVILEGES ON wordpress.* TO 'YOURNAME'@'wordpress';
        4. FLUSH PRIVILEGES;
    8. You can use this command to check your database
        - SHOW DATABASES;
5. Install WordPress
    1. [Download WordPress](https://wordpress.org/download/)
        1. Click the "Download WordPress 5.0.3" button
        2. Your download will start. When finished, extract the files into your PHP Storm project directory "PHPstormProjects"
    2. Configure your "wp-config.php" file
        1. Open the extracted directory in PHP Storm, located in "PHPstormProjects", and create a new file named "wp-config.php"
        2. Find the file "wp-config-sample.php" and copy its content into the file named "wp-config.php"
        3. Open and edit the "wp-config.php" file's "MySQL settings" such as the database name, user name, and password
    3. Add Configuration
        1. In PHP Storm, click on "Add Configuration..."
        2. Click on the plus icon to dropdown its options
        3. Click on "PHP Built-in Web Server"
        4. Click "Apply" and "Okay"
    4. Enable "WordPress Support" to get better error messages
        1. This is enabled by default
        2. If disabled, go to "Plugins settings" and enabled it there
6. Run the server
    1. Click on "Run" button, located next to the "Add Configuration..." button
    2. Open your browser and type "localhost" as the URL
    3. The WordPress account creator should display and create an account
    4. If an error is displayed, your can check if you are using the correct "php.ini" file
        1. Create a "test.php" file in your wordpress directory
        2. In "test.php", echo the function called "phpinfo()"
        3. Then in your browser type "localhost/test.php" to see where "php.ini" is being loaded
        
# How to work collaboratively on GitHub with Team
This Tutorial based on PHPStorm. How you can use GitHub on PHPStorm to collaborate with your teammates to work on a project.
After creating a repository, the owner of the repository have to add collaborator to the repository. In order to add collaborator to a repository, Go to settings and select "Collaborators" for left panel and add collaborator.
Here some tips and tricks how you can collaborate on a project on GitHub.

1.First of all you have to clone the repository in your localhost. You will get all the code of the repository. You ca edit the code.

2. After making every change you have to commit to github. Commit is basically details comments what you have change.

3. Push the code to github. the way the code will appear on github.

4. If you work on a new feature always creat new branch to work on it. By creating new branch you will work on copy version of the code, not on the master code. if you made any mistake that will only affect on the brach you working on

5. If the code of new branch works perfect you can push to the github or marge on to the master branch
