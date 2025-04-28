1. Naimportovat do virtual boxu ubuntu 22.04
2. Vygenerovat ssh klíče(ssh-keygen)
3. Nakopírovat ssh párový klíč na server(ssh-copy-id)
4. Vypnutí příhlášení se na ssh server pomocí jména a hesla(edit /etc/ssh/sshd_config), parametr PasswordAuthentification nastavit na no
5. Přihlásit se přes ssh
6. "apt update"
7. "apt install phpmyadmin"
8. Configure database for phpmyadmin with dbconfig-common? [yes/no] - odpověd = no
9. Web server to reconfigure automatically: apache2(1)
    !!! reconfigure phpmyadmin příkaz "dpkg-reconfigure phpmyadmin"
10. Vyhledat modul php pro apache: "apt search apache2 | grep php"
11. "apt install libapache2-mod-php"
12. "apt install mariadb-server nebo mysql-server"
13. Vytvoření účtu do mysql serveru pro přístup tcp localhost  
    - přehlásit se jako root ("su -" nebo "sudo su -")
    - příkaz "mysql" (cli management mysql databáze)
    - "CREATE USER wordpress@localhost IDENTIFIED BY 'wordpress';"
    - "CREATE DATABASE wordpress;"
    - "GRANT ALL PRIVILEGES ON wordpress.* TO wordpress@localhost;"
    - "flush privileges;"
14. Změna adresáře "cd /var/www/html"
15. Stažení wordpressu příkaz "wget http://192.168.10.1/petrg/wordpress.zip"
16. Rozbalení zipu "unzip wordpress.zip"
17. Změna uživatele adresáře wordpress "chown www-data.www-data -R wordpress"
18. Přihlásit se přes chrome http://[server]:/wordpress

na windows

1. rozbalit slozku
2. spustime si xamp a tam zalozime databazi wordpress
3. otevru ji na googlu localhost/wordpress
4. zadam údaje, uživatelské jméno musí být to co nám umožní pracovat s databází
5. pak jsme ve wordpressu
