# **Resumen Clase 2**

En la segunda clase el profesor nos enseño a instalar docker y docker compose.

para esto lo hicimos en ubuntu conectandonos por ssh a nuestras maquinas.

- Primero 
>sudo apt-get update 

para actualizar los repositorios del sistema
- Instalamos dependecias necesarias con  
>sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    gnupg \
    lsb-release.
- Agregamos la llave de Docker con el siguiente comando 
>curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg.
- Descargamos Docker con el siguiente comando 
>echo \ "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \$(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
- Docker se instala con
>sudo apt-get update 
>sudo apt-get install docker-ce docker-ce-cli containerd.io
- Una vez instalado podemos probarlo con 
>sudo docker run hello-world

Ahora procedemos con la instalacion del Docker Compose

- ejecutamos el siguiente comando 
>curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose.
- luego 
>sudo chmod +x /usr/local/bin/docker-compose.
- y por ultimo clonamos el repositorio donde esta la aplicacion 
>git clone https://github.com/jsgiraldoh/Codimd.git
