# Task-1

text = input("Введіть текст: ").lower()

text_length = len(text)

symbol_frequency = []         # Список зі значеннями частот для символів

empty_set = set()

symbol_rating = []            # Список частот за спаданням для символів


for i in text:

    if i not in empty_set:
    
        symb_freq = text.count(i)/text_length
        
        symbol_frequency.append(symb_freq)
        
        symbol_rating.append(str(float('{:.5f}'.format(symb_freq))) + " - частота появи символу " + i + "." + " Кількість появ у тексті - " + str(text.count(i)))
    
    empty_set.add(i)


print("Список частот за спаданням для символів:")

symbol_rating.sort(reverse=True)                                 # Відсортували список з частотами символів по спаданню

print('\n'.join(symbol_rating),'\n')

input()
