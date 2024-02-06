<h1>Explore o Machine Learning Automatizado no Azure Machine Learning</h1>
<hr>
<p>Neste exercício, você usará o recurso de aprendizado de máquina automatizado no Azure Machine Learning para treinar e avaliar um modelo de aprendizado de máquina.</p>
<p>Selecione + Criar um recurso , pesquise Machine Learning e crie um novo recurso do Azure Machine Learning com as seguintes configurações:</p>

<li>Grupo de recursos : Crie ou selecione um grupo de recursos .</li>
<li>Nome : Insira um nome exclusivo para seu espaço de trabalho .</li>
<li>Região : Selecione a região geográfica mais próxima .</li>
<li>Registro de contêiner : Nenhum</li>
<br>
<p>Selecione Revisar + criar e selecione Criar . Aguarde a criação do seu espaço de trabalho (pode demorar alguns minutos) e, em seguida, vá para o recurso implantado.</p>
<p>No estúdio Azure Machine Learning, você deverá ver seu espaço de trabalho recém-criado.</p>
<h2>Use aprendizado de máquina automatizado para treinar um modelo</h2>
<p>O aprendizado de máquina automatizado permite que você experimente vários algoritmos e parâmetros para treinar vários modelos e identificar o melhor para seus dados.</p>
<p>Na aba do lado esquerdo selecione Automated ML.</p>
<br>
Configurações básicas:
<li>Nome do trabalho : mslearn-bike-automl</li>
<li>Novo nome do experimento : mslearn-bike-rental</li>
<li>Descrição : Aprendizado de máquina automatizado para previsão de aluguel de bicicletas</li>
<li>Marcadores : nenhum</li>
<br>
<li>Tipo de tarefa e dados:Selecione o tipo de tarefa : Regressão</li>
<li>Selecionar conjunto de dados : crie um novo conjunto de dados com as seguintes configurações:</li>
<br>
Tipo de dados:
<li>Nome : aluguel de bicicletas</li>
<li>Descrição : dados históricos de aluguel de bicicletas</li>
<li>Tipo : Tabular</li>
<br>
Fonte de dados:
<li>Selecione Dos arquivos da web</li>
<br>
URL da Web:
<li>URL da Web :https://aka.ms/bike-rentals</li>
<li>Ignorar validação de dados : não selecionar</li>
<br>
Configurações:
<li>Formato de arquivo : Delimitado</li>
<li></li>Delimitador : Vírgula</li>
<li>Codificação : UTF-8</li>
<li>Cabeçalhos de coluna : apenas o primeiro arquivo possui cabeçalhos</li>
<li>Pular linhas : Nenhum</li>
<li>O conjunto de dados contém dados multilinhas : não selecione</li>
<br>
Esquema:
<li>ncluir todas as colunas exceto Caminho</li>
<br>
<p>Selecione Criar . Após a criação do conjunto de dados, selecione o conjunto de dados de aluguel de bicicletas para continuar a enviar o trabalho de ML automatizado.</p>
<br>
Configurações de tarefa:
<li>Tipo de tarefa : Regressão</li>
<li>Conjunto de dados : aluguel de bicicletas</li>
<li>Coluna de destino : Aluguéis (inteiro)</li>
<br>
Configurações adicionais:
<li>Métrica primária : raiz do erro quadrático médio normalizado</li>
<li>Explique o melhor modelo : Não selecionado</li>
<li>Usar todos os modelos suportados : Desmarcado.</li>
<li>Modelos permitidos : Selecione apenas RandomForest e LightGBM</li>
<br>
Limites:
<li>Máximo de testes : 3</li>
<li>Máximo de testes simultâneos : 3</li>
<li>Máximo de nós : 3</li>
<li>Limite de pontuação da métrica : 0,085</li>
<li>Tempo limite : 15</li>
<li>Tempo limite de iteração : 15</li>
<li>Habilitar rescisão antecipada : selecionado</li>
<br>
Validação e teste:
<li>Tipo de validação : divisão de validação de treinamento</li>
<li>Porcentagem de dados de validação : 10</li>
<li>Conjunto de dados de teste : Nenhum</li>
<br>
Calcular:
<li></li>Selecione o tipo de computação : sem servido</li>
<li>Tipo de máquina virtual : CPU</li>
<li>Camada de máquina virtual : Dedicada</li>
<li>Tamanho da máquina virtual : Standard_DS3_V2*</li>
<li>Número de instâncias : 1</li>
<br>
<h2>Avalie o melhor modelo</h2>
<br>
<h2>Implantar e testar o modelo</h2>
<br>
<h2>Testar o serviço implantado</h2>
<br>
<code>{
  "Inputs": {
    "data": [
      {
        "day": 0,
        "mnth": 0,
        "year": 0,
        "season": 0,
        "holiday": 0,
        "weekday": 0,
        "workingday": 0,
        "weathersit": 0,
        "temp": 0.0,
        "atemp": 0.0,
        "hum": 0.0,
        "windspeed": 0.0
      }
    ]
  },
  "GlobalParameters": 0.0
}</code>
<br>
<br>
<br>
<code>{
  "Results": [
    492.265776724701
  ]
}</code>


