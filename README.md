# Black Computing

Портфолио медиахудожника и геймдизайнера Аркадия Кукина — **[blackcomputing.art](https://blackcomputing.art)**

*Portfolio of Arkady Kukin, media artist and game designer — [blackcomputing.art](https://blackcomputing.art)*

Игры, инсталляции, выставки и исследования. Чёрные плитки с голубыми рамками, между которыми живёт пиксельная экосистема; имя в шапке нарисовано шейдером. Две версии: русская и английская.

*Games, installations, exhibitions and research. Black tiles with cyan hairline borders, a pixel ecosystem living between them, and a shader-drawn name in the header. Available in Russian and English.*

## Что здесь лежит

Репозиторий — это готовый статический сайт, который публикуется через GitHub Pages. Сборки и серверной части нет.

| Файл или папка | Что это |
|---|---|
| `index.html` | главная страница и все разделы (маршрутизация по хэшу: `#bio`, `#portfolio`, `#p-<id>`) |
| `content.json` | весь контент и раскладка плиток: единственный источник данных |
| `p/<id>/` | страницы-заглушки проектов с превью для соцсетей, ведут на `/#p-<id>` |
| `media/` | короткие локальные видео: `<имя>.mp4` (с кнопками) или `<имя>.webm` (тихий луп) и постер `<имя>.jpg`; подключаются полем `clips` проекта в `content.json` |
| `img/`, `files/`, `fonts/` | картинки, PDF (портфолио, CV, био), локальные шрифты |
| `editor.html` | визуальный редактор сайта (см. ниже) |
| `sitemap.xml`, `robots.txt`, `404.html`, `CNAME` | служебные файлы |

Внешних запросов страница не делает: шрифты и картинки свои, аналитики и трекеров нет.

## Редактор

`editor.html` — один файл, который работает в Chrome или Edge и правит эту папку напрямую через File System Access API: тексты, картинки, плитки проектов и их раскладку. Он пересобирает `index.html`, страницы проектов и `sitemap.xml`, после чего остаётся сделать commit и push.

1. Откройте `editor.html` в Chrome → «Открыть папку сайта» → выберите папку клона репозитория.
2. Правьте плитки на холсте, нажмите «Сохранить» (Ctrl+S).
3. Commit → Push, через минуту-две сайт обновится.

## Публикация

GitHub Pages: ветка `main`, папка `/ (root)`, свой домен задан файлом `CNAME`. DNS у регистратора: четыре A-записи на `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` и CNAME для `www`.

## Авторские права

© Аркадий Кукин. Все права защищены. Работы, изображения, тексты и документы на этом сайте принадлежат автору и не подлежат использованию без разрешения. Исходный код страницы можно читать и изучать; для повторного использования свяжитесь с автором.

*© Arkady Kukin. All rights reserved. The artworks, images, texts and documents on this site belong to the author and may not be used without permission. The page code may be read and studied; contact the author for any reuse.*
