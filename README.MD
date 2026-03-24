# 💡 EcoAgente: Otimizador de Energia Inteligente (MVP)

[![Streamlit App](https://img.shields.io/badge/Demo%20ao%20vivo-Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white)](https://hackathoncid.streamlit.app/)
[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Google Gemini](https://img.shields.io/badge/Google%20Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://deepmind.google/technologies/gemini/)

> 🏆 Projeto desenvolvido durante o **Hackathon Careers in Data**, entregue em tempo real de competição por uma equipe de 5 pessoas.

---

## 📸 Demonstração

![EcoAgente Demo](https://hackathoncid.streamlit.app/)

> 👉 Acesse o app ao vivo: **[hackathoncid.streamlit.app](https://hackathoncid.streamlit.app/)**

---

## Sobre o projeto

O **EcoAgente** é um MVP que usa Inteligência Artificial e Machine Learning para identificar desperdício de energia residencial. O sistema analisa dados históricos de consumo, detecta anomalias estatísticas e projeta tendências para as próximas 24 horas — tudo isso com um agente conversacional integrado via Google Gemini que responde perguntas e sugere ações de economia.

O contexto importa: esse projeto foi concebido, desenvolvido e entregue **dentro do tempo de um hackathon**, o que significa que cada decisão técnica foi tomada sob pressão e com foco em funcionar.

---

## ✨ Funcionalidades

| Pilar | Descrição | Tecnologia |
|---|---|---|
| **Detecção de Anomalias** | Identifica picos de consumo estatisticamente atípicos no submedidor de entretenimento, com limite baseado em **1.5 Desvios Padrão** (μ + 1.5σ) do histórico completo | Análise Estatística |
| **Previsão de Tendência** | Projeta o consumo das próximas 24 horas com base no histórico, usando variáveis defasadas (t-1, t-24) | Regressão Linear (OLS) |
| **Agente Proativo** | Gera alertas e respostas contextuais com sugestões de economia em linguagem natural | Google Gemini API |
| **Análise Interativa** | Permite selecionar qualquer dia do histórico para investigação de anomalias | Streamlit |

---

## 🛠️ Stack utilizada

**Interface**
`streamlit` `altair`

**Machine Learning e Estatística**
`pandas` `numpy` `statsmodels`

**Inteligência Artificial**
`google-genai`

---

## ▶️ Como rodar localmente

### 1. Clone o repositório
```bash
git clone https://github.com/marcellospff/hackathoncid.git
cd hackathoncid
```

### 2. Instale as dependências
```bash
pip install -r requirements.txt
```

### 3. Configure a chave da API Gemini

Crie o arquivo `.streamlit/secrets.toml` na raiz do projeto (esse arquivo **não deve ser versionado**):

```toml
GEMINI_API_KEY = "sua_chave_api_aqui"
```

### 4. Dados

O arquivo `household_power_consumption.txt` já está incluído no repositório. Certifique-se de que ele está na raiz antes de rodar.

### 5. Execute o app

```bash
streamlit run hacka2.py
```

---

## 🎯 Testando a detecção de anomalia

1. Acesse a seção **Detecção de Anomalia e Chat**
2. Selecione a data **2007-08-11**
3. O sistema deve retornar um **ALERTA DE ANOMALIA** com o horário e valor do pico detectado

---

## 👥 Time

Projeto desenvolvido em equipe durante o Hackathon Careers in Data:

| Nome | GitHub |
|---|---|
| Marcello Siqueira | [@marcellospff](https://github.com/marcellospff) |
| Vitor Batista | — |
| Pedro Veloso | — |
| João Filipe | — |
| Ricardo | — |

---

## 📄 Licença

Este projeto está sob a licença MIT. Sinta-se livre para usar como referência ou ponto de partida.
