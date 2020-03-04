### HW "Архитектура сетей"

При выполнении данного ДЗ у меня получились следующие подсети:

## Сеть "точка-точка" для соединения роутеров:

- 192.168.255.0/30 - interRouter (192.168.255.1) -> centralRouter (192.168.255.2)  
Свободных адерсов нет.  
Broadcast - 192.168.255.3

- 192.168.255.4/30 - centralRouter (192.168.255.5) -> office1Router (192.168.255.6)  
Свободных адерсов нет.  
Broadcast - 192.168.255.7

- 192.168.255.8/30 - centralRouter (192.168.255.9) -> office2Router (192.168.155.10)  
Свободных адерсов нет.  
Broadcast - 192.168.255.11

Свободные подсети:
- 192.168.255.12/30  
Свободных адресов - 2  
Broadcast - 192.168.255.15

- 192.168.255.16/28  
Свободных адресов - 14  
Broadcast - 192.168.255.31

- 192.168.255.32/27  
Свободных адресов - 30  
Broadcast - 192.168.255.63

- 192.168.255.64/26  
Свободных адресов - 62  
Broadcast - 192.168.255.127

- 192.168.255.128/25  
Свободных адресов - 126  
Broadcast - 192.168.255.255

Свободные подсети сделал самые большие, а так можно всю подсеть 192.168.255.0/24 разбить на подсети для соединения типа "точка-точка"

## Сеть Central:

directors:
- 192.168.0.0/28 - centralRouter (192.168.0.1) -> centralServer (192.168.0.2)  
Свободных адресов - 28  
Broadcast - 192.168.0.31

office hardware:
- 192.168.0.32/28  
Свободных адресов - 30  
Broadcast - 192.168.0.63

wifi:
- 192.168.0.64/26  
Свободных адресов - 30  
Broadcast - 192.168.0.127

Свободная подсеть:
- 192.168.0.128/25  
Свободных адресов - 126  
Broadcast - 192.168.0.255

## Сеть Office1

dev:
- 192.168.2.0/26 - office1Router (192.168.2.1) -> office1Server (192.168.2.2)  
Свободных адресов - 60  
Broadcast - 192.168.2.63

test servers:
- 192.168.2.64/26  
Свободных адресов - 62  
Broadcast - 192.168.2.127

managers:
- 192.168.2.128/26  
Свободных адресов - 62  
Broadcast - 192.168.2.191

office hardware:
- 192.168.2.192/26  
Свободных адресов - 62  
Broadcast - 192.168.2.255

## Сеть Office2:

dev:
- 192.168.1.0/25 - office2Router (192.168.1.1) -> office2Server (192.168.1.2)  
Свободных адресов - 124  
Broadcast - 192.168.1.127

test servers:
- 192.168.1.128/26  
Свободных адресов - 62  
Broadcast - 192.168.1.191

office hardware:
- 192.168.1.192/26  
Свободных адресов - 62  
Broadcast - 192.168.1.255

