Puedes usar esta descripción corta para el repositorio:

# Administración de Servicios en Linux – Apache/Nginx, Postfix y CUPS

Repositorio que documenta la implementación y configuración de diferentes servicios de red en Linux, incluyendo un servidor web HTTP, un servidor de correo SMTP y un servidor de impresión. Cada práctica contiene evidencias, configuraciones, capturas de pantalla y pruebas de funcionamiento realizadas en un entorno Linux.

Tecnologías utilizadas:

* Apache2 / Nginx
* Postfix SMTP
* CUPS (Common UNIX Printing System)
* HTML
* Linux
* Cliente Windows

El objetivo de estas prácticas es comprender la instalación, configuración y administración de servicios fundamentales utilizados en entornos empresariales y de infraestructura TI.

Y este README completo para GitHub:

# Administración de Servicios en Linux

**Autor:** Victor José De Peña Bernard
**Matrícula:** 2023-0506

## Descripción

Este repositorio contiene el desarrollo de tres prácticas enfocadas en la instalación y administración de servicios de red en sistemas Linux. Se implementaron servicios web, correo electrónico e impresión, aplicando conceptos de configuración de servidores y administración de sistemas.

---

# Práctica 1: Servidor HTTP Apache2/Nginx

## Objetivo

Instalar y configurar un servidor web HTTP utilizando Apache2 o Nginx, creando múltiples sitios web mediante Hosts Virtuales.

## Actividades Realizadas

### Website 1

Se creó un sitio web estático HTML con el siguiente contenido:

```html
<h1>Hola Mundo</h1>
```

### Host Virtual Puerto 80

Se configuró un Host Virtual escuchando en el puerto 80 para mostrar el sitio web anterior.

Características:

* Sitio principal del servidor.
* Acceso mediante navegador web.
* Respuesta HTTP correcta.

### Website 2

Se creó un segundo sitio web estático HTML mostrando:

* Nombre del estudiante
* Matrícula
* Nombre de la materia

### Host Virtual Puerto 8080

Se configuró un segundo Host Virtual escuchando en el puerto 8080.

Ejemplo de acceso:

```bash
http://IP_DEL_SERVIDOR:8080
```

## Evidencias

* Captura del sitio "Hola Mundo".
* Captura del sitio con datos personales.
* Configuración de Virtual Hosts.
* Verificación de funcionamiento desde navegador.

---

# Práctica 2: Servidor de Correo SMTP con Postfix

## Objetivo

Implementar un servidor SMTP utilizando Postfix para el envío de correos electrónicos.

## Actividades Realizadas

### Instalación de Postfix

Instalación del servicio SMTP:

```bash
sudo dnf install postfix -y
```

o

```bash
sudo apt install postfix -y
```

### Configuración del Servicio

Se configuró:

* Nombre del servidor.
* Dominio local.
* Parámetros SMTP.
* Inicio automático del servicio.

Verificación:

```bash
systemctl status postfix
```

### Envío de Correo

Se realizó una prueba enviando un correo electrónico con:

**Asunto:**

```text
MambruSeFueALaGuerra
```

**Contenido:**

```text
Nombre: Victor José De Peña Bernard
Matrícula: 2023-0506
```

## Evidencias

* Configuración de Postfix.
* Estado del servicio.
* Registro de envío.
* Confirmación de recepción del correo.

---

# Práctica 3: Servidor de Impresión CUPS

## Objetivo

Instalar y configurar un servidor de impresión utilizando CUPS y una impresora virtual PDF.

## Actividades Realizadas

### Instalación de CUPS

```bash
sudo dnf install cups -y
```

o

```bash
sudo apt install cups -y
```

Inicio del servicio:

```bash
sudo systemctl enable cups
sudo systemctl start cups
```

Verificación:

```bash
sudo systemctl status cups
```

### Configuración de Impresora Virtual PDF

Se instaló una impresora PDF virtual y se configuró dentro de la interfaz de administración de CUPS.

Acceso a CUPS:

```text
http://IP_DEL_SERVIDOR:631
```

### Compartición de Impresora

Se habilitó:

* Compartición de impresoras.
* Acceso remoto.
* Publicación en la red.

### Instalación en Cliente

Desde el equipo cliente Windows se agregó la impresora utilizando la dirección IP del servidor.

Ejemplo:

```text
http://IP_DEL_SERVIDOR:631/printers/PDF
```

### Prueba de Impresión

Se creó un documento de Microsoft Word y se envió a la impresora virtual.

Resultado:

* Conversión exitosa a PDF.
* Generación correcta del documento.
* Almacenamiento del archivo PDF en el servidor.

## Evidencias

* Configuración de CUPS.
* Impresora PDF creada.
* Cliente conectado al servidor.
* Documento Word convertido a PDF.
* Resultado final de impresión.

---

# Servicios Implementados

| Servicio          | Software        |
| ----------------- | --------------- |
| HTTP              | Apache2 / Nginx |
| SMTP              | Postfix         |
| Impresión         | CUPS            |
| Impresora Virtual | PDF Printer     |

---

# Competencias Desarrolladas

* Administración de servidores Linux.
* Configuración de servicios de red.
* Gestión de correo electrónico.
* Implementación de servidores web.
* Administración de impresión en red.
* Solución de problemas en infraestructura TI.

---

# Conclusión

Estas prácticas permitieron adquirir experiencia en la implementación de servicios fundamentales dentro de una infraestructura Linux. Se configuraron correctamente servicios web, correo electrónico e impresión, verificando su funcionamiento mediante pruebas reales y acceso desde equipos clientes.
