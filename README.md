# LR6

# Лабораторная работа №6

Певым шагом мы создаем копию репозитория https://github.com/Kurtyanik/LR6 в личном хранилище.

![1](https://user-images.githubusercontent.com/89647102/200087903-e42ac66a-0f71-4450-a918-4d0ecece26a6.jpg)

Затем настраиваем клиент git, вводим имя пользователя и email.
Комманды: git config --global user.name <username>; git config --global user.email <email>.

![2](https://user-images.githubusercontent.com/89647102/200087961-96f7b7fd-091a-4172-88f1-8b0d895282be.jpg)

Клонируем удалённый репозиторий на компьютер.
Комманда: git clone.

![3](https://user-images.githubusercontent.com/89647102/200087973-d85f4449-0bae-49f7-8dd0-d11e66fdfbc4.jpg)

Проверяем, что при клонировании репозитория, все файлы из удаленного репозитория перешли в локальный.
Команда: git pull.

![4](https://user-images.githubusercontent.com/89647102/200087992-8dd71d84-555f-4c37-9371-129da150c701.jpg)

Добавляем файл через интерфейс GitHub.
Нажимаем на кнопку Add file, затем на Create new file.

![5](https://user-images.githubusercontent.com/89647102/200088025-d1b98666-48d3-4bb4-b600-44313cd1fed2.jpg)

С помощью появившегося интерфейса вводим название файла и его содержимое.

![6](https://user-images.githubusercontent.com/89647102/200088031-f3646b6c-54e9-41b0-8da2-aef92bf9f72a.jpg)

Прописываем комментарий к коммиту и соответственно делаем сам коммит

![7](https://user-images.githubusercontent.com/89647102/200088038-0e8cfc4b-c406-468a-8eda-2e269028be03.jpg)

В итоге файл появляется в репозитории на GitHub

![8](https://user-images.githubusercontent.com/89647102/200088042-57f893fe-37d1-4542-af30-150ee127d628.jpg)

Поддтягиваем изменения с удаленного репозитория в локальный.
Комманда: git pull.

![9](https://user-images.githubusercontent.com/89647102/200088202-e1675d8a-0b82-41af-9dda-61d0e7d69a73.jpg)

Посмотрим коммиты веток
Коммиты ветки master. Комманда: git log.

![10](https://user-images.githubusercontent.com/89647102/200088205-42195fbc-144b-4a93-a73b-1317366faaad.jpg)

Переходим на вторую ветку branch1. Команда: git checkout branch1

![11](https://user-images.githubusercontent.com/89647102/200088208-f56fd4d4-6860-493b-bb3d-29cf360bbae2.jpg)

Коммиты ветки branch1. Комманда: git log.

![12](https://user-images.githubusercontent.com/89647102/200088220-feb98364-b866-4c30-a95e-2f4df48d80b9.jpg)

Подробно рассмотрим коммиты ветки branch1.
Комманда: git log -p.

![13_1](https://user-images.githubusercontent.com/89647102/200088233-2c9c69d8-ccc0-4bfc-9198-8e8651210c88.jpg)
![13_2](https://user-images.githubusercontent.com/89647102/200088240-01472dfc-ea02-4ba4-a2a7-28c63e1605af.jpg)

Возвращаемся обратно на ветку master.
Команда: git checkout master.

![14](https://user-images.githubusercontent.com/89647102/200088320-652c2376-6363-4c7b-984b-132d3c30ce30.jpg)

Выполняем слияние ветки branch1 в ветку master.
Комманда: git merge branch1.

![15](https://user-images.githubusercontent.com/89647102/200088323-ef2e04e6-971e-42a2-aeb2-2d26ee7577aa.jpg)

Разрешаем возникший конфликт: в теории конфликт возник из-за того, что файл mergefile.txt не отслеживается. Проверив это и убедившись, добавляем файл для отслеживания, составляем коммит.
Проверим, есть ли файлы, которые не отслеживаются. Команда: git status.

![16](https://user-images.githubusercontent.com/89647102/200088332-f346179b-92b6-4073-806e-101afc01eaa4.jpg)

Добавим файл для отслеживания. Команда: git add mergefile.txt.

![17](https://user-images.githubusercontent.com/89647102/200088335-33a97928-2cc2-4124-8c07-9e38c8796b1b.jpg)

Проверим, что больше не осталось неотслеживаемых файлов. Команда: git status.

![18](https://user-images.githubusercontent.com/89647102/200088340-c3e92c94-a92d-466f-b9d5-29c32966a076.jpg)

Создаем коммит. Команда: git commit -m "merge conflict of branch1->master resolved".

![19](https://user-images.githubusercontent.com/89647102/200088345-f954abc0-ce13-457c-b40d-bfc7548f7fc7.jpg)

Пушим (отправляем) наши локальные изменения в удаленный репозиторий.
Команды: git status; git push.

![20](https://user-images.githubusercontent.com/89647102/200088362-e23aa35e-ee28-4dfe-9d18-26ee1cca6846.jpg)

Удаляем (локально) побочную ветку после успешного слияния.
Удаляем ветку branch1 локально. Команда: git branch -d branch1.

![21](https://user-images.githubusercontent.com/89647102/200088370-12bebc8c-75c5-4339-8d0a-aa42e23371cd.jpg)

Проверяем, что локальная ветка удалена. Команда: git branch -a

![22](https://user-images.githubusercontent.com/89647102/200088457-bab0e944-9331-4974-8cdd-eba3023feab5.jpg)

Добавляем (папку и файлы) изменения и фиксируем их (коммитим). Каждому изменения приписываем комментарий.
Создаем папку и переходим в нее. Команды: mkdir changes; cd changes/.

![23](https://user-images.githubusercontent.com/89647102/200088468-6a5271b5-526d-4cc5-b5db-3040f105b596.jpg)

Создаем файл, соержащий в себе данные о папке. Команда: echo "package LR6.changes;" > package-info.java.

![24](https://user-images.githubusercontent.com/89647102/200088471-3bfc4764-14a0-4b7c-b2ad-4c7c5cb484b2.jpg)

Добавляем файл в отслеживаемые. Команда: git add package-info.java.

![25](https://user-images.githubusercontent.com/89647102/200088477-a9a287b9-4a7e-46d3-9c1e-87d189436876.jpg)

Создаем коммит. Команда: git commit -m "added new directory plus package-info".

![26](https://user-images.githubusercontent.com/89647102/200088480-fc49aa40-62ab-4cf9-9e0e-f7de05645002.jpg)

Создаем пустой файл. Команда: echo "" > empty.txt.

![27](https://user-images.githubusercontent.com/89647102/200088488-6ea160b3-768a-4040-bdbc-ab76e0cd3678.jpg)

Добавляем файл в отслеживаемые. Команда: git add empty.txt.

![28](https://user-images.githubusercontent.com/89647102/200088502-56a843d7-84bb-44f9-8a95-f3a62267de71.jpg)

Создаем коммит. Команда: git commit -m "empty.txt added"

![29](https://user-images.githubusercontent.com/89647102/200088504-9953acc8-f144-44b8-acd5-15024b38efa8.jpg)

Сделаем откат последнего коммита.
Найдем идентификатоор последнего коммита. Команда: git log.

![30](https://user-images.githubusercontent.com/89647102/200088507-160b37a6-c0b0-4b0c-adb7-1a380a34ced8.jpg)

Скопируем id коммита и откатим его. Команда: git revert.

![31](https://user-images.githubusercontent.com/89647102/200088513-6bb05777-64b7-4f28-9142-0e7a2304252c.jpg)
![32](https://user-images.githubusercontent.com/89647102/200088520-aa442614-9da6-41ce-992e-b682efd5b97b.jpg)
![33](https://user-images.githubusercontent.com/89647102/200088524-a9269628-38b0-4b4e-9e1b-a4b4084cc375.jpg)

Отправим (запушим) коммиты в удаленный репозиторий.
Проверка состояния контроля версий. Команда: git status.

![34](https://user-images.githubusercontent.com/89647102/200088539-af384b14-d7bf-4686-82d6-24e9a0995c7d.jpg)

Отправка коммитов. Команда: git push.

![35](https://user-images.githubusercontent.com/89647102/200088547-11d067fb-4d31-4970-90aa-14a5ba541d95.jpg)

Проверяем, что все запушили. Команда: git status.

![36](https://user-images.githubusercontent.com/89647102/200088600-64a2ce84-8a87-44f9-b6d2-b33f1f5083e5.jpg)

Создаем ветку для отчёта.
Создаем ветку report. Комманда: git branch report.

![37](https://user-images.githubusercontent.com/89647102/200088606-dcb51f01-0085-4a94-b632-7998c8063d6f.jpg)

Переходим на ветку report. Команда: git checkout report.

![38](https://user-images.githubusercontent.com/89647102/200088612-4f9ee58b-08df-4120-a9a4-b01fa7733edb.jpg)

Создаем пустой файл отчета — README.md. Команда: echo "" > READEME.md.

![39](https://user-images.githubusercontent.com/89647102/200088615-3e61f40a-47a4-4e8a-b068-694e800f3308.jpg)

Добавляем отчет в систему контроля версий. Команда: git add README.md.

![40](https://user-images.githubusercontent.com/89647102/200088623-85d1acc9-f6f8-41d2-b7c2-680cc0b82338.jpg)

Создаем коммит с пустым отчетом. Команда: git commit -m "added README.md empty report".

![41](https://user-images.githubusercontent.com/89647102/200088637-d6368400-1800-44eb-819e-0bb0c3659ae6.jpg)

Получаем итоговую историю операций в форматированном виде (сокращённый хэш - дата, имя автора : комментарий).
Комманда: git log --pretty=format:"%h - %ar, %an : %s".

![42](https://user-images.githubusercontent.com/89647102/200088647-28b013d4-a1ed-44a0-aeb7-7c62732f5628.jpg)

Оформляем отчёт в файле README.md. 
После редактирования отчета, его нужно будет сохранить и закоммитить git commit.
В конце работы необходимо будет запушить все локальные изменения в сетевое хранилище GitHub командой git push.

Все снимки экрана, используемые в этом отчете находятся в папке img.
