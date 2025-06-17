
# 🏥 Sistema de Consultas Médicas para Clínicas Rurales

Este proyecto es un sistema distribuido orientado a facilitar la atención médica en clínicas rurales o con recursos limitados. Permite agendar citas, registrar consultas, dar seguimiento al historial clínico de los pacientes y operar en modo offline. Está compuesto por una API RESTful, una aplicación de escritorio y un módulo para pacientes.

---

## 🔧 Tecnologías utilizadas

- **Backend (API RESTful)**: ASP.NET Core
- **Frontend Escritorio (Cliente Rico)**: WPF en C#
- **Frontend Web (Pacientes)**: HTML/JS con consumo de API
- **Base de datos**: MongoDB
- **Autenticación**: JWT + hashing de contraseñas
- **Arquitectura**: Tres capas (presentación, negocio, datos)

---

## 👥 Roles y permisos

| Rol           | Acceso                                               |
|---------------|------------------------------------------------------|
| Médico        | Acceso completo a historial clínico, registro de consultas |
| Recepcionista | Gestión de citas y usuarios                          |
| Paciente      | Acceso a sus citas e historial                   |

---

## ✅ Funcionalidades principales

- **Registro de usuarios:** Alta de médicos, recepcionistas y pacientes.
- **Autenticación segura:** Validación de credenciales mediante tokens JWT.
- **Agenda médica:** Programación de citas por disponibilidad, asignación automática.
- **Consultas médicas:** Registro de síntomas, diagnóstico, tratamientos.
- **Historial clínico:** Visualización ordenada de la atención médica.
- **Módulo web para pacientes:** Consulta de próximas citas e historial.
- **Reportes médicos:** Por paciente, médico o periodo de tiempo.
- **Modo offline:** El cliente de escritorio puede operar sin conexión y sincroniza al recuperar conectividad.
- **Notificaciones:** Alertas y recordatorios de citas para pacientes y médicos.
- **Concurrencia y control de fallos:** Prevención de citas duplicadas y manejo transparente del modo offline.

---

## 📦 Estructura del repositorio

Este repositorio contiene tres submódulos:

```
MedicalSystem/
├── PacienteApp/               # Aplicación WPF para pacientes
├── ClienteConsultasMedicas/   # Aplicación WPF para médicos/recepcionistas
└── MedicalAPI/                # API RESTful (ASP.NET Core)
```

---

## 🚀 Cómo ejecutar

1. Clonar el repositorio con submódulos:

```bash
git clone --recurse-submodules https://github.com/alexdz14/MedicalSystem.git
```

2. Accede a cada submódulo y sigue las instrucciones específicas para ejecutar:

- `MedicalAPI`: Monta la base de datos, configura las variables de entorno y lanza la API.
- `ClienteConsultasMedicas`: Ejecuta la aplicación WPF desde Visual Studio.
- `PacienteApp`: Ejecuta la aplicación WPF desde Visual Studio.

---

## 🔐 Seguridad

- Tokens JWT para sesiones autenticadas.
- Cifrado de contraseñas.
- Control de acceso por roles (médico, recepcionista, paciente).
- Configuración CORS para permitir acceso controlado desde la web.
- Soporte para reconexión y sincronización de datos tras fallos de red.

---

## 📄 Documentación incluida

- Prototipos de interfaz de usuario
- Diagrama de contexto y modelo de datos
- Casos de uso por tipo de usuario
- Manual de usuario
- Documentación técnica de la API REST
- Justificación de la pila tecnológica

---

## 👨‍💻 

Desarrollado como parte del proyecto final para la EE **Tecnologías para Integración de Soluciones**, Universidad Veracruzana.

---
