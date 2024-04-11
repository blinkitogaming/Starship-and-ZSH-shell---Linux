# Starship shell - Linux

## Description
Puesta en marcha y configuración de la terminal Starship y ZSH para Linux.

### Pre-requisitos
Instalar una fuente de Nerd Font.

Para ello:

- visita el sitio: https://www.nerdfonts.com/font-downloads

- Elige una fuente.

- Descarga la fuente y descomprime el archivo .ZIP en la ruta: /usr/share/fonts

- Recarga el caché con el siguiente comando:
    
    fc-cache -f -v

### Paso 1 - Instala Starship
    
    curl -sS https://starship.rs/install.sh | sh

### Paso 2 - Instala ZSH

    sudo apt install zsh

Verifica la instalación con el comando:

    zsh --version

Deberías tener un resultado como este indicando tu versión instalada:

    zsh 5.0.8

### Paso 3 - Clona el repositorio
El repositorio tiene la estructura de directorios y archivos necesarios para que funcione.

Son los siguientes:

.zshrc (configuración de ZSH. En él se hace referencia al archivo functions.zsh, a la configuración de starship.toml e introduce la variable que hace que se use por defecto la terminal de Starship: *eval "$(starship init zsh)"*)

/.zsh/
    functions.zsh (tiene funciones, de prueba viene una que invoca un mapa de colores con sus códigos para usar en ZSH. Puedes invocarlo con el comando 'colormap')
    starship.toml (archivo de configuración de la terminal de Starship)

### Paso 4 - Reinicia tu terminal
Sal de la terminal y vuelve a abrir una nueva. Verás que ha cambiado por completo tanto en su estructura como en colores.