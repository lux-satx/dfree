# Projeto de distribuição de pacotes
[TOC]

O projeto não precisa recriar os pacotes mas trabalhar para distribuir os existentes.
Na instalação do programa ter um termo de uso pequeno onde as pessoas saibam que estão ajudando a comunidade e um sistema mais distribuido.

## BlockChain (Daemon)
O projeto é tipo blockchain, aonde os dados serão distribuido entre os participantes. Para pouparnos de tanta criptografia coisa que o client seŕa responsavel podemos criptografrar os dados assim que transmitidos e por o client para descriptografar. 
É interessante fazer o uso do avahi para que possamos distribuir localmente também.

### Rotas
Os dados de rota teem 4 pontos importantes
- Origin (IP inicial onde serão trocados os primeiro IPs)
- IP
- Port
- ID (UUID)

### Banco
O banco será um array com as seguintes informações:
- SHA512( dos pacotes anteriores)
- SHA512 (dos pacotes atuais)
- Data
- Pacotes

#### Pacotes
Os dados necessários referentes aos pacotes são um array contendo os campos:

- name
- version
- description
- arch
- licence
- group (null)
- depend (null)
- dependopt (null)
- conflict (null)
- subistitui (null)
- sha512
- assign (null)
- author
- magnect (link do torrent ou outra tecnologia usada, array ou string)

## Client
O client é responsável por descriptografar e interpretar os dados recebidos.
Verificar se os dados estão hospedados localmente através do avahi e baixar-los.
Caso não estejam disponiveis verificar com o daemon os dados para download.
Tendo as seguintes opções básicas:

- Buscar
- Listar
- Instalar
- Remover
- Listar instalados 

