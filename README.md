# Dados da origem geográfica dos estudantes da ESDI/UERJ [TCC]

Este repositório reúne as planilhas utilizadas na coleta, organização e análise dos dados do Trabalho de Conclusão de Curso apresentado ao curso de Design da Universidade do Estado do Rio de Janeiro (UERJ)

## conteúdo

A pasta `/dados` contém três conjuntos de arquivos:

### master

**esdi_origem_estudantes_master.ods**

Arquivo completo em formato OpenDocument contendo todas as abas originais utilizadas na organização dos dados.

### anos

Arquivos em formato CSV contendo os registros de estudantes por ano analisado.

Cada arquivo inclui:

- ano de ingresso  
- bairro de residência  
- cidade
- CEP  

Exemplos:

- estudantes_esdi_1963.csv  
- estudantes_esdi_1973.csv  
- estudantes_esdi_1983.csv  
- estudantes_esdi_1993.csv  
- estudantes_esdi_2003.csv  
- estudantes_esdi_2009.csv  
- estudantes_esdi_2014.csv  
- estudantes_esdi_2019.csv  
- estudantes_esdi_2024.csv  

### resumo

**resumo_bairros_por_ano.csv**

Arquivo contendo a contagem de estudantes por bairro em cada ano analisado e informações adicionais como cidade, latitude e longitude aproximada de cada local e classificação (Centro, Zona Sul, Zona Norte, Zona Oeste, RMRJ ou Outras cidades).

Este arquivo corresponde à base utilizada para análises comparativas e visualizações do trabalho.

## metodologia

Os dados foram obtidos a partir de duas fontes principais:

- consulta manual a arquivos físicos da ESDI/UERJ  
- base digital contendo registros de CEP de ingressantes disponível no Estudo de Conjuntura do NIESC/DataUERJ. 

A catalogação das informações necessárias para a análise da origem territorial dos estudantes teve início com a definição de um recorte temporal. Para fins de comparação da evolução do perfil discente, estabeleceu-se que os anos anteriores à implementação das políticas afirmativas seriam catalogados de 10 em 10 anos (1963, 1973, 1983, 1993 e 2003) e, posteriormente, adotaria-se intervalos quinquenais. Devido à indisponibilidade de dados digitalizados pela UERJ no período imediatamente posterior a 2003, foi necessário estabelecer um intervalo excepcional de seis anos, passando diretamente para o ano de 2009. Dessa forma, ao todo, foram reunidas informações referentes aos ingressantes dos anos de 1963, 1973, 1983, 1993, 2003, 2009, 2014, 2019 e 2024.

Os dados relativos ao período anterior às políticas afirmativas encontram-se disponíveis apenas em formato físico, registrados nas fichas de matrícula dos estudantes que estão armazenadas no arquivo da ESDI. Nessa etapa, foram coletados o bairro de residência, ano de ingresso e ano de conclusão (quando disponível) de ingressantes dos anos 1963, 1973, 1983, 1993 e 2003. Os registros entre 1963 e 1993 apresentavam certa consistência, com a presença dos dados necessários para a análise. Já os documentos de 2003 possuíam lacunas significativas: apenas 50% dos ingressantes tiveram sua ficha de matrícula preservada.
Paralelamente à análise do acervo histórico, iniciou-se a obtenção dos registros dos anos mais recentes. Inicialmente, foram solicitadas ao Departamento de Administração Acadêmica e à Pró-Reitoria de Graduação da UERJ informações sobre o bairro de residência, ano de ingresso, ano de conclusão e tipo de ingresso (cotistas e não cotistas). No entanto, foi informado não ser possível disponibilizar tais dados, em razão da falta de sistematização dos registros administrativos e da incerteza quanto à viabilidade jurídica de divulgação de informações que podem ser consideradas sensíveis no âmbito da Lei Geral de Proteção de Dados Pessoais (Lei nº 13.709/2018).

Diante dessas limitações, optou-se pela utilização dos dados do Estudo de Conjuntura do DataUERJ, plataforma gerida pelo Núcleo de Informação e Estudos de Conjuntura (Niesc). O levantamento consiste em um panorama dos locais de residência dos inscritos no vestibular, classificados, matriculados e não classificados nos anos de 2009, 2014, 2019 e 2024. Embora os dados não incluam informações sobre o tipo de ingresso (por cota ou ampla concorrência), a série histórica permite observar o impacto das políticas afirmativas na diversificação territorial do corpo discente ao longo do tempo (DataUERJ, 2025).
Conforme a catalogação ocorria, as informações acerca da distribuição geográfica dos discentes da ESDI ao longo dos anos foram organizadas em uma planilha. Como metodologias distintas foram utilizadas, a uniformização da base de dados foi necessária para viabilizar a análise. 
Primeiro, foi necessário transformar os CEPs obtidos por meio do DataUERJ para os respectivos endereços completos. Utilizou-se a API pública do ViaCEP no Google Apps Script do Google Planilhas para buscar automaticamente logradouro, bairro, cidade e estado. Em seguida, foi necessário um trabalho de revisão e conferência da veracidade das informações.

Em relação aos dados coletados das fichas de matrícula dos alunos de 1963 a 2003, para obter o CEP utilizou-se a API do CepAberto, um banco de dados com informações de logradouros e suas respectivas localizações. Por fim, para a obtenção das coordenadas geográficas (latitude e longitude) de todos os bairros catalogados, foi utilizada a API pública do OpenStreetMap, que retornou os valores de latitude e longitude mais prováveis para aquela localidade. Adicionalmente, as coordenadas de cada um dos 91 bairros catalogados foi conferida manualmente.

Considerando o caráter manual de parte da coleta realizada em arquivos físicos, podem existir inconsistências pontuais de catalogação, sem impacto significativo nas análises apresentadas na pesquisa.

## observações

- Os dados não permitem identificação individual dos estudantes.  
- As informações disponibilizadas destinam-se exclusivamente a **fins acadêmicos**.  
