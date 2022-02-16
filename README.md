# ETHICAL-HACKER-WORK-ENVIRONMENT
     # TMCyber
     # ETHICAL HACKER | CEH | PYTHON IA|ML | |Bug Bounty|Researcher|
BSPWM + LSD + POLYBAR + GNOME TERMINAL + POWERLEVEL10K
![Captura de pantalla -2022-02-10 19-59-39](https://user-images.githubusercontent.com/97669969/154141253-28876c7b-c3a2-4fc0-afb4-287c14752633.png)
BSPWM + GNOME TERMINAL + POWERLEVEL10K + POLYBAR THEME
![Captura de pantalla -2022-02-10 18-55-01](https://user-images.githubusercontent.com/97669969/154141266-2e1d424d-2d37-465a-8094-a59e164b43e8.png)
BSPWM + POLYBAR + ROFI THEME
![Captura de pantalla -2022-02-10 16-30-10](https://user-images.githubusercontent.com/97669969/154141274-15c5a6de-49fe-49bf-9ee1-0ba650b4605a.png)
BSPWM + POLYBAR + CAJA
![Captura de pantalla -2022-02-10 19-30-59](https://user-images.githubusercontent.com/97669969/154141282-b176cf7a-aa96-4766-a35c-0ba89d804577.png)
BSPWM + POLYBAR + POWERLEVEL10K + COMPLETADOR INTELIGENTE | NETCAT | NMAP 
![Captura de pantalla -2022-02-10 19-07-13](https://user-images.githubusercontent.com/97669969/154141288-443e7565-1a94-47a9-ab3c-268f6f6abbf1.png)
BSPAM + POLYBAR + CODIUM 
![Captura de pantalla -2022-02-10 22-25-28](https://user-images.githubusercontent.com/97669969/154141304-25db8fc3-95e8-4161-b0b7-59a98f3c799d.png)
BSPWM + FIBONACCI TERMINAL'S
![Captura de pantalla -2022-02-10 22-22-18](https://user-images.githubusercontent.com/97669969/154141307-d78820ee-3322-4da0-a750-ebcff2deec68.png)
BSPWM + POLYBAR + BRAVE
![Captura de pantalla -2022-02-10 22-21-36](https://user-images.githubusercontent.com/97669969/154141320-a49440e3-1460-4a9c-a8f1-7a683f2f92c8.png)
  
# MUY IMPORTANTE: Este entorno esta habilitado con transparencias en TODAS las ventanas. 
  
     #Configura y haz la instalacion en una maquina virtual,  o clona la maquina .
     #Solo en el caso de no tener experiencia con gestores de ventanas y sus previas configuraciones)
     #Configura y haz la instalacion en una maquina virtual,  o clona la maquina .
     #Solo en el caso de no tener experiencia con gestores de ventanas y sus previas configuraciones)

    # Presta atencion, alos pasos a seguir, no hagas nada con root, usa tu usuario diario, o creea uno nuevo, como creas conveniente.
    # Solo en el caso de que haga falta o se especifica tal caso se usa sudo.
    # Los comandos estan preparados para copy/paste si lo prefieres, en algunos casos tendras que reemplazar con tu usuario, o cambiar directorios.
    # La mayoria de las clones y instalaciones se hacen en /Downloads /Descargas, hay exceptions en /Home , presta atencion.
   
   #Instalacion hecha sobre : Parrot OS 4.11.3 2022 (probada tambien en Kali -sin problemas previos) 


# Librerias Necesarias 
* hacer sudo apt install de todas, si algunas se encuentran instaladas , pasas a las siguente, hasta tener todas instaladas.

```bash
sudo apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev 
libxcb-keysyms1-dev libxcb-xinerama0-dev libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev
```

```bash
sudo apt install cmake cmake-data pkg-config python3-sphinx libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev 
libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev libxcb-xkb-dev 
libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev libjsoncpp-dev libmpdclient-dev libcurl4-openssl-dev libnl-genl-3-dev
```

```bash
sudo apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev 
libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev 
libgl1-mesa-dev libpcre2-dev libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev
```

```bash
sudo apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev libxcb-keysyms1-dev libxcb-xinerama0-dev libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev
 ```

```bash
sudo apt update
```
# Instalamos bspwm y sxhkd 

```bash
# cd Downloads
# sudo apt install bspwm
$ git clone https://github.com/baskerville/bspwm.git
# cd bspwm/
# make
# sudo make install
```

# Proceedemos con sxhkd 

```bash
# cd Downloads
# sudo apt install sxhkd
$ git clone https://github.com/baskerville/sxhkd.git
# cd sxhkd/
# make
# sudo make install
```
      # Creeamos directorios y copiamos los config en los directorios corespondientes, do copy/paste.
      # Si no te funciona desde home dirigete y entra dentro  de las carpetas correspondientes y haz cp desde ahy, apuntando hacia esos directorios.

```bash
cd
mkdir ~/.config/bspwm
mkdir ~/.config/sxhkd
cd /home/tmcyber/bspwm/         (reemplaza el usuario,al tuyo..)
cp examples/bspwmrc ~/.config/bspwm/
chmod +x ~/.config/bspwm/bspwmrc 
cp examples/sxhkdrc ~/.config/sxhkd/
```


# nano/vim y editamos los shortcuts a nuestro gusto:
    # En mi caso los shorts miois estan en el repo sxhkdrc.



# Instalamos Polybar

    # Abre tu navegador y dirigete a https://www.nerdfonts.com/ o algun otro sitio tuyo preferido.
    # Instala algunas de las fuentes a tu gusto, te recomiendo por lo menos 2 tipos de fonts como serian: JetBrainsMono, Iosevka, UbuntuMono, Hack Nerd Fonts .etc.

# Sitos:

• https://github.com/be5invis/Iosevka/releases
• https://www.nerdfonts.com/font-downloads
• https://www.1001fonts.com/jetbrains-mono-font.html
• https://www.1001freefonts.com/es/ubuntu-mono.font
 
   # Por ex Hack Nerd Fonts de nerdfonts.com : 
```bash
   # cd Descargas
   # sudo mv Hack.zip /usr/share/local/fonts   (si falla de dir/ en mi caso fue : usr/share/fonts)
   # sudo unzip
   # ahora abre una terminal WIN+ENTER (segun los shortcuts que has elegido de preferencia) mira arriba de las terminales y dirigete a Preferencias de perfil , editar perfil , dirigete a fonts.
   # ahy busca y elige tu estilo de font que descargaste, y listo.
 ```

# Clonamos desde github la polybar

```bash
# cd Downloads
$ git clone --recursive https://github.com/polybar/polybar
# cd polybar/
# mkdir build
# cd build/
# cmake ..
# make -j$(nproc)
# sudo make install
```

# Executa echo sobre bspqm -archivo de arranque- (verifica con un cat) :

```bash
# echo '~/.config/polybar/./launch.sh' >> ~/.config/bspwm/bspwmrc
```

# IMPORTANTE 
• si tienes el error comun de cmake .. con CMakeLists.txt? instala estas librerias de nuevo.

```bash
sudo apt install libxcb-xkb-dev libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev i3-wm libjsoncpp-dev libmpdclient-dev libcurl4-openssl-dev libnl-genl-3-dev

sudo apt install build-essential git cmake cmake-data pkg-config python3-sphinx python3-packaging libuv1-dev libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev

sudo apt update
```

# En este punto se puede reinciar (sudo kill -9 -1) , iniciar en bspwm.
•  Y puedes ver la polybar arriba (es la polybar normal, enseguida lo tuneamos con temas interesantes, paciencia es la clave.
•  Se puede dar el caso ,que no aparezca o NO ESTE, que en diferentes ocasiones me paso a mi , para esto ejecuta un sudo rm -r polybar y clonea de nuevo siguiendo los pasos descritos.
•  Se puede dar el caso de que te falta aguna libreria.

# Instalamos TEMAS para Polybar

• Descarga materialicons en /HOME , el repositorio : https://github.com/google/material-design-icons.git 
• No olvide al final del clone hacer fc-cache -fv

• Temas que uso : https://github.com/adi1090x/polybar-themes (tiene una gran variedad de temas)
• Sigue los pasos indicados en el repositorio, las fuentes las tienes instaladas desde el paso de ariba descrito, como material icons.
 
# No olvides esta linea se codigo: bash ~/.config/polybar/launch.sh --cuts  
•  en ~/.config/bspwm/bspwmrc 
•  --cuts es el nombre del tema, tu elige el tuyo.

• En el repo arriba se encuentra un archivo modules.ini , editado y configurado al maximo, con icons etc, modules , scripts. 
•  Lo puedes modificar al maximo (ten mucho cuidado lo que tocas , te puedes quedar sin barra, te recomiendo investigar un poco.
•  De igual manera con copy/paste al mio tienes la polybar tuneada de manera mia.

# Fondo de Pantalla con feh

```bash
# sudo apt install feh
# cd ~/.config/bspwm/bspwmrc 
# nano bspwmrc
```

• ahora agregamos la siguente linea al final : feh --bg-fill /home/tmcyber/images/hacking-hackers.jpg
• Ten en cuenta tu nombre de usuario y los directorios, modifica y pon los tuyos.
• Abres google y descargas un fondo de pantalla , o si no lo pasas mediante samba o servidor a tu maquina, etc.


# Transparencias con picom (el viejo compton) 

• ejecuta el cloneo en la carpeta /Descargas) suele saltar errores a la hora de clonar en /Home
# Instala estas librerias, si las tienes pues perfecto.

```bash
sudo pip3 install meson

sudo apt install libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libxcb-glx0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev libpcre2-dev libpcre3-dev libevdev-dev uthash-dev libev-dev libx11-xcb-dev meson
```

```bash
# sudo apt update
$ git clone https://github.com/ibhagwan/picom.git
# cd picom/
# git submodule update --init --recursive
# meson --buildtype=release . build
# ninja -C build
# sudo ninja -C build install
```

• cp picom.conf al directorio ~/.config/picom 
• mira los permisos que tiene siempre si no : chmod +x y listo.
• En algunos casos usuarios se han trepado con que el archivo picom.conf no esta , si este es tu caso creeamos uno en el dir : cd~/.config/picom con touch picom.conf  (dale permisos chmod +x)
• Mi conf de picom esta en el repo copy/paste en el tuyo , listo : # NO OLVIDES LO QUE DIJE AL PRINCIPIO , ESTA CONFIGURADA PARA TRANSPARENCIAS EN TODO SISTEMA!

# MUY IMPORTANTE

• El .conf esta editado y descomentado todo lo relacionado con blur y cambiado el 'backend = "glx"' por 'backend = "xrender"' , nada de glx.
• En multitud de ocasiones "glx y Blur bloqueo el gestor y las ventanas, o se experimento una lentitud de la maquina, te lo digo por experiencia.
• Si te interesa tener blurring en las ventanas, comenta las lineas de codigo en el apartado blur, e intentalo , pero no te lo recomiendo , en mi caso no me gusta el blurring.

# AHORA 

• nos dirigimos a cd ~/.config/bspwm/bspwmrc (el cerebro de nuestro entorno), abres con nano o vim  y agregas al final lo siguente : 

picom &

• Listo, guardas y sales . reinicio total de configuraciones  WIN+ALT+R (en mi caso)

• OPCIONAL si queres quitar todos los bordes, y tener esquinas redondeadas aplica esto:
```bash
echo 'picom --experimental-backends &' >> ~/.config/bspwm/bspwmrc 
echo 'bspc config border_width 0' >> ~/.config/bspwm/bspwmrc
```

# Lanzador rofi

```bash
# cd
# sudo apt update
# sudo apt install rofi
```
• WIN+D (shortcut a tu gusto, deberia aparecer rofi)
• rofi-theme-selector (elige tema a tu gusto)
• En los repositorios de github hay temas por gustos.


# TUNNING DE TERMINALES POWERLEVEL10K 
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
```

• en tu terminal escribe : zsh 


# IMPORTANTE: Para el usuario root debe hacer lo mismos pasos.

      # nano ~/.p10k.zsh  (el conf editable de powerlevel10k , lo puedes configurar as tu gusto quitando y agregando cositas..etc)


# OPCIONAL  : 
          # Enlace simbolico de .zshrc (todos los cambios que efectuas con tu usuario normal, se aplica tambien para root.)
```bash
ln -s -f /home/tmcyber/.zshrc .zshrc
```
               # modifica y pon tu usuario tu usuario 

# Aplicamos zsh como nuestra shell por defecto, es opcional.

```bash
usermod --shell /usr/bin/zsh tmcyber       (seguido de tu usuario)
usermod --shell /usr/bin/zsh root            (para root tambien executas esto)
```

# Instalamos Brave Browser

• brave es muy seguro 
• rastreadores y bloqueadores incorporados 
• no hace falta agregar extensiones como adblocker o parecidas
• en recursos de sistema tiene muy bajo consumo, menos que firefox.

```bash
# sudo apt install apt-transport-https curl
# sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg
# echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list
# sudo apt update
# sudo apt install brave-browser
```

# Instalamos lsd

• Repositorio Github : https://github.com/Peltoche/lsd
• ve a releases > version , en mi caso amd64 , io tengola 0.21.0 )

    # Instalas con sudo dkpg -i 
    # lsd -l  y veras la diferencia

# Instalamos ranger

```bash
sudo apt install ranger
```
                 # en tu terminal ranger y veras la diferencia


# Instalamos bat

• https://github.com/sharkdp/bat

                      # sudo dpkg -i  para instalar bat 
                      # uso la version 19 punto algo, en la pagina>releases elije desde 19 para arriba , en mi caso para amd64.

• cat vs bat . prueba y veras la diferencia



# DIRECTORIOS IMPORTANTES :

• cd~/.config/             

       # Es un directorio oculto en tu /HOME, ahy se encuentra casi todos los .config del sistema.                                                                                        
• cd ~/.config/bspwm/  
        
         # Gestor ventanas, es el cerebro de toda la interfaz)

• cd ~/.config/sxhkd/   
            
           # Gestor de Shortcuts

• cd~/.config/polybar   
        
         # Barra de estados Polybar

• cd~/.config/picom     
        
        # Gestor de transparencias y efectos,blurring sobre ventanas etc)

• cd~/.config/feh         
          
            # Sencillo Gestor de fondos de Pantalla)


• cd /home/tmcyber/polybar-themes/bitmap/hack/ 
       
         # directorio de mi tema establecido de polybar
         # cada tema tiene un config.ini suyo 
         # con nano/vim abres y puedes modificarla yo personalizarla al maximo





