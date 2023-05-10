# Acendendo-Lampada-Inteligente
Utilizando Controlador para acender ou desligar a luz de um ambiente com interruptor digital ou  com  palmas.

# Índice
* [  Acendendo Lampada Inteligente ](#Acendendo-Lampada-Inteligente)
* [ Desenvolvedor ](#Desenvolvedor)
* [Resumo ](#Resumo)
* [Objetivos](#Objetivos)
* [Materiais ](#Materiais)
* [Metodologia ](#Metodologia)
* [Link do video-demonstração ](#Link-do-video-demonstração)
* [Link do documento final ](#Link-do-documento-final)
* [Conclusões](#Conclusões)
* [ Referências ](#Referências)

# Desenvolvedor 
Bruno Sousa Silva (brunosilva1405@hotmail.com)

# Resumo:
Em geral, podemos definir que a internet das Coisas (IoT) é o uso dos dispositivos conectados em rede, incorporados no ambiente físico, com o objetivo de melhorar os processos existentes ou criar um cenário inexistente. O IoT se tornou tendência, principalmente para auxiliar em muitos processos rotineiros, e possui efeitos duradouros para a sociedade. Pensando nisso, o presente projeto possui como objetivo demonstrar que através de simples bater de palmas e por um interruptor digital podemos acender, ou apagar as luzes de um ambiente com auxílio de um controlador. Com as luzes apagadas, ao bater uma palma, ou acionar o interruptor digital no modo ON, o modulo sensor de som e o módulo de wifi repassa para o controlador a informação que, por sua vez, verifica a informação, analisa a codificação, e repassa o comando para o modulo relé, que funciona como um interruptor para acende a luz. Caso haja uma segunda palma, em certo intervalo de tempo, ou acionamento do interruptor digital no modo OFF, o módulo sensor de som e o módulo de wifi repassam a informação para o controlador, o qual verifica a informação, analisa a codificação e repassa o comando para o módulo relé, o qual apaga a luz. Com isso, por meio de IoT podemos automatizar uma simples lâmpada, com auxílio de um controlador, acendendo-a, ou, apagando-a, com simples palmas ou com um interruptor digital facilitando a rotina do dia a dia. 

Palavras-chave: Internet das Coisas, MQTT, Luzes, Sensor de som, Objetos inteligentes, Wifi, Arduino.

# Objetivo:
O projeto possui como objetivo demonstrar que através de uma simples palmas ou um interrupot digita poder acender ou apagar as luzes de um ambiente com ajuda de um controlador.

# Materiais:
Para desenvolmento do projeto, foram adquiridos:

  1.Controlador: Foi adquirido um Arduino UNO R3 com as seguintes especificações do controlador: Microcontrolador: ATmega328, Tensão 5V, 7-12V de Tensão de entrada, 14 Pontos digitais, 6 Portas analógicas, 40mA de Corrente pinos I/O, 50mA de Corrente Pinos 3,3V e 16MHz de Velocidade do Clock.
  
![Arduino](https://user-images.githubusercontent.com/78832216/236969416-9158eee7-5089-4701-ab21-f84bf0d5d142.PNG)
 
 2. Cabo USB 2.0 – A/B: Foi adquirido um Cabo USB 2.0 – A/B com as seguintes especificações: 50 cm de comprimento, compatível com Arduino, computadores, impressoras, scanners entre outros aparelhos com entrada USB, Windows, Linux e Mac, e com até 11 Mbps de transferência de dados.

![Cabo USB](https://user-images.githubusercontent.com/78832216/236973656-8985a93f-83bf-40a9-bf30-5caca635bdc5.PNG)

3.Módulo sensor de som KY-037: Foi adquirido um Módulo sensor de som KY-037 com as seguintes especificações: com 3.3-5V DC de tensão de operação (VCC), sensibilidade ajustada via potenciômetro, saída digital (DO)/analógica (AO ), pinagem Terra (GND) e com LED indicador para saída digital.

![Sensor](https://user-images.githubusercontent.com/78832216/236973871-6d1197e3-1503-4a2c-8be4-65e96e2111e6.PNG)

4.  Interruptor eletromecânico (módulo relé): Foi adquirido um Módulo Relé 2 Canais 5V com Optoacoplador com as seguintes especificações: 5VDC (VCC e GND) de Tensão de Operação, 5VCD (IN1 e IN2) de Tensão de sinal, 1520mA de corrente típica de operação, contato do relé permite tensão de até 250VAC a 10A, 510ms de tempo de resposta e com LED de indicador de funcionamento.

![Modulo Rele](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/5d350e92-0726-4424-bc42-d90a3fb5043d)

5.  Protoboard 830 pontos: Foi necessário uma Protoboard 830 pontos com as seguintes especificações: para terminais e condutores de 0,3 a 0,8 mm (20 a 29 AWG), resistência de isolamento de 100MΩ min, tensão máxima de 500v AC por minuto e com 830 furos.

![Protoboard](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/62721284-93fb-46a9-9767-06a67271af56)

6.  Jumper macho/fêmea: Foram adquiridos jumpers macho/fêmea de 10cm.

![Jumper Macho_Femea](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/a86cdd7d-4c49-4777-ae08-504bb3a5265b)

7.  Jumper macho/macho: Foram adquiridos jumpers macho/macho de 10cm.

![Jumper Macho_Macho](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/f3ee7c39-20a4-4b6c-b0f5-28a519f2c342)

8.  Adpatdor para ESP01: Foi adquirido um Adaptador USB para Módulo WiFi ESP8266 ESP-01 com as seguintes especificações: Conexão USB-Serial, Chip Controlador CH340G e tensão 6.3V.

![Adaptador ESP01](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/6dbf0064-df17-4d2e-aa5d-28c7587078d1)

9. Módulo Wifi:Foi adquirido um Módulo WiFi Serial ESP8266 ESP-01 com as seguintes especificações: Padrão 802.11 b/g/n, Wi-Fi Direct (P2P), contém Stack TCP/IP integrado, segurança WPA, WPA2, tensão 3.3V.

![Modulo Wifi](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/2025d9fd-617f-4c33-8a94-ee45f2ff021f)

10.  Plugue macho: Foram adquiridos 2 plugues macho de 2 pinos com as seguintes especificações: 10A até 250V.

![Plugue Macho](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/66003b80-5f01-45c9-ae41-48d7947aa0cd)

11.  Plugue fêmea: Foi adquirido 1 plugue fêmea de 2 pinos com as seguintes especificações: 10A até 250V.

![Plugue Femea](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/a50d731f-2ef5-40fb-85c9-eb48c9f9d645)

12. Cabo flexível: Foi adquirido 8m de cabo flexível com as seguintes especificações: 750V de tensão, 2,5mm² de seção nominal, cor branco e 0,8mm de espessura.

![Cabo flexível](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/b1052da8-0482-44c2-8f7d-89aeddc79ba1)

13. Soquete bocal de lâmpada - Pendente: Foi adquirido um soquete bocal estilo pendente bivolt na cor preta.

![Soquete bocal lampada](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/49c22e4c-8f0a-42c0-a056-d7dfc0548ef7)

14. Lâmpada LED 110V: Foi adquirida uma lâmpada de LED Bulbo 110V, 9W da marca FOXLUX.

![lampada led](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/a9b155aa-9881-43ca-9d9f-5bb991f755ac)

# Metodologia:

#### Etapa 1 - Controlador, Protoboard, Módulo Sensor de Som, Módulo Wifi e Módulo Relé:
Inicialmente, os jumpers foram inseridos no controlador, protoboard, módulo sensor de som e no módulo relé de forma a realizar as funções solicitadas. Protoboard ligado ao controlador pela entrada “GND” e “5V”, sendo que o “GND” foi ligado no polo negativo e a entrada de “5V” foi ligada no polo positivo da protoboard, conforme figura abaixo:
![imagem](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/056c9315-dc90-4298-9159-3b2cbd04f985)

Sensor de som conectado a protoboard, sendo que a entrada “G” do sensor foi ligada ao polo negativo e a entrada “+” do sensor foi ligada ao polo positivo da protoboard.
![imagem2](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/9903fa0c-3ffd-44a9-9aad-6b47fddbfebe)

Sensor de som conectado ao controlador, sendo que a entrada “DO” foi conectada à entrada “7” do controlador.
![imagem3](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/8501d036-aff9-458d-9cb9-1ea7e970b54d)

Módulo Relé conectado ao Protoboard e Controlador, sendo que a entrada “VCC” do módulo relé foi ligada ao polo positivo da protoboard, e a entrada “GND” do módulo relé foi ligada ao negativo da protoboard. Pela entrada “IN2” o módulo relé foi ligado ao controlador pela entrada “4”.
![imagem4](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/cdf603e1-4522-4694-82ee-2733e22634f4)

Módulo Wifi conectado ao controlador, sendo que a entrada “GND” do módulo wifi foi ligada ao “GND” do controlador, a entrada “GPIO2” do módulo wifi foi ligada a entrada “A5” do controlador, a entrada “GPIO0” do módulo wifi foi conectado a entrada do “A4” do controlador, e as entradas “VCC” e “CH_PD” do módulo wifi foi conectado a entrada 3.3V do controlador.
![imagem5](https://github.com/Bruno14058610/Acendendo-Lampada-Inteligente/assets/78832216/e237fa69-4089-4fbd-8a6a-f8a5ba104ff5)













