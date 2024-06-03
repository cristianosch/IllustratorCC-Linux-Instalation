  <img height="170em" width="400" src="image.jpg"/>

# Como instalar Adobe Illustrator no Linux Ubuntu

- Instalar o Wine e Dependencias 

**1. Adicionar o Repositório do Wine:**

<p>sudo dpkg --add-architecture i386</p>
<p>sudo mkdir -pm755 /etc/apt/keyrings</p>
<p>wget -O - https://dl.winehq.org/wine-builds/winehq.key | sudo tee /etc/apt/keyrings/winehq-archive.key</p>
<p>sudo wget -NP /etc/apt/sources.list.d/ https://dl.winehq.org/wine-builds/ubuntu/dists/$(lsb_release -cs)/winehq-$(lsb_release -cs).sources</p>


**2. Instalar Wine:**

<p>sudo apt update</p>
<p>sudo apt install --install-recommends winehq-stable</p>


**3. Instalar Winetricks (Ferramenta para Instalar Componentes Adicionais):**

<p>sudo apt install winetricks</p>


# Passo 2: Configurar o Wine

**1. Configurar o Wine:**

<p>Execute o comando winecfg para abrir a configuração do Wine e faça o seguinte:</p>

    Na aba Applications, defina a versão do Windows para Windows 10.
    Na aba Libraries, adicione as seguintes bibliotecas e defina-as como native, builtin:
        gdiplus
        msxml6
        vcrun2010
        atmlib
        msvcr100
        msvcr120
    Na aba Graphics, marque as opções:
        Emulate a virtual desktop (com uma resolução apropriada, por exemplo, 1920x1080).
        Allow the window manager to decorate the windows.
        Allow the window manager to control the windows.
        
**2. Instalar Componentes Adicionais com o Winetricks:**

<p>Execute os seguintes comandos para instalar componentes adicionais:</p>

<p>winetricks gdiplus</p>
<p>winetricks msxml6</p>
<p>winetricks vcrun2010</p>
<p>winetricks atmlib</p>
<p>winetricks msvcr100</p>
<p>winetricks msvcr120</p>


**3. Instalar o Illustrator**

git clone https://github.com/Gictorbit/illustratorCClinux.git

**Executar o Script de Instalação:**

cd illustratorCClinux

- Torne o script executável:

chmod +x setup.sh

- Execute o script de configuração:

./setup.sh

OPÇÃO 1

Windows 10         OK

PROCESSO CONCLUIDO





