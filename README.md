# Shedule


hostnamectl set-hostname isp.au-team.irpo
exec bash

После перезапускаем интерфейс ens3 и командой ip –c —br a смотрим наш
IP адрес Интернета (он будет использоваться для шлюзов).IP


Для добавления нового пользователя используем команды useradd и passwd
useradd sshuser -u 1010 -U
passwd sshuser
usermod –aG sudo sshuser
Для беспарольного доступа к sudo заходим в /etc/sudoers, командой
nano /etc/sudoers (или просто команда visudo) и пишем там строку
sshuser ALL=NOPASSWD: ALL
useradd net_admin -U
passwd net_admin
usermod –aG sudo net_admin
В /etc/sudoers
net_admin ALL=(ALL) NOPASSWD: ALL
Выполняем вход под пользователем net_admin (login net_admin) и
выполняем sudo -i или другие команды требующую повышения привелегий
до root


