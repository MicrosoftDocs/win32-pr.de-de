---
title: Eine einfache Wiedergabeliste
description: Eine einfache Wiedergabeliste
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Windows Media Metadatei-Wiedergabelisten, einfaches Beispiel für Wiedergabeliste
- Wiedergabelisten, einfaches Wiedergabelisten Beispiel
- Metadatei-Wiedergabelisten, einfaches Beispiel für Wiedergabeliste
- Windows Media Player, Wiedergabelisten Beispiele
- Windows Media Player, Beispiel Wiedergabelisten
- Windows Media Player, Beispiel Wiedergabelisten
- Beispiel für Windows Media Player, einfache Wiedergabeliste
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
ms.openlocfilehash: 93bdd9b8ace378c4bcb5b3d6fa98bf3a690e8b60
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037463"
---
# <a name="a-basic-playlist"></a>Eine einfache Wiedergabeliste

Das folgende Wiedergabelisten Beispiel zeigt einen einfachen Satz von Wiedergabelisten Elementen. Wenn Sie Ihren eigenen Code schreiben, müssen Sie alle URLs und Dateinamen in gültige Dateinamen ändern, die für Ihre Windows-Media Player verfügbar sind.

**Code Beispiel**


```XML
<ASX version = "3.0">
<TITLE>Basic Playlist Demo</TITLE>
    <ENTRY>
        <TITLE>An Entry in a basic playlist</TITLE>
        <AUTHOR>Microsoft Corporation</AUTHOR>
        <COPYRIGHT>(c)2000 Microsoft Corporation</COPYRIGHT>
        <REF HREF = "mms://proseware.com/path/Yourfile.wma" />
    </ENTRY>
</ASX>

```



In der folgenden Tabelle finden Sie ausführliche Informationen zur Verwendung der einzelnen Elemente im Beispielcode.



| Zeile                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <ASX version = "3.0">                                                                     | Das Element " [ASX](asx-element.md) " identifiziert für den Client (Windows Media Player), dass es sich hierbei um eine Windows Media Metadatei-Wiedergabeliste handelt. Das **Versions** Attribut gibt die Versionsnummer der Metadateielemente an.                                                                                                                                                                                                                                                                                                                                           |
| <TITLE>Grundlegende Wiedergabelisten Demo</TITLE>                                                  | Das [Title](title-element--metafile.md) -Element identifiziert den Titel der Wiedergabeliste als Ganzes. In Windows Media Player werden diese Metadaten als Show-Titel angezeigt.                                                                                                                                                                                                                                                                                                                                                                                               |
| <ENTRY>                                                                                   | Startet das [Eintrags](entry-element.md) Element. Ein **Entry** -Element ist eine Möglichkeit, einen bestimmten Clip in einer Wiedergabeliste zu definieren.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <TITLE>Ein Eintrag in einer einfachen Wiedergabeliste</TITLE>                                         | Gibt den Titel des Wiedergabelisten Clips an. Sie unterscheidet sich vom vorherigen **Title** -Element, da dieses in einem **Entry** -Element geschachtelt ist. Windows Media Player zeigt diese Metadaten als Clip Titel an.                                                                                                                                                                                                                                                                                                                                         |
| <AUTHOR>Microsoft Corporation</AUTHOR>                                              | Das [Author](author-element.md) -Element identifiziert den Autor des Medienclips. Windows Media Player zeigt diese Metadaten als Clip **Autor** an.                                                                                                                                                                                                                                                                                                                                                                                                         |

| <!-- This is a comment. Change the following path to point to your Windows media file --> | Ein Kommentar. [Kommentare](comments.md) sind nur sichtbar, wenn der Code angezeigt wird, und weisen das gleiche Format wie **XML** -Kommentare auf.                                                                                                                                                                                                                                                                                                                                                                                                                                  | | <REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | Tatsächlicher Zeiger auf die Mediendatei. Das [ref](ref-element.md) -Element identifiziert die Zeile als Zeiger auf den Medieninhalt, während das **href** -Attribut die URL der Mediendatei ist. In diesem Fall verwendet die URL das MMS-Protokoll, sodass Sie auf einen Windows Media-Server verweist. Mediendateien auf dem Medienserver werden in der Regel nicht am gleichen Speicherort wie Ihre HTML-Dokumente gespeichert.<br/> Beachten Sie die Verwendung des XML-ähnlichen Schließens des Elements "/>" anstelle von " &lt; /ref &gt; ". Da dieses Element nicht über untergeordnete Elemente verfügt, wird es selbst geschlossen.<br/> | | </ENTRY>                                                                                  | Gibt das Ende des **Eintrags** Elements an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | | </ASX>                                                                                    | Gibt das Ende der Wiedergabeliste an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

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

 

 





