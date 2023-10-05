# ПРОЧИТАЙМЕНЯ

~~Зачеркнули~~

## Основные команды которые я запомнил:

- _pwd_ - вывод пути текущей директории
- _cd_ - смена директории по типу (cd dir1/dir2, cd .. - возврат на уровень выше cd ~ - переход в домашнюю папку)
- _ls_ - вывод содержимого папки _ls -a_ - вывод со скрытыми файлами
- _touch_ - создание нового файла **путь/путь/имя файла**
- _mkdir_ - создание директории **mkdir имя**; _mkdir -p_ - создание структуры папок **d/d1/d2/d3**
- _cp_ - копирование что что что.... куда **cp a.txt b.txt c.html home/dir1**
- _mv_ - перенос имя*файла имя*папки **mv a.txt mydir/newdir**
- _cat_ - чтение файла имя_файла

## Хеши, логи, HEAD

- _Хеш_ - уникальный идентификатор коммита, зная его можно получить всю информацию о коммите, авторе и закоммиченных файлах.
- _Логи_ - история коммитов. **git log** - выведет историю всех коммитов, начиная с самого последнего. **Git log --oneline** -выводит все коммиты в сокращенном виде.
- ~~БОШКА~~ _HEAD_ - при вызове **git log** выводится HEAD -> master, файл _HEAD_ указывает на последний сделанный коммит, он находится в папке **.git** и содержит _ссылку_ на служебный файл вида **refs/heads/master** в этом файле содержится _хеш_ последнего элемента

## Статусы файлов

### Основные статусы:

_*untracked/tracked* git понятия не имеет о файле/файл известен моему git и ранее уже что-то делал с ним -*staged* файл подготовлен и ждет коммита
__modified_ файл подготовлен к коммиту, но после подготовки был изменен \*_нет ничего из вышеперечисленного_ это значит, что все файлы закоммичены и изменения в файлах соответсвтуют изменениям в коммитах

###Короче:

```mermaid
  graph TD;
      UNTRACKED-->STAGED_TRACKED;
      STAGED_TRACKED-->TRACKED;
      TRACKED-->MODIFIED;
      MODIFIED-->STAGED_TRACKED;
```
