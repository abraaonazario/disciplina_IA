# CHyPS: Classificador Híbrido Ponderado para Dados Socioterritoriais

Este repositório contém a implementação em Python do **CHyPS (Classificador Híbrido Ponderado para Dados Socioterritoriais)**, um novo meta-algoritmo proposto como parte de uma pesquisa de Aprendizado de Máquina e LLMs

## Sobre o Projeto

A classificação de dados socioterritoriais, como os do repositório DataLuta, é um desafio complexo devido à heterogeneidade das fontes, que mesclam dados estruturados e textuais. Abordagens que utilizam apenas aprendizado de máquina (ML) tradicional ou Modelos de Linguagem de Larga Escala (LLMs) de forma isolada enfrentam dificuldades para lidar com essa dualidade.

Este projeto propõe o **CHyPS**, um framework que busca resolver este problema através de uma abordagem de **IA Híbrida**. O CHyPS combina dinamicamente as predições de um modelo de ML robusto (Random Forest) e de um LLM por meio de uma lógica de ponderação adaptativa. A decisão final considera a natureza de cada registro de dado, priorizando o LLM para textos semanticamente ricos e o Random Forest para dados mais curtos ou estruturados.

O objetivo é demonstrar que esta fusão sinérgica alcança um desempenho superior em acurácia e robustez em comparação com os modelos de base operando isoladamente.

## Tecnologias e Bibliotecas

O projeto foi desenvolvido em Python 3 e utiliza as seguintes bibliotecas principais:

-   **Pandas:** Para manipulação e carregamento dos dados.
-   **Scikit-learn:** Para o treinamento dos modelos de Machine Learning (Random Forest, SVM) e para a avaliação das métricas.
-   **spaCy:** Para o pré-processamento avançado de texto (lematização, remoção de stopwords).
-   **Matplotlib:** Para a visualização dos resultados e geração de gráficos comparativos.
-   **NumPy:** Para operações numéricas.

## Estrutura do Repositório

-   `notebook_chyps.ipynb`: O notebook principal contendo todo o fluxo do projeto, desde o carregamento dos dados até a avaliação final e visualização.
-   `data/`: Pasta destinada a armazenar a base de dados utilizada (ex: `Exemplo.xlsx`).
-   `article/`: Pasta contendo o artigo científico relacionado à pesquisa.
-   `results/`: Pasta onde as imagens dos gráficos e tabelas de resultados são salvas.
-   `requirements.txt`: (Opcional) Arquivo com as dependências para fácil instalação do ambiente.

## Como Executar

1.  **Clone o repositório:**
    ```bash
    git clone [URL-DO-SEU-REPOSITORIO]
    cd [NOME-DO-SEU-REPOSITORIO]
    ```

2.  **Instale as dependências:**
    Recomenda-se o uso de um ambiente virtual (`venv`).
    ```bash
    pip install -r requirements.txt
    # ou instale manualmente
    pip install pandas openpyxl scikit-learn spacy matplotlib numpy
    # Baixe o modelo de linguagem do spaCy
    python -m spacy download pt_core_news_lg
    ```

3.  **Execute o Notebook:**
    Abra e execute o arquivo `notebook_chyps.ipynb` em um ambiente como Jupyter Notebook, Jupyter Lab ou Google Colab. As células estão organizadas de forma sequencial e autoexplicativa.

    *Nota: A implementação da chamada ao LLM é simulada. Para uma execução real, insira sua chave de API e a lógica de chamada na célula correspondente.*

## Contribuição

A principal contribuição deste trabalho é a proposição de um framework de decisão híbrido e adaptativo que alavanca as forças complementares de diferentes paradigmas de IA, oferecendo uma solução mais robusta para a classificação de dados heterogêneos.

## Citação

Se você utilizar este trabalho, por favor, cite o artigo associado:

*Nazário, A. G. (2025). Combinando Aprendizado de Máquina e LLMs: Proposta e Avaliação do Framework Híbrido CHyPS. [Nome da Conferência ou Periódico].*
