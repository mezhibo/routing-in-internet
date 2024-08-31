**Задание 1**

Маршрутизатор А объявляет свою собственную сеть 172.17.1.0 своим одноранговым узлам BGP.

- Какой маршрутной информацией будет обладать маршрутизатор D о доступности сети 172.17.1.0?

- Как будут выглядеть атрибуты AS-path?

- Через какие роутеры пройдет трафик при передаче информации от маршрутизатора D к маршрутизатору А?


![alt text](https://github.com/mezhibo/routing-in-internet/blob/9a6735ef97812f1e91dd639d06cbbf31ebdc254d/IMG/1.jpg)


**Решение 1**

1. В процессе работы протокола BGP роутер D получит информацию о сети 172.17.1.1 через оба пути, AS55000 и AS60000. В маршрутной информации будет указан полный путь до сети - AS-path (а так же другие атрибуты), версия протокола, ID маршрутизатора.

2. AS-path для маршрутизатора D будет включать в себя последовательность номеров автономных систем (AS), через которые прошел каждый маршрут.

3. Если все политики настроены по умолчанию (атрибуты, кроме AS-path, одинаковы), решение о предпочтительном маршруте принимается на основании AS-path. Маршрутизатор D выберет более короткий путь через маршрутизатор E, так как он содержит меньшее количество переходов.


**Задание 2**

Что означает следующий узел 0.0.0.0 в выходных данных команды show ip bgp?



**Решение 2**

Предпочтительный локальный маршрут роутера. В этом случае BGP использует локальный интерфейс для доставки пакетов к указанному маршруту.


**Задание 3. Лабораторная работа "Настройка конфигурации BGP"**

В Cisco Packet Tracer соберите сеть, состоящую из двух маршрутизаторов R1 и R2, находящиеся в разных AS. Настройте между ними BGP.



**Решение 3**


![alt text](https://github.com/mezhibo/routing-in-internet/blob/4a70778173e95b5ae891162bc043cd4c1c6e7c76/IMG/2.jpg)


[PKT](https://github.com/mezhibo/routing-in-internet/blob/4a70778173e95b5ae891162bc043cd4c1c6e7c76/IMG/roiutininternet.pkt)




