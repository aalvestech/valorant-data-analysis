FROM jupyter/pyspark-notebook

# Cria e muda para o diretório de trabalho
WORKDIR /home/jovyan/repos/valorant-data-analysis

# Copia os arquivos necessários para o diretório de trabalho
COPY . .

# Instala as dependências do Python
RUN conda install pip && \
    pip install --no-cache-dir -r requirements.txt && \
    python -m ipykernel install --user --name pyspark --display-name "PySpark"

CMD ["start-notebook.sh", "--NotebookApp.token=''", "--NotebookApp.password=''"]