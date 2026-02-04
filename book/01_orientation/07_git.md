# Guía Completa: Configurar Git y GitHub desde Cero

## Para Windows

### Paso 1: Descargar e Instalar Git

1. Ve al sitio oficial de Git: [https://git-scm.com/download/win](https://git-scm.com/download/win)
2. Descarga el Standalone Installer (se descargará automáticamente)
3. Ejecuta el archivo descargado (`.exe`)
4. Durante la instalación:
   - Acepta la licencia
   - Deja las opciones por defecto (recomendado para principiantes)
   - En "Adjusting your PATH environment", selecciona **"Git from the command line and also from 3rd-party software"**
   - En "Choosing the SSH executable", deja **"Use bundled OpenSSH"**
   - Continúa haciendo clic en "Next" hasta finalizar
5. Haz clic en "Install" y luego en "Finish"

### Paso 2: Verificar la Instalación

1. Abre **PowerShell** o **Command Prompt** (CMD):
   - Presiona `Windows + R`
   - Escribe `cmd` o `powershell`
   - Presiona Enter  
2. Escribe el siguiente comando y presiona Enter:
```bash
   git --version
```
3. Deberías ver algo como: `git version 2.43.0` (el número puede variar)

### Paso 3: Configurar Tu Identidad en Git

1. En la misma terminal, configura tu nombre:
```bash
   git config --global user.name "Tu Nombre Completo"
```
   Ejemplo:
```bash
   git config --global user.name "Maria Rodriguez"
```

2. Configura tu correo electrónico (usa el mismo que usarás para GitHub):
```bash
   git config --global user.email "tuemail@ejemplo.com"
```
   Ejemplo:
```bash
   git config --global user.email "maria.rodriguez@ejemplo.com"
```

3. Verifica tu configuración:
```bash
   git config --list
```

### Paso 4: Crear una Cuenta en GitHub

1. Ve a [https://github.com](https://github.com)
2. Haz clic en **"Sign up"** (Registrarse)
3. Ingresa tu correo electrónico (el mismo que configuraste en Git)
4. Crea una contraseña segura
5. Elige un nombre de usuario
6. Verifica tu cuenta por correo electrónico
7. Completa el proceso de configuración inicial

Si todos estos comandos funcionan, ¡tu configuración está completa! 🎉

## Para macOS

### Paso 1: Instalar Command Line Tools de Xcode (Requerido)

Antes de instalar Git, necesitas instalar las herramientas de línea de comandos de Xcode:

1. Abre **Terminal**:
   - Presiona `Cmd + Espacio`
   - Escribe "Terminal"
   - Presiona Enter

2. Instala las Command Line Tools:
```bash
   xcode-select --install
```

3. Aparecerá una ventana emergente. Haz clic en **"Instalar"**

4. Acepta los términos y condiciones

5. Espera a que termine la descarga e instalación (puede tomar varios minutos)

6. Verifica la instalación:
```bash
   xcode-select -p
```
   Deberías ver algo como: `/Library/Developer/CommandLineTools`

**Nota:** Este paso instala automáticamente una versión básica de Git. Puedes verificarlo con:
```bash
git --version
```

### Paso 2: Configurar Tu Identidad en Git

1. En Terminal, configura tu nombre:
```bash
   git config --global user.name "Tu Nombre Completo"
```
   Ejemplo:
```bash
   git config --global user.name "Carlos Mendez"
```

2. Configura tu correo electrónico:
```bash
   git config --global user.email "tuemail@ejemplo.com"
```
   Ejemplo:
```bash
   git config --global user.email "carlos.mendez@ejemplo.com"
```

3. Verifica tu configuración:
```bash
   git config --list
```

### Paso 4: Crear una Cuenta en GitHub

1. Ve a [https://github.com](https://github.com)
2. Haz clic en **"Sign up"**
3. Ingresa tu correo electrónico (el mismo que configuraste en Git)
4. Crea una contraseña segura
5. Elige un nombre de usuario
6. Verifica tu cuenta por correo electrónico
7. Completa el proceso de configuración inicial

Si todos estos comandos funcionan, ¡tu configuración está completa! 🎉