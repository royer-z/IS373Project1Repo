# Assignment 1

WordPress Installation:
1. Install PHP
    1. [Download Visual C++ Redistributable for Visual Studio 2015](https://www.microsoft.com/en-us/download/details.aspx?id=48145)
        1. Scroll to and click red download button
        2. Select an option according to your system and click next
        3. Your download will start. When finished, click it and follow its instructions
    2. [Download PHP](https://windows.php.net/download/)
        1. Click on the Zip link according to your system
        2. Your download will start. When finished, extract its contents into your C:\PHP7 directory
    3. Create and configure your php.ini file
        1. In your C:\PHP7 directory, create a file named php.ini
        2. Find a file named php.ini-development and copy its content into your php.ini file
        3. Edit php.ini file
            1. edit memory_limit from 128M to 1G
            2. edit max_execution_time to at least 90
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
    4. Add C:\PHP7 to your Windows system path
        1. Open your System Control Panel
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