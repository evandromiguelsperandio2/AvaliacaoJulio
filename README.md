# AvaliacaoJulio

# 📊 Projeto de Avaliação - Streamlit na AWS EC2

Este projeto tem como objetivo demonstrar a criação e o deploy de uma aplicação simples utilizando a biblioteca **Streamlit** em uma instância **EC2 da AWS**, permitindo acesso público via navegador. A aplicação carrega e exibe dados de um arquivo CSV, gerando uma visualização interativa.

---

## ✅ Objetivo da Avaliação

- Criar uma instância EC2 com Ubuntu 22.04 ou superior.
- Instalar Python, pip e dependências.
- Configurar o ambiente para rodar uma aplicação Streamlit.
- Subir uma aplicação que lê um CSV e mostra visualizações.
- Tornar a aplicação acessível via navegador (porta 8501).
- Subir o código no GitHub com um README explicativo.

---

## 🛠️ Tecnologias Utilizadas

- Python 3.12
- Streamlit
- Pandas
- Matplotlib
- AWS EC2 (Ubuntu Server)
- Git

---

## 📁 Estrutura do Projeto

AvaliacaoJulio/
├── app.py # Aplicação Streamlit
├── MS_Financial_Sample.csv # Arquivo de dados
├── requirements.txt # Lista de dependências
└── README.md # Este arquivo

---

## 🚀 Como Rodar o Projeto Localmente

### 1. Clone o repositório

bash
git clone https://github.com/SEU_USUARIO/SEU_REPOSITORIO.git
cd SEU_REPOSITORIO

### 2. (Opcional) Crie um ambiente virtual
python3 -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

### 3. Instale as dependências
pip install -r requirements.txt

### 4. Execute o Streamlit
streamlit run app.py

Acesse em seu navegador:
http://localhost:8501
