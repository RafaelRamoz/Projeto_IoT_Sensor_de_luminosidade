Monitoramento Inteligente de Iluminação em Ambientes Industriais

Descrição do Projeto

Este projeto consiste no desenvolvimento de um sistema IoT para monitoramento de iluminação em ambientes industriais que manipulam insumos fotossensíveis. Utilizando um sensor de luz (LDR), um microcontrolador NodeMCU ESP8266 e o protocolo MQTT, o sistema detecta níveis de iluminação em tempo real. Caso a iluminação ultrapasse o limite seguro pré-definido, um buzzer é ativado para alertar os operadores. Os dados são enviados a uma dashboard no Adafruit IO, permitindo visualização e análise.

Objetivo

Garantir a qualidade e segurança na produção de insumos fotossensíveis ao monitorar e controlar a iluminação, prevenindo exposições inadequadas à luz.

Características do Sistema

- Monitoramento em tempo real da intensidade luminosa.
- Geração de alertas automáticos via buzzer em casos de exposição excessiva à luz.
- Armazenamento e visualização dos dados em uma dashboard personalizada no Adafruit IO.
- Comunicação eficiente e leve com o protocolo MQTT.

Componentes Utilizados

Hardware

- Sensor LDR (Light Dependent Resistor): Detecta a intensidade de luz.
- NodeMCU ESP8266: Microcontrolador com Wi-Fi integrado, responsável pela coleta e transmissão dos dados.
- Buzzer Ativo 5V: Emite alertas sonoros.
- Protoboard e Fios Jumper: Para montagem do circuito.
- Resistor 10kΩ: Para o divisor de tensão no sensor LDR.

Software

- IDE do Arduino: Para programar o NodeMCU.
- Adafruit IO: Plataforma para visualização e gerenciamento de dados.
- Bibliotecas:

◦ ESP8266WiFi

◦ PubSubClient

◦ Adafruit\_MQTT

Montagem do Circuito

1. Conecte o LDR a um resistor de 10kΩ em um divisor de tensão.
1. Ligue o divisor de tensão ao pino analógico A0 do NodeMCU.
1. Conecte o buzzer a um pino digital do NodeMCU (ex.: D1).
1. Utilize uma protoboard para montar o circuito de forma modular.

Configuração do Software

1. Configuração do NodeMCU
- Instale a IDE do Arduino e adicione o suporte ao NodeMCU ESP8266.
- Instale as bibliotecas:

◦ PubSubClient

◦ Adafruit MQTT

2\. Configuração do Adafruit IO

1. Crie uma conta no Adafruit IO.
1. Crie um feed para armazenar os dados de iluminação.
1. Configure uma dashboard para visualização dos dados.
1. Código do NodeMCU
- Carregue o código fornecido para o NodeMCU, substituindo as credenciais Wi-Fi e do Adafruit IO:

#include <ESP8266WiFi.h>

#include <Adafruit\_MQTT.h>

#include <Adafruit\_MQTT\_Client.h>

#define NETWORK\_SSID "SEU-WIFI-AQUI"

#define NETWORK\_PASSWORD "SUA-SENHA-AQUI"

#define IO\_SERVER      "io.adafruit.com"

#define IO\_PORT        1883

#define IO\_USERNAME    "SEU-USUARIO-AQUI"

#define IO\_KEY         "SUA-KEY-AQUI"

- Compile e envie o código para o NodeMCU pela IDE do Arduino.

Funcionamento

1. O sensor LDR detecta a intensidade luminosa.
1. O NodeMCU processa os dados e os envia para o Adafruit IO via MQTT.
1. Se o nível de luz ultrapassar o limite seguro, o buzzer emite um alerta sonoro.
1. Os dados podem ser visualizados em tempo real na dashboard do Adafruit IO.

Aplicações

- Fábricas que produzem insumos fotossensíveis, como filmes e produtos químicos.
- Monitoramento de iluminação em ambientes controlados, como laboratórios.
