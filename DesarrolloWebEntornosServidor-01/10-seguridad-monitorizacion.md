- [10. Conceptos Clave de Seguridad y Monitorización](#10-conceptos-clave-de-seguridad-y-monitorización)
    - [10.1. Seguridad en Servidores Web (Autenticación HTTP Basic/Digest, Control de Acceso)](#101-seguridad-en-servidores-web-autenticación-http-basicdigest-control-de-acceso)
    - [10.2. Monitorización con Archivos de Registro (Logs CLF, Rotación de Logs)](#102-monitorización-con-archivos-de-registro-logs-clf-rotación-de-logs)

# 10. Conceptos Clave de Seguridad y Monitorización

## 10.1. Seguridad en Servidores Web (Autenticación HTTP Basic/Digest, Control de Acceso)

La seguridad es un pilar fundamental. No basta con que funcione, debe ser seguro.

*   **Autenticación**: ¿Quién eres?
    *   **HTTP Basic**: Usuario/Contraseña en Base64. ⚠️ **Inseguro** si no va por HTTPS (se lee fácil).
    *   **Digest**: Envía un hash, no la contraseña. Algo mejor.
    *   **Token (JWT)**: Lo moderno para APIs.
*   **Autorización**: ¿Qué puedes hacer?
*   **Control de Acceso**: Restringir por IP o carpeta.
    *   En Apache: `.htaccess` o `Require ip 192.168.1.50`.

### 🛂 Analogía: El Pasaporte y la Pulsera del Hotel

*   **Autenticación (Pasaporte)**: Demuestras quién eres en el mostrador del hotel. Te validan y te dan acceso.
*   **Autorización (Pulsera TI)**: Una vez dentro, la pulsera dice qué puedes hacer. ¿Tienes la pulsera "Todo Incluido" (Admin) o la "Solo Desayuno" (User)? Puedes ser Obama (Autenticado), pero si no tienes la pulsera VIP (Autorizado), no entras a la zona VIP.

## 10.2. Monitorización con Archivos de Registro (Logs CLF, Rotación de Logs)

Los **Logs** son la caja negra del avión. Si algo falla, mira los logs.
*   **Access Log**: Quién entra, qué pide, código de estado (200, 404).
*   **Error Log**: Por qué falla el servidor (PHP Error, configuración mal, etc.).
*   **Formato CLF**: Estándar (`IP - User - Fecha - "GET /path" - 200 - Size`).

**Rotación de Logs (`logrotate`)**:
Los logs ocupan espacio. La rotación consiste en:
1.  Archivar el log actual (`access.log` -> `access.log.1`).
2.  Comprimir los antiguos (`access.log.2.gz`).
3.  Borrar los muy antiguos.
Si no rotas, ¡el disco duro se llena y el servidor se cae!

![img](/images01/log.jpg)

💡 **Tip del Profesor**: Cuando algo no funcione en clase, lo primero que te diré es: **"¿Qué dice el log?"**. Acostúmbrate a leer `/var/log/apache2/error.log` (o equivalente).