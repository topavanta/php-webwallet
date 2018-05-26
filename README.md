# php-webwallet
Веб базиран портфейл 

# Requirements
Requirements: composer, webserver with php7.2, the mynamecoin wallet and mysql.
# Installation
clone this repository into the /var/www/html(Linux) directory or in the htdocs directory(Windows, Mac); The the easiest way to install all librarys for php is running this command: <code>composer require chillerlan/php-qrcode mynamecoin/mynamecoin-walletd-rpc-php</code>.
Create a database named mynamecoin (or you have to change it in the conf.php) and a table named addresses.The table should have this format: <code>CREATE TABLE 'mynamecoin'.'addresses' ( 'id' INT NOT NULL AUTO_INCREMENT , 'address' VARCHAR(255) NOT NULL , 'privview' VARCHAR(255) NOT NULL , 'pubspend' VARCHAR(255) NOT NULL , 'privspend' VARCHAR(255) NOT NULL , UNIQUE ('id'), PRIMARY ('id')) ENGINE = InnoDB;</code>.
# Using
You are now ready to visit your webserver and do your stuff, but before that we have to start the wallet daemon. You don't have a wallet? run on terminal/cmd <code>./walletd -g -w walletname -p thestrongestpasswordeversonoonecancrackit</code> on Linux/Mac and <code>walletd.exe -g -w walletname -p thestrongestpasswordeversonoonecancrackit</code> on Windows. Have a wallet already(or generated one yet)? you'r on the target line, just run <code>./walletd -w walletname -p thestrongestpasswordeversonoonecancrackit --rpc-password thestrongestpasswordeversonoonecancrackit --daemon-address public.mynamenode.io</code> on Linux/Mac and <code>walletd.exe -w walletname -p thestrongestpasswordeversonoonecancrackit --rpc-password thestrongestpasswordeversonoonecancrackit --daemon-address public.mynamenode.io</code> on Windows.
# Be Happy
Wow you are now ready to get some users, make sure you only present stable releases to your users, test pre-releases on test-servers to avoid dependency issues! 
