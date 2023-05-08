# 0x80a40401 ☠
Полезная информация по ошибке в Xbox: 0x80a40401 (служба недоступна) в России.

## Официальный ответ от Microsoft

Официального ответа от Microsoft **нет**. 

Всё, что пользователи, блогеры, каналы и т.п. пишут, это не является действительностью, это всего лишь догадки. 

Сама поддержка Microsoft отвечает всегда по-разному, в некоторых случаях они говорят, что им известна проблема и их тех. специалисты делают все возможное для устранения, в другому случае говорят "нам так жаль, но ваш регион действительно заблокирован, играйте оффлайн". Пример переписок [в конце страницы](#приколы-от-тех-поддержки-microsoft).

Текущие догадки от комьюнити:

- Блокировка серых консолей во всех странах.
- Технических сбой Microsoft.
- Виноваты российские провайдеры и их оборудование.

## Изменение DNS

Легенда для таблицы:
- ✅ - проверено лично и другими пользователями
- ⁉ - проверено другими пользователями, не проверено лично
- ❌ - не работает
- Интернет Beeline 100 mb/s

Основной|Дополнительный|Скорость|Статус
---|---|---|---
178.122.22.10|185.51.200.2|~45-75 mb/s|✅
185.51.200.2|-|~50-80 mb/s|✅
178.22.122.100|78.157.42.100|~40-70 mb/s|✅
78.157.42.100|8.8.8.8|~40-70 mb/s|✅
78.157.42.100 |78.157.42.101|~70-90 mb/s|⁉
27.22.122.100|-|-|⁉
212.220.116.30|-|-|⁉

- DNS лучше всего прописывать в роутере для домена `xsts.auth.xboxlive.com`, в дополнение ещё можно для `user.auth.xboxlive.com`.
- Не рекомендуется прописывать DNS для всего трафика (глобально). 
  - <details>
    <summary>Почему? Ответ от ChatGPT 🤖 (клик)</summary>

    Если вы пропишете один и тот же DNS-сервер для всех подключений на своем компьютере или сети, это может привести к следующим проблемам:

    - Неэффективное использование ресурсов: если все запросы на DNS будут направляться на один DNS-сервер, это может вызвать перегрузку и недостаток ресурсов этого сервера, что может замедлить работу вашей сети.

    - Ограниченная защита от атак: если вы используете только один DNS-сервер, то ваша сеть становится уязвимой к атакам на DNS-серверы. Если DNS-сервер, на который вы полагаетесь, будет атакован или скомпрометирован, то вся ваша сеть может стать уязвимой к атакам и краже данных.

    - Ограничение доступа к контенту: некоторые сайты могут блокироваться на уровне DNS. Если вы используете только один DNS-сервер, то может быть заблокирован доступ к тем сайтам, которые заблокированы на уровне DNS-сервера.

    - Ограниченная гибкость: использование только одного DNS-сервера может ограничить ваши возможности в настройке и управлении сетью, в том числе ограничить возможности настройки фильтров контента, защиты от вредоносного ПО и улучшения производительности сети.

    В целом, использование только одного DNS-сервера для всех подключений на вашей сети не является безопасным и может ограничить гибкость и производительность вашей сети. Рекомендуется использовать несколько DNS-серверов для обеспечения более надежной и гибкой работы сети.

    </details>

## Инструкции

- [Подброная и обновляемая инструкция по подмене IP через роутер с использованием Telnet.](https://2ds.ru/posts/xbox-live-80a40401a/)

  **В дополнение к инструкции:** 

  <details>
  <summary>Список известных IP адресов (клик)</summary>
  
  > **Note**
  > [Адреса использовать на свой страх и риск — что это за адреса и куда уходит запрос до конца не ясно.](https://habr.com/ru/news/733476/#comment_25524098)
  
  - `50.7.87.82`
  - `50.7.87.83`
  - `50.7.87.84`
  - `50.7.87.85`
  - `50.7.87.86`
  - `50.7.85.218`
  - `50.7.85.219`
  - `50.7.85.220`
  - `50.7.85.221`
  - `50.7.85.222`
  </details>
  
  Или получить IP для `xsts.auth.xboxlive.com` можно следующим образом:
  - Запустите через командную строку на ПК `nslookup`.
  - Вбейте домен `xsts.auth.xboxlive.com`, далее пробел и вбейте DNS через который хотите подключиться. Например `nslookup xsts.auth.xboxlive.com 185.51.200.2`.
  - Нажмите Enter и вы получите актуальные IP адрес. Например из примера выше будет адрес `50.7.85.220`.

- [Подробная инструкция по Telnet и `xsts.auth.xboxlive.com`](https://4pda.to/forum/index.php?showtopic=996985&st=30820#entry122634980)

- [Обзор сервиса Control D. Как обходить геоблокировку стримминговых сервисов](https://dtf.ru/u/67084-podpiska/1583518-obzor-servisa-control-d-kak-obhodit-geoblokirovku-strimmingovyh-servisov)

- [Mikrotik, как добавить DNS](https://4pda.to/forum/index.php?showtopic=996985&st=30800#entry122634526)

- [Инструкция по Telnet на роутере Asus RTN12 (возможно подойдет на все роутеры от Asus)](https://4pda.to/forum/index.php?showtopic=996985&st=31060#entry122650365)

## Полезные ссылки

> **Note**
>
> Блять! 🤬 Модераторы на 4pda почистили тему и некоторые ссылки теперь не открывают нужное сообщение.

- [Инструкция с VPN на fornex.com](https://4pda.to/forum/index.php?showtopic=996985&st=30880#entry122637403)
- [Как подключиться к сервисам ЕА, на примере Fifa Ultimate Team](https://4pda.to/forum/index.php?showtopic=996985&st=30860#entry122636246)
- [Дополнение к ЕА сервисам выше](https://4pda.to/forum/index.php?showtopic=996985&st=30860#entry122636299)
- [Пост со списком вариантов DNS](https://4pda.to/forum/index.php?showtopic=996985&st=30680#entry122631115)
- [Скрин с DNS в настройках роутера (EA сервисы работают)](https://4pda.to/forum/index.php?showtopic=996985&st=30900#entry122637969)
- [Уменьшение пинга при подмене IP адреса на примере `50.7.85.221`](https://4pda.to/forum/index.php?showtopic=996985&st=30820#entry122634976)
- [Еще один способ подмены DNS и IP адреса на Mikrotik и `adguard-dns.io`](https://4pda.to/forum/index.php?showtopic=996985&st=30600#entry122626683)
- [Ещё один пост про подмену IP адреса](https://4pda.to/forum/index.php?showtopic=996985&st=30660#entry122628671)
- [Подробности от майков без пруфов](https://4pda.to/forum/index.php?showtopic=996985&st=30820#entry122635306)
- [Дополнения на подробности от майков выше](https://4pda.to/forum/index.php?showtopic=996985&st=30820#entry122635428)
- [Controld - Польша, в консоли тоже Польша - все ок](https://4pda.to/forum/index.php?showtopic=996985&st=30960#entry122640212)

## Приколы от тех. поддержки Microsoft

<details>
  <summary>SMMщики Xbox Support в Твиттере дают разную информацию.</summary>
  <img src="https://user-images.githubusercontent.com/19103498/236703763-24ca4584-bf60-402d-9ab2-12e007ff86ed.PNG" alt="Alt text" title="Optional title">
</details>

## Обновления и обсуждения

Помоги в обновлении и дополнении информации на этой странице, сделай [Pull Request](https://github.com/chipslays/0x80a40401/pulls).

Больше полезной информации в разделе [Discussions](https://github.com/chipslays/0x80a40401/discussions).




