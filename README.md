# BookMedik
Sistema de Citas Medicas usando PHP, MySQL y Bootstrap.

> fork para estudio en clase

## Instalacion
* Apache2
* MariaDB
* PHP

## Configuracion de Apache2
* Configura Virtualhost
* Configura DocumentRoot

## Configuracion de MariaDB
* Crea base de datos a partir del volcado de datos `schema.sql` . Ese volcado crea un usuario admin/admin. Puedes cambiarlo en el archivo `schema.sql` o crear uno nuevo.

https://github.com/lmorillas/bookmedik/blob/efa12823abc5bbcc295f0764219db2f96a59602e/schema.sql#L20

* Crea el usuario en MariaDB para que pueda acceder a la base de datos. Y dale permisos.
```sh
$ sudo mysql -u root
MariaDB [(none)]> CREATE USER 'admin'@'localhost' IDENTIFIED BY 'admin';
MariaDB [(none)]> GRANT ALL PRIVILEGES ON bookmedik.* TO 'admin'@'localhost';
FLUSH PRIVILEGES;
```

## Dominio
Crea el nombre `bookmedik.local` en el archivo `/etc/hosts` o en windows en `C:\Windows\System32\drivers\etc\hosts` para que apunte a `localhost`.

## Acceder con navegador
Comprueba que funciona correctamente accediendo con el navegador a `http://bookmedik.local:8080` (o el puerto que hayas configurado en el `Vagrantfile`)

## Si hay errores
* comprueba el log de apache2 en `/var/log/apache2/error.log`


Link: http://evilnapsis.com/2015/08/10/bookmedik-sistema-de-citas-medicas/

### Version 2.0

- Gestion de Pacientes, Medicos
- Creacion de Citas: Asunto, Paciente, medico, Fecha, Hora, Enfermedad, Sintomas, Medicamentos, Costo
- Vista de Calendario
- Correccion de Bugs
- Integracion de Areas con Medicos
- Integracion de estado de cita y tipo de pago
- Busqueda avanzada
- Reportes por paciente, medico, rango de fecha, estado, tipo de pago
- Descarga de reporte enformato word

### Powered by Evilnapsis