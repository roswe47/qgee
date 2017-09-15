server {
        listen   80;
        server_name  phpmyadmin.domain.ru;

        access_log  /var/log/nginx/phpmyadmin.domain.ru.access.log;

        location / {
                root /usr/share/phpmyadmin;
                index index.php;
        }

        location ~ \.php$ {
                fastcgi_pass   127.0.0.1:9000;
                fastcgi_index  index.php;
                fastcgi_param  SCRIPT_FILENAME  /usr/share/phpmyadmin$fastcgi_script_name;
                include fastcgi_params;
        }
}
