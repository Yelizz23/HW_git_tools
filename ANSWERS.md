### 1. Найдите полный хеш и комментарий коммита, хеш которого начинается на `aefea`:
    git show aefea 

    commit aefead2207ef7e2aa5dc81a34aedf0cad4c32545
    commit message: Update CHANGELOG.md

### 2. Какому тегу соответствует коммит `85024d3`?
    git show 85024d3

    Коммит `85024d3` соответствует тегу v0.12.23

### 3. Сколько родителей у коммита `b8d720`? Напишите их хеши.
    git show --pretty=format:' %P' b8d720
    
    56cd7859e0 
    9ea88f22fc

### 4. Перечислите хеши и комментарии всех коммитов которые были сделаны между тегами  v0.12.23 и v0.12.24:
    git log  v0.12.23..v0.12.24  --oneline

    33ff1c03bb (tag: v0.12.24) v0.12.24 
    b14b74c493 [Website] vmc provider links 
    3f235065b9 Update CHANGELOG.md 
    6ae64e247b registry: Fix panic when server is unreachable 
    5c619ca1ba website: Remove links to the getting started guide's old location 
    06275647e2 Update CHANGELOG.md 
    d5f9411f51 command: Fix bug when using terraform login on Windows 
    4b6d06cc5d Update CHANGELOG.md 
    dd01a35078 Update CHANGELOG.md 
    225466bc3e Cleanup after 

### 5. Найдите коммит в котором была создана функция func providerSource, ее определение в коде выглядит так func providerSource(...) (вместо троеточего перечислены аргументы):
    git log -S'func providerSource' --oneline

    5af1e6234a main: Honor explicit provider_installation CLI config when present 
    8c928e8358 main: Consult local directories as potential mirrors of providers

### 6. Кто автор функции synchronizedWriters?
    git log -S'func synchronizedWriters' --pretty=format:'%h - %an %ae'
    git show 5ac311e2a9
    git show bdfea50cc8

    Автором функции synchronizedWriters является Martin Atkins <mart@degeneration.co.uk>


