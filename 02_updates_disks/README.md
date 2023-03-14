# Введение
В данном руководстве рассмотрим с вами добавление некомерческих репозиториев для обновления ОС, а также создадим локальное хранилище (storage)
## Цели
- Добавить алтернативные репозитории обновления ОС 
- Поизвести проверку и обновление системы
- Создать storage для дальнейшей установки виртуальных машин и контейнеров

## Настройка репозитория
- Так как по умолчанию используется комерческий репозиторий обновлений, который доступен по подписке, необходимо проделать ряд действий по смене его на бесплатный
![Screenshot_5](https://user-images.githubusercontent.com/1348639/225052262-8af40ee7-7f97-4056-a17c-49ec5e7cca2c.png)
![image](https://user-images.githubusercontent.com/1348639/225052678-e688be69-8acb-412b-b2ad-6d5cf62c69e7.png)
![image](https://user-images.githubusercontent.com/1348639/225052834-b860d82b-30ba-431e-9987-13c742756b26.png)
![image](https://user-images.githubusercontent.com/1348639/225053047-a9f6357a-c813-4a34-85bc-95bea3bb181c.png)
![image](https://user-images.githubusercontent.com/1348639/225053162-df31cf2c-803b-4aab-a721-150ba211a88d.png)
## Обновление
![image](https://user-images.githubusercontent.com/1348639/225053511-60046ba0-52d5-4271-afa8-87dd3f7a9b38.png)
![image](https://user-images.githubusercontent.com/1348639/225053551-0acfd349-55cf-4018-9f09-311c29f0670f.png)
- Окно обновления можно закрыть только после статуса "TASK OK" 
![image](https://user-images.githubusercontent.com/1348639/225053648-b8112eb1-211f-438d-afd3-8044d469a57c.png)
![image](https://user-images.githubusercontent.com/1348639/225053924-90fe05b5-656a-451d-8236-87016d7fa3dd.png)
![image](https://user-images.githubusercontent.com/1348639/225054309-e741119f-a208-491e-92c0-a8d2e6411b2d.png)
## Создание локального storage
- Для дальнейшей работы с виртуальными машинами, необходимо создать дисковое хранилище. В случае работы на виртуальной машине - диски будут виртуальные (созданные ранее)
![image](https://user-images.githubusercontent.com/1348639/225055577-daafa0a1-18f3-495b-bf7f-1956b32f953a.png)
- при подговке дисков будьте внимательные и не произведите форматирование диска, на котором установлена операционная система!
![image](https://user-images.githubusercontent.com/1348639/225056310-20b4f081-71c7-4b21-a1c8-9d186bfdaa55.png)
![image](https://user-images.githubusercontent.com/1348639/225056553-0a885349-2a95-4d70-816b-f0160c341006.png)
![image](https://user-images.githubusercontent.com/1348639/225056653-fba5e02c-a130-47c0-b10e-8bfe92ef0699.png)
![image](https://user-images.githubusercontent.com/1348639/225056916-e84119bf-13a5-4120-85e3-fa873639564a.png)
- Зададим параметры хранилища
![image](https://user-images.githubusercontent.com/1348639/225057432-d8bcb0f2-2bc2-4c0d-acbf-c38892a9eeac.png)
![image](https://user-images.githubusercontent.com/1348639/225057530-428eb4f2-9750-46cb-b2a8-5ea2f94069f2.png)
## Создание Dataset
- Создадим dataset в только что созданном storage. Это необходимо для организовации хранения файлов вне системного диска.
![image](https://user-images.githubusercontent.com/1348639/225075096-67c962b8-4894-440b-922a-4d465bca0833.png)
```
zfs create pool_name/data_set_name -o mountpoint=/mnt_point
#где pool_name - имя вашего storage (в нашем случае Pool1);
#где data_set_name - имя dataset, которое мы зададим для создания (в нашем случае data1)
#где mnt_point - имя точки монтирования (в нашем случае data).
```
![image](https://user-images.githubusercontent.com/1348639/225072891-79f3b33d-14e3-4550-81f0-4be43eb28b03.png)
![image](https://user-images.githubusercontent.com/1348639/225074281-2532e82b-a387-437e-9e4e-514396cfe179.png)
![image](https://user-images.githubusercontent.com/1348639/225076892-1719b1c4-bf3f-43ac-a8eb-f38671179a08.png)
![image](https://user-images.githubusercontent.com/1348639/225077075-000f17e0-84f8-471c-81a0-6d6ae0433cc5.png)

На этом настройка завершена

