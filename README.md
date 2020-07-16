# Protheus x Telegram

Estrutura b�sica de integra��o entre ERP Protheus x Telegram. O modelo a seguir contempla apenas o envio de mensagens. A recep��o\resposta ser� disponibilizada em um outro momento com duas op��es sendo que a primeira ser� utilizada um JOB para ficar monitorando o recebimento de mensagens e o segundo ser� a cria��o de um servi�o API WebHook que na minha opini�o � a melhor op��o.


Veja como � simples a chamada:

![message](./message.png)


# O que posso fazer com bots no Telegram? 


As possibilidades s�o infinitas. Para nomear apenas algumas delas, podemos citar:

- [x] Notificar e monitorar eventos do ERP.
- [x] Realizar aprova��es de pedidos e titulos do ERP.
- [x] Pode ser definido comandos ao Bot-Telegram para que o mesmo solicite  informa��es ao ERP. 
- [x] Servi�os de redes sociais e muito mais.

<b>Aten��o:</b> Atrav�s deste modelo de integra��o j� � poss�vel implementar o primeiro item desta lista pois n�o exige resposta.


# Como utilizar?

```
1. Primeiro passo � ter um Telegram Bot. 

    1.1 -   Para cri�-lo, abra seu app do Telegram, busque por: @BotFather e clique sobre ele. 
    1.2 -   Envie o comando: /newbot.
    1.3 -   Insira um nome para o seu bot. (Exemplo: Bot Teste)
    1.4 -   Insira um username. O username obrigatoriamente tem que terminar com a palavra bot. Ex: MultErpbot, MeuRobo_bot.
    1.5 -   Feito isso, voc� receber� um Token. Ele ser� usado para a integra��o com a Protheus ent�o copie ou salve em algum documento. 
    1.6 -   Para enviar mensagens para um determinado chat ser� preciso obter o ID do bate-papo, neste caso fa�a o seguinte, inclua-o em grupo por exemplo.
    1.7 -   Ap�s adiciona-lo ao grupo abra o browse e cole o seguinte endere�o:
 
            https://api.telegram.org/bot <YourBOTToken> /getUpdates
            
            Ex: Substitua o <YourBOTToken>  pelo seu Token.
            
            Caso tenha ocorrido tudo certo ser� exibido um JSON com os dados do chat. Procure o objeto "chat" e guarde o numero correspondente pois ele tamb�m ser� utilizado na integra��o.

            {"update_id": 8393, "message": {"message_id": 3, "de": {"id": 7474, "first_name": "AAA"}, "chat": {"id":803967136, "t�tulo ":" "}," date ": 25497," new_chat_participant ": {" id ": 71," first_name ":" NAME "," username ":" YOUR_BOT_NAME "}}}
    
    1.8 - Para mais detalhes acesse a p�gina oficial do Telegram: https://core.telegram.org/bots#6-botfather  
 

2. Fa�a o ajuste do fonte Telegram.prw substituindo o Token e o Chat Id que foi gerado pelo bot.
3. Agora � s� compilar e executar ! 
```


## Tecnologias

Projeto desenvolvido em:

- [Advpl](https://tdn.totvs.com/display/tec/AdvPL)

