---
title: Eine erweiterte Wiedergabeliste
description: Eine erweiterte Wiedergabeliste
ms.assetid: 3f27562f-bc3b-4b7f-a83b-78317d3ad612
keywords:
- Windows Medienmetadatei-Wiedergabelisten, Wiedergabelistenbeispiele
- Wiedergabelisten, Wiedergabelistenbeispiele
- Metafile-Wiedergabelisten, Wiedergabelistenbeispiele
- Windows Medienmetadatei-Wiedergabelisten, Beispielwiedergabelisten
- Wiedergabelisten, Beispielwiedergabelisten
- Metadatei-Wiedergabelisten, Beispielwiedergabelisten
- Windows Medienmetadatei-Wiedergabelisten, Beispielwiedergabelisten
- Wiedergabelisten, Beispielwiedergabelisten
- Metadatei-Wiedergabelisten, Beispielwiedergabelisten
- Windows Medienmetadatei-Wiedergabelisten, Codebeispiel
- Wiedergabelisten, Codebeispiel
- Metadatei-Wiedergabelisten, Codebeispiel
- Windows Medienmetadatei-Wiedergabelisten, Beispiel für erweiterte Wiedergabeliste
- Wiedergabelisten, Beispiel für erweiterte Wiedergabeliste
- Metadatei-Wiedergabelisten, Beispiel für erweiterte Wiedergabeliste
- Beispiele für Windows Media Player, Wiedergabelisten
- Windows Media Player,Beispielwiedergabelisten
- Windows Media Player, Beispielwiedergabelisten
- Beispiel für Windows Media Player,erweiterte Wiedergabeliste
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
ms.openlocfilehash: 6573d5bef05c8af943368a12d03677526a9783915d6915b6cc5f1516bc9942f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583257"
---
# <a name="an-advanced-playlist"></a>Eine erweiterte Wiedergabeliste

Das folgende Wiedergabelistenbeispiel zeigt, wie Sie einen vollständigeren Satz von Wiedergabelistenelementen verwenden. Wenn Sie Ihren eigenen Code schreiben, müssen Sie alle URLs und Dateinamen in gültige Dateinamen ändern, auf die Ihre Windows Media Player zugreifen können.

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



| Linie                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                             |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| `<ASX version = "3.0">`                                                                     | Das [ASX-Element](asx-element.md) identifiziert für den Client (Windows Media Player), dass es sich um eine Windows Media-Metadateiwiedergabeliste handelt. Das  Versionsattribut gibt die Versionsnummer der Metadateielemente an.                                                                                                                    |
| `<TITLE>Advanced Playlist Demo</TITLE>`                                               | Das [TITLE-Element](title-element--metafile.md) identifiziert den Titel der Wiedergabeliste als Ganzes. Windows Media Player zeigt diese Metadaten als Titel an.                                                                                                                                                                        |
| `<ABSTRACT>More Information at this Web Site< /ABSTRACT>`                             | Das [ABSTRACT-Element](abstract-element.md) stellt die QuickInfo für den Showtitel bereit.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF ="https://www.microsoft.com/windows/windowsmedia" />`                        | Das [MOREINFO-Element](moreinfo-element.md) verknüpft den Showtitel mit einer URL. Wenn Sie den Mauszeiger über dem Titel anzeigen anhalten, wird auf die QuickInfo zugegriffen, sofern diese definiert ist. Wenn Sie den Titel anzeigen auswählen, wird die angegebene URL geöffnet.                                                                                                                |
| `<BANNER HREF = "..\\samples\\home.gif">`                                                   | Das [BANNER-Element](banner-element.md) erstellt ein Werbebanner in Windows Media Player. Das **HREF-Attribut** gibt die Bannergrafik an (die 194 Pixel breit und 32 Pixel hoch sein muss).                                                                                                                                  |
| `<ABSTRACT>MSN website</ABSTRACT>`                                                    | Das [ABSTRACT-Element](abstract-element.md) stellt die QuickInfo für das **BANNER** bereit.                                                                                                                                                                                                                                                   |
| `<MOREINFO HREF = "https://www.msn.com" </ABSTRACT>`                                      | Das [MOREINFO-Element](moreinfo-element.md) verknüpft die **BANNER-Grafik** mit einer URL. Wenn Sie den Mauszeiger über dem **BANNER** halten, wird auf eine QuickInfo zugegriffen, sofern diese definiert ist. Wenn Sie das **BANNER** auswählen, wird die angegebene URL geöffnet.                                                                                                                |
| <PARAM name = "track" value="1"/>                                                         | Das [PARAM-Element](param-element.md) definiert einen benutzerdefinierten Parameter. Das **attribut name** definiert den Namen des benutzerdefinierten Parameters als "track". Das **Value-Attribut** definiert den Wert von "track" als "1".                                                                                                                          |
| `</BANNER>`                                                                                 | Schließt das  BANNER-Element.                                                                                                                                                                                                                                                                                                           |
| `<ENTRY ClientSkip="no">`                                                                   | Startet den [ENTRY-Elementblock.](entry-element.md) Dieses Element definiert einen Clip in einer Wiedergabeliste, indem ein Link im **REF-Element** angegeben wird. Das Festlegen von **ClientSkip** auf "Nein" bedeutet, dass der Benutzer nicht schnell vorwärts oder zum nächsten Clip springen kann.                                                                                             |
| `<BANNER HREF = "..\\samples\\contact.gif">`                                                | Erstellt ein Werbebanner. **HREF** ist die Bannergrafik (194 x 32 Pixel).                                                                                                                                                                                                                                                      |
| `<ABSTRACT>Visit Our website< /ABSTRACT>`                                             | Stellt die QuickInfo für das Banner bereit.                                                                                                                                                                                                                                                                                                    |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Stellt einen Link zur URL für das Banner bereit. Wenn Sie das Banner auswählen, wird eine Verbindung mit der URL hergestellt.                                                                                                                                                                                                                                                    |
| `</BANNER>`                                                                                 | Schließt das  BANNER-Element.                                                                                                                                                                                                                                                                                                           |
| `<MOREINFO HREF = "https://www.msn.com" />`                                                  | Stellt einen Link zur URL für den **Titeltext** des Clips bereit.                                                                                                                                                                                                                                                                                 |
| `<!--This is the ToolTip text for the Title text -->`                                       | Kommentar. [Kommentare](comments.md) sind nur sichtbar, wenn der Code angezeigt wird.                                                                                                                                                                                                                                                        |
| `<Abstract>Visit the YourImage website</abstract>`                                    | Stellt die QuickInfo für den **Titeltext** des Clips bereit.                                                                                                                                                                                                                                                                                       |
| `<TITLE>The first entry in an advanced playlist</TITLE>`                              | Identifiziert den Titel des Clips. Es handelt sich um den Clip **TITLE,** da er in einem **ENTRY-Element** geschachtelt ist. Windows Media Player zeigt diese Metadaten als Cliptitel an.                                                                                                                                                             |
| `<AUTHOR>YourImage</AUTHOR>`                                                          | Identifiziert den Autor des Medienclips. Diese Metadaten werden als Clip **AUTHOR** von Windows Media Player angezeigt.                                                                                                                                                                                                                     |
| `<COPYRIGHT>(c)2000 YourImage</COPYRIGHT>`                                            | Das [COPYRIGHT-Element](copyright-element.md) gibt die dem Medienclip zugeordneten Copyrights an. Windows Media Player zeigt diese Metadaten als Clip COPYRIGHT an.                                                                                                                                                              |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Ein Kommentar im gleichen Format wie **XML-Kommentare.**                                                                                                                                                                                                                                                                                      |
| `<REF HREF = "..\\media\\laure.wma" />`                                                     | URL für den Medieninhalt. Das [REF-Element](ref-element.md) identifiziert die Zeile als Zeiger auf Medieninhalte. Das **HREF-Attribut** ist die URL zur Datei. Beachten Sie die Verwendung des XML-ähnlichen Schließens des Elements , "/>" anstelle von &lt; &gt; "/REF". Da dieses Element keine untergeordneten Elemente enthält, schließt es sich selbst.<br/> |
| `</ENTRY>`                                                                                  | Gibt das Ende des ersten **ENTRY-Elements** an.                                                                                                                                                                                                                                                                                |
| `<ENTRY>`                                                                                   | Beginnt das zweite **ENTRY-Element.**                                                                                                                                                                                                                                                                                                    |
| `<TITLE>The second Entry in the advanced playlist</TITLE>`                            | Identifiziert den Titel des zweiten Clips.                                                                                                                                                                                                                                                                                                |
| `<AUTHOR>Microsoft Corporation</AUTHOR>`                                              | Identifiziert den Autor des zweiten Medienclips.                                                                                                                                                                                                                                                                                         |
| `<!--This is the ToolTip text for the Title/Author/Copyright text -->`                      | Kommentar. Sie ist nur sichtbar, wenn der Code angezeigt wird.                                                                                                                                                                                                                                                                             |
| `<ABSTRACT>This is where you can include your tool tips</ABSTRACT>`                   | Dies ist der QuickInfo-Text für den **TITLE-Text** des Clips.                                                                                                                                                                                                                                                                            |
| `<!-- This is a comment. Change the following path to point to your Windows Media file -->` | Kommentar. Sie ist nur sichtbar, wenn der Code angezeigt wird.                                                                                                                                                                                                                                                                             |
| `<REF HREF = ..\\media\\mellow.wma" />`                                                     | Identifiziert die Zeile als Zeiger auf Medieninhalte. Das **HREF-Attribut** ist die URL zur Datei.                                                                                                                                                                                                                                       |
| `</ENTRY>`                                                                                  | Gibt das Ende des zweiten **ENTRY-Elements** an.                                                                                                                                                                                                                                                                                      |
| `</ASX>`                                                                                    | Gibt das Ende der Wiedergabeliste an.                                                                                                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen von Metafile-Wiedergabelisten**](creating-metafile-playlists.md)
</dt> <dt>

[**Beispielwiedergabelisten**](example-playlists.md)
</dt> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Media Metafile Guide**](windows-media-metafile-guide.md)
</dt> </dl>

 

 





