Список - это коллекция, которая упорядочена и может быть изменена. Позволяет создавать дубликаты элементов.  
Кортеж - это коллекция, которая упорядочена и не подлежит изменению. Позволяет создавать дубликаты элементов.  
Set — это коллекция, которая не упорядочена, не может быть изменена* и не индексирована. Никаких дубликатов участников.  
Словарь - это коллекция, которая упорядочена** и может быть изменена. Никаких дубликатов участников.  

# 1. List (список)  

✅ Упорядочен, ✅ изменяемый, ✅ дубликаты  

### Создание  
my_list = ["apple", "banana", "cherry"]  

### Доступ по индексу  
print(my_list[0])        # apple  

### Изменение  
my_list[1] = "mango"  

### Добавление  
my_list.append("orange") # в конец  
my_list.insert(1, "kiwi")# по индексу  

### Удаление  
my_list.remove("apple")  # по значению  
my_list.pop(1)           # по индексу  
del my_list[0]           # удалить по индексу  
my_list.clear()          # очистить  

### Полезное  
print(len(my_list))      # длина  
print("mango" in my_list) # проверка  
my_list.sort()           # сортировка  
my_list.reverse()        # разворот  

# 2. Tuple (кортеж)  

✅ Упорядочен, ❌ неизменяемый, ✅ дубликаты  
  
### Создание  
my_tuple = ("apple", "banana", "cherry")  

### Доступ по индексу   
print(my_tuple[0])   # apple  

### Кортеж нельзя изменять, но можно:  
print(len(my_tuple))     # длина  
print("banana" in my_tuple) # проверка  

### Трюк — преобразовать в список и обратно:  
temp = list(my_tuple)  
temp[1] = "mango"  
my_tuple = tuple(temp)  

# 3. Set (множество)  

❌ Неупорядочен, ✅ изменяемый (частично), ❌ нет дубликатов  

### Создание  
my_set = {"apple", "banana", "cherry"}  
  
### Добавление  
my_set.add("orange")  

### Несколько сразу  
my_set.update(["kiwi", "mango"])  
  
### Удаление  
my_set.remove("banana")  # ошибка если нет элемента  
my_set.discard("banana") # безопасно  
x = my_set.pop()         # удалить случайный элемент  
my_set.clear()           # очистить  

### Операции множеств  
a = {1, 2, 3}  
b = {3, 4, 5}  
print(a.union(b))        # объединение  
print(a.intersection(b)) # пересечение  
print(a.difference(b))   # разность  

# 4. Dict (словарь)  

✅ Упорядочен, ✅ изменяемый, ❌ ключи уникальны  
  
### Создание  
my_dict = {"name": "John", "age": 25}  

### Доступ  
print(my_dict["name"])        # John  
print(my_dict.get("age"))     # 25  

### Добавление / изменение  
my_dict["city"] = "London"  
my_dict["age"] = 30  

### Удаление  
my_dict.pop("age")       # по ключу  
del my_dict["name"]  
my_dict.clear()          # очистить  

### Полезное  
print(len(my_dict))      # длина   
print("city" in my_dict) # проверка ключа  

### Перебор  
for k, v in my_dict.items():  
    print(k, v)  # name John  

### Копия  
copy_dict = my_dict.copy()  
  
