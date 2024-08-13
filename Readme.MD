# EduHub

### Backend
O repositório Backend do EduHub é a base da plataforma de gerenciamento de cursos, construída com Ruby on Rails. Esta aplicação robusta e escalável fornece APIs RESTful para gerenciar cursos e arquivos associados. O sistema inclui gerenciamento de uploads de arquivos, e cálculo de métricas, como o espaço ocupado por curso.

- Tecnologias: 
    - Ruby
    - Rails
    - Sqlite
    - Docker

- Funcionalidades:
    - Criação, leitura, atualização e exclusão (CRUD) de cursos
    - Gestão de arquivos de cursos, incluindo upload e cálculo por tamanho do conteudo do curso
    - Configuração para deploy em ambientes Docker

### Frontend

O repositório Frontend do EduHub é a interface de usuário interativa e responsiva da plataforma de gerenciamento de cursos, desenvolvida com React, Typescript e Vite. Utilizando ChakraUI para estilização e componentes visuais, o frontend proporciona uma experiência de usuário fluida e intuitiva. Ele consome as APIs fornecidas pelo backend, permitindo a interação completa com o sistema de gerenciamento de cursos, incluindo o cadastro e visualização de cursos, upload de arquivos, e monitoramento de métricas.

- Tecnologias: 
    - Typescript
    - React
    - Vite
    - ChakraUI

- Funcionalidades:
    - Interface de usuário responsiva e amigável para gerenciamento de cursos
    - Consumo de APIs RESTful para exibir e manipular dados de cursos
    - Gerenciamento de arquivos, incluindo upload e visualização
    - Design moderno e acessível com ChakraUI

### Passo a passo de inicialização

## Instalação do Git no Windows

- Baixar o instalador do Git

> Acesse o site oficial do Git: Git for Windows. O download deve começar automaticamente. Se não, clique no link de download.

- Instalar o Git

> Abra o arquivo .exe que você baixou. Siga o assistente de instalação.

- Após a instalação, abra o Git Bash (procure por "Git Bash" no menu Iniciar).

- Digite o seguinte comando para verificar a instalação:

````
git --version
````

- Se o Git foi instalado corretamente, ele exibirá a versão instalada.

#### Instalação do Git no MacOS
Instalar via Homebrew (Recomendado):

Se você já tem o Homebrew instalado, basta executar:

````
brew install git
````

- Se você ainda não tem o Homebrew, instale-o primeiro executando o seguinte comando no terminal:

````
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
````

- Depois, instale o Git

````
brew install git
````

- Verifique a instalação. Abra o Terminal e digite:

````
git --version
````

- A versão instalada do Git será exibida.

#### Instalação do Git no Linux

>A instalação do Git no Linux pode variar de acordo com a distribuição que você está usando.

- Ubuntu/Debian:

- Abra o Terminal e atualize os pacotes do sistema:

````
sudo apt-get update
sudo apt-get install git
git --version
````

#### Fedora

- Abra o Terminal e instale o Git

````
sudo dnf install git
git --version
````

- Arch Linux

- Abra o Terminal e instale o Git

````
sudo pacman -S git
````


## Instalar o Docker

>Se você não tem o Docker instalado, siga os passos abaixo para instalá-lo no seu sistema operacional:

#### Windows/MacOS:

- Acesse o site oficial do Docker e baixe o Docker Desktop: Docker Desktop.

- Siga o assistente de instalação para instalar o Docker Desktop.

- Após a instalação, abra o Docker Desktop e verifique se o Docker está rodando corretamente.

#### MacOS

- Execute o seguinte comando no homebrew:

````
brew install --cask docker
````

- Iniciar o Docker Desktop:

>Após a instalação, abra o Docker Desktop. Você pode encontrá-lo na pasta Applications ou usar o Spotlight para buscar por "Docker".
Clique duas vezes no ícone do Docker para iniciar o Docker Desktop.
Pode ser necessário conceder permissões durante o processo inicial de configuração.

- Verificar se o Docker está em execução:

- Você verá o ícone do Docker na barra de menu superior, indicando que o Docker Desktop está rodando.

- Verificar a Instalação do Docker. Abra o Terminal e digite o seguinte comando:

````
docker --version
````

> Isso deve retornar a versão do Docker instalada, confirmando que a instalação foi bem-sucedida.

#### Linux (Ubuntu/Debian):

- Atualize os pacotes do sistema:

````
sudo apt-get update
sudo apt-get upgrade
````

Instale o Docker:

````
sudo apt-get install docker.io
````

- Inicie o serviço do Docker e configure-o para iniciar automaticamente:

````
sudo systemctl start docker
sudo systemctl enable docker
````

- Verifique se o Docker está instalado corretamente:

````
docker --version
````

### Instalar o Docker Compose

>O Docker Compose é uma ferramenta para definir e gerenciar aplicações multi-container.

#### Windows/MacOS:

>O Docker Compose já vem incluído no Docker Desktop, então não é necessário instalá-lo separadamente.

#### Linux (Ubuntu/Debian):

- Baixe a versão mais recente do Docker Compose:

````
sudo curl -L "https://github.com/docker/compose/releases/download/v2.20.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
````

- Dê permissão de execução ao binário do Docker Compose:

````
sudo chmod +x /usr/local/bin/docker-compose
````

- Verifique se o Docker Compose foi instalado corretamente:

````
docker-compose --version
````

#### Preparar o Projeto

>Certifique-se de que você tem os diretórios ./BackEndEduHub e ./FrontEndEduHub com os respectivos arquivos Dockerfile e código-fonte dentro deles.

### Rodar o Docker Compose

>Com o docker-compose.yml configurado e o Docker/Docker Compose instalados, siga os passos abaixo:

- Abra um terminal (ou o prompt de comando no Windows) e navegue até o diretório onde está o arquivo docker-compose.yml.
Construa e inicie os containers com o seguinte comando:

````
docker-compose up --build
````

- O Docker Compose vai baixar as imagens necessárias, construir os containers para o backend e frontend, e iniciar os serviços.

#### Acessar a Aplicação

````
O backend estará acessível em http://localhost:5000
````

````
O frontend estará acessível em http://localhost:5173
````