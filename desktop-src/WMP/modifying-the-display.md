---
title: Ändern der Anzeige
description: Ändern der Anzeige
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Windows Media Metadatei-Wiedergabelisten, Ändern von anzeigen
- Wiedergabelisten, Ändern von anzeigen
- Metadatei-Wiedergabelisten, Ändern von anzeigen
- Windows Media Metadatei-Wiedergabelisten, Änderung anzeigen
- Wiedergabelisten, Änderung anzeigen
- Metadatei-Wiedergabelisten, Änderung anzeigen
- Windows Media Player, Änderung anzeigen
- Windows Media Player, Ändern von anzeigen
- Windows Media Player, Texteigenschaften
- Windows Media Player, Bildeigenschaften
- Eigenschaften von Windows Media Player, morumfo
- Windows Media Player, abstrakter Text
- Moreingefo-Eigenschaften
- Abstrakter Text
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: c5c36c55b455b797446cde627449ea705b3bd2ce
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036748"
---
# <a name="modifying-the-display"></a>Ändern der Anzeige

Wiedergabelisten können die Windows Media Player-Benutzeroberfläche auf vier verschiedene Arten ändern:

-   Text Eigenschaften
-   Image-Eigenschaften
-   Moreingefo-Eigenschaften
-   Abstrakter Text

## <a name="text-properties"></a>Text Eigenschaften

Windows Media Player ermöglicht das Anzeigen von Text für Titel, Autor, Copyright und Beschreibungs Metadaten. Clip-Metadaten können aus dem Stream oder der Mediendatei stammen, oder Sie können aus einer Wiedergabeliste stammen. Metadaten anzeigen stammt aus der Wiedergabeliste. Im Allgemeinen sind Wiedergabelisten eine bessere Methode, Texteigenschaften an Windows-Media Player zu übergeben, insbesondere, wenn sich Textelemente wahrscheinlich ändern. Es ist einfacher, Text in einer Wiedergabeliste zu bearbeiten, als eine Mediendatei neu zu erstellen. Und da aus einer Wiedergabeliste gelesene Eigenschaften die in der Mediendatei enthaltenen Eigenschaften überschreiben, können Sie den Anzeige Text einfach aktualisieren, indem Sie den neuen Text der entsprechenden Eigenschaft in einer Wiedergabeliste hinzufügen. Im folgenden Beispiel überschreibt der Text der Titel-und Author-Metadaten in der Wiedergabeliste den Titel und den Autor Text, der in der Mediendatei Sample. WMA enthalten ist.

Der **Beschreibungs** Text wird aus einer Windows-Mediendatei abgerufen, auf die in einem **Entry** -Element verwiesen wird, es sei denn, es gibt ein **abstraktes** Element in einer Wenn **abstrakter** Text vorhanden ist, wird er angezeigt, und der **Beschreibungs** Text wird überschrieben.


```XML
<ASX version="3.0" BANNERBAR="AUTO" >
    <ENTRY>
        <BANNER HREF="YourPath\2.gif">
        </BANNER>
        <TITLE>Upgrade</TITLE>
        <AUTHOR>Ad Department</AUTHOR>
        <REF href="YourPath\sample.wma"/>
    </ENTRY>
</ASX>

```



## <a name="image-properties"></a>Image-Eigenschaften

Banner Bilder können der Benutzeroberfläche von Windows Media Player hinzugefügt werden. Die Grafik kann für Werbung, Bereitstellung von Informationen und Bereitstellung von Zugriff auf Websites verwendet werden, um einige Möglichkeiten zu benennen.

Verwenden Sie das **Banner** -Element, um ein Grafik Bild (32 Pixel hoch um 194 Pixel breit) für die Anzeige durch Windows Media Player anzugeben. Die Grafik wird unterhalb der Videoinhalte angezeigt. Ein Link kann dem Banner mithilfe des untergeordneten **Morein FO** -Elements hinzugefügt werden.

Eine QuickInfo kann von einem **abstrakten** Element innerhalb des Gültigkeits Bereichs des **Banner** Elements definiert werden. Jeder definierte QuickInfo-Text kann angezeigt werden, indem der Mauszeiger über der Banner Grafik angehalten wird. Wenn Sie die Banner Grafik mit dem Mauszeiger auswählen, wird ein beliebiger Hyperlink aktiviert, der mit dem Element **Moran FO** definiert ist.

Das bevorzugte **Banner** Grafikformat ist das GIF-Format. Das JPG-Format kann verwendet werden, wenn die Grafik ordnungsgemäß formatiert ist.

Das vorherige Beispiel veranschaulicht die Verwendung des **Banner** -Elements.

> [!Note]  
> **Banner** Bilder werden bei DRM-Dateien nicht unterstützt, oder wenn Windows Media Player in eine Webseite eingebettet ist.

 

Weitere Informationen zu Banner finden Sie unter [benutzerdefinierte Grafiken in Windows Media Player](custom-graphics-in-windows-media-player.md).

## <a name="moreinfo-properties"></a>Moreingefo-Eigenschaften

Text-und Bildbereiche der Benutzeroberfläche können URLs zugeordnet werden. Während der Wiedergabe können Benutzer einen dieser Abschnitte auswählen, um eine Verbindung mit der zugeordneten URL in Ihrem Webbrowser herzustellen. Beispielsweise können Sie die Website eines Werbe einbilds wie im folgenden Code Ausschnitt gezeigt einem Werbebanner Bild zuordnen.


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a>Abstrakter Text

Der **abstrakte** Text wird verwendet, um eine kurze Popup Beschreibung der Text-oder Bildbereiche der Benutzeroberfläche anzuzeigen, der er zugeordnet ist. Wenn der Mauszeiger während der Wiedergabe auf einen dieser Bereiche zeigt, wird neben dem Mauszeiger eine QuickInfo mit dem **abstrakten** Text angezeigt, der dem Bereich zugeordnet ist. Der **abstrakte** Text wird aus einer Metadatei abgerufen und mit dem **abstrakten** Element definiert. Das **abstrakte** Element kann ein untergeordnetes Element eines- **Eintrags** oder eines **Banner** -Elements sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Leitfaden für Windows Media-Metadateien**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




