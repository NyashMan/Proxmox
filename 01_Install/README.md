# Введение  
В данном руководстве рассмотрим полную установку операционной системы Proxmox 7.3.1 на базе Linux Debian.  
Установку системы можно выполнить как с помощью средств виртуализации, так и с использованием реального оборудования.  
В данном пособие установка будет произвониться с помощью стредств виртуалзиции WMware Workstation 16 Pro.  
## Цели  
- Скачивание дистрибутива с официального сайта  
- Установка Proxmox  
## Перед началом установки:  
- Проверьте наличие на вашем компьютере одной из систем виртуализации (VMware/ VirtualBox /Hyper-V) (при сценарии установки системы с использованием программного гипервизора)  

- Проверьте совместимость вашего оборудования на соответствие [минимальным системным требованиям](https://www.proxmox.com/en/proxmox-ve/requirements/) (при сценарии установки системы на реальное оборудование)  

## Скачивание и настройка виртуальной машины  
Переходим на официальный сайт по ссылке: https://www.proxmox.com/  
![image](https://user-images.githubusercontent.com/1348639/224510137-314a1328-a1d5-41b0-8bb4-ac0380cc596c.png)
![image](https://user-images.githubusercontent.com/1348639/224510159-4eb87a11-d04a-4e17-a701-7c8bc070e52d.png)
Необходимо установить чекбокс для эмуляции виртуализации  
![image](https://user-images.githubusercontent.com/1348639/224531484-e70e4056-bec2-412d-b817-df448c9113c0.png)
Создадим несколько виртуальных жёстких дисков  
![image](https://user-images.githubusercontent.com/1348639/224531722-71488144-e8de-44a6-9f9f-e139f696580e.png)
![image](https://user-images.githubusercontent.com/1348639/224531756-53a4ca24-6a76-4c01-b180-56f67aa0c79c.png)
![image](https://user-images.githubusercontent.com/1348639/224531778-f5b110fe-f76a-4c42-9f21-1467448c9eeb.png)
- (По желанию) убрать чекбокс с пункта "Allocate all disk space now." для экономии места и времени создания файла  
![image](https://user-images.githubusercontent.com/1348639/224531883-4f6cf656-5482-4a29-84d2-c3ce74abeb4a.png)
![image](https://user-images.githubusercontent.com/1348639/224531815-828c2429-8810-4d1d-97ab-d3df3006858c.png)
- Итоговый вид окна настройки виртуальной машины  
![image](https://user-images.githubusercontent.com/1348639/224532114-1ff38a04-72c1-4515-ac1b-8cc2fa290a26.png)
# Установка  
![image](https://user-images.githubusercontent.com/1348639/224531576-02e6f106-8b74-445d-b0b2-c71892576bca.png)
![image](https://user-images.githubusercontent.com/1348639/224531617-9bf2896a-be45-478a-bef7-6a2bd29ed4da.png)
![image](https://user-images.githubusercontent.com/1348639/224531655-6564a7c9-3564-4e9b-b131-53a7e34c3161.png)
![image](https://user-images.githubusercontent.com/1348639/224532208-e08cda39-b677-46ac-9119-a5378426171c.png)
![image](https://user-images.githubusercontent.com/1348639/224532237-13c08607-f4af-405f-a353-dc9e6f2ca7a8.png)
Проверяем настройки сети, по которым в дальнейшем будем осуществлять настройку и задаём имя хоста  
![image](https://user-images.githubusercontent.com/1348639/224532352-36980833-89b1-4480-b139-63b831e83bc0.png)
![image](https://user-images.githubusercontent.com/1348639/224532368-5dfc8f57-03fe-4b60-be27-358a3746728c.png)
- По завершению установки, машина перезагрузится и мы попадём на экран входа в систему. На экране указан адрес, по которому нужно перейти используя веб-браузер.  
![image](https://user-images.githubusercontent.com/1348639/224532767-c00f23e6-4f3f-4185-9512-68074a2ef004.png)
- Для авторизации используем логин root, пароль заданный вами при установке.  
![image](https://user-images.githubusercontent.com/1348639/224533103-89f3dccf-2cf7-4776-9c0a-717a00601a52.png)
![image](https://user-images.githubusercontent.com/1348639/224533139-5857389b-87ae-484d-ac4c-f6520af0575c.png)
![image](https://user-images.githubusercontent.com/1348639/224533164-cb04c674-7619-40a0-bb58-69d7c844c825.png)

# Решение возникших проблем  
## После установки, по адресу в командной строке не удаётся перейти в панель управления.  
- Прежде всего необходимо проверить настройки сетевого интерфейса в программе виртуализации.  
![image](https://user-images.githubusercontent.com/1348639/224533371-d16a6549-cf37-45f8-949d-cb9cd9106b8f.png)
- Затем открываем окно виртуальной машины и вводим данные для авторизациию Логин: root, пароль: заданный вами при установке системы  
![image](https://user-images.githubusercontent.com/1348639/224533304-fa27d937-f2b8-49d7-bdb0-aa43c4fd0f42.png)
![image](https://user-images.githubusercontent.com/1348639/224533418-80683671-490f-42fd-91b6-14c5c628f8c2.png)
![image](https://user-images.githubusercontent.com/1348639/224533441-52c55a37-d33f-4067-9794-5b7ed4653fbd.png)
- Узнав валидный IP-адрес, пробуем вновь зайти на веб-интерфейс системы.  
![image](https://user-images.githubusercontent.com/1348639/224533476-5aad4201-aed1-4371-8696-666c72c9aee9.png)



