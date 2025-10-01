<p align="center">
  <h1 align="center"> Community Policy Classifier</h1>
  <p align="center">Classificação de frases <b>Adequadas</b> vs. <b>Potencialmente Violadoras</b> usando LSTM, GRU e BERT</p>

  <!-- Badges principais -->
  <p align="center">
    <img src="https://img.shields.io/badge/python-3.12-blue?logo=python&logoColor=white" alt="Python Version">
    <img src="https://img.shields.io/badge/TensorFlow-2.x-orange?logo=tensorflow&logoColor=white" alt="TensorFlow">
    <img src="https://img.shields.io/badge/Explainers-LIME%20%7C%20SHAP-green" alt="Explainability">
    <img src="https://img.shields.io/badge/status-educacional-lightgrey" alt="Status">
  </p>
</p>

---


# 🧠 Community Policy Classifier
Classificador de frases **Adequadas vs. Potencialmente Violadoras de Políticas de Comunidade**, desenvolvido como estudo de **NLP aplicado à moderação de conteúdo**.  
O projeto implementa diferentes modelos de **Deep Learning (LSTM/GRU)** e **Transformers (BERT)**, avaliando desempenho, métricas e interpretabilidade com **LIME e SHAP**.

---

## 📌 Objetivo
Demonstrar um pipeline completo de **Processamento de Linguagem Natural (NLP)**:
1. Coleta e construção de dataset fictício e seguro.
2. Pré-processamento (tokenização, padding).
3. Treinamento de modelos avançados (LSTM, GRU, BERT).
4. Avaliação com métricas clássicas e avançadas.
5. Explicabilidade (LIME/SHAP) para interpretação de decisões.
6. Documentação ética sobre uso responsável.

---

## 📂 Estrutura do Projeto
```
NLP_CommunityPolicyClassifier/
├── data/ # Dados fictícios (CSV)
├── notebooks/ # Jupyter Notebooks com experimentos
│ ├── lstm_gru_classifier.ipynb
│ └── explainability.ipynb
├── models/ # Modelos treinados (.h5, .pt)
├── reports/ # Gráficos, métricas e explicações
├── src/ # Código modularizado
│ ├── preprocess.py
│ ├── train.py
│ ├── evaluate.py
│ └── explain.py
├── README.md # Este arquivo
└── ETHICS.md # Documento de ética e boas práticas
```

---

## ⚙️ Tecnologias Utilizadas
- **Linguagem:** Python 3.12  
- **Bibliotecas principais:**
  - `TensorFlow / Keras` (LSTM, GRU)
  - `scikit-learn` (métricas)
  - `LIME` e `SHAP` (explicabilidade)
  - `Matplotlib / Seaborn` (visualizações)

---

## 🔎 Dataset Fictício
Criado manualmente para fins **didáticos**.  
Classes:
- `0 = Adequado`
- `1 = Potencial violador`

Exemplo:
| Frase | Label |
|-------|-------|
| "Seu trabalho ficou excelente, parabéns!" | 0 |
| "Você só fala besteira, cala a boca" | 1 |

---

## 📊 Modelos Implementados

### 🔹 LSTM / GRU (Keras)
- **Embedding + LSTM/GRU + Dense**  
- Métricas: Accuracy, Precision, Recall, F1, ROC-AUC  
- Explicabilidade: **LIME** (local) e **SHAP** (global)


---

## 📈 Resultados

| Modelo   | Accuracy | Precision | Recall | F1 | AUC  | Tempo de Treino |
|----------|----------|-----------|--------|----|------|-----------------|
| **LSTM** | 0.90     | 0.91      | 0.89   | 0.90 | 0.92 | ~12s |
| **GRU**  | 0.88     | 0.89      | 0.87   | 0.88 | 0.91 | ~8s  |

*(valores ilustrativos, ajustar após rodar no notebook)*

---

## 📊 Visualizações

### Avaliação do Modelo (LSTM)

Para avaliar o desempenho do modelo LSTM, utilizamos a **Matriz de Confusão**, que mostra a quantidade de classificações corretas e incorretas:

- **Classe 0** → Comentários não ofensivos  
- **Classe 1** → Comentários ofensivos  

Na figura abaixo:  
- 🔵 Os quadrados escuros representam predições corretas.  
- ⚪ Os quadrados claros representam erros de classificação.  

![Matriz de Confusão - LSTM](./reports/matriz_confusao.jpeg)


### Interpretação do Modelo com LIME

Para entender como o modelo de NLP chega às suas previsões, utilizamos a técnica **LIME (Local Interpretable Model-agnostic Explanations)**.  
Abaixo, um exemplo de explicação para a frase *"Adoro participar das discussões neste fórum"*:

- As palavras destacadas em azul contribuíram fortemente para a classificação como **Classe 0** (comentário não ofensivo).
- A probabilidade prevista foi de **98% para Classe 0** e **2% para Classe 1**.

![Explicação LIME](./reports/html.jpeg)


---

## 🛡️ Ética e Limitações
> ⚠️ Este projeto tem **finalidade exclusivamente educacional**.

- Dataset **fictício e seguro** → sem frases reais de ódio.  
- Modelos de NLP para moderação **não devem ser usados em produção sem revisão humana**.  
- Possibilidade de **falsos positivos** (moderar frases aceitáveis) ou **falsos negativos** (não detectar violação).  
- Explicabilidade (LIME/SHAP) usada para garantir **transparência** das decisões.  

📖 Detalhes adicionais em [ETHICS.md](./ETHICS.md)

---

## 🚀 Como Rodar

# Clonar repositório
```
git clone https://github.com/seu-usuario/NLP_CommunityPolicyClassifier.git
cd NLP_CommunityPolicyClassifier
```

# Criar ambiente virtual
```
python -m venv .venv
source .venv/bin/activate  # Linux/Mac
.venv\Scripts\activate     # Windows
```

# Instalar dependências
```
pip install -r requirements.txt
```

# Rodar notebooks
```
jupyter notebook notebooks/lstm_gru_classifier.ipynb
```


Próximos Passos

- Testar outros modelos pré-treinados (RoBERTa, DistilBERT).

- Experimentar técnicas de data augmentation para aumentar robustez.

- Deploy com FastAPI/Streamlit (apenas para demonstração com exemplos fictícios).