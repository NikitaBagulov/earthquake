# Earthquake
 Пакет Earthquake для постоения графиков о землетрясениях по данным. Данные глобальной сети GNSS доступны на https://simurg.space, данные ионозондов доступны на https://giro.uml.edu. Бумага с данными вместе с блокнотом (с сохраненными выходными данными) доступны здесь https://cloud.iszf.irk.ru/index.php/s/3RcnGdohf38kmAO. Пишите по адресу artem_vesnin@iszf.irk.ru, если у вас есть какие-либо вопросы о формате данных или поведении того или иного фрагмента кода.


## Установка
1. Склонируйте репозиторий на свой компьютер\
```git clone https://github.com/NikitaBagulov/earthquake```
2. Установите Conda и откройте Conda Prompt
3. Создайте окружение и активируйте его\
```conda create -n earthquake```\
```conda activate earthquake```
4. Перейдите в директорию с проектом\
```cd path/to/file```
5. Установите библиотеку Cartopy\
```conda install cartopy```
6. Протестируйте библиотеку \
```make test```


 

## Использование
prepare_layout: Это функция, которая настраивает макет графика, включая ограничения по долготе и широте, сетку, и добавление некоторых географических элементов (побережье, границы, озера, реки).

plot_map: Это функция для построения графика данных для одного момента времени. Она принимает временные метки, данные, тип данных, ограничения по долготе и широте, количество строк и столбцов в макете графика, маркеры, флаги сортировки и использования альфа-канала, а также ограничения для цветовой шкалы. Функция создает графики с использованием библиотеки Matplotlib и Cartopy.

retrieve_data: Это функция для извлечения данных из файла в формате HDF5. Она принимает имя файла и тип данных и возвращает словарь, где ключами являются временные метки, а значениями - соответствующие данные.

_merge_structured_arrays: Это вспомогательная функция для объединения структурированных массивов данных.

retrieve_data_multiple_source: Это функция для извлечения данных из нескольких файлов и объединения их в один словарь. Она принимает список файлов, тип данных и временные метки (если указаны).

plot_maps: Это функция для построения графиков на основе данных из нескольких источников. Она принимает список файлов данных, словарь типов данных для каждого файла, словарь с информацией об эпицентрах, ограничения для цветовой шкалы, временные метки и масштаб. Функция использует предыдущие функции для извлечения данных и построения графиков.




![Результат функции plot_map:][1]Результат функции plot_map:

[1]:https://github.com/NikitaBagulov/earthquake/blob/develop/images/image1.png

## Лицензия

Этот проект находится под лицензией MIT. Подробную информацию можно найти в файле `LICENSE.md`.
