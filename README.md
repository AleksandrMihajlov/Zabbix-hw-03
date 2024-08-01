Система мониторинга Zabbix. Часть 2 - Aleksandr Mihajlov SYS34  
  
**Задание1**  
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/1.png)  
  
 **Задание2-3**  
Добавление готового шаблона Linux by Zabbix Agent и вывод Latest Data.
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/2.png)    
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/2.1.png)    
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/2.2.png)    
  
Далее необходимо добавить свой шаблон. Параметры CPU и RAM присутствуют в обоих шаблонах, как результат конфликт. Оставляем свой шаблон.
  
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/3.png)    
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/3.1.png)    
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/3.2.png)    
  
**Задание4**  
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/4.png)  
  
**Задание5**  
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/5.png)  
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/5.1.png)  
  
**Задание6**  
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/6.png)  
  
**Задание7**  
```python
import sys
import os
import re
import datetime
if (sys.argv[1] == '-ping'): # Если -ping
    result=os.popen("ping -c 1 " + sys.argv[2]).read() # Делаем пинг по заданному адресу
    result=re.findall(r"time=(.*) ms", result) # Выдёргиваем из результата время
    print(result[0]) # Выводим результат в консоль
elif (sys.argv[1] == '-simple_print'): # Если simple_print
    print(sys.argv[2]) # Выводим в консоль содержимое sys.arvg[2]
elif (sys.argv[1] == '1'): # Если ввод 1
    print(f"Aleksandr Mihajlov") # Выводим в консоль имя фамилия
elif (sys.argv[1] == '2'): # Если ввод 2
    res = datetime.datetime.now()
    print(res) # Выводим в консоль время
else: # Во всех остальных случаях
    print(f"unknown input: {sys.argv[1]}") # Выводим непонятый запрос в консоль  
```

![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/7.png)  
  
**Задание8**  
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/8.png)  
![alt text](https://github.com/AleksandrMihajlov/Zabbix-hw-03/blob/main/8.1.png) 