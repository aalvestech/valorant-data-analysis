FROM jupyter/pyspark-notebook

WORKDIR /home/jovyan/repos/valorant-data-analysis

COPY . .

RUN conda install pip && \
    pip install --no-cache-dir -r requirements.txt && \
    python -m ipykernel install --user --name pyspark --display-name "PySpark"

CMD ["start-notebook.sh", "--NotebookApp.token=''", "--NotebookApp.password=''"]