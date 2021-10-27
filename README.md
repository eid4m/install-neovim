### Acerca de:

------------



- Todos los recursos necesarios estaran aquí, sin necesidad de abrir otras páginas.
- Los Plugins y temas más conocidos igualmente se encontrarán aquí.

- Markdown Extras : Support ToC (Table of Contents), Emoji, Task lists, @Links...;
- Compatible with all major browsers (IE8+), compatible Zepto.js and iPad;
- Support identification, interpretation, fliter of the HTML tags;
- Support TeX (LaTeX expressions, Based on KaTeX), Flowchart and Sequence Diagram of Markdown extended syntax;
- Support AMD/CMD (Require.js & Sea.js) Module Loader, and Custom/define editor plugins;

# Instalar Vim/Neovim

![](https://stsewd.dev/images/nvim/neovim-logo.png)



**Table of Contents**



##Recursos
- Git
- Node.js
- Chocolatey
	- Windows 7+ / Windows Server 2003+
	- PowerShell v2+ (minimum is v3 for install from this website due to TLS 1.2 requirement)
	- .NET Framework 4+ (the installation will attempt to install .NET 4.0 if you do not have it installed)(minimum is 4.5 for install from this website due to TLS 1.2 requirement)

##Instalar los recursos
- Descargue e instale Git desde [aquí](http://git-scm.com/ "aquí").
- Descargue e instale Node.js en la [versión LTS](http://nodejs.org/es/ "versión LTS").
- Descargue el Windows Terminal desde [Microsoft Store](http://www.microsoft.com/en-us/p/windows-terminal/9n0dx20hk701?activetab=pivot:overviewtab "Microsoft Store").

###Instalar Chocolatey

Instale el administrador de paquetes Chocolatey ejecutando el siguiente código desde el Windows PowerShell **(Administrador)**:

    Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
	
#Instalar  Neovim
- Una vez instalado los recursos continuaremos a instalar el edito de código.
- Abrimos Windows PowerShell y ejecutamos el siguiente código:


    choco install neovim
	
Para instalar la versión pre-release

    choco install neovim --pre

##Configurar Neovim
###Verificar el archivo init.vim

Diríjase a `C:\Users\YourUser\AppData\Local`, ahí debe haber una carpeta nombrada "nvim", aparte de "nvim-data", si no está creela y dentro de dicha carpeta cree el archivo `init.vim` y abrelo con un editor de texto, copie y pque el siguiente [código](http://github.com/EduarCuri/my_init.vim/blob/master/init.vim "código"):
###Instalar vim-plug

- En Windows PowerShell **(Administrador)**, ejecute el siguiente código:


    iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
        ni "$(@($env:XDG_DATA_HOME, $env:LOCALAPPDATA)[$null -eq $env:XDG_DATA_HOME])/nvim-data/site/autoload/plug.vim" -Force
    
	
###Primer inicio de Neovim

Abrimos el Windows Terminal y debemos abrir el archivo "init.vim" para aplicar todos los plugins pre-instalados en dicho archivo.
- Diríjase a la siguiente dirección: `C:\Users\YourUser\AppData\Local\nvim`.
- Ejecute el siguiente código para abrir el archivo con neovim:


    nvim init.vim


> Donde "nvim", se usa para abrir el edito de código en sí y "init.vim", en este caso de ejemplo se usa para abrir el archivo o carpeta.


###Aplicar la instalación de Plugins

Una vez dentro de neovim damos `Enter`, y nos aparecerá el código del archivo init.vim.
- Luego tipeamos `:` , y automáticamente nos mandará a la linea de abajo y escribimos el siguiente comando: `PlugInstall` y damos **Enter.**

Y los plugins deben instalarse automaticamente.
- Reiniciamos neovim de la siguiente manera:
- Tipeamos `:`  y **q**
- Luego tipeamos `:`  y **wq** para aplicar los cambios.

Volveremos al Windows Terminal y volveremos a ejecutar el comando:

    nvim init.vim
	
Y ya veremos los cambios aplicados y a Neovim con una **nueva apariencia.**
