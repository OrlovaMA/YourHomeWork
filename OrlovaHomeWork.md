# Базовые команды Git

* *git init* - команда инициализирующая репозиторий в текущей директории;

* *git add* - команда, добавляющая текущую версию файла к отслеживанию (готовит к коммиту);

* *git commit -m "Message"* - команда фиксирующая изменения;
  > Например: *git commit -m "git add info added"*

* *git log* - посмотреть список изменений;

* *git status* - проверить текущее состояние репозитория;

* *git diff* - для просмотра изменений между сохраненными версиями;

* *git branch* - команда, отображающая все существующие ветки и на какой ветке сейчас находимся;

* *git branch BranchName* - команда для создания новой ветки с именем "BranchName";

* *git branch -d BranchName* - команда для удаления ветки с именем BranchName;

* *git merge BranchName* - команда для слияния ветки BranchName с веткой master; выполняется из позиции в ветке master;

# Команды для работы с удалёнными репозиториями на GitHub

## Команда для копирования удалённого репозитория в локальное хранилище

* *git clone* - команда копирует репозиторий на компьютер в открытую сейчас папку;

Варианты исполнения:

1. В строке терминала набрать команду *git clone ссылка_на_репозиторий*.
2. В проводнике выбрать *клонировать репозиторий* --> в всплывающей вверху строке написать ссылку на репозиторий --> выбрать папку на компьютере, куда сохранить репозиторий;

После клонирования удалённого репозитория, не требуется делать *git init*!

## Команды для копирования локального репозитория в свой аккаунт на GitHub

 * __*git push*__

1. В своём аккаунте создать новый репозиторий: New repository
2. В терминале выполнить следующие 3 команды (для связи локального репозитория и удалённого):
* *git remote add origin ссылка_на_новый_репозиторий* - показать гиту путь, куда загружать локальный репозиторий;
* *git branch -M master* - обозначить ветку, которая будет основной;
* *git push -u origin master* - запушить локальный репозиторий в удалённый.

Далее, после сохранения локальных изменений и отправки их на этот же удалённый репозиторий, использовать команду: 

* *git push* - отправка закоммиченных изменений в удалённый репозиторий

## Команда для копирования чужого удалённого репозитория в свой аккаунт на GitHub

* *Fork* - создание копии чужого удалённого репозитория в своём аккаунте. При этом, моя копия это будет как ветка для оригинального репозитория.

Пройти по ссылке в удалённый репозиторий --> Справа вверху нажать на Fork --> Creat forc. 
После этого в моём аккаунте появится этот репозиторий.

Далее, с помощью команды 
* *git clone*, 

копировать на компьютер для локальной работы с репозиторием.

## Команды для синхронизации изменений между локальным и своим удалённым репозиторием

* *git push* - отправка изменений из локального в удалённый репозиторий;

* *git pull* - "скачивание" изменений, произведённых в удалённом репозитории, в локальный;

## Команды для внесения изменений на чужом удалённом репозитории

* *pull request* - запрос на внесение изменений

Порядок действий:

1. В своём аккаунте на GitHub зайти в нужный репозиторий на вкладку __Pull requests__.
2. Нажать кнопку __New pull request__.
3. Проверить, что слияние возможно, и нажать кнопку __Creat pull request__.
4. В поле __Write__ можно написать комментарий и ещё раз нажать на __Creat pull request__.

## Команды для работы с ветками 

* *git push --set-upstream origin NameBranch* - отправить ветку на свой удалённый репозиторий