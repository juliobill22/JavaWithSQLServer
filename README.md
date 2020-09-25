# JavaWithSQLServer
Date 25/09/2020 Autor Julio Bill Schvenger  
Projeto conexão Java com o Sql Server   

Esse projeto é simples e demonstra como conectar o Java com o Sql Server. 
Para este exemplo, estou utilizando Uma máquina com processador x64, "JRE8","NetBeans IDE 8.2" e "SQL Server 2017 Express".  

Vamos começar!
Precisamos preparar o ambiente.  

1º passo é baixar:   
  * "NetBeans IDE 8.2"    
  * "SQL Server 2017 Express"   
  * JDK8   

  Através dos links: 
    https://netbeans.org/downloads/8.2/rc/    
      * netbeans-8.2-javaee-windows.exe   
    
    https://www.microsoft.com/pt-br/download/details.aspx?id=55994    
      * SQL Server 2017 - "SQLServer2017-SSEI-Expr"   
      
    https://www.oracle.com/br/java/technologies/javase/javase-jdk8-downloads.html     
      "Windows x64 - jdk-8u261-windows-x64.exe"  

2º passo é instalar os executáveis acima.     
  Obs, ao instalar o sql server, verifique se o serviço de update do windows está ativo e se o firewall não está bloqueando a instalação.  
  
3º instalar o JDK e setar a variável de ambiente JAVA_HOME     
  no DOS execute o comando "set JAVA_HOME=C:\Program Files\Java\jdk1.8.0_111"  
  
4º passo pra conectar com o Java, precisamos da ponte de conexão, vamos utilizar o "JDBC Driver 6.0 for SQL Server". 
  Para baixar é possível através do link: https://www.microsoft.com/en-us/download/confirmation.aspx?id=11774  
  
5ª passo é adicionar o JAR ao projeto Após baixar o arquivo acima "Microsoft JDBC Driver" e descompactar, 
  será criado um diretório "Microsoft JDBC Driver 6.0 for SQL Server/sqljdbc_6.0/enu/jre8/sqljdbc42.jar". 
    Esse "sqljdbc42.jar" você precisa adicionar ao seu projeto.  
    
O último passo é fazer a conexão com o banco. 
E para isso, analise o código!  

O pulo do gato está aqui: Você precisa colocar na pasta bin "C:\Program Files\Java\jdk1.8.0_111\bin" a dll "sqljdbc_auth.dll" 
  que está disponível no diretório "C:\Java\Microsoft JDBC Driver 6.0 for SQL Server\sqljdbc_6.0\enu\auth\x64"  
  
Se ocorrer o erro "The TCP/IP connection to the host XXX, port 1433 has failed." 
  https://kb.sos-berlin.com/pages/viewpage.action?pageId=17499564  
  
OUTRAS Referencias Sintaxe da cadeia de conexão https://docs.microsoft.com/pt-br/dotnet/framework/data/adonet/connection-string-syntax  

PESQUISAR OS ERROS do SQL https://docs.microsoft.com/pt-br/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-ver15  
MENSAGEM NA TELA https://www.guj.com.br/t/to-me-matando-pra-achar-showmessage-resolvido/37184/2 https://kb.sos-berlin.com/pages/viewpage.action?pageId=17499564  
CONFIG IP SQL SERVER https://kb.sos-berlin.com/pages/viewpage.action?pageId=17499564

Abraços a todos!
