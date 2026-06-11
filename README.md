# base-de-datos

documento: https://github.com/muntanermatias-cloud/base-de-datos/blob/main/Documento.pdf

codigo: https://github.com/muntanermatias-cloud/base-de-datos/blob/main/codigo-supabase.txt

# Supabase vs SQLime: Características, Ventajas y Desventajas

Este repositorio contiene una investigación comparativa detallada entre **Supabase** y **SQLime**, desarrollada para la asignatura de **Base de Datos I** en la **Universidad de Belgrano**.

## 📝 Descripción del Proyecto

El proyecto analiza dos herramientas fundamentales en el ecosistema actual de bases de datos:
- **Supabase:** Una plataforma de desarrollo backend completa basada en PostgreSQL [1, 2].
- **SQLime:** Un entorno de práctica (playground) basado en el navegador para SQLite [3, 4].

## 🚀 Supabase: El Backend como Servicio (BaaS)

Supabase se define como la alternativa de código abierto a Firebase [5]. Su arquitectura se apoya en **PostgreSQL**, permitiendo a los desarrolladores centrarse en el frontend mientras la plataforma gestiona la infraestructura [1, 6].

### Ventajas Principales [6-13]
- **Velocidad de desarrollo:** Reduce tiempos de meses a días al entregar infraestructura ya optimizada.
- **PostgreSQL nativo:** Ofrece la potencia y confiabilidad de un estándar industrial de más de 30 años.
- **Sin Vendor Lock-in:** Al ser código abierto, permite la migración a servidores propios en cualquier momento.
- **Seguridad RLS:** Implementa *Row Level Security* (Seguridad a Nivel de Fila) de forma nativa.
- **Escalabilidad elástica:** Diseñado para manejar picos masivos de tráfico automáticamente.

### Desventajas [14-22]
- **Rigidez estructural:** Al ser relacional, requiere una planificación de datos estricta desde el inicio.
- **Curva de aprendizaje:** El manejo de políticas de seguridad (RLS) puede ser complejo y afectar el rendimiento si se diseña mal.
- **Costos variables:** Los planes de pago escalan según el consumo de recursos, lo que puede generar facturas inesperadas.

---

## 🍋 SQLime: El Simulador de SQLite

SQLime es una herramienta web diseñada para simplificar el aprendizaje y la experimentación con bases de datos **SQLite** sin necesidad de instalaciones locales [3, 23].

### Ventajas Principales [24-30]
- **Acceso instantáneo:** Cero configuración; funciona directamente en Chrome, Safari o Firefox.
- **Entorno Sandbox:** Ejecución local en la memoria del navegador (WebAssembly), lo que lo hace 100% seguro contra errores destructivos.
- **Privacidad:** Permite importar archivos `.db` o `.sqlite` y procesarlos localmente sin enviar datos a internet.
- **Colaboración:** Facilidad para compartir consultas a través de Gists de GitHub.

### Desventajas [31-37]
- **Sin persistencia:** Los datos son volátiles; se pierden al refrescar o cerrar la pestaña si no se exportan.
- **Incapacidad multiusuario:** No permite el trabajo colaborativo en tiempo real sobre la misma base.
- **Limitación de rendimiento:** Colapsa con bases de datos gigantescas al depender de la RAM del dispositivo local.

---

## 📊 Comparativa Rápida [38]

| Característica | SQLime | Supabase |
| :--- | :--- | :--- |
| **Motor de BD** | SQLite | PostgreSQL |
| **Entorno** | Navegador Web | Plataforma Cloud |
| **Autenticación** | No | Sí |
| **APIs Automáticas** | No | Sí |
| **Tiempo Real** | No | Sí |
| **Escalabilidad** | Baja | Alta |
| **Uso Principal** | Aprendizaje y pruebas | Desarrollo de aplicaciones |

---

## 💻 Ejemplos de Consultas (DQL)

### En Supabase (SQL estándar) [39]
```sql
SELECT nombre, email
FROM usuarios
WHERE activo = true;
En SQLime (SQLite)
SELECT name, department, salary
FROM employees
WHERE department = 'IT';
