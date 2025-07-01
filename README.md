# 📚 Aplicación Spring Boot, JDBC y MySQL en Docker

Este proyecto es una aplicación Java usando **Spring Boot** y **JDBC** que se conecta a una base de datos **MySQL** dentro de un contenedor Docker. Su objetivo es demostrar cómo se puede crear, insertar y consultar datos desde una tabla `customers`.

---

## 🧠 Marco Teórico

### 🔹 ¿Qué es JDBC?
JDBC (Java Database Connectivity) es una API de Java que permite a las aplicaciones Java interactuar con bases de datos relacionales como MySQL. Proporciona métodos para conectar, ejecutar consultas y procesar resultados.

### 🔹 ¿Qué es Spring Boot?
Spring Boot es un framework que simplifica el desarrollo de aplicaciones Java basadas en Spring. Permite configurar proyectos rápidamente con dependencias preestablecidas, y facilita la creación de aplicaciones web, REST, y conexión con bases de datos.

### 🔹 ¿Qué es Docker?
Docker es una plataforma que permite crear, desplegar y ejecutar aplicaciones dentro de contenedores. Un contenedor es una unidad aislada con todo lo necesario para ejecutar una aplicación, incluyendo el sistema de archivos, dependencias y configuración.

---

## 📁 Estructura de Archivos

### ✅ `Customer.java`
Define el modelo Customer, que representa un cliente con id, firstName y lastName. Contiene constructor, getters, setters y un toString() que facilita la impresión legible de los datos.

### ✅ `JdbcApplication.java`
Clase principal de la aplicación. Al iniciar, crea la tabla `customers` si no existe, inserta registros de ejemplo usando `JdbcTemplate.batchUpdate`, y luego realiza una consulta filtrada por nombre (`first_name = 'Josh'`). Implementa `CommandLineRunner` para ejecutar esta lógica al arrancar la aplicación.

### ✅ `application.properties`
Archivo de configuración que define los parámetros de conexión a la base de datos (URL, usuario, contraseña, driver JDBC). También contiene configuraciones específicas de Spring Boot, como el puerto del servidor y el comportamiento ante definiciones duplicadas de beans.

### ✅ `docker-compose.yml`
Archivo de orquestación de Docker que define el servicio de base de datos MySQL. Crea un contenedor llamado `estudiante_mysql`, define el usuario root y la base de datos `estudiantes_db`, expone el puerto 3306 y utiliza un volumen persistente para guardar los datos.

---

## ▶️ Instrucciones de Uso

1. Iniciar Docker
2. Levantar el contenedor MySQL
3. Verificar contenedor activo
4. Ejecutar la aplicación de Spring-boot
5. Ver salida en consola

---

## 📸 Capturas de Pantalla

![image](https://github.com/user-attachments/assets/4177c577-ab26-42de-8bf4-31c98adc56c5)

