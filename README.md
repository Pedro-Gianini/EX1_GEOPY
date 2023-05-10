## Solução dos exercícios da primeira aula do curso GeoPY

Bibliotecas usadas: shapely.geometry ; pandas ; tqdm ; geopandas ; google.colab

Funções usadas:
Aqui estão todas as funções utilizadas nos códigos fornecidos:
Point() ; distance() ;  LineString() ; length() ; Polygon() ; centroid() ; area() ; box() ; MultiPoint() ; read_csv() ; unique() ; tqdm()

Conteúdos abordados/explicação do exercício :
# Exercício 1 #
Esse código em Python usa a biblioteca shapely para manipular objetos geométricos, tais como pontos, linhas e polígonos.
Na primeira parte do código, o objeto "Point" é importado da biblioteca shapely. Em seguida, cinco pontos são criados manualmente e a distância entre cada par de pontos é calculada e exibida na tela. Em seguida, um loop é usado para automatizar o cálculo das mesmas distâncias.
Na segunda parte do código, o objeto "LineString" é importado da biblioteca shapely. Uma linha é criada a partir dos pontos criados anteriormente e o comprimento dessa linha é calculado e exibido na tela.
Na terceira parte do código, o objeto "Polygon" é importado da biblioteca shapely. Um polígono é criado a partir dos pontos criados anteriormente e o centroide desse polígono é calculado e exibido na tela. Além disso, a área do polígono é calculada e exibida na tela.
Na quarta parte do código, o objeto "box" é importado da biblioteca shapely. A partir dos valores mínimo e máximo das coordenadas dos pontos, uma caixa delimitadora é criada e exibida na tela.
Na quinta parte do código, o objeto "MultiPoint" é importado da biblioteca shapely. Vários pontos são agrupados em um único objeto do tipo MultiPoint e esse objeto é exibido na tela.

# Exercício 2 #
Este é um código escrito em Python que utiliza bibliotecas como Pandas, Shapely, TQDM e Geopandas para fazer análise e visualização de dados geoespaciais. O objetivo do código é criar pontos e linhas a partir de dados em tabelas CSV e, em seguida, plotá-los em um mapa.
A primeira parte do código monta o Google Drive, onde estão armazenados os arquivos CSV com os dados que serão utilizados. Em seguida, o código carrega o arquivo "stops.txt" em um dataframe do Pandas e cria uma lista de objetos Point do Shapely a partir das coordenadas de latitude e longitude das paradas de ônibus contidas na tabela. 
A segunda parte do código carrega o arquivo "shapes.txt" em um dataframe do Pandas e seleciona apenas as linhas com um determinado ID de forma (shape_id). Em seguida, cria uma lista de objetos Point do Shapely a partir das coordenadas de latitude e longitude das formas de ônibus contidas na tabela. Depois, usa esses pontos para criar uma única linha usando o objeto LineString do Shapely.
 A terceira parte do código utiliza um loop para criar uma lista de linhas de ônibus para cada shape_id contido na tabela "shapes.txt". O loop usa o tqdm() para medir o progresso do processo. Em cada iteração, o loop seleciona as linhas de ônibus correspondentes ao shape_id atual, ordena-as pela ordem das paradas e cria uma linha a partir dos pontos contidos nessas linhas.
A quarta parte do código calcula o comprimento médio das linhas de ônibus geradas na parte C. Em seguida, utiliza o objeto MultiLineString do Shapely e o pacote Geopandas para plotar as linhas de ônibus em um mapa.

DESAFIO -- -- --- --- -- -- -- --- -- --- -- ----- --- -- -- --- -- --- --- --- -- --- --- -- --- ---- -- --- --- -- 
Além disso, o código apresenta uma função para criar pontos e uma função para criar linhas. A função "cria_pontos" utiliza a biblioteca Shapely para criar objetos Point a partir das coordenadas de latitude e longitude contidas em uma tabela do Pandas. A função "cria_linhas" utiliza a biblioteca Shapely para criar objetos LineString a partir das coordenadas de latitude e longitude contidas em uma tabela do Pandas e ordena esses pontos de acordo com uma coluna de sequência. Ambas as funções podem ser usadas para criar pontos e linhas personalizados a partir de tabelas de dados CSV. No final do código, a função "cria_linhas" é chamada para criar uma linha a partir das formas de ônibus contidas no dataframe "linhas_sub".
