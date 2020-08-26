# django-to-heroku-deploy-example

https://www.youtube.com/watch?v=GMbVzl_aLxM

## Heroku ##
Config Vars

https://stackoverflow.com/questions/36665889/collectstatic-error-while-deploying-django-app-to-heroku

DISABLE_COLLECTSTATIC = 1

### Links ###

https://medium.com/@BennettGarner/deploying-django-to-heroku-procfile-static-root-other-pitfalls-e7ab8b2ba33b

## Manual ##

### addUser

http://127.0.0.1:8000/addUser

Создает нового пользователя и возвращает его токен.

Пример ответа:

```json
{"token": "d31f02a8-c217-4e04-bee2-226ad90bf598"}
```

### startStream

[http://127.0.0.1:8000/startStream?authToken=xyz&streamName=foobar](http://127.0.0.1:8000/startStream?authToken=xyz&streamName=foobar)

Создает у пользователя стрим с заданным именем и возвращает инфу о стриме.

Пример ответа:

```json
{
	"name": "foobar",
	"id": "eb0cbd72-45e2-410e-a720-a7fca73f8fc5",
	"key": "ld95-zflg-812b-kiya",
	"playback_id": "u6qbm7bfdkqhdnaw"
}
```

Видеопоток со стрима льется в:

```https://fra-cdn.livepeer.com/hls/<playbackId>/index.m3u8```

### getStreams

http://127.0.0.1:8000/getStreams
Получить список активных стримов

Пример ответа:

```json
[
	{"name": "foobar",
	"playback_id": "u6qbm7bfdkqhdnaw"}
]
```
