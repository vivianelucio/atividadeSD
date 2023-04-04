Este projeto foi desenvolvido pelos alunos Anderson Maciel, Joelson Silva e Viviane Lúcio, do 3º semestre do curso de Tecnologia em Análise e Desenvolvimento de Sistemas (Noturno). O referido projeto é composto por três atividades, sendo divididas da seguinte maneira: 
A primeira atividade é chamada de “Calculadora Remota em UDP”, que apresenta duas classes (server e client)
Quando for testar:
- Inicie a classe server.
- Em seguida, execute a classe client. 
- Após aparecer a mensagem no console, insira o primeiro número, dê um espaço, digite o símbolo da operação, dê um espaço novamente, e logo após, insira o segundo número e aperte enter.
- Então, aparecerá a resposta da operação.

A segunda atividade é chamada de “Classificados de veículos”. Por sua vez, nesta atividade foram criadas cinco classes (InterfaceVeiculos, ClassificadosVeiculos, Veiculos, ServerRMI, ClientRMI).
Quando for testar:
- Inicie a classe ServerRMI.
- Em seguida, execute a classe ClientRMI.
- Irá aparecer uma janela, através de JOPtionPane, onde o cliente poderá escolher uma dentre as três opções disponíveis. A primeira opção consiste em adicionar um veículo, a segunda consiste em consultar a lista de veículos inserindo o ano e a terceira opção é para sair.

A terceira atividade "Chat Room TCP" é um projeto Java que mostra como criar uma aplicação de chat cliente/servidor utilizando as
interfaces `ServerSocketChannel` e `SocketChannel`.
É mostrado como desenvolver a aplicação 
utilizando chamadas não bloqueantes (non-blocking), 
para permitir que o servidor possa aceitar conexões e receber mensagens de múltiplos usuários
simultaneamente.

O projeto é composto por duas aplicações console:

- link:src/main/java/com/manoelcampos/chat/NonBlockingChatClient.java[Cliente]
- link:src/main/java/com/manoelcampos/chat/NonBlockingChatServer.java[Servidor]

== Servidor

O servidor escuta numa porta configurada por meio de uma constante em sua classe.
Tal constante é utilizada pelo cliente para saber qual porta se conectar ao servidor.
O servidor inicia e fica em loop infinito, aguardando conexões de clientes em tal porta.
Com uso da API não bloqueante NIO.2, conseguimos processar as conexões e recebimento de mensagens
sem obrigatoriamente utilizarmos Threads. 

== Cliente

O cliente conecta na porta especificada na classe do servidor, no endereço definido em uma constante na classe do cliente. O usuário pode digitar mensagens que são enviadas ao servidor. 
O cliente então aguarda a resposta do servidor e exibe na tela.
A aplicação fica em loop até o usuário digitar "sair" para encerrar.

== Executando as Aplicações

O servidor deve ser iniciado a partir da classe link:src/main/java/com/manoelcampos/chat/ChatServer.java[Servidor].
Isto pode ser feito no NetBeans, abrindo tal classe e pressionando `SHIFT+F6`.

Depois de iniciado o servidor, pode-se executar várias instâncias do cliente para representar diversos usuários conectados ao chat. No NetBeans, basta abrir a classe link:src/main/java/com/manoelcampos/chat/ChatClient.java[Cliente] e pressionar `SHIFT+F6` para cada cliente que desejar executar.
