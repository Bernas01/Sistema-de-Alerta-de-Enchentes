Sistema de Alerta de Enchentes com Arduino 

Descrição do Projeto 

Este projeto utiliza um Arduino Uno com um sensor ultrassônico HC-SR04 para monitorar o nível da água em tempo real. Baseado na distância medida pelo sensor, o sistema aciona LEDs indicadores e um buzzer para emitir alertas visuais e sonoros, classificando o nível de enchente em seguro, atenção ou crítico. 

O objetivo principal é auxiliar na prevenção de desastres naturais, fornecendo um sistema de aviso rápido e eficiente para enchentes. 

 

Componentes Utilizados 

Componente 

Quantidade 

Função 

Arduino Uno 

1 

Controlador principal do sistema 

Sensor Ultrassônico HC-SR04 

1 

Medição da distância até o nível da água 

LEDs Verde, Amarelo e Vermelho 

6 

Indicação visual dos níveis de alerta 

Buzzer 

1 

Alerta sonoro 

Jumpers 

Vários 

Conexão entre os componentes e a protoboard 

Protoboard 

1 

Montagem dos circuitos 

 

Descrição dos Pinos 

Componente 

Pino Arduino 

Função 

Sensor Ultrassônico HC-SR04 (Echo) 

12 

Entrada para o pulso refletido 

Sensor Ultrassônico HC-SR04 (Trig) 

13 

Saída para disparar o pulso 

LED Verde 

2 

Indica nível muito seguro 

LED Amarelo 1 

3 

Indica nível seguro 

LED Amarelo 2 

4 

Indica nível seguro 

LED Vermelho 1 

5 

Indica nível médio 

LED Vermelho 2 

6 

Indica nível alto 

LED Vermelho 3 

7 

Indica nível crítico 

Buzzer 

8 

Emite alerta sonoro 

 

Funcionamento do Sistema 

O sensor ultrassônico HC-SR04 dispara um pulso de alta frequência pelo pino trigger (13). 

O sensor mede o tempo até o eco (pulso refletido) ser recebido no pino echo (12). 

O Arduino calcula a distância até a superfície da água com base no tempo medido. 

Conforme a distância medida, o sistema acende os LEDs correspondentes e ativa o buzzer para alertar níveis de água: 

Distância (cm) 

Ação 

LEDs Acesos 

Buzzer 

< 10 

Nível Crítico (risco iminente) 

Vermelho 1, 2 e 3 

Ligado 

10 - 19 

Nível Alto 

Vermelho 1 e 2 

Ligado 

20 - 29 

Nível Médio 

Vermelho 1 

Ligado 

30 - 199 

Nível Seguro 

Amarelo 1 e 2 

Desligado 

>= 200 

Nível Muito Seguro 

Verde 

Desligado 

 

Código Fonte 

//  
 

 

Como Usar 

Monte o circuito conforme o diagrama. 

Faça o upload do código para o Arduino. 

Abra o monitor serial para visualizar as leituras de distância. 

Observe os LEDs e o buzzer reagindo conforme a variação do nível de água simulada. 

 

Simulação Online 

Você pode testar o projeto no Tinkercad no link abaixo: 
 Simulação Tinkercad - Sistema de Alerta de Enchentes 

Clique em Start Simulation para iniciar e variar a distância no sensor ultrassônico para testar as respostas dos LEDs e do buzzer. 

 

Testes Realizados 

Teste de diferentes níveis de água simulados para validação da ativação correta dos LEDs e buzzer. 

Teste de precisão na medição do sensor ultrassônico. 

Verificação do tempo de resposta do sistema para alertas em tempo real. 

 

Melhorias Futuras 

Integração com módulo GSM para envio de SMS de alerta. 

Registro dos níveis de água para análise histórica. 

Implementação de painel LCD para exibir o nível da água em tempo real. 

Integração com sistema IoT para monitoramento remoto. 
 
