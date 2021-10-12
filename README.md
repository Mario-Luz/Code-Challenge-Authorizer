# Code Challenge: Autorizador
### O que essa aplicação faz:
aplicação que autoriza transações para uma conta específica seguindo uma
série de regras predefinidas.
Dado um arquivo chamado operations que contém diversas linhas descrevendo operações no formato
json :
```console
$ cat operations
{"account": {"active-card": true, "available-limit": 100}}
{"transaction": {"merchant": "Burger King", "amount": 20, "time": "2019-02-
13T10:00:00.000Z"}}
{"transaction": {"merchant": "Habbib's", "amount": 90, "time": "2019-02-
13T11:00:00.000Z"}}
{"transaction": {"merchant": "McDonald's", "amount": 30, "time": "2019-02-
13T12:00:00.000Z"}}
```

A aplicação deve ser capaz de receber o conteúdo do arquivo via stdin , e para cada operação processada
fornecer um output adequado de acordo com a lógica de negócio:

```console
$ authorize < operations
{"account": {"active-card": true, "available-limit": 100}, "violations": []}
{"account": {"active-card": true, "available-limit": 80}, "violations": []}
{"account": {"active-card": true, "available-limit": 80}, "violations": ["insufficient-limit"]}
{"account": {"active-card": true, "available-limit": 50}, "violations": []}
```
Operações do Autorizador
O programa deve lidar com dois tipos de operações, decidindo qual delas executar de acordo com a linha
que estiver sendo processada:
1. Criação da conta
2. Autorização de uma transação na conta
Para simplificar o programa, você pode assumir que:
Todos os valores monetários são inteiros positivos, portanto é uma moeda sem centavos;
As transações na conta chegarão no autorizador em ordem cronológica.

# Iniciando o Projeto
- Para iniciar o projeto precisamos ter :
    - Node.JS : [Link para a página de download do Node.JS](https://nodejs.org/pt-br/download/)
    - Passo a passo para rodar o projeto
        #Instale os pacotes npm
        $ npm install
       E pronto, a pasta node_modules será gerada com os modulos que o projeto utilizar.

        #Execute a aplicação
        $ npm start
       
### Testes
![test-coverage](https://i.ibb.co/Sx177D4/Captura-de-tela-de-2021-09-24-16-16-10.png).
### Arquitetura 
Ainda tenho muito o que aprender sobre arquitetura, tentei deixar o projeto o mais flexivel possivel
### Tecnologias Preferenciais:
Escolhi NodeJS por questão de afinidade com a tecnologia, é onde me sinto mais confortavel para desenvolver.
### Nota Adicional
Eu sou um desenvolvedor Jr que está buscando aprender cada dia mais, tenho um longo caminho pela frente.