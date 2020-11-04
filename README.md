# Email Finder
Это **бесплатный** инструмент для поиска почтовых ящиков *кандидатов* в гитхабе. Cкрипт предназначен для того, чтобы сделать этот мир чуточку лучше, а именно, помочь рекрутерам находить контакты, чтобы иметь возможность предложить кандидату вакансию его мечты (как минимум тем, кто не использует сгенерированные ящики:)

---

### Принцип работы:
Вам необходимо ввести **username** пользователя GitHub, после чего, скрипт сперва поищет ящики в github public API, а затем зайдет в репозитории, выберет каждый первый коммит соберет все почтовые ящики и имена авторов, результатом вернет все уникальные. Скрипт будет обходить форкнутые и архивные репозитории, а так же, по возможности, будет обходить других авторов коммитов. Тем не менее, в редких случаях будут попадаться чужие почтовые ящики, но так как скрипт показывает имя или ник хозяина почты, будет легко идентифицировать, кому принадлежит контакт. 

Так же скрипт проверяет по нику в GitHub наличие аккаунта с таким же ником в телеграме, чтобы у рекрутера была возможность написать напрямую, минуя почту. Если пользователь телеграм аккаунта указал имя или ФИО, скрипт вернет информацию с этим, в противном случае будет только ссылка. Здесь следует учитывать, что аккаунты с одинаковыми никами могут принадлежать разным пользователям, однако, при тестировании, в 60% случаев, хозяин двух аккаунтов совпадал.

--- 

### Инструкция для рекрутеров:

Если вы не знаете, как использовать скрипт или запустить его, для вас я оставлю самый простой способ. Для запуска скрипта, вам необходимо использовать [Google Colab](https://colab.research.google.com/), это среда для выполнения кода с возоможностью запуска прямо из вашего личного google drive.

Вам необходимо:
1. Зайти в ваш Google Drive аккаунт
2. В левом верхнем углу кликнуть на "создать"
3. Из списка предложенных вариантов выбрать Google Colaboratory
4. Открыть скрипт mailstretcher.py в самом репозитории и скопировать из него код
5. В Google Colaboratory вставить содержимое из буфера в доступную ячейку и выполнить скрипт, кликнув по элементу со стрелкой слева от кода
6. Когда тетрадка запустится, снизу появится поле, в которое будет предложено ввести UserName пользователя GitHub

--- 

## Как выглядит результат работы скрипта:
<img src="https://github.com/carrollstreet/Email-Finder/raw/main/img.png" width="500" height="400" />

