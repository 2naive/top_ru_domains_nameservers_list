# Top DNS providers in Russia used by RU domains from Alexa Top 1M
```
1. cloudflare.com
2. nic.ru
3. reg.ru
4. yandex.net
5. beget.ru
6. timeweb.ru
7. selectel.ru
8. fastvps.ru
9. r01.ru
10. masterhost.ru
11. ihc.ru
12. cloudns.net
13. webnames.ru
```

Nameservers rating lists ns_top10k.txt, ns_top100k.txt, ns_top1m.txt obtained as follows:
```
wget -q -O - https://raw.githubusercontent.com/zer0h/top-1000000-domains/master/top-10000-domains | grep "^.*\.ru$" | xargs dig SOA +noall +answer +short | cut -d " " -f1 | cut -d "." -f2- | sort | uniq -c | sort -nr > ns_top10k.txt

wget -q -O - https://raw.githubusercontent.com/zer0h/top-1000000-domains/master/top-100000-domains | grep "^.*\.ru$" | xargs dig SOA +noall +answer +short | cut -d " " -f1 | cut -d "." -f2- | sort | uniq -c | sort -nr > ns_top100k.txt

wget -q -O - https://raw.githubusercontent.com/zer0h/top-1000000-domains/master/top-1000000-domains | grep "^.*\.ru$" | xargs dig SOA +noall +answer +short | cut -d " " -f1 | cut -d "." -f2- | sort | uniq -c | sort -nr > ns_top1m.txt
```

Subdomains were cut for counting purpose with ` cut -d "." -f2- ` command, which should be ommitted to get actual DNS servers list.

Top .ru domain lists ru_alexa_top1m.txt, ru_alexa_top1m_v2.txt obtained as follows:

```
wget -q -O - https://github.com/zer0h/top-1000000-domains/raw/master/top-1000000-domains | grep "^.*\.ru$" > ru_alexa_top1m.txt
wget -q -O - https://raw.githubusercontent.com/dingzhaohan/alexa_top_1m/master/top-1m.csv | cut -d "," -f2- | grep "^.*\.ru$" > ru_alexa_top1
m_v2.txt

```

[Comparison table](https://docs.google.com/spreadsheets/d/1AIlKX6xdvqXKou6kzspskn4pfu8bo-oYan2JaN6PVbI/edit)
