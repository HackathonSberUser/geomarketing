# "Географический анализ для размещения сферы услуг"

 
## Введение

Мы приглашаем участников хакатона разработать геомаркетинговое приложение/сервис. Задача команд заключается в создании интерфейса, который позволит пользователю получить отчет с рекомендациями по размещению объекта бизнеса из сферы услуг. Участники должны будут использовать данные по навигации, точки интереса в городе и расположение конкурентов. Основной целью является создание понятного и эффективного решения, способного помочь проанализировать городское пространство перед открытием бизнеса. 


## Описание целевого сервиса/приложения

 - предоставляет интерфейс управления подбора коммерческих объявлений по их атрибутам

 - обеспечивает поиск объявлений с учетом критериев близости/удаленности других объектов к потенциальному месту размещения

 
## Про используемые данные

Источники данных можно поделить на 4 категории: предоставлемые организаторами обязательные для использования, предоставляемые организаторами необязательные для использования, сторонние (III) и проверочные (IV). Подробное описание структуры атрибутов и ссылки см. в "Описание наборов данных"

Обязательным для использования от организаторов являются следующие наборы данных:
 - потенциальные места (объявления коммерческой аренды) для возможного размещения бизнеса
 - POI (набор о различных точках города от бизнес-центров, больниц, кинотеатров до кофейн, парикмахерских или даже знаменитых мостов)

Для реализации сервиса понадобятся данные о расстояния между объектами их можно определить с помощью:
 - граф от организаторов (для участников с опытом работы с гис пакетами)
 - сторонние сервисы 2GIS, Yandex, Google

Для визуализации результатов потребуется нанести объекты на карту с помощью:
 - карты от организаторов
 - сторонних сервисов и технологий (Leaflet, GeoServer, 2GIS API и пр)

Проверочные данные очень похожи на обязательные для использования от организаторов, но в них содержатся дополнительные данные
 - POI (набор о различных точках города от бизнес-центров, больниц, кинотеатров до кофейн, парикмахерских или даже знаменитых мостов)


## Описание наборов данных
 
### Объявления REALTY

./data/realty.csv

Атибуты:
- unid (идентифкатор),
- point_x (долгота),
- point_y (широта),
- main_type (тип права),
- segment_type (сегмент),
- entity_name (категория),
- total_area (площадь),
- floor (этаж),
- lease_price (цена),
- additional_info (ссылка),
- source_info (сайт-источник),
- address (адрес),
- update_date (дата)

  ### Точки интереса POI
  ./data/poi.csv

   Атрибуты:
  - name (имя),
  - address_comment (комментарий адреса),
  - lat (широт),
  - lon (долгота),
  - rubrics (рубрики)
 
  ### Карта Петербурга
  ./data/SPB_MAP (архив из двух файлов - внутри изображение и координаты углов)
