Este template foi customizado a partir do https://github.com/suportecavalcante/zabbix.templates/tree/master
Creditos ao Diego Cavalcante

Funciona perfeitamente nas versoes 4 - 6 do zabbix e nas versões 2008 em diante do mssql server.

# zabbix-templates
#Templates de zabbix para monitoramento de serviços de banco de dados

#Primeiro de tudo faça download dos arquivos e pastas e jogue dentro da pasta do zabbix agent.
#No arquivo de configuração do agente, inclua os diretórios conforme as linhas abaixo:
Include=.\mssql.backup.userparams.conf
Include=.\monitoramento-sql\scripts\*.conf
Include=.\monitoramento-sql\userParameters\*.conf

Caso você opte por salvá-los em outro diretorio, preencha o caminho completo conforme o exemplo
#Include=C:\Program Files\Zabbix Agent 2\monitoramento-sql\userParameters\*.conf

Depois de feito upload das pastas bin e monitoramento-sql, bem como o arquivo mssql.backup.userparams.conf no diretório do zabbix agent, crie um usuário no banco com permissoes de leitura a todas as instancias que você deseja monitorar. O usuário e senha deve ser preenchido no arquivo
