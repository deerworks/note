# dockerコンテナでApache2＋PHP環境の作成

## 使用するdockerコンテナ

ubuntu/apache2

## PHPの導入

1. apt update
1. apt upgrade
1. apt install apt install php php-cgi php-pear php-mbstring php-mysql php-imagick php-curl php-zip php-int
1. cd /etc/php/8.1/mods-available
1. tee /etc/php/8.1/mods-available/my.php.ini <<"EOF"
; configuration for php my.php module
; priority=90
date.timezone = "Asia/Tokyo"
EOF
1. phpenmod my.php
2. 2enconf php8.1-cgi
3. service apache2 reload