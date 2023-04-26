# Создание поля

lines = [1,2,3,
         4,5,6,
         7,8,9]

# Варианты победы

viclin = [[0,1,2],[3,4,5],[6,7,8],[0,3,6],[1,4,7],[2,5,8],[0,4,8],[2,4,6]]

# Вывод поля

def print_lines():
    print(lines[0], end = " ")
    print(lines[1], end = " ")
    print(lines[2])

    print(lines[3], end = " ")
    print(lines[4], end = " ")
    print(lines[5])

    print(lines[6], end = " ")
    print(lines[7], end = " ")
    print(lines[8])

# Ход в ячейку

def step_lines(mapr,sym):
    ind = lines.index(mapr)
    lines[ind] = sym
    
# Результат игры

def get_result():
    win = ""

