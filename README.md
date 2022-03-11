# Instalación
Para instalar el repository junto a la ui simplemente hay que copiar el archivo `.env.example` a `.env` y rellenar con los 
datos de configuración de tu entorno

## Auth htaccess
Si se desea autenticación con htaccess en el registry se pueden seguir estos pasos

1. instalar localmente las apache utils 
`sudo apt install apache2-utils`
2. Crear dentro de la carpeta auth un archivo con nombre `registry.password` con el usuario y las credenciales, para hacerlo utilizar el comando
`htpasswd -Bc registry/auth/registry.password username`
3. Tener en cuenta esas credenciales para informarlas en las variables de entorno `REGISTRY_USERNAME` Y `REGISTRY_PASSWORD`.
4. Por último levantar el docker en el entorno que se prefiera
`docker-compose -f docker-compose.local.yml up -d`

