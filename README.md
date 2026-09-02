# Mini-Projeto MNIST - Classificação de Dígitos Manuscritos

Pipeline ponta a ponta de Machine Learning para classificação multiclasse de dígitos manuscritos (0-9) utilizando o dataset MNIST.

## Problema

O dataset MNIST contém 70.000 imagens em escala de cinza (28x28 pixels) de dígitos manuscritos de 0 a 9. O objetivo é construir, treinar, comparar e estressar modelos preditivos para classificar esses dígitos, incluindo testes de robustez com dados fora da distribuição (OOD) e imagens reais.

## Técnicas e Tecnologias

- **Linguagem**: Python 3.14
- **Modelos**: Random Forest, KNN, MLP (Perceptron Multicamadas)
- **Bibliotecas**: scikit-learn, matplotlib, seaborn, pandas, numpy, Pillow
- **Avaliação**: Matriz de confusão, Accuracy, Precision, Recall, F1-Score
- **Desafios**: Class masking (treino sem classes 4 e 7), teste OOD, imagens manuscritas próprias

## Como Executar

1. Clone o repositório:
```bash
git clone https://github.com/robertosim/mini-projeto-mnist.git
cd mini-projeto-mnist
```

2. Instale as dependências:
```bash
pip install -r requirements.txt
```

3. Abra o notebook:
```bash
jupyter notebook mini_projeto_mnist.ipynb
```

4. Para o Desafio C, adicione suas imagens manuscritas na pasta `data/meus_digitos/` (formato PNG ou JPG, fundo branco com traço escuro).

## Estrutura do Projeto

```
mini-projeto-mnist/
├── data/
│   └── meus_digitos/          # Imagens manuscritas (Desafio C)
├── mini_projeto_mnist.ipynb    # Notebook principal
├── requirements.txt            # Dependências
├── README.md                   # Esta documentação
└── LICENSE
```

## Fases do Pipeline

1. **Fase 1** - Carregamento e Análise Exploratória (EDA)
2. **Fase 2** - Pré-processamento e Divisão dos Dados
3. **Fase 3** - Implementação e Treinamento de 3 Modelos
4. **Fase 4** - Avaliação Comparativa de Desempenho
5. **Fase 5** - Estresse e Robustez (Desafios A, B e C)

## Melhorias Futuras

- Data augmentation para aumentar variância do treino
- Arquiteturas CNN (Redes Neurais Convolucionais) para extração espacial de features
- Tuning de hiperparâmetros com GridSearchCV/RandomizedSearchCV
- Ensemble dos 3 modelos para predição final
- Implantação via API REST (Flask/FastAPI)
