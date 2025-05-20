O projeto em questão contempla o desmatamento em biomas do Brasil. O repositório contem os seguintes arquivos:
  - fonte de dados de arquivo csv (tabela de dados);
  - documentação das etapas desenvolvidas em arquivo pdf;
  - manipulação e preparação dos dados via pyspark em arquivo ipynb;
  - arquivo pdf contendo o layout visual do relatório;
  - link para p dashboard interativo no google looker studio;

Foi feito download da fonte de dados do site basededados.org em formato csv. Em seguida foi criado a estrutura em Pyspark no Google Colab para receber esses dados e ser possível sua manipulação. Neste ambiente 
os dados foram preparados e ajustados, sendo possível a extração de algumas informações já neste momento.
Vale a observação que no código ipynb no Google Colab foi criado um campo "caracteristicas" que armazenava os valores de outros 5 campos, e em seguida um novo
campo foi criado chamado "caracteristicas_normalizadas". Utilizei esse campo para o modelo de regressão linear, para verificar o impacto desses valores sobre o 
campo "desmatado". Porém, no fim, para conseguir salvar como csv foi necessário deletar as duas colunas contendo vetores, caso não fizesse isso, seria necessário
salvar o arquivo como .parquet.
Em seguida, com os dados já tratados, fizemos a integração com o Looker Studio para gerar um relatório interativo, que desse a possibilidade do usuário 
personalizar a visualização dos dados de acordo com o que quisesse ver no momento.
