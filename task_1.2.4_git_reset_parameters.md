# Отличия между git reset --soft --mixed --hard

## git reset --soft B
Перемещает HEAD на указанынй коммит B. Изменения из последнего коммита (например, С) будут в индексе. Если выполнить git commit, то получим коммит идентичный последнему (С).

## git reset --mixed B
Перемещает HEAD на указанынй коммит B. Но, в отличие от **--soft** параметра, изменения из последнего коммита (например, С) не будут в индексе (not staged). Чтобы их закоммитить, нужно сначала выполнить git add и только потом git commit.

## git reset --hard B
Перемещает HEAD на указанынй коммит B. Но, в отличие от **--mixed** параметра, изменения из последнего коммита (например, С) будут удалены и файлы в репозитории будут соответствовать коммиту B.