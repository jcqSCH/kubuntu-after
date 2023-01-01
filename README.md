# KUBUNTU 22.04.1 LTS: after install
🧐 Things to do after installing Kubuntu Operating System. <br/>
✅ Tested version: Kubuntu 22.04.1 LTS <br/>
⏬ https://kubuntu.org/alternative-downloads/

<br/>

## 1 ➜ DOWNLOAD .DEB PACKAGES
**VS Code:** https://code.visualstudio.com/download/ <br/>
**PowerShell:** https://github.com/PowerShell/PowerShell#get-powershell <br/>
**Google Chrome:** https://www.google.com/chrome/browser/desktop/ <br/>
**WPS Office:** https://www.wps.com/pt-BR/office/linux/ <br/>
**Spotify:** https://www.spotify.com/br/download/linux/ <br/>
**OpenRGB:** https://openrgb.org/releases.html

<br/>

## 2 ➜ RUN COMMANDS IN TERMINAL
	sudo apt update && 

	# sudo apt install kde-l10n-ptbr -y &&			# ALREADY INCLUDED IN KUBUNTU 22.04
	# sudo apt install libreoffice-l10n-pt-br -y &&		# ALREADY INCLUDED IN KUBUNTU 22.04
	# sudo apt install libreoffice-style-sifr -y &&		# ALREADY INCLUDED IN KUBUNTU 22.04
	# sudo apt install software-properties-common -y &&	# ALREADY INCLUDED IN KUBUNTU 22.04
	sudo apt install kubuntu-restricted-extras -y && 
	sudo apt install unace unrar zip unzip p7zip-full p7zip-rar sharutils rar -y && 
	sudo apt install git-all -y && 
	sudo apt install krusader -y && 
	sudo apt install bleachbit -y && 

	sudo apt update && 

	sudo add-apt-repository ppa:numix/ppa -y && 
	sudo add-apt-repository ppa:danielrichter2007/grub-customizer -y && 
	sudo add-apt-repository ppa:docky-core/stable -y && 
	sudo add-apt-repository ppa:qbittorrent-team/qbittorrent-stable -y && 
	sudo add-apt-repository ppa:inkscape.dev/stable -y && 
	sudo add-apt-repository ppa:rvm/smplayer -y && 

	sudo apt update && 

	sudo apt install numix-icon-theme numix-icon-theme-circle -y && 
	sudo apt install grub-customizer -y && 
	sudo apt install plank -y && 
	sudo apt install qbittorrent -y && 
	sudo apt install inkscape -y && 
	sudo apt install smplayer smplayer-themes smplayer-skins -y && 
	sudo apt install mpv -y

> Join lines using Sublime Text or VS Code shortcut `CTRL + J`. Then run all commands at once.

<br/>

### 2.1 – REALTEK RTL8821CU WI-FI DRIVER
	sudo apt install build-essential dkms git-all bc -y 
	
	# OPEN DRIVER FOLDER IN TERMINAL #
	
	sudo su
	make
	sudo make install
	sudo reboot

- Source 1: https://github.com/brektrou/rtl8821CU
- Source 2: https://www.youtube.com/watch?v=tyLMzIAxj-4
- Source 3: https://github.com/jcqSCH/kubuntu-after/blob/master/Driver_RTL8821CU_RAW.7z

<br/>

### 2.2 – WPS OFFICE TRANSLATION PT-BR
	# OPEN TRANSLATION FOLDER IN TERMINAL #
	
	bash install.sh

- Source 1: https://github.com/vaamonde/pt_br-wpsoffice
- Source 2: https://www.youtube.com/watch?v=PzIgNdJDdFE
- Source 3: https://github.com/jcqSCH/kubuntu-after/blob/master/Translation_WPS_Office_PT-BR.7z

<br/>

## 3 ➜ SETTINGS

### 3.1 – Plank:
Download themes: https://github.com/dabrowski-adam/plank-themes

|  SETTINGS        |             …             |
|       ---        |            ---            |
|  Theme:          |  Shade                    |
|  Icons:          |  68                       |
|  Zoom:           |  125                      |

>**Ordem:** Dolphin, Terminal, Spotify, Firefox, Chrome, VS Code, KCalc, Writer, Impress, KSysGuard, System Settings

<br/>

### 3.2 – Fontes do Sistema:
|  Configurações   |             …             |
|       ---        |            ---            |
|  Geral:          |  Segoe WP 14              |
|  Largura fixa:   |  Courier 10 Pitch 16      |
|  Pequena:        |  Segoe WP 13              |
|  Barra:          |  Segoe WP 13              |
|  Menu:           |  Segoe WP 14              |
|  Título:         |  Segoe WP 14 ( negrito )  |
|        …         |             …             |
|  Anti-aliasing   | Habilitado, RGB, Leve     |

<br/>

### 3.3 – Barra Superior:
>**Ordem:** Menu de Aplicativos, Gerenciador de Tarefas com Ícones, Lixeira, Área de Notificação, Bloquear/Encerrar, Relógio, Área de Trabalho

<br/>

### 3.4 – Spotify:
	sudo kate /usr/share/applications/spotify.desktop
>**Substituir:** Exec=spotify %U <br/>
>**Por:** Exec=spotify %U --force-device-scale-factor=1.25

<br/>

## 4 ➜ HINTS

### 4.1 – Open folder as Administrator:
Open Krusader ➜ Tools ➜ Start Root Mode Krusader (**ALT + SHIFT + K**)
- Source: https://askubuntu.com/questions/990611/how-to-run-dolphin-as-root/1048826#1048826

<br/>

### 4.2 – Unmount the Windows partition while logged into Kubuntu:
	mount -o ro /dev/sda2
> Edit `sda2` above if that's not the partition your Windows is installed on.
- Source: https://askubuntu.com/questions/335909/error-mounting-dev-sda2-at-media/335922#335922

<br/>

### 4.3 – Check the video driver installed
	lspci -k | grep -EA3 'VGA|3D|Display'
> The `VGA|3D|Display` stands for `INTEL|NVIDIA|AMD` respectively.

<br/>

### 4.4 – Fix the bug "Can't move files to the trash":
	sudo chown -R “$USER” ~/.local/share/Trash
> Edit the `“$USER”` part above and enter your Kubuntu username (without quotes).
- Source: https://askubuntu.com/questions/288513/cant-move-files-to-the-trash/298335#298335

<br/>

### 4.5 – Recover lost GRUB after a Windows update (dual boot):
	bcdedit /set "{bootmgr}" path \EFI\ubuntu\grubx64.efi
> Logged into Windows, run the command above in PowerShell as Administrator.
- Source: https://askubuntu.com/questions/655011/windows-10-upgrade-kills-grub-and-boot-repair-doesnt-help/655279#655279

<br/>
