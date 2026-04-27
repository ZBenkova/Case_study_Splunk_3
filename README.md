# Splunk exercises 3

Můj příkaz:

```
index = bongo sourcetype = access_combined | stats count by useragent
```

---

Teď mám tabulku s user-agenty:

| useragent                                                                                                                                                                                                                                                                                                         | count |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ----- |
| -                                                                                                                                                                                                                                                                                                                 | 360   |
| Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.0.0 Safari/537.36                                                                                                                                                                                                   | 164   |
| Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/108.0.0.0 Safari/537.36                                                                                                                                                                                                   | 72    |
| Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/120.0.0.0 Safari/537.36                                                                                                                                                                                                             | 64    |
| Wget/1.21.4                                                                                                                                                                                                                                                                                                       | 60    |
| Mozilla/5.0 (compatible; CensysInspect/1.1; +[https://about.censys.io/](https://about.censys.io/))                                                                                                                                                                                                                | 52    |
| Mozilla/5.0 (compatible; YandexBot/3.0; +[http://yandex.com/bots](http://yandex.com/bots))                                                                                                                                                                                                                        | 43    |
| Wget/1.21.3                                                                                                                                                                                                                                                                                                       | 40    |
| Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/78.0.3904.108 Safari/537.36                                                                                                                                                                                               | 37    |
| Mozlila/5.0 (Linux; Android 7.0; SM-G892A Bulid/NRD90M; wv) AppleWebKit/537.36 (KHTML, like Gecko) Version/4.0 Chrome/60.0.3112.107 Moblie Safari/537.36                                                                                                                                                          | 35    |
| Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:77.0) Gecko/20100101 Firefox/77.0                                                                                                                                                                                                                                | 34    |
| Mozilla/5.0 zgrab/0.x                                                                                                                                                                                                                                                                                             | 31    |
| Mozilla/5.0 (X11; Fedora; Linux x86_64; rv:94.0) Gecko/20100101 Firefox/95.0                                                                                                                                                                                                                                      | 30    |
| Expanse, a Palo Alto Networks company, searches across the global IPv4 space multiple times per day to identify customers' presences on the Internet. If you would like to be excluded from our scans, please send IP addresses/domains to: [scaninfo@paloaltonetworks.com](mailto:scaninfo@paloaltonetworks.com) | 29    |
| Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/90.0.4430.85 Safari/537.36 Edg/90.0.818.46                                                                                                                                                                                | 28    |
| Mozilla/5.0 (Macintosh; Intel Mac OS X 10.15; rv:123.0) Gecko/20100101 Firefox/123.0                                                                                                                                                                                                                              | 27    |
| Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/60.0.3112.113 Safari/537.36                                                                                                                                                                                               | 27    |
| python-requests/2.31.0                                                                                                                                                                                                                                                                                            | 26    |
| Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:83.0) Gecko/20100101 Firefox/83.0                                                                                                                                                                                                                                    | 20    |
| Mozilla/5.0 (compatible; YandexFavicons/1.0; +[http://yandex.com/bots](http://yandex.com/bots))                                                                                                                                                                                                                   | 18    |
| Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/114.0.0.0 Safari/537.36                                                                                                                                                                                             | 17    |
| Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:123.0) Gecko/20100101 Firefox/123.0                                                                                                                                                                                                                                  | 17    |
| Mozilla/5.0 (X11; Ubuntu; Linux x86_64; rv:76.0) Gecko/20100101 Firefox/76.0                                                                                                                                                                                                                                      | 17    |
| Mozilla/5.0 (compatible; Googlebot/2.1; +[http://www.google.com/bot.html](http://www.google.com/bot.html))                                                                                                                                                                                                        | 17    |
| Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/81.0.4044.129 Safari/537.36                                                                                                                                                                                                         | 16    |
| Mozilla/5.0 (compatible; BackupLand/1.0; [https://go.backupland.com/](https://go.backupland.com/); Domain check for viruses;)                                                                                                                                                                                     | 15    |
| Python/3.11 aiohttp/3.9.3                                                                                                                                                                                                                                                                                         | 14    |
| Mozilla/5.0 (Windows NT 10.0; WOW64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/51.0.2704.103 Safari/537.36                                                                                                                                                                                                    | 13    |
| Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:123.0) Gecko/20100101 Firefox/123.0                                                                                                                                                                                                                                  | 13    |
| Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/121.0.0.0 Safari/537.36                                                                                                                                                                                                             | 13    |
| 2ip bot/1.1 (+[http://2ip.io](http://2ip.io))                                                                                                                                                                                                                                                                     | 12    |
| Go-http-client/1.1                                                                                                                                                                                                                                                                                                | 12    |
| Mozilla/5.0                                                                                                                                                                                                                                                                                                       | 12    |
| Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/96.0.4664.110 Safari/537.36                                                                                                                                                                                         | 12    |
| python-requests/2.27.1                                                                                                                                                                                                                                                                                            | 12    |
| Mozilla/5.0 (compatible; InternetMeasurement/1.0; +[https://internet-measurement.com/](https://internet-measurement.com/))                                                                                                                                                                                        | 11    |
| fasthttp                                                                                                                                                                                                                                                                                                          | 10    |

---

## Pozorování

* wget = možné automatizované stahování nebo podezřelá aktivita
* python-requests = skripty / API volání, nutno kontrolovat
* Go-http-client / aiohttp / fasthttp = programatický provoz
* boty (Googlebot, YandexBot) = legitimní crawling
* zgrab a podobné UA = často scanning nástroje

---

## Další search

```
index = bongo sourcetype = access_combined status=404
```

```
index = bongo sourcetype = access_combined status=404 | stats count by uri
```

### Co je URI

URI říká, který konkrétní zdroj nebo část aplikace byla požadována.

Ve Splunku je URI stopa po tom, kam uživatel nebo systém sáhl.

---

```
index = bongo sourcetype = access_combined status=404 | stats count by clientip
```

```
index = bongo sourcetype = access_combined status=404 | stats values(uri) count by clientip
```

Tady se dívám na:

* kam daná IP adresa šla
* co se snažila najít

---

## Interpretace chování

* wget → automatizované pokusy nebo command injection
* wordpress/setup-config → hledání WordPress instalace
* systembc/password.php → podezřelý soubor, reconnaissance nebo scanning

---

## Závěr

Jde o:

* automatický scanning
* reconnaissance
* mapování dostupných cest na serveru
