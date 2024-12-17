# Phishing-para-captura-de-senhas-do-Facebook
Nesse projeto vamos usar uma técnica de Phishing para capturar usuário e senha do Fecebook com uma página fake, clone da página real rodando em ambiente controlado de rede interna do alvo.

## Ferramentas:
  - VirtualBox
  - Kali Linux
     - Tela de login e backend
     - setoolkit
  - Win-10

## Etapas: 
  - Instalar o VirtualBox
  - Instalar a ISO do kali
  - Instalar ISO do WIN-10
  - Configurar a placa de rede do VirtualBox e das máquinas virtuais na mesma rede
  - Acessar o kali e preparar o ambiente
    - Node.js
    - backend
    - A página HTML
    - O JavaScript
  - Acesso o kali como root: sudo su
  - Iniciando o setoolkit: setoolkit
  - Escolher o tipo de ataque: Social-Engineering Attacks
  - Escolher vetor de ataque: Web Site Attack Vectors
  - Escolher o método de ataque: Credential Harvester Attack Method
  - Escolher o método de ataque: Site Cloner
  - Obtendo o endereceço da máquina que receberá: ifconfig
  - Informar URL para clone. Exemplo: http://www.facebook.com
  - Caso o Setoolkit não consiga realizar o clone, ou o site esteja usando uma tecnica de hash pode usar o comando (curl -L)
    - Usando o comando (curl -L) será baixado uma cópia da página
    - Usando um servidor web para colocar essa página no ar voce consegue rodar o setoolkit na pagina local e usar para ataque phishimg e capturar usuário e senha.

## Preparando o ambiente:

- Tela do VirtualBox após receber as imagens ISO:
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/01.png)

- Tela do Kali Linux pronto para as próximas etapas:
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/02.png)

- Sistema operacional Windows-10 instalado e pronto para teste sumulando usuário:
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/03.png)

- Ferramenta que vai ser usada Setoolkit pronta e atualizada:
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/04.png)

- Seleciona 1 para: Social-Engineering Attacks
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/05.png)

- Seleciona 2 para: Web Site Attack Vectors
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/06.png)

- Seleciona 3 para: Credential Harvester Attack Method
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/07.png)

- Seleciona 2 para: Site Cloner
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/08.png)

- Digite o ip do atacante que vai receber as credenciais, ou enter para confirmar o ip encontrado pelo setoolkit. Caso não saiba digite no terminal do kali o comando (ifconfig)
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/09.png)

- Digite a URL do site que será clonado. Precisa está hospedado na mesma rede (LAN) do alvo. Caso não tenha URL pode ser o endereço ip do servidor a ser clonado que pode ser resolvino no dns local para ocultar o ip. Trocando o ip local para a URL desejada.
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/10.png)

- Clone sendo realizado
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/11.png)

- Após finalizar o clone, será informado o link fake que vai responder na pora 80
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/16.png)

- Ao acessar o link fake que vai responder na pora 80
![](https://github.com/MagnoSi1va/Phishing-para-captura-de-senhas-do-Facebook/blob/main/18.png)

- Ao tentar realizar login o atacante receberá em texto puro o usuário e senha usado no formúlario
- Esse ataque só é possível em rede interna (atacante e alvo na mesma rede)
- Alguns sites que não criptografa, usam bcrypt ou Argon2, a senha será armazenada como um hash seguro
  - Hashing: Converte a senha em um formato ilegível.
  - Bcrypt: Introduz uma camada de segurança com salt, dificultando ataques de força bruta.


  
  
