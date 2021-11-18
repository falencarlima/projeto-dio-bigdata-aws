# projeto-dio-bigdata-aws
Contar repetição de palavras do livro Sherlock.txtc

## Objeivo:
Utilizar recursos computacionais da aws para calcular a repetição de palavras contidas no livro Sherlock.txt.
## Comando para submeter o job:
python3 main.py -r emr s3://{bucket-name}/data/sherlock.txt --cluster-id "CLUSTER-ID" --output-dir=s3://{bucket-name}/output/log01 --cloud-tmp-dir=s3://{bucket-name}/temp/ --conf-path mrjob.conf
## Arquivos do projeto:
* main.py
* mrjob.conf
* sherlock.txt
## Resultado
Três arquivos foram gerados como saída:
* part-00000
* part-00001
* part-00002
## Problema ocorrido:
A biblioteca boto3 está descontinuada, por esse motivo tive que criar o cluster manualmente para poder enviar o job.
