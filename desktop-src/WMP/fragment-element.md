---
title: Fragment-Element
description: Das Fragment-Element gibt eine Bedingung der Abfrage an, die Elemente aus der Bibliothek auswählt. Bedingungen werden durch Bedingungs Zeichenfolgen angegeben. Eine Bedingungs Zeichenfolge weist in der Regel einen Namensteil, einen Bedingungs Teil und einen Wertanteil auf.
ms.assetid: 1575318f-8527-42ba-9c2f-9993a60987d7
keywords:
- Fenster Media Player des fragmentelements
topic_type:
- apiref
api_name:
- fragment Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da4cd18c6286cf2439e310b4e797f6978f3b2395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362001"
---
# <a name="fragment-element"></a>Fragment-Element

Das **Fragment** -Element gibt eine Bedingung der Abfrage an, die Elemente aus der Bibliothek auswählt. Bedingungen werden durch Bedingungs Zeichenfolgen angegeben. Eine Bedingungs Zeichenfolge weist in der Regel einen Namensteil, einen Bedingungs Teil und einen Wertanteil auf.

``` syntax
<fragment
    name = "string"
>
</fragment>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**Name** (erforderlich) 
</dt> <dd>

Ein Teil einer Bedingungs Zeichenfolge. Siehe Hinweise.

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                                                               |
|-----------|------------------------------------------------------------------------|
| Parent    | [Filter](filter-element.md), [SourceFilter](sourcefilter-element.md) |
| Untergeordnet     | [argument](argument-element.md)                                       |



 

## <a name="remarks"></a>Bemerkungen

Bestimmte Bedingungs Zeichenfolgen verfügen über einen metadatenattributteil, einen Bedingungs Teil und einen Wertteil. In der Bedingungs Zeichenfolge "Album Artist is Joe" lautet der metadatenattributteil z. b. "Album Artist", der Bedingungs Teil ist "is", und der Wert Teil ist "Joe".

Beispiel:


```XML
<fragment name = "Album Artist">
    <argument name = "condition">Is</argument>
    <argument name = "value">Joe</argument>
</fragment>
```



Für Bedingungs Zeichenfolgen dieses Typs zeigt die folgende Tabelle die möglichen Metadatenattribute, mögliche Bedingungen und mögliche Werte an:



| Metadatenattribut                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Mögliche Bedingungen                                                                                             | Mögliche Werte                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Actor Album-Künstler<br/> Titel des Albums<br/> Autor<br/> Caption<br/> Channel<br/> Composer<br/> Dirigentin<br/> Inhaltsanbieter<br/> Inhaltsanbieter Genre<br/> Beitragende Künstlerin<br/> Copyright Text<br/> Regisseur<br/> Episode<br/> Dateityp<br/> Genre<br/> Schlüssel<br/> Keywords<br/> Sprache<br/> Mood<br/> Eltern Bewertung<br/> Zeitraum<br/> Producer<br/> Anbieter<br/> Publisher<br/> Reihen<br/> Stationsname<br/> Subgenre<br/> Untertitel<br/> Titel<br/> Writer<br/> | Equalsist nicht gleich<br/> Is<br/> Ist nicht<br/> Enthält<br/> Enthält nicht<br/> | Ein beliebiger Zeichenfolgenwert                                                                                                                                                                                                                                                                                                  |
| Bitrate (in Kilobyte pro Sekunde)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | Equalsist nicht gleich<br/> Is<br/> Ist nicht<br/> Enthält<br/> Enthält nicht<br/> | 4864<br/> 96<br/> 128<br/> 160<br/> 192<br/> 256<br/> 300<br/> 500<br/> 750<br/> 1000<br/> 1500<br/> 3000<br/> 4500<br/> 6000<br/> 7.500<br/>                                                                            |
| Sekundärer Medientyp                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | Equalsist nicht gleich<br/> Is<br/> Ist nicht<br/> Enthält<br/> Enthält nicht<br/> | Audiodatei: newsaudiodatei: Talk Show<br/> Audiodokumentation: Audiobücher<br/> Audiosprache: audiowort<br/> Video: Neuigkeiten<br/> Video: Talk Show<br/> Video: Homepage-Video<br/> Video: Movie/Film<br/> Video: TV Show<br/> Video: Video zu Unternehmen<br/> Video: Musikvideo<br/> |
| Bildhöhe der Dateigröße (in KB)<br/> Bildbreite<br/> Wiedergabe Anzahl: Gesamtsummen<br/> Wiedergabe Anzahl: Abend Summen<br/> Wiedergabe Anzahl: Morgen Summen<br/> Wiedergabe Anzahl: Nacht Summen<br/> Wiedergabe Anzahl: Gesamt Gesamt<br/> Wiedergabe Anzahl: Gesamter Wochentag<br/> Wiedergabe Anzahl: Gesamt Wochenende<br/>                                                                                                                                                                                                                                                                                                                  | Ist kleiner als<br/> Is<br/> Ist nicht<br/>                                          | Beliebige Zahl                                                                                                                                                                                                                                                                                                        |
| Broadcast-timedate-codiert<br/> Erfasste Datumsangaben<br/> Datum der Erstellung<br/> Releasejahr<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Ist "beforeis" nach<br/> Is<br/> Ist nicht<br/>                                                    | Gestern letzte Woche<br/> Letzter Monat<br/> 6 Monate<br/> 1 Jahr<br/> 2 Jahre<br/> 5 Jahre<br/> 2000er Sek.<br/> 1990er Jahren<br/> 1980er<br/> 70er Jahren<br/> 60er Jahren<br/> 50er Jahre<br/> 1940s<br/>                                                            |
| Date Added                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Ist "beforeis" nach<br/> Is<br/> Ist nicht<br/>                                                    | Gestern letzte Woche<br/> Letzter Monat<br/> 6 Monate<br/> 1 Jahr<br/> 2 Jahre<br/> 5 Jahre<br/>                                                                                                                                                                                   |
| Letztes Datum                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | Älterer thanaktueller als<br/> Is<br/> Ist nicht<br/>                                           | Gestern letzte Woche<br/> Letzter Monat<br/> 6 Monate<br/> 1 Jahr<br/> 2 Jahre<br/> 5 Jahre<br/>                                                                                                                                                                                   |
| Ergriffene Monate                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Ist beforeis aktueller als<br/> Is<br/> Ist nicht<br/>                                         | 12<br/> 3<br/> 4<br/> 5<br/> 6<br/> 7<br/> 8<br/> 9<br/> 10<br/> 11<br/> 12<br/> 13<br/>                                                                                                                                                  |
| Jahres Angabe                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Ist beforeis aktueller als<br/> Is<br/> Ist nicht<br/>                                         | Beliebiges Jahr                                                                                                                                                                                                                                                                                                          |
| Automatische Ratingbewertung<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Ist bei "leastis" nicht mehr als<br/> Is<br/> Ist nicht<br/>                                           | Unrated1-Stern<br/> Zwei Sterne<br/> Drei Sterne<br/> Vier Sterne<br/> Fünf Sterne<br/>                                                                                                                                                                                                              |
| Benutzerdefiniertes Feld \# 1 benutzerdefiniertes Feld \# 2<br/> Dateiname<br/> Schlüsselfelder<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | "Kontains" enthält nicht<br/>                                                                             | Beliebige Zeichenfolge                                                                                                                                                                                                                                                                                                        |



 

Bestimmte Bedingungs Zeichenfolgen haben einen begrenterteil, einen Zahlen Teil und einen Format Teil. In der Bedingungs Zeichenfolge "begrenzen der Gesamtgröße auf 3 Megabyte" lautet der Begrenzungs Teil beispielsweise "begrenzen der Gesamtgröße auf", der Zahlen Teil "3" und der Format Teil "Megabytes".

Beispiel:


```XML
<fragment name = "Limit Total Size To">
  <argument name = "number">3</argument>
  <argument name = "format">Megabytes</argument>
</fragment>
```



Für Bedingungs Zeichenfolgen dieses Typs werden in der folgenden Tabelle die möglichen begrentoren und Formate angezeigt.



| Einschränkung                 | Mögliche Zahlen | Mögliche Formate                |
|-------------------------|------------------|---------------------------------|
| Beschränken der Gesamtgröße auf     | Beliebige Zahl       | Kilobyte, Megabyte, Gigabyte |
| Beschränken der Gesamtdauer auf | Beliebige Zahl       | Sekunden, Minuten, Stunden, Tage   |



 

Bestimmte Bedingungs Zeichenfolgen haben einen begrenterteil und einen Zahlen Teil. In der Bedingungs Zeichenfolge "Anzahl von Elementen auf 25 begrenzen" lautet der Begrenzungs Teil beispielsweise "Limit number of Items", und der Zahlen Teil ist "25".

Beispiel:


```XML
<fragment name = "Limit Number of Items">
    <argument name = "number">25</argument>
</fragment>
```



Für Bedingungs Zeichenfolgen dieses Typs wird in der folgenden Tabelle die einzige mögliche Begrenzung angezeigt.



| Einschränkung               | Mögliche Zahlen |
|-----------------------|------------------|
| Anzahl der Elemente begrenzen | Beliebige Zahl       |



 

Bestimmte Bedingungs Zeichenfolgen verfügen über einen Schutzbereich und einen Bedingungs Teil. Beispielsweise ist die Bedingungs Zeichenfolge "Schutz ist vorhanden" der Schutz Teil "Schutz", und der Bedingungs Teil ist "ist".

Beispiel:


```XML
<fragment name = "Protection">
    <argument name = "condition">Is</argument>
</fragment>
```



Für Bedingungs Zeichenfolgen dieses Typs zeigt die folgende Tabelle die möglichen Bedingungen an.



| Schutz Teil | Mögliche Bedingungen             |
|--------------------|---------------------------------|
| Schutz         | Is<br/> Ist nicht<br/> |



 

Es gibt einen Typ von **Fragment** -Element, der keine Bedingungs Zeichenfolge enthält. Wenn das Name-Attribut eines **Fragment** -Elements "zufällige Wiedergabe Reihenfolge" ist, enthält das **Fragment** -Element keine **Argument** Elemente. Dieses **Fragment** -Element weist den Player an, die Liste in zufälliger Reihenfolge wiederzugeben.

Beispiel:


```XML
<fragment name = "Randomize Playback Order">
</fragment>
```



Bestimmte Bedingungs Zeichenfolgen verfügen über einen Sortierungs Teil, einen Wertanteil und einen Bedingungs Teil. In der Bedingungs Zeichenfolge "Sortieren nach Titel aufsteigender Reihenfolge" lautet der Sortierungs Teil z. b. "Sortieren nach", der Wertteil ist "Title", und der Bedingungs Teil ist "Aufsteigend". Beachten Sie, dass in diesem Fall der Wert Teil ein Metadatenattribut ist.

Beispiel:


```XML
<fragment name = "Sort By">
    <argument name = "value">Title</argument>
    <argument name = "condition">Ascending</argument>
</fragment>
```



Für Bedingungs Zeichenfolgen dieses Typs zeigt die folgende Tabelle die möglichen Werte und Bedingungen an.



| Sortier Teil | Mögliche Werte                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Mögliche Bedingungen                              |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Sortieren nach      | Genretitle<br/> Date Added<br/> Automatische Bewertung<br/> Meine Bewertung<br/> Wiedergabe Anzahl: Gesamt Gesamt<br/> Wiedergabe Anzahl: Morgen Summen<br/> Wiedergabe Anzahl: Gesamtsummen<br/> Wiedergabe Anzahl: Abend Summen<br/> Wiedergabe Anzahl: Nacht Summen<br/> Wiedergabe Anzahl: Gesamter Wochentag<br/> Wiedergabe Anzahl: Gesamt Wochenende<br/> Akteur<br/> Untertitel<br/> Stationsname<br/> Channel<br/> Broadcast Zeit<br/> Regisseur<br/> Releasejahr<br/> Writer<br/> Producer<br/> Erfasste Datumsangaben<br/> Codiertes Datum<br/> Bitrate<br/> Schutz<br/> | Aufsteisteigend<br/> Zufällig<br/> |



 

Wenn Sie ein Fragment-Element zum Sortieren einer Wiedergabeliste verwenden, müssen Sie nach einem Metadatenattribut sortieren, das für den Typ der zu sortierenden Medienelemente gilt. Wenn Sie z. b. Musik Elemente sortieren, können Sie nicht nach Actor sortieren. In der folgenden Tabelle sind die Metadatenattribute aufgeführt, die Sie zum Sortieren der Medientypen verwenden können.



| Medientyp  | Mögliche Metadatenattribute                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Musik       | Genretitle<br/> Date Added<br/> Automatische Bewertung<br/> Meine Bewertung<br/> Wiedergabe Anzahl: Gesamt Gesamt<br/> Wiedergabe Anzahl: Morgen Summen<br/> Wiedergabe Anzahl: Gesamtsummen<br/> Wiedergabe Anzahl: Abend Summen<br/> Wiedergabe Anzahl: Nacht Summen<br/> Wiedergabe Anzahl: Gesamter Wochentag<br/> Wiedergabe Anzahl: Gesamt Wochenende<br/>                                                                                                                                                                                                                                                                                            |
| Video oder TV | Genreaktor<br/> Untertitel<br/> Titel<br/> Date Added<br/> Automatische Bewertung<br/> Stationsname<br/> Channel<br/> Broadcast Zeit<br/> Regisseur<br/> Releasejahr<br/> Writer<br/> Producer<br/> Erfasste Datumsangaben<br/> Codiertes Datum<br/> Bitrate<br/> Meine Bewertung<br/> Schutz<br/> Wiedergabe Anzahl: Gesamt Gesamt<br/> Wiedergabe Anzahl: Morgen Summen<br/> Wiedergabe Anzahl: Gesamtsummen<br/> Wiedergabe Anzahl: Abend Summen<br/> Wiedergabe Anzahl: Nacht Summen<br/> Wiedergabe Anzahl: Gesamter Wochentag<br/> Wiedergabe Anzahl: Gesamt Wochenende<br/> |
| Radio       | Titledate hinzugefügt<br/> Bitrate<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Photo       | Titel                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Sonstiges       | Genretitle<br/> Date Added<br/> Automatische Bewertung<br/> Meine Bewertung<br/> Bitrate<br/> Wiedergabe Anzahl: Gesamt Gesamt<br/> Wiedergabe Anzahl: Morgen Summen<br/> Wiedergabe Anzahl: Gesamtsummen<br/> Wiedergabe Anzahl: Abend Summen<br/> Wiedergabe Anzahl: Nacht Summen<br/> Wiedergabe Anzahl: Gesamter Wochentag<br/> Wiedergabe Anzahl: Gesamt Wochenende<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Argument-Element**](argument-element.md)
</dt> <dt>

[**Filter-Element**](filter-element.md)
</dt> <dt>

[**SourceFilter-Element**](sourcefilter-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





