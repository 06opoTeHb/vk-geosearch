# vk-geosearch
[![Platform](https://img.shields.io/badge/Platform-Linux-brightgreen.svg)](https://shields.io/)
[![Python](https://img.shields.io/badge/Python-3.6-brightgreen.svg)](https://shields.io/)

**Поиск фотографий по геометкам в социальной сети [vk.com](https://vk.com)**

![Demo Photo](http://i.piccy.info/i9/07277ceee30da11d077c3a4f00f18544/1556797628/82386/1315967/screen1.jpg)

![Result Photo](http://i.piccy.info/i9/4c686f00c3a6123586868e37e981eadd/1556797717/169127/1315967/screen2.jpg)

## Зависимости

* proxybroker
* requests


## Установка


```
git clone https://github.com/yevgen2020/vk-geosearch.git
pip3 install proxybroker requests
cd vk-geosearch
chmod +x *
```

## Использование

Для поиска фото в VK нужен сервисный ключ доступа или токен. Создайте  [Standalone-приложение.](https://vk.com/editapp?act=create) Перейдите в настройки и в поле состояние установите "Приложение включено и видно всем". Сохраните изменения. Скопируйте ваш сервисный ключ доступа, откройте в редакторе **search.py** и измените ключ на свой (можно использовать токен вместо ключа).

![Key Photo](http://i.piccy.info/i9/c892cacfa39cdc3e06151b36385cae26/1556800215/29459/1315967/screen3.png)

Специально для тех у кого заблокирован доступ к вк :ukraine: есть поддержка прокси. Результаты сохраняются в файл с названием 'текущий timestamp'.html Фото не загружаются на локальную машину, а тянутся с сервера при открытии html с результатми. На странице фото будут в максимально возможном качестве и соответственно весить будут немало, учтите это когда задаете временной интервал. Кликнув по фото открывается страница владельца в новой вкладке. Парсятся только изображения с личных страниц пользователей (в том числе с удаленных и заблокированых), фото с групп отфильтровываются иначе большая часть поисковой выдачи будет состоять из ногтей, ресничек, депиляций и т.д.

### P.S.

```./proxy.py``` поднимет на **127.0.0.1:8888** локальный прокси-сервер который будет держать в пуле 5 HTTPS proxy . Подробнее можно узнать [здесь](https://github.com/constverum/ProxyBroker)






