```markdown
# Реализация абстрактных структур данных

Этот проект представляет собой реализацию различных абстрактных структур данных с базовым набором операций и удобным интерфейсом командной строки для взаимодействия с ними.

## Реализованные структуры данных

* **Массив (Array):**  Реализация динамического массива с операциями добавления, получения, удаления, замены элементов и определения размера.
* **Список (List):**  Односвязный и двусвязный списки с операциями добавления, удаления, поиска и получения элементов.
* **Очередь (Queue):** Реализация очереди (FIFO) с операциями добавления (enqueue), удаления (dequeue) и чтения (peek).
* **Стек (Stack):** Реализация стека (LIFO) с операциями добавления (push), удаления (pop) и чтения (peek).
* **Хеш-таблица (Hash Table):** Хеш-таблица с обработкой коллизий методом цепочек,  операциями добавления, получения и удаления элементов.
* **АВЛ-дерево (AVL Tree):**  Сбалансированное двоичное дерево поиска с операциями добавления, поиска, удаления и обхода.

## Использование

Для взаимодействия со структурами данных используется интерфейс командной строки.

```bash
./dbms --file <имя_файла> --query <запрос>
```

**Аргументы:**

* `--file <имя_файла>`: Путь к файлу для хранения данных (опционально. Если не указан, данные хранятся в памяти).
* `--query <запрос>`:  Запрос к базе данных, состоящий из команды и параметров.


**Примеры запросов:**

```bash
./dbms --file data.txt --query 'SPUSH mystack item'  # Добавляет "item" в стек "mystack"
./dbms --file data.txt --query 'QPOP myqueue'       # Удаляет элемент из очереди "myqueue"
./dbms --file data.txt --query 'HSET myhash key value' # Добавляет пару "key: value" в хеш-таблицу "myhash"
```

##  Производительность (Big O notation)

| Структура данных | Добавление | Удаление | Поиск    | Получение |
|-------------------|------------|----------|----------|-----------|
| Массив           | O(1) амортизированное | O(n)     | O(1)     | O(1)     |
| Список           | O(1)       | O(n)     | O(n)     | O(n)     |
| Очередь          | O(1)       | O(1)     | O(n)     | O(1)     |
| Стек             | O(1)       | O(1)     | O(n)     | O(1)     |
| Хеш-таблица     | O(1) среднее, O(n) в худшем случае | O(1) среднее, O(n) в худшем случае | O(1) среднее, O(n) в худшем случае | O(1) среднее, O(n) в худшем случае |
| АВЛ-дерево       | O(log n)   | O(log n) | O(log n) | O(log n) |