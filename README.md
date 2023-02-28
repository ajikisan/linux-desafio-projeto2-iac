
### Infraestrutura como Código: Script de Provisionamento de um Servidor Web (Apache)
<p>Aluna: Mirian Ajiki Molicawa </p>
<p>Digital Innovation One </p>
<p>Instrutor: Denilson Bonatti </p>
<p>Data: 27/02/2023 </p>

--------------------------------------------------------------------------------------------------------------------------------------------------------
### Desafio: 
* Restaurar o snapshot criado anteriormente no virtualbox;
* Atualizar o servidor;
* Instalar o apache2;
* Instalar o unzip;
* Baixar a aplicação disponível no endereço https://github.com/denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip  no diretório /tmp
* Copiar os arquivos da aplicação no diretório padrão do apache
* Subir arquivo de script para um repositório no GitHub.

--------------------------------------------------------------------------------------------------------------------------------------------------------

root@LAPTOP-6BPS8238:/home/ajikisan# mkdir /tmp
mkdir: cannot create directory ‘/tmp’: File exists
root@LAPTOP-6BPS8238:/home/ajikisan# mkdir /script2
root@LAPTOP-6BPS8238:/script2# ls
root@LAPTOP-6BPS8238:/script2# nano script-iac2.sh
root@LAPTOP-6BPS8238:/script2# ls
script-iac2.sh
root@LAPTOP-6BPS8238:/script2# chmod +x script-iac2.sh
root@LAPTOP-6BPS8238:/script2# ./script-iac2.sh
Atualizado o servidor...
Get:1 http://security.ubuntu.com/ubuntu focal-security InRelease [114 kB]
Get:2 http://archive.ubuntu.com/ubuntu focal InRelease [265 kB]
...
Fetched 27.5 MB in 54s (509 kB/s)
Reading package lists... Done
Building dependency tree
Reading state information... Done
Calculating upgrade... Done
The following packages have been kept back:
  base-files fwupd libfwupd2 libfwupdplugin1 libgl1-mesa-dri libglapi-mesa libglx-mesa0 mesa-vulkan-drivers sosreport
  ubuntu-advantage-tools ubuntu-server
The following packages will be upgraded
...
287 upgraded, 0 newly installed, 0 to remove and 11 not upgraded.
Need to get 135 MB of archives.
After this operation, 70.6 MB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu focal-updates/main amd64 bash amd64 5.0-6ubuntu1.2 [639 kB]
...
Fetched 135 MB in 4min 9s (542 kB/s)
Extracting templates from packages: 100%
Preconfiguring packages ...
(Reading database ... 31836 files and directories currently installed.)
Preparing to unpack .../bash_5.0-6ubuntu1.2_amd64.deb ...
Unpacking bash (5.0-6ubuntu1.2) over (5.0-6ubuntu1) ...
Setting up bash (5.0-6ubuntu1.2) ...
update-alternatives: using /usr/share/man/man7/bash-builtins.7.gz to provide /usr/share/man/man7/builtins.7.gz (builtins.7.gz) in auto mode
(Reading database ... 31836 files and directories currently installed.)
...
Baixando e copiando  os arquivos da aplicação ...
--2023-02-27 21:10:38--  https://github.com/denilsonbonatti/linux-site-dio/archive/refs/heads/main.zip
Resolving github.com (github.com)... 20.201.28.151
Connecting to github.com (github.com)|20.201.28.151|:443... connected.
Connecting to codeload.github.com (codeload.github.com)|20.201.28.149|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 17218148 (16M) [application/zip]
Saving to: ‘main.zip’
main.zip                      100%[=================================================>]  16.42M   805KB/s    in 22s
...
  inflating: linux-site-dio-main/vendor/themify-icons/index.html
  inflating: linux-site-dio-main/vendor/themify-icons/readme.txt
  inflating: linux-site-dio-main/vendor/themify-icons/themify-icons.css
Fim do script...
