# Практическая работа №8

### Тема: Работа с Firebase
### Цель работы: произвести первичную настройку Firebase во Flutter, реализовать анонимный вход, пользовательский вход, генерацию письма для регистрации на почту.

###
### Ход работы:
### Для начала работы необходимо настроить проект в Firebase и подключить его Flutter-проекту, в котором будет реализовано приложение. На картинке показан Firebase с подключенным проектом во Flutter.
![image](https://user-images.githubusercontent.com/99389490/221417356-c64b5e2a-b660-4dd1-9f1f-94dee5cd04a9.png)
###
### Для того, чтобы настроить дальнейшую авторизацию и регистрацию в приложении, необходимо перейти во вкладку "Authentication" в Firebase, где подключить метод входа "Email/Password".
![image](https://user-images.githubusercontent.com/99389490/221417720-73f8269a-258b-4cc6-8de2-42c32aba771e.png)
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
### Код реализации аккаунта пользователя с отображением почты и кнопкой "Выход".
![image](https://user-images.githubusercontent.com/99389490/221419470-901da375-09f9-4d30-897b-08c7d0c1a66a.png)
###
### Также необходимо реализовать обновление пароля. Для этого понадобятся файлы "user.dart" и "app_user_controller.dart". Для обновления пароля был использован метод POST. После необходимо протестировать работоспособность авторизации в Thunder Client с помощью запроса "http://localhost:8888/user" и указанием параметров query "oldPassword" и "newPassword".
![image](https://user-images.githubusercontent.com/99389490/216462270-9cb01bb5-49dc-4755-960c-09df2fbea39a.png)
![image](https://user-images.githubusercontent.com/99389490/216462161-f9f8d19d-fd49-41db-8a58-a98bf95a9855.png)
###
### На рисунке ниже продемонстрированы данные, которые хранятся в БД.
![image](https://user-images.githubusercontent.com/99389490/216462366-e0f95cf2-3f6e-4228-81bc-c379d85d06df.png)
###
### Далее необходимо перейти к реализации создания заметки. Для этого понадобятся файлы "note.dart" и "app_note_controller". В сущности заметки хранятся элементы таблицы, такие как: число, описание, имя, категория, дата создания, также дата редактирования и логическое удаление. Для создания заметки были использован метод POST. После необходимо протестировать работоспособность авторизации в Thunder Client с помощью запроса "http://localhost:8888/notes?search=/b/". На рисунке будет указано, что заметка не найдена, так как поиск осуществляется не по категории, а по имени, поэтому правильным запросом в данной ситуации будет "http://localhost:8888/notes?search=aboba". Также существует запрос для вывода всех заметок "http://localhost:8888/notes" с методом GET.
![image](https://user-images.githubusercontent.com/99389490/216462726-4262c3fd-fcd1-49dc-87c4-0bbe753e19f6.png)
![image](https://user-images.githubusercontent.com/99389490/216462804-bbdf7874-04c1-4c5c-a2db-04584b46f2ed.png)
![image](https://user-images.githubusercontent.com/99389490/216463015-24050b99-fd4f-4cfe-bbac-b5e6c560f055.png)
###
### Далее необходимо перейти к реализации поиска заметок. Для этого понадобятся файлы "note.dart" и "app_note_controller". Для поиска заметки были использован метод GET. После необходимо протестировать работоспособность авторизации в Thunder Client с помощью запроса "http://localhost:8888/notes?search=/b/". На рисунке будет указано, что заметка не найдена, так как поиск осуществляется не по категории, а по имени. 
![image](https://user-images.githubusercontent.com/99389490/216463307-32bc8368-ffd4-41fb-826c-46f7b6a3f80b.png)
![image](https://user-images.githubusercontent.com/99389490/216463195-fdefadd5-ef40-4065-a128-dc8d6796a5a3.png)
![image](https://user-images.githubusercontent.com/99389490/216463223-ff232da5-8d56-4ff7-be9c-17dd08514823.png)
###
### Далее необходимо перейти к реализации удаления заметки. Для этого понадобятся файлы "note.dart" и "app_note_controller". Для удаления заметки были использован метод DELETE. После необходимо протестировать работоспособность авторизации в Thunder Client с помощью запроса "http://localhost:8888/notes/3".
![image](https://user-images.githubusercontent.com/99389490/216463463-d56b76d7-3a60-4cc9-a4fd-f7d2d75b2933.png)
![image](https://user-images.githubusercontent.com/99389490/216463514-802bbd9c-644a-4a1a-9ac0-ba139fc0a39b.png)
###
### Далее необходимо перейти к реализации восстановления заметки. Для этого понадобятся файлы "note.dart" и "app_note_controller". Для восстановления заметки понадобился метод GET. После необходимо протестировать работоспособность авторизации в Thunder Client с помощью запроса "http://localhost:8888/notes/5?restore" с использованием query-параметра "restore".
![image](https://user-images.githubusercontent.com/99389490/216463686-27eb4db6-bbef-4844-aa15-bb5bf08a45f8.png)
![image](https://user-images.githubusercontent.com/99389490/216463812-0f187246-bbe1-4235-b017-be766eefac25.png)
###
### После необходимо перейти к реализации логического удаления. Для этого понадобятся файлы "note.dart" и "app_note_controller". Для фильтрации используется метод GET. После необходимо протестировать работоспособность авторизации в Thunder Client с помощью запроса "http://localhost:8888/notes?deleted=0" с использованием query-параметра "deleted".
![image](https://user-images.githubusercontent.com/99389490/216463951-686286fb-e435-4d80-8306-dfc95801b9a1.png)
###
### В конце необходимо создать историю всех действий. В сущности истории хранятся элементы таблицы, такие как: id, действие, которое было произведено и дата редактирования. Для создания истории всех действий был использован метод GET. После необходимо протестировать работоспособность авторизации в Thunder Client с помощью запроса "http://localhost:8888/history".
![image](https://user-images.githubusercontent.com/99389490/216464062-7c963e30-e408-4923-b4b3-9f4ef60ee7f5.png)
![image](https://user-images.githubusercontent.com/99389490/216464150-6a959c46-9399-4f38-9680-4927f39978f2.png)
![image](https://user-images.githubusercontent.com/99389490/216464339-c093cdf5-e8ad-4280-9c6d-921b686bdea4.png)
###
### Ниже представлены все хранящиеся данные в БД.
![image](https://user-images.githubusercontent.com/99389490/216464555-dea17267-2da4-494c-a0b5-bea4f9e1efe0.png)
![image](https://user-images.githubusercontent.com/99389490/216464590-9528b782-69ab-4136-9bd8-19e479a227ea.png)
### Вывод: В данной практической работе была произведена первичная работа с Conduit. Были реализованы функции: регистрация, авторизация, RefreshToken, Вывод данных пользователя, редактирование данных пользователя, изменение пароля пользователя, CRUD действия по теме, поиск, фильтрация, логическое удаление и восстановление, история действий.
