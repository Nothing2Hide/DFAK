---
layout: page
title: "Устранение последствий DdoS-атак"
author: RaReNet
language: ru
summary: "Многие независимые журналисты, новостные сайты и блогеры сталкиваются с тем, что их голоса оказываются заглушены вследствие того, что их сайт перестал работать или был подменен/захвачен. Во многих случаях это безобидная проблема, вызывающая лишь чувство разочарования, но иногда это вызвано намеренной атакой типа «отказ в обслуживании» (DDoS) или захватом сайта. Этот раздел поможет вам осуществить базовую диагностику потенциальных проблем. Если ваш сайт подвергся атаке DDoS, то вам предлагается немедленно предпринять шаги, описанные ниже."
date: 2015-08
redirect_from: /ru/DDoSMitigation/
permalink: /ru/УстранениепоследствийDdoS-атак/
parent: /ru/
---

# Устранение последствий DdoS-атак

Многие независимые журналисты, новостные сайты и блогеры сталкиваются с тем, что их голоса оказываются заглушены вследствие того, что их сайт перестал работать или был подменен/захвачен. Во многих случаях это безобидная проблема, вызывающая лишь чувство разочарования, но иногда это вызвано намеренной атакой типа «отказ в обслуживании» (DDoS) или захватом сайта. Этот раздел поможет вам осуществить базовую диагностику потенциальных проблем. Если ваш сайт подвергся атаке DDoS, то вам предлагается немедленно предпринять шаги, описанные ниже.

В целом важно осознавать, что ваш сайт может оказаться неработоспособным по множеству причин. Наиболее часто это происходит при допущении ошибок в программировании или из-за технических проблем у компании, предоставляющей хостинг для вашего сайта. Иногда, например, изменения в законодательстве могут вызвать отключение вашего сайта. Определение проблемы и поиск возможных путей её решения может стать весьма обременительным занятием, если у вас нет опыта работы с хостингом. Таким образом, если есть такая возможность, вам стоит обратиться к надёжному человеку, способному помочь в решении проблем с сайтом (ваш веб-мастер, люди, которые помогали вам с настройкой вашего сайта, ваши сотрудники, если таковые имеются, компания, предоставляющая хостинг вашему сайту).

После изучения стандартных причин неполадок **вам стоит связаться как с вашим веб-мастером, так и с компанией, предоставляющей хостинг**! Информация о проблеме, с которой вы столкнулись, возможно, ещё не была опубликована на сайте хостинг-провайдера; возможно, проблема носит временный характер или же компания даже не знает о её существовании. Хорошие отношения с провайдером имеют важное значение: изъясняйтесь чётко и вежливо, сообщите о результатах своих изысканий, используя приведенные ниже вопросы, чтобы помочь провайдеру быстро устранить проблему.

## Для начала ответьте на эти простые вопросы:

### Основная информация

- Кто разработал ваш сайт? Могут ли они помочь?
- Кто является вашим хостинг-провайдером? Это компания, предоставляющая сервер, на котором располагается ваш сайт. Если вы не знаете этого, вы можете использовать следующий или аналогичный [инструмент](http://www.whoishostingthis.com/).
- Есть ли у вас подробный лог-файл учётной записи этого хостинг-провайдера?
- Где вы приобрели доменное имя для своего сайта? В некоторых случаях эта компания и предоставляет хостинг для сайта.
- Есть ли у вас подробный лог-файл сервиса доменных имён? Если нет, то получение этих данных является первым шагом к восстановлению работоспособности сайта.
- Кто ещё имеет доступ к указанным выше данным?

### Информация по диагностике

Различные обстоятельства могут стать причиной того, что ваш сайт перестал работать. От проблем сети до политики компании: это могут быть проблемы с хостингом, блокирование учётной записи, сбой в программном обеспечении, захват/подмена сайта или проблемы с производительностью хостинг-сервера. Следующий раздел описывает виды проблем и способы их диагностики.

- **Ваш хостинг работает, но сайт недоступен?**
    1. Проверьте его с помощью [сервиса](http://www.isup.me/).
        - Возможно, ваш сайт работает, но в следствие проблем с сетью вы не можете получить к нему доступ.
            - Возможно, проблема заключается в вашем **подключении к сети или в блокировке**.
            - Также это может означать, что ваша учётная запись была деактивирована. **Вы получали сообщения от вашего хостинг-провайдера?**
                - Вас могли отключить из-за неоплаты счёта, нарушения закона, нарушения авторских прав либо по каким-то другим причинам.
                - Эта проблема относится к разряду **политики компании**. Для начала убедитесь в том, что ваши счета оплачиваются своевременно и у вас нет непогашенной задолженности перед хостинг-провайдером или компанией, продавшей вам доменное имя. Если в сообщении говорится о нарушении закона, то [ресурсы сайта EFF](https://www.eff.org/issues/bloggers/legal/liability/IP), хоть и сфокусированы на законах о защите авторских прав в США, но всё-таки являются неплохим источником дополнительной информации.
        - **Ваш сайт вообще не загружается?** Возможно, возникли проблемы у хостинг-провайдера, в этом случае вы сталкиваетесь с **проблемой, связанной с хостингом**.
            - Вы можете зайти на сайт вашего хостинг-провайдера? Это не раздел администратора вашего сайта, а сайт той организации, которая предоставляет вам хостинг. Постарайтесь найти их блог, где публикуются актуальные проблемы (например, status.dreamhost.com) и ознакомьтесь с ним. Также поищите обсуждение проблем данного провайдера другими пользователями на twitter.com.
                - Простой запрос типа «[название компании] лежит/тормозит» зачастую может дать информацию о том, встречается ли проблема у других пользователей.
    2. **Можете ли вы зайти на другие сайты с аналогичным контентом?**
        - Попробуйте зайти на сайты, имеющие аналогичную тематику. Также для получения доступа к своему сайту попробуйте использовать [Tor](https://www.torproject.org/projects/gettor.html) или [Psiphon](https://psiphon.ca/products.php). Если это поможет, то вы столкнулись с **проблемой блокировки**. В этом случае ваш сайт доступен для пользователей в других странах, но подвергся цензуре в вашей стране.
    3. **Получаете ли вы сообщения об ошибке?**
        - Это может свидетельствовать **о сбое программного обеспечения**. Вы должны вспомнить все недавние изменения, внесённые вами или вашей командой, и связаться с вашим веб-мастером.
            - Отправьте ему снимок экрана с сообщением об ошибке и ссылку на страницу, с которой у вас возникли проблемы. Таким образом, вы поможете ему быстрее выяснить причину возникшей проблемы.
            - Вы также можете воспользоваться поиском в интернете, указав текст ошибки, чтобы узнать, насколько сложно её исправить.
    4. **Загружается сайт, который явно вам не принадлежит? Получаете предупреждение вашего браузера о вредоносности вашего собственного сайта?**
        - Эта проблема может быть связана с **deface - типом хакерской атаки, при которой главная страница сайта заменяется на другую.**. Ознакомьтесь с шагами, указанными ниже; вам потребуется работать совместно с вашим хостинг-провайдером. Также ознакомьтесь с разделом «Взлом учётных записей».
    5. **Ваш сайт загружается прерывисто или необычно медленно?**
        - Ваш сайт может быть перегружен большим количеством и высокой частотой запросов, что свидетельствует о **проблеме производительности**. Это может быть «хорошо», если связано с тем, что ваш сайт становиться всё более популярным. В этом случае требуется лишь некоторое повышение производительности сайта, которое позволит обеспечить его корректную работу при большем количестве посещений.
            - Ознакомьтесь с аналитикой сайта на предмет долгосрочной модели роста аудитории.
            - Свяжитесь с веб-мастером или хостинг-провайдером и попросите совета. Множество популярных платформ управления контентом сайта (Joomla, Wordpress, Drupal и др.) предлагают плагины для организации локального кэширования сайта и интеграции в сети доставки и дистрибуции контента (CDN), что позволяет значительно повысить производительность сайта и его устойчивость. Многие из представленных ниже способов также могут решить проблемы, связанные с производительностью.

## Первые шаги по исправлению проблемы

### Если вы столкнулись с атакой типа «отказ в обслуживании» (DDoS)

Если вышеуказанные способы диагностики не помогли определить характер возникшей проблемы (или вы столкнулись с **нехваткой производительности** хостинг-сервера), то ваш сайт мог стать жертвой **атаки типа «отказ в обслуживании»**, когда злоумышленник / злоумышленники пытаются открывать веб-страницы вашего сайта много раз подряд с большой частотой (используя специальные автоматизированные средства), тем самым вытесняя обычных пользователей вашего сайта. Иногда только один «атакующий» проводит подобную атаку. Обычно это не причиняет особого вреда вашему сайту за исключением тех случаев, когда вы платите за трафик. Однако более распространена атака типа «распределённый отказ в обслуживании» («Distributed» denial of Service - DDoS), когда злоумышленник использует для атаки тысячи компьютеров, заражённых вредоносным программным обеспечением и находящихся под его контролем.

- Шаг 1: Свяжитесь с надёжным человеком, который может помочь вам с вашим сайтом (ваш веб-мастер, люди, помогавшие с настройкой вашего сайта, ваши сотрудники, если таковые имеются, компания, предоставляющая хостинг вашему сайту).
- Шаг 2: Свяжитесь с компанией, продавшей вам доменное имя (например, EasyDNS, [Network Solutions](http://www.networksolutions.com/support/how-to-manage-advanced-dns-records/), [GoDaddy](http://support.godaddy.com/help/article/680/managing-dns-for-your-domain-names) и измените настройку параметра «Time to Live» или TTL на 1 час. Это позволит намного быстрее настроить переадресацию вашего сайта в случае атаки (значение по умолчанию 72 часа, или 3 дня). Эта опция, как правило, находится в «Дополнительных» свойствах вашего домена, иногда в разделе SVR или «Service records».
- Шаг 3: Переместите ваш сайт на сервис защиты от DDoS-атак. [полный список](https://github.com/OpenInternet/MyWebsiteIsDown/blob/master/MyWebsiteIsDown.md#mitigation-services). Некоторые ресурсы из этого списка:
    - [Deflect.ca](https://deflect.ca/)
    - [Проект Shield компании Google](https://projectshield.withgoogle.com/en/)
    - [Проект Galileo от CloudFlare](https://www.cloudflare.com/galileo)
- Шаг 4: Как только вы получите контроль над своим сайтом, пересмотрите свои потребности и либо выберите размещение сайта на сервере защищённого хостинг-провайдера, либо продолжайте пользоваться услугами по защите от DdoS-атак.

### Если ваш сайт захвачен и подменён злоумышленниками

- Шаг 1: Удостоверьтесь в том, что ваша проблема является результатом злонамеренного захвата вашего сайта. К сожалению, распространённой, но законной практикой является выкуп доменных имён, продление владения которыми не было вовремя оплачено. Это позволяет «захватчикам» воспользоваться трафиком сайта в рекламных целях. Очень важно вовремя совершать платежи за доменное имя вашего сайта.
- Шаг 2: Если ваш сайт был взломан, для начала восстановите контроль над своей учётной записью администратора сайта и смените пароль. См. раздел «Взлом учётных записей».
- Шаг 3: Сделайте резервную копию взломанного сайта, чтобы в последствии использовать её для расследования этого происшествия.
- Шаг 4: Временно отключите свой сайт, используйте простую страничку-уведомление или страничку с указанием того, что на сайте ведутся работы.
- Шаг 5: Определите, каким образом ваш сайт был взломан. В этом вам, возможно, сможет помочь ваш хостинг-провайдер. Как правило, проблемой является использование устаревших разделов вашего сайта, на которых запущены пользовательские скрипты/инструменты, использование устаревших CMS (систем управления контентом), а также программирование с допущением брешей в безопасности сайта.
- Шаг 6: Восстановите оригинальный сайт из резервной копии. Если ни у вас, ни у хостинг-провайдера нет резервной копии сайта, то вам, возможно, придётся заново его разрабатывать! Также имейте в виду, что если резервные копии находятся только у хостинг-провайдера, то злоумышленник может удалить их при получении контроля над вашим сайтом!
- Шаг 7: Переместите сайт на сервис защиты от DdoS-атак или на сервер защищённого хостинг-провайдера. Deflect.ca может позволить вам обезопасить сайт от сетевых атак. CloudFlare также может отразить множество распространённых атак. Защищённые хостинг-провайдеры, например, VirtualRoad/Qurium, делают все возможное, чтобы обнаружить и предотвратить подобные атаки.

## Не останавливайтесь на этом! Следуйте инструкциям, приведённым ниже.

**Не дожидайтесь, когда вас атакуют!** Все перечисленные ниже сервисы быстро окажут вам помощь в момент атаки либо после неё, но вы и сами можете защитить себя ещё до того, как произойдёт атака! Это позволит снизить стоимость обслуживания вашего сайта, снижая потребляемый трафик и помогая вашему сайту оставаться в работоспособном состоянии во время атаки. Если вас атакуют, может понадобиться до трёх дней, чтобы сеть интернет «нашла» ваш сайт, перемещённый на новый защищённый адрес. Так что почти в каждом случае будет гораздо **лучше подготовиться заранее, и начать стоит прямо сейчас**.

1. **Защищённые хостинг-провайдеры** требуют полного перемещения сайта на их серверы – вам придётся сменить хостинг-провайдера. Большинство из них поможет вам «переехать». Преимущества использования защищённых хостинг-провайдеров состоят в том, что они зачастую предоставляют также и множество других услуг в дополнение к защите от DdoS-атак. Обратной стороной медали может стать стоимость их услуг (в зависимости от того, сколько вы платите в настоящее время) и предоставление контроля над своим сайтом, для чего вы должны полностью доверять хостинг-провайдеру.
    - Аргументы «за»:
        - предоставляется один сервис, удовлетворяющий большинству, если не всем требованиям вашего сайта;
        - предоставляется защита от DdoS-атак, хакеров и спамеров;
        - часто в вашем распоряжении оказывается и множество других услуг, консультации и даже ограниченная юридическая поддержка в некоторых случаях;
        - часто предоставляется исчерпывающая помощь со стороны команды поддержки.Provides one central service for most, if not     - Аргументы «против»:
        - вы должны разместить ваш сайт на хостинге этого сервиса;
        - вы должны доверить этому сервису управление вашим сайтом и защиту ваших прав;
        - часто такие сервисы весьма дорогостоящи (но вам больше не придётся платить другим сервисам хостинга/DNS!).

2. **Сервисы защиты от DDoS-атак** позволяют размещать ваш сайт на сервере любого хостинг-провайдера и всего лишь изменяют способ того, как пользователи находят его в интернете и получают к нему доступ – в основном это гораздо легче настроить. Такие сервисы имеют серверы по всему миру, которые, по сути, являются буфером, защищающим ваш сайт, поглащающим или просто игнорирующим вредоносный трафик. Они создают «зеркальные» копии вашего сайта и постоянно их обновляют. Эти сервисы легко настроить, у вас будет абсолютный контроль над вашим сайтом и настройками хостинга. Сложностью, связанной с проксируемыми сервисами, является то, что в случае сложных сайтов иногда могут возникать проблемы со входом в систему пользователей неадминистраторов и с отображением сложных интерактивных страниц сайта (с использованием технологии Java script). Пожалуйста, обсудите это со своим веб-мастером и провайдером проксируемого сервиса, так как большинство проблем можно решить.
    - Аргументы «за»:
        - низкая стоимость (иногда с наличием бесплатного тарифа);
        - быстрая и лёгкая настройка;
        - не придётся менять существующего хостинг-провайдера;
        - вы можете перейти на другой сервис либо прекратить пользоваться подобными сервисами в любое время.
    - Аргументы «против»:
        - ограниченные возможности службы поддержки;
        - ориентация в основном только на предотвращение DdoS-атак – совсем не обязательно, что они смогут помочь с предотвращением атак вредоносного программного обеспечения или спамеров;
        - шифрованные данные (трафик SSL) будут кратковременно расшифрованы и затем перешифрованы прокси-сервером для их передачи на ваш сайт.

3. Выберите подходящего поставщика услуг. Вам должно быть удобно с ним работать. В большей степени это относится к доверию, но также и к бизнес-модели: они оказывают платные услуги? Есть ли у них бесплатные планы обслуживания, получают ли пользователи бесплатных планов меньшую поддержку, чем пользователи, оплачивающие услуги? Финансируется ли этот провайдер государством? Лучше всего сразу получить как можно больше информации о поставщиках услуг для того, чтобы избежать неприятных сюрпризов впоследствии.

### По каждому провайдеру задайте себе следующие вопросы:

- Как компания/организация структурирована и за счёт чего поддерживает своё существование? Какие типы проверок и отчетности выполняются, если таковые имеются?
- Примите во внимание информацию о том, в какой стране/ в каких странах компания зарегистрирована и, соответственно, каким юридическим нормам и запросам со стороны правоохранительных органов должна подчиняться.
- Какие данные регистрируются в лог-файлах и какое время они хранятся?
- Есть ли касающиеся вас ограничения, например, тематические разновидности контента, неприемлемые для данного сервиса?
- Есть ли ограничения, касающиеся стран, в которых провайдер может предоставлять сервис?
- Принимается ли предпочитаемая вами форма оплаты? Можете ли вы позволить себе регулярную оплату услуг?
- Безопасное общение. Вы должны иметь возможность безопасного подключения к сайту и конфиденциальной коммуникации с поставщиком услуг.
- Поддерживает ли сервис двухфакторную аутентификацию, чтобы повысить уровень безопасности административного доступа? Это и другие правила безопасности могут позволить вам снизить риск других возможных атак на ваш веб-сайт.
- Какие типы постоянной поддержки входят в состав приобретаемого вами пакета услуг? Существуют ли дополнительные виды расходов, связанные с поддержкой или вы получите достаточный уровень поддержки даже при использовании "бесплатного" пакета?
- Можете ли вы потестировать услуги с помощью временного сайта, прежде чем полностью перенести ваш веб-сайт?

### Вопросы по работе хостируемых сервисов

- Предоставляет ли провайдер услуги поддержки при переносе вашего сайта на его платформу?
- Предоставляемые им услуги аналогичны или лучше тех, которые в настоящее время входят в ваш хостинг пакет (как минимум относительно используемых вами инструментов/сервисов)? Основные элементы, которые надо проверить:
    - панель управления, например, cPanel;
    - учетные записи эл. почты (сколько, ограничения, доступ через SMTP, IMAP);
    - базы данных (сколько, типы, доступ);
    - удаленный доступ через SFTP/SSH;
    - поддержка языков программирования (PHP, Perl, Ruby, cgi-bin доступ и др.) или системы управления контентом (Drupal, Joomla, Wordpress и т.д.), которую использует ваш сайт.

### Вопросы по работе проксируемых сервисов:

- Если вы пользуетесь SSL (HTTPS, или безопасный веб-трафик), спросите, как они работают с SSL. В некоторых конфигурациях самым простым вариантом может быть предоставление своего секретного SSL-ключа. В этом случае вы должны действительно доверять поставщику услуг, так как он может "подделать" ваш сайт (на самом деле именно это вы и просите их сделать, предоставляя ваш прокси!).
- Узнайте, как осуществляется работа с административными / редакционными логинами и страницами.
- Обсудите интерактивные части вашего веб-сайта (пользователи, которые авторизовываются и комментируют, административные и редакционные требования, сложные интерактивные страницы / javascript / анимации). Разные прокси-сервисы по-разному работают с этими элементами веб-сайта; вы должны будете потестировать их, прежде чем окончательно перейти на использование сервиса.

### Конкретные примеры сервисов по предотвращению атак

Конкретные сервисы по предотвращению атак [подробно описаны на сайте](https://github.com/OpenInternet/MyWebsiteIsDown/blob/master/MyWebsiteIsDown_RU.md#Сервисы-защиты-от-ddos-атак). Имейте в виду, что указанный там список неполон, существует большое количество подобных сервисов. Однако приведенные в списке сервисы являются достойными примерами, так как используются многими представителями независимых СМИ, защитниками прав человека и обществами, борющимися за свободу слова. В рамках этого руководства рекомендуем вам обратить внимание на следующие варианты:

- Сервисы по предоставлению защищённого хостинга:
    - [Qurium (бывш. Virtual Road)](https://www.qurium.org/)
    - [The Positive Internet Company](http://www.positive-internet.com/services/vip-hosting)
    - [Greenhost](https://greenhost.net/)

- Проксируемые решения защиты от DDoS-атак:
    - [Deflect.ca](https://deflect.ca/)
    - [Проект Shield от компании Google](https://projectshield.withgoogle.com/en/)
    - [Проект Galileo от CloudFlare](https://www.cloudflare.com/galileo)

## Дополнительные меры предосторожности от хакерских атак

Даже если вы не подвергались DdoS-атаке, это руководство предлагает вам проделать определённые шаги, чтобы подготовиться к ней, в надежде на полное предотвращение перебоев в работе вашего сайта. Перейдите сразу к разделу [Как реагировать на DoS атаку](https://github.com/OpenInternet/MyWebsiteIsDown/blob/master/MyWebsiteIsDown_RU.md#Как-реагировать-на-dos-атаку) и ознакомьтесь с наиболее распространёнными решениями, которые вы можете внедрить сейчас, ещё до атаки. В разделе «Полезная информация» вы можете ознакомиться с руководствами по сохранению работоспособности вашего сайта.

- **Резервные копии**: Всегда полезно убедиться в наличии резервных копий (которые вы храните в месте, отличном от места размещения вашего сайта!). Множество хостинг-провайдеров и веб-платформ предлагают эту услугу, но лучше всего иметь дополнительные копии, сохранённые на личных носителях.
- **Обновляйтесь**: Если вы используете систему управления контентом сайта (CMS), такую как WordPress или Drupal, убедитесь, что программное обеспечение вашего сайта актуально. В особенности это касается обновлений, связанных с безопасностью. Если вы используете какое-либо другое программное обеспечение, рассмотрите возможность перехода на систему CMS, которая регулярно обновляется.
- **Мониторинг**: Существует множество сервисов, которые на постоянной основе проверяют доступность вашего сайта и присылают вам сообщение по электронной почте или СМС в случае, если сайт перестаёт отвечать на запросы. [Эта статья Mahsable](http://mashable.com/2010/04/09/free-uptime-monitoring/) перечисляет десять наиболее популярных сервисов. Имейте в виду, что адрес электронной почты или телефон, который вы используете для мониторинга, будет напрямую связан с управлением проверяемого сайта.

## Расследуйте

Если вы стали жертвой **DdoS-атаки** или **ваш сайт взломали**, полезно понять, почему вы подверглись атаке и почему именно сейчас.

**Почему вы подверглись атаке и почему именно сейчас**: Как вы считаете, кто мог быть заинтересован в атаке на ваш сайт или на вашу организацию? Размещали ли вы в последнее время информацию на спорные темы, может ли эта атака быть связана с вашей работой, а может ваш сайт получает слишком большое количество трафика или прошёл срок оплаты за домен?
Почему сейчас? Могло ли изменение контента вашего сайта вызвать DdoS-атаку или стать причиной его взлома со стороны злоумышленников? В разделе «Полезная информация» вы найдёте ссылки на руководства по предотвращению цифровых чрезвычайных ситуаций, которые позволят вам проявить инициативу в отношении собственной цифровой безопасности.

## Полезные ресурсы и ссылки:

- [Что делать, если ваш сайт подвергся атаке:](https://github.com/OpenInternet/MyWebsiteIsDown/blob/master/MyWebsiteIsDown_RU.md)
- [Поддержание вашего сайта в рабочем состоянии](https://www.eff.org/ru/keeping-your-site-alive)
- [«Безопасность в коробке»](https://securityinabox.org/en/chapter_7_2) [ENG]
- [«Самозащита от слежки в интернете»](https://ssd.eff.org/risk/threats) [ENG]
