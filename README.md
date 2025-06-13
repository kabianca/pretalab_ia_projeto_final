
# 🧪 Análise do Sistema Nacional de Informações sobre Saneamento (SNIS)

Este repositório contém o projeto final do ciclo formativo de IA do PretaLab e tem como objetivo analisar a situação do saneamento básico nos estados brasileiros e sua relação com indicadores de saúde pública. 

Através da integração dos dados do SNIS com as bases do DataSUS via BigQuery, investigamos se há correlação entre investimentos em saneamento e a taxa de mortalidade por doenças relacionadas à ausência de infraestrutura adequada.

---

## 👥 Integrantes do Grupo

Projeto desenvolvido no curso de Inteligência Artificial da Pretalab por:

| Nome               | GitHub                                                                 |
|--------------------|------------------------------------------------------------------------|
| Aliana Simões      | [alia](https://github.com/alia)                                        |
| Fernanda Brito     | [pherys](https://github.com/pherys)                                    |
| Izaura Souza       | [izaurahae](https://github.com/izaurahae)                              |
| Jordânia Gabrielle | [JordaniaGabrielle](https://github.com/JordaniaGabrielle)              |
| Karla Oliveira     | [kabianca](https://github.com/kabianca)                                |
| Mariana Freitas    | [marianafreitas13](https://github.com/marianafreitas13)                |
| Taís Guimarães     | [taisgb](https://github.com/taisgb)                                    |

---

## 🎯 Objetivo do Projeto

Avaliar a cobertura de saneamento básico no Brasil nos últimos 5 anos, identificar padrões regionais, analisar a evolução dos investimentos públicos e verificar a correlação entre os dados de saneamento e os índices de mortalidade por doenças evitáveis.

---

## ❓ Perguntas Norteadoras

- Qual é a cobertura de acesso à água potável e esgotamento sanitário nos estados brasileiros nos últimos 5 anos?
- Quais os 5 estados com maior cobertura de água e de esgoto?
- Como variou o investimento público ao longo dos anos por estado?
- Qual a natureza jurídica mais recorrente na prestação desses serviços?
- Qual a tendência da natureza jurídica das instituições gestoras nos últimos 5 anos?
- Como os indicadores de saneamento se correlacionam com índices de saúde?

---

## ⚙️ Metodologia

### 1. Coleta e Pré-processamento

- Utilização da biblioteca `basedosdados` para acessar dados via Google BigQuery.
- Dados do SNIS (1995 a 2021); o ano de 2022 foi excluído por inconsistência.
- Complementação com dados do DataSUS via BigQuery.

### 2. Tratamento dos Dados

- Normalização com `pandas`.
- Conversão de tipos e remoção de registros ausentes/inconsistentes.
- Agrupamento por estado e ano.

### 3. Análises Realizadas

- Cobertura de água e esgoto por estado.
- Frequência da natureza jurídica das prestadoras.
- Evolução de investimento público por estado.
- Top 5 estados com maior cobertura.
- Análise das regiões com maior déficit.
- Correlação com mortalidade por doenças de veiculação hídrica.

---

## 🛠️ Tecnologias Utilizadas

- **Python**
  - `pandas`, `numpy` – manipulação de dados
  - `matplotlib`, `seaborn`, `plotly` – visualização de dados
- **Google Colab**
- **Google BigQuery**
  - `google.cloud.bigquery` – integração com BigQuery

---

## 📊 Resultados Destacados

- A cobertura de água potável é mais ampla que a de esgoto, principalmente nas regiões Norte e Nordeste.
- Rankings elaborados com foco na população urbana:

**Top 5 Cobertura de Água Potável**  
**Top 5 Cobertura de Esgotamento Sanitário**

- **Investimento público nos últimos anos:**
  - **Estável:** Distrito Federal
  - **Queda:** Acre, Alagoas, Espírito Santo, Goiás, Pernambuco, Rondônia, Roraima, São Paulo, Tocantins
  - **Crescimento:** Amazonas, Bahia, Ceará, Maranhão, Mato Grosso, Pará, Piauí, Rio Grande do Sul
  - **Oscilação:** Amapá, Minas Gerais, Mato Grosso do Sul, Paraíba, Paraná, Rio de Janeiro, Rio Grande do Norte, Santa Catarina, Sergipe

- **Natureza jurídica predominante:**  
  - Sociedade de Economia Mista com Administração Pública
  - Em seguida: Administração Pública Direta, Autarquias e Empresas Públicas

---

## 📚 Fontes de Dados

1. Dados sobre o saneamento básico no país - [Base de Dados do SNIS](https://basedosdados.org/dataset/2a543ad8-3cdb-4047-9498-efe7fb8ed697?table=df7cf198-4889-4baf-bb77-4e0e28eb90ca)
2. Dados de informações de causas de internação usada para levantamento de doenças ocasionadas por falta de saneamento básico - [Base de Informações Hospitalares do SUS](https://basedosdados.org/dataset/ff933265-8b61-4458-877a-173b3f38102b?table=74f616d0-933c-4198-9f8e-00858eff807d)
3. Tutorial de vinculação do Big Query ao Google Colab - [Notebook com exemplo e orientações de conexão Colab e Big Query](https://colab.research.google.com/drive/1_DeLAGUiC3SFOahmwpyF5iBtJZ6rzttA?usp=sharing)
4. Documentação da plataforma Base de Dados sobre uso dos dados no Big Query - [Documentação BD sobre conexão com Big Query](https://basedosdados.org/docs/home#acessando-tabelas-tratadas-bd)
5. Matéria sobre as principais doenças ocasionadas por falta de saneamento básico - [Doenças por falta de saneamento básico - Habitat Brasil](https://habitatbrasil.org.br/doencas-falta-de-saneamento-basico/)

---

## 📌 Conclusão

O estudo demonstrou uma correlação significativa entre a precariedade no saneamento e o aumento das taxas de mortalidade por doenças evitáveis (tais como: Diarreia, Amebíase, Amebiase, Cólera, Leptospirose, Disenteria, Hepatite A, Esquistossomose, Tifoide, Dengue, Febre Amarela, Malaria), com destaque para alguns estados das regiões Norte e Nordeste. 
Outro ponto observado, foi o fato de que em tempos onde a privatização de serviços básicos tem sido constante no debate público focamos em observar como a gestão desses serviços tem sido conduzida a nível regional. 
Cabe pontuar que a gestão compartilhada, Sociedade de economia mista com administracao publica, tem liderado a gestão desses serviços em todas as regiões, em seguida gestão pública direta ainda segue firme na condução desses serviços, contabilizando nessa categoria a Administraão publica direta, Autarquia e Empresa publica.

Por fim, em relação a influência da falta de saneamento básico na saúde da população local, ainda que tenhamos percebido uma correlação relevante com o Estado do Acre que lidera o número de doenças associadas a falta desses serviços e apresenta baixos indices de cobertura de água e, sobretudo, esgoto. Olhar para apenas um único ano e apenas para as variáveis analisadas, não parece ser suficiente para entender essa questão, visto que não houve uma correlação tão direta com os demais estados que lideram o ranking das doenças observadas. 
Seria o caso de observar mais doenças? Deveríamos observar dados de saneamento de anos anteriores, pois surtos de doenças demoram um pouco mais para serem observáveis nos dados? A questão que fica e que não pode ser ignorada dados os estudos da OMS é que torna-se cada vez mais evidente que há uma necessidade de Políticas Públicas específicas para esse contexto e investimentos contínuos em saneamento, reforçando sua importância como determinante social da saúde.
