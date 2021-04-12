---
title: Erstellen von Metafile-Wiedergabelisten
description: Erstellen von Metafile-Wiedergabelisten
ms.assetid: 0afe3aaa-bcd1-4060-8772-add50f3b6bac
keywords:
- Windows Media Metadatei-Wiedergabelisten, erstellen
- Wiedergabelisten, erstellen
- Metadatei-Wiedergabelisten, erstellen
- Erstellen von Windows Media-Metadatei-Wiedergabelisten
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d4acff6452640c3f0b66219b765a931033b9f3a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207111"
---
# <a name="creating-metafile-playlists"></a>Erstellen von Metafile-Wiedergabelisten

Sie können eine Wiedergabeliste mit einem beliebigen Text-Editor erstellen, z. b. Microsoft Notepad. Öffnen Sie den Text-Editor. Geben Sie die Skript Einträge ein, die Sie implementieren möchten. Nachdem Sie die Eingabe in Notepad abgeschlossen haben, speichern Sie die Datei mit einem entsprechenden Dateinamen und einer Dateinamenerweiterung. Weitere Informationen zu Erweiterungen finden Sie unter [Richtlinien für metadateierweiterungen](metafile-extension-guidelines.md). In der Regel ist der Dateiname der Name der Windows Media-Datei oder des Streams, gefolgt von der Erweiterung. Wax,. wvx oder. ASX. Wenn Ihr Medieninhalt z. b. eine Windows Media-Audiodatei mit der Erweiterung. WMA ist, verwenden Sie die Erweiterung. Wax, wenn Sie die Wiedergabeliste benennen. Wiedergabelisten dürfen keine Formatierungscodes eines Textprozessors enthalten, wie z. b. Microsoft Word. Speichern Sie die Datei als nur-Text-oder ASCII-Datei, um sicherzustellen, dass keine Formatierungscodes in der Wiedergabeliste enthalten sind.

> [!Note]  
> Bei Elementen und Attributen wird Groß-/Kleinschreibung nicht beachtet Der Text, der in der Wiedergabeliste zum Definieren eines Elements oder Attributs verwendet wird, kann entweder groß-oder Kleinbuchstaben oder eine Kombination aus beidem sein.

 

Wenn ein Element über keine untergeordneten Elemente verfügt (solche, die sich in einem anderen Element ändern oder befinden), kann ein einzelner Schrägstrich (/) am Ende des öffnenden Tags direkt vor dem ">" anstelle eines Endtags verwendet werden. Untergeordnete Elemente eines Elements müssen zwischen dem öffnenden und dem schließenden Tag für dieses Element angezeigt werden. Andernfalls sind Sie keine untergeordneten Elemente für dieses Element und werden ignoriert, oder es wird ein Fehler in der Syntax der Wiedergabeliste verursacht.

Die ersten vier Zeichen einer Wiedergabeliste müssen " &lt; ASX" lauten. Das Element " **ASX** " wird in allen Wiedergabelisten verwendet, unabhängig davon, ob die Erweiterung. Wax,. wvx oder. ASX ist. Es darf nur ein **ASX** -Element pro Wiedergabeliste vorhanden sein. Dieses Element identifiziert die Datei als Windows Media-Metadatei-Wiedergabeliste. Der Typ der Wiedergabeliste wird nicht angegeben.

Das Element " **ASX** " hat drei mögliche Attribute:

**VERSION**

Das **Versions** Attribut ist erforderlich und muss unmittelbar hinter dem Element " **ASX** " folgen, z. b. "<-Version =" 3,0 " &gt; ". Die aktuelle Versionsnummer ist 3,0. Windows Media Player unterstützt alle vorherigen Versionen. Zulässige Werte für das **Versions** Attribut sind 3,0 und 3 (ohne Dezimaltrennzeichen).

**PREVIEWMODE**

Das **PreviewMode** -Attribut ist optional. Es bietet einen weiteren Mechanismus zum angeben, wie lange ein Clip dargestellt werden soll. Wenn der Wert des **PreviewMode** -Attributs auf "yes" festgelegt ist, renderMedia Player jedes Clip für die Dauer, die durch das Element " **previewduration**" angegeben wird. Für jeden Clip kann eine **previewduration** angegeben werden.

**Bannerbar**

Das optionale **bannerbar** -Attribut definiert, ob das Windows Media Player-Steuerelement Platz für eine Banner Grafik reserviert. (Verwenden Sie das **Banner** -Element, um die anzuzeigende Grafik anzugeben.) Wenn der Wert von " **bannerbar** " festgelegt ist, reserviert Windows Media Player Bannerbereich für die Anzeige und für jeden Clip, ob die Metadatei-Wiedergabeliste ein Banner für die Anzeige oder den Clip angibt. Dadurch wird die Größe des Fensters "Windows Media Player" unverändert gehalten (es sei denn, die Videogröße wird geändert), unabhängig davon, ob eine Banner Grafik vorhanden ist oder nicht. Wenn dem anzeigen oder Clip kein Banner zugeordnet ist, ist der reservierte Speicherplatz schwarz. Wenn der Wert des **bannerbar** -Attributs "Auto" ist, reserviert Windows Media Player Platz für das Banner nur dann, wenn die Anzeige oder der Clip eine enthält.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >

```



Weitere Informationen zu den drei Attributen des **-Elements für das-** Element finden Sie im Referenz Eintrag für das-Element von [ASX](asx-element.md).

Ein **ASX** -Element enthält untergeordnete **Eintrags** Elemente, die Informationen zu den Mediendateien definieren, auf die zugegriffen werden soll. Jedes **Entry** -Element muss ein **ref** -Element enthalten, das den Pfad zu der Mediendatei angibt, die gestreamt werden soll. Es muss mindestens ein **Entry** -oder **ENTRYREF** -Element in einem **ASX** -Element vorhanden sein.

Andere Elemente, die im Gültigkeitsbereich des **ASX** -Elements definiert sind, z. b. **Title** und **Author**, werden den von Windows Media Player angezeigten Metadaten zugeordnet.

Die einfachsten Wiedergabelisten werden erstellt, indem einer Metadatei mehrere **Entry** -Elemente mit einem einzelnen **ref** -Element hinzugefügt werden. Jedes **Entry** -Element in einer Metadatei-Wiedergabeliste wird in der Reihenfolge gerendert, in der es in der Datei angezeigt wird, als ob der Benutzer den einzelnen Clip manuell

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



Stellen Sie sicher, dass die Wiedergabeliste funktioniert, indem Sie in Windows-Explorer darauf doppelklicken. Windows Media Player sollte geöffnet werden und mit dem Streamen der Medieninhalte beginnen. Nachdem Sie sich vergewissert haben, dass die Wiedergabeliste funktioniert, speichern Sie sie zusammen mit ihren Webseiten auf Ihrem Webserver, und verknüpfen Sie Sie über ein **href** -Element, oder Betten Sie Sie mithilfe des Windows-Media Player **Object** -Elements in eine Webseite ein.

Die folgenden Abschnitte enthalten weitere Informationen:

-   [Schachteln von Metadateien](nesting-metafiles.md)
-   [Verwenden von ASP-Seiten zum dynamischen Erstellen von Windows Media Metafile-Wiedergabelisten](using-asp-pages-to-dynamically-create-windows-media-metafile-playlists.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Banner-Element**](banner-element.md)
</dt> <dt>

[**Beispiel Wiedergabelisten**](example-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




