# Detecção de Heavy Hitters em Network-Wide com Switches Multi-Pipes 

## Descrição

Este repositório contém um emulador para detecção de *Heavy Hitters* em *Network-Wide* com switches *multi-pipes* . O emulador suporta duas abordagens distintas para essa detecção: a abordagem Accumulator (*A*) e a abordagem Local-Pipe (*LP*). Cada abordagem tem sua implementação correspondente no código-fonte, identificada pelas letras *A* e *LP* nos nomes dos programas.

Além disso, ambas as abordagens oferecem duas opções de métodos de detecção: com Limites Adaptáveis e com Limite Fixo.

Ambas as abordagens oferecem opções de detecção adaptáveis, permitindo que o usuário ajuste os seguintes parâmetros:

- **Quantidade de Switches**: O número de switches envolvidos na detecção pode ser especificado pelo usuário.

- **Limite**: O usuário pode definir um limite global para a detecção de *Heavy Hitters*, seja adaptável ou fixo.

- **Fator de Suavização**: A suavização pode ser personalizada com um fator escolhido pelo usuário. O Fator de suavização refere-se a variavel responsavel paelo limite adaptativo.

- **Pipes**: O usuário pode configurar a quantidade de pipes conforme necessário, que seja até 16 pipes.

## Abordagens

- **Abordagem Accumulator (*A*)**: Esta abordagem utiliza um acumulador no switch para controle da contagem e comunicação com o plano de controle.

- **Abordagem Local Pipe (*LP*)**: Esta abordagem comunica individualmente por pipe com o plano de controle.

## Execução
Utilizamos um Trace CAIDA Equinix-NYC, que foi dividido em partes para cada switch, com intuito de simular a distribuição do fluxo de dados em diferentes switches na rede. O trace inteiro se encontra no código "f1Score.py", que realiza a contagem real para obtenção da métrica F1-Score.

Para a execução do código é preciso rodar o "terminalA.py" para o Accumulator ou "terminalLP.py" para o Local-pipe. 
Caso queira alterar o trace, será necessario altera-lo nos switches de rede e no código f1Score.



