# Возвращаем YouTube в строй

## Дискуссии насчёт замедления

Ниже будут обсуждения, в которых могут появляться новые способы обхода блокировок

- [Обсуждение на ntc.party](https://ntc.party/t/%D0%BE%D0%B1%D1%81%D1%83%D0%B6%D0%B4%D0%B5%D0%BD%D0%B8%D0%B5-%D0%B7%D0%B0%D0%BC%D0%B5%D0%B4%D0%BB%D0%B5%D0%BD%D0%B8%D0%B5-youtube-%D0%B2-%D1%80%D0%BE%D1%81%D1%81%D0%B8%D0%B8/8074)
- [Ветка yt-dlp](https://github.com/yt-dlp/yt-dlp/issues/10443) / Полезна для скачивания с YouTube

## Обход замедления

### Не забывайте про VPN

Хорошие VPN и альтернативы им можно найти на [vpnlove.me](https://storage.googleapis.com/vpnlove/index.html#)

### Использование QUIC в браузере

> [!WARNING]
> Некоторые способы обхода могут не работать при включённом QUIC (+Kyber)

#### В Chormium браузерах (Chrome, Яндекс Браузер и так далее)

- Переходим по `chrome://flags/#enable-quic`
- В поиске пишем `QUIC`, если автоматом не перешло
- Включаем протокол

#### В Firefox и его форках

Обычно, там включён QUIC по умолчанию, но

- Переходим по `about:config`
- Ищем `network.http.http3.enable`
- Убеждаемся, что HTTP3 (QUIC) включён

### Бегаем от DPI

[Комментарий от ValdikSS, конкретно насчёт YouTube](https://github.com/yt-dlp/yt-dlp/issues/10443#issuecomment-2248940967)

- Windows
  - [GoodbyeDPI](https://github.com/ValdikSS/GoodbyeDPI)
  - [byedpi](https://github.com/hufrea/byedpi)
  - [zapret](https://github.com/bol-van/zapret)
- Linux
  - [youtubeUnblock](https://github.com/Waujito/youtubeUnblock)
  - [zapret](https://github.com/bol-van/zapret)
  - [byedpi](https://github.com/hufrea/byedpi)

## Как вернуть аватарки

### С помощью [Piped Proxy](https://github.com/TeamPiped/piped-proxy)

#### Шаг 1

Скачайте расширение [Redirector](https://github.com/einaregilsson/Redirector)

- [Firefox](https://addons.mozilla.org/ru/firefox/addon/redirector/)
- [Chrome](https://chrome.google.com/webstore/detail/redirector/ocgpenflpmgnfapjedencafcfakcekcd)
- Opera - [Установите это и скачайте версию для](https://addons.opera.com/en/extensions/details/install-chrome-extensions/) [Chrome](https://chrome.google.com/webstore/detail/redirector/ocgpenflpmgnfapjedencafcfakcekcd)

#### Шаг 2

Скачайте файл Redirector.json

- [Тут](https://raw.githubusercontent.com/NoPlagiarism/UnblockYouTubeRU/master/Redirector.json)
- [Или Тут](https://github.com/NoPlagiarism/UnblockYouTubeRU/releases/download/V0.0.1/Redirector.json)

#### Шаг 3

- Зайдите в настройки Redirector (Иконка -> Edit Redirects)
- Нажмите Import
- Выберите файл, скачанный во 2-ом шаге

#### Аватарки всё равно не грузятся

Выберите вместо стандартного домена [любой другой](https://github.com/NoPlagiarism/instances-list/tree/master/instances/youtube/piped-proxy#readme).

---
---

## А почему это происходит?

### РКН vs Google

С начала существования РосКомНадзора, гос. машина часто сходила с ума. В пример можно привести ту же [блокировку Telegram](http://tass.ru/ekonomika/5129977), которая сильно навредила интернету в тот момент. ([1](https://www.gazeta.ru/business/2018/04/20/11722969.shtml) [2](https://usher2.club/articles/google-ban))

Борьба государства с Google идёт давно ([1](https://roskomsvoboda.org/en/post/rkn-protokol-google-242) [2](https://roskomsvoboda.org/en/post/amersocseti-ignotyat-rkn) [3](https://www.bbc.com/russian/news-57231773)), но обострилась с началом войны. ([1](https://www.forbes.ru/tekhnologii/459521-roskomnadzor-obvinil-youtube-v-dejstviah-terroristiceskogo-haraktera) [2](https://www.rbc.ru/rbcfreenews/669645689a7947fa4ca5cf2b) [3](https://www.interfax.ru/russia/937201) [4](https://www.interfax.ru/russia/937201) [5](https://www.reuters.com/technology/google-pauses-all-ad-sales-russia-2022-03-04))

И теперь всё обострилось до замедления

### Реакция

> «Деградация» YouTube — вынужденный шаг, направленный не против российских пользователей, а против администрации иностранного ресурса, который по-прежнему считает, что может безнаказанно нарушать и игнорировать наше законодательство
>
> [:copyright: Депутат ГосДумы Александр Хинштейн](https://t.me/Hinshtein/7276)
---
> Докладываю: администрации Ютуба всё это глубоко до фонаря. Они из-за этого ТОЧНО не пострадают ни разу. А вот российские пользователи - очень даже. И зрители и те, кто используют Ютуб, как главный рабочий инструмент. Смотреть будет труднее, работать тоже.
> Так что эта мера направлена по факту именно против российских пользователей, чтобы там не врал депутат Хинштейн.
> Рутуб и пр. отечественные площадки работают гораздо, в разы хуже ютуба и в смысле удобства пользования, и в смысле удобства труда.
> Когда наши слуги народа ради народа очередной раз испортят народу жизнь, хоть какие-то стимулы для и так, видит бог, более чем скромных успехов развития Рутуба и пр., исчезнут окончательно. Конкурировать будет не с кем. И не за чем. 
> А вы, то есть мы, будем жрать, что дают, т.к. альтернатив никаких не будет. Впрочем, это уже не в первый раз.
>
> Касательно антироссийской позиции Ютуба.
> Ютуб в настоящий момент почти безальтернативная мега-сми-сеть. Титаническая библиотека со всемирным охватом самой разнообразной информации с 20 летним стажем накопления. Ни ВК ни рутуб даже рядом не стояли с этой библиотекой в плане наполнения. Нет такого количества лекций, документальных фильмов и пр, причем на самых разных языках.
> Что антироссийского, скажем, в лекции доктора Тобиаса Кепвелла об английских доспехах XV века?
>
> [:copyright: Клим Жуков, видеоблогер-историк](https://t.me/klimzhukoff/3902)
---
> Но давайте про актуальное, про альтернативу ютубу - ВКОНТАКТЕ.
> БЕЗ ШУТОК, сегодня этот сервис работает ужаснейшим образом. Тормозить и тупить стал очень сильно. Вы точно по ютубу ударили?
> Или на радостях от новостей про замедление ютуба администрация ВК вообще забила на работу?
>
> [:copyright: Евгений "BadComedian" Баженов, видеоблогер](https://t.me/TheBadComedian/1324)

---
---

Данный шаг направлен не только против администрации YouTube, они от этого пострадают меньше, чем любой пользователь рунета, провайдер и так далее.

Чтобы этот бред начал подходить к концу, должен прекратиться и [другой бред](https://wiki2.org/ru/Вторжение_России_на_Украину_(2022))

Берегите себя, своих близких и свой рассудок
