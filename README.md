# Задача

Написать мобильное приложение, которое отображет список контактов и выполняет поиск по ним. Приложение должно быть написано на React Native и запускаться на iOS и Android. Решенное задание выложить на github/gitlab, код в архиве приниматься не будет.

## Описание

Приложение получает данные из трех источников, и сохраняет их локально. _Для получения прямой ссылки на json нажать View Raw при просмотре._
- [источник 1](json/generated-01.json), 
- [источник 2](json/generated-02.json), 
- [источник 3](json/generated-03.json) 

Полученные данные отображает и позволяет выполнять поиск по ним.

![Список контактов](static/Contacts.png)
![Описание контакта](static/Profile.png)

Контакт описан таким образом:

- `id (string)` — ID контакта
- `name (string)` — Имя человека
- `height (float)` — Рост человека
- `biography (string)` — Биография человека
- `temperament (enum)` — Темперамент человека (`melancholic, phlegmatic, sanguine, choleric`)
- `educationPeriod (object)` — Период прохождения учебы. Состоит из дат `start` и `end`.

## Задача

1. Список контактов можно обновить свайпом вниз.
2. Сортировать список по имени в алфавитном порядке.
3. Поиск среди контактов происходит по имени или номеру телефона с любым форматом (4622257 должен найти Macdonald Talley).
4. Результаты поиска появляются по мере ввода символов в строку поиска и могут отображаться в основном списке.
5. При клике на контакт открывается экран с подробной информацией.
6. Клик по номеру телефона запускает звонок.
7. Если при запуске приложения с момента прошлой загрузки данных прошло __более 1 минуты__, то данные необходимо загрузить заново, иначе, нужно показать данные, сохраненные локально.
8. Если при загрузке или обновлении данных происходит ошибка, то нужно показать ее как на скриншоте:

![Ошибка при загрузке](static/Contacts_Error.png)
