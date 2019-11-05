## Questions_list_ND_V2

Необходимо реализовать следующий алгоритм 

Вывести последовательно 2 вопроса (см. ниже).

Первый вопрос всегда один и тот же (вопрос 1), второй – либо (вопрос 2), либо (вопрос 3) в произвольном порядке.

При выборе определённого ответа меняются характеристики (есть в описании варианта ответа), после выбора ответа сравниваем их с критическими значениями и выдаем сообщение.
 

### Начальные характеристики:

* Здоровье – 2 (от 0);
* Настроение – 2 (от 0);
* Деньги – 125 (от 0).
 
### Список вопросов:

#### Вопрос 1 (радиобаттон):

1.1 Купить новый пенал – Деньги -75;

1.2 Просидеть до позднего вечера и починить старый пенал – Здоровье -1;

1.3 Продолжить пользоваться старым пеналом без починки – Настроение -1.
 

#### Вопрос 2 (радиобаттон):

2.1 Купить косточку – Деньги -55;

2.2 Задержаться в парке и поиграть – Здоровье -1, Настроение +1;

2.3 Пойти домой – Настроение -1.

#### Вопрос 3 (радиобаттон):

3.1 Раздать листовки – Деньги +100, Здоровье -1;

3.2 Отказаться от купона – Настроение -1.

### Проверка критических условий: 

* Если здоровье упало до 0 выдавать сообщение в модальном окне – «Мои силы закончились, кажется я заболеваю..»

* Если настроение упало до 0 выдавать сообщение в модальном окне – «У меня совсем нет настроения идти в эту школу..»

* Если деньги упали до 0 выдавать сообщение в модальном окне – «Кажется, я никогда не смогу управлять своими финансами..»

* Если критических точек нет, то – «Как же хорошо, теперь моя мечта осуществится!»


### Дополнительные условия задания: 

Характеристики записывать в localStorage в виде объекта, например:

parameters: {
  health: 2,
  mood: 2,
  money: 125
}

После прохождения сценария сохранять текущие параметры в localStorage.

Читать их в начале следующей итерации и выводить в лог консоли как результат прошлого сценария. Добавить кнопку сброса сценария.