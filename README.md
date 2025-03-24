Данный проект был создан для первого тура чемпионата «IT-Планета 2025» в конкурсе «Создание проектов автоматизации бизнес-процессов предприятия на платформе 1С:Предприятие 8».

# Задача проекта

Разработать программу для клиента ООО «ЛюбимОбработкиПоЧтениюCSV», которая:

- Принимает на вход файл с данными в формате Excel, который необходимо прочитать и отобразить в таблице на форме;
- Реализует проверку на существование выбранного файла и его формат (Excel);
- Избегает дублирования строк при повторном чтении файла и удаляет пустые строки;
- Обеспечивает соответствие типов данных в 1С типам данных из файла Excel;
- Учитывает пожелания клиента по расположению элементов управления на форме, чтобы избежать ошибок в интерфейсе;
- Представлена в виде внешней обработки с расширением «.epf».

### Исходные данные

Таблица (1C_data.xlsx) пользователей/работников с полями:
* ФИО [тип данных: строка];
* Пол [тип данных: строка];
* День рождения [тип данных: дата];
* Оклад [тип данных: финансовый];
* Логин [тип данных: строка];
* Пароль [тип данных: строка].

Иллюстрация желаемой формы клиентом:

![forma](https://github.com/user-attachments/assets/b41be4bd-3da8-443c-a98d-e6bb5cee146a)

## Принцип работы кода

Код позволяет пользователю выбрать файл Excel, проверяет его существование и формат, извлекает данные в нужных типах, избегая дублирования и пустых строк, а затем отображает их в желаемой клиентом форме.

## Структура кода

1.  **ПутьКФайлуНачалоВыбора**: Открывает диалог выбора файла с фильтром для форматов .xls и .xlsx;
2.  **ПутьКФайлуНачалоВыбораЗавершение**: Сохраняет полный путь к выбранному файлу в поле ввода, если файл был выбран;
3.  **ПрочитатьДанные**: Вызывает серверную процедуру для чтения данных из выбранного Excel файла;
4.  **ЧтениеЭксельЧерезПостроительЗапроса**: Читает данные из Excel файла, обрабатывает их и заполняет таблицу пользователей, избегая пустых строк и дублирования.
