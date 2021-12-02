#devops-netology
DevOps course from netology

В корневом .gitignore добавлены правила игнорирования файлов и каталогов IDE (PyCharm)

В /teraform/.gitignore игнорируются:

* директория .terraform и ее вложенные файлы
* файлы с расширением .tfstate, 
* файлы начинающиеся и оканчивающиеся на любые символы, содержащие в центре .tfstate.
* файл crash.log
* все файлы с расширением .tfvars
* файлы (override.tf, override.tf.json)
* файлы оканчивающиеся на: _override.tf, _override.tf.json
* конфигурационные файлы (.terraformrc, terraform.rc)


