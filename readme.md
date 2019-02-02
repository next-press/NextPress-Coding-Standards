# NextPress Coding Standards

The goal of this repo is to provide the necessary sniffs for our custom coding standards, making sure that all NextPress products maintain a consitent codebase.

## Installation

### Installing PHPCS
To install our coding standards, first we need to make sure we have PHPCS installed and running on your machine. The easist way of doing this is installing it globally via Composer:
```
composer global require "squizlabs/php_codesniffer=*"
```

### Installing WordPress Coding Standards
After you install PHPCS, you need to install WordPress Code Standards. Our custom code standards rely heavily on the standarts set by WordPress, so they are a pre-requisite before you get up and running with our own CS.

To install WordPress coding standards, clone their repo on a directory of your choosing. ~/utilities, for example:
```
cd
mkdir utilities
cd utilities
git clone -b master https://github.com/WordPress-Coding-Standards/WordPress-Coding-Standards.git wpcs
```
This will place the WordPress coding standards on the wpcs directory inside your utilities folder.

### Installing NextPress Coding Standards
The procedure to install the NextPress coding standards is the same. You close this repo to your utilities folder (or other folder of your choosing):
```
cd
cd utilities
git clone -b master https://github.com/next-press/NextPress-Coding-Standards.git nextpresscs
```
This will place the NextPress coding standards on the nextpresscs directory inside your utilities folder.

### Telling PHPCS to use our newly added standards
Now that you have both WordPress CS and NextPress CS inatalled on your machine, you simply need to tell phpcs to use them. To do that, open a terminal window and run the code below:
```
phpcs --config-set installed_paths /Users/youruser/utilities/wpcs,/Users/youruser/utilities/nextpresscs
```

To confirm that the new Code Standards where installed, run:
```
phpcs -i
```
You should see WordPress-Core, WordPress-Docs, WordPress-Extra and NextPress on that list.

# Changelog

### Version 0.0.1
* Added: Initial version of the Coding Standards;