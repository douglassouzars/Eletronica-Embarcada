<H1>BOLA NO TUBO</H1>

Este projeto, desenvolvido para a disciplina de Eletrônica Embarcada, consiste em um desenvolvimento de firmware para controlar a posição vertical de uma bola por meio de um fluxo de ar gerado através de uma ventoinha controlada pela abertura ou fechamento de uma válvula acoplada a um motor de passo.

Serão utilizados um sensor óptico refletivo para detecção da abertura total da válvula, um sensor ultrassonico para medição da altura da bola e um sensor de temperatura para compensação da medição da altura da bola. A transmissão e recepção de dados será realizada utilizando uma interface bluetooth que possibilitará a comunicação entre o sistema e o usuário (via celular ou computador).

O firmware desenvolvido será implementado em um microcontrolador PIC16F1827/I-P e utilizadas as ferramentas SNAP, que permite programar e debuggar o código desenvolvido, da Microchip, e um Analisador Lógico de 8 canais para visualização e aferição dos sinais digitais. O diagrama de blocos do projeto está apresentado conforme a Figura 1:

<div align="center">
  
  <img src="https://github.com/fernandarmuro/wingardium-levibola/blob/be5bb0134b2ad3a82d7c9f4d4b3726b2a49a7895/Diagrama_de_blocos.png" alt="Diagrama da FSM do Bola no Tubo" width="600"/> 
  
  <em>Figura 1: Diagrama de blocos do projeto bola no tubo.</em>
  
</div>



O projeto será dividido em 4 módulos, os quais o desenvolvimento, teste e simulação do código será de responsabilidade individual à cada integrante do grupo. Ao final, cada parte desenvolvida será integrada e testada em um protótipo físico disponibilizado para validadação e verificação do funcionamento do firmware.

O projeto e as atividades de cada integrante seguem a seguinte divisão:

1. Douglas Rodrigues:
   
   - Medição da altura da bola e temperatura.
     
3. Fernanda Muro:
   
   - Comunicação bluetooth.
   
5. Matheus Neves:

   - Controle dos atuadores (ventoinha e válvula).
   
7. Pedro Barros:

   - Algoritmo de controle PID.

O detalhamento de cada módulo desenvolvido no projeto, assim como os arquivos mcc.c e mcc.h de cada um, estão disponíveis nas pastas nominais de cada integrante.
=======
Este projeto consiste em um sistema de aquisição de dados e controle da altura de uma bola
que flutua dentro de um tubo vertical pela ação de um fluxo de ar. O fluxo de ar é gerado por uma
ventoinha e pode ser controlado mudando o ciclo útil do sinal de alimentação da ventoinha ou pela
abertura ou fechamento de uma válvula acoplada a um motor de passo.

Um sensor óptico refletivo (TCRT-5000) detecta abertura total da válvula, permitindo inicializar sua
posição. Este sensor entrega um valor analógico de tensão, sendo mínimo quando o sinal luminoso
não reflete na válvula, indicando que está totalmente aberta. Em qualquer outra posição, onde o
sensor estiver tampado pela válvula e o sinal seja refletido, o valor de tensão será máximo por
conta da queda de tensão no resistor R3 e da condução do optotransitor que o sensor possui na
sua saída.

Outro sensor (HC-SR04) possibilita medir a altura da bola, emitindo um sinal de ultrassom que
impacta contra a bola e retorna para o sensor. O tempo de voo do sinal permite calcular a distância
entre o sensor e a bola. Mas, a velocidade do som muda com a temperatura e por isso se utiliza
um sensor de temperatura (LM35) para compensar a medição de altura.

Uma interface Bluetooth permite o envio e recepção de dados entre o sistema e um celular ou um
computador. Um microcontrolador PIC16F1827/I-P, alimentado com 5V, controla todo o sistema.
O sistema também possui um programador SNAP da Microchip e um Analisador Lógico de 8 canais,
que permitem programar e debuggar o firmware e visualizar os sinais digitais envolvidos.

O projeto foi realizado por 4 alunos do curso de engenharia eletronica, dividido nas respectivas pasta com os nomes e tendo como as devidas atividades desenvolvidas:
<ul>
  <li>DOUGLAS: Medição de altura da bola</li>
  <li>FERNANDA: Comunicação serial-BT</li>
  <li>MATHEUS: Movimento do motor de passo e detecção do fim de curso</li>
  <li>PEDRO: Controle PI ou PID</li>
</ul>
Objetivo final conforme a imagem:<img width="875" height="740" alt="image" src="https://github.com/user-attachments/assets/14256940-2174-4fa8-963d-095cd81767e7" />
