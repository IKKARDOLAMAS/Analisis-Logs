### Monitoreo de Eventos y Análisis de Logs (Blue Team) 🕵️‍♂️🛡️

Hoy realicé un laboratorio de defensa activa enfocado en la detección de intentos de acceso no autorizados mediante el servicio SSH.

**Actividades principales:**
* **Simulación de Intrusión:** Generación de intentos de acceso fallidos utilizando usuarios inexistentes (`analista_falso`).
* **Análisis Forense en Tiempo Real:** Uso del comando `journalctl` para monitorear el demonio `sshd` y capturar indicadores de compromiso (IoC).
* **Identificación de Patrones:** Localización de registros de `Failed password` e `Invalid user` con sus respectivos metadatos (IP de origen y marca de tiempo).

**Evidencia de Logs Capturada:**
```text
Apr 21 14:28:39 kali sshd-session[122180]: Failed password for invalid user analista_falso from ::1 port 55686 ssh2
Apr 21 14:29:05 kali sshd-session[122180]: Failed password for invalid user analista_falso from ::1 port 55686 ssh2
