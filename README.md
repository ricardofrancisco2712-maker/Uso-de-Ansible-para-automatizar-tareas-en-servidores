# Uso-de-Ansible-para-automatizar-tareas-en-servidores


En esta practica, vamos a usar ansible para la automatizar la instalacion de aplicaciones en servidores. Como no tenemos servidores en la nube (aws, etc), usaremos docker para crear 5 servidores virtuales de ubuntu (contenedores), y luego usar ansible para realizar la automatizacion.  Necesitas tener una PC o laptop para realizar esta practica.

Usar chatgpt para indicando lo siguiente: 

1) Crear imagen (Dockerfile) de Ubuntu que tenga instalado ssh server, se cree el usuario ansible con password ansible y que con privilegios sudo sin password. (Necesitas tener docker instalado)

2) Crear el archivo docker-compose.yml con usando la imagen anterior de ubuntu y crear 5 servicios (servidores) de ubuntu. Subir los servidores con el comando "docker compose up -d"

3) Instalar ansible. Si usas windows, debes de instalar primero el WSL en la terminal con el comando "wsl --install". Esto instalara una maquina virtual de ubtuntu, en la cual ya puedes instalar ansible con el comando "sudo apt install ansible".

4) Crear el archivo inventario.ini con los nombres, las ips, usuario y clave ansible, y tambien el archivo ansible.cfg conteniendo el archivo de inventario y que ignore la advertencia de ssh.

5) Crear y ejecutar los playbooks de ansible con las instrucciones arriba mencionadas

Luego, con ansible, automatizar lo siguiente:

- Actualizar cache de APT del sistema operativo
- crear el usuario itla en cada servidor
- crear una carpeta llamada "app" 
- crear un archivo hola.txt en la carpeta app en cada servidor
- instalar la applicacion "cowsay" y "htop"  en cada servidor
