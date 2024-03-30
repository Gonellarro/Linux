# Apps i confs post instal·lació
## Install vulkan-tools Using apt
Update apt database with apt using the following command.
```bash:
sudo apt update
```
After updating apt database, We can install vulkan-tools using apt by running the following command:
```bash:
sudo apt -y install vulkan-tools
```
> Font: [Installati.one](https://installati.one/install-vulkan-tools-ubuntu-22-04/?expand_article=1)

## Instal·lar Retoques i Gnome Extensions Manager(tweaks)
```bash:
sudo apt install gnome-tweaks
sudo apt install gnome-shell-extension-manager
```

Instal·lar com extensions:
- Applications menu
- User themes

### Personalització temes i icones

- Descarregar de [Gnome Look](https://www.gnome-look.org/browse?cat=135&ord=rating) els temes que vulguem   
- Descarregar de [Gnome Look](https://www.gnome-look.org/browse?cat=132&ord=rating) les icones que vulguem

Un cop descarregats, per instal·lar cada apartat, només els hem de copiar a les carpetes corresponents.

- Copiar la carpeta de tema a /usr/share/themes
- Copiar la carpeta d'icones a .icons

Anam a Retoques i sel·leccionam el tema que volem, les icones que volem i el shell que volem (configura també l'aparença del dock)

### Personalització terminal
- Obrir un terminal 
- Anar a Preferecies
- Crear un nou perfil
- Anar a Texte
- Canviar tipologia predeterminada a font 14
- Anar a colores
- Canviar per l'esquema "Tango oscuro"

## Instal·lació de git, zsh, ohmyzsh i power10K
```bash:
sudo apt install git
sudo apt install zsh
zsh --version
chsh -s /bin/zsh
grep "^${USER}" /etc/passwd
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
nano ~/.zshrc
```
- Canviar ZSH_THEME per "powerlevel10k/powerlevel10k"
- Instal·lar les fonts [Meslo Nerd](https://github.com/romkatv/powerlevel10k/blob/master/font.md)
- Anar a les preferències del terminal, perfil Martí, Texto i canviar la tipografia a Meslo Nerd
```bash:
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

Sortim i tornam a entrar al terminal i es posa en marxa la configuració de powerlevel10. Feim la configuració al nostre gust.

Si no ens queda com volem, podem tornar a configurar-ho executant "pk10 configure"

### Configurar plugins: 
```bash:
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
nano ~/.zshrc
```
Afegim els plugins a la llista:

```yaml:
plugins=( 
git
zsh-syntax-highlighting
zsh-autosuggestions
)
```

>Font: [Dev.to](https://dev.to/christopherjael/como-personalizar-tu-terminal-utilizando-oh-my-zsh-con-powerlevel10k-4bdi)




