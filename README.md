# Отчёт о тестировании приложения "Precision"

## Краткое описание

В целях проверки работоспособности приложения для внедрения дополнительного бонуса новым клиентам, было проведено тестирование части рабочего кода. В ходе тестирования было обнаружено слабое место программы
, которое не позволяет получить точное итоговое значение бонуса.

## Описание тестов

Было проведено функциональное тестирование, чтобы выяснить складываются ли заданные значения бонусов, и правильно ли программа выводит результат.

## Результаты

1. 70% успешных тестов
2. [Найденный баг](https://github.com/NAleshina/Precision/issues/1)

## Общие рекомендации

Для решения найденного бага можно использовать следующие изменения 

```java
import java.text.DecimalFormat;

public class main {
  public static void main(String[] agrs) {
    double regularBonus = 0.3;
    double specialBonus = 0.6;
    double totalBonus = regularBonus + specialBonus;
    DecimalFormat df = new DecimalFormat (rattern: "#.#");
    System.out.println(df.format(totalBonus));
    }
   }
```
