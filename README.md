# repository
### 1. На локальном репозитории сделать ветки для Postman, Jmeter, CheckLists, Bag_Reports, SQL, Charles, Mobile_testing
    git branch Postman && git branch Jmeter && git branch Checklists && git branch Bug_Reports && git branch SQL && git branch Charles && git branch Mobile_testing
### 2. Запушить все ветки на внешний репозиторий
    git push -u origin --all
### 4. В ветке Bag_Reports сделать текстовый документ со структурой баг репорта
- Перейти в ветку:

        git checkout Bug_Reports
- Создать файл:

        vim bug_reports.txt
- Перейти в режим редактирования:

        i
- Написать структуру баг-репорта:

        id:
        summary:
        environment:
        precondisions:
        steps:
        expected result:
        actual result:
        priority:
        severity:
        assign:
- Выйти из режима редактирования:

        esc
- Выйти из редактора текста:

        :wq
### 5. Запушить структуру багрепорта на внешний репозиторий

        git add bug_reports.txt && git commit -m "add bug_reports.txt on branch Bag_Reports" && git push -u origin Bag_Reports

### 6. Вмержить ветку Bag_Reports в Main
- Перейти в ветку, в которую будем мержиться (Main):
  
        git checkout main

- Слить ветки:


        git merge Bug_Reports

### 7. Запушить main на внешний репозиторий
        git push origin main
### 8. В ветке CheckLists набросать структуру чек листа
- Перейти в ветку:

        git checkout CheckLists
- Создать файл:

        vim checklists.txt
- Перейти в режим редактирования:

        i
- Написать структуру чек-листа:

        id:
        module:
        submodule:
        checking:
        status:

- Выйти из режима редактирования:

        esc
- Выйти из редактора текста:

        :wq
### 9. Запушить структуру чек-листа на внешний репозиторий
        git add checklists.txt && git commit -m "add checklists.txt on branch Checklists" && git push -u origin CheckLists
### 10. На внешнем репозитории сделать Pull Request ветки CheckLists в main
- Находясь на внешнем репозитории, открыть Pull Request:
  
     |Compare and pull request|
     |------------------------|
- Создать Pull Request:
  
     |Create pull request|
     |-------------------|

- Смержить Pull Request:

     |Merge pull request|
     |------------------|

- Подтвердить слияние:

     |Confirm merge|
     |-------------|

### 11. Синхронизировать Внешнюю и Локальную ветки Main
        git fetch && git pull
