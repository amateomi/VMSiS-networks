## 1. Понятие системного администрирования

Системное администрирование решает задачи связанные с созданием и поддержанием
работоспособности информационных систем, состоящих из аппаратных и программных средств.

Сетевое администрирование неотделимо от администрирования. Им занимается системный
администратор.

Стратегии администрирования:
- Распределенное (нет единого центра регламентирующего политику администрирования)
- Централизованное (есть единый центр регламентирующий политику администрирования)

## 2. Выбор программного обеспечения администратором

Классификация ПО:
- Системное (напрямую взаимодействует с ОС для решения низкоуровневых задач) (непосредственно ОС и её компоненты, утилиты, субд)
- Прикладное (решает прикладные задачи пользователей) (веб-сайты, офисы)
- Инструментальное (способствует разработке и тестированию другого ПО)
- Встраиваемое (управляет устройством) (firmware)

По отношению к ОС ПО делят на:
- Native (от того же разработчика)
- Third party (от других разработчиков)

Критерии выбора:
- Степень соответствия требованиям
- Стоимость (приобретения, освоения, использования)
- Доступность (сложность приобретения и освоения)
- Эргономичность (сложность использования)
- Качество технической поддержки

## 3. Установка программного обеспечения администратором

Способы установки ПО:
- Ручное копирование исполняемых и вспомогательных файлов
- Ручная проверка зависимостей и сборка приложения из исходного кода
- Через пакетный менеджер (активно используется в Linux)
- Через установщик (активно используется в Windows)

Классификация сборок ПО:
- Development/pre-alpha/nightly (текущая)
- Alpha
- Beta
- Release candidate (прошла несколько этапов тестирования и рассматривается как возможный релиз)
- Release to manufacturing (промежуточный либо окончательный релиз)
- Final (окончательный релиз, после которого разработка считается завершенной)

## 4. Сопровождение программного обеспечения администратором

Сопровождение ПО - это одна из фаз жизненного цикла программного обеспечения,
следующая за фазой передачи ПО в эксплуатацию. В ходе сопровождения в программу
вносятся изменения с целью повысить удобство использования и применимость ПО.

С точки зрения системного администратора сопровождение ПО заключается в его обновлении
и устранении неисправностей.

Стратегии устранения неисправностей:
- Сверху вниз (начинать с прикладного уровня и спускаться вплоть до физического)
- Снизу вверх (начинать с физического уровня и подниматься на прикладной)
- Разделяй и властвуй (начинать с наиболее вероятного уровня и продолжать искать в двух направлениях)

## 5. Маршрутизаторы Cisco как специализированное сетевое оборудование

Категории маршрутизаторов Cisco:
- Branch
- WAN aggregation
- Service provider
- Industrial
- Virtual
- Small business

В сегментах small-to-medium businesses (SMB) и small office/small home (SOHO),
преобладают маршрутизаторы серий Integrated Services Routers (ISR). В
частности, их же принято использовать при обучении, на них ориентируется
программа CCNA.

Многие серии представляют собой гибриды с коммутаторами (Nexus).

## 6. Модули маршрутизаторов Cisco

Маршрутизаторы Cisco разрабатывают модульными, с возможностью установить
различные модули на специальное шасси.

Выделяют 5 групп модулей:
- Интерфейсные карты (WIC - WAN Interface Network, HWIC - High-speed WIC, EHWIC - Enhanced HWIC)
- Интерфейсные модули (NIM - Network Interface Module, NM - Network Module, NMD - NM Double-wide, NME - NM Enhanced)
- Внутренние модули (AIM - Advanced Integration Module, ISM - Internal Services Module)
- DSP-сопроцессоры
- Порт-адаптеры и другие модули для высокопроизводительных платформ

В названии модуля отражено его наполнение (HWIC-2FE добавляет 2 интерфейса Fast Ethernet).

## 7. Учебные маршрутизаторы Cisco

Для первоначального обучения администрированию маршрутизаторов Cisco
используются младшие модели ISR для сегмента SMB и старшие для сегмента SOHO.

Применительно к ISR - 1841, 2811, у ISR G2 - 1941, 2901, ISR 4K - 4331, 4221

Сетевое устройство можно рассматривать в 3 плоскостях:
1. Management (весь инструментарий для управления и отладки маршрутизатора, например, SSH)
2. Data (все необходимое для пересылки трафика, например, таблицу маршрутизации)
3. Control (служебная надстройка над данными, используется для коммуникации с другими сетевыми устройствами, например, OSPF)

Могут выделяться и другие плоскости. Плоскости могут быть разделены не только
программно, но и аппаратно (отдельные ядра или процессоры).

## 8. Структура маршрутизаторов Cisco

Структура маршрутизатора:
- Процессор
- Память
- Устройства ввода-вывода

В большинстве случаев используют процессоры на базе RISC архитектур, в
особенности MIPS. В более производительных маршрутизаторах применяются
ASIC (Application-specific integrated circuit).

Подсистемы памяти:
1. BootROM (ПЗУ хранящее загрузчик ROMMON)
2. NV-RAM (энергонезависимое ОЗУ для хранения конфигурации)
3. Flash (ПЗУ для хранения образов IOS, может хранить пользовательские файлы)
4. DRAM (обычное ОЗУ хранящее запущенную IOS и все необходимые для неё данные)

Устройства ввода-вывода в первую очередь реализуют сетевые интерфейсы.
Поддерживается подключение различных flash-устройств.

## 9. Cisco IOS как встраиваемая операционная система

Cisco Internetwork Operating System относится к специализированным
встраиваемым ОС. Главной задачей IOS является предоставление возможностей
конфигурирования маршрутизаторов и коммутаторов Cisco.

Линейки IOS:
- IOS XE
- IOS XR
- NX-OS

На сегодняшний день IOS XE является основной ОС, базируется на ядре Linux.

Средства для взаимодействия с IOS:
- CLI
- Веб-интерфейс
- ПО для устройств с DNA (Digital Network Architecture)

Для работы с CLI необходимо осуществить физическое подключение консоли 
через RS-232, более новые модели маршрутизаторов поддерживают подключение
по USB.

До недавнего времени CLI был основным способом конфигурирования IOS, однако
в последние годы активно продвигается централизованное конфигурирование
на базе DNA по средствам веб-интерфейса.

## 10. Загрузка IOS

Загрузка состоит из следующих этапов:
1. bootstrap выполняет POST (Power-On Self-Test) и инициализирует аппаратные структуры и подсистемы, а также программные структуры загрузочной среды, например, переменные окружения
2. bootstrap ищет образ IOS по специальной строке в конфигурации либо по значению переменной BOOT. Если не нашел, то поиск продолжается в подсистеме Flash памяти, выбирая первый попавшийся. Если образов не найдено, то запускается интерпретатор командной строки ROMMON, позволяющий скопировать образ в Flash.
3. Образ IOS загружается в DRAM и инициализирует все необходимые программные и аппаратные структуры
4. Если загрузочная конфигурация отсутствует, то будет выведено предложение о начале конфигурационного диалога, в случае отказа будет выбрана конфигурация по умолчанию. В конце выведется сообщение, предлагающее начать работу, при согласии произойдет копирование загрузочной конфигурации либо ранее настроенной в рабочую конфигурацию. Появится приглашение командной строки (prompt)

## 11. Режимы IOS

Основные режимы IOS:
1. Пользовательский исполнительский (просмотр состояния системы и проверка связи)\
   Приглашение: `Device>`
2. Привилегированный исполнительский (просмотр конфигурации, работа с файлами, перезагрузка)\
   Приглашение: `Device#`\
   Для перехода: `Device> enable`
3. Глобальный конфигурационный (конфигурирование устройства в целом)\
   Приглашение: `Device(config)#`\
   Для перехода: `Device# configure terminal`
4. Конфигурирования интерфейса (конфигурирование отдельного интерфейса)\
   Приглашение: `Device(config-if)#`\
   Для перехода: `Device(config)# interface <какой-либо интерфейс>`
5. Конфигурирования линии (конфигурирование отдельной линии)\
   Приглашение: `Device(config-line)#`\
   Для перехода: `Device(config)# line <какая-либо линия>`
6. ПЗУ-монитор (диагностика и восстановление)\
   Переход осуществляется прерыванием загрузки IOS

## 12. Система команд IOS и ее особенности

Большинство команд требуют наличия аргументов. Почти всегда IOS не различает
строчные и прописные буквы при вводе команд (исключение, например, пароли).

У каждого режима свои команды. Из режимов конфигурирования можно выполнить
команды исполнительских режимов путем добавления `do` в начале.

С помощью команды `?` можно запросить список доступных команд либо варианты
подстановки аргументов в уже начатой команде. Часть команд скрыта (нерекомендуемые).

Некоторые команды можно инвертировать используя префикс `no`, например,
убрать ip адрес с интерфейса можно добавив `no` в начале той команды,
которая этот ip адрес установила.

CLI IOS поддерживает сокращение команд по названию, например, вместо
`configure terminal` можно написать `conf t`.

## 13. Файлы конфигурации и файловая система IOS

В Cisco IOS можно выделить два файла конфигурации:
- running-config (содержит текущую конфигурацию запущенного устройства)
- startup-config (содержит конфигурацию применяемую при запуске устройства в качестве running-config)

Файлы конфигурации состоят из секций, состоящих по большей части из команд.
Если строка в конфигурации начинается с `!`, то эта строка игнорируется
IOS (можно использовать для комментариев).

В IOS используется специальная файловая система IFS (IOS File System). В её
основе лежит FAT16 (обычная IOS) и ext2 (IOS XE). IFS включает 3 подсистемы:
- network file systems
- special file systems
- storage file systems

Для обращения к локальным или удаленным файловым ресурсам используют
специальные префиксы. Рабочим каталогом по умолчанию является `flash:`.

Основные команды для работы с файлами:
- cd (сменить каталог)
- pwd (вывести на экран название текущего каталога)
- more (вывести на экран содержимое файла)
- dir (вывести на экран содержимое текущего каталога)
- copy (скопировать файл либо каталог)
- rename (переименовать файл либо каталог)
- delete (удалить файл)
- rmdir (удалить каталог)
- mkdir (создать каталог)
- erase (удалить все файлы и каталоги из файловой системы)
- format (отформатировать файловую систему)

## 14. Основные команды IOS для базовой настройки маршрутизатора и просмотра его состояния

К базовой настройке маршрутизатора можно отнести задание правильного времени,
названия хоста и пароля.

Для работы со временем используются команды `clock` и `calendar` в 
привилегированном режиме. Команда `clock` взаимодействует с программными
часами, а `calendar` - с аппаратными. Предпочтительней использовать
программные часы, они более точны, могут обновлять свое состояние по
протоколу NTP.

Название хоста можно изменить командой `hostname` в режиме конфигурации.
По умолчанию маршрутизаторы Cisco именуются Router.

Настройка пароля осуществляется с помощью команды `enable secret <пароль>`
в режиме конфигурации.

Просмотр состояния различных подсистем IOS осуществляется с помощью команды
`show` с различными аргументами:
- running-config/startup-config (соответствующая конфигурация)
- interfaces (подробное состояние всех сетевых интерфейсов, или некоторого конкретного, если передан соответсвующий аргумент)
- line (подробное состояние всех линий, или некоторой конкретной, если передан соответсвующий аргумент)
- version (общая информация об IOS и маршрутизаторе)
- processes (подробная информация об процессах)

## 15. Сетевые интерфейсы в IOS

Cisco разделяет конфигурируемые сетевые интерфейсы на L2 и L3.

На гибридных маршрутизаторах имеется возможность преобразовать L2 и L3
интерфейсы друг в друга с помощью команд `switchport` и `no switchport`.

Сетевые интерфейсы коммутаторов по умолчанию L2 и административно включены,
а маршрутизаторов - L3 и административно выключены.

Cisco Loopback - программный L3-интерфейс использующийся для отладки.

Cisco Null - программный L3-интерфейс использующийся для устранения
маршрутизационных циклов. Не принимает и не передает пакеты.

Именование сетевых интерфейсов:
- маршрутизаторы: type slot/subslot/port
- коммутаторы: type switch/slot/port

Основные типы: Ethernet, FastEthernet, GigabitEthernet, TenGigabitEthernet,
Serial.

Сетевые интерфейсы, предназначенные для подключения терминалов, Cisco
называет линиями (lines).

## 16. Сетевые интерфейсы и подсети

Логически Internet состоит из множества подсетей.

Подсеть (subnet) - адресное пространство, в котором имеется некоторое
количество устройств. Минимально подсеть соответствует сегменту.

Критерии объединения станций в подсети:
- Расположение
- Назначение
- Принадлежность

Типы станций:
- пользовательские (за ними работают обычные пользователи сети)
- шлюзы (объединяют подсети)

Сетевой интерфейс - минимально адресуемый компонент в сети передачи данных,
входящий в состав станции. Станция может содержать несколько сетевых
интерфейсов (обычно пользовательская содержит один, а шлюзовая - минимум два).
Обычно сетевой интерфейс имеет только один физический порт. Каждый сетевой
интерфейс имеет свой IP-адрес (не все IP-адреса разрешены).

## 17. Классы IPv4-адресов

Выделяют 5 классов IP-адресов: A, B, C являются основными, классы D и E -
дополнительными. Класс D используется для адресации мультикаст-групп. Класс E
зарезервирован для будущего использования.

Любой IP-адрес состоит из подсетевой (subnet) и станционной (node) частей.

*S - Subnet, N - Node*

### A:
Первый байт: 0xxx_xxxx\
Формат адреса: S.N.N.N
### B:
Первый байт: 10xx_xxxx\
Формат адреса: S.S.N.N
### C:
Первый байт: 110x_xxxx\
Формат адреса: S.S.S.N
### D:
Первый байт: 1110_xxxx
### E:
Первый байт: 1111_0xxx

## 18. Явные IPv4-параметры сетевого интерфейса

Явные IP-параметры сетевого интерфейса:
- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

### IP Address
Служит для адресации станции посредством соответствующего сетевого интерфейса.
Уникальный в пределах подсети.

### Subnet Mask
Предназначена для определения адреса подсети и её размера исходя из IP-адреса.

В двоичном виде представляет собой непрерывную последовательность единиц и
следующую за ней непрерывную последовательность нулей. Единицы соответствуют
подсетевой части, а нули - стационарной.

Пример маски класса C: `255.255.255.0`. В нотации CIDR (Classless Inter-Domain
Routing) эта маска будет выглядеть так: `/24`.

### Default Gateway
Шлюз по умолчанию - адрес сетевого интерфейса из текущей подсети, на который
будут направляться пакеты направленные в другие подсети в том случае, когда
остальные маршруты не подошли.

Принято в качестве шлюза по умолчанию назначать адрес первого сетевого
интерфейса в подсети. Принято в пределах подсети использовать только один
шлюз по умолчанию.

### DNS Server
Адрес DNS-сервера необходим для обращения к службе DNS, позволяющей
восстановить цифровое значение адреса станции-абонента исходя из символьного.

## 19. Неявные IPv4-параметры сетевого интерфейса

Определение явных IP-параметров подразумевает задание ещё двух неявных:
- Subnet Address
- Broadcast Address

### Subnet Address
Используется для поочередной адресации всех возможных станций подсети.
Адрес подсети всегда самый нижний адрес подсети из из диапазона адресов
подсети.

### Broadcast Address
Широковещательный адрес используется для одновременной адресации всех
возможных станций подсети. Широковещательный адрес всегда самый верхний адрес
из диапазона адресов подсети.

Пример: устройство с IP-адресом `192.168.0.13/24`:
- Subnet Address `192.168.0.0`
- Broadcast Address `192.168.0.255`

Таким образом в каждой подсети всегда два адреса зарезервировано, а значит
маску 255.255.255.254 практического смысла использовать не имеет.

## 20. Классификация IPv4-адресов

По видимости:
- Публичные
- Приватные (видны только во внутренней сети предприятия или организации)

Для внутренних подсетей зарезервированы следующие диапазоны адресов:
- A: 10.x.x.x
- B: 172.16.0.0 - 172.31.255.255
- C: 192.168.x.x

По временному постоянству:
- Статические (устанавливается администратором вручную)
- Динамические (присваивается станции в процессе загрузки на время сеанса работы).

Динамический адрес может назначаться по определенному протоколу (например,
DHCP), а может случайно генерироваться (адреса Link Local 169.254.x.x).

0.0.0.0 - адрес всей глобальной сети Internet (имеет другие значения в
зависимости от контекста).

255.255.255.255 - глобальный широковещательный адрес (однако на сегодняшний
день шлюзы его подавляют).

127.0.0.1 - адрес интерфейса-заглушки. Пакеты с такими адресами назначения
передаются на прикладной уровень этой же станции.
