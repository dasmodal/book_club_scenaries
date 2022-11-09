## User

- nickname - string

- email - string

- password - 

- is_admin - boolean

## Book

- title - string

- year - integer

- author - string

- genre - string

- cover - attached

- rating - float # средний рейтинг из оценок

- user_id - references # айди юзера который добавил книгу

## Rate

- value - integer

- book_id - references

- user_id - references

## Comment

- text - string

- book_id - refernces

- user_id - references

## Complaint # жалоба на книгу

- text - string

- book_id - references

- user_id - references # айди юзера который отправил предупреждение

## List

- title - string

- user_id - references

## BookList # связывающая таблица many to many для List и Book

- book_id - references

- list_id - references

## BlockWarning # предупреждение или бан, выдаваемое админом юзеру

- text - string

- ban - boolean

- admin_id - references # айди админа

- user_id - references # айди юзера которому выписано предупреждение
