# Домашнее задание: Первые шаги с Ansible
Подготовить стенд на Vagrant как минимум с одним сервером. На этом сервере используя Ansible необходимо развернуть nginx со следующими условиями:
-    необходимо использовать модуль yum/apt;
-    конфигурационные файлы должны быть взяты из шаблона jinja2 с перемененными;
-    после установки nginx должен быть в режиме enabled в systemd;
-    должен быть использован notify для старта nginx после установки;
-    сайт должен слушать на нестандартном порту - 8080, для этого использовать переменные в Ansible.

# Выполнение
Из приложенного Vagrantfile разворачиваем виртуальную машину с установленным Nginx, соответствующим заданным условиям.

Проверяем работоспособностьd в браузере или терминале:

```bash

vagrant@ubuntu-focal:~$ curl localhost:8080
<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
    body {
        width: 35em;
        margin: 0 auto;
        font-family: Tahoma, Verdana, Arial, sans-serif;
    }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>
```
