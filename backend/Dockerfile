# Use uma imagem oficial do Python
FROM python:3.9-slim

# Defina o diretório de trabalho dentro do container
WORKDIR /app

# Copie os arquivos requirements.txt para o container
COPY requirements.txt .

# Instale as dependências do Python
RUN pip install --no-cache-dir -r requirements.txt

# Copie o restante do código da aplicação para o container
COPY . .

# Defina a variável de ambiente para o Flask
ENV FLASK_APP=app.py

# Exponha a porta 5000
EXPOSE 5000

# Comando para rodar a aplicação Flask
CMD ["flask", "run", "--host=0.0.0.0"]
