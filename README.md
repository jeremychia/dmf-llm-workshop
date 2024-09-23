# dmf-llm-workshop
2024.09.23 in porto

# Why groq?
* [Groq Console](https://console.groq.com/login)
* Free LLMs


Install requirements:
```shell
pip install tqdm jupyter elasticsearch groq
```

Launch jupyter notebook:
```shell
jupyter notebook
```

Run elastic search with Docker:
```shell
docker run -it \
    --rm \
    --name elasticsearch \
    -m 2G \
    -p 9200:9200 \
    -p 9300:9300 \
    -e "discovery.type=single-node" \
    -e "xpack.security.enabled=false" \
    docker.elastic.co/elasticsearch/elasticsearch:8.4.3
```

Check that Elastic Search is running:
```shell
curl http://localhost:9200
```

For this course, they used the sample:
```shell
wget https://github.com/alexeygrigorev/llm-rag-workshop/raw/main/notebooks/documents.json
```

Now try with something local:
```shell
curl -fsSL https://ollama.com/install.sh | sh
```

To run phi3
```shell
ollama start;
ollama run phi3
```