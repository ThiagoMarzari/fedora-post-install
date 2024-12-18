# fedora-post-install


## Atualizar sistema
- `sudo dnf -y update`
- Reiniciar pc

## Instalar o RPM Fusion
- `sudo dnf install https://mirrors.rpmfusion.org/free/fedora/rpmfusion-free-release-$(rpm -E %fedora).noarch.rpm https://mirrors.rpmfusion.org/nonfree/fedora/rpmfusion-nonfree-release-$(rpm -E %fedora).noarch.rpm`
- `sudo dnf group upgrade core`

## Instalar drivers da nvidia
`
sudo dnf update
sudo dnf install akmod-nvidia
sudo dnf install xorg-x11-drv-nvidia-cuda
`

## Codecs 
`sudo dnf swap 'ffmpeg-free' 'ffmpeg' --allowerasing # Switch to full FFMPEG.
sudo dnf4 group upgrade multimedia
sudo dnf update @multimedia --setopt="install_weak_deps=False" --exclude=PackageKit-gstreamer-plugin # Installs gstreamer components. Required if you use Gnome Videos and other dependent applications.
sudo dnf update @sound-and-video # Installs useful Sound and Video complement packages.`

## Instalar programas para jogos
`
sudo dnf install steam -y
flatpak install flathub com.heroicgameslauncher.hgl
`

## Instalar aplicativos gerais
`
flatpak install flathub com.spotify.Client
flatpak install flathub org.gnome.Boxes
flatpak install flathub com.obsproject.Studio
flatpak install flathub com.rtosta.zapzap
flatpak install flathub com.todoist.Todoist
`
