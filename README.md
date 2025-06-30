![Logo CDS](https://www.hpecds.com/assets/CDS-positive-rgb.svg)

# Requisitos para la Formación en Automatización https://github.com/cds-automatizacion/prerrequisitos

## 1. Docker Desktop o WSL Docker

### Docker Desktop (Windows)
**Docker Desktop** es una herramienta que facilita el uso de Docker en sistemas operativos como Windows. Es el método más sencillo para trabajar con contenedores Docker en tu máquina local, y a día de hoy es gratuito para uso personal. Puedes descargarlo aqui [Docker Desktop Download](https://www.docker.com/).

### Docker en WSL
Si prefieres usar **Docker** directamente en **WSL 2** (Windows Subsystem for Linux), sin necesidad de Docker Desktop, sigue estas instrucciones.

#### Instrucciones de instalación:
1.1. Instala una distribución de **WSL** (si no la tienes):
   - Abre PowerShell y ejecuta:
     ```powershell
     wsl.exe -l -o # Lista distros disponibles
     wsl --install -d Ubuntu # Instalaría la distro Ubuntu
     ```
1.2. Dentro de tu distribución instalada en WSL, sigue las [instrucciones de instalación de **Docker**](https://docs.docker.com/engine/install/)
   - Una vez instalado **Docker** añade tu usuario al grupo docker para obtener los permisos necesarios para el uso de docker.

     ```bash
     sudo usermod -aG docker $USER
     sudo service docker start
     ```
## 2. Instalación de Visual Studio Code

Usaremos **Visual Studio Code** para el desarrollo de los playbooks, se puede descargar en [https://code.visualstudio.com/](https://code.visualstudio.com//).

## 3. Clonado del repositorio con las prácticas de laboratorio

Se proporcionará un token para poder clonar el repositorio de las prácticas:
11BQJJSNI0qGN9uv7Xugoq_YGGfctmmcSsznFgf2DMS5nbkV6TgvKN8je0rN0kEmDcYPNOPXXTLtBAzZ87

## 4. Workaround para el error de locales en central
```bash
apt update
apt install locales -y
locale-gen en_US.UTF-8
locale-gen
```
