# gitflow-example




GitFlow:

1) СОздать репозиторий и склонировать его на компьютер
git clone https://github.com/serhiibublyk88/gitflow-example.git

2) Cоздать ветку develop и перейти на неее
git branch develop
git checkout develop

3) Отправляем ветку на гитхаб
git push origin develop

4) Далее создаються ветки в develop:

git branch feature/main-page - главная страница

git branch feature/about-page - страница о компании (git checkout -b feature/about-page) -сразу новая ветка и перекл на нее

git branch feature/modals - модальные окна

git branch feature/global-styles - модальные стили

потом все мерджится в develop

5)Создание ветки release/0.1.0 от develop - новые фичи не добавляються - только исправление багов
git checkout -b release/0.1.0

6) Когда ветка elease/0.1.0 закончена - она мержится в девелоп и майнили мастер и потом удаляеться
 git checkout main
  git merge release/0.1.0

  git checkout develop
  git merge release/0.1.0

  git branch -d release/0.1.0 - удаление

  git checkout main
  git push origin main

  7) Если в ветке main или master  обнаруживаеться ошибка, тосоздаеться hotfix ветка
  8git) когда робота на hotfix заверщается, то ее нужно мержить в девелоп ив мейн
  git checkout -b hotfix/about-main-page
  изменение
  git add .
   git commit -m"add title on the title"
   git push origin hotfix/about-main-page

   git checkout main
   git merge hotfix/about-main-page
   git push origin main

    git checkout develop
   git merge hotfix/about-main-page
   git push origin develop


git branch -d hotfix/about-main-page