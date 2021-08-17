---
title: Erstellen von Metadateiwiedergabelisten
description: Erstellen von Metadateiwiedergabelisten
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Windows Wiedergabelisten von Medienmetadateien, Erstellen
- Wiedergabelisten,erstellen
- Metafile-Wiedergabelisten,erstellen
- Erstellen Windows Medienmetadatei-Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 765d8ab507c2ce502f1cad021696b0fc2ecfd110da8dfa95ccc84a43a8987561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750467"
---
# <a name="creating-metafile-playlists"></a>Erstellen von Metadateiwiedergabelisten

Sie können eine Wiedergabeliste mit einem beliebigen Text-Editor erstellen, z. B. microsoft Editor. Öffnen Sie den Text-Editor. Geben Sie die Skripteinträge ein, die Sie implementieren möchten. Nachdem Sie die Eingabe in Editor, speichern Sie die Datei mit einem entsprechenden Dateinamen und einer entsprechenden Dateierweiterung. Weitere Informationen zu Erweiterungen finden Sie unter [Metafile Extension Guidelines](metafile-extension-guidelines.md). In der Regel ist der Dateiname der Name der Windows Media-Datei oder des Datenstroms, gefolgt von der Erweiterung ".dateityp", ".wvx" oder ".asx". Wenn ihr Medieninhalt z. B. eine Windows Media-Audiodatei mit der Erweiterung .wma ist, verwenden Sie beim Benennen der Wiedergabeliste die Erweiterung .extension. Wiedergabelisten dürfen keine Formatierungscodes von einem Textprozessor enthalten, z. B. Microsoft Word. Um sicherzustellen, dass keine Formatierungscodes in der Wiedergabeliste enthalten sind, speichern Sie die Datei als Nur-Text- oder ASCII-Datei.

> [!Note]  
> Bei Elementen und Attributen wird die Kleinschreibung nicht beachtet. Der Text, der in der Wiedergabeliste zum Definieren eines Elements oder Attributs verwendet wird, kann groß- oder klein geschrieben oder eine Mischung aus beidem sein.

 

Wenn ein Element keine untergeordneten Elemente enthält (elemente, die ändern oder in einem anderen Element enthalten sind), kann ein einzelner Schrägstrich (/) am Ende des öffnenden Tags direkt vor dem ">" statt eines schließenden Tags verwendet werden. Untergeordnete Elemente eines Elements müssen zwischen dem öffnenden und dem schließenden Tag für dieses Element angezeigt werden. andernfalls sind sie keine untergeordneten Elemente für dieses Element und werden ignoriert oder verursachen einen Fehler in der Syntax der Wiedergabeliste.

Die ersten vier Zeichen einer Wiedergabeliste müssen &lt; "ASX" sein. Das **ASX-Element** wird in allen Wiedergabelisten verwendet, unabhängig davon, ob die Erweiterung .playlist, .wvx oder .asx ist. Pro Wiedergabeliste darf nur ein **ASX-Element** enthalten sein. Dieses Element identifiziert die Datei als Wiedergabeliste Windows Medienmetadatei. Der Typ der Wiedergabeliste wird nicht angegeben.

Das **ASX-Element** verfügt über drei mögliche Attribute:

**VERSION**

Das **VERSION-Attribut** ist erforderlich und muss unmittelbar nach dem **ASX-Element** folgen, z. B. "<ASX version = "3.0" &gt; ". Die aktuelle Versionsnummer ist 3.0. Windows Media Player unterstützt alle vorherigen Versionen. Zulässige Werte für das **VERSION-Attribut** sind 3.0 und 3 (ohne Dezimaltrennzeichen).

**PREVIEWMODE**

Das **PREVIEWMODE-Attribut** ist optional. Es stellt einen weiteren Mechanismus zum Angeben der Länge des Renderns eines Clips dar. Wenn der Wert des **PREVIEWMODE-Attributs** YES ist, rendert Windows Media Player jeden Clip für die dauer, die durch das **Element PREVIEWDURATION angegeben wird.** Für jeden Clip kann **PREVIEWDURATION angegeben** werden.

**BANNERBAR**

Das **optionale BANNERBAR-Attribut** definiert, ob das Windows Media Player-Steuerelement Platz für eine Bannergrafik reserviert. (Verwenden Sie das **BANNER-Element,** um die anzuzeigende Grafik anzugeben.) Wenn der Wert von **BANNERBAR** FEST ist, reserviert Windows Media Player Bannerraum für die Show und für jeden Clip, unabhängig davon, ob die Metadateiwiedergabeliste ein Banner für die Show oder den Clip angibt. Dadurch bleibt die Größe des Windows Media Player-Fensters gleich (es sei denn, die Videogröße ändert sich), unabhängig davon, ob eine Bannergrafik vor ort ist. Wenn der Show oder dem Clip kein Banner zugeordnet ist, ist der reservierte Speicherplatz schwarz. Wenn der Wert des **BANNERBAR-Attributs** AUTO ist, reserviert Windows Media Player Platz für das Banner nur, wenn die Show oder der Clip ein Banner enthält.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



Weitere Informationen zu den drei Attributen des **ASX-Elements** finden Sie im Verweiseintrag für das [ASX-Element.](asx-element.md)

Ein **ASX-Element** enthält untergeordnete **ENTRY-Elemente,** die Informationen zu den Mediendateien definieren, auf die zugegriffen werden soll. Jedes **ENTRY-Element** muss ein **REF-Element** enthalten, das den Pfad zur zu streamenden Mediendatei angibt. In einem ASX-Element muss mindestens ein **ENTRY-** oder **ENTRYREF-Element** **enthalten** sein.

Andere Elemente, die innerhalb des Bereichs des **ASX-Elements** definiert sind, z. B. **TITLE** und **AUTHOR,** werden den Metadaten zugeordnet, die von der Windows Media Player.

Die einfachsten Wiedergabelisten werden erstellt, indem einer Metadatei mehrere **ENTRY-Elemente** mit einem **einzelnen REF-Element** hinzugefügt werden. Jedes **ENTRY-Element** in einer Metadateiwiedergabeliste wird in der Reihenfolge gerendert, in der es in der Datei angezeigt wird, als ob der Benutzer jeden Clip manuell geöffnet hätte.

Beispielcode


```XML
<ASX version = "3.0">
<!--A simple playlist with entries to be played in sequence.-->
    <Title>The Show Title</Title>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title1.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title2.wma" />
    </Entry>
    <Entry>
        <Ref href = "mms://adventure-works.com/Path/title3.wma" />
    </Entry>
</ASX>

```



Stellen Sie sicher, dass die Wiedergabeliste funktioniert, indem Sie im Windows doppelklicken. Windows Media Player sollte den Medieninhalt öffnen und mit dem Streamen beginnen. Nachdem Sie bestätigt haben, dass die Wiedergabeliste funktioniert, speichern Sie sie zusammen mit Ihren Webseiten auf Ihrem Webserver, und verknüpfen Sie sie mithilfe eines **HREF-Elements,** oder betten Sie sie mithilfe des Windows Media Player **OBJECT-Elements** in eine Webseite ein.

Die folgenden Abschnitte enthalten weitere Informationen:

-   [Schachteln von Metadateien](nesting-metafiles.md)
-   [Verwenden von ASP-Seiten zum dynamischen Erstellen Windows Medienmetadatei-Wiedergabelisten](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**BANNER-Element**](banner-element.md)
</dt> <dt>

[**Beispielwiedergabelisten**](example-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Leitfaden zur Medienmetadatei**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




