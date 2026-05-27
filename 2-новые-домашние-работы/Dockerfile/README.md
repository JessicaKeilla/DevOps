<img width="898" height="628" alt="image" src="https://github.com/user-attachments/assets/1a1b37eb-ff16-4ffa-976f-0f8d1cf24709" />

<img width="1106" height="560" alt="image" src="https://github.com/user-attachments/assets/0a459210-0133-41dc-9857-4dd56005062a" />

---

### This project contains a Docker image with:

- Веб-сервер Nginx
- База данных MySQL
- Объединены в одном контейнере (в образовательных целях)

Образ демонстрирует использование:
FROM, RUN, CMD, COPY, ADD, ENV, WORKDIR, VOLUME, USER, EXPOSE, MAINTAINER

Команда сборки:
docker build -t chiponde_jk_image_2026-05-27 .

Для просмотра слоев:
docker history chiponde_jk_image_2026-05-27

