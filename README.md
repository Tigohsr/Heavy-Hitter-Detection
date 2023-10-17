# Detecção de Heavy Hitters em Switches Multi-Pipes

## Descrição

Este repositório contém um emulador para detecção de *Heavy Hitters* em switches multi-pipes. O emulador suporta duas abordagens distintas para essa detecção: a abordagem Accumulator (*A*) e a abordagem Local Pipe (*LP*). Cada abordagem tem sua implementação correspondente no código-fonte, identificada pelas letras *A* e *L* nos nomes dos programas.

Além disso, ambas as abordagens oferecem duas opções de métodos de detecção: com Limites Adaptáveis e com Limite Fixo.

Ambas as abordagens oferecem opções de detecção altamente adaptáveis, permitindo que o usuário ajuste os seguintes parâmetros:

- **Quantidade de Switches**: O número de switches envolvidos na detecção pode ser especificado pelo usuário.

- **Limite**: O usuário pode definir um limite para a detecção de *Heavy Hitters*, seja adaptável ou fixo.

- **Fator de Suavização**: A suavização pode ser personalizada com um fator escolhido pelo usuário.

- **Pipes**: O usuário pode configurar a quantidade de pipes conforme necessário, que seja até 16 pipes.

## Abordagens

- **Abordagem Accumulator (*A*)**: Esta abordagem utiliza um acumulador no switch para controle da contagem e comunicação com o plano de controle.

- **Abordagem Local Pipe (*LP*)**: Esta abordagem, por sua vez, comunica individualmente por pipe com o plano de controle. 
