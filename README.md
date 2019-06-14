


# Instalación y Configuración de PHP
Pasos para instalar y configurar **PHP** junto con **Apache**

## Descarga
1. Vaya al sitio oficial de **PHP [aquí]([https://windows.php.net/download](https://windows.php.net/download))**
2. Seleccione el link con la *version y distribución adecuada para su computadora* de **PHP** (Nosotros usamos la thread safe binaries).
3. **Extraiga** el archivo descargado en el *directorio raiz que se adapte a sus necesidades* (Nosotros usamos el directorio **C:/**)

## Instalación
***PHP*** no se instala, esta compuesto por un conjunto de archivos binarios que permiten interpretar la sintaxis de ***PHP***

## Configuración
***PHP*** posee un archivo de configuración cuyo nombre es php.ini y que podrás encontrar en el directorio de instalación de ***PHP***.

Debemos editar nuestro archivo de configuración de Apache, llamado **`httpd.conf`** agregando las siguientes líneas . 

**`AddHandler application/x-httpd-php .php  
AddType application/x-httpd-php .php .html  
LoadModule php7_module "c:/php/php7apache2_4.dll"  
PHPIniDir "c:/php7"`**

Debemos añadir un par de líneas de configuración del módulo de Apache.

Agregue al directorio de apache un archivo llamado **`info.php`** con el siguiente código:
**`<?php phpinfo(); ?>`**
**En el navegador web** navegue a la url **`localhost/info.php`** para verificar que **PHP** es interpretado y bien configurado.

[**Ver cómo configurar APACHE**](https://github.com/bitcubico/apache-install-config-win/blob/master/README.md)
