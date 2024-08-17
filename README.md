# ru-block-v2ray-rules
[![Generate v2ray routing rules](https://github.com/pvolkov/ru-block-v2ray-rules/actions/workflows/release.yml/badge.svg)](https://github.com/pvolkov/ru-block-v2ray-rules/actions/workflows/release.yml)

## Что это?
Список блокировок Роскомнадзора в GeoIP и GeoSite для xray или любого другого маршрутизатора трафика принимающего geosite и geoip файлы.

https://antifilter.download/ - Списки блокировок которые используются.

## Как использовать?

<details>
<summary>Загрузка и использование</summary>

Использовать правило `ext:geosite_RU.dat:ru-block` для сайтов или `ext:geoip_RU.dat:ru-block` для ip адресов.

Ввести в консоль:
```
sudo rm -rf /usr/local/x-ui/bin/geosite_RU.dat && sudo curl -sSL https://github.com/pvolkov/ru-block-v2ray-rules/raw/release/geosite.dat -o /usr/local/x-ui/bin/geosite_RU.dat && sudo chmod 744 /usr/local/x-ui/bin/geosite_RU.dat
sudo rm -rf /usr/local/x-ui/bin/geoip_RU.dat && sudo curl -sSL https://github.com/pvolkov/ru-block-v2ray-rules/raw/release/geoip.dat -o /usr/local/x-ui/bin/geoip_RU.dat && sudo chmod 744 /usr/local/x-ui/bin/geoip_RU.dat
```

После в `sudo crontab -e`, добавить следующее:
```
@daily rm -rf /usr/local/x-ui/bin/geosite_RU.dat && curl -sSL https://github.com/pvolkov/ru-block-v2ray-rules/raw/release/geosite.dat -o /usr/local/x-ui/bin/geosite_RU.dat && chmod 744 /usr/local/x-ui/bin/geosite_RU.dat
@daily rm -rf /usr/local/x-ui/bin/geoip_RU.dat && curl -sSL https://github.com/pvolkov/ru-block-v2ray-rules/raw/release/geoip.dat -o /usr/local/x-ui/bin/geoip_RU.dat && chmod 744 /usr/local/x-ui/bin/geoip_RU.dat
```

Настроить правила в X-UI или 3X-UI
</details>

## Благодарности
[Nidelon](https://github.com/Nidelon/ru-block-v2ray-rules)
