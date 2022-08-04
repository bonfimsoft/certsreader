# CertsReader
Projeto utilizado para capturar certificados de um site SSL para importar no cacerts do Java

# Processo de Importação
## Importar um certificado no cacerts (Padrão da JRE em JAVA_HOME/jre/lib/security)
keytool -import -kestore <cacerts> -alias <ALIAS> -file <ARQUIVO_CER>

Ex: keytool -import -keystore C:\Java\jdk-11.0.16\lib\security\cacerts -alias login.des.caixa-0.cer -file login.des.caixa-0.cer

Senha Padrão: changeit

# Processo de Exportação
## Retirar um certificado do arquivo nfe-cacerts gerado pela execução do aplicativo
keytool -export -keystore C:\path\arquivo\exported-cacerts -file api.des.caixa-0.cer -alias api.des.caixa-0
