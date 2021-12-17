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

##Домашнее задание к занятию «2.4. Инструменты Git»
 1. Найдите полный хеш и комментарий коммита, хеш которого начинается на aefea.

Ответ: Получено командой: git show aefea
* полный хеш: aefead2207ef7e2aa5dc81a34aedf0cad4c32545
* комментарий коммита: Update CHANGELOG.md

 2. Какому тегу соответствует коммит 85024d3?

Ответ: Получено командой: git show 85024d3
* тег: tag: v0.12.23)

 3. Сколько родителей у коммита b8d720? Напишите их хеши.

Ответ: Получено командой: git show --pretty=format:'%P' b8d720
* 56cd7859e05c36c06b56d013b55a252d0bb7e158
* 9ea88f22fc6269854151c571162c5bcf958bee2b

 4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами v0.12.23 и v0.12.24.

Ответ: Получено командой: git log v0.12.23..v0.12.24 --oneline
* 33ff1c03b (tag: v0.12.24) v0.12.24
* b14b74c49 [Website] vmc provider links
* 3f235065b Update CHANGELOG.md
* 6ae64e247 registry: Fix panic when server is unreachable
* 5c619ca1b website: Remove links to the getting started guide's old location
* 06275647e Update CHANGELOG.md
* d5f9411f5 command: Fix bug when using terraform login on Windows
* 4b6d06cc5 Update CHANGELOG.md
* dd01a3507 Update CHANGELOG.md
* 225466bc3 Cleanup after v0.12.23 release

 5. Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит 
так func providerSource(...) (вместо троеточия перечислены аргументы).

Ответ: Получено командой: git log -S'func providerSource' --pretty=medium
* получено два коммита первый от 2 апреля, второй от 21 апреля. 
Соответственно функция создана в самом раннем коммите с хешем 8c928e83589d90a031f811fae52a81be7153e82f

 6. Найдите все коммиты в которых была изменена функция globalPluginDirs.

Ответ: Получено командой: git log -G 'globalPluginDirs' --oneline
* 22a2580e9 main: Use the new cliconfig package credentials source
* 35a058fb3 main: configure credentials from the CLI config file
* c0b176109 prevent log output during init
* 8364383c3 Push plugin discovery down into command package

 7. Кто автор функции synchronizedWriters?

Ответ: Получено командой: git log -S'synchronizedWriters' --pretty=format:'%h / %as / %s / %an <%ae>'
* Полученно несколько результатов изменения данной функции, впервые (2017-05-03) функция (synchronizedWriters) была создана в коммите (hash: 5ac311e2a, сообщение: 'main: synchronize writes to VT100-faker on Windows') автором Martin Atkins <mart@degeneration.co.uk>
 

