---
title: Eine erweiterte Wiedergabeliste
description: Eine erweiterte Wiedergabeliste
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
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
- Windows Media Metadatei-Wiedergabelisten, Beispiel für erweiterte Wiedergabelisten
- Wiedergabelisten, Beispiel für erweiterte Wiedergabelisten
- Metadatei-Wiedergabelisten, Beispiel für erweiterte Wiedergabelisten
- Windows Media Player, Wiedergabelisten Beispiele
- Windows Media Player, Beispiel Wiedergabelisten
- Windows Media Player, Beispiel Wiedergabelisten
- Windows Media Player, Beispiel für erweiterte Wiedergabelisten
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
ms.openlocfilehash: f52251fedb13d41be5c94706bee4460c3f13c1e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036752"
---
# <a name="an-advanced-playlist"></a>Eine erweiterte Wiedergabeliste

Im folgenden Wiedergabelisten Beispiel wird gezeigt, wie ein ausführlichere Satz von Wiedergabelisten Elementen verwendet wird. Wenn Sie Ihren eigenen Code schreiben, müssen Sie alle URLs und Dateinamen in gültige Dateinamen ändern, die für Ihre Windows-Media Player verfügbar sind.

Beispielcode


``` XML
<ASX version = "3.0">
    <TITLE>Advanced Playlist Demo</TITLE>
    <ABSTRACT>More Information at this website</ABSTRACT>
    <MOREINFO HREF="https://www.microsoft.com/windows/windowsmedia" />
    <BANNER HREF = "..\samples\home.gif">
        <ABSTRACT>MSN website</ABSTRACT>
        <MOREINFO HREF = "https://www.msn.com" />
    </BANNER>
    <PARAM name="track" value="1"/>
    <ENTRY ClientSkip="no">
        <BANNER HREF = "..\sample\contact.gif">
            <ABSTRACT>Visit Our website</ABSTRACT>
            <MOREINFO HREF = "https://www.msn.com" />
        </BANNER>
        <MOREINFO HREF = "https://www.msn.com" />
        <!-- This is the ToolTip text for Title/Author/Copyright text -->
        <ABSTRACT>Visit the YourImage website</ABSTRACT>
        <TITLE>The first entry in an advanced playlist</TITLE>
        <AUTHOR>YourImage</AUTHOR>
        <COPYRIGHT>(c)2000 YourImage</COPYRIGHT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
         <REF HREF = "..\media\laure.wma" />
    </ENTRY>

    <ENTRY>
        <TITLE>The second entry in the advanced playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <!-- This is the ToolTip text for Title text -->
        <ABSTRACT>This is where you can include your tool tips</ABSTRACT>
        <!-- This is a comment.  Change the following path to point to 
            your Windows Media file -->
        <REF HREF = "..\media\mellow.wma" />
    </ENTRY>
</ASX>

```



In der folgenden Tabelle wird die vorangehende erweiterte Wiedergabeliste beschrieben.



| Zeile                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | Das Element " [ASX](asx-element.md) " identifiziert für den Client (Windows Media Player), dass es sich hierbei um eine Windows Media Metadatei-Wiedergabeliste handelt. Das **Versions** Attribut gibt die Versionsnummer der Metadateielemente an.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | Das [Title](title-element--metafile.md) -Element identifiziert den Titel der Wiedergabeliste als Ganzes. In Windows Media Player werden diese Metadaten als Show-Titel angezeigt.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | Das [abstrakte](abstract-element.md) Element stellt die QuickInfo für den Show-Titel bereit.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | Das [moreinfo](moreinfo-element.md) -Element verknüpft den Show-Titel mit einer URL. Wenn Sie den Mauszeiger über den Show-Titel bewegen, greift auf die QuickInfo zu, falls definiert. Wenn Sie den Titel anzeigen auswählen, wird die festgelegte URL geöffnet.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | Das [Banner](banner-element.md) -Element erstellt ein Werbe Banner in Windows Media Player. Das **href** -Attribut gibt die Banner Grafik an (die 194 Pixel breit und 32 Pixel hoch sein muss).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | Das [abstrakte](abstract-element.md) Element stellt die QuickInfo für das **Banner** bereit.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | Das [Moran FO](moreinfo-element.md) -Element verknüpft die **Banner** Grafik mit einer URL. Wenn Sie mit dem Mauszeiger auf das **Banner** zugreifen, wird eine QuickInfo angezeigt, sofern definiert. Wenn Sie das **Banner** auswählen, wird die festgelegte URL geöffnet.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | Das [param](param-element.md) -Element definiert einen benutzerdefinierten Parameter. Mit dem **Name** -Attribut wird der Name des benutzerdefinierten Parameters als "Track" definiert. Das **value** -Attribut definiert den Wert von "Track" als "1".                                                                                                                          |
| `</BANNER>`                                                                                 | Schließt das **Banner** Element.                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Beginnt den Block " [Entry](entry-element.md) Element". Dieses Element definiert einen Clip in einer Wiedergabeliste durch Angeben eines Links im **ref** -Element. Wenn **clientskip** auf "No" festgelegt wird, kann der Benutzer nicht schnell vorwärts wechseln oder zum nächsten Clip springen.                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Erstellt ein Werbebanner. Der **href** ist die Banner Grafik (194x32 Pixel).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Stellt die QuickInfo für das Banner bereit.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Stellt einen Link zur URL für das Banner bereit. Die Auswahl des Banners stellt eine Verbindung mit der URL her.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Schließt das **Banner** Element.                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Stellt einen Link zur URL für den Clip **Titel** Text bereit.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Kommentar. [Kommentare](comments.md) sind nur sichtbar, wenn der Code angezeigt wird.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Stellt die QuickInfo für den Clip **Titel** Text bereit.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Gibt den Titel des Clips an. Dies ist der Clip- **Titel** , da er in einem **Entry** -Element geschachtelt ist. Windows Media Player zeigt diese Metadaten als Clip Titel an.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Identifiziert den Autor des Medienclips. Diese Metadaten werden als Clip- **Autor** von Windows Media Player angezeigt.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | Das [Copyright](copyright-element.md) -Element gibt die dem Medien Clip zugeordneten Urheberrechte an. In Windows Media Player werden diese Metadaten als Clip Copyright angezeigt.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Ein Kommentar im gleichen Format wie **XML** -Kommentare.                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | Die URL für den Medieninhalt. Das [ref](ref-element.md) -Element identifiziert die Zeile als Zeiger auf den Medieninhalt. Das **href** -Attribut ist die URL der Datei. Beachten Sie die Verwendung des XML-ähnlichen Schließens des Elements "/>" anstelle von " &lt; /ref &gt; ". Da dieses Element nicht über untergeordnete Elemente verfügt, wird es selbst geschlossen.<br/> |
| `</ENTRY>`                                                                                  | Gibt das Ende der des ersten **Entry** -Elements an.                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Startet das zweite **Entry** -Element.                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Gibt den Titel des zweiten Clips an.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Identifiziert den Autor des zweiten Medienclips.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Kommentar. Er ist nur sichtbar, wenn der Code angezeigt wird.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Dies ist der QuickInfo-Text für den **Titeltext** des Clips.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Kommentar. Er ist nur sichtbar, wenn der Code angezeigt wird.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Identifiziert die Zeile als Zeiger auf Medieninhalt. Das **href** -Attribut ist die URL der Datei.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Gibt das Ende des zweiten **Entry** -Elements an.                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Gibt das Ende der Wiedergabeliste an.                                                                                                                                                                                                                                                                                                      |



 

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

 

 





