# DataEng
Para esse desafio, foram criados os seguintes arquivos:<br>
![tree.jpg](./images/tree.jpg)

## Descrição dos arquivos

**database.ini** -> arquivo com os dados para conexão do banco de dados<br>
**docker-compose.yml** -> arquivo com o serviço para o banco de dados "Kzas"<br>
**requirements.txt** -> arquivo com as bibliotecas necessárias para a execução do script python<br>
**script.ipynb** -> script python em formato notebook para download, inclusão e geração dos dataset enriquecido no banco de dados<br>
**script.py** -> versão do script em python.<br>
**modelagem.sql** -> script sql para criação das tabelas.<br>

## Execução
Para execução do script, é necessario a instalação do docker e python.<br><br>
1. No diretorio, onde os arquivos estão localizados, execute: <br>
```docker-compose up -d```
2. depois execute: <br>
  ``` python Script.py ```

Apos a execução do script, será gerado 3 tabelas no banco de dados: <br>

**ads** -> tabela com os dados de ads mais **"id_building"** no qual e feito o relacionamento com a tabela **"buildings"**<br>
**buildings** -> tabela com os dados de "buildings.csv"<br>
**ads_buildings** -> tabela com os registros de 1 ad para "n" registros de buildings

## Relacionamentos

**ads.id_building** -> **buildings.id** <br>
**ads.id** -> **ads_buildings.id_ad** <br>
**buildings.id** -> **ads_buildings.id_build**
