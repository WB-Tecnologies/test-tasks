Нужно разработать простой сервис Time-tracker. Пользователь может создавать задачи, отмечать сколько времени он на них потратил. 

Для хранения данных использовать localstorage (далее LS). 

Функциональные части сервиса:
* Регистрация и аутентификация. Открывается по URL /enter. При входе пользователь вводит логин и пароль. Если такого логина нет в LS, то он сохраняется вместе с паролем. Если есть, то проверяется совпадают ли сохраненный и введенный пароли. Если нет, показывается сообщение об ошибке. После успешного ввода происходит редирект на страницу со списком задач.
* Список задач. Открывается по URL /todos. Задачи располагаются списком сверху вниз от самой важной до наименее важной. Есть кнопка показать\скрыть завершенные.
* Добавление задачи
  * Название
  * Срок. Дата когда задача должна быть выполнена. Реализовать в виде календаря где можно выбрать дату.
  * Дополнительно. Теги (можно несколько, например [bug] [срочно]). Вводятся текстом в то же поле что и название, выделяются квадратными скобками. В списке задач теги должны выглядеть как лейблы http://getbootstrap.com/components/#labels
* Удаление задачи. Перед удалением показывать сообщение “точно удалить задачу?”. 
* Редактирование задачи. Можно отредактировать название, срок, теги.
* Приоритет. Изменяется перетаскиванием задач в рамках списка.
* Затраченное время. У каждой задачи есть иконка-кнопка в виде часов после нажатия на которую предлагается ввести затраченного количество времени в минутах. Дополнительно можно реализовать что бы воспринимались разные форматы ввода для часов и минут. Например 1 час = вводим 60m или 1h 
* Завершение задачи. У каждой задачи можно поставить галочку и задача отмечается как завершенная. Завершенные задачи по умолчанию не показываются в списке, но сделать кнопку которая их покажет (выделить их можно, например,перечеркнутым названием).