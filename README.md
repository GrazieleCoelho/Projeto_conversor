# Projeto 10: **ontrole de LEDs e Exibição Gráfica com ADC no RP2040**
**EMBARCATECH - UNIDADE 04**

## Desenvolvedora
**Aluna Graziele Coelho de Alencar**

## Links: 
- Execução na BitDogLab:
https://youtube.com/shorts/iiRAP6QkqZM

## Descrição
Este projeto tem como objetivo consolidar o uso de Conversores Analógico-Digitais (ADC) no microcontrolador RP2040 e explorar funcionalidades como PWM, exibição gráfica em display SSD1306 e interrupções. A implementação é realizada na placa BitDogLab.

## Objetivos

- Compreender o funcionamento do ADC no RP2040.

- Utilizar PWM para controlar a intensidade de dois LEDs RGB com base nos valores do joystick.

- Exibir a posição do joystick no display SSD1306 por meio de um quadrado móvel.

- Aplicar o protocolo de comunicação I2C para integração com o display.

- Implementar interrupções (IRQ) e debouncing via software para manipulação de botões.



## Componentes e Configuração dos Pinos

- LED RGB conectado ás GPIO 11, 12 e 13
- Joystick conectado ás GPIO 26 (eixo X), GPIO 27 (eixo Y) e GPIO 22 (botão do Joystick)
- Botão A conectado á GPIO 5
- Display SSD1306 conectada ás GPIO 14 (SDA) e GPIO 15 (SCL)

## Funcionalidades Implementadas

**Controle dos LEDs RGB via Joystick**

- O LED Azul varia de intensidade com o eixo Y do joystick.
- O LED Vermelho varia de intensidade com o eixo X.
- Quando o joystick está solto (2048), os LEDs estão apagados.
- Nos extremos (0 e 4095), os LEDs atingem a intensidade máxima.
- O controle é feito via PWM para permitir transições suaves.

**Exibição Gráfica no Display SSD1306**

- Um quadrado de 8x8 pixels é desenhado no display.
- A posição do quadrado é atualizada de acordo com os valores do joystick.

**Controle via Botões**

- Botão do Joystick (GPIO 22):

Alterna o estado do LED Verde.

Modifica a borda do display ao ser pressionado.

- Botão A (GPIO 5):

Ativa ou desativa os LEDs RGB controlados por PWM.

## Como Copiar o Repositório do GitHub

Para baixar e executar o projeto no seu computador, siga os passos abaixo:

- Abra o seu terminal de comando.

- Navegue até o diretório onde deseja clonar o repositório:

*cd /caminho/do/diretorio/*

- Clone o repositório do GitHub usando o seguinte comando:

*git clone https://github.com/GrazieleCoelho/Projeto_conversor.git*

- Acesse o diretório do projeto:

*cd seu-repositorio*

- Compile e execute o código.
