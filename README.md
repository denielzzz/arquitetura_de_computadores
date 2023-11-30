# MIPS Pipeline
### Trabalho Final de Arquitetura de Computadores
Equipe:
  - Daniel Lins;
  - Juliana Zambon;
  - Matheus Piovesan.

### Desenvolvimento do MIPS Pipeline

Desenvolvimento de um Pipeline MIPS no Logisim Evolution com um programa de teste destinado a calcular o décimo sexto termo da sequência de Fibonacci.<br>
Como parte integrante deste projeto, foi elaborado um programa de teste específico com o propósito de calcular o décimo sexto termo da sequência de Fibonacci, uma série matemática notável, na qual cada termo é a soma dos dois anteriores. O décimo sexto termo da sequência de Fibonacci é particularmente interessante, pois exige uma quantidade substancial de cálculos iterativos, oferecendo assim uma avaliação abrangente da capacidade do pipeline em lidar com operações complexas de maneira eficiente. <br>
<br>
O clock é configurado de maneira invertida, indicando que sua operação ocorre especificamente na borda de descida. 
Os blocos de registradores intermediários, compreendendo as etapas IF/ID, ID/EX, EX/MEM e MEM/WB, desempenham um papel essencial no fluxo ordenado de dados em um processador. Cada um desses blocos armazena os dados por um ciclo de clock. <br>
No  (ID), ocorre a decodificação da instrução, na qual a informação é formatada e distribuída em diversos bits para os campos funct, shamt, RD, imm, RT, RS e opcode - de acordo com o formato da instrução, R, I ou J. <br>
Na unidade de controle (Control), os sinais de controle são distribuídos com base nos valores do OPcode e funct. O OPcode é utilizado exclusivamente quando seu valor é distinto de zero; caso contrário, o funct é utilizado para determinar os sinais de controle pertinentes. Essa lógica de seleção entre OPcode e funct contribui para uma adaptação precisa e eficaz do controle conforme a natureza da instrução em execução. <br>
Contamos com um multiplexador que realiza um flush, transformando a instrução em uma bolha. Em situações como saltos ou load seguido de uso, o multiplexador distribui o valor zero para todos os sinais, indicando que nenhuma operação deve ser executada.
