---
title: fragment-Element
description: Das Fragmentelement gibt eine Bedingung der Abfrage an, die Elemente aus der Bibliothek auswählt. Bedingungen werden durch Bedingungszeichenfolgen angegeben. Eine Bedingungszeichenfolge verfügt in der Regel über einen Namensteil, einen Bedingungsteil und einen Wertteil.
ms.assetid: 1575318f-8527-42ba-9c2f-9993a60987d7
keywords:
- fragment-Element Windows Media Player
topic_type:
- apiref
api_name:
- fragment Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1010b269302f88f163232bcaf3e37111e5fc219944ff1d141c1189e119bba05a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003700"
---
# <a name="fragment-element"></a>fragment-Element

Das **Fragmentelement** gibt eine Bedingung der Abfrage an, die Elemente aus der Bibliothek auswählt. Bedingungen werden durch Bedingungszeichenfolgen angegeben. Eine Bedingungszeichenfolge verfügt in der Regel über einen Namensteil, einen Bedingungsteil und einen Wertteil.

``` syntax
<fragment
    name = "string"
>
</fragment>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (erforderlich) 
</dt> <dd>

Ein Teil einer Bedingungszeichenfolge. Siehe Hinweise.

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                                                               |
|-----------|------------------------------------------------------------------------|
| Parent    | [filter](filter-element.md), [sourceFilter](sourcefilter-element.md) |
| Untergeordnet     | [argument](argument-element.md)                                       |



 

## <a name="remarks"></a>Hinweise

Bestimmte Bedingungszeichenfolgen verfügen über einen Metadatenattributteil, einen Bedingungsteil und einen Wertteil. In der Bedingungszeichenfolge "Album Interpret Is Joe" ist der Metadatenattributteil beispielsweise "Album Interpret", der Bedingungsteil ist "Is", und der Wertteil ist "Joe".

Beispiel:


```XML
<fragment name = "Album Artist">
    <argument name = "condition">Is</argument>
    <argument name = "value">Joe</argument>
</fragment>
```



Für Bedingungszeichenfolgen dieses Typs enthält die folgende Tabelle die möglichen Metadatenattribute, mögliche Bedingungen und mögliche Werte:



| Metadatenattribut                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Mögliche Bedingungen                                                                                             | Mögliche Werte                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Actor ("Actor("Akteur)"<br/> Albumtitel<br/> Autor<br/> Caption<br/> Kanal<br/> Composer<br/> Dirigent<br/> Inhaltsanbieter<br/> Content Provider Genre<br/> Mitwirkende Interpretin<br/> Copyrighttext<br/> Regisseur<br/> Episode<br/> Dateityp<br/> Genre<br/> Key<br/> Keywords<br/> Sprache<br/> Stimmung<br/> Bewertung der Eltern<br/> Zeitraum<br/> Producer<br/> Anbieter<br/> Herausgeber<br/> Reihen<br/> Stationsname<br/> Subgenre<br/> Untertitel<br/> Titel<br/> Writer<br/> | EqualsDoes Not Equal<br/> Is<br/> Ist nicht<br/> Enthält<br/> Enthält nicht<br/> | Ein beliebiger Zeichenfolgenwert                                                                                                                                                                                                                                                                                                  |
| Bitrate (in Kilobytes pro Sekunde)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | EqualsDoes Not Equal<br/> Is<br/> Ist nicht<br/> Enthält<br/> Enthält nicht<br/> | 4864<br/> 96<br/> 128<br/> 160<br/> 192<br/> 256<br/> 300<br/> 500<br/> 750<br/> 1000<br/> 1500<br/> 3000<br/> 4500<br/> 6000<br/> 7.500<br/>                                                                            |
| Sekundärer Medientyp                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | EqualsDoes Not Equal<br/> Is<br/> Ist nicht<br/> Enthält<br/> Enthält nicht<br/> | Audio: NewsAudio: Talk Show<br/> Audio: Audio Books<br/> Audio: Gesprochenes Audiowort<br/> Video: Neuigkeiten<br/> Video: Talk Show<br/> Video: Home-Video<br/> Video: Film/Film<br/> Video: TV-Show<br/> Video: Unternehmensvideo<br/> Video: Musik Video<br/> |
| Dateigröße (in KB)Bildhöhe<br/> Bildbreite<br/> Anzahl der Wiedergaben: Gesamtsummen der Gesamtanzahl der Sonntage<br/> Anzahl der Wiedergaben: Gesamtsummen für den Abend<br/> Play Count : Morning Totals<br/> Play Count : Night Totals<br/> Wiedergabeanzahl: Gesamtsumme<br/> Play Count : Total Weekday<br/> Play Count : Total Weekend<br/>                                                                                                                                                                                                                                                                                                                  | Ist kleiner alsIs größer als<br/> Is<br/> Ist nicht<br/>                                          | Beliebige Zahl                                                                                                                                                                                                                                                                                                        |
| BroadcastzeitDate codiert<br/> Aufgezeichnetes Datum<br/> Datum der Erstellung<br/> Releasejahr<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Ist BeforeIs After<br/> Is<br/> Ist nicht<br/>                                                    | Gestrige Letzte Woche<br/> Letzter Monat<br/> 6 Monate<br/> 1 Jahr<br/> 2 Jahre<br/> 5 Jahre<br/> 2000er<br/> 1990er-Jahre<br/> 1980er-Jahre<br/> 1970er jahren<br/> 1960er jahren<br/> 1950er-Jahre<br/> 1940er-Jahre<br/>                                                            |
| Date Added                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Ist BeforeIs After<br/> Is<br/> Ist nicht<br/>                                                    | Gestrige Letzte Woche<br/> Letzter Monat<br/> 6 Monate<br/> 1 Jahr<br/> 2 Jahre<br/> 5 Jahre<br/>                                                                                                                                                                                   |
| Datum der letzten Abspielung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Älter alsWeiter zuletzt als<br/> Is<br/> Ist nicht<br/>                                           | Gestrige Letzte Woche<br/> Letzter Monat<br/> 6 Monate<br/> 1 Jahr<br/> 2 Jahre<br/> 5 Jahre<br/>                                                                                                                                                                                   |
| Genommener Monat                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Ist beforeIs aktueller als<br/> Is<br/> Ist nicht<br/>                                         | 12<br/> 3<br/> 4<br/> 5<br/> 6<br/> 7<br/> 8<br/> 9<br/> 10<br/> 11<br/> 12<br/> 13<br/>                                                                                                                                                  |
| Aufgenommenes Jahr                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Ist beforeIs aktueller als<br/> Is<br/> Ist nicht<br/>                                         | Beliebiges Jahr                                                                                                                                                                                                                                                                                                          |
| Automatische BewertungMeine Bewertung<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Ist at leastIs nicht mehr als<br/> Is<br/> Ist nicht<br/>                                           | Unrated1 Star<br/> Zwei Sterne<br/> Drei Sterne<br/> Vier Sterne<br/> Fünf Sterne<br/>                                                                                                                                                                                                              |
| Benutzerdefiniertes \# Feld 1Custom Field \# 2<br/> Dateiname<br/> Schlüsselfelder<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | ContainsDoes Not Contain<br/>                                                                             | Beliebige Zeichenfolge                                                                                                                                                                                                                                                                                                        |



 

Bestimmte Bedingungszeichenfolgen verfügen über einen Begrenzungsteil, einen Zahlenteil und einen Formatteil. In der Bedingungszeichenfolge "Limit Total Size To 3 Megabytes" ist der Limiterteil beispielsweise "Limit Total Size To", der Zahlenteil ist "3" und der Formatteil ist "Megabytes".

Beispiel:


```XML
<fragment name = "Limit Total Size To">
  <argument name = "number">3</argument>
  <argument name = "format">Megabytes</argument>
</fragment>
```



Für Bedingungszeichenfolgen dieses Typs enthält die folgende Tabelle die möglichen Grenzwerte und Formate.



| Limiter                 | Mögliche Zahlen | Mögliche Formate                |
|-------------------------|------------------|---------------------------------|
| Gesamtgröße begrenzen auf     | Beliebige Zahl       | Kilobytes, Megabytes, Gigabytes |
| Gesamtdauer begrenzen auf | Beliebige Zahl       | Sekunden, Minuten, Stunden, Tage   |



 

Bestimmte Bedingungszeichenfolgen verfügen über einen Begrenzungsteil und einen Zahlenteil. In der Bedingungszeichenfolge "Limit Number of Items to 25" (Anzahl von Elementen auf 25 beschränken) ist der Limiterteil beispielsweise "Limit Number of Items" (Anzahl der Elemente begrenzen) und number (Anzahl) ist "25".

Beispiel:


```XML
<fragment name = "Limit Number of Items">
    <argument name = "number">25</argument>
</fragment>
```



Für Bedingungszeichenfolgen dieses Typs zeigt die folgende Tabelle den einzigen möglichen Grenzwert.



| Limiter               | Mögliche Zahlen |
|-----------------------|------------------|
| Begrenzen der Anzahl von Elementen | Beliebige Zahl       |



 

Bestimmte Bedingungszeichenfolgen verfügen über einen Schutz- und einen Bedingungsteil. In der Bedingungszeichenfolge "Protection Is present" (Schutz ist vorhanden) ist der Schutzteil "Protection", und der Bedingungsteil ist "Is".

Beispiel:


```XML
<fragment name = "Protection">
    <argument name = "condition">Is</argument>
</fragment>
```



Für Bedingungszeichenfolgen dieses Typs zeigt die folgende Tabelle die möglichen Bedingungen.



| Schutzteil | Mögliche Bedingungen             |
|--------------------|---------------------------------|
| Schutz         | Is<br/> Ist nicht<br/> |



 

Es gibt einen **Fragmentelementtyp,** der keine Bedingungszeichenfolge enthält. Wenn das Name-Attribut eines **Fragmentelements** "Randomize Playback Order" lautet, enthält das **Fragmentelement** keine **Argumentelemente.** Dieses **Fragmentelement** weist den Spieler an, die Liste in zufälliger Reihenfolge wieder zu spielen.

Beispiel:


```XML
<fragment name = "Randomize Playback Order">
</fragment>
```



Bestimmte Bedingungszeichenfolgen verfügen über einen Sortierteil, einen Wertteil und einen Bedingungsteil. In der Bedingungszeichenfolge "Sort By Title Ascending Order" ist der Sortierteil beispielsweise "Sort By", der Wertteil ist "Title" und der Bedingungsteil ist "Ascending". Beachten Sie, dass in diesem Fall der Wertteil ein Metadatenattribut ist.

Beispiel:


```XML
<fragment name = "Sort By">
    <argument name = "value">Title</argument>
    <argument name = "condition">Ascending</argument>
</fragment>
```



Für Bedingungszeichenfolgen dieses Typs enthält die folgende Tabelle die möglichen Werte und Bedingungen.



| Sortierteil | Mögliche Werte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Mögliche Bedingungen                              |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Sortieren nach      | GenreTitle<br/> Date Added<br/> Automatische Bewertung<br/> Meine Bewertung<br/> Wiedergabeanzahl: Gesamtsumme<br/> Play Count : Morning Totals<br/> Anzahl der Wiedergaben: Gesamtsummen der Gesamtanzahl der Sonntage<br/> Anzahl der Wiedergaben: Gesamtsummen für den Abend<br/> Play Count : Night Totals<br/> Play Count : Total Weekday<br/> Play Count : Total Weekend<br/> Akteur<br/> Untertitel<br/> Stationsname<br/> Kanal<br/> Übertragungszeit<br/> Regisseur<br/> Releasejahr<br/> Writer<br/> Producer<br/> Aufgezeichnetes Datum<br/> Datumscodiert<br/> Bitrate<br/> Schutz<br/> | AscendingDescending<br/> Zufällig<br/> |



 

Wenn Sie ein Fragmentelement zum Sortieren einer Wiedergabeliste verwenden, müssen Sie nach einem Metadatenattribut sortieren, das für den Typ der Medienelemente gilt, die Sie sortieren. Wenn Sie beispielsweise Musikelemente sortieren, können Sie nicht nach Actor sortieren. Die folgende Tabelle zeigt, welche Metadatenattribute Sie zum Sortieren der Medientypen verwenden können.



| Medientyp  | Mögliche Metadatenattribute                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Musik       | GenreTitle<br/> Date Added<br/> Automatische Bewertung<br/> Meine Bewertung<br/> Wiedergabeanzahl: Gesamtsumme<br/> Play Count : Morning Totals<br/> Anzahl der Wiedergaben: Gesamtsummen der Gesamtanzahl der Spiele<br/> Play Count :Evening Totals<br/> Play Count :Night Totals<br/> Play Count :Total Weekday<br/> Play Count : Total Weekend<br/>                                                                                                                                                                                                                                                                                            |
| Video oder TV | GenreActor<br/> Untertitel<br/> Titel<br/> Date Added<br/> Automatische Bewertung<br/> Stationsname<br/> Kanal<br/> Übertragungszeit<br/> Regisseur<br/> Releasejahr<br/> Writer<br/> Producer<br/> Aufgezeichnetes Datum<br/> Datumscodiert<br/> Bitrate<br/> Meine Bewertung<br/> Schutz<br/> Wiedergabeanzahl: Gesamtsumme<br/> Play Count : Morning Totals<br/> Anzahl der Wiedergaben: Gesamtsummen der Gesamtanzahl der Sonntage<br/> Anzahl der Wiedergaben: Gesamtsummen für den Abend<br/> Play Count : Night Totals<br/> Play Count : Total Weekday<br/> Play Count : Total Weekend<br/> |
| Radio       | TitleDate hinzugefügt<br/> Bitrate<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Photo       | Titel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Andere       | GenreTitle<br/> Date Added<br/> Automatische Bewertung<br/> Meine Bewertung<br/> Bitrate<br/> Anzahl der Wiedergaben: Gesamt gesamt<br/> Anzahl der Wiedergaben: Gesamtsummen am Morgen<br/> Anzahl der Wiedergaben: Gesamtsummen<br/> Anzahl der Wiedergaben: Abendsummen<br/> Play Count : Night Totals<br/> Anzahl der Wiedergaben: Gesamter Wochentag<br/> Play Count : Total Weekend<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9er Serie oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**argument-Element**](argument-element.md)
</dt> <dt>

[**filter-Element**](filter-element.md)
</dt> <dt>

[**sourceFilter-Element**](sourcefilter-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





