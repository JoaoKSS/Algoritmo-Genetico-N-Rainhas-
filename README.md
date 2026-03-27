# Algoritmo Genético para N-Rainhas

![Badge](https://img.shields.io/badge/Python-3.x-blue?style=flat&logo=python)
![Badge](https://img.shields.io/badge/NumPy-Computa%C3%A7%C3%A3o%20Vetorizada-orange?style=flat&logo=numpy)
![Badge](https://img.shields.io/badge/Matplotlib-Visualiza%C3%A7%C3%A3o-green?style=flat&logo=plotly)
![Badge](https://img.shields.io/badge/Jupyter-Notebook-orange?style=flat&logo=jupyter)

Repositório do projeto de Computação Evolucionária para resolver o problema das N-Rainhas com Algoritmo Genético (AG), incluindo comparação de múltiplas estratégias de atualização populacional.

---

## Visão Geral

O projeto está organizado em duas partes principais no notebook:

1. AG base para instâncias `n = 8, 15, 20, 30`.
2. AG alternativo com 6 estratégias de sobrevivência entre pais e filhos.

Além da implementação, o notebook gera:

- Tabela comparativa de tempo, gerações, taxa de sucesso e conflito médio final.
- Curvas de convergência (conflitos x geração).
- Boxplot da distribuição de conflitos na população final.
- Visualização dos melhores tabuleiros encontrados.

---

## Estrutura do Projeto

- `AG_N_Rainhas.ipynb`: implementação completa, experimentos e gráficos.
- `RELATORIO_AG_N_RAINHAS.md`: relatório técnico com análise dos resultados.

---

## Estratégias de Atualização (Parte Alternativa)

Foram comparados os seguintes métodos:

1. Substituição total sem elitismo.
2. Substituição total com elitismo.
3. `k` melhores pais + `N-k` filhos.
4. Somente `k` melhores filhos (substituindo os piores pais).
5. Melhores `N` da união pais + filhos.
6. Seleção aleatória da união pais + filhos.

---

## Como Instalar e Executar

### 1. Clonar o repositório

```bash
git clone <URL_DO_REPOSITORIO>
cd CN
```

### 2. Criar ambiente virtual

No Linux/macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
```

No Windows (PowerShell):

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

### 3. Instalar dependências

```bash
pip install numpy matplotlib jupyter
```

### 4. Abrir e executar o notebook

```bash
jupyter notebook
```

Depois, abra `AG_N_Rainhas.ipynb` e execute as células em ordem.

---

## Reprodutibilidade

- O AG é estocástico; os valores podem mudar entre execuções.
- Para comparação justa entre métodos, mantenha os mesmos parâmetros de população, mutação e gerações.
- Se quiser resultados idênticos entre rodadas, defina uma semente aleatória (`random.seed` e `np.random.seed`).

