# ModBus_TCP_RTU_Proxy
Proxy ModBus TCP to ModBus RTU
Программа преобразует протокол ModBus TCP в ModBust RTU

В программе реализован асинхронный сокет сервер.
Когда от клиента поступает запрос по протоколу ModBus программа добавляет клиента в список обрабатываемых клиентов. С этого момента все команды приходящие от этого клиента будут транслироваться на com порт номер которого указан в stationId пакета.
Так как устройства с которыми работает данная программа не поддерживали массив адресов modbus больше чем 10 штук. Пакеты делятся на блоки по 10 адресов.
Алгоритм работы программы подробно описан в комментариях в основной части программы в файле Form1.cs