# active-directory-home-lab
## 📌 1. Proyecto

- Active Directory Home Lab 05/05/2026

---

## 📌 2. Arquitectura

- Server: Windows Server 2022 (DC)
- Client: Windows 11 Pro
- Network: 192.168.122.0/24
- Tools: virt-manager, AD DS, GPO

---

## 📌 3. Implementacion

### AD Setup

- Creacion de Dominio
- Configuracion DNS
- Clientes habilitados

### Usuarios y Grupos

- Creado grupo "IT"
- Usuarios creados "Juan, Maria"

### Archivos compartidos

- SMB compartido
- Permisos NTFS vs Share 
- Carpeta compartida: `home$`
- Path: `C:\home`
- Acceso via:
    - `\\carlostech.local\home$`
- Mapeo:
    - H: mapeado al home user

### GPO

- Panel de control deshabilitado 
- Aplicado al Dominio

## 📌 4. Modelos de Permisos

- Permisos Share:
    - Usuarios Autenticados → Modify
    - Administradores → Control total
    - SYSTEM → Control Total
- Permisos NTFS:
    - Usuarios Autenticados → Modify
    - Administradores → Control total
    - SYSTEM → Control Total
---

## 📌 5. Problemas y Soluciones

- Problemas iniciales conla configuracion de IPs entre el dominio y el cliente
- Problemas iniciales con ejecución de scripts en GPO
- La carpeta personal no se creaba automáticamente
    - Solución temporal: creación manual de carpetas
- Aprendizaje clave sobre:
    - diferencia entre acceso por IP vs nombre de dominio
    - importancia del DNS en Active Directory
    - relación entre GPO, permisos y ejecución de scripts

---

## 📌 6. Que he aprendido

- Active Directory depende completamente de DNS
- Las GPO deben aplicarse correctamente según OU
- Los permisos SMB y NTFS deben estar alineados
- Las carpetas personales pueden gestionarse manual o automáticamente
