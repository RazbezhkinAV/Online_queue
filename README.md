# Online_queue
RESTfull pet project online queue

GET localhost:8080/api/persons - получение информации авторизированного пользователя;
POST localhost:8080/api/persons - сохранение нового пользователя в БД (Json передаётся в Body -> объект Person);
PUT localhost:8080/api/persons - обновление информации пользователя (Json передаётся в Body -> объект Person);
DELETE localhost:8080/api/persons - удаление авторизированного пользователя;
POST localhost:8080/api/persons/registration-ticket - регистрация билета на указанное время (Json передаётся в Body -> String с указанием времени в формате HH:mm);

GET localhost:8080/api/reception - получение информации о состоянии ресепшена;
PUT localhost:8080/api/reception/registration - регистрация пользователя по номеру телефона на приём если подошло его время (Json передаётся в Body -> String phoneNumber);
PUT localhost:8080/api/reception/end-meeting - окончание встречи;

GET localhost:8080/api/tickets - получение всех билетов;
GET localhost:8080/api/tickets/free - получение свободных билетов начиная с текущего времени;
GET localhost:8080/api/tickets/near-active - получение занятых в ближайшие 30 минут билетов;
DELETE localhost:8080/api/tickets - удаление билета по времени (Json передаётся в Body -> String с указанием времени в формате HH:mm);
PUT localhost:8080/api/tickets/{id} - подтверждение билета по id;
GET localhost:8080/api/tickets/{id} - получение билета по id;
