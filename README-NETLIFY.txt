HADIS TRAZILICA — KATALOG ZA BESPLATNI SERVER
================================================================

Ova mapa se postavlja na besplatan hosting (Netlify) i aplikacija
"Hadis Tražilica" čita knjige odatle.

KORACI (Netlify — najjednostavnije):
1. Idite na  https://app.netlify.com/drop  (prijava putem GitHub/Google).
2. Povucite CIJELU ovu mapu (web_site) u prozor i pustite.
3. Netlify će dati adresu, npr.  https://oransko-stablo-123.netlify.app
4. U aplikaciji: Postavke -> "Adresa servera" -> upišite tu adresu
   (bez / katalog.json, npr. https://oransko-stablo-123.netlify.app)
   -> "Testiraj vezu" -> treba pisati "Katalog učitano: 19 stavki".
5. Hadisi, Kur'an, Biblija i Tefsir se povlače sa servera. Aplikacija je
   lagana i brza.

ŠTA OVA MAPA SADRŽI:
- index.html           -> početna stranica (kad neko otvori sajt u pregledniku)
- katalog.json         -> spisak knjiga (aplikacija ovaj fajl prvo čita)
- _headers             -> Netlify pravilo (CORS) da aplikacija smije čitati fajlove
- data/                -> tekst: Buhari, Ebu Davud, Nesai, Kur'an, Tefsir indeks, Biblija
- docs/ibn_kesir_tefsir.pdf  -> cijeli Tefsir Ibn Kesir (28 MB) za čitanje u app
- docs/sunen_nesai_1.pdf, sunen_nesai_2.pdf -> Nesai PDF za "Stranicu u knjizi"

KAKO DODATI TRMIZI I MUSLIM (PDF čitanje):
Tirmizi i Muslim su skenirani (nemaju tekst), pa se čitaju kao PDF.
Samo preimenuj svoje PDF-ove i stavi ih u mapu docs/ (povuci preko
drag&drop u Netlify kad drugi put deployaš):
  Tirmizi:
    docs/tirmizi_1.pdf .... docs/tirmizi_6.pdf   (skenovi "crno bijelo")
    docs/tirmizi_7.pdf                            (7. tom, ima tekst)
  Muslim:
    docs/muslim_1.pdf     docs/muslim_2.pdf      docs/muslim_3.pdf
Aplikacija u tabu "Biblioteka" automatski pokazuje sve PDF-ove i uspijeva
otvoriti one koji stvarno postoje na serveru.

NOVI PDF: kad god hoćeš dodati još neku PDF knjigu, dodaj je u
katalog.json (ispod "pdfs") i preimenuj fajl u docs/. Aplikacija će je
pokazati u "Biblioteka".

NAPOMENA O VELIČINI:
- Netlify (free): podržava velike fajlove; Muslim 2. tom (151 MB) i 1. tom
  (177 MB) mogu biti granični — ako baci grešku, prenesi Muslim u manjim
  dijelovima ili iskoristi drugi hosting.
- GitHub Pages: dozvoljava do 100 MB po fajlu.
