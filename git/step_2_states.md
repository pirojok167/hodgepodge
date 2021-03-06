## Состояния
#### В гите есть следующие состояния файлов:

1. *Индексированные* - готовые к коммиту.
2. *Изменённые* - файлы с изменениями, но не проиндексированные.
3. *Игнорированные* - файлы, которые игнорируются для коммитов.

#### Состояние файлов можно посмотреть с помощью команды:
```git
git status
```

## Индексирование
#### Добавление файла в отслеживаемые (индексируемые):
```git
git add <filename>
``` 
Эта команда фиксирует состояние для коммита.

#### Удаление файла из индексируемых:
```git
git reset HEAD hello.html
```

## Изменение рабочего каталога
#### При изменении файла он автоматически попадает в изменённые.

> Если изменения были проиндексированы, и файл снова был изменён, то он окажется в двух списках, 
> но при коммите сохранятся только проиндексированные изменения. 
>
> Чтобы сохранить новые изменения, нужно опять проиндексировать файл `git add <filename>`.
>
> Таким образом можно решать какие изменения в какой коммит попадут.

#### Удаление файла из изменённых, то есть удаление изменений:
```git
git checkout <filename>
```

## Игнорирование файлов
Все файлы в *.gitignore* не будут никогда проиндексированы.

Примеры паттернов по [ссылке](https://www.atlassian.com/git/tutorials/saving-changes/gitignore#git-ignore-patterns).