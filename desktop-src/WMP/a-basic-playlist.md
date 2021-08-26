---
title: Eine einfache Wiedergabeliste
description: Eine einfache Wiedergabeliste
ms.assetid: fdd87959-861a-456e-b903-f5a27b4f6221
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
- Windows Medienmetadatei-Wiedergabelisten, einfaches Wiedergabelistenbeispiel
- Wiedergabelisten, einfaches Wiedergabelistenbeispiel
- Metadatei-Wiedergabelisten, Einfaches Wiedergabelistenbeispiel
- Beispiele für Windows Media Player, Wiedergabelisten
- Windows Media Player, Beispielwiedergabelisten
- Windows Media Player, Beispielwiedergabelisten
- Beispiel für Windows Media Player,Einfache Wiedergabeliste
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
ms.openlocfilehash: c8284acfe86cb204293902c0fb8664e74b12f3d2cc176d762f1aff079faac0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004580"
---
# <a name="a-basic-playlist"></a>Eine einfache Wiedergabeliste

Das folgende Wiedergabelistenbeispiel zeigt einen grundlegenden Satz von Wiedergabelistenelementen. Wenn Sie Ihren eigenen Code schreiben, müssen Sie alle URLs und Dateinamen in gültige Dateinamen ändern, auf die Ihre Windows Media Player zugreifen kann.

**Codebeispiel**


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



Die folgende Tabelle enthält Details zur Verwendung der einzelnen Elemente im Beispielcode.



| Linie                                                                                            | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \<ASX version = "3.0">                                                                     | Das [ASX-Element](asx-element.md) identifiziert für den Client (Windows Media Player), dass es sich um eine Windows Media-Metadateiwiedergabeliste handelt. Das  Versionsattribut gibt die Versionsnummer der Metadateielemente an.                                                                                                                                                                                                                                                                                                                                           |
| \<TITLE>Demo zur grundlegenden Wiedergabeliste\</TITLE>                                                  | Das [TITLE-Element](title-element--metafile.md) identifiziert den Titel der Wiedergabeliste als Ganzes. Windows Media Player zeigt diese Metadaten als Titel an.                                                                                                                                                                                                                                                                                                                                                                                               |
| \<ENTRY>                                                                                   | Beginnt das [ENTRY-Element.](entry-element.md) Ein **ENTRY-Element** ist eine Möglichkeit, einen bestimmten Clip in einer Wiedergabeliste zu definieren.                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<TITLE>Ein Eintrag in einer einfachen Wiedergabeliste\</TITLE>                                         | Identifiziert den Titel des Wiedergabelistenclips. Es unterscheidet sich vom vorherigen **TITLE-Element,** da dieses element innerhalb eines **ENTRY-Elements** geschachtelt ist. Windows Media Player zeigt diese Metadaten als Cliptitel an.                                                                                                                                                                                                                                                                                                                                         |
| \<AUTHOR>Microsoft Corporation\</AUTHOR>                                              | Das [AUTHOR-Element](author-element.md) identifiziert den Autor des Medienclips. Windows Media Player zeigt diese Metadaten als Clip **AUTHOR** an.                                                                                                                                                                                                                                                                                                                                                                                                         |
| \<!-- This is a comment. Change the following path to point to your Windows media file --> | Kommentar. [Kommentare](comments.md) sind nur sichtbar, wenn der Code angezeigt wird, und haben das gleiche Format wie **XML-Kommentare.**                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| \<REF HREF = "mms://proseware.com/path/Yourfile.wma" />                                    | Tatsächlicher Zeiger auf die Mediendatei. Das [REF-Element](ref-element.md) identifiziert die Zeile als Zeiger auf Medieninhalte, während das **HREF-Attribut** die URL zur Mediendatei ist. In diesem Fall verwendet die URL das MMS-Protokoll, sodass sie auf einen Windows Medienserver verweist. Mediendateien auf Dem Medienserver werden in der Regel nicht am gleichen Speicherort wie Ihre HTML-Dokumente gespeichert.<br/> Beachten Sie die Verwendung des XML-ähnlichen Schließens des Elements , "/>", anstelle von &lt; &gt; "/REF". Da dieses Element keine untergeordneten Elemente enthält, schließt es sich selbst.<br/> |
| \</ENTRY>                                                                                  | Gibt das Ende des **ENTRY-Elements** an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| \</ASX>                                                                                    | Gibt das Ende der Wiedergabeliste an.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |



 

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

 

 





