# Custom WordPress coding standards

1. Install [CodeSniffer](https://github.com/squizlabs/PHP_CodeSniffer) globally 

    `composer global require "squizlabs/php_codesniffer=*"`

2. Clone this repo, I have it in Wamp root folder which I called _standards so be sure to use that name in config below

    `git clone git@github.com:marko-stimac/Custom-Wordpress-coding-standards.git`

3. Install official Wordpress coding standards in a subfolder  

    `composer create-project wp-coding-standards/wpcs --no-dev wpcs`

3. Set path to files

    `phpcs --config-set installed_paths C:\wamp64\www\_standards\wpcs,C:\wamp64\www\_standards`

4. Set default standard

    `phpcs --config-set default_standard _standards`

5. Check for folder or files manually

    `phpcs /folderName
    phpcs page.php`

6. If you want to check all files in current directory with verbose flag

    `phpcs -v folder_name`

7. If you use VSCode install PHP CodeSniffer for Visual Studio Code and place following code in User Settings so that it automatically checks your files after save. Make sure to name it the same as you named the folder where you cloned the repo

    `"phpcs.enable": true,`\
    `"phpcs.standard": "_standards"`