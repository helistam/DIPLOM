# Для каждого ресурса будет свой файл с ожидаемым состоянием
## Условный синтаксис для Deployment 
---
```
Name_of_namespace_1:
    name_of_deployment1:
        replicas: n
        containerName: n
        containerCPURequests: n
        ...
    name_of_deployment2:
        replicas: m
        ....
    ...
Name_of_namespace_2:
    ....
```
Обязательные параметры :
```
- Имя Deployment 
- Имя Namespace
```
---
## Результат 
---
Для каждого Deployment в указанном namespace будут применены только те изменения, которые указаны. Таким образом есть возможность не переписывать множество манифестов вручную, а укаывать имена деплойментов и что хотим изменить.

---
# Доп. возможности 
Будет создан свой параметр с названием COPY_REQUESTS_TO_LIMITS , позволяющий присовоить значение Requests в Limits.   
### Состояния данного параметра 
```
- all
- cpu
- memory
- false 
```