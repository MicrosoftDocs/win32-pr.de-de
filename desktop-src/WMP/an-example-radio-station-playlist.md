---
title: Beispiel für eine Radio Station-Wiedergabeliste
description: Beispiel für eine Radio Station-Wiedergabeliste
ms.assetid: 99b33036-6391-446c-816c-8d5d76107d37
keywords:
- Windows Media Metadatei-Wiedergabelisten, Beispiele für Wiedergabelisten
- Wiedergabelisten, Wiedergabelisten Beispiele
- Metadatei-Wiedergabelisten, Wiedergabelisten Beispiele
- Windows Media Metadatei-Wiedergabelisten, Beispiel Wiedergabelisten
- Wiedergabelisten, Beispiel Wiedergabelisten
- Metadatei-Wiedergabelisten, Beispiel Wiedergabelisten
- Windows Media Metadatei-Wiedergabelisten, Beispiel Wiedergabelisten
- Wiedergabelisten, Beispiel Wiedergabelisten
- Metadatei-Wiedergabelisten, Beispiel Wiedergabelisten
- Windows Media Metadatei-Wiedergabelisten, Codebeispiel
- Wiedergabelisten, Codebeispiel
- Metadatei-Wiedergabelisten, Codebeispiel
- Windows Media Metadatei-Wiedergabelisten, Beispiel für Radio Station-Wiedergabeliste
- Wiedergabelisten, Beispiel für Radio Stations Wiedergabe
- Metadatendatei-Wiedergabelisten, Beispiel für Radio Stations Wiedergabe
- Windows Media Player, Wiedergabelisten Beispiele
- Windows Media Player, Beispiel Wiedergabelisten
- Windows Media Player, Beispiel Wiedergabelisten
- Beispiel für Windows Media Player, Radio Station-Wiedergabeliste
- Wiedergabelisten Beispiele
- Beispiel Wiedergabelisten
- Beispiel Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da797937ee461ccb3afbfb000e7704486d6896e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388187"
---
# <a name="an-example-radio-station-playlist"></a>Beispiel für eine Radio Station-Wiedergabeliste

Im folgenden Beispielcode wird veranschaulicht, wie Sie eine Wiedergabeliste erstellen, um drei feldepages zu scannen. Die fiktive Firma Adventure Works Radio Brand befindet sich in der Wiedergabeliste und in allen einzelnen Streams in der Wiedergabeliste. Wenn Sie Ihren Code schreiben, ändern Sie alle URLs und Dateinamen in gültige Dateinamen, die für Ihre Windows-Media Player verfügbar sind.

Für jede der Stationen wird eine Wiedergabeliste erstellt. Eine vierte Wiedergabeliste scannt die ersten drei. Die Wiedergabelisten werden erstellt, um auf dynamisch generierte Ankündigungen zu verweisen und Adventure Works Radio Branding zu haben.

Eine der Wiedergabelisten, die eine Radio Station darstellen, könnte wie folgt aussehen.


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



Die Wiedergabeliste kann dann aus verweisen auf die einzelnen Wiedergabelisten erstellt werden.

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



In diesem Beispiel wird eine Werbe einblenden, gefolgt von 30 Sekunden für jede der drei Stationen, auf die verwiesen wird, abgespielt. Dieser Cycle wird unbegrenzt wiederholt, da das **count** -Attribut des **Repeat** -Elements nicht definiert ist.

-   Die in den Beispielen verwendeten Firmen, Organisationen, Produkte, Personen und Ereignisse sind frei erfunden, soweit nichts anderes angegeben ist. Jede Ähnlichkeit mit bestehenden Firmen, Organisationen, Produkten, Personen oder Ereignissen ist rein zufällig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Beispiel Wiedergabelisten**](example-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




