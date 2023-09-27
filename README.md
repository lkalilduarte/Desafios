# Desafios
Nesse repositório estão:
- Os dois arquivos csv fornecidos no desafio, Sensor_FieldPRO e Estacao_Convencional;
- O notebook Jupyter com o códido comentado de resolução do desafio e
- O html do resultado da previsão da chuva.

O html também está em um bucket do S3 com acesso público, e pode ser acessado pela url abaixo:
https://luiskalildesafiofieldpro.s3.us-east-2.amazonaws.com/previsaodechuva.html

O código está estruturado da seguinte forma:
1- Análise e ajustes dos dados do csv Sensor_FieldPRO
2- Análise e ajustes dos dados do csv Estacao_Convencional
3- Análise da intersecção dos dados dos dois csvs
4- Merge dos dois csvs nos datetimes de intersecção
5- Aplicação da Regressão Linear em diferentes combinações de dados para identificar o melhor modelo preditivo
6- Comparação dos resultados das regressões lineares e definição do melhor modelo
7- Aplicação do melhor modelo para obter a predição das chuvas
8- Criar uma tabela com as datas, horários e chuvas previstas
9- Transformar essa tabela em html para que seja possível visualizar fora do código

Sobre o código:
Optei por usar a Regressão Linear por ser uma boa opção para aplicação em modelos preditivos.
Tentei todas as cobinações de dados que incluissem pelo menos uma das colunas originais (piezo_charge, piezo_temperature e num_resets) e também
com as colunas extras (humidade do ar, temperaturado ar e pressão atmosférica), com o intuito de garantir a melhor previsão e utilizando os dados da estação.

Sobre o resultado do código:
O melhor modelo, ou seja, o que previo as chuvas com menor erro, foi o que possui os dados de peizo_charge e humidade do ar.
