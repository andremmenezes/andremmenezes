# André Macedo Menezes

Engenharia e perícia, com software escrito para resolver o problema técnico que
está na frente. Transporte de carga, estruturas, automação fiscal e acervo
documental.

O critério que atravessa todos os projetos aqui é o mesmo que um laudo exige:
**resultado rastreável, premissa declarada e limitação dita em voz alta.** Número
sem procedência e sem data não serve, e os pipelines foram escritos para não
produzir nenhum.

## Áreas

**Perícia e engenharia forense.** Simulação e análise aplicadas a sinistro de
transporte e a falha de estrutura. Sloshing em tanque rodoviário, tombamento,
limite de velocidade regulamentado com rastreabilidade de fonte, silo metálico.

**Automação fiscal brasileira.** NF-e modelo 55, DANFE, NFS-e, chave de acesso,
integração com a API do SERPRO, consolidação com granularidade de item.

**Engenharia de dados e documentos.** Extração estruturada de PDF, OCR, busca
vetorial sobre acervo documental, classificação de documento com score de
confiança e controle explícito de custo de token.

**Simulação numérica e dados geoespaciais.** CFD multifásico, validação contra
modelo analítico independente, pipeline reprodutível a partir de API de dados
abertos.

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![SciPy](https://img.shields.io/badge/SciPy-8CAAE6?logo=scipy&logoColor=white)
![OpenFOAM](https://img.shields.io/badge/OpenFOAM-1d7a8a)
![GeoPandas](https://img.shields.io/badge/GeoPandas-139C5A)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL%20%2B%20pgvector-4169E1?logo=postgresql&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Tesseract](https://img.shields.io/badge/Tesseract%20OCR-4A90D9)

| Domínio | Ferramentas |
|---|---|
| Linguagem | Python |
| Dados e análise | pandas, NumPy, SciPy, Parquet |
| Geoespacial | GeoPandas, Shapely, pyproj, H3, GeoJSON, MapLibre |
| Simulação | OpenFOAM, método VOF, modelagem analítica |
| Documentos | PyMuPDF, pdfplumber, pdf2image, pyzbar, Tesseract |
| Busca e IA | pgvector, LangChain, embeddings, LLM com fallback por regra |
| Interface e entrega | Streamlit, HTML, Docker |
| Infra e processo | Git, GitHub Actions, Make, Bash |

## Projetos

| Projeto | O que é | Stack |
|---|---|---|
| [mapa-limites-velocidade](https://github.com/andremmenezes/mapa-limites-velocidade) | Consolida oito bases abertas de limite de velocidade regulamentado, de cinco publicadores, em acervo consultável por coordenada, com mapa web. 35.971 dispositivos, dedupe por célula H3, procedência e data em cada linha. | Python, GeoPandas, H3, Parquet, MapLibre |
| [sloshing-tanque-rodoviario](https://github.com/andremmenezes/sloshing-tanque-rodoviario) | Quantifica por CFD e por modelo analítico independente a amplificação da aceleração lateral em tanque parcialmente cheio. 24 casos, concordância mediana de 4,27% entre os dois métodos. | OpenFOAM, VOF, Python, SciPy |
| [nfe-pipeline](https://github.com/andremmenezes/nfe-pipeline) | Extrai a chave de acesso de DANFEs em PDF por código de barras com fallback de OCR, busca o XML autorizado na API do SERPRO e consolida em planilha com 28 colunas por item. | Python, pyzbar, Tesseract, SERPRO, Streamlit |

## Um resultado, para dar a medida

Em `sloshing-tanque-rodoviario`, um dos 24 casos resume o motivo de o trabalho
existir. Curva de 100 m a 100 km/h, tanque meio cheio:

```
margem de segurança pela aceleração nominal   MS = 1,0330   acima de 1: não tomba
margem de segurança pela aceleração efetiva   MS = 0,9632   abaixo de 1: tomba
```

A amplificação de 7,24 por cento causada pelo movimento do líquido é a
diferença entre um conjunto que passa com folga de 3 por cento no cálculo
convencional e um conjunto que tomba. É o tipo de caso em que a análise sem
sloshing erra a conclusão, e não apenas o número.

## Contato

- E-mail: macedomenezesandre@gmail.com
- GitHub: [@andremmenezes](https://github.com/andremmenezes)
