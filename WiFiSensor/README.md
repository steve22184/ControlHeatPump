# WiFi Sensor
ВНИМАНИЕ! Если прошивка не компилится то необходимо заменить буквенное обозначение выводов D2 на просто цифры 2. (причину пока не выяснили, что то с SDK)
В этой директории лежит все что касается WiFi Sensor. Это не обязательное оборудование! <br>
<img src="https://github.com/pav2000/ControlHeatPump/blob/master/WiFiSensor/Screen/01.jpg"/><br>
Автор данного устройства Sheeny.

Удаленное (связь по WiFi) устройство с двумя удаленными датчиками температуры, экраном и web интерфейсом для настроек.
Устройство реализовано на ESP8266. В качестве датчиков используются ds18b20. Экран - OLED 0.96 128x64 по протоколу i2C.

Что умеет устройство:
 - передавать данные с двух датчиков температуры на Народный контроллер
 - выводить данные температуры на экран и web страничку
 - получать параметры от Народного контроллера и выводить их на экран и web страничку
 - сигнализировать экраном об ошибке, возникшей на ТН <br>

Для передачи и получения данных устройство подключается по WIFI к домашней сети.<br>
Если подключиться не удалось, либо "прошитая" сеть не доступна, устройство подымает собственную точку WIFI, подключившись к которой (адрес точки 192.168.4.1) возможно настроить подключение к домашней сети WIFI, либо проверить настройки.
WEB интерфейс позволяет задавать статичный IP для устройства, сканировать эфир на наличие сетей, настраивать параметры подключения к выбранной сети, настраивать параметры собственной точки доступа.
Так же есть возможность настроить параметры подключения к Народному контроллеру.
Можно использовать как 2 датчика температуры вместе, так и один из них. Интервал отправки данных на контроллер так же настраивается.

На экран выводиться следующая информация: <br>
1. Режим работы теплового насоса, которым управляет Народный контроллер
2. Данные с датчика/датчиков температуры
3. Сообщение об отсутствии датчиков температуры. В этом случаи выводится значения TIN и TOUT, полученные с контроллера.
4. Наличие/отсутствие подключения к WIFI и IP адрес, по которому доступен WEB интерфейс устройства.
5. Сигнализация, в случае возникновения ошибки в работе ТН.





