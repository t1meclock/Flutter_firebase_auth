# Практическая работа №8

### Тема: Работа с Firebase
### Цель работы: произвести первичную настройку Firebase во Flutter, реализовать анонимный вход, пользовательский вход, генерацию письма для регистрации на почту.

###
### Ход работы:
### Для начала работы необходимо настроить проект в Firebase и подключить его Flutter-проекту, в котором будет реализовано приложение. На картинке показан Firebase с подключенным проектом во Flutter.
![image](https://user-images.githubusercontent.com/99389490/221417356-c64b5e2a-b660-4dd1-9f1f-94dee5cd04a9.png)
###
### Для того, чтобы настроить дальнейшую авторизацию и регистрацию в приложении, необходимо перейти во вкладку "Authentication" в Firebase, где подключить метод входа "Email/Password".
![image](https://user-images.githubusercontent.com/99389490/221419840-46aeec7c-7456-4717-8d5c-2955a2f64206.png)
### 
### После во вкладке "Users" будут отображаться зарегистрированные пользователи.
### 
### Далее необходимо перейти к Flutter-проекту, где необходимо инициализоровать Firebase. Также в проекте сгенерируется файл "firebase_options.dart", в котором указаны данные подключенного Firebase-проекта. В файле "pubspec.yaml" необходимо указать такие dependencies как: 
  firebase_core: ^2.7.0
  firebase_auth: ^4.0.2
  email_validator: ^2.1.17
##
![image](https://user-images.githubusercontent.com/99389490/221417858-721a80fd-1ef6-416c-bd9f-a289dd6a341c.png)
![image](https://user-images.githubusercontent.com/99389490/221417944-4662cf3d-990f-45d1-89d2-5c840d621b71.png)
![image](https://user-images.githubusercontent.com/99389490/221418420-31321d4c-f48e-4859-b728-92b5acd4db9c.png)
###
### После необходимо перейти к реализации анонимного входа, регистрации и авторизации для пользователя. Анонимный вход в приложение производится сразу после запуска, что показывает главный экран.
![image](https://user-images.githubusercontent.com/99389490/221418152-66b78e4e-3b25-4df8-a758-4a5dc2260668.png)
###
### Код регистрации через Email и пароль и верификацией по Email. 
![image](https://user-images.githubusercontent.com/99389490/221419019-148e1216-1405-44e6-a104-a226a54917e0.png)
![image](https://user-images.githubusercontent.com/99389490/221419244-29267f02-f4ce-4680-b3d7-a8124fc861d2.png)
###
### Пример регистрации через Email и пароль с верификацией по Email. После верификации в приложении автоматически выполняется пользовательский вход, сигналом является желтоватая иконка пользователя.
![image](https://user-images.githubusercontent.com/99389490/221419162-32717b44-7fc6-4432-9f05-9c5668370986.png)
![image](https://user-images.githubusercontent.com/99389490/221419180-78277956-f3c2-4b32-bf9f-bf054076fefc.png)
![image](https://user-images.githubusercontent.com/99389490/221419283-64fd9970-959a-4359-9998-bc5248d57685.png)
![image](https://user-images.githubusercontent.com/99389490/221419291-63be2adf-b6e5-4c98-b22d-fb4e8c1d8f27.png)
![image](https://user-images.githubusercontent.com/99389490/221419319-c6eac05b-4ac0-492b-b565-31d33f5add40.png)
###
### Также можно увидеть отображение нового пользователя в Firebase.
![image](https://user-images.githubusercontent.com/99389490/221419542-2a0f1ffd-7375-4a4b-a632-b218d56c0476.png)
###
### Код реализации аккаунта пользователя с отображением почты и кнопкой "Выйти". После того, как будет нажата кнопка выхода, пользователь перенесется в анонимный вход в приложение.
![image](https://user-images.githubusercontent.com/99389490/221419470-901da375-09f9-4d30-897b-08c7d0c1a66a.png)
###
### Пример реализации аккаунта пользователя с отображением почты и кнопкой "Выйти".
![image](https://user-images.githubusercontent.com/99389490/221419903-c6aeddea-c1f0-4724-817b-f35b47272f72.png)
###
### Код реализации авторизации в приложении.
![image](https://user-images.githubusercontent.com/99389490/221420429-86699593-6a9d-4e64-bfb5-c7883938a0d8.png)
###
### Пример реализации авторизации в приложении.
![image](https://user-images.githubusercontent.com/99389490/221420489-52d3d108-a9c9-4c34-a5bb-f60055698e72.png)
![image](https://user-images.githubusercontent.com/99389490/221420498-91fe5e6e-f5cd-43ba-8caa-5453ee6798a9.png)
###
### Вывод: В данной практической работе была произведена первичная работа с Firebase. Были реализованы функции: анонимный вход, пользовательский вход, генерация письма для регистрации на почту.
