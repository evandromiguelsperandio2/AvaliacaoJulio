# Deploy de Aplicação Streamlit na AWS EC2

Este projeto demonstra como criar e hospedar uma aplicação Streamlit simples em uma instância EC2 da AWS, utilizando Ubuntu 22.04 ou superior. A aplicação exibe um título, um texto e um gráfico gerado a partir de um dataset.

## 🚀 Objetivo

Tornar uma aplicação Streamlit acessível publicamente por meio de um navegador, utilizando uma instância EC2 na AWS.

---

## 🛠️ Passo a Passo

### 1. Criar Instância EC2
- Sistema operacional: **Ubuntu Server 22.04 ou superior**
- Tipo de instância: `t2.micro` (para fins de teste)
- Grupo de Segurança: libere as portas:
  - `22` (SSH)
  - `8501` (Streamlit)

### 2. Conectar via SSH

chmod 400 sua-chave.pem
ssh -i "sua-chave.pem" ubuntu@<IP-da-instância>
3. Instalar Python, pip e dependências

sudo apt update && sudo apt upgrade -y
sudo apt install python3 python3-pip -y
pip3 install streamlit pandas matplotlib

4. Enviar ou criar o arquivo app.py
Você pode usar scp para enviar arquivos:
scp -i admin.pem app.py ubuntu@44.203.254.93:/home/ubuntu/app.py
scp -i admin.pem "MS_Financial_Sample.csv" ubuntu@44.203.254.93:/home/ubuntu/AvaliacaoJulio/

Ou clone diretamente do GitHub (se já estiver publicado):
git clone https://github.com/evandromiguelsperandio2/AvaliacaoJulio
cd AvaliacaoJulio

5. Rodar a aplicação Streamlit
streamlit run app.py --server.port=8501 --server.address=0.0.0.0

🌐 Acessar Aplicação no Navegador
Abra no navegador:
http://<IP-da-instância>:8501

📄 Como Rodar Localmente
Requisitos:
Python 3.8+
pip

Instalação:
git clone https://github.com/evandromiguelsperandio2/AvaliacaoJulio
cd nome-do-repo
pip install -r requirements.txt

Executar:
streamlit run app.py

📁 Estrutura do Projeto
📦nome-do-repo
 ┣ 📄 app.py
 ┣ 📄 dataset.csv
 ┣ 📄 README.md
 ┗ 📄 requirements.txt
📦 Requisitos
No arquivo requirements.txt, inclua:
streamlit
pandas
matplotlib


🏆 Critérios Avaliados
Item	Pontos
EC2 configurada corretamente	30
Acesso público pela porta 8501	30
Aplicação funcional com Streamlit	20
Código limpo e funcional	10
README com instruções detalhadas	10
Total	100


