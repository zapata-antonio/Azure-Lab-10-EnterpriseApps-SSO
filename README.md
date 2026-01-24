# Lab 10 — Enterprise Applications & SSO (Gallery Apps) | Microsoft Entra ID

## Contexto (por qué lo hice)
En entornos reales, el acceso a aplicaciones SaaS externas se gobierna desde **Enterprise Applications**: asignación de usuarios, visibilidad, control por grupos y experiencia de inicio de sesión.  
En este lab trabajo la parte “operativa” de IAM: **control de acceso** y **SSO**, no el registro de aplicaciones (App registrations).

## Objetivo
Centralizar y gobernar el acceso a una aplicación SaaS de galería mediante:
- Asignación **por grupos** (no asignación individual)
- Configuración de visibilidad para el usuario (**My Apps**)
- Revisión de la configuración inicial de **SSO (SAML)**

> Alcance: configuración inicial y revisión. La integración completa requiere configuración adicional en el proveedor SaaS (Oracle) y queda fuera de este lab.

---

## Tareas realizadas

### Parte A — Alta de aplicación desde galería
1. Alta de una aplicación SaaS desde la galería (**Oracle Fusion ERP**).
2. Revisión de propiedades de la aplicación empresarial.
3. Validación de parámetros básicos (Id. de aplicación, Id. de objeto, URL de acceso).

### Parte B — Control de acceso por identidad (grupos)
4. Creación de un grupo de seguridad para controlar el acceso.
5. Asignación de la aplicación empresarial al grupo.
6. Inclusión de un usuario estándar en el grupo.
7. Verificación de que el acceso se concede **por pertenencia al grupo** (gobierno escalable).

### Parte C — Visibilidad y experiencia de usuario (My Apps)
8. Configuración de **Visible para los usuarios = Sí**.
9. Validación del comportamiento en **My Apps** con usuario estándar.

> Nota: algunas apps de galería pueden no aparecer en My Apps si no existe una experiencia de inicio de sesión válida o completa, incluso estando asignadas y visibles.

### Parte D — Introducción a SSO (SAML)
10. Acceso a la sección **Inicio de sesión único**.
11. Revisión de parámetros SAML (Entity ID, Reply URL, Sign-on URL).
12. Identificación de lo necesario para una integración completa con el proveedor.

---

## Evidencias

### 01 — Aplicación creada desde galería (Enterprise Applications)
[<img src="images/01-enterprise-app.png" width="800">](images/01-enterprise-app.png)

### 02 — Propiedades de la aplicación (Visible para los usuarios / Asignación requerida)
[<img src="images/02-app-properties.png" width="800">](images/02-app-properties.png)

### 03 — Aplicación asignada a grupo (Users and groups)
[<img src="images/03-app-assigned-to-group.png" width="800">](images/03-app-assigned-to-group.png)

### 04 — Usuario dentro del grupo (Group membership)
[<img src="images/04-user-in-group.png" width="800">](images/04-user-in-group.png)

### 05 — My Apps (vista del usuario estándar)
[<img src="images/05-myapps-user-view.png" width="800">](images/05-myapps-user-view.png)

### 06 — Configuración inicial de SSO (SAML)
[<img src="images/06-sso-saml-configuration.png" width="800">](images/06-sso-saml-configuration.png)

---

## Checklist de verificación
- [x] Aplicación creada desde galería
- [x] Asignación por grupo de seguridad
- [x] Usuario obtiene acceso por pertenencia al grupo
- [x] Aplicación visible en My Apps
- [x] Configuración inicial de SSO (SAML) revisada

---

## Qué explicaría en una entrevista / a un cliente
“Centralizo el acceso a aplicaciones SaaS externas con **Enterprise Applications**, asignando acceso por **grupos** y revisando la configuración de **SSO (SAML)**. Esto permite gobernar quién accede, aplicar políticas como MFA/Conditional Access antes de llegar al SaaS y mejorar trazabilidad y control.”
