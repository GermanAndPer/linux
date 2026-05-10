# 🐧 Guía Completa de Comandos Ubuntu Linux
> Organizada por categorías e importancia de uso

---

## 📊 Niveles de Importancia

| Nivel | Símbolo | Descripción |
|-------|---------|-------------|
| Crítico | 🔴 | Uso diario imprescindible |
| Alto | 🟠 | Uso frecuente y muy útil |
| Medio | 🟡 | Uso situacional importante |
| Básico | 🟢 | Complementario / avanzado |

---

## 1. 📁 Gestión de Archivos y Directorios

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `ls` | Lista archivos y directorios | `ls -la` |
| `cd` | Cambia de directorio | `cd /home/usuario` |
| `pwd` | Muestra el directorio actual | `pwd` |
| `cp` | Copia archivos o directorios | `cp archivo.txt /destino/` |
| `mv` | Mueve o renombra archivos | `mv viejo.txt nuevo.txt` |
| `rm` | Elimina archivos | `rm -rf carpeta/` |
| `mkdir` | Crea directorios | `mkdir -p ruta/nueva` |
| `touch` | Crea archivos vacíos | `touch archivo.txt` |
| `cat` | Muestra contenido de archivos | `cat archivo.txt` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `find` | Busca archivos en el sistema | `find / -name "*.log"` |
| `locate` | Búsqueda rápida en base de datos | `locate archivo.conf` |
| `ln` | Crea enlaces simbólicos o duros | `ln -s /origen /destino` |
| `tree` | Muestra estructura en árbol | `tree -L 2` |
| `du` | Uso de espacio en disco | `du -sh *` |
| `stat` | Información detallada de archivo | `stat archivo.txt` |

### 🟡 Media Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `file` | Tipo de archivo | `file imagen.jpg` |
| `wc` | Cuenta líneas/palabras/caracteres | `wc -l archivo.txt` |
| `diff` | Compara dos archivos | `diff a.txt b.txt` |
| `split` | Divide archivos grandes | `split -b 100M archivo` |
| `shred` | Elimina archivos de forma segura | `shred -u secreto.txt` |

---

## 2. 📦 Gestión de Paquetes (APT)

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `apt update` | Actualiza lista de paquetes | `sudo apt update` |
| `apt upgrade` | Actualiza paquetes instalados | `sudo apt upgrade -y` |
| `apt install` | Instala un paquete | `sudo apt install nginx` |
| `apt remove` | Elimina un paquete | `sudo apt remove nginx` |
| `apt purge` | Elimina paquete y configuración | `sudo apt purge nginx` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `apt search` | Busca paquetes disponibles | `apt search python3` |
| `apt show` | Info detallada de un paquete | `apt show curl` |
| `apt autoremove` | Elimina dependencias huérfanas | `sudo apt autoremove` |
| `apt list --installed` | Lista paquetes instalados | `apt list --installed` |
| `dpkg -i` | Instala paquete .deb local | `sudo dpkg -i paquete.deb` |
| `dpkg -l` | Lista paquetes dpkg | `dpkg -l | grep nginx` |

### 🟡 Media Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `apt-cache` | Consulta la caché de paquetes | `apt-cache depends curl` |
| `add-apt-repository` | Añade repositorio PPA | `sudo add-apt-repository ppa:nombre` |
| `snap install` | Instala paquetes Snap | `sudo snap install code --classic` |
| `snap list` | Lista snaps instalados | `snap list` |

---

## 3. 👤 Gestión de Usuarios y Permisos

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `sudo` | Ejecuta como superusuario | `sudo apt update` |
| `chmod` | Cambia permisos de archivos | `chmod 755 script.sh` |
| `chown` | Cambia propietario de archivos | `chown usuario:grupo archivo` |
| `passwd` | Cambia contraseña | `passwd usuario` |
| `su` | Cambia de usuario | `su - usuario` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `useradd` | Crea un nuevo usuario | `sudo useradd -m juan` |
| `userdel` | Elimina un usuario | `sudo userdel -r juan` |
| `usermod` | Modifica un usuario | `sudo usermod -aG sudo juan` |
| `groupadd` | Crea un grupo | `sudo groupadd devs` |
| `groups` | Muestra grupos del usuario | `groups juan` |
| `who` | Usuarios conectados | `who` |
| `id` | Info del usuario actual | `id` |

### 🟡 Media Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `visudo` | Edita el archivo sudoers | `sudo visudo` |
| `last` | Historial de inicios de sesión | `last` |
| `w` | Quién está conectado y qué hace | `w` |
| `umask` | Máscara de permisos predeterminada | `umask 022` |
| `chgrp` | Cambia el grupo de un archivo | `chgrp devs archivo.txt` |

---

## 4. 🖥️ Gestión de Procesos

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `ps` | Lista procesos activos | `ps aux` |
| `kill` | Termina un proceso por PID | `kill -9 1234` |
| `top` | Monitor de procesos en tiempo real | `top` |
| `htop` | Monitor interactivo (mejorado) | `htop` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `killall` | Termina procesos por nombre | `killall firefox` |
| `pkill` | Termina procesos por patrón | `pkill -f "python"` |
| `bg` | Envía proceso al fondo | `bg %1` |
| `fg` | Trae proceso al frente | `fg %1` |
| `jobs` | Lista trabajos en segundo plano | `jobs` |
| `nohup` | Ejecuta sin interrupción al cerrar | `nohup script.sh &` |
| `nice` | Ejecuta con prioridad ajustada | `nice -n 10 comando` |

### 🟡 Media Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `pgrep` | Busca PID por nombre | `pgrep nginx` |
| `renice` | Cambia prioridad de proceso activo | `renice -5 -p 1234` |
| `strace` | Traza llamadas al sistema | `strace -p 1234` |
| `lsof` | Archivos abiertos por procesos | `lsof -i :80` |
| `watch` | Ejecuta comando periódicamente | `watch -n 2 df -h` |

---

## 5. 🌐 Redes y Conectividad

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `ping` | Prueba conectividad | `ping google.com` |
| `ip addr` | Muestra interfaces de red | `ip addr show` |
| `curl` | Transferencias HTTP/S | `curl -O https://url/archivo` |
| `wget` | Descarga archivos desde la web | `wget https://url/archivo` |
| `ssh` | Conexión remota segura | `ssh usuario@192.168.1.1` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `netstat` | Estadísticas de red | `netstat -tuln` |
| `ss` | Reemplazo moderno de netstat | `ss -tuln` |
| `traceroute` | Rastrea ruta de paquetes | `traceroute google.com` |
| `nmap` | Escaneo de puertos | `nmap -sV 192.168.1.1` |
| `scp` | Copia archivos por SSH | `scp archivo usuario@host:/ruta` |
| `rsync` | Sincroniza archivos/directorios | `rsync -avz origen/ destino/` |
| `ufw` | Firewall simplificado | `sudo ufw enable` |

### 🟡 Media Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `dig` | Consultas DNS detalladas | `dig google.com` |
| `nslookup` | Resolución de nombres DNS | `nslookup google.com` |
| `ifconfig` | Configuración de red (legacy) | `ifconfig eth0` |
| `iptables` | Reglas de firewall avanzadas | `sudo iptables -L` |
| `route` | Tabla de enrutamiento | `route -n` |
| `host` | Info DNS de un dominio | `host google.com` |

---

## 6. 💾 Sistema de Archivos y Discos

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `df` | Espacio en disco por partición | `df -h` |
| `mount` | Monta sistemas de archivos | `sudo mount /dev/sdb1 /mnt` |
| `umount` | Desmonta sistemas de archivos | `sudo umount /mnt` |
| `fdisk` | Administra particiones | `sudo fdisk -l` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `lsblk` | Lista dispositivos de bloque | `lsblk` |
| `blkid` | Info de UUID/tipo de partición | `blkid` |
| `mkfs` | Formatea una partición | `sudo mkfs.ext4 /dev/sdb1` |
| `fsck` | Verifica y repara sistemas de arch | `sudo fsck /dev/sda1` |
| `dd` | Copia byte a byte (imágenes) | `dd if=/dev/sda of=backup.img` |
| `tar` | Empaqueta y comprime archivos | `tar -czf backup.tar.gz /datos` |

### 🟡 Media Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `zip` / `unzip` | Comprime/descomprime ZIP | `zip -r archivo.zip carpeta/` |
| `gzip` / `gunzip` | Compresión gzip | `gzip archivo.txt` |
| `parted` | Gestión avanzada de particiones | `sudo parted /dev/sdb` |
| `ncdu` | Uso de disco interactivo | `ncdu /` |
| `smartctl` | Estado SMART del disco | `sudo smartctl -a /dev/sda` |

---

## 7. ⚙️ Servicios del Sistema (systemd)

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `systemctl start` | Inicia un servicio | `sudo systemctl start nginx` |
| `systemctl stop` | Detiene un servicio | `sudo systemctl stop nginx` |
| `systemctl restart` | Reinicia un servicio | `sudo systemctl restart nginx` |
| `systemctl status` | Estado de un servicio | `systemctl status nginx` |
| `systemctl enable` | Habilita inicio automático | `sudo systemctl enable nginx` |
| `systemctl disable` | Deshabilita inicio automático | `sudo systemctl disable nginx` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `journalctl` | Logs del sistema (systemd) | `journalctl -u nginx -f` |
| `systemctl list-units` | Lista todos los servicios | `systemctl list-units --type=service` |
| `systemctl daemon-reload` | Recarga configuración | `sudo systemctl daemon-reload` |
| `reboot` | Reinicia el sistema | `sudo reboot` |
| `shutdown` | Apaga el sistema | `sudo shutdown -h now` |

---

## 8. 🔍 Búsqueda y Texto

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `grep` | Busca patrones en texto | `grep -r "error" /var/log/` |
| `nano` | Editor de texto sencillo | `nano archivo.conf` |
| `vim` | Editor de texto avanzado | `vim archivo.conf` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `sed` | Edición de texto en flujo | `sed -i 's/viejo/nuevo/g' arch` |
| `awk` | Procesamiento de texto/columnas | `awk '{print $1}' archivo.txt` |
| `sort` | Ordena líneas de texto | `sort -n archivo.txt` |
| `uniq` | Elimina líneas duplicadas | `sort file.txt \| uniq` |
| `cut` | Extrae columnas de texto | `cut -d: -f1 /etc/passwd` |
| `head` / `tail` | Primeras/últimas líneas | `tail -f /var/log/syslog` |

### 🟡 Media Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `tr` | Traduce o elimina caracteres | `tr 'a-z' 'A-Z' < archivo` |
| `tee` | Duplica salida a archivo | `ls \| tee salida.txt` |
| `xargs` | Pasa argumentos a comandos | `find . -name "*.log" \| xargs rm` |
| `column` | Formatea en columnas | `column -t archivo.tsv` |

---

## 9. 📈 Monitoreo del Sistema

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `free` | Uso de memoria RAM | `free -h` |
| `uptime` | Tiempo encendido y carga | `uptime` |
| `uname` | Info del sistema operativo | `uname -a` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `vmstat` | Estadísticas de memoria/CPU/IO | `vmstat 1 5` |
| `iostat` | Estadísticas de E/S de disco | `iostat -xz 1` |
| `sar` | Historial de rendimiento | `sar -u 1 5` |
| `dmesg` | Mensajes del kernel | `dmesg | tail -20` |
| `lscpu` | Info del procesador | `lscpu` |
| `lshw` | Hardware detallado del sistema | `sudo lshw -short` |
| `lspci` | Dispositivos PCI | `lspci` |
| `lsusb` | Dispositivos USB | `lsusb` |

---

## 10. 🔐 Seguridad

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `ufw` | Firewall sencillo | `sudo ufw status` |
| `ssh-keygen` | Genera claves SSH | `ssh-keygen -t ed25519` |
| `sudo` | Elevación de privilegios | `sudo -l` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `fail2ban` | Bloqueo de IPs maliciosas | `sudo fail2ban-client status` |
| `openssl` | Criptografía y certificados | `openssl req -new -x509 ...` |
| `gpg` | Cifrado y firma digital | `gpg --encrypt archivo` |
| `chattr` | Atributos inmutables de archivos | `sudo chattr +i archivo.conf` |
| `auditd` | Auditoría del sistema | `sudo auditctl -l` |

---

## 11. 🛠️ Utilidades del Shell

### 🔴 Críticos

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `history` | Historial de comandos | `history | grep apt` |
| `alias` | Crea atajos de comandos | `alias ll='ls -la'` |
| `echo` | Imprime texto en pantalla | `echo "Hola Mundo"` |
| `export` | Define variables de entorno | `export PATH=$PATH:/ruta` |
| `env` | Muestra variables de entorno | `env` |

### 🟠 Alta Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `cron` / `crontab` | Tareas programadas | `crontab -e` |
| `at` | Tarea en momento específico | `at 14:30 < script.sh` |
| `screen` | Sesiones de terminal persistentes | `screen -S nombre` |
| `tmux` | Multiplexor de terminal avanzado | `tmux new -s sesion` |
| `man` | Manual de comandos | `man grep` |
| `which` | Ruta de un ejecutable | `which python3` |
| `type` | Tipo de comando (built-in/alias) | `type ls` |

### 🟡 Media Importancia

| Comando | Descripción | Ejemplo |
|---------|-------------|---------|
| `xclip` | Copia al portapapeles | `cat archivo.txt \| xclip` |
| `date` | Fecha y hora del sistema | `date '+%Y-%m-%d'` |
| `cal` | Muestra calendario | `cal 2025` |
| `bc` | Calculadora de línea de comandos | `echo "5*8" \| bc` |
| `tput` | Controla la terminal | `tput clear` |

---

## 🧠 Trucos y Combinaciones Útiles

```bash
# Ver los 10 procesos que más CPU consumen
ps aux --sort=-%cpu | head -11

# Buscar texto en múltiples archivos y mostrar número de línea
grep -rn "ERROR" /var/log/ --include="*.log"

# Monitorear logs en tiempo real con filtro
tail -f /var/log/syslog | grep -i "error"

# Liberar caché de memoria sin reiniciar
sudo sync && echo 3 | sudo tee /proc/sys/vm/drop_caches

# Ver puertos abiertos y sus procesos
sudo ss -tulnp

# Comprimir y transferir directorio vía SSH
tar -czf - /carpeta | ssh usuario@host "tar -xzf - -C /destino"

# Encontrar archivos modificados en las últimas 24 horas
find /var/www -mtime -1 -type f

# Contar líneas de código en proyecto
find . -name "*.py" | xargs wc -l | tail -1

# Reemplazar texto en múltiples archivos
find . -name "*.conf" -exec sed -i 's/antiguo/nuevo/g' {} +

# Backup rápido de archivo antes de editar
cp archivo.conf{,.bak}
```

---

## 📌 Atajos de Teclado en la Terminal

| Atajo | Acción |
|-------|--------|
| `Ctrl + C` | Interrumpe el proceso actual |
| `Ctrl + Z` | Suspende el proceso actual |
| `Ctrl + D` | Cierra la sesión (EOF) |
| `Ctrl + L` | Limpia la pantalla |
| `Ctrl + A` | Mueve al inicio de la línea |
| `Ctrl + E` | Mueve al final de la línea |
| `Ctrl + R` | Búsqueda en historial |
| `Ctrl + U` | Borra desde cursor al inicio |
| `Ctrl + K` | Borra desde cursor al final |
| `Tab` | Autocompletado |
| `!!` | Repite el último comando |
| `!$` | Último argumento del comando anterior |

---

## 📚 Recursos Recomendados

- **Manual integrado:** `man <comando>` — documentación oficial
- **Info pages:** `info <comando>` — documentación extendida
- **Ayuda rápida:** `<comando> --help`
- **tldr pages:** `tldr <comando>` — ejemplos simplificados (instalar: `sudo apt install tldr`)
- **Documentación oficial:** [ubuntu.com/server/docs](https://ubuntu.com/server/docs)

---

*Guía generada para Ubuntu 22.04 LTS / 24.04 LTS — Mayo 2025*
