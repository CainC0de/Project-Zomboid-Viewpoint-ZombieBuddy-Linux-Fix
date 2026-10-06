# Project-Zomboid-Viewpoint-ZombieBuddy-Linux-Fix
Repositório focado exclusivamente em documentar o processo de instalação e execução do mod Viewpoint (câmera 3D) em conjunto com o framework ZombieBuddy em sistemas Linux (Arch, Fedora e outras distribuições) para o Project Zomboid (Build 42+).
📌 Sobre o Projeto
Devido à forma como o Java e as interfaces gráficas (X11/Wayland) interagem no Linux, a injeção nativa do ZombieBuddy muitas vezes falha, não exibe o pop-up de segurança necessário ou apresenta o erro JAR manifest missing. Este repositório fornece a solução exata para injetar o mod manualmente e aprová-lo via terminal, permitindo que os jogadores de Linux utilizem a câmera 3D sem problemas.

🛠️ O que este guia/fix aborda?
Extração e Execução Nativa: Como utilizar o ZombieBuddyInstaller-linux-amd64 corretamente via terminal.

Injeção do Java (JSON): Configuração correta do arquivo ProjectZomboid64.json para garantir que o executável do jogo reconheça o -javaagent:ZombieBuddy.jar.

Bypass de Interface Gráfica: Como executar o script projectzomboid.sh diretamente pelo terminal para conseguir visualizar e aprovar (Y) a permissão de segurança do mod durante o carregamento do mapa.

Organização de Diretórios: Caminhos corretos para mover o arquivo .jar da pasta da Oficina da Steam para a raiz do jogo no Linux.

⚙️ Requisitos
Sistema Operacional Linux (Testado em Arch Linux e Fedora)

Project Zomboid na versão (Default Public Version) (Build 42.21 ou superior) -- O MOD SÓ FUNCIONA COM O JOGO DA STEAM
<img width="1128" height="343" alt="image" src="https://github.com/user-attachments/assets/6d5d7db3-ef3a-4338-956f-de934dee88da" />


LINK DOS MODS 
https://steamcommunity.com/sharedfiles/filedetails/?id=3810302175
https://steamcommunity.com/sharedfiles/filedetails/?id=3807686870
https://steamcommunity.com/workshop/filedetails/?id=3619862853
https://steamcommunity.com/sharedfiles/filedetails/?id=3809306528 

Project Viewpoint
[B42] ZombieBuddy Extensions
6244 3D models for Viewpoint [sour_kisel]
ZombieBuddy 
