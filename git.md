.gitignore служит для указания в нём файлов и папок, которые необходимо скрыть от системы контроля версий git.

Как правило, скрывают файлы или папки, которые автоматически генерируют своё содержимое, либо имеют конфигурационные параметры, которые могут различаться у тех, кто совместно работает над проектом.

Приведу простой пример: у вас имеется файл " /config/db.php", в нём прописаны параметры подключения к БД, причём на вашей локальной машине и на сервере эти параметры будут разниться.
А если эти файлы различны, то git будет при каждом pull/push ругаться на то, что имеется конфликт.

Другой пример: если вы используете NetBeans и настройки своего проекта храните непосредственно в папке с проектом, то вам необходимо закрыть от git`а директорию "nbproject", чтобы другие участники вашего проекта не страдали от того, что вы случайно закомитили эту директорию.