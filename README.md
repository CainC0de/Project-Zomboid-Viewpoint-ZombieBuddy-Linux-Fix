# Project Zomboid: Viewpoint & ZombieBuddy Linux Fix

Repositório focado exclusivamente em documentar o processo de instalação e execução do mod **Viewpoint** (câmera 3D) em conjunto com o framework **ZombieBuddy** em sistemas Linux (Arch, Fedora e outras distribuições) para o Project Zomboid.

---

## 📌 Sobre o Projeto

Devido à forma como o Java e as interfaces gráficas (X11/Wayland) interagem no ambiente Linux, a injeção nativa do ZombieBuddy muitas vezes falha, não exibe o pop-up de segurança necessário ou apresenta o erro `JAR manifest missing`. 

Este repositório fornece a solução exata para injetar o mod manualmente e aprová-lo via terminal, permitindo que os jogadores de Linux utilizem a câmera 3D fluidamente e sem problemas.

## 🛠️ O que este guia aborda?

* **Extração e Execução Nativa:** Como utilizar o `ZombieBuddyInstaller-linux-amd64` corretamente via linha de comando.
* **Injeção do Java (JSON):** Configuração exata do arquivo `ProjectZomboid64.json` para garantir que o executável do jogo reconheça o parâmetro `-javaagent:ZombieBuddy.jar`.
* **Bypass de Interface Gráfica:** Como executar o script `projectzomboid.sh` diretamente pelo terminal para conseguir visualizar e aprovar (`Y`) a permissão de segurança do mod durante a tela de carregamento.
* **Organização de Diretórios:** Caminhos corretos para movimentação de arquivos `.jar` da pasta da Oficina da Steam para a raiz do jogo no Linux.

---

## ⚙️ Requisitos

* **Sistema Operacional:** Linux (Processo testado e homologado em Arch Linux e Fedora).
* **Versão do Jogo:** Project Zomboid na versão **Default Public Version** (Build 42.21 ou superior). 
* **Plataforma:** ⚠️ **O mod só funciona com a versão original do jogo na Steam.**

<img width="1128" alt="Configuração da Versão na Steam" src="https://github.com/user-attachments/assets/6d5d7db3-ef3a-4338-956f-de934dee88da" />

---

## 🔗 Links dos Mods (Oficina da Steam)

**Mods Obrigatórios:**
* 🧟‍♂️ [ZombieBuddy](https://steamcommunity.com/workshop/filedetails/?id=3619862853)
* 🎥 [Project Viewpoint](https://steamcommunity.com/sharedfiles/filedetails/?id=3810302175)
* 📦 [6244 3D models for Viewpoint [sour_kisel]](https://steamcommunity.com/sharedfiles/filedetails/?id=3809306528)
* [[B42] ZombieBuddy Extensions](https://steamcommunity.com/sharedfiles/filedetails/?id=3807686870)



---

## 🚀 Instalação Passo a Passo

### 1. Preparação e Download
1. Certifique-se de estar inscrito nos mods **ZombieBuddy**, **Viewpoint** e no pacote de **Modelos 3D** listados acima.
2. **Cancele a inscrição** no mod obsoleto `[B42] ZombieBuddy Extensions` caso o tenha instalado anteriormente.
3. Para baixar o instalador, vá até a seção **Releases** deste repositório (na lateral direita da página), clique na release **"Zombie Buddy"**, baixe o arquivo `ZombieBuddy-linux-test-v2.zip` e salve-o em um diretório de sua preferência no seu sistema.

### 2. Extração e Execução
Abra o seu emulador de terminal, navegue até a pasta onde o download foi feito e execute os comandos abaixo sequencialmente:

```bash
unzip ZombieBuddy-linux-test-v2.zip
cd ZombieBuddy-linux-test-v2
chmod +x ZombieBuddyInstaller-linux-amd64
./ZombieBuddyInstaller-linux-amd64
