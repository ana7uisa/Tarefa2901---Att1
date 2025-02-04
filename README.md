🟢 Atividade 1 - Temporizador Periódico para Controle de Semáforo 🚦

🎯 Objetivo

Desenvolver um sistema de semáforo utilizando a função add_repeating_timer_ms() do Pico SDK, com um intervalo de 3 segundos para cada mudança de sinal.

📌 Componentes Necessários

Microcontrolador: Raspberry Pi Pico W

LEDs: Vermelho, Amarelo e Verde

Resistores: 330Ω para cada LED

📋 Requisitos

Início do Ciclo: O semáforo deve iniciar com o LED Vermelho aceso, seguindo para o Amarelo e depois para o Verde, conforme mostrado na Figura 1.

Temporização: O tempo de troca entre os LEDs deve ser de 3 segundos (3.000 ms).

Função de Call-Back: A transição dos LEDs será implementada na função de call-back do temporizador, similar ao exemplo trabalhado na aula com a função repeating_timer_callback().

Saída Serial: A cada segundo (1.000 ms), a rotina principal, dentro do loop while, deve enviar uma mensagem pela porta serial, ficando o conteúdo desta mensagem a critério do estudante.

Experimento com BitDogLab: Utilize a Ferramenta Educacional BitDogLab para testar o código, conectando o LED RGB aos GPIOs 11, 12 e 13 do Raspberry Pi Pico W.

📜 Código-fonte

O código faz uso da função add_repeating_timer_ms() para alternar entre os estados do semáforo. A função de call-back é responsável por realizar a troca de LEDs, enquanto a função principal envia mensagens periódicas via serial.

🔧 Implementação

GPIOs utilizados:

LED Vermelho: GPIO 11

LED Amarelo: GPIO 12

LED Verde: GPIO 13

Bibliotecas empregadas:

pico/stdlib.h para manipulação dos GPIOs e temporizadores

stdio.h para comunicação serial

Mecanismo de Temporização:

A função add_repeating_timer_ms() alterna os LEDs a cada 3 segundos, enquanto a função repeating_timer_callback() gerencia o comportamento do semáforo.

🔍 Testes e Validação

Utilize o BitDogLab para simular o comportamento do semáforo com o LED RGB conectado aos pinos GPIOs 11, 12 e 13, validando a funcionalidade e temporização do sistema.
