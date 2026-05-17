# Sasinos CZ AdBlock

DNS-level blocklist pro české a slovenské reklamní sítě. Určeno pro **AdGuard Home**, **Pi-hole** a další DNS resolvery podporující AdBlock syntax.

## 🎯 Cíl projektu

Většina veřejných DNS blocklistů (OISD, Hagezi, AdGuard DNS filter) je zaměřena na globální adtech (Google Ads, Facebook). České reklamní sítě (Sklik, Etarget, R2B2, MAFRA) jsou v nich pokryty jen částečně.

Tento seznam **doplňuje** globální seznamy o CZ/SK-specific reklamní infrastrukturu.

## 📦 Použití

### AdGuard Home

1. Otevři **Filtry → DNS seznam blokovaných**
2. Klikni **Přidat seznam blokovaných** → **Přidat vlastní seznam**
3. Vyplň:
   - **Název:** `Sasinos CZ AdBlock`
   - **URL:** `https://raw.githubusercontent.com/Sasinos/adguard-cz-blocklist/main/sasinos-cz-adblock.txt`
4. Klikni **Uložit**

### Pi-hole

1. **Group Management → Adlists → Add**
2. Vlož URL výše
3. **Tools → Update Gravity**

## 🛡️ Co seznam pokrývá

| Kategorie | Příklady |
|---|---|
| **Sklik / Seznam ad network** | `imedia.cz`, `sklik.cz`, `ssp.seznam.cz` |
| **Etarget (CZ/SK PPC)** | `etarget.cz`, `etarget.com`, `etarget.eu` |
| **R2B2 (programmatic)** | `r2b2.cz`, `r2b2.io`, `ssp.r2b2.cz` |
| **MAFRA ad delivery** | `gidnes.cz`, `topkontakt.cz`, `bbelements.com` |
| **Czech News Center** | `ads.cncenter.cz`, `cnc-ads.bbelements.com` |
| **Native ads** | `toptext.cz`, `lookit.cz` |
| **Banner delivery** | `ibillboard.com`, `nuggad.net` |
| **Adform** | `adform.net`, `serve.adform.net` |
| **SmartAdServer** | `smartadserver.com`, `sas.smartadserver.com` |
| **Centrum, Nova, Aktuálně, IHNED** | `ads.centrum.cz`, `ads.nova.cz`, `advert.ihned.cz` |

## ❌ Co seznam nepokrývá

- **Globální adtech** (Google Ads, Facebook) → použij [OISD Big](https://oisd.nl/) nebo [Hagezi Pro](https://github.com/hagezi/dns-blocklists)
- **Analytics a tracking** → kryto OISD/Hagezi
- **Malware / phishing** → použij Hagezi TIF nebo URLhaus filter
- **Cosmetic filters** (skrytí HTML elementů) → vyžaduje uBlock Origin v prohlížeči + [EasyList Czech and Slovak](https://github.com/tomasko126/easylistczechandslovak)

## 📋 Doporučená kombinace seznamů

Tento seznam funguje nejlépe v kombinaci s:

1. **AdGuard DNS filter** (built-in v AGH)
2. **OISD Big** — `https://big.oisd.nl/`
3. **Hagezi Pro** — `https://raw.githubusercontent.com/hagezi/dns-blocklists/main/adblock/pro.txt`
4. **Sasinos CZ AdBlock** (tento seznam)

Pro **kompletní ad-free experience na českém webu** přidej do prohlížeče:

- **uBlock Origin** + **EasyList Czech and Slovak**

## 📊 Statistiky

- **123 blokovaných pravidel**
- **12 whitelist výjimek** (české banky, Heureka, Zboží.cz)
- Aktualizace: dle commitů

## 🔄 Aktualizace

AdGuard Home / Pi-hole automaticky kontroluje aktualizace každých 24 hodin. Pro okamžitý update klikni **Zkontrolovat aktualizace** v UI.

## 🐛 Hlášení problémů

Pokud zjistíš:
- **False positive** (zablokovaná legitimní stránka) → otevři [Issue](https://github.com/Sasinos/adguard-cz-blocklist/issues) s URL a popisem
- **Missing block** (reklama prošla) → otevři Issue s doménou reklamního serveru

## 📜 Licence

Tento seznam je licencován pod [CC-BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).

## 🙏 Inspirace

Projekt vychází z analýzy českého adtech ekosystému s respektem k práci komunit:
- [AdGuard Team](https://github.com/AdguardTeam)
- [OISD](https://oisd.nl/)
- [Hagezi DNS blocklists](https://github.com/hagezi/dns-blocklists)
- [EasyList Czech and Slovak](https://github.com/tomasko126/easylistczechandslovak)
