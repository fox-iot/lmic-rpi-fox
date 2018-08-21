# Biblioteca para Shield LoRaWAN Raspberry Pi (desenvolvido por [Fox IoT](http://foxiot.com.br/))

Essa biblioteca proporciona interface entre hardware e software, composta por um chip LoRa [RFM95](http://www.hoperf.com/upload/rf/RFM95_96_97_98W.pdf)
operando na frequência de 915 MHz e três LEDs indicadores, sendo um de cor verde que indica power on e dois vermelhos de uso geral podendo ser configurados
para indicar algum tipo de status do sistema.

Obs.: A construção dessa biblioteca teve como base a [lmic_pi](https://github.com/dragino/lmic_pi) com algumas adaptação para ser
compatível com a rede LoRaWAN da [Universidade Federal de Santa Maria](https://www.ufsm.br/).

## Pimeiros passos antes de fazer o download da biblioteca

- Formatar o cartão SD com [SD Memory Card Formatter](https://www.sdcard.org/downloads/formatter_4/) 
- Instalar o sistema operacional Raspbian na Raspberrypi, que pode ser instalado via [NOOBS](https://www.raspberrypi.org/downloads/noobs/)
- Habilidar a interface SPI em preferences => Raspberrry pi configuration => interfaces 

## Instalação da biblioca WiringPi

A biblioteca [WiringPi](http://wiringpi.com/) proporciona a interface dos GPIO do Raspberry Pi

- Instale o git (Se não tiver instalado)

  $ sudo apt-get install git-core

- Faça o clone do repositório

  $ git clone git://git.drogon.net/wiringPi

- Acesse a pasta wiringPi 

  $ cd wiringPi

- Faça o build da lib

  $ ./build

## Instalação da biblioca [lmic-rpi-fox](https://github.com/lucasmaziero/lmic-rpi-fox.git)

- Faça o clone do repositório

  $ git clone https://github.com/lucasmaziero/lmic-rpi-fox.git

- Acesse a pasta lmic-rpi-fox

  $ cd lmic-rpi-fox/examples/ttn-abp-send

- Faça o make do projeto (lembrando que qualquer mudança feita no código posteriormente deve ser execudado o comando "make")

  $ make

- Executando o programa

  $ ./ttn-abp-send

## Mapeamento de hardware

O mapeamento completo de pinos da WiringPi pode ser visto [aqui](https://github.com/lucasmaziero/lmic-rpi-fox/blob/master/Raspberry%20Pi%20GPIO%20Pins.png)

WiringPi 0 == Reset
  
WiringPi 4 == DIO0

WiringPi 5 == DIO1

WiringPi 1 == DIO2 (Não utilizado)
  
WiringPi 12 == MOSI
  
WiringPi 13 == MISO
  
WiringPi 14 == SCK

WiringPi 2 == LED1

WiringPi 3 == LED2
  
GND  == GND
  
3.3V  == +3.3V  

## Licença

O conteúdo está licenciado sob a licença MIT. Veja [License File](LICENSE) para mais informações.
