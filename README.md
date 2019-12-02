## Projeto Final
Análise do dataset do paper "From Reports to Bug-Fix Commits: A 10 Years Dataset of Bug-Fixing Activity from 55 Apache's Open Source Projects" disponível em Local O Foco da nossa análise foi sobre o dataset de bug-fixed do Hadoop (Core, HDFS, Yarn e MapReduce)

### Descrição do projeto:
Este projeto tem como objetivo explorar e analisar um subconjunto de datasets extraídos e propostos no paper "From Reports to Bug-Fix Commits: A 10 Years Dataset of Bug-Fixing Activity from 55 Apache’s Open Source Projects" [1], visto a importância da análise de repositórios de softwares livres através da mineração de dados para identificar padrões de comportamento dos bugs ao longo da evolução do software. Por exemplo, tipos de bug, criticidade, predição, correção entre outros fatores críticos referentes a análise de bugs podem ser explorados. Como o dataset é muito grande (156 arquivos .csv) resolvemos escolher um subconjunto do dataset do framework do Hadoop [2] (composto pelos módulos Core [3], Yarn [4], HDFS [5] e Mapreduce [6]), visto que o percentual de bugs da suíte do Hadoop representa aproximadamente 30% do conjunto total de bugs registrados.

### Público Alvo:
Developers que usam o framework e developers que dão manutenção no mesmo.

### Descrição dos Dados:
Os dados foram obtidos por meio do paper em análise, o qual foram disponibilizados 156 arquivos no formato .csv. Devido o dataset ser muito grande, resolvemos escolher um subconjunto de dados, nesse subconjunto estão inclusos os seguintes módulos do framework Hadoop: Core, Yarn, HDFS e Mapreduce. Ao total são cerca de 10.735 registros de bugs o que representa aproximadamente 30% do conjunto total de bugs registrados. Para a análise inicial do dataset e geração dos protótipos de gráficos no Tableau [7] foi necessário substituir o separador de vírgula para ponto e vírgula, além de realizar uma junção dos arquivos .csv referentes aos projetos em análise, visto que cada projeto analisado possui um arquivo em separado com os registros de seus respectivos bugs. Para fazer a limpeza e transformação dos dados foi usada a biblioteca Pandas [8] do Python [9]. Nessa etapa, cada arquivo .cvs foi analisado de forma a identificar os tipos de dados de cada coluna, identificar dados faltantes, dados nulos, transformações de dados do tipo string para numéricos ou tipos data, eventualmente também poderão ser criados campos calculados para facilitar a análise dos dados. Além disso, todas as etapas de limpeza e transformação de dados foram publicadas no notebook do Google Colabs [10] via link para que sejam visualizadas de forma detalhada o que foi feito em cada uma das etapas.

### Perguntas de partida / hipóteses:
- Qual o tempo médio de resolução dos bugs?
- Qual a prioridade dos bugs?
- Os bugs críticos são resolvidos mais rápidos?

### Tecnologias/ferramentas utilizadas:
Python [9], Pandas [8], Seaborn [11], Jupyter Notebook [12], JavaScript [13] e D3 [14], Google Colabs [10], Tableau [7] e Code Flower.

### Referências

## Referencias bibliográficas

- [1] Renan Vieira, Antônio da Silva, Lincoln Rocha, and João Paulo Gomes. 2019. From Reports to Bug-Fix Commits: A 10 Years Dataset of Bug-Fixing Activity from 55 Apache's Open Source Projects. In Proceedings of the Fifteenth International Conference on Predictive Models and Data Analytics in Software Engineering (PROMISE'19). ACM, New York, NY, USA, 80-89. DOI: https://doi.org/10.1145/3345629.3345639

- [2] Hadoop - Framework open-source para computação massiva paralela e distribuída de dados. Disponível em [https://hadoop.apache.org](https://hadoop.apache.org)

- [3] Hadoop Core - Integração do Sistema de Arquivos distribuídos HDFS e o modelo de programação Mapreduce. Disponível em [https://hadoop.apache.org/releases.html](https://hadoop.apache.org/releases.html)

- [4] Hadoop Yarn - Gerenciamento dos recursos dentro dos clusters criados. Disponível em https://[hadoop.apache.org/docs/current/hadoop-yarn/hadoop-yarn-site/YARN.html](hadoop.apache.org/docs/current/hadoop-yarn/hadoop-yarn-site/YARN.html)

- [5] Hadoop HDFS - Sistema de Arquivos Distribuídos do Hadoop. Disponível em https://[hadoop.apache.org/docs/r1.2.1/hdfs_design.html](hadoop.apache.org/docs/r1.2.1/hdfs_design.html)

- [6] Hadoop Mapreduce - Modelo de Programação Paralela do Hadoop. Disponível em https://[hadoop.apache.org/docs/r1.2.1/mapred_tutorial.html](hadoop.apache.org/docs/r1.2.1/mapred_tutorial.html)

- [7] Tableau - Software de Visualização de Dados. Disponível em [https://www.tableau.com](https://www.tableau.com)

- [8] Pandas - Biblioteca de Software escrita em Python para manipulação e análise de dados. Disponível em [https://pandas.pydata.org](https://pandas.pydata.org)

- [9] Python - Linguagem de Programação interpretada de propósito geral. Disponível em [https://www.python.org](https://www.python.org)

- [10] Google Colabs - Plataforma on-line do Google implementada sobre o Jupyter Notebook para publicar na Web programas feitos em Python. Disponível em [https://colab.research.google.com/](https://colab.research.google.com/)

- [11] Seaborn - Biblioteca escrita em Python para construção e exibição de gráficos estatísticos. Disponível em [https://seaborn.pydata.org](https://seaborn.pydata.org)

- [12] Jupyter Notebook - Plataforma on-line para publicar dados interativos. Disponível em [https://jupyter.org](https://jupyter.org)

- [13] JavaScript - Linguagem de programação interpretada para Browsers Web e Servidores Web. Disponível em [https://developer.mozilla.org/en-US/docs/Web/JavaScript](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

- [14] D3 (Data-Driven Documents) - Biblioteca JavaScript para produzir visualização de dados em Browsers Web disponível em [https://d3js.org](https://d3js.org)

- [15] Code Flower - Ferramenta para visualização de repositório de código em uma árvore interativa. Disponível em [http://www.redotheweb.com/CodeFlower/](http://www.redotheweb.com/CodeFlower/)
