# Вместе на такси - TogetherByTaxi
Сервис, который позволяет пользователям экономить на такси, а сервисам такси использовать свои данные в одной общей площадке
Основные тезисы
1) Мобильное приложение + сайт
2) Пользователь выбирает куда он хочет ехать, есть возможность указать из какой точки он едет(либо автоматически при запросе координат)
3) У пользователя отображается сколько рядом есть людей, с этим приложением, и кто едет из этого же района в тот район, что он указал
4) Работа с картами(выбора на карте + ввод данных по адресу). Либо гугл карты, либо яндекс карты
5) У пользователя есть свой профиль, где он может разместить фото(или вход под аккаунтами вконтакте, одноклассники, фэйсбук, майкрософт, возможно что-то ещё).
6) Этот профиль возможно просмотреть пользователю в расширенной версии.
7) В расширенной версии(или в простой) пользователь может указать оценкой операторов такси
8) В расширенной версии(или в простой) пользователь может указать оценкой попутчиков(насколько адекватен, насколько с ним комфортно). Возможно ранжирование по шкале
9) Для сервисов такси - это что-то наподобие нового агрегатора, где прямо из приложения пользователь может вызвать такси(подумать, как лучше всего это делать)
10) Сервисы такси могут разместить просто свои телефоны, для набора номера
11) Пользователь может расширить и сузить круг поиска откуда он едет(поиск попутчиков), и круг поиска куда едет(так же поиск попутчиков по месту прибытия)
12) Возможность сохранения своих проезженных маршрутов(история с возможностью удаления).
13) Возможно ввести стандартные маршруты - дом, работа, бар любимый
14) Умение работать на всех моделей телефонов - начинаем с андроид
15) Пользователь в настройках может разрешать/запрещать искать его
16) Пользователь может указывать количество людей с собой.
17) При создании  "Поездки" пользователям необходимо сделать селфи, чтобы попутчики были уверны с кем они едут

Приложение написано на принципе микросервисов. За основу берём .net core

Микросервисы, которые нужны
1) Сервис авторизации(Identity) - https://github.com/sevastopolsharks/TogetherByTaxi_Identity
2) WebApi - апи для возврата основных результатов и работы с основными данными
3) UI - вот тут полная свобода, предлагаю сайт пилить на Angular + нативное приложение для Android
4) Сервис уведомлений - получает уведомления через шину и потом эти уведомления рассылает(SignalR, почта, sms)
5) SignalR - https://github.com/sevastopolsharks/TogetherByTaxi_SignalR

P.S. Список сервисов может расширяться после применения DDD и выявления доменных моделей и связей между ними
