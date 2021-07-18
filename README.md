# INTEGRACuBe

INTEGRACuBe (INTErlevel data inteGRAtionCuBe) é uma ferramenta desenvolvida na plataforma do Pentaho Data Integration através do framework ETL4LOD+ (https://ufrj.gitbook.io/etl4lod/) com objetivo de aplicar os recursos do vocabulário RDF Data Cube a um conjunto de dados armazenado no \textit{Triplestore}, através de mecanismos semiautomatizados, transformando o grafo tradicional em um grafo multidimensional. 

# Detalhes da Ferramenta

INTEGRACuBe utiliza um metaesquema, mais especificamente os recursos table e tuple, da abordagem INTEGRA (https://github.com/jonesavelino/INTEGRA). Ele foi implementado por meio de um Job, composto por seis Steps que permitem identificar os recursos dimensão e fato a partir do metaesquema do INTEGRA. Em seguida, INTEGRACuBe  realiza o mapeamento das classes do metamodelo RDF Data Cube, até a geração do cubo de dados e sua persistência no Triplestore. A ferramenta INTEGRACuBe utiliza dois mecanismos para persistir o cubo de dados gerado. A primeira utiliza o Openlink Virtuoso (https://virtuoso.openlinksw.com/) para armazenamento dos dados. Já a segunda, gera o cubo de dados no formato NTriples (https://www.w3.org/TR/n-triples/). A exportação do cubo de dados permite que os dados sejam explorados através de ferramentas que adotam o paradigma OLAP com o vocabulário RDF Data Cube. Nesse sentido, INTEGRACuBe utiliza o OpenCube Toolkit (http://opencube-toolkit.eu/) para exploração dos dados. 

# Descrição do Projeto

A ferramenta INTEGRACuBe oferece um conjunto de passos bem definidos que permitem a adoção do vocabulário RDF Data Cube em grafos RDF. INTEGRACuBe surge para atender a necessidade de análise de dados em grafos RDF utilizando dimensões e fatos. Esse mecanismo é extremamente importante quando há demandas de gestores que realizam análises de dados utilizando mais de uma única dimensão.

# Pré-requisito

Este projeto possui as seguintes dependências:

- [Java 8] (https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html) para rodar as bibliotecas e desenvolvimento, caso necessário.
- [Maven] (https://maven.apache.org/) para gestão de dependências, caso necessário.
- [Pentado PDI - Kettle 8.2] (https://sourceforge.net/projects/pentaho/) para rodar a solução INTEGRATeS (conjunto de arquivos .ktr)
- [ETL4LOD Plus] (https://github.com/johncurcio/ETL4LODPlus) para rodar e utilizar as bibliotecas de triplificação 
- [LIMES] (https://github.com/dice-group/LIMES) para rodar a solução de descoberta de ligações
- [Openlink Virtuoso] (https://virtuoso.openlinksw.com/) para armazenar os dados dos _datasets_ e os _matchers_
- [OpenCube Toolkit] (http://opencube-toolkit.eu/) para realizar a exploração dos cubos de dados.

# Instalação

- [X] Instalar o JAVA 8 (JDK);
- [X] Instalar o Maven;
- [X] Instalar o Pentado PDI - Kettle;
- [X] Instalar os packages do ETL4LODPlus, conforme instruções do proprietário;
- [X] Instalar os packages do LIMES, conforme instruções do proprietário;
- [X] Instalar o OpenCube Toolkit;

# Deploy
- Executar o comando: mvn clean install
