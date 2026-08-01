# HMA: A Construção Hierárquica do Afeto na Música 🎵🧠

[![R](https://img.shields.io/badge/R-4.5.0-blue.svg)](https://www.r-project.org/)
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()
[![License](https://img.shields.io/badge/License-BSD_3--Clause-blue.svg)](LICENSE)

> **Repositório Oficial (Research Compendium)** contendo os dados, scripts de análise e materiais suplementares do capítulo/artigo sobre o **Modelo Hierárquico do Afeto Musical (HMA)** e a escala **ALMA (AvaLiação Musical do Afeto)**.

## 📌 Sobre o Projeto

Este projeto investiga a arquitetura estrutural da percepção emocional na música, desafiando o modelo circumplexo bidimensional clássico (Russell, 1980). Através de uma extensa triangulação metodológica que contrasta a decodificação algorítmica de Inteligências Artificiais de última geração (*Audio Transformers* como MERT e CLAP) com a cognição humana, o estudo demonstra que o afeto musical opera sob uma arquitetura hierárquica.

A pesquisa comprova matematicamente que a **Intensidade** não é um ruído metodológico a ser ipsatizado, mas um **Fator Geral (FG)** substantivo que atua como fundação para a experiência qualitativa. A máquina falha em compreender o afeto ao tentar medir energia de forma estritamente mecânica (*Clever Hans Effect*), gerando a **"Lacuna da Melancolia"**, enquanto o ser humano utiliza um **"Filtro de Serenidade"** — suprimindo ativamente o ruído para construir o relaxamento — e modula sua percepção através da Matriz de Personalidade (GFP) e Expertise Musical.

### 🌟 Destaques do Repositório

O projeto está dividido em três grandes eixos empíricos:
1. **Estudo 1 (Descoberta Controlada):** Duelo metodológico provando que o framework HMA dobra a capacidade de explicar a acurácia humana em comparação à ipsatização bidimensional clássica. Apresenta o "Paradoxo da Serenidade".
2. **Estudo 2 (Falsificação em Big Data - DEAM):** Teste em larga escala (1.802 faixas) revelando o colapso preditivo (ΔAIC maciços) do MERT e CLAP quando forçados a operar no espaço 2D sem a magnitude.
3. **Estudo 3 (Calibração Humana e ALMA):** Extração de traços latentes via TRI e CFA Bifactor (Fator Geral de Personalidade e *p-factor*). Modelagem reflexivo-formativa (PLS-SEM) validando a escala **ALMA** e provando que a educação suprime e a personalidade amplifica o impacto da música.

---

## 📂 Estrutura do Repositório

A arquitetura deste repositório segue os princípios de pesquisa reprodutível (*Reproducible Research*):

```text
├── data/                  # Bases de dados brutas e tratadas (CSVs e Excel)
│   ├── Raw_Data.xlsx      # Dados primários sociodemográficos, BFI-2, DASS-21 e ALMA
│   └── embeddings_*.csv   # Embeddings extraídos do MERT e CLAP
├── figures/               # Gráficos em alta resolução (PNG/TIFF) gerados pelas análises
│   ├── Figura_5.png       # O Paradoxo da Serenidade (Interação Magnitude x Categoria)
│   └── ...                # Diagramas estruturais PLS-SEM e hEGA
├── scripts/               # Scripts em RMarkdown (.Rmd) e seus relatórios renderizados (.pdf/.html)
│   ├── Estudo_1.Rmd       # Convergência Físico-Perceptiva e Regressões Logísticas Mistas
│   ├── Estudo_2.Rmd       # Generalização Computacional (Duelo de Ipsatização da IA)
│   └── Estudo_3.Rmd       # Psicometria (TRI, CFA Bifactor, PLS-SEM) e Modelos Lineares Mistos
└── supplementary/         # Material suplementar excluído do manuscrito principal
    ├── PCA_Hum.xlsx       # Matriz completa de cargas fatoriais (Humano)
    └── PCA_IA.xlsx        # Matriz completa de cargas fatoriais (MERT)

## 🚀 Como Reproduzir as Análises

As análises foram conduzidas em ambiente **R**. O código foi desenhado para ser executado de forma linear através dos arquivos RMarkdown localizados na pasta `/scripts`.

### Pacotes Principais Utilizados:
* **`tidyverse`**: Manipulação e visualização de dados
* **`lme4` & `lmerTest`**: Modelagem de Equações Lineares Mistas
* **`seminr`**: Modelagem de Equações Estruturais via Mínimos Quadrados Parciais (PLS-SEM)
* **`lavaan`**: Análise Fatorial Confirmatória e *Bifactor*
* **`EGAnet`**: Análise Exploratória de Grafos Hierárquica
* **`eRm`**: Teoria de Resposta ao Item / Modelos de Crédito Parcial
* **`performance`**: Comparação de modelos, AIC, R²

### Instruções:
1. Clone este repositório no seu terminal: 
   ```bash
   git clone https://github.com/SeuUsuario/HMA.git
```

1. Abra o seu ambiente R/RStudio.
2. Certifique-se de que os caminhos (paths) nos chunks de carregamento de dados (ex: read.csv("data/nome_do_arquivo.csv")) estão relativos ao seu diretório de trabalho.
3. Execute os blocos de código ou faça o Knit dos arquivos .Rmd presentes na pasta scripts/ para compilar os relatórios localmente.

📖 Citação
Se você utilizar os dados, a modelagem estatística (HMA) ou a escala ALMA em sua pesquisa, por favor, cite o capítulo/artigo:
Pedrosa, F. G. (2026). A Construção Hierárquica do Afeto na Música: Valência e Ativação como Qualidade Residual frente à Intensidade. Em preparação / Submetido.
