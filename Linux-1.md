![linux-logo](./img/linux-logo.png)

# Linux - 11

  - [Provisionando o Ambiente](#provisionando-o-ambiente)
    - [Virtual Box](#virtual-box)
    - [Vagrant](#vagrant)
  - [Breve História](#breve-história)
    - [Início do Linux](#início-do-linux)
    - [FOSS](#foss)
  - [Inicialização do Sistema](#inicialização-do-sistema)
    - [Introdução](#introdução)
    - [Gerenciando Serviços](#gerenciando-serviços)
    - [Systemd](#systemd)
  - [File System](#file-system)
    - [Arquitetura de diretórios](#arquitetura-de-diretórios)
  - [Comandos Essenciais](#comandos-essenciais)
    - [Linha de comando](#linha-de-comando)
    - [Documentações e Filtros](#documentações-e-filtros)
    - [Redirecionamento](#redirecionamento)
    - [Pesquisas e REGEX](#pesquisas-e-regex)
  - [Editores de Texto](#editores-de-texto)
    - [Overview dos editores](#overview-dos-editores)
    - [VIM](#vim)
  - [Shell](#shell)
    - [Tipos de Shell](#tipos-de-shell)
    - [Configurações do Bash](#configurações-do-bash)
  - [Empacotadores e Compressão](#empacotadores-e-compressão)
    - [Empacotamento com TAR](#empacotamento-com-tar)
    - [Tipos de compressão](#tipos-de-compressão)
    - [Empacotando e Comprimindo](#empacotando-e-comprimindo)
  - [Instalação de Programas](#instalação-de-programas)
    - [Gerenciadores de Pacotes](#gerenciadores-de-pacotes)
    - [DPKG e RPM](#dpkg-e-rpm)
    - [APT e YUM](#apt-e-yum)
    - [Compilação de Pacotes](#compilação-de-pacotes)
  - [Gerenciamento de Usuários](#gerenciamento-de-usuários)
    - [Administração de usuários](#administração-de-usuários)
    - [Gerenciamento de Permissões](#gerenciamento-de-permissões)
    - [Configurando SUDO](#configurando-sudo)
  - [Gerenciamento de Redes](#gerenciamento-de-redes)
    - [Configuração de Interfaces](#configuração-de-interfaces)
    - [Rotas estáticas](#rotas-estáticas)
    - [Resolução de Nomes](#resolução-de-nomes)
    - [DHClient](#dhclient)
  - [Acesso Remoto](#acesso-remoto)
    - [Conceitos de Acesso Remoto](#conceitos-de-acesso-remoto)
    - [Conceitos de Criptografia](#conceitos-de-criptografia)
    - [SSH e Chaves RSA](#ssh-e-chaves-rsa)
  - [Gerenciamento de Logs, Time Zone e NTP](#gerenciamento-de-logs-time-zone-e-ntp)
    - [Arquivos de logs](#arquivos-de-logs)
    - [RSyslog](#rsyslog)
    - [Time Zone](#time-zone)
    - [NTP](#ntp)
  - [Gerenciamento de Processos](#gerenciamento-de-processos)
    - [Introdução à Processos](#introdução-à-processos)
    - [Pesquisas e Filtros de Processos](#pesquisas-e-filtros-de-processos)
    - [Planos e Prioridades](#planos-e-prioridades)
  - [Gerenciamento de Dispositivos e Discos](#gerenciamento-de-dispositivos-e-discos)
    - [Gerenciamento de Dispositivos](#gerenciamento-de-dispositivos)
    - [Gerenciamento de Discos e Pontos de Montagem](#gerenciamento-de-discos-e-pontos-de-montagem)
    - [LVM](#lvm)
  - [Shell Script e Cron](#shell-script-e-cron)
    - [Conceitos de Shell Script](#conceitos-de-shell-script)
    - [Agendamento de tarefas com Crontab](#agendamento-de-tarefas-com-crontab)
  - [Conteúdo complementar:](#conteúdo-complementar)
    - [Livros:](#livros)
    - [Regex:](#regex)
    - [Shell:](#shell-1)
    - [VIM](#vim-1)
    - [SIMULADO LPI 1](#simulado-lpi-1)

## Provisionando o Ambiente
### Virtual Box
### Vagrant

---

## Breve História
### Início do Linux
### FOSS

---

## Inicialização do Sistema
### Introdução
### Gerenciando Serviços
### Systemd

BIOS > Bootloader-1 (MBR) > Bootloader-2 (GRUB) > Kernel > INIT

rc0 = 
rc1 = 
rc2-5 = 
rc6 = 

service = 
systemctl = 
insserv = 

/lib/systemd/system/ = 

---

## File System
### Arquitetura de diretórios

---

## Comandos Essenciais
### Linha de comando

- whoami = mostra o usuário corrente

- last = mostra os ultimos usuários conectados

- passwd = alteração de senha

- hostname = mostra o nome da máquina

- uname = informações do kernel / SO

- ifconfig / ip a = informações de rede

- sudo = elevação de permissão

- ls = listagem de diretórios e arquivos

- pwd = diretório corrente

- cat = mostra o conteúdo de um arquivo

- mkdir = criação de diretórios

- touch = criação de arquivos em branco | alteração de data de modificação do arquivo

- tree = mostra os níveis dos diretórios e arquivos

- stat = status de arquivos | tipo de arquivo | tamanho | criação, modificação...

- cp = copiar

- file = tipo arquivo

- mv = mover | renomear

- rm = remover arquivo

- rmdir = remover diretórios em branco

- ln = criação de atalhos

- unlink = remoção de atalhos

- clear ou ctrl+l = limpa a tela do bash

- ctrl+r ou setas = busca comandos já executados

### Documentações e Filtros

man = Manual dos comandos, contendo descrição e os parametros possiveis

mandb = Criar ou atualizar o cache dos manuais

help = Ajuda sintetizada sobre o comando

apropos ou man -k = Mostra o propósito do comando

wc = Contagem bytes, palavras, linhas, etc..

head = Pega as primeiras 10 linhas de um arquivo ou saida de um comando

tail = Mesma coisa que o head, porém com o final do conteúdo

sort = Ordena a saída

tr = Transforma minusculo em maiusculo

cut = Filtrar com delimitador e pegar somente os campos desejados

awk = Filtrar com delimitador e pegar somente os campos desejados

locate = Verficar a localização de um arquivo

grep - egrep = Filtros por palavra chave

diff = Visualizar a diferença entre os arquivos


### Redirecionamento

- > = Direcionar a saida padrão (stdout) de um comando
- >> = Concatenar a saida de um comando
- 2> = Direcionando a saida de erro (stderr)
- 2>&1 = Direcionar a saída de erro para o mesmo destino da saida padrão


### Pesquisas e REGEX

---

## Editores de Texto
### Overview dos editores
### VIM

vimtutor = Manual

:q = sair
:q! = sair sem salvar
:w = salvar
:x = salvar e sair
ZZ = salvar e sair
gg = vai para o topo do arquivo
yy = copia a linha
G = vai para o final do arquivo
p = Cola
cc = Recortar
dd = Recortar ou Deletar
ESC ou  crtl+c = Sair do modo de inserção
i ou insert = Entrar no modo de inserção
/ ou ? = Abre uma busca no VIM
vim -O = Permite abrir 2 ou mais arquivos simultâneos, divididos horizontalmente
ctrl+ww = Alternar entre os arquivos abertos simultâneamente
:set = Permite habilitar ou desabilitar funções do VIM
:syntax = Habilita ou desabilita interpretação do conteúdo e coloração
:! = Permite executar comando no bash sem sair do VIM
:r = Permite trazer o conteúdo de saida de um comando para dentro do arquivo no VIM

---

## Shell
### Tipos de Shell
### Configurações do Bash

Local = Só é válida para aquela sessão de shell de um usuário
Global = Será válida para todas as sessões de shell de um usuário

export = Deixar a variável de modo global
set = Lista as variáveis locais e globais
unset = Remover variáveis
env = Lista as variáveis globais

$SHLVL = Armazena o nivel de sessão shell
$PATH = Armazena o valor dos diretórios que contem os binários dos comandos
$USER = Armazena o nome do usuário corrente
$PWD = Armazena o diretório corrente
$SHELL = Armazena o tipo shell padrão
$EDITOR = Armazena o valor do editor de texto padrão

/etc/profile = Contem todas as configurações de shell comum para os usuários
.profile = Único por usuário e contem configurações de shell dele
.bash_login = Mensagem de boas vindas por usuário
.bashrc = Contem configurações de shell do usuário corrente
.bash_logout = Mensagens/Baner ou ações após a saída do shell


source = Serve para carregar as informações atualizadas de um arquivo de configuração
alias = Apelido, para transformar uma palavra qualquer em um comando

---

## Empacotadores e Compressão
### Empacotamento com TAR
### Tipos de compressão
### Empacotando e Comprimindo

tar = empacotador
cpio = empacotador (desenvolvido para backup)
zip = Compressão de arquivos
gzip = algoritmo para compressão de arquivos
bzip2 =algoritmo para compressão de arquivos (Taxa de compressão mais alta, porém leva mais tempo) 
unzip = Descompressão de arquivos
gunzip = descompressão de arquivos GZIP
bunzip2 = descompressão de arquivos BZIP2

---

## Instalação de Programas
### Gerenciadores de Pacotes
### DPKG e RPM
### APT e YUM
### Compilação de Pacotes

dpkg = Gerenciador de pacotes de baixo nível para sistemas baseados em Debian
rpm = Gerenciador de pacotes de baixo nível para sistemas baseados em Red Hat
apt = Gerenciador de pacotes de alto nível para sistemas baseados em Debian
yum = Gerenciador de pacotes de alto nível para sistemas baseados em Red Hat
alien = Programa utilizado para transformar um pacote .DEB para .RPM <>
rpmrebuild = Validar a compilação do pacote RPM

rpmrebuild -pe dateutils-0.4.1-2.x86_64.rpm

rpm -Uvh rpmbuild/RPMS/x86_64/dateutils-0.4.1-2.x86_64.rpm 

lstop = Visualização do consumo de recursos
htop = Visualização do consumo de recursos com mais recursos gráficos
tar = Empacotamento

---

## Gerenciamento de Usuários

adduser = Cria novos usuário
userdel = Deleta usuários
usermod = Altera as propriedades de um usuário
chage = Configurar as políticas de senha
who - w = Mostra todos os usuários logados naquele momento
finger = Mostra informações detalhadas do usuário
id = Mostra id do usuário
groups = Mostra os grupos que um usuário pertence
getent = Mostra/Captura dados dos arquivos de base de dados do sistema, ex: passwd, shadow, groups, hosts...

### Administração de usuários

/etc/passwd lala
/etc/shadow = Contem as senhas dos usuários
/etc/groups = Contem as informações dos grupos do sistema
/etc/gshadow = Contem as senhas dos grupos
/etc/login.defs = Contem as definições de login dos usuários
/etc/skel/ = Contem a hierarquia de diretórios e arquivos da home dos usuários (template)

getent = Mostra/Captura dados dos arquivos de base de dados do sistema, ex: passwd, shadow, groups, hosts...
id = Mostra id do usuário
groups = Mostra os grupos que um usuário pertence
finger = Mostra informações detalhadas do usuário
who - w = Mostra todos os usuários logados naquele momento
adduser = Cria novos usuário
userdel = Deleta usuários
usermod = Altera as propriedades de um usuário
chage = Configurar as políticas de senha

groupadd = Cria um grupo
gpasswd = Adiciona usuários à um grupo
chown = Altera o owner(dono) de um diretório/arquivo
chgrp = Alterar o grupo owner de um diretório/arquivo

### Gerenciamento de Permissões

r = 4
w = 2
x = 1

umask = define o padrão de permissões para criação de diretórios e arquivos
suid bit = Herdar as permissões do owner de um binário na hora da execução
sgid bit = Permite a herança de permissões em diretórios
stick bit = Restingir a deleção de objetos para para o owner

### Configurando SUDO

/etc/sudoers = Configuração dos limites de execução de comandos dos usuários

---

## Gerenciamento de Redes
### Configuração de Interfaces
### Rotas estáticas
### Resolução de Nomes
### DHClient

ifconfig =  listar as interfaces e suas configurações
mii-tool = mostra o status detalhados de uma interface
route = gerencia da tabela de rotas
ethtool = mostra o status detalhados de uma interface
ip = Gerenciar as configurações de rede
dhclient = Buscar um novo ip dinamicamente no servidor de DHCP

/etc/hosts = Contem a relação de ip/fqdn inseipconfig
ipcinfigrida manualmente
/etc/resolv.conf = Conter as informações de servidor DNS e domínio
/etc/nsswitch.conf = Contem a ordem que o sistema operacional irá tentar resolver os nomes
/etc/hostname = Contem o nome da máquina

/etc/network/interfaces/ = Debian
/etc/sysconfig/network-s/ = CentOS/Red Hat


---

## Acesso Remoto
### Conceitos de Acesso Remoto
### Conceitos de Criptografia
### SSH e Chaves RSA

ssh = Protocolo "Secure Shell"
rsync = Utilitário para realizar sincronização entre diretórios locais e/ou remotos

openssh = Pacote para instalação do SSH

~/.ssh/known_hosts = Arquivo que armazena o fingerprint dos hosts já acessados
~/.ssh/authorized_keys = Arquivo que armazena as chaves públicas copiadas
/etc/ssh/ssh_config = Arquivo de configuração do cliente SSH
/etc/ssh/sshd_config = Arquivo de configuração do servidor SSH

ssh-keygen = Comando para gerar par de chaves criptográficas
ssh-copy-id = Copia a chave pública para o servidor remoto

/etc/hosts.allow = Lista de permissão para utilização de serviços
/etc/hosts.deny = Lista de restrição para utilização de serviços

---

## Gerenciamento de Logs, Time Zone e NTP
### Arquivos de logs

dmesg = Contem as informações de hardware mapeadas pelo kernel
messages = Contem todas as informações de aplicações e serviços
lastlog = Contem as informações de login de usuários
wtmp = Contem as informações de queme stá logado no momento
auth.log = Contem as informações sobre autenticação e alteração de usuário

### RSyslog

logrotate = Comando para realizar a rotação de log manualmente

/etc/rsyslog.conf = Arquivo principal de configuração do RSYSLOG 
/etc/logrotate.d/ = Diretório para aramazenar arquivos de configuração adicional para o logrotate

### Time Zone

locale-gen = Habilitar ou desabilitar idioma e localização
dpkg-reconfigure locales = Habilitar ou desabilitar idioma e localização
update-locale = Configura o idioma e localização
timedatectl = Listar/Configurar as configurações de local, data e hora
TZ = Variável que contem o valor de timezone

### NTP

ntp = Network Time Protocol
hwclock = Sincronizar o horário da BIOS com o  do sistema operacional
date = Visualizar a data e/ou configurar uma data e hora
ntpdate = Sincroniza o horário com o servidor NTP

/etc/ntp.conf = Arquivo de configuração do NTP

---

## Gerenciamento de Processos
### Introdução à Processos
### Pesquisas e Filtros de Processos

ps = Lista os processos em execução
pstree = Lista os processos em execução com a visualização de árvore
pgrep = Procura por uma parte do nome do processo e mostra o PID
pidof = Mostra o PID do processo, porém é só procurar pelo nome completo
lsof = Lista os arquivos abertos
kill = Envia sinais de controle para os processos
pkill = Permite tratar um processo colocando apenas uma parte do nome

### Planos e Prioridades

jobs = Lista os programas executando em segundo plano
fg = Envia o programa para o primeiro plano
bg = Executa os comandos parados em segundo plano
nohup = Inicia um programa em segundo plano sem prender a sessão de terminal
nice = Inicia um programa com a prioridade alterada
renice = Altera a prioridade de um programa em execução


---

## Gerenciamento de Dispositivos e Discos
### Gerenciamento de Dispositivos

devfs = Gerenciador de dispositivos que cria todos os arquivos de dispositivos no boot
udev = Gerenciador de dispositivos dinâmico que cria os arquivos apenas quando este é acionado

/proc/cmdline = Argumentos passados para Kernel pelo loader (Grub)
/proc/cpuinfo = Informações específicas sobre processador
/proc/filesystems = Sistemas de arquivos suportados pelo Kernel
/proc/interrupts = Informações sobre o número de interrupções e seus dispositivos
/proc/meminfo = Informações sobre memória da máquina
/proc/modules = Informações sobre módulos carregados na memória
/proc/partitions = Partições conhecidas pelo sistema
/proc/uptime = Tempo que o sistema está ligado

lspci (pciutils) = Mostra os dispositivos integrados ao barramento PCI
lsusb (usbutils)= Mostra os dispositivos conectados ao barramento USB
lsmod = Lista os módulos ativos no sistema pelo Kernel

### Gerenciamento de Discos e Pontos de Montagem

fdisk = Programa para criação e manipulação de tabelas de partições (GPT, MBR, Sun, SGI e BSD)
cfdisk = Programa para criação e manipulação de tabelas de partições (GPT, MBR, Sun, SGI e BSD)
gdisk = Programa para criação e manipulação de tabelas de partições GPT
partprobe = Reeleitura da tabela de particionamento sem precisar de reinicialização

ext2 = Um dos primeiros filesystem do Linux
ext3 = Idêntico ao ext2 porém com função de journal
ext4 = Evolução do ext3 tratando arquivos maiores e com funções adicionais
xfs = Melhor tratamento com objetos grandes, indicado para banco de dados por sua performance
swap = Parte do disco utilizado como "RAM"

mkfs.*** = Formata uma partição com um filesystem escolhido
mkswap = Formata uma partição de swap
mount = Lista e configura pontos de montagem
umount = Realiza a desmontagem
df = 
du = 
swapon = 
swapoff = 
sysctl = 
blkid = 
lsblk = 
tune2fs = 
e2fsck = 
/etc/fstab = 
autofs = 
cryptsetup = 
cryptfs = 
modprobe = 

### LVM

---

## Shell Script e Cron
### Conceitos de Shell Script

1 - Primeira linha deve conter o interpretador shell
2 - Permissão de execução no arquivo
3 - Por convenção inserir ".sh" no nome do arquivo

echo = Exibe um texto na saída padrão
sleep = aguarda um período de tempo para execução do comando seguinte
read = recebe o valor de uma variável
& = executa o comando em segundo plano
exit = sai do 

\$1 = Valor do primeiro parâmetro
\$* = Valor de todos os parâmetros
\$# = Quantidade de parâmetros passados
\$0 = Nome do 
\$? = exibe o código de retorno do comando

-eq = num1 -eq num2 : num1 é igual a num2 (equal to)
-ne = num1 -ne num2 : num1 não é igual a num2 (not equal to)
-gt = num1 -gt num2 : num1 é maior que num2 (greater than)
-ge =num1 -ge num2 : num1 é maior ou igual a num2 (greater or equal)
-lt = num1 -lt num2 : num1 é menor que num2 (less than)
-le = num1 -le num2 : num1 é menor ou igual a num2 (less or equal)

-e = O arquivo existe (exists)
-nt = O arquivo é mais novo que (newer than)
-ot = O arquivo é mais antigo que (older than)
-d = O diretório existe

test = Teste condicional
if = Utilizamos operações lógicas, permitindo que o  tome decisões, ou seja, que exceções sejam tratadas
case = Utilizado para comandos de fluxo, tal como o if, porém enquanto if testa expressões não exatas, "case" agirá de acordo com resultados exatos
while = Acontecerá execução enquanto a condição for verdadeira
for = Para cada valor recebido será feito o que for determinado

### Agendamento de tarefas com Crontab

time = exibe o tempo gasto na execução de um comando
at = agendamentos únicos de tarefas
atq = exibe a fila de agendamento do AT
cron = agendador de tarefas recorrentes, nativo no Linux
crontab = arquivo de configuração para agendar as tarefas
run-parts = Teste de execução das tarefas no cron

---

## Conteúdo complementar:

- [Guia Foca Linux](https://www.guiafoca.org/)

### Livros:

- [Sistemas Operacionais](https://www.amazon.com.br/Sistemas-operacionais-modernos-Andrew-Tanenbaum/dp/8543005671/ref=sr_1_1?index.html__mk_pt_BR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=SVTT0WMQRSEE&dchild=1&keywords=sistema+operacional&qid=1612300968&s=books&sprefix=sistema+operaci%2Cstripbooks%2C263&sr=1-1)

- [Linux A Biblia](https://www.amazon.com.br/Linux-B%C3%ADblia-Christopher-Negus/dp/8576087995)

- [LPIC-1](https://www.amazon.com.br/Certifica%C3%A7%C3%A3o-LPI-1-Luciano-Antonio-Siqueira/dp/8550810614/ref=sr_1_1?__mk_pt_BR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=lpi&qid=1612301022&s=books&sr=1-1)


- [Shell - 1](https://www.amazon.com.br/-Profissional-Aurelio-Marinho-Jargas/dp/8575221523/ref=pd_bxgy_img_3/140-0347945-3566272?_encoding=UTF8&pd_rd_i=8575221523&pd_rd_r=68f0b5ed-064a-4134-ad01-8c2925b77b4d&pd_rd_w=2E1WI&pd_rd_wg=1xiq8&pf_rd_p=400138fd-99e3-44de-aed2-5a7aff7ca010&pf_rd_r=N8D8ST00FMK71Q65Y76P&psc=1&refRID=N8D8ST00FMK71Q65Y76P)

- [Shell - 2](https://www.amazon.com.br/Programa%C3%A7%C3%A3o-Shell-Linux-Julio-Cezar/dp/8574528331/ref=sr_1_2?__mk_pt_BR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&dchild=1&keywords=shell+&qid=1612301124&s=books&sr=1-2)

### Regex:

- https://regex101.com/
- https://pythex.org/
- https://regexr.com/

### Shell:

- [https://explainshell.com/](https://explainshell.com/) -> explicação de comando do shell
- [https://cheat.sh/](https://cheat.sh/) -> exemplos de utilização de comandos
- [https://tldr.sh/](https://tldr.sh/) -> páginas de manual resumidas
- [https://cmdchallenge.com](https://cmdchallenge.com) -> desafios de shell gameficados
- [https://www.redhat.com/en/command-line-heroes/bash/index.html](https://www.redhat.com/en/command-line-heroes/bash/index.html) -> desafios de shell da Red Hat


### VIM
https://vim-adventures.com/

### SIMULADO LPI 1
https://www.udemy.com/course/simulado-certificacao-lpic-1-e-comptia-linux/
