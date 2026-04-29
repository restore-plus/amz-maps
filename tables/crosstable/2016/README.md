# Cruzamentos espaciais com a classificação da 4CN (2016)

Todos os cruzamentos espaciais foram realizados no SITS, utilizando dados raster com resolução espacial de 30x30m. Os resultados estão expressos em **número de pixels**.

**Ano base:** 2016

---

## Amazônia

As colunas das tabelas correspondem às classes da 4CN. Foram utilizados dados oficiais do PRODES e TerraClass, considerando que as melhorias dessas bases já estão incorporadas na classificação do Restore+.

### Dados utilizados

| Fonte | Ano | Disponível em | Tabela resultante |
|---|---|---|---|
| Classificação rasterizada (30x30m) da 4CN | 2016 | | |
| TerraClass | 2016 | [terraclass.gov.br](https://www.terraclass.gov.br/) | `crosstable-4in-amazon-terraclass-2016.csv` |
| PRODES | 2025 | [TerraBrasilis](https://terrabrasilis.dpi.inpe.br/) | `crosstable-4in-amazon-prodes-2025.csv` |
| Classificação Restore+ | 2016 | | `crosstable-4in-amazon-restore-2016.csv` |

### Observação sobre o PRODES

O dado PRODES utilizado corresponde à versão de 2025 e contém as seguintes classes: desmatamento acumulado, incrementos de desmatamento, hidrografia, resíduo, vegetação nativa florestal e vegetação nativa não florestal.

Para **incremento** e **resíduo**, a interpretação das classes na tabela segue a notação `dYYYY` e `rYYYY`, onde `YYYY` corresponde ao ano de referência. Alguns exemplos:

| Código | Significado |
|---|---|
| `d2007` | Desmatamento acumulado em áreas florestais até 2007 |
| `d2008` | Incremento de desmatamento no ano de 2008 |
| `d2015` | Incremento de desmatamento no ano de 2015 |
| `r2010` | Resíduo referente ao ano de 2010 (área desmatada detectada posteriormente) |
| `r2018` | Resíduo referente ao ano de 2018 (área desmatada detectada posteriormente) |

A classe `d2007` refere-se ao desmatamento acumulado em áreas florestais até 2007. Para os demais anos (ex.: `d2008`), os valores correspondem a incrementos anuais de desmatamento em vegetação nativa, tanto florestal quanto não florestal. Em áreas de **não floresta**, os incrementos foram registrados de forma bienal entre 2002 e 2018. A exceção é o ano de 2012, substituído por 2013 devido à indisponibilidade de imagens adequadas. A partir de 2018, os incrementos passaram a ser anuais.

A classe `rYYYY` corresponde ao resíduo de determinado ano. São áreas desmatadas que não foram detectadas no ano correspondente, geralmente por cobertura de nuvens, e acabaram sendo mapeadas posteriormente.

---

## Cerrado

### Dados utilizados

| Fonte | Ano | Disponível em | Tabela resultante |
|---|---|---|---|
| Classificação rasterizada (30x30m) da 4CN | 2016 | | |
| PRODES | 2025 | [TerraBrasilis](https://terrabrasilis.dpi.inpe.br/) | `crosstable-4in-cerrado-prodes-2025.csv` |

### Observações sobre o PRODES

O conjunto de dados inclui as classes: desmatamento acumulado, incrementos de desmatamento, hidrografia, resíduo e vegetação nativa.

A classe `d2000` representa o desmatamento acumulado até o ano 2000. As classes `dYYYY` correspondem aos incrementos de desmatamento e seguem uma série bienal de 2002 a 2012. A partir de 2013, passam a uma série anual.

A classe `rYYYY` corresponde ao resíduo. São áreas desmatadas não detectadas no ano correspondente, geralmente devido à cobertura de nuvens.
