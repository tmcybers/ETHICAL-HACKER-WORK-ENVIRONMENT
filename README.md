


#Librerias Necesarias (hacer sudo apt install de todas, si algunas se encuentran instaladas , pasas a las siguentes..hasta tener todas instaladas.) :

sudo apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev 
libxcb-keysyms1-dev libxcb-xinerama0-dev libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev

sudo apt install cmake cmake-data pkg-config python3-sphinx libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev 
libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev libxcb-xkb-dev 
libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev libjsoncpp-dev libmpdclient-dev libcurl4-openssl-dev libnl-genl-3-dev

sudo apt install meson libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev 
libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libpixman-1-dev libdbus-1-dev libconfig-dev 
libgl1-mesa-dev libpcre2-dev libevdev-dev uthash-dev libev-dev libx11-xcb-dev libxcb-glx0-dev

sudo apt install build-essential git vim xcb libxcb-util0-dev libxcb-ewmh-dev libxcb-randr0-dev libxcb-icccm4-dev libxcb-keysyms1-dev libxcb-xinerama0-dev libasound2-dev libxcb-xtest0-dev libxcb-shape0-dev




INSTALACION BSPWM Y SXHKD :

sudo apt install bspwm    
(y tambien lo clonaremos mediante github.)
cd
git clone https://github.com/baskerville/bspwm.git
cd bspwm/
make
sudo make install

Proceedemos con sxhkd :

sudo apt install sxhkd    (por si no esta..si se encuentra instalado, |perfecto| seguiremos clonandolo no pasa nada..)
cd
git clone https://github.com/baskerville/sxhkd.git
cd ../sxhkd/
make
sudo make install

Creeamos directorios y copiamos los config en los directorios corespondientes, do copy/paste : 

(ejecuta cd muy importante y luego creea los directorios, y copia los archivos, si no te funciona desde home dirigete y entra dentro 
de las carpetas correspondientes y has cp (copy) desde ahy..apuntando hacia esos directorios)

cd
mkdir ~/.config/bspwm
mkdir ~/.config/sxhkd
cd /home/tmcyber/bspwm/         (reemplaza el usuario,al tuyo..)
cp examples/bspwmrc ~/.config/bspwm/
chmod +x ~/.config/bspwm/bspwmrc 
cp examples/sxhkdrc ~/.config/sxhkd/


+Ahora abrimos sxhkdrc con nano/vim y editamos los shortcuts a nuetro gusto
+En mi caso los shorts mios son estos: 




POLYBAR :

Abre tu navegador y dirigete a https://www.nerdfonts.com/ o algun otro sitio tuyo preferido.
Instala algunas de las fuentes a tu gusto, te recomiendo por lo menos 2 tipos de fonts como serian: JetBrainsMono, Iosevka, UbuntuMono, Hack Nerd Fonts .etc.
Io tengo las 4, por gusto las cambio despues de un tiempo.!
https://github.com/be5invis/Iosevka/releases
https://www.nerdfonts.com/font-downloads
https://www.1001fonts.com/jetbrains-mono-font.html
https://www.1001freefonts.com/es/ubuntu-mono.font
 
Por ex Hack Nerd Fonts de nerdfonts.com : 

cd Descargas
sudo mv Hack.zip /usr/share/local/fonts   (si falla de dir/ en mi caso fue : usr/share/fonts)
sudo unzip
ahora abre una terminal WIN+ENTER (segun los shortcuts que has elegido de preferencia) mira arriba de las terminales y dirigete a Preferencias de perfil , editar perfil ,dirigete a fonts 
ahy busca y elige tu estilo de font que descargaste, y listo.
 
 (clonamos desde github LA POLYBAR) 
cd 
git clone --recursive https://github.com/polybar/polybar
cd polybar/
mkdir build
cd build/
cmake ..
make -j$(nproc)
sudo make install

Executa echo sobre bspqm -archivo de arranque- (verifica con un cat) :
echo '~/.config/polybar/./launch.sh' >> ~/.config/bspwm/bspwmrc


IMPORTANTE 
-si tienes el error comun de cmake .. con CMakeLists.txt? instala estas librerias de nuevo : ---------------------
sudo apt install libxcb-xkb-dev libxcb-xrm-dev libxcb-cursor-dev libasound2-dev libpulse-dev i3-wm libjsoncpp-dev libmpdclient-dev libcurl4-openssl-dev libnl-genl-3-dev
sudo apt install build-essential git cmake cmake-data pkg-config python3-sphinx python3-packaging libuv1-dev libcairo2-dev libxcb1-dev libxcb-util0-dev libxcb-randr0-dev libxcb-composite0-dev python3-xcbgen xcb-proto libxcb-image0-dev libxcb-ewmh-dev libxcb-icccm4-dev

sudo apt update




En este punto ia se puede reinciar (sudo kill -9 -1) , y iniciar en bspwm.

+Y podemos ver Polybar arriba (es la polybar normal..enseguida lo tuneamos con temas interesantes..paciencia..o lo puedes modificar a tu gusto con el tiempo...)
! Se puede dar el caso ,que no aparezca o NO ESTE, que en diferentes ocasiones me paso a mi , para esto ejecuta un sudo rm -r polybar y clonea de nuevo siguinedo los pasos descritos.




Instalamos TEMAS para Polybar

+Descarga materialicons en /HOME , el repositorio : https://github.com/google/material-design-icons.git (no olvide al final del clone hacer fc-cache -fv)

+Temas--lo que uso es esto : https://github.com/adi1090x/polybar-themes (tiene una gran variedad de temas)
+Sigue los pasos indicados en el repositorio, las fuentes las tienes instaladas desde el paso de ariba descrito, como material icons.
 ==no olvides esta linea se codigo: bash ~/.config/polybar/launch.sh --cuts   (en ~/.config/bspwm/bspwmrc ) (--cuts es el nombre del tema,tu elige el tuyo)

+En el repo arriba se encuentra un archico modules.ini , editado y configurado al maximo, con icons etc, modules , scripts. 
+ Lo puedes modificar al maximo (ten mucho cuidado lo que tocas , te puedes quedar sin barra, te recomiendo investigar un poco por tu cuenta.
  de igual manera con copy/paste al mio teienes la polybar tuneada de manera mia+






FONDO DE PANTALLA CON feh

sudo apt install feh
cd ~/.config/bspwm/bspwmrc 
nano bspwmrc
ahora agregamos la siguente linea al final : feh --bg-fill /home/tmcyber/images/hacking-hackers.jpg
---ten en cuenta tu nombre de usuario y los directorios, modifica y pon los tuyos---
(abres google y descargas un fondo de pantalla ,o si no lo pasa mediante samba o servidor a tu maquina..etc)


TRANSPARENCIAS CON picom (compton) 

=(ejecuta el cloneo en la carpeta /Descargas) suele saltar errores a la hora de clonar en /Home)

sudo pip3 install meson
sudo apt install libxext-dev libxcb1-dev libxcb-damage0-dev libxcb-xfixes0-dev libxcb-shape0-dev libxcb-render-util0-dev libxcb-render0-dev libxcb-randr0-dev libxcb-composite0-dev libxcb-image0-dev libxcb-present-dev libxcb-xinerama0-dev libxcb-glx0-dev libpixman-1-dev libdbus-1-dev libconfig-dev libgl1-mesa-dev libpcre2-dev libpcre3-dev libevdev-dev uthash-dev libev-dev libx11-xcb-dev meson
sudo apt update
git clone https://github.com/ibhagwan/picom.git
cd picom/
git submodule update --init --recursive
meson --buildtype=release . build
ninja -C build
sudo ninja -C build install

cp picom.conf al directorio ~/.config/picom 
--mira los permisos que tiene siempre si no : chmod +x y listo.
+En algunos casos usuarios se han trepado con que el archivo picom.conf no esta , si este es tu caso creeamos uno en el dir : cd~/.config/picom con touch picom.conf  (dale permisos chmod +x)
+Aqui tienes mi conf de picom copy/paste en el tuyo , listo : 

MUY IMPORTANTE
El .conf esta editado y descomentado todo lo relacionado con blur y cambiado el 'backend = "glx"' por 'backend = "xrender"'  (nada de glx).
--En multitud de ocasiones "glx y Blur bloqueo el gestor y las ventanas, o se experimento una lentitud de la maquina) (te lo digo por experiencia).
--Si te interesa tener blurring en las ventanas, comenta las lineas de codigo en el apartado blur, e intentalo , pero no te lo recomiendo , (en mi caso no me gusta el blurring)
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
AHORA nos dirigimos a cd ~/.config/bspwm/bspwmrc (el cerebro de nuestro entorno), abres con nano o vim  y agregas al final lo siguente : 

picom &

-Listo, guardas y sales . reinicio total de configuraciones  WIN+ALT+R (en mi caso), listo.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
+OPCIONAL si queres quitar todos los bordes, y tener esquinas redondeadas aplica esto:
echo 'picom --experimental-backends &' >> ~/.config/bspwm/bspwmrc 
echo 'bspc config border_width 0' >> ~/.config/bspwm/bspwmrc

Listo!


LANZADOR ROFI

cd
sudo apt update
sudo apt install rofi
WIN+D (shortcut a tu gusto, deberia aparecer rofi)
rofi-theme-selector (elige tema tu gusto)
(+En los repositorios de github hay temas por gustos..)


TUNNING DE TERMINALES POWERLEVEL10K 

Repositorio :
https://github.com/romkatv/powerlevel10k

O si prefieres, copy/paste y listo!

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/powerlevel10k
echo 'source ~/powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc

en tu terminal escribe : zsh 


IMPORTANTE: Para el usuario root debe hacer lo mismos pasos.
Listo.
nano ~/.p10k.zsh  (el conf editable dela powerlevel10k , lo puedes configurar as tu gusto quitando y agregando cositas..etc)

OPCIONAL  : Enlace simbolico de .zshrc (todos los cambios que efectuas con tu usuario normal, se aplica tambien para root.)
ln -s -f /home/tmcyber/.zshrc .zshrc

APLICAMOS LA SHELL ZSH POR DEFECTO 
(es opcional, si queres seguir en bash , no es obligatorio..es tema de gustos,etc) ; 

usermod --shell /usr/bin/zsh tmcyber       (seguido de tu usuario)
usermod --shell /usr/bin/zsh root            (para root tambien executas esto)




OPCIONAL INSTALAMOS BRAVE BROWSER

+brave es muy seguro 
+rastreadores y bloqueadores incorporados 
+no hace falta agregar extensiones como adblocker o parecidas
+en recursos de sistema tiene muy bajo consumo, no como firefox.

sudo apt install apt-transport-https curl

sudo curl -fsSLo /usr/share/keyrings/brave-browser-archive-keyring.gpg https://brave-browser-apt-release.s3.brave.com/brave-browser-archive-keyring.gpg

echo "deb [signed-by=/usr/share/keyrings/brave-browser-archive-keyring.gpg arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main"|sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update

sudo apt install brave-browser

Listo!



OPCIONAL INSTALAMOS LSD

Repositorio Github : https://github.com/Peltoche/lsd
(igual que en caso de bat , releases> version , en mi caso amd64 , io tenngo la 0.21.0 )
sudo dkpg -i  (archivo que descargaste...enter y listo)

lsd -l  (veras la diferencia de ls)



OPCIONAL INSTALAMOS RANGER

sudo apt install ranger
 listo !
 
 ahora escribe en tu terminal ranger y veras la diferencia.(si lo queres usar , es tema de gustos...a mi me parece super util)
 
 

OPCIONAL INSTALAMOS BAT

https://github.com/sharkdp/bat

sudo dpkg   para instalar bat 
(io uso la version 19 punto algo, en la pagina>releases y escoje desde 19 para arriba , en mi caso para amd64 )

cat vs bat (prueba y veras la diferencia)
