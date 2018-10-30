# Aprendizagem de Máquina

## 2ª Rodada de Problemas - Grupo A

### Dataset

O Dataset do problema mede o tempo de execução de um produto matricial (A * B = C), no qual todas as matrizes possuem o tamanho 2048x2048. em um kernel GPU SGEMM parametrizável com 241600 combinações possíveis. Para cada combinação foram executados 4 testes, com a medição do tempo em milissegundos.

O dataset do problema pode ser encontrado [aqui](https://archive.ics.uci.edu/ml/datasets/SGEMM+GPU+kernel+performance#)

#### Conjunto de Dados

1. **MWG e NWG**
    * Colunas 1 e 2
    * **Descrição:** ladrilhos 2D por matriz no nível do grupo de trabalho.
    * **Domínio:** {16, 32, 64, 128} (Inteiro)
1. **KWG**
    * Coluna 3
    * **Descrição:** dimensão interna do ladrilho 2D no nível do grupo de trabalho.
    * **Domínio:** {16, 32} (Inteiro)
1. **MDIMC e NDIMC**
    * Colunas 4 a 5
    * **Descrição:** tamanho do grupo de trabalho local.
    * **Domínio:** {8, 16, 32} (Inteiro)
1. **MDIMA e NDIMB**
    * Colunas 6 a 7
    * **Descrição:** forma da memória local.
    * **Domínio:** {8, 16, 32} (Inteiro)
1. **KWI**
    * Coluna 8
    * **Descrição:** fator de desenrolamento loop do kernel.
    * **Domínio:** {2, 8} (Inteiro)
1. **VWM e VWN**
    * Colunas 9 a 10
    * **Descrição:** larguras do vetor por matriz para carregamento e armazenamento.
    * **Domínio:** {1, 2, 4, 8} (Inteiro)
1. **STRM e STRN**
    * Colunas 11 a 12
    * **Descrição:** _stride_ habilitado para acesso da memória fora do chip em uma única _thread_.
    * **Domínio:** {0, 1} (Categórico)
1. **SA e SB**
    * Colunas 13 a 14
    * **Descrição:** cache manual por matriz do bloco de grupo de trabalho.
    * **Domínio:** {0, 1} (Categórico)