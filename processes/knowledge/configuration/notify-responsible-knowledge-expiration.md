# Notificar responsável da expiração de conhecimento

Este conhecimento tem por objetivo configurar a notificação por e-mail para
avisar o responsável (criador e publicador) acerca da expiração de
conhecimentos.

Antes de Começar
--------------------

É necessário ter ao menos um conhecimento cadastrado na base de conhecimento.

Procedimento
----------------

1.  Configurar o parâmetro 78 com a quantidade de dias anteriores a expiração do
    conhecimento do qual deseja notificar o responsável pelo conhecimento;

2.  Criar um rotina de processamento batch de notificação:

    -   Acessar a funcionalidade através do menu principal Sistema \>
        Processamento Batch e clicar no botão "Novo";

    -   Definir a descrição da rotina, selecionar o tipo "Classe Java" e
        estabelecer a situação como "Ativo";

    -   Selecionar o agendamento como "Diário" e indicar o horário em que será
        processado a rotina;

    -   Na área "Conteúdo" copiar o script abaixo:

        -   br.com.centralit.citcorpore.quartz.job.VerificaValidadeBaseConhecimento

    -   Clicar no botão "Gravar" para efetuar a operação.

3.  Se desejar, é possível personalizar o modelo de e-mail. Basta acessar a
    funcionalidade através do menu principal Sistema \> Configuração \> Modelo
    de e-mail, selecionar o modelo de e-mail com ID = "7" e realizar a mudança
    pretendida.


