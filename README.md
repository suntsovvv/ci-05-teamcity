# Домашнее задание к занятию 11 «Teamcity»
## Основная часть

1. Создайте новый проект в teamcity на основе fork.
![image](https://github.com/user-attachments/assets/7cb1adf7-9f3e-4de1-aefd-1adb5603d8ce)
![image](https://github.com/user-attachments/assets/543015dc-32f5-4067-9817-be1d3a2726bb)
2. Сделайте autodetect конфигурации.
![image](https://github.com/user-attachments/assets/5d0139bf-3173-4f91-a5f9-06d4e6332291)
3. Сохраните необходимые шаги, запустите первую сборку master.
![image](https://github.com/user-attachments/assets/332922e5-c507-4ce1-9755-f56bc5a76c73)
4. Поменяйте условия сборки: если сборка по ветке `master`, то должен происходит `mvn clean deploy`, иначе `mvn clean test`.
![image](https://github.com/user-attachments/assets/39ea92ef-3c77-4d78-8b78-6e67231ea7a0)
5. Для deploy будет необходимо загрузить [settings.xml](./teamcity/settings.xml) в набор конфигураций maven у teamcity, предварительно записав туда креды для подключения к nexus.
6. В pom.xml необходимо поменять ссылки на репозиторий и nexus.
7. Запустите сборку по master, убедитесь, что всё прошло успешно и артефакт появился в nexus.
![image](https://github.com/user-attachments/assets/9c063712-d3b6-41c9-8914-20c2ead1505d)
![image](https://github.com/user-attachments/assets/2a26a5ab-694a-442e-9382-1c84b2f5c8b0)
8. Мигрируйте `build configuration` в репозиторий.
![image](https://github.com/user-attachments/assets/5b08fd78-238d-44fe-99e3-3a3f7a648d86)
![image](https://github.com/user-attachments/assets/e2eb14b1-2a84-48b2-866b-854bef916586)

10. Создайте отдельную ветку `feature/add_reply` в репозитории.
11. Напишите новый метод для класса Welcomer: метод должен возвращать произвольную реплику, содержащую слово `hunter`.
12. Дополните тест для нового метода на поиск слова `hunter` в новой реплике.
13. Сделайте push всех изменений в новую ветку репозитория.
14. Убедитесь, что сборка самостоятельно запустилась, тесты прошли успешно.
![image](https://github.com/user-attachments/assets/db11f413-efaf-4877-aa0c-1454d353f27c)
15. Внесите изменения из произвольной ветки `feature/add_reply` в `master` через `Merge`.
17. Убедитесь, что нет собранного артефакта в сборке по ветке `master`.
![image](https://github.com/user-attachments/assets/e7b8577d-470d-4250-aac6-3eb9542af8ca)

18. Настройте конфигурацию так, чтобы она собирала `.jar` в артефакты сборки.
![image](https://github.com/user-attachments/assets/5ddbbf39-3343-45f2-b3ab-4b1da8c27773)

19. Проведите повторную сборку мастера, убедитесь, что сбора прошла успешно и артефакты собраны.
![image](https://github.com/user-attachments/assets/dab84db8-142f-4f74-a757-bd6523aadb79)

20. Проверьте, что конфигурация в репозитории содержит все настройки конфигурации из teamcity.
![image](https://github.com/user-attachments/assets/848eab5d-3ec5-4b01-9e30-52bcf51c5ae2)

21. В ответе пришлите ссылку на репозиторий.
https://github.com/suntsovvv/example-teamcity
