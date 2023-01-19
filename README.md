# **Улучшенный вектор**
*Учебный проект Яндекс.Практикума*

Vector - аналог стандартного контейнера vector, со сходной структурой и функционалом. В основе — массив в динамической памяти. Сам контейнер хранит лишь адрес начала массива, а также информацию о его текущем размере и вместимости.

**В классе вектора реализован следующий функционал:**
- Конструкторы.
  - По умолчанию. Создаёт пустой вектор с нулевой вместимостью. Не выделяет динамическую память и не выбрасывает исключений.
  - Параметризованный конструктор, создающий вектор заданного размера. Элементы вектора инициализированы значением по умолчанию для типа Type. Вектор имеет одинаковые размер и вместимость. Если размер нулевой, динамическая память для его элементов не выделяется.
  - Конструктор из std::initializer_list. Элементы вектора содержат копию элементов initializer_list. Имеет размер и вместимость, совпадающую с размерами и вместимостью переданного initializer_list.
  - Конструктор копирования. Копия вектора имеет вместимость, достаточную для хранения копии элементов исходного вектора.
  - Конструктор перемещения.
  - Конструктор, резервирующий нужное количество памяти.
- Оператор [] для доступа к элементу вектора по его индексу. Имеет две версии — константную и неконстантную. Не выбрасывает исключений. Для корректной работы оператора индекс элемента массива не должен выходить за пределы массива.
- Оператор присваивания. Обеспечивает строгую гарантию безопасности исключений.
- Операторы == и !=.
- Операторы <, >, <=, >=, выполняющие лексикографическое сравнение содержимого двух векторов.
- Метод GetSize для получения количества элементов в векторе. Не выбрасывает исключений.
- Метод GetCapacity для получения вместимости вектора. Не выбрасывает исключений.
- Метод IsEmpty, сообщающий, пуст ли вектор. Не выбрасывает исключений.
- Метод At для доступа к элементу вектора по его индексу, аналог метода at класса vector. В случае выхода индекса за пределы массива выбросывает исключение std::out_of_range.
- Метод Clear для очистки массива без изменения его вместимости. Не выбрасывает исключений.
- Метод Resize для изменения количества элементов в массиве. Метод предоставляет строгую гарантию безопасности исключений.
- Методы begin, end, cbegin и cend, возвращающие итераторы на начало и конец массива. В качестве итераторов используйте указатели.
- Метод PushBack, добавляющий элемент в конец вектора. Обеспечивает строгую гарантию безопасности исключений.
- Метод PopBack, удаляющий последний элемент вектора. Не выбрасывает исключений.
- Метод Insert, вставляющий элемент в произвольное место контейнера. Обеспечивает базовую гарантию безопасности исключений.
- Метод Erase, удаляющий элемент в произвольной позиции вектора. Обеспечивает базовую гарантию безопасности исключений.
- Метод swap, обменивающий содержимое вектора с другим вектором. Не выбрасывает исключений, имеет время выполнения O(1).
- Метод Reserve задает ёмкость вектора. Этот метод повышает эффективность кода в случае, когда пользователь заранее знает хотя бы приблизительное количество элементов в векторе. Reserve сразу выделяет нужное количество памяти. При добавлении новых элементов в вектор копирование будет происходить или значительно реже или совсем не будет.
