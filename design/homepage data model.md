# Hierarchy

- Project (keegi väljast ei näe, rahastus, lepingud)
    - Interview
        - Chapter
        - TimecodedSubject
    - Story / videolugu
        - TimecodedSubject
- Sponsor (toetajad)

# Definitions

## Project *(Project)*

- name
- code (võibla me ei kasutagi koode)
- projekti lepingu alguse aasta
- kirjeldus
- toetajad -> ***Sponsor***



## Interview *(interview)*
Täispikk videointervjuu, milles vestja räägib oma loo.

- photo
- date(s) (AASTA, SALVESTUSKUUPÄEV(AD))
- category (KATEGOORIA) -> ***Category***
- language (KEEL)
- storyteller(s) (LOORÄÄKIJAD) -> ***Person***
- title / **multilingual** - paneme kokku
    - titleShort:public (INTERVJUU PEALKIRI (lühike))
    - titleLong:private (INTERVJUU PEALKIRI (pikk))
- recordingLocation (KOGUMISE / SALEVESTUSE TOIMUMISKOHT)
- description / **multilingual** - rus (LÜHIKIRJELDUS, LÜHIKIRJELDUSE KEEL) + (LISAINFO)
- mention(s) (MAINITUD ISIKUD) -> ***Person***
- region(s) (MAINITUD PIIRKONNAD) -> ***Region***
- tag (YOUTUBE SILDID) -> ***Tag***
- lookup property: story -> ***self.Story***
- lookup property: project -> ***self.Project***
- videoUrl
- author (VIDEOLOO AUTOR) -> ***Person***
- link(s) -> ***Link*** - references to documents/sources


Supakate keel valida siit:  [vimeo supakad](https://vimeo.com/help/faq/managing-your-videos/captions-and-subtitles#what-caption-and-subtitle-file-formats-does-vimeo-support)  
Oleks hea, kui see sobiks ka muude ajakodeeritud väljade jaoks.


> Märksõnu võib igaüks panna ja välja mõtelda; Teemad on etteantud klassifikaatorid


## Story *(story)*
> videolugu

- photo
- category (KATEGOORIA) -> ***Category***
- title / **multilingual** - paneme kokku
- language(s) - keeled, mida kasutatakse jutus
- subtitles / **multilingual**
- lookup property: project (PROJEKT) -> ***self.Project***
- interview(s) -> ***Interview***
- tag(s) -> ***Tag***
- description / **multilingual** - (LÜHIKIRJELDUS, LÜHIKIRJELDUSE KEEL) + (LISAINFO)
- videoUrl (VIDEOLOO LINK YOUTUBE-is)
- storyteller(s) (LOORÄÄKIJAD) -> ***Person***
- author -> ***Person***
- link(s) -> ***Link*** - references to documents/sources


## Chapter
- time (hh:mm:ss)
- chapter name / **multilingual** - (INTERVJUUS KÄSITLETUD TEEMAD AJAKOODIDEGA)


## Timecoded Subject
- time (hh:mm:ss)
- subject -> ***Subject***


## Subject *(subject)*
Is hierarchical

- name / **multilingual** - (ÕPPEKAVAGA SEOTUD MÄRKSÕNAD / MÕISTED AJAKOODIDEGA) 


## Tag *(tag)*

- name


## Category *(category)*

- code (võibla me ei kasutagi koode)
- name
- color
- description


## Storyteller on hoopis *(person)*

- email (LOORÄÄKIJA KONTAKT)
- phone (LOORÄÄKIJA KONTAKT)
- birthYear (LOO RÄÄKIJA SÜNNIAEG)
- name (LOORÄÄKIJAD)
- description (SOTSIAALNE TAUST)


## Author on hoopis *(person)*

- email
- phone
- name


## Region *(region)*
Is hierarchical

- name
- fullName (Kogu asukoha hierarhiline rada)
- otherName(s) - Piirkonnal ajalooliselt olnud teised nimed
- feature (Kas näidata kodulehe klassifikaatoris)


## Links *(link)*
- name - string
- url - string
- photo - thumbnail from attached documents/url's
- document(s) - file - for self-hosted documents.


## Toetajad *(sponsor)*

- name
- logo
- link
- contact -> ***Person***


### Originaalväljad

- REGISTRI NR - N/A
- AASTA == ***Interview.tellingDate***
- KEEL == ***Interview.language***
- PROJEKT == ***Story.project***
- KATEGOORIA == ***Story.category***
- LOORÄÄKIJAD == ***Chapter.storyteller***, ***Interview.storyteller***
- TUNTUD INIMENE? == kaob ära
- LOO RÄÄKIJA SÜNNIAEG == ***Storyteller.birthYear***
- LOORÄÄKIJA KONTAKT == ***Storyteller.email/.phone***
- INTERVJUU PEALKIRI (pikk) == ***Interview.title***
- INTERVJUU PEALKIRI (lühike) == ***Interview.title***
- LÜHIKIRJELDUS == ***Chapter.description***
- LÜHIKIRJELDUSE KEEL == ***Chapter.description***
- KOGUMISE / SALEVESTUSE TOIMUMISKOHT == ***Interview.recordingLocation***
- ANDMEFORMAAT - kõik on video tüüpi?
- SALVESTISE ORIGINAALFORMAAT - oluline?
- BROADCAST STANDARD - oluline?
- "SALVESTUSKUUPÄEV
  - tervik  
    AAAA-KK-PP formaat" == ***Interview.date***
  - VÕI
  - "SALVESTUSKUUPÄEVAD
    - alguskuupäev  
      AAAA-KK-PP formaat" == ***Interview.date***
    - lõppkuupäev  
      AAAA-KK-PP formaat" == ***Interview.date***
- MAINITUD ISIKUD == ***Chapter.mentions***
- MAINITUD PIIRKONNAD == ***Chapter.region***
- SOTSIAALNE TAUST == ***Storyteller.background***
- VIDEOLOO AUTOR == ***Chapter.author***
- VIDEOLOO PEALKIRI == ***Chapter.title***
- VIDEOLOO LINK YOUTUBE-is == ***Chapter.videoUrl (VIDEOLOO LINK YOUTUBE-is)***
- INTERVJUUS KÄSITLETUD TEEMAD AJAKOODIDEGA == ***Interview.timecodedSubjects***
- ÕPPEKAVAGA SEOTUD MÄRKSÕNAD / MÕISTED AJAKOODIDEGA == ***Interview.timecodedCurriculum***
- KANAL
- YOUTUBE SILDID == ***Chapter.tag***
- LISAINFO == ***Story.legend***

---
