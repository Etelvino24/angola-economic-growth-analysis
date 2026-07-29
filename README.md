# 🇦🇴 PIB POR PROVÍNCIA 2025 (1)


##  📊 Concentração, Consistência e os Motores do Crescimento Regional

## 🎯 Problema de negócio

Antes de investigar qualquer província ou setor em particular, conduzi uma análise exploratória
para perceber como o crescimento económico está distribuído entre as províncias angolanas — tanto
a nível nacional (que peso cada província tem na economia do país) como a nível individual
(quais províncias cresceram mais, e se esse crescimento foi consistente ou instável ao longo do
tempo). Usei a série histórica de 2020 a 2025 (dados do INE) precisamente para reduzir o ruído de
oscilações pontuais e conseguir identificar tendências reais de crescimento, com foco analítico no
ano de 2025.

## ❓ Perguntas de negócio

1. **Visão geral** 
- Como está distribuída a atividade económica entre as províncias? 
- Existe concentração económica num grupo reduzido de províncias, ou o PIB nacional está bem distribuído?

2. **Evolução do crescimento**
- A economia provincial está a crescer? 
- Esse crescimento é consistente ao longo do tempo, ou volátil? 
- O dinamismo do crescimento económico está a acelerar ou a perder força?
- Qual a estrutura setorial das províncias com maior crescimento (2020–2025)?

3. **Preço vs. Volume**
- O crescimento observado resultou do aumento real da produção (volume),
   ou foi impulsionado principalmente pela variação dos preços?

4. **Estrutura económica** 
- Como é composta a economia de cada província (Agropecuária,
   Indústria, Serviços, Impostos sobre os Produtos)?

## 🗂️ Dados

**Fonte:** Instituto Nacional de Estatística de Angola (INE) — Contas Nacionais, PIB por Província 2025 (1).

**Período de análise:** 2020–2025, com foco analítico em 2025 — a série mais longa serve para
reduzir a influência de oscilações pontuais e isolar tendências reais de crescimento.
**Dimensão:** 6 quadros (tabelas) do INE, cada um representando uma perspetiva diferente da
atividade económica:

| Quadro | Conteúdo |
|---|---|
| Q1 | PIB por província, a preços correntes (mil milhões de Kwanzas), 2015–2025 |
| Q3 | PIB por província, a preços do ano anterior (mil milhões de Kwanzas), 2015–2025 |
| Q4 | PIB por província — variação percentual de preços, 2015–2025 |
| Q5 | PIB per capita por província, a preços correntes (milhares de Kwanzas) |
| Q6 | PIB por província e por setor de atividade, a preços correntes (milhões de Kwanzas) |
| Q8 | PIB por província — variação percentual de volume, 2015–2025 |

[![INE Dataset](https://custom-icon-badges.demolab.com/badge/INE-DADOS-F4801E?style=for-the-badge&logo=organization&logoColor=white&labelColor=1B2A41)](https://www.ine.gov.ao/Diretorios/Ver?caminho=CfDJ8MUwRPStJ4tBpiAAwXNh-s0o16ePsD50EBgFL7sa6AGhxJO8zdZZLuHdNxorX_q233MhNzkH1xAsWNMIoBk8qgKTgzl_we8YFFFlHgF9hkKQdLCwNXHQJamHm5fB9HTpNF-atxYb9lugtvE9sI2sP25xSIIuJ5uw9DmylnVeBR4E)

**`Clica para ver dados`**

## 🛠️ Metodologia

**Modelação de dados** — os 6 quadros do INE foram importados para o Excel e reorganizados numa
estrutura tabular padronizada (cada quadro do INE vem num formato próprio, pouco amigável para
análise direta). O processo seguiu 4 etapas: importação dos dados brutos → padronização da
estrutura tabular → organização por tema (PIB, crescimento em volume, variação de preços,
composição setorial) → criação de tabelas auxiliares para consolidar indicadores usados nos
dashboards.

**Ferramentas:** Microsoft Excel — Power Query (ETL), Tabelas Dinâmicas, PROCX, fórmulas avançadas,
gráficos e dashboards construídos nativamente no Excel.

**Métodos analíticos**, aplicados a cada pergunta de negócio especificamente:
- Crescimento acumulado e desvio padrão — para medir não só *se* uma província cresceu, mas se
  esse crescimento foi consistente ou instável.
- Inclinação da tendência — para avaliar se o dinamismo económico está a acelerar ou a perder força.
- Variação média de preço vs. volume, com classificação cruzada — para diferenciar crescimento
  real (mais produção) de crescimento inflacionário (só preços mais altos).
- Participação setorial (Agropecuária, Indústria, Serviços, Impostos sobre os Produtos) — para
  comparar a estrutura produtiva entre províncias.

**Comunicação executiva:** dashboard executivo e relatório de análise, com resultados e
recomendações apresentados separadamente deste documento de contextualização.

> ⚠️ Como o próprio projeto reconhece: a análise identifica relações estatísticas e permite
> comparar desempenho entre províncias — mas não isola causas específicas (eventos económicos,
> sociais ou institucionais) nem prova causalidade. É um mapa do *o quê*, não do *porquê*.

## 📈 Dashboard
<img width="1343" height="605" alt="image" src="https://github.com/user-attachments/assets/6017896b-dbf7-45e4-9d21-01852c9226d6" />
<img width="1340" height="598" alt="image" src="https://github.com/user-attachments/assets/76698217-86e1-421b-b9cb-fca5c374c6af" />
<img width="1340" height="601" alt="image" src="https://github.com/user-attachments/assets/c0f516f2-375d-4367-a055-d12a39f53590" />
<img width="1339" height="598" alt="image" src="https://github.com/user-attachments/assets/e6bc060a-87ed-4e85-a689-a1bf721cc63c" />

## 💡 Descobertas

- **A economia angolana está fortemente concentrada, não distribuída.** Nove das 18 províncias
  (metade) respondem por 81,3% do PIB nacional, e Luanda sozinha pesa 31,8% — mais do que a soma
  das nove províncias de menor contribuição. A concentração reduz a diversificação territorial da
  economia e aumenta a dependência do desempenho de poucas regiões.

- **O crescimento acumulado (2020-2025) foi liderado por Benguela (+64,4%), não por Luanda.**
  As províncias de maior crescimento têm perfis produtivos diferentes entre si — sinal de uma
  expansão relativamente diversificada, não concentrada num único tipo de economia. Um caso
  particular: Bengo partiu de crescimento negativo e reverteu para o 5º maior crescimento
  acumulado do país, evidenciando mudanças reais na dinâmica regional.

- **A consistência do crescimento não depende do tamanho da economia.** Entre as províncias mais
  estáveis (menor variação ano a ano) estão tanto Luanda — a maior economia do país — como Uíge e
  Cuanza Norte, de participação muito menor no PIB. Isto sugere que previsibilidade económica é uma
  característica da dinâmica local, não do porte da província.

- **Nem todo o crescimento nominal é crescimento real — e isso varia por província.** A
  decomposição preço × volume identificou três perfis distintos: províncias com **crescimento real
  forte** (preço e volume ambos a subir, ex.: Benguela, Bengo, Malanje); províncias sob **pressão de
  preços** (crescimento nominal puxado principalmente por preço, com volume quase estagnado, ex.:
  Luanda, Namibe); e um grupo de **risco** — Cabinda, Cuando Cubango e Zaire — onde o preço sobe mas
  o volume **cai**, ou seja, o crescimento nominal mascara uma retração real da produção.

- **O país tem um perfil produtivo dual: litoral em Serviços/Indústria, interior em
  Agropecuária.** Luanda é a província mais dependente de Serviços; Zaire lidera em peso industrial
  (provavelmente ligado à atividade petrolífera); já Uíge, Malanje, Cuanza Sul, Huambo, Bié e
  Benguela mantêm a Agropecuária como base produtiva dominante.

## 📂 Estrutura deste projeto

 ```
  ├── excel/
  │   ├── pib-provincia-2025.xlsx
  |
  ├── relatorio/
  │   ├── pib-provincia-relatorio-executivo.pdf
  |
  └── documentacao/
      └── contextualizacao-projeto.pdf

 ```

## 📎 Ficheiros

- [Relatório executivo (PDF)](./relatorio/PIB_Provincia_Relatorio_Executivo.pdf)
- [Ficheiro Excel (dados, tabelas dinâmicas e cálculos)](./excel/PIB_POR_PROVÍNCIA_2025_(1).xlsx)
- [Documento de contextualização do projeto (PDF)](./documentacao/Documento_de_Contextualização_do_Projeto.pdf)
