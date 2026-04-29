# Cruzamentos espaciais com a classificação da 4CN (2016)

Esse diretório contém os cruzamentos espaciais entre os dados da 4 comunicação nacional (4CN) e as bases do PRODES, TerraClass e Restore+. As análises foram conduzidas a partir do pacote [SITS](github.com/e-sensing/sits).

> O **ano base** para os cruzamentos foi 2016. No caso do PRODES, fez-se o uso da versão de 2025.

---

## Download

Para baixar os cruzamentos gerados em `.zip`, [clique aqui](https://github.com/restore-plus/amz-maps/raw/refs/heads/main/tables/crosstable/2016/data/crosstable-4cn.zip). Para acessar os cruzamentos gerados individualemente [clique aqui](data/). 

## Formato da tabela de cruzamento

O formato das tabelas de cruzamento segue um padrão em que: 

**a.** As colunas correspondem às classes da 4CN (dado rasterizado em 30m para o ano de 2016);

**b.** As linhas correspondem às classes da base de dados avaliadas (ie., PRODES, TerraClass e Restore+);

**c.** Os valores correspondem aos **números de pixels**.

**Exemplo:**

| Reference              | < Classe 4CN >                                 |
|------------------------|----------------------------------------------|
| < Classe base de dados > | < Número de pixels cruzados entre as classes > |
| < Classe base de dados > | < Número de pixels cruzados entre as classes > |
| < Classe base de dados > | < Número de pixels cruzados entre as classes > |

### Observação sobre o PRODES

O dado PRODES utilizado corresponde a versão de `2025` e contém classes de desmatamento acumulado, incrementos de desmatamento, hidrografia, resíduo, vegetação nativa florestal e vegetação nativa não florestal.

Para **incremento** e **resíduo**, a interpretação das classes na tabela segue a notação `dYYYY` e `rYYYY`, onde `YYYY` corresponde ao ano de referência. Alguns exemplos:

| Código | Significado |
|---|---|
| `d2007` | Desmatamento acumulado em áreas florestais até 2007 |
| `d2008` | Incremento de desmatamento no ano de 2008 |
| `d2015` | Incremento de desmatamento no ano de 2015 |
| `r2010` | Resíduo referente ao ano de 2010 (área desmatada detectada posteriormente) |
| `r2018` | Resíduo referente ao ano de 2018 (área desmatada detectada posteriormente) |

A classe `d2007` refere-se ao desmatamento acumulado em áreas florestais até 2007. Para os demais anos (ex.: `d2008`), os valores correspondem a incrementos anuais de desmatamento em vegetação nativa, tanto florestal quanto não florestal. Em áreas de **não floresta**, os incrementos foram registrados de forma bienal entre 2002 e 2018. A exceção é o ano de 2012, substituído por 2013 devido à indisponibilidade de imagens adequadas. A partir de 2018, os incrementos passaram a ser anuais.

A classes de resíduos representam áreas desmatadas que não foram identificadas no ano do desmatamento, geralmente por cobertura de nuvens, sendo mapeadas posteriormente.

## Bioma Amazônia

Para os cruzamentos do Bioma Amazônia foram utilizados dados oficiais do PRODES, TerraClass e Restore+. A Tabela abaixo apresenta as bases de dados e as respectivas tabelas de cruzamento geradas. 


| Base de dados | Ano | Fonte | Tabela de cruzamento com o 4CN |
|---|---|---|---|
| TerraClass | 2016 | [terraclass.gov.br](https://www.terraclass.gov.br/) | [crosstable-4cn-amazon-terraclass.csv](data/amazon/terraclass/crosstable-4cn-amazon-terraclass.csv) |
| PRODES | 2025 | [TerraBrasilis](https://terrabrasilis.dpi.inpe.br/) | [crosstable-4cn-amazon-prodes.csv](data/amazon/prodes/crosstable-4cn-amazon-prodes.csv) |
| Classificação Restore+ | 2016 | [Zenodo](https://doi.org/10.5281/zenodo.19341175) | [crosstable-4cn-amazon-restore.csv](data/amazon/restore/crosstable-4cn-amazon-restore.csv) |

## Bioma Cerrado

Para os cruzamentos do Bioma Cerrado foi utilizado o PRODES. A Tabela abaixo apresenta a base de dados e a respectiva tabela de cruzamento gerada. 


| Base de dados | Ano | Fonte | Tabela de cruzamento com o 4CN |
|---|---|---|---|
| PRODES | 2025 | [TerraBrasilis](https://terrabrasilis.dpi.inpe.br/) | [crosstable-4cn-cerrado-prodes.csv](data/cerrado/prodes/crosstable-4cn-cerrado-prodes.csv) |
