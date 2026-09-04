# MapReduce

MapReduce em Python Puro Análise de Viagens de Táxi de Nova York

Atividade avaliativa que implementa o paradigma MapReduce (Map → Shuffle → Reduce) do zero, em Python nativo, sem nenhuma biblioteca externa nem módulo da biblioteca padrão, para responder seis perguntas sobre uma amostra de 1 milhão de viagens de táxi amarelo de Nova York em 2024.

Open In Colab

Substitua SEU_USUARIO/SEU_REPOSITORIO no link acima pelo caminho real do seu repositório antes de publicar.

Sobre a atividade
Aluno: Kaike
Curso: Data Science e Inteligência Artificial — Centro Universitário IESB
Professor: Alexandre Vaz Roriz
Restrição da atividade: nenhuma biblioteca pode ser usada — apenas recursos nativos do Python (open, str, list, dict, for, sum, max, len, enumerate) e os conceitos de MapReduce.
Sobre os dados
Dataset: amostra de 1.000.000 de viagens de táxi amarelo de NY em 2024 (nyc_tripdata_2024_sample_1M.csv), baseada no dataset público de Yellow Taxi Trip Records da NYC Taxi & Limousine Commission (TLC).
Dicionário de dados oficial: NYC TLC — Trip Record Data
O arquivo CSV (~130 MB) não está neste repositório. O GitHub bloqueia push de arquivos acima de 100 MB sem Git LFS, então o dataset precisa ser baixado separadamente e colocado na pasta /content do Colab antes de rodar o notebook (o link para baixar fica na seção "Como rodar" abaixo).
Metodologia

O notebook implementa um pequeno "motor" de MapReduce genérico com quatro funções:

mapear — fase Map: transforma cada viagem em um ou mais pares (chave, valor).
agrupar — fase Shuffle: agrupa os pares gerados por chave.
reduzir — fase Reduce: aplica uma função de agregação sobre os valores de cada chave.
map_reduce — orquestra as três fases acima.

Cada uma das 6 perguntas é resolvida escrevendo apenas uma função de map e uma de reduce específicas, reaproveitando esse mesmo motor. A leitura do CSV também é feita na mão (open() + str.split(",")), sem o módulo csv.

Como rodar
Baixe o CSV nyc_tripdata_2024_sample_1M.csv (fonte listada acima) e faça upload manual para a pasta /content do Google Colab (aba de arquivos → ícone de upload).
Abra o notebook Atividade_MapReduce.ipynb deste repositório no Colab (pode usar o badge "Open in Colab" no topo deste README).
Rode todas as células em ordem: Ambiente de execução → Executar tudo.
