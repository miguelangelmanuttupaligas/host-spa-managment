# Pasos
## Requerimientos
- Visual Studio Code
- MobaXterm
## Crear máquina virtual (Capaz de servir a X alumnos)
1vCPU, 2 GB RAM

## Instalar Nginx
```sh
sudo apt update
sudo apt install nginx
```
## Instalar NodeJS 18
```sh
sudo apt install software-properties-common apt-transport-https ca-certificates gnupg2 curl build-essential
curl -sL https://deb.nodesource.com/setup_18.x | sudo -E bash -
sudo apt install nodejs -y
```

## Subir repositorios a /home/user
### Ejecutar javascript-spa-simple
```sh
npm install
NODE_OPTIONS=--openssl-legacy-provider npm start
# Luego Ctrl + Z
# Agregar a backgroud: bg
```
### Ejecutar insta-repo-app
```sh
npm install
HOST=0.0.0.0 npm start
# Luego Ctrl + Z
# Agregar a backgroud: bg
```

### Crear interfaz de Nginx
- Subir en /home/operator los 3 archivos
```sh
sudo mv /home/operator/index.nginx-debian.html /var/www/html/
sudo mv /home/operator/spa.webp /var/www/html/
sudo mv /home/operator/static_page.webp /var/www/html/
sudo chmod 777 /var/www/html/index.nginx-debian.html
sudo chmod 777 /var/www/html/spa.webp
sudo chmod 777 /var/www/html/static_page.webp
```
> No olvidar, antes de copiar, traducir el texto

## Habilitar puertos
sudo ufw allow 9000/tcp
sudo ufw allow 3000/tcp
sudo ufw allow ssh
sudo ufw allow http
sudo ufw allow https
sudo ufw enable