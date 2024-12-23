# Maven Dependency Graph Visualizer

## Описание
Этот проект позволяет анализировать зависимости Maven из файла `pom.xml` и визуализировать их в виде графа с использованием Graphviz. Основной пакет анализируется как корневой узел, а его зависимости отображаются в виде связей с дополнительной информацией, такой как группа, артефакт и версия.

## Возможности
- **Анализ зависимостей Maven** из файла `pom.xml`.
- **Визуализация зависимостей** с использованием Graphviz.
- **Гибкая настройка через JSON-конфигурацию**, включая:
  - Имя анализируемого пакета.
  - Путь к программе Graphviz.
  - Путь для сохранения изображения графа.
  - Максимальная глубина анализа зависимостей.

## Установка и запуск
1. Убедитесь, что у вас установлен Python 3.8 или выше.
2. Установите библиотеку Graphviz 
3. Установите зависимости Python:
   ```zsh
   pip install graphviz
   ```
4. Скачайте проект или клонируйте репозиторий.
5. Создайте JSON-конфигурационный файл для настройки. Пример:
   ```json
   {
       "graphviz_program_path": "/usr/local/bin",
       "package_name": "MyProject",
       "graph_image_path": "dependencies_graph",
       "max_depth": 3,
       "pom_file_path": "pom.xml"
   }
   ```
6. Запустите проект:
   ```zsh
   python3 main.py путь_к_конфигурации
   ```

### Пример
```zsh
python3 main.py config.json
```

## Тестирование
1. Для запуска тестов выполните:
   ```zsh
   python3 -m unittest test_main.py
   ```
2. Убедитесь, что тестовые файлы, такие как `test_config.json` и `test_pom.xml`, находятся в рабочем каталоге.

---
