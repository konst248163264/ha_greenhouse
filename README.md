# ha_greenhouse

Конфигурация для Home Assistant, автоматизирующая работу теплицы.

## Использованные характеристики

- Home Assistant Core 2022.6.6 (гггг.мм.релиз_по_счету_в_месяце)
- Home Assistant Operating System 7.6 (28 марта 2022)

## Параметры машины

- Виртуальная машина VirtualBox (.vdi)
- 2GB RAM
- 32GB Storage
- 2vCPU

(взяты из минимальных рекомендованных параметров из документации по установке на 28.06.2022 https://www.home-assistant.io/installation/windows)

## Другие варианты машины

- Raspberry Pi 4 (3 тоже подойдёт) https://www.home-assistant.io/installation/raspberrypi
    - Micro SD Card 32+ GB (рекомендуется Application Class 2)
    - SD Card reader
    - Ethernet cable (рекомендуется, но можно и WiFi)
- Другие варианты https://www.home-assistant.io/installation/

## Установка

### Windows:
1) Скачать образ вирутальной машины https://github.com/home-assistant/operating-system/releases/download/8.2/haos_ova-8.2.vdi.zip
2) Создать новую виртуальную машину
3) Выбрать тип “Linux” и версию “Linux 2.6 / 3.x / 4.x (64-bit)”
4) Выберите “Use an existing virtual hard disk file”, выберите разархивированный файл VDI сверху.
5) Выберите “Settings” виртуальной машины и идите в раздел “System” затем “Motherboard” и выберите “Enable EFI”
6) Далее “Network” “Adapter 1” выберите “Bridged Adapter” и там ваш сетевой адаптер.
7) Потом “Audio” и выберите “Intel HD Audio” в качестве аудио адаптера.

### Raspberry Pi
1) Установить на накопитель снимок системы, например, при помощи [Balena Etcher](https://www.balena.io/etcher).
2) Вставить накопитель в микроконтроллер.

### Общее продолжение
1) Пройти процесс регистрации пользователя.
2) Нажать на иконку пользователя внизу боковой панели слева. В открывшемся окне включить Advanced Mode.
3) Перейти во вкладку Settings -> Add-ons -> Add-on Store.
4) Найти и установить Terminal & SSH.
5) Открыть Terminal & SSH, прописать команды:
    - git init
    - git remote add origin URL/TO/REPO
    - git fetch
    - git checkout -t origin/master
6) Вкладка Developer Tools -> Configuration validation -> Restart
