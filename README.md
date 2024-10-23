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
9. Создайте отдельную ветку `feature/add_reply` в репозитории.

10. Напишите новый метод для класса Welcomer: метод должен возвращать произвольную реплику, содержащую слово `hunter`.
11. Дополните тест для нового метода на поиск слова `hunter` в новой реплике.
12. Сделайте push всех изменений в новую ветку репозитория.
13. Убедитесь, что сборка самостоятельно запустилась, тесты прошли успешно.
14. Внесите изменения из произвольной ветки `feature/add_reply` в `master` через `Merge`.
15. Убедитесь, что нет собранного артефакта в сборке по ветке `master`.
16. Настройте конфигурацию так, чтобы она собирала `.jar` в артефакты сборки.
17. Проведите повторную сборку мастера, убедитесь, что сбора прошла успешно и артефакты собраны.
18. Проверьте, что конфигурация в репозитории содержит все настройки конфигурации из teamcity.
19. В ответе пришлите ссылку на репозиторий.
