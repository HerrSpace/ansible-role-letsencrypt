
* Include the following where you think appropriate to your Nginx tasks.
``` YAML
- name: Run letsencrypt/nginx.yml
  include_role:
    name: letsencrypt
    tasks_from: nginx
```

* Add `include /etc/nginx/snippets/lets-encrypt.conf;` to your nginx sites.
* Add something like this to your vars:
``` YAML
letsencrypt_email: h.acker@example.com
letsencrypt_webroot_dir: /mnt/data/www/acme-challenges/
letsencrypt_cert_domains:
  mail.example.com:
    - imap.example.com
    - smtp.example.com
  example.com:
    - www.example.com
```

* ???
* Profit
 
