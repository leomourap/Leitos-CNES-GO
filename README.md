![Análise_Dados_Públicos_de_Leitos_Hospitalares_-_CNES-GO__nDurante_a_Pandemia_de_COVID-19](https://user-images.githubusercontent.com/105673165/211730019-49b074ad-58da-4781-b643-31d576a839c6.png)

#### Considere a notícia abaixo:

"Governo de Goiás mantém leitos instalados no período crítico da pandemia" https://www.saude.go.gov.br/noticias/16950-governo-de-goias-mantem-leitos-instalados-no-periodo-critico-da-pandemia

Sabendo que: Os leitos são cadastrados no subsistema LT do sistema CNES (Cadastro Nacional de Estabelecimentos de Saúde); Os dados do CNES.LT estão disponíveis publicamente no servidor FTP do DataSUS conforme exposto no endereço https://datasus.saude.gov.br/transferencia-de-arquivos/ ¹

Desenvolva uma análise exploratória que descreva a evolução da capacidade hospitalar (número de leitos) durante a pandemia de Covid-19 em Goiás. Você pode realizar a análise sobre qualquer perspectiva, mas abaixo listamos algumas sugestões:

-Compare a distribuição geográfica dos leitos por município antes e depois da pandemia; ou

-Analise a evolução do número de leitos no tempo; ou

-Verifique se em algum momento pôde ser observado um declínio na capacidade hospitalar instalada; ou

-Comparar a quantidade de leitos SUS e leitos não SUS no tempo e no espaço.

#### --------------------------------------------------------------------------------------------

O primeiro caso confirmado de pessoa com o coronavírus no Brasil ocorreu em 26 de fevereiro de 2020. Desde então, já foram registrados mais de 36 milhões de casos no país.

Em 11 de março de 2020, a COVID-19 foi caracterizada pela OMS como uma pandemia.

Portanto, vou utilizar os dados dos leitos do CNES desde janeiro de 2020 até novembro de 2022 (dezembro ainda não está disponível).

#### --------------------------------------------------------------------------------------------


> **_NOTA:_**  Utilizei o pacote "microdatasus" do R! para obter os dados públicos do período e do estado que eu precisava. Os comandos foram:

![image](https://user-images.githubusercontent.com/105673165/211731356-55174095-ffd8-488c-aa93-b0af63051838.png)


#### As bibliotecas de Python que utilizei para o tratamento e a análise dos dados foram:
- pandas
- numpy
- matplotlib
- datetime

#### --------------------------------------------------------------------------------------------

Então realizei o tratamento dos dados e a seleção das variáveis que iria utilizar nas análises:
#### Ex: remoção de coluna vazia.
![tratamentodados](https://user-images.githubusercontent.com/105673165/211733694-a6f52898-f70e-4672-b83e-7474d6235137.jpg)


E com os dados prontos, parti para sua análise, direcionado a algumas questões:
#### Como foi a evolução do número de leitos ao longo do período?; Em algum momento pôde ser observado um declínio na capacidade hospitalar instalada?;
![download](https://user-images.githubusercontent.com/105673165/211732658-71fab537-ebed-4efc-94b3-e348dbe81254.png)

#### Como podemos observar no gráfico acima:
- A partir do final de fevereiro de 2020, período que podemos chamar do início da pandemia de COVID-19 no Brasil, o número de leitos cresceu mês após mês (salvo algumas exceções, como em novembro de 2021), até o mês de dezembro de 2021.

- Podemos dizer que o pico da pandemia no Brasil aconteceu em Março de 2021, com aproximadamente 79 mil mortes causadas pela doença naquele mês. Este número veio diminuindo com o passar dos meses, após o pico.

- Podemos pensar que houve um atraso ou que não houve um planejamento precoce visando se preparar para meses em que o surto da pandemia seria maior, como em Março de 2021, visto que mesmo sendo o mês de pico no número de mortes, não é o mês em que haviam mais leitos disponíveis (pelo menos em Goiás). Também, esta menor disponibilidade de leitos naquele momento pode ter contribuído para os péssimos índices do mês.

- De qualquer forma, quando comparado com o período pré pandêmico, o estado mantém até hoje boa parte dos leitos que foram criados.


#### Comparar a distribuição geográfica dos leitos por município antes e depois da pandemia.
![download (1)](https://user-images.githubusercontent.com/105673165/211732771-770e0d62-fdb4-49e4-a53d-dcd82ebc6e91.png)

- Os 5 municípios com mais leitos no estado se mantiveram praticamente nas mesmas posições, quando comparamos os leitos disponíveis antes da pandemia e em Novembro de 2022 (após uma certa normalização do cenário pandêmico).

#### São eles:

- 520870 - GOIANIA (como esperado, a capital se manteve em primeiro lugar em ambos os períodos analisados);
- 520140 - APARECIDA DE GOIANIA;
- 520110 - ANAPOLIS;
- 521880 - RIO VERDE (possuía menos leitos disponíveis do que Trindade, antes da pandemia, cenário que se alterou hoje em dia);
- 522140 - TRINDADE.

> **_NOTA:_**  Também vale destacar o município de GOIANESIA (código 520860), que estava entre os 10 municípios do estado com mais leitos disponíveis antes da pandemia, e que atualmente não consta mais nesta lista.

#### --------------------------------------------------------------------------------------------

#### Fontes:
- JHU CSSE COVID-19 Data - https://github.com/CSSEGISandData/COVID-19 ;

- Histórico da pandemia de COVID-19 - OPAS/OMS - https://www.paho.org/pt/covid19/historico-da-pandemia-covid-19#:~:text=Em%2011%20de%20mar%C3%A7o%20de,pela%20OMS%20como%20uma%20pandemia ;

- Dois anos do primeiro caso de coronavírus no Brasil - https://www12.senado.leg.br/radio/1/noticia/2022/02/23/dois-anos-do-primeiro-caso-de-coronavirus-no-brasil ;

- Estabelecimentos Cadastrados nos Municípios do Estado de GOIAS - http://cnes2.datasus.gov.br/Lista_Tot_Es_Municipio.asp?Estado=52&NomeEstado=GOIAS ;

- Pico da pandemia em 2021 teve mais que o dobro de mortes que a alta em 2020 - https://www.poder360.com.br/coronavirus/pico-da-pandemia-em-2021-teve-mais-que-o-dobro-de-mortes-que-a-alta-em-2020/ .
