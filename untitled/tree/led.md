# Светодиод \(LED\)

Простой светодиод для индикации. Вам нужно отправить 0, чтобы выключить светодиод. И 255 для того, чтобы включить светодиод. Или просто используйте Blynk API, как описано ниже:

```cpp
//регистрируемся на виртуальном пине 1
WidgetLED led1(V1);
led1.off();
led1.on();
```

Все значения от 0 до 255 изменяют яркость светодиода:

```cpp
WidgetLED led2(V2);
//установить яркость светодиода на 50%.
led2.setValue(127);
```

Вы также можете изменить цвет светодиода с помощью кода:

```cpp
//#D3435C - Красный в RGB формате
Blynk.setProperty(V1, "color", "#D3435C");
```

## Светодиод на рабочем столе

Вы можете добавить виджет светодиод на рабочий стол Android. В этом случае светодиод работает через протокол HTTPS. Имейте в виду, что в режиме «Рабочий стол» виджет светодиода имеет некоторые ограничения. Светодиод будет обновлять свое состояние только один раз в 15 минут. Вы можете изменить этот интервал через настройки виджета. Однако интервал обновления менее 15 минут не гарантируется.

**Примечание:** Добавление виджета на рабочий стол стоит 100 энергии. Эта энергия не возвращается при удалении виджета.

**Примечание:** Виджеты рабочего стола для локальных серверов Blynk требуют открыть порт 8080.

**Пример кода:** [Диод](https://github.com/blynkkk/blynk-library/blob/master/examples/Widgets/LED/LED_Blink/LED_Blink.ino)
