instala

```
#!/bin/bash

# Actualizar y upgrading
apt update
apt upgrade

# Configurar almacenamiento
termux-setup-storage

# Crear archivo .hushlogin
touch .hushlogin

# Instalar paquetes
pkg install git zsh bat lsd -y

# Instalar oh-my-zsh
sh -c "$(curl -fsSL https://raw.githubusercontent.com/robbyrussell/oh-my-zsh/master/tools/install.sh)"

# Clonar powerlevel10k
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k

# Agregar powerlevel10k a .zshrc
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
```

descarga
sal y entra a termux
comando:
# Configurar powerlevel10k
comando:
```
p10k configure
```

```
#!/bin/bash

# Instalar zsh-autosuggestions
mkdir -p ~/.plugins/zsh-autosuggestions
git clone --depth 1 https://github.com/zsh-users/zsh-autosuggestions.git ~/.plugins/zsh-autosuggestions
echo "source ~/.plugins/zsh-autosuggestions/zsh-autosuggestions.zsh" >> $HOME/.zshrc

# Instalar zsh-syntax-highlighting
mkdir -p ~/.plugins/zsh-syntax-highlighting
git clone --depth 1 https://github.com/zsh-users/zsh-syntax-highlighting.git ~/.plugins/zsh-syntax-highlighting
echo "source ~/.plugins/zsh-syntax-highlighting/zsh-syntax-highlighting.zsh" >> $HOME/.zshrc

# Recargar configuración de Termux
termux-reload-settings
```
# KEYS
en la ruta
`~/.termux/termux.properties`

```
extra-keys = [['ESC','|','-', {key: HOME, display: 'INC'},'UP',{key: END, display: 'FIN'}, 'APOSTROPHE', {macro: "clear ENTER", display: '×'}],['TAB','CTRL','BACKSLASH','LEFT','DOWN','RIGHT','KEYBOARD','DEL'] ]
```

colores:
```
#!/bin/bash

# Configurar colores en ~/.termux/colors.properties
echo "# Colores" > ~/.termux/colors.properties
echo "color0=#303030" >> ~/.termux/colors.properties
echo "color1=#8B0000" >> ~/.termux/colors.properties
echo "color2=#6AEB36" >> ~/.termux/colors.properties
echo "color3=#F5B337" >> ~/.termux/colors.properties
echo "color4=#6F7CEF" >> ~/.termux/colors.properties
echo "color5=#F537C2" >> ~/.termux/colors.properties
echo "color6=#31DEEF" >> ~/.termux/colors.properties
echo "color7=#8a8a8a" >> ~/.termux/colors.properties
echo "color8=#494949" >> ~/.termux/colors.properties
echo "color9=#EE146F" >> ~/.termux/colors.properties
echo "color10=#4FDA15" >> ~/.termux/colors.properties
echo "color11=#F4C82D" >> ~/.termux/colors.properties
echo "color12=#6F6FFC" >> ~/.termux/colors.properties
echo "color13=#b03b76" >> ~/.termux/colors.properties
echo "color14=#13CDAF" >> ~/.termux/colors.properties
echo "color15=#cfcfcf" >> ~/.termux/colors.properties
echo "background=#1A1A1E" >> ~/.termux/colors.properties
echo "foreground=#d9e6f2" >> ~/.termux/colors.properties
echo "cursor=#d9e6f2" >> ~/.termux/colors.properties

# Recargar configuración de Termux
termux-reload-settings
```
