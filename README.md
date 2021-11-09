# dio_bigdata_aws

Projeto do Bootcamp Cognizant Cloud Data Engineer
Curso "Criando seu Ecossistema de Big Data na Nuvem"
O desenvolvimento do projeto consistia em criar uma conta
na AWS, criar um bucket S3, uma chave no EC2, subir um arquivo
txt, e por meio de um script Python ler o arquivo txt
gerar uma saída com as palavras do arquivo e a contagem de
ocorrências dessas palavras no texto.
O script original foi modificado, pois o script dos 2 passos
executava somente 1 e dava erro no segundo passo, dessa forma
o script no repositório possui apenas 1 passo, agradeço a colaboração
do dev Alan Silva que compartilhou a solução no fórum do bootcamp.
Diferentemente do tutorial do curso, foi utilizado o powershell
do Windows 10 para rodar o script, o arquivo gerado contendo
a chave foi do tipo *.ppk que é o padrão para ambiente windows.
Como o script busca o arquivo mrjob.conf na raiz do Linux, para 
rodar no Windows foi acrescentado na linha de comando o path necessário
o comando utilizado foi o seguinte:
python dio-live-wordcount-test.py
--conf-path={endereço da pasta}ssh/mrjob.conf
-r emr s3://dio-cognizant/data/sherlock.txt
--output-dir=s3://dio-cognizant/output/logs1
--cloud-tmp-dir=s3://dio-cognizant/temp/
No repositório estão o script e o arquivo part-00000 com a saída do wordcount.
