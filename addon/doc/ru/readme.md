# Newfon

* Авторы: Сергей Шишминцев, Alexy Sadovoi, Сергей A.K.A. Electrik, Kvark и другие разработчики
* Скачать [стабильную версию][1]
* Совместимость с NVDA: 2019.2 to 2023.1

### О Newfon

Newfon — синтезатор речи, впервые с момента выпуска поддерживающий русский и украинский языки. Позже были добавлены хорватский, польский и сербский языки.

### Общие возможности:

* Возможность смены языков;
* Смена частоты дискретизации;
* Интерполяция звука, что позволяет имитировать звучание старых DOS скринридеров и чтецов книг;
* Чтобы синтезатор прочитывал текст так как написано, есть возможность отключения встроенного словаря ударений. опция работает только для русского языка;
* Синтезатор помимо основной скорости от 0 до 100 %, поддерживает дополнительное ускорение речи, что уменьшает время прочтения текста;
* чтобы получить более сглаженное чтение на больших скоростях, есть возможность регулировки пауз между фразами.

### Примечание:

Многочисленные версии Newfon были выпущены с момента его первой публикации на официальном сайте дополнений NVDA, но, к сожалению, ведущий разработчик Сергей Шишминцев умер, что задержало обновление синтезатора на сайте.

В 2017 году нынешние разработчики синтезатора речи Newfon получили возможность получить исходные коды разработок Сергея. Его родственники, благодаря которым это произошло, поставили им лишь одно условие: если развитие его проектов продолжится, они должны стать бесплатными.

Разработчики, в свою очередь, решили, что история не должна забывать Сергея Шишминцева, так как он был уникальным программистом с колоссальным запасом упорства, трудолюбия и знаний.

## История изменений

### Версия 2023.1

* Добавлена ​​совместимость с NVDA 2023.1 (по-прежнему поддерживается обратная совместимость с NVDA 2019);
* Добавлено лицензионное соглашение Newfon на английском языке;
* Добавлена ​​документация на русском языке.

### Версия 2022.04.16

Совместимость с NVDA 2022 (по-прежнему поддерживается обратная совместимость с NVDA 2019.2).

### Версия 2021.06.06

Для совместимости с последующими версиями NVDA, Был изменён параметр lastTestedNVDAVersion.

### Версия 2021.03.19

Для совместимости с последующими версиями NVDA, были изменены внутренние механизмы взаимодействия синтезатора с драйверами NVDA.

### Версия 2021.01.16
#### Добавлено:

speech.BreakCommand — данная возможность требуется некоторым дополнениям, чтобы приостановить речь на какое-то время.

#### Исправлено:

В украинском языке, некоторые большие буквы читались не корректно.

### Версия 2020.12.28

В этой версии сделана значительная переработка скриптов, реструктуризация дополнения, новые языки (возможность тестирования) и многое другое.

#### Добавлено:

* Новые языки: хорватский, польский, сербский. Эти скрипты были взяты из открытых источников и предоставлены бета-тестерами. Автор не может нести ответственность за работу этих скриптов, поэтому вы используете их как есть - без каких-либо гарантий;
* В русский язык были добавлены некоторые старорусские символы: «і»: «и десятеричное», «ѣ»: «ять», «ѳ»: «фита», «ѵ»: «ижица», «ў»: «у краткое», «ґ»: «гэ взрывное», Соответственно, если вы прочтёте старорусское слово, оно прочитается корректно;
* Интерполяция звука. Теперь вы можете имитировать звучание ньюфона, так как это было в старых DOS скринридерах и чтецах книг. Для реализации этой возможности используется библиотека libsamplerate;
* Теперь можно отключить чтение десятичных дробей (только для русского и украинского языка), что улучшает чтение версий программ.

#### Изменено:

* Произведена полная переработка дополнения. теперь весь код не находится в одном файле __init__.py, что позволяет обслуживать код и добавлять новые языки гораздо проще;
* Очереди из DLL были перенесены на Python, что хорошо сказалось на стабильности дополнения.

#### Исправлено:

Ошибка рассинхронизации звука, изредка проявлявшаяся на последних версиях NVDA.

### Версия 2020.09.12
#### Изменено:

Из за изменения способа работы со звуковой подсистемой В новых альфа версиях NVDA, частота дискретизации не переключалась должным образом.

### Версия 2020.03.12
#### Добавлено:

* По просьбам пользователей, добавлена опциональная возможность при английском произношении, заместо звука е произносить звук э — как в старых дополнениях;
* Теперь дополнение имеет локализацию, соответственно, на украинском интерфейсе NVDA все дополнительные параметры будут отображаться на соответствующем языке.

#### Изменено

* Благодаря программисту Kvark — была переписана внутренняя архитектура дополнения на третий Python;
* Для любителей нестандартных голосов, расширен список выбора частот дискретизации.

[1]: https://github.com/DraganRatkovich/newfon/releases/download/2023.1/newfon-2023.1.nvda-addon