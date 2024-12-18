
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

**Аргументы:**

* `--file <имя_файла>`: Путь к файлу для хранения данных (опционально. Если не указан, данные хранятся в памяти).
* `--query <запрос>`:  Запрос к базе данных, состоящий из команды и параметров.
```

**Вот примеры запуска каждого из контейнеров:**

**Массив**

```bash
./dbms —file array.txt —query "MPUSH hello"
```

Эта команда добавляет строку "hello" в конец массива и сохраняет результат в файле `array.txt`.

**Связный список**

```bash
./dbms —file list.txt —query "LPUSH hello"
```

Эта команда добавляет строку "hello" в голову связного списка и сохраняет результат в файле `list.txt`.

**Очередь**

```bash
./dbms —file queue.txt —query "QPUSH hello"
```

Эта команда добавляет строку "hello" в очередь и сохраняет результат в файле `queue.txt`.

**Стек**

```bash
./dbms —file stack.txt —query "SPUSH hello"
```

Эта команда добавляет строку "hello" в стек и сохраняет результат в файле `stack.txt`.

**Хэш-таблица**

```bash
./dbms —file hash.txt —query "HSET key hello"
```

Эта команда добавляет запись с ключом "key" и значением "hello" в хэш-таблицу и сохраняет результат в файле `hash.txt`.

**АВЛ-дерево**

```bash
./dbms —file tree.txt —query "TINSERT hello"
```

Эта команда добавляет строку "hello" в АВЛ-дерево и сохраняет результат в файле `tree.txt`.

##  Производительность (Big O notation)

| Структура данных | Добавление | Удаление | Поиск    | Получение |
|-------------------|------------|----------|----------|-----------|
| Массив           | O(1) амортизированное | O(n)     | O(1)     | O(1)     |
| Список           | O(1)       | O(n)     | O(n)     | O(n)     |
| Очередь          | O(1)       | O(1)     | O(n)     | O(1)     |
| Стек             | O(1)       | O(1)     | O(n)     | O(1)     |
| Хеш-таблица     | O(1) среднее, O(n) в худшем случае | O(1) среднее, O(n) в худшем случае | O(1) среднее, O(n) в худшем случае | O(1) среднее, O(n) в худшем случае |
| АВЛ-дерево       | O(log n)   | O(log n) | O(log n) | O(log n) |