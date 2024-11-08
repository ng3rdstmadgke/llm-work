# 起動方法

JupyterLabの起動

```bash
./bin/jupyter.sh
```

notebookを開いてランタイムに先ほど起動したJupyterのプロセスを指定

ランタイムの項目をクリック

<img src="./docs/img/jupyter/01.png" width="700px">

「別のカーネルを選択」をクリック

<img src="./docs/img/jupyter/02.png" width="700px">

「既存のJupyterサーバー」をクリック

<img src="./docs/img/jupyter/03.png" width="700px">

JupyterのURLを設定

<img src="./docs/img/jupyter/04.png" width="700px">

任意の表示名を入力

<img src="./docs/img/jupyter/05.png" width="700px">


# Langserveの起動

```bash
python app/main.py
```

http://localhost:8000/chain/playground/ にアクセス


# LangSmithの利用

https://smith.langchain.com/ にアクセスしてサインアップ


手順に沿ってAPIキーを作成して、環境変数を設定


<img src="./docs/img/langsmith/01.png" width="1000px">


OpenAIのAPIにアクセスする

```python
from langchain_openai import ChatOpenAI
llm = ChatOpenAI()
llm.invoke("Hello, world!")
```

# Tavilyの利用

https://tavily.com/