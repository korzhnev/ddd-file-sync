## Синхронизация двух каталогов source и destination

### Цель репозитория
Показать преимущества использования правильных абстракций на примере простой задачи.

### Требования
* если файл существует в источнике, но отсутствует в месте назначения, копируем его.
* если файл существует в источнике, но имеет другое имя, чем в месте назначения, переименуем файл назначения в соответствующий.
* если файл существует в месте назначения, но не существует в источнике, удалим его.
* если в каталогах содержатся подкаталоги, игноририуем их. 

### Реализация
* В папке internal/dirty содержится неправильная реализация.
** Высокоуровневый код связан с низкоуровневыми деталями, что усложняет жизнь.
** Слишком громозкие тесты. Которых, помимо всего прочего недостаточно для покрытия всех кейсов.
** Код сложно расширять
** Тесты связаны с i/o, что не делает их быстрыми 
* В папке internal/clear - рекомендуемая.