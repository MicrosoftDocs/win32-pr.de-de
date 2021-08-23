---
title: Beispielwiedergabeliste für Radiosender
description: Beispielwiedergabeliste für Radiosender
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Windows Wiedergabelisten von Medienmetadateien, Wiedergabelistenbeispiele
- Wiedergabelisten,Wiedergabelistenbeispiele
- Metafile-Wiedergabelisten, Wiedergabelistenbeispiele
- Windows Wiedergabelisten von Medienmetadateien, Beispielwiedergabelisten
- Wiedergabelisten,Beispielwiedergabelisten
- Metafile-Wiedergabelisten, Beispielwiedergabelisten
- Windows Wiedergabelisten von Medienmetadateien, Beispielwiedergabelisten
- Wiedergabelisten, Beispielwiedergabelisten
- Metafile-Wiedergabelisten, Beispielwiedergabelisten
- Windows Wiedergabelisten von Medienmetadateien,Codebeispiel
- Wiedergabelisten,Codebeispiel
- Metafile-Wiedergabelisten,Codebeispiel
- Windows Wiedergabelisten von Medienmetadateien, Beispiel für Radiostationswiedergabeliste
- Wiedergabelisten, Beispiel für Radiosender-Wiedergabeliste
- Metafile-Wiedergabelisten, Beispiel für Radiosender-Wiedergabeliste
- Windows Media Player,Wiedergabelistenbeispiele
- Windows Media Player,Beispielwiedergabelisten
- Windows Media Player,Beispielwiedergabelisten
- Windows Media Player,Beispiel für Radiostation-Wiedergabeliste
- Wiedergabelistenbeispiele
- Beispielwiedergabelisten
- Beispielwiedergabelisten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6db52d8eb9f109df870e65f79906761cfadee4a7871f4776fae3122dd93c8605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055028"
---
# <a name="an-example-radio-station-playlist"></a>Beispielwiedergabeliste für Radiosender

Der folgende Beispielcode veranschaulicht das Erstellen einer Wiedergabeliste zum Scannen von drei Funkstationen für Gestein. Die fiktive Marke Adventure Works Radio befindet sich in der Wiedergabeliste und in allen einzelnen Streams innerhalb der Wiedergabeliste. Wenn Sie Ihren Code schreiben, ändern Sie alle URLs und Dateinamen in gültige Dateinamen, auf die Ihre Windows Media Player.

Für jede Station wird eine Wiedergabeliste erstellt. Eine vierte Wiedergabeliste durchsucht die ersten drei. Die Wiedergabelisten werden erstellt, um auf dynamisch generierte Ankündigungen zu verweisen, und verfügen über ein Adventure Works Radio-Branding.

Eine der Wiedergabelisten, die einen Radiosender darstellen, könnte wie dies aussehen.


```XML
<ASX version = "3.0">
    <TITLE>Adventure Works Radio</TITLE>
    <MOREINFO href = "https://www.adventure-works.com" />
    <ENTRY clientSkip = "no" skipIfRef = "yes">
       <REF href = "https://www.adventure-works.com/ad.asp/" />
    </ENTRY>
    <ENTRY>
        <TITLE>MyWRCK Radio</TITLE>
        <ABSTRACT>MyTown's Best Rock 'n Roll</ABSTRACT>
        <COPYRIGHT>2000 RadioNetwork</COPYRIGHT>
        <MOREINFO href = "https://www.adventure-works.com" />
        <REF href = "https://www.adventure-works.com" />
        <REF href = "https://backup.adventure-works.com" />
    </ENTRY>
</ASX>

```



Die Wiedergabeliste kann dann aus Verweisen auf die einzelnen Wiedergabelisten erstellt werden.

Beispielcode


```XML
<ASX Version = "3.0">
    <TITLE>Adventure Works Radio Top 3 Rock Stations</TITLE>
    <MOREINFO href = "https://www.adventure-works.com/MyTop3Rocks"/>
    <REPEAT>
        <ENTRY ClientSkip = "no">
            <REF HREF = "https://www.adventure-works.com/ad.asp/">
        </ENTRY>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF  HREF = "https://www.adventure-works.com/asx/RadioNetwork.wax"/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork2.wax/>
        <DURATION VALUE="00:00:30" />
        <ENTRYREF HREF = "https://www.adventure-works.com/asx/RadioNetwork3.wax"/>
    </REPEAT>
</ASX>

```



In diesem Beispiel wird eine Werbeanzeige gefolgt von 30 Sekunden jeder der drei Stationen, auf die verwiesen wird, nacheinander abspielt. Dieser Zyklus wird unbegrenzt wiederholt, da das **COUNT-Attribut** des **REPEAT-Elements** nicht definiert ist.

-   Die in den Beispielen verwendeten Firmen, Organisationen, Produkte, Personen und Ereignisse sind frei erfunden, soweit nichts anderes angegeben ist. Jede Ähnlichkeit mit bestehenden Firmen, Organisationen, Produkten, Personen oder Ereignissen ist rein zufällig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metadateiwiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Beispielwiedergabelisten**](example-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Leitfaden zur Medienmetadatei**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




