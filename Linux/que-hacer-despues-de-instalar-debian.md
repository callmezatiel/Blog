Agregamos los repositorios non-free y backports

``` 
# Repos oficiales no libres
deb https://ftp.debian.org/debian/ bookworm contrib main non-free non-free-firmware
# deb-src https://ftp.debian.org/debian/ bookworm contrib main non-free non-free-firmware

# Actualizaciones
deb https://ftp.debian.org/debian/ bookworm-updates contrib main non-free non-free-firmware
# deb-src https://ftp.debian.org/debian/ bookworm-updates contrib main non-free non-free-firmware
deb https://ftp.debian.org/debian/ bookworm-proposed-updates contrib main non-free non-free-firmware
# deb-src https://ftp.debian.org/debian/ bookworm-proposed-updates contrib main non-free non-free-firmware

# Seguridad
deb https://security.debian.org/debian-security/ bookworm-security contrib main non-free non-free-firmware
# deb-src https://security.debian.org/debian-security/ bookworm-security contrib main non-free non-free-firmware

# Repositorios Backports
deb https://ftp.debian.org/debian/ bookworm-backports contrib main non-free non-free-firmware
# deb-src https://ftp.debian.org/debian/ bookworm-backports contrib main non-free non-free-firmware

# Multimedia
deb https://www.deb-multimedia.org bookworm main non-free

```

Agregar claves GPG

```
apt-key adv --keyserver keyring.debian.org --recv-keys 5C808C2B65558117
apt-key export 65558117 | sudo gpg --dearmour -o /etc/apt/trusted.gpg.d/debian-multimedia.gpg
```

actualizamos el repositorio y el sistema
```
sudo apt update && sudo apt upgrade -y
```
