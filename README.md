# Requisitos para Formación en Automatización

Este README contiene los pasos necesarios para configurar tu entorno de trabajo para una formación de automatización. Asegúrate de seguir las instrucciones cuidadosamente para tener todo listo.

## 1. Docker Desktop o WSL Docker

### Docker Desktop (Windows)
**Docker Desktop** es una herramienta que facilita el uso de Docker en sistemas operativos como Windows. Es el método más sencillo para trabajar con contenedores Docker en tu máquina local.

#### Instrucciones de instalación:
1. Dirígete a la página oficial de Docker: [Docker Desktop Download](https://www.docker.com/products/docker-desktop).
2. Descarga e instala **Docker Desktop**.
3. Sigue las instrucciones del instalador. Durante la instalación, se te pedirá activar la integración con **WSL 2**.
4. **Habilitar WSL 2**:
   - Si no tienes WSL 2 instalado, Docker Desktop te guiará para instalarlo.
   - Abre PowerShell como administrador y ejecuta el siguiente comando para habilitar la característica de WSL 2:
     ```powershell
     dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
     dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
     ```
   - Descarga el paquete de actualización del kernel de Linux para WSL 2 desde [este enlace](https://aka.ms/wsl2kernel).
   - Establece **WSL 2** como la versión predeterminada:
     ```powershell
     wsl --set-default-version 2
     ```

### Docker en WSL
Si prefieres usar **Docker** directamente en **WSL 2** (Windows Subsystem for Linux), sin necesidad de Docker Desktop, sigue estas instrucciones.

#### Instrucciones de instalación:
1. Instala **Ubuntu WSL** (si no lo tienes):
   - Abre PowerShell y ejecuta:
     ```powershell
     wsl --install -d Ubuntu
     ```
2. Dentro de tu distribución **Ubuntu** instalada en WSL, ejecuta los siguientes comandos:
   ```bash
   sudo apt update
   sudo apt install docker.io
   sudo usermod -aG docker $USER
   sudo service docker start
