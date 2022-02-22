 1) На локальном репозитории сделать ветки для:
- Postman
- Jmeter
- CheckLists
- Bug Reports
- SQL
- Charles
- Mobile testing
  == `git branch Postman`; `git branch Jmeter`; `git branch CheckLists`; `git branch Bug_Reports`; `git branch SQL`; `git branch Charles`; `git branch Mobile_testing`
2) Запушить все ветки на внешний репозиторий 
  == `git push -u origin --all` 
3) В ветке Bug Reports сделать текстовый документ со структурой баг репорта
  == `git checkout Bug_reports`; `cat > bug_reports.txt`
  ID
Summary
Project
Version
Severity
Priority
Condition
Steps to reproduce
Actual result
Expected result
Addition
= CTRL+C
4) Запушить структуру багрепорта на внешний репозиторий 
  == `git add` .; `git commit -m "add bug_reports.txt"`; `git push`
5) Вмержить ветку Bug Reports в Main
  == `git checkout main`; `git merge Bug_reports`
6) Запушить main на внешний репозиторий
  == `git add` . ; `git commit -m "merge Bug_reports to main`" ; `git push`
7) В ветке CheckLists набросать структуру чек листа
  == `git checkout CheckLists`; `cat > checklist.txt`
  ID
  Title
  Precondition
  Steps to reproduce
  Expected result
  Status
  == Ctrl+C 
8) Запушить структуру на внешний репозиторий
  == `git add .`; `git commit -m "add checklist.txt`; `git push`
9) На внешнем репозитории сделать Pull Request ветки CheckLists в main
  == Перейти на веб версию github в нужный репозиторий, изменить ветку на `Checklists`, `нажать Pull Request`
10) Синхронизировать Внешнюю и Локальную ветки Main
  == `git checkout main`; `git pull`