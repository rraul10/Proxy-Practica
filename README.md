# Proxy-Practica

## Estructura de archivos

Creamos la siguiente estructura de archivos:

![image](https://github.com/user-attachments/assets/25123bfe-f45e-448a-b1f6-e6c1e7b250e8)

Hacemos tres contenedores uno de apache, otro de nginx y proxy. 

- Creamos una carpeta llamada `proxy` donde estará la configuración por defecto de Nginx y los certificados generados.

![image](https://github.com/user-attachments/assets/bbb46d06-b987-4dda-8516-ddd77b731755)

- En la carpeta conf `nginx.conf` se encontrara toda la configuración de proxy y toda la web de nginx.

![image](https://github.com/user-attachments/assets/e11ef0ec-ce7d-4453-a270-c17ea51266ef)

- En la carpeta `certs` pondremos los certificados generados a traves de la consola OpenSsl.

![Captura de pantalla 2024-10-27 114826](https://github.com/user-attachments/assets/72fa5ca8-b746-44b2-9085-101a8eb9a5d9)

- Creamos la carpeta `apache` donde estaran las carpetas  `htpasswd`,  `sites-available` y  `website`.

-  `Htpasswd` se encontrara el nombre de usuario y la contraseña que habremos generado con el bcrypt.

![image](https://github.com/user-attachments/assets/489136f6-ba26-4d22-b6ba-f5ee5cd37851)

- `sites-available`, dentro de `apache` crearemos  `000-default.conf` con la configuración de la web `/fernandez`, la web `/privado` dentro de esta y sus páginas de errores.

![image](https://github.com/user-attachments/assets/e8adaf08-5b54-44c0-8a9b-c2d41fcb6f67)

- Creamos carpeta `website` dentro de `apache` y dentro añadimos los dintintos HTML que formarán nuestra web `/apellido` y `/privado`. Además, añadiremos el archivo `.htaccess` con la configuración de acceso.

![image](https://github.com/user-attachments/assets/0fc6768e-bb1c-4819-a0ce-049e6dfcba7f)

- Dentro `nginx` crearemos dos carpetas que seran `sites-available` y  `website`.

![image](https://github.com/user-attachments/assets/a8da2fe7-7463-4b12-a3d8-21f56d6453ed)

- En el  `sites-available`  encontraremos dentro de `nginx` y añadimos archivo `default` con la configuración del proxy y de la web `/raul` así como sus páginas de errores.

![image](https://github.com/user-attachments/assets/bdc63b87-70b0-4026-bbde-ef4e326914cf)

- En el  `website` dentro de `nginx` y dentro añadimos los dintintos HTML que formarán nuestra web `/raul`.

![image](https://github.com/user-attachments/assets/8225774a-d380-43a9-9551-d3858d2a0384)

## Archivo hosts

![image](https://github.com/user-attachments/assets/7bb293e7-2b46-48be-816f-186bbdfb3b12)

## Pruebas en el navegador

1- Paso, generamos los contenedores.

![image](https://github.com/user-attachments/assets/3fd8cc94-2914-432d-bdf7-6444ab76aea4)

2- Buscamos proxyraul.com.

![image](https://github.com/user-attachments/assets/80d2cf5d-975b-4d85-87e4-74a84a385379)

3- Nos metemos en raul.com

![image](https://github.com/user-attachments/assets/6b983958-68cd-4d2a-9e52-65a97b82bcc3)

![image](https://github.com/user-attachments/assets/ba3de4c6-c1d8-431b-b89a-7894786d62da)

4- Ahora nos metemos en fernandez.com

![image](https://github.com/user-attachments/assets/dc1bb85e-5d9e-4757-a669-30a575edc64c)

5- Damos a area de privado.

![image](https://github.com/user-attachments/assets/6890145c-d372-42e3-85b9-c14ec473ee49)

6- En caso de error.

![image](https://github.com/user-attachments/assets/0ac7c646-014b-4322-867f-c0450cbc3879)
