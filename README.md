
<p align="center">
  <a href="https://icr-evolution.com/en/" target="_blank">
    <img src="https://icr-evolution.com/wp-content/uploads/2020/11/logo-icrevolution.png.webp" alt="ICR Evolution">
  </a>
</p>

<h1 align="center">The Intelligent Contact Center (R)evolution</h1>


# SIP Call Manager Installation Script - README

Este archivo proporciona instrucciones detalladas sobre cómo usar el script para instalar el SIP Call Manager (SCM), una solución basada en Asterisk y FreePBX. Siga estas instrucciones para instalar y configurar el SCM en su sistema.

## Requisitos previos

Antes de ejecutar el script, asegúrese de que su sistema cumpla con los siguientes requisitos:

- **Sistema operativo**: Red Hat Enterprise Linux 8, AlmaLinux 8, Rocky Linux 8, Oracle Linux 8.
- **Permisos**: Necesitará acceso como usuario con privilegios de administrador (root).
- **Conectividad a Internet**: Para descargar dependencias y componentes adicionales.
- **Herramientas de desarrollo**: El script instala herramientas de desarrollo si no están presentes.
- **Aprobaciones**: Asegúrese de que tiene permiso para instalar y modificar el sistema según sea necesario.

## Uso

Para usar el script, asegúrese de que tenga permisos de ejecución. Luego, ejecútelo con el siguiente comando:

```bash
./install_asterisk18_RHEL8.sh install
```

El script también acepta varios argumentos opcionales para personalizar la instalación. Aquí está la lista de argumentos y sus usos:

- **language**: Define el idioma para la interfaz del SCM (opciones: es, en).
- **sounds**: Define el idioma para los mensajes de sonido del sistema (opciones: es, en, fr).
- **repo**: Define el tipo de repositorio para obtener el software (opciones: local, remote).
- **evoserver**: Define la dirección IP para la conexión con el servidor EVO.
- **cdr**: Habilita o deshabilita la funcionalidad de registro de CDR (opciones: enable, disable).

## Ejemplos
 - Instalar el SCM con el idioma en inglés y repositorio local:

    ```bash
    ./install_asterisk18_RHEL8.sh install --language=en --repo=local
    ```
 - Instalar el SCM y desactivar la funcionalidad de CDR:

    ```bash
    ./install_asterisk18_RHEL8.sh install --cdr=disable
    ```


## Pasos de instalación

1. **Ejecución del script**: Inicie el script como se muestra arriba.
2. **Configuraciones adicionales**: El script realizará comprobaciones de sistema y deshabilitará SELinux si es necesario.
3. **Instalación de dependencias**: El script instalará los componentes necesarios, incluyendo herramientas de desarrollo y repositorios EPEL.
4. **Compilación e instalación**: El script compilará e instalará Asterisk y FreePBX con las configuraciones necesarias.
5. **Configuraciones finales**: El script realizará configuraciones adicionales para HTTPD, PHP, y otros componentes del sistema.
6. **Reinicio del sistema**: El script reiniciará el sistema para aplicar los cambios.

## Notas adicionales

- **Respaldos**: Asegúrese de tener respaldos de cualquier dato importante antes de ejecutar el script.
- **Cambios de configuración**: Este script puede modificar configuraciones del sistema, como puertos y SELinux.
- **Información de contacto**: Para más información, visite [ICR Evolution](http://www.icr-evolution.com).

