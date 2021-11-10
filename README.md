# Charles-Fiddler
## Charles_HW_1
Настроить сниффинг трафика на Android.
________________________________________________________________________________
## **Charles HW_2** [ссылка]()
+ Ex_0: Сфокусироваться на ниже перечисленных запросах
```
Protocol: http
IP: 162.55.220.72
Port: 5005
```
+ Ex_1: 
```
Method: GET
EndPoint: /get_method
request url params: 
 name: str
 age: int

response: 
[
    “Str”,
    “Str”
]
```
Task:

Сделать и в Rewrite, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)
    
1. Подменить url в Charles чтобы в запросе ушло имя которые вы вписали в Postman, а вернулось то, которое вы подставили в Charles.


+ Ex_2:
```
Method: POST
EndPoint: /user_info_3
request form data: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}
```
Task:

Сделать и в Rewrite, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)

1. Подменить body в Charles так чтобы в запросе ушла salary которую вы вписали в Postman, а в u_salary_1_5_year цифра вернулась меньше оригинальной из запроса.


+ Ex_3:
```
Method: GET
EndPoint: /object_info_1
request url params: 
 name: str
 age: int
 weight: int

response: 
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}
```
Task:

Сделать и в Rewrite, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)

1. Подменить параметры запроса в Charles так, чтобы в Postman пришел ответ где другое name, daily_food > weight из запроса, а daily_sleep < weight из запроса.


+ Ex_4:
```
Method: GET
EndPoint: /object_info_3
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
          }
```
Task:

Сделать и в Rewrite, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)

1. Сделать через Charles так, чтобы сервер вернул 500 код.
2. Сделать через Charles так, чтобы сервер вернул 405 код.


+ Ex_5:
```
Method: GET
EndPoint: /object_info_4
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': int(age),
          'salary': [salary, str(salary * 2), str(salary * 3)]}
```
Task:

Сделать и в Rewrite, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)

1. Сделать через Charles так, чтобы сервер вернул 405 ошибку.
2. Подменить salary в request
3. Подменить (salary * 2) в response


+ Ex_6:
```
Method: POST
EndPoint: /user_info_2
request form data: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```

Task:

Сделать и в Rewrite, и в BreakPoint (можно отключить чтобы не стопило на каждом запросе)

1. Сделать через Charles так, чтобы в Postman вернулся ответ, в котором qa_salary_after_1.5_year переименовано в qa_salary_after_1.5_month
2. Сделать так чтобы qa_salary_after_3.5_years было меньше qa_salary_after_12_months в response
________________________________________________________________________________
## **Fiddler HomeWork** [ссылка]()

+ Ex_0: Отфильтровать выдачу запросов по нужному ip
```
Protocol: http
IP: 162.55.220.72
Port: 5005
```
+ Ex_1: 
```
Method: GET
EndPoint: /get_method
request url params: 
 name: str
 age: int

response: 
[
    “Str”,
    “Str”
]
```
Task:

Сделать правила:

1. Подменить url в чтобы в запросе поменялся name которые вы вписали в Postman.
2. Подменить url в чтобы в запросе поменялся age которые вы вписали в Postman. 


+ Ex_2:
```
Method: POST
EndPoint: /user_info_3
request form data: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'u_salary_1_5_year': salary * 4}}
```
Task:

Сделать правила:

1. Подменить тело запроса чтобы поменялся name которые вы вписали в Postman.
2. Подменить тело запроса чтобы поменялся age которые вы вписали в Postman. 
3. Подменить тело запроса чтобы поменялся salary которые вы вписали в Postman. 
4. Подменить тело запроса чтобы удалился age которые вы вписали в Postman.  (Получить 500 код)
5. В ответе поменять children на neighbors. 
6. В ответе поменять значение зарплаты u_salary_1_5_year на другую цифру. 
7. В ответе удалить параметр salary. 


+ Ex_3:
```
Method: GET
EndPoint: /object_info_1
request url params: 
 name: str
 age: int
 weight: int

response: 
{'name': name,
          'age': age,
          'daily_food': weight * 0.012,
          'daily_sleep': weight * 2.5}
```
Task:

Сделать правила:

1. Подменить url в чтобы в запросе поменялся name которые вы вписали в Postman.
2. Подменить url в чтобы в запросе поменялся age которые вы вписали в Postman. 
3. Подменить url в чтобы в запросе удалился weight которые вы вписали в Postman.
4. В ответе удалить параметр  daily_food.
5. В ответе поменять значение параметра daily_food на другую цифру. 
6. В ответе переименовать daily_sleep на sleep
7. В ответе поменять значение параметра daily_sleep на другую цифру. 


+ Ex_4:
```
Method: GET
EndPoint: /object_info_3
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': age,
          'salary': salary,
          'family': {'children': [['Alex', 24], ['Kate', 12]],
                     'pets': {'cat':{'name':'Sunny',
                                     'age': 3},
                              'dog':{'name':'Luky',
                                     'age': 4}},
                     'u_salary_1_5_year': salary * 4}
          }
```
Task:

Сделать правила:

1. Подменить url в чтобы в запросе поменялся name которые вы вписали в Postman.
2. Подменить url в чтобы в запросе поменялся age которые вы вписали в Postman. 
3. Подменить url в чтобы в запросе удалился name которые вы вписали в Postman.
4. В ответе удалить параметр  salary.
5. В ответе поменять значение параметра cat на другой json. 
6. Получить 405 код


+ Ex_5:
```
Method: GET
EndPoint: /object_info_4
request url params: 
 name: str
 age: int
 salary: int

response: 
{'name': name,
          'age': int(age),
          'salary': [salary, str(salary * 2), str(salary * 3)]}
```
Task:

1. Подменить url в чтобы в запросе поменялся name которые вы вписали в Postman.
2. Подменить url в чтобы в запросе поменялся age которые вы вписали в Postman. 
3. Подменить url в чтобы в запросе удалился salary которые вы вписали в Postman.
4. В ответе удалить параметр  salary.
5. В ответе поменять значение параметра salary на значение текстового типа. 
6. Получить 405 код


+ Ex_6:
```
Method: POST
EndPoint: /user_info_2
request form data: 
 name: str
 age: int
 salary: int

response: 
{'start_qa_salary': salary,
          'qa_salary_after_6_months': salary * 2,
          'qa_salary_after_12_months': salary * 2.7,
          'qa_salary_after_1.5_year': salary * 3.3,
          'qa_salary_after_3.5_years': salary * 3.8,
          'person': {'u_name': [user_name, salary, age],
                     'u_age': age,
                     'u_salary_5_years': salary * 4.2}
          }
```
Task:

Сделать правила:

1. Подменить тело запроса чтобы поменялся age которые вы вписали в Postman. 
2. Подменить тело запроса чтобы поменялся salary которые вы вписали в Postman. 
3. Подменить тело запроса чтобы удалился salary которые вы вписали в Postman.
4. В ответе поменять qa_salary_after_6_months на qa_salary_after_10_months. 
5. В ответе поменять значение зарплаты qa_salary_after_1.5_year на другую цифру. 
6. В ответе удалить параметр person. 
7. В ответе поменять значение параметр person с json на xml. 
