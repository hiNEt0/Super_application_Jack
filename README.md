# Super_application_Jack
Игруля Flappy Bird
Наша команда представляет игру Flappy Bird в оригинальной конфигурации.
Написанная на языка программирования Jack она служит хорошим показателям его возможностей.
Так, напрмер, в классе pipe можно наблюдать взаимодействие с экраном с помощью специального класса,
А в классе Bird тоже взаимодействие с экраном, но уже с помощью работы непосредственно с памятью.
Также работа с памятью помогла реализовать "коллайдер" для птицы:
Так все поле, крмое мест с трубами, пустое, то можно предугадывать куда попадет птица(т.к. у неё прописана физика) -
И благодаря этой информации обращаться к соответсвующим ячейкам памяти, чтобы проверить, есть ли там какие-то биты.
В классе Random написан простой алгоритм получения псевдорандомных чисел 
При помощи написанной в классе MathExtensions функции findRemains.
Чтобы числа были ещё более рандомными, мы решили сделать следующий трюк:
При запускании программы отсчитываем количество прошедших тиков,
Причем функция findRemains помогает избежать ошибки переполнения.
В классе Bird реализована простая анимация полета:
Как только птица теряет скорость, её крылья поднимаются, чтобы парить на воздухе;
Нажмите на space, чтобы птица смогла оттолкнутся от воздуха и взлететь ввысь!
Благодаря непосредственно работе с памятью нам удалось менять состояние птицы практически без "моргания".
В классе GameField реализовано движения игрового поля: самая нетривиальная задача.
Пришлось сохранять объекты поля - трубы - в массиве и заколцевать их в игровом поле, чтобы не было переполнения памяти.
При работе с GameField пришлось обходить недостаток языка Jack:
Если в массиве лежит ссылка на класс, то по ней нельзя обратиться к данному классу -
С помощью ввода дополнительной переменной.

Получилось отличное знакомство с языком, компилятор для которого нам ещё предстоит написать.
Мы отметили все плюсы и недостатки слабой типизации, вспомогательных слов(do, let) и многих других особенностей Jack.