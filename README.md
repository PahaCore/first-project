# Практика - шпаргалки по командам 

## Настройка
```
git config --global user.name user
git config --global user.email user@mail.ru
```
## Посмотреть настройки git
```
git config --list
```
## Сделать папку репозиторием
```
git init
```
## Посмотреть в каком состоянии репозиторий
```
git status
```
## Подготовить к сохранению сразу все файлы
```
git add --all
```
## Добавить в репозиторий текущую папку со всеми файлами
```
git add .
```
## Сделать коммит
```
git commit -m "Описание коммита"
```
## Сокращённый лог
```
git log --oneline
```
## Проверить что ssh доступ работает
```
ssh -T git@github.com
```
## Привязать удалённый репозиторий к локальному
```
git remote add origin git@github.com:User/project.git
```
## Убедиться, что репозитории связаны
```
git remote -v
```
## Синхронизировать локальный и удалённый репозиторий
```
git push -u origin main
```
## Отправить изменения на удалённый репозиторий
```
git push
```
## Статусы

- Статусом untracked помечается файл, о существовании которого Git знает, но не следит за изменениями в нём. Этот статус — противоположность tracked, в который попадают все файлы, отслеживаемые Git.
- Файл переходит в статус staged после выполнения git add.
- Статус modified означает, что файл был изменён.
```mermaid
graph LR;
  untracked -- "git add" --> staged;
  staged    -- "git commit -m "описание коммита"" --> tracked/comitted;
```
### Большинство файлов в проектах «шагает» по следующему циклу: «изменён» → «добавлен в список на коммит» → «закоммичен» → «изменён» → и так далее.
