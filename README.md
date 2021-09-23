### 10.02_monitoring_systems </br>
#### Обязательные задания: </br>
### 1) Опишите основные плюсы и минусы pull и push систем мониторинга: </br>
#### Pull модель, инициатор передачи - система мониторинга, имеет следующие плюсы: </br>
 - Позволяют гарантировать доставку и корректность данных, благодаря протоколу TCP. </br>
 - Легче контролировать подлинность данных, т.к только из указанных источников производиться загрузка данных </br>
 - Можно настроить единый proxy сервер(балансировщик) до всех агентов с TLS, это сделает независимыми систему мониторинга и агентов </br>
 - Упрощённая отладка получения данных с агентов, т.к для получения используется HTTP и дебажить можно через браузер либо curl </br>
#### Push модель, инициатор передачи - агент, имеет следующие плюсы: </br>
 - Упрощённая система репликации(на агенте можно указать много резервных нод системы мониторинга) </br>
 - Более гибкая настройка отправки пакетов данных, т.к отправку можно настроить индивидуально на каждом агенте </br>
 - Более производительная система т.к UDP легче в передаче пакетов </br>
### 2) Какие из ниже перечисленных систем относятся к push модели, а какие к pull? А может есть гибридные?</br>
- Prometheus - </br>
- TICK - </br>
- Zabbix - </br>
- VictoriaMetrics - </br>
- Nagios - </br>
### 4) Склонировать [рапозиторий](https://github.com/influxdata/sandbox/), запустить TICK-стэк: </br>
Вывод curl http://localhost:8086/ping </br>
Вывод curl http://localhost:8888 </br>
Вывод curl http://localhost:9092/kapacitor/v1/ping </br>
А также скриншот веб-интерфейса ПО chronograf (http://localhost:8888). </br>

