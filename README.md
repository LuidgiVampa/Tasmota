Дисплей 2004 (погода улица, климат в помещение, дата-время)
Данные о погоде с улице приходят по подписке с уличных датчиков 

Subscribe/Unsubscribe (https://tasmota.github.io/docs/MQTT/#subscribeunsubscribe)


Подписаться/Отписаться~
Эта функция не включена в предварительно скомпилированные двоичные файлы.

Чтобы использовать его, вам необходимо скомпилировать сборку . Добавьте следующее в user_config_override.h:

#ifndef SUPPORT_MQTT_EVENT
#define SUPPORT_MQTT_EVENT
#endif

По умолчанию максимальный размер сообщения MQTT, которое может обработать Tasmota, составляет 256 байт. Вы можете увеличить его, переопределив следующую константу в user_config_override.h:
#ifdef RULE_MAX_MQTT_EVENTSZ
#undef RULE_MAX_MQTT_EVENTSZ
#endif
#define RULE_MAX_MQTT_EVENTSZ  512
