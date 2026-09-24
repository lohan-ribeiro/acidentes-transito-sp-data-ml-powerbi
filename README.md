# Análise de Acidentes de Trânsito em São Paulo - 2025

![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter%20Notebook-F37626?logo=jupyter&logoColor=white)
![Power BI](https://img.shields.io/badge/Power%20BI-F2C811?logo=powerbi&logoColor=black)
![Pandas](https://img.shields.io/badge/Pandas-150458?logo=pandas&logoColor=white)
![Scikit--learn](https://img.shields.io/badge/Scikit--learn-F7931E?logo=scikit-learn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?logo=matplotlib&logoColor=white)

## 📋 Visão Geral

Este projeto realiza uma análise abrangente dos acidentes de trânsito ocorridos em São Paulo durante o ano de 2025. Utilizando análise de dados, Machine Learning e visualização em Power BI, buscamos identificar padrões e fatores associados às ocorrências para melhor compreender as características relacionadas à gravidade dos acidentes.

## 🎯 Objetivo

**Objetivo Geral:**  
Analisar os acidentes de trânsito ocorridos em São Paulo em 2025, utilizando análise de dados, Machine Learning e visualização em Power BI para identificar padrões e fatores associados às ocorrências.

**Pergunta Principal:**  
Quais foram os principais fatores associados aos acidentes de trânsito em São Paulo em 2025?
<br></br>

## 🔍 Problema e Escopo

Identificar os principais fatores associados aos acidentes de trânsito em São Paulo em 2025, buscando entender quais características estão mais relacionadas à **ocorrência** e à **gravidade dos acidentes**.

### Métricas de Análise
- **Horário:** Horário em que ocorreu o acidente
- **Dia da Semana:** Segunda-feira a domingo
- **Condições Climáticas:** Condição do tempo no momento do acidente
- **Tipo de Via:** Características da via onde ocorreu o acidente
- **Velocidade:** Velocidade registrada ou estimada
- **Iluminação:** Condição de iluminação do local
- **Tipo de Veículo:** Veículo envolvido no acidente
- **Região:** Região de São Paulo da ocorrência
- **Idade dos Condutores:** Faixa etária dos condutores envolvidos
- **Tipo de Acidente:** Colisão, atropelamento, capotamento, etc.
<br></br>

## 🏗️ Arquitetura

![arquitetura](.\docs\arquitetura_PI4.drawio.png)

<p align="center">
    <em>Arquitetura desenvolvida utilizando Draw.io</em>
</p>

## 🛠️ Tecnologias Utilizadas

| Ferramenta | Aplicação |
|-----------|-----------|
| **Jupyter Notebook** | Coleta, integração, tratamento, análise e modelagem |
| **Python** | Linguagem principal de processamento |
| **Pandas** | Manipulação e análise de dados |
| **NumPy** | Computação numérica |
| **Matplotlib/Seaborn** | Visualizações estatísticas |
| **Scikit-learn** | Algoritmos de Machine Learning |
| **Power BI** | Dashboard interativo e KPIs |

---

## 📊 Workflow do Projeto

### 1. **Coleta dos Dados**
Dados coletados do site: [InfoSiga - DETRAN SP](https://infosiga.detran.sp.gov.br/#referencia)

### 2. **Organização dos Dados**
- Armazenar dados originais em pasta de dados brutos
- Criar versão tratada separada
- Documentar colunas em dicionário de dados

### 3. **Tratamento e Limpeza**
- Verificar tipos de dados
- Identificar e tratar valores ausentes
- Remover duplicidades e erros
- Padronizar textos, datas e horários
- Validar registros dentro do período analisado

### 4. **Engenharia de Atributos (Feature Engineering)**
Criar variáveis úteis como:
- Mês e hora do acidente
- Período do dia
- Dia da semana
- Faixas de idade e velocidade
- Manter variáveis originais para rastreabilidade

### 5. **Análise Exploratória (EDA)**
- Distribuição de acidentes por categorias
- Gráficos de horário, dia da semana, clima, tipo de via
- Análises cruzadas com gravidade
- Estatísticas descritivas

### 6. **Formulação de Hipóteses**
Exemplos:
- Velocidades maiores associadas a acidentes mais graves
- Tipos de veículos com maior proporção de ocorrências graves
- Condições de iluminação relacionadas à gravidade

### 7. **Machine Learning**
- Definir variável-alvo (ex: gravidade do acidente)
- Escolher modelo supervisionado (Logistic Regression) ou não supervisionado (Isolation Forest)
- Separar variáveis de entrada (X) e alvo (y)
- Codificar variáveis categóricas
- Dividir dados em treino e teste
- Treinar modelo(s)

### 8. **Avaliação dos Modelos**
Métricas:
- Accuracy
- Precision, Recall, F1-score
- Matriz de Confusão
- Atenção especial a Recall e F1-score se houver desbalanceamento de classes

### 9. **Interpretação do Modelo**
- Análise de importância das variáveis
- Utilizar SHAP se necessário
- Destacar que correlação ≠ causalidade

### 10. **Preparação para Power BI**
- Exportar base final tratada e consistente
- Criar tabelas auxiliares (datas, regiões, categorias)
- Definir KPIs e gráficos

### 11. **Dashboard no Power BI**
Sugestão de layout:
- **Página 1 - Visão Geral:** Total de acidentes, graves/fatais, evolução mensal
- **Página 2 - Fatores Associados:** Velocidade, veículo, clima, iluminação
- **Página 3 - Perfil dos Acidentes:** Região, tipo de acidente, idade dos condutores

### 12. **Conclusões e Insights**
- Responder pergunta principal com dados reais
- Destacar 3 a 5 principais insights
- Documentar limitações e próximos passos
<br></br>

## 📁 Estrutura do Projeto

```
acidentes-transito-sp-data-ml-powerbi/
│
├── README.md                          
├── data/
│   ├── raw/                          # Dados originais
│   └── processed/                    # Dados tratados
│
├── notebooks/
│   ├── 01_coleta_tratamento.ipynb   # Importação, limpeza e tratamento dos dados
│   ├── 02_analise_exploratoria.ipynb # EDA - Análise Exploratória dos Dados
│   └── 03_machine_learning.ipynb     # ML e interpretação
│
├── powerbi/
│   └── acidentes_sp_2025.pbix        # Dashboard Power BI
│
└── requirements.txt                   # Dependências Python
```
---

## 🎓 KPIs Principais

- **Total de Acidentes**
- **Total e Percentual de Acidentes Graves/Fatais**
- **Total de Vítimas** (se disponível)
- **Velocidade Média** (se disponível)
- **Idade Média dos Condutores** (se disponível)
- **Índice de Gravidade**
<br></br>

## ⚠️ Cuidados Metodológicos

1. **Correlação ≠ Causalidade:** Não afirmar que uma variável causa o acidente apenas porque apresenta correlação ou importância no modelo
2. **Qualidade dos Dados:** Verificar cobertura e representatividade da base
3. **Documentação:** Registrar valores ausentes e decisões de tratamento
4. **Evitar Vazamento de Dados (Data Leakage):** Garantir separação correta entre treino e teste
5. **Classes Desbalanceadas:** Usar métricas adequadas (Recall, F1-score) se houver desproporção
6. **Rigor Analítico:** Apresentar apenas o que os dados realmente sustentarem
<br></br>

## 🚀 Como Usar Este Repositório

### Pré-requisitos
- Python 3.8+
- Jupyter Notebook
- Power BI Desktop (opcional, para visualizar dashboard)

### Instalação

```bash
# Clone o repositório
git clone https://github.com/lohan-ribeiro/acidentes-transito-sp-data-ml-powerbi.git

# Acesse o diretório
cd acidentes-transito-sp-data-ml-powerbi

# Instale as dependências
pip install -r requirements.txt
```

### Execução

```bash
# Inicie o Jupyter Notebook
jupyter notebook

# Execute os notebooks em ordem:
# 1. 01_coleta_tratamento.ipynb
# 2. 02_analise_exploratoria.ipynb
# 3. 03_machine_learning.ipynb
```

---

## 📈 Fluxo Resumido do Projeto

```
Coleta -> Limpeza -> Feature Engineering -> EDA -> Hipóteses -> ML -> 
Avaliação -> Interpretação -> Power BI -> Insights -> Conclusões
```

---

## 📝 Fonte de Dados

- **Website:** [InfoSiga - DETRAN SP](https://infosiga.detran.sp.gov.br/#referencia)
- **Período:** 2025
- **Abrangência:** São Paulo
<br></br>

## 📌 Observações Importantes

- Este documento serve como guia orientador do projeto
- Todos os pontos podem ser ajustados conforme necessário
- Dados e análises estão sujeitos a disponibilidade e qualidade das informações coletadas
- Resultados refletem padrões nos dados de 2025 e podem não ser generalizáveis para outros períodos
<br></br>


## 👤 Colaboradores

<table align="center">
  <tr>
    <td align="center">
      <a href="https://github.com/lohan-ribeiro">
        <img src="https://github.com/lohan-ribeiro.png" width="100px" style="border-radius: 50%;">
        <br>
        <sub><b>Lohan Ribeiro Cerqueira</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/rafanatdaniel-stack">
        <img src="https://github.com/rafanatdaniel-stack.png" width="100px" style="border-radius: 50%;">
        <br>
        <sub><b>Rafael Dias de Santi</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/FelipeSilva-Oliveira">
        <img src="https://github.com/FelipeSilva-Oliveira.png" width="100px" style="border-radius: 50%;">
        <br>
        <sub><b>Felipe da Silva Faria de Oliveira</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="https://github.com/RodrigoBitener">
        <img src="https://github.com/RodrigoBitener.png" width="100px" style="border-radius: 50%;">
        <br>
        <sub><b>Rodrigo Souza Machado Bitener</b></sub>
      </a>
    </td>
  </tr>

  <tr>
    <td align="center">
      <a href="https://github.com/Isac-Teixeira">
        <img src="https://github.com/Isac-Teixeira.png" width="100px" style="border-radius: 50%;">
        <br>
        <sub><b>Isac Teixeira Almeida</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="">
        <img src="" width="100px" style="border-radius: 50%;">
        <br>
        <sub><b>Wanderley Maciel Souza</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="">
        <img src="" width="100px" style="border-radius: 50%;">
        <br>
        <sub><b>Wellington dos Santos de Souza</b></sub>
      </a>
    </td>
    <td align="center">
      <a href="">
        <img src="" width="100px" style="border-radius: 50%;">
        <br>
        <sub><b>Wilson Ademar de Arruda</b></sub>
      </a>
    </td>
  </tr>
</table>

<br></br>

## 📄 Licença

Esse projeto está sob licença Apache 2.0. Veja o arquivo  [LICENSE](acidentes-transito-sp-data-ml-powerbi\LICENSE) para mais detalhes.
<br></br>

## 📚 Saiba Mais

Quer entender melhor como o projeto foi desenvolvido? Confira a documentação abaixo:

(obs: sera incluido depois)


