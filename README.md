# Interfaces_offset
Repository with program
В данном каталоге содержится директория data, в которой хранятся данные по исследованиям.
Вам нужно пройтись рекурсивно по директориям и считать все файлы, у которых выполнены условия (для этого нужно создать
менеджер контекста, который принимает на вход путь к директории и будет возвращать подходящие файлы).
Пример:
with file_names in DirReader("dir"):
    ...
Условие для чтения файла - файл оканчивается на .txt.
Внутри файлов хранится информация по ученым, которые открыли новую последовательность. По этим данным постройте граф, 
в котором вершина - это имя ученого,
а ребро будем проводить в случае, если два ученых открыли хотя бы одну последовательность.

Нам интересно знать, какие именно ученые открыли больше всего последовательностей, для этого реализуйте итератор 
GraphIterator, который на вход будет принимать граф и выдавать ученого с количеством открытых последовательностей 
(выдавать в порядке убывания по количеству открытых последовательностей). 
Пример
with science_name, count_seq in GraphIterator(G):
    ...
    
Реализуйте декоратор print_iter для GraphIterator с аргументом для задания имени файла (по умолчанию 'result.txt'), 
который будет записывать результаты в файл во время итерирования по графу.
@print_iter
class GraphIterator:
    ...
Задание нужно оформить в гит репозитории, с настроенным CI и тестированием.
