view = list(range(1, 10))

victory_lines = [(1,2,3),(4,5,6),(7,8,9),(3,5,7),(1,5,9),(1,4,7),(2,5,8),(3,6,9)]



def inter_view():
    print("-" * 13)
    for a in range(3):
        print("|", view[0 + a * 3], "|", view[1 + a * 3], "|", view[2 + a * 3], "|")
    print("-" * 13)

    
def lin_inter(take):
    while True:
        line = inter('Делаем ход ' + take)
        line = int(line)
        if str(view[line - 1]) in 'X0':
            print('Занято')
            continue
        view[line - 1] = take
break
def result_win():
    for b in result_win:
        if (view[b[0]-1]) == (view[b[1]-1]) == (view[b[2]-1]):
           return view[b[1] - 1]
        else:
            return False
                

def bik():
    value = 0
    while True:
        inter_view()
        if value % 2 == 0:
            lin_inter('X')
        else:
            lin_inter('0')
        if value > 3:
            win = result_win()
            if win:
                inter_view()
                print(win, 'Победил')
                break
        value += 1
        if value > 8:
            inter_view()
            print('Никто не победил')
            break
        
bik()

