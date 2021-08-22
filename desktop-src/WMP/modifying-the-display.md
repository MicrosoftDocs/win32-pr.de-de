---
title: Ändern der Anzeige
description: Ändern der Anzeige
ms.assetid: 21d68a34-d3d8-4b5b-b8fe-0489dc6247ec
keywords:
- Windows Wiedergabelisten von Medienmetadateien, Ändern von Anzeigen
- Wiedergabelisten,Ändern von Anzeigen
- Metafile-Wiedergabelisten, Ändern von Anzeigen
- Windows Wiedergabelisten von Medienmetadateien, Änderung der Anzeige
- Wiedergabelisten,Anzeigeänderung
- Metafile-Wiedergabelisten,Anzeigeänderung
- Windows Media Player,Anzeigeänderung
- Windows Media Player,Ändern von Anzeigen
- Windows Media Player,Texteigenschaften
- Windows Media Player,Imageeigenschaften
- Windows Media Player,MOREINFO-Eigenschaften
- Windows Media Player,ABSTRACT-Text
- MOREINFO-Eigenschaften
- ABSTRACT-Text
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1e18ca15f71d9d25d9c99db36683a61b52057580022805c9d5f0f0d250aa738a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054608"
---
# <a name="modifying-the-display"></a>Ändern der Anzeige

Wiedergabelisten können die benutzeroberfläche Windows Media Player auf vier Arten ändern:

-   Texteigenschaften
-   Image-Eigenschaften
-   MOREINFO-Eigenschaften
-   ABSTRACT-Text

## <a name="text-properties"></a>Texteigenschaften

Windows Media Player ermöglicht die Anzeige von Metadatentext für Titel, Autor, Copyright und Beschreibung. Clipmetadaten können aus dem Stream oder der Mediendatei oder aus einer Wiedergabeliste stammen. Metadaten anzeigen stammt aus der Wiedergabeliste. Im Allgemeinen sind Wiedergabelisten eine bessere Methode zum Übergeben von Texteigenschaften Windows Media Player, insbesondere dann, wenn sich Textelemente wahrscheinlich ändern. Es ist einfacher, Text in einer Wiedergabeliste zu bearbeiten, als eine Mediendatei neu zu erstellen. Und da Eigenschaften, die aus einer Wiedergabeliste gelesen werden, die in der Mediendatei enthaltenen Eigenschaften überschreiben, können Sie den Anzeigetext problemlos aktualisieren, indem Sie den neuen Text der entsprechenden Eigenschaft in einer Wiedergabeliste hinzufügen. Im folgenden Beispiel überschreibt der Text der Titel- und Autorenmetadaten in der Wiedergabeliste den In der Mediendatei sample.wma enthaltenen Titel- und Autorentext.

**DESCRIPTION-Text** wird aus einer Windows Mediendatei abgerufen, auf die in einem **ENTRY-Element** verwiesen wird, es sei denn, eine Metadateiwiedergabeliste enthält ein **ABSTRACT-Element.** Wenn **ABSTRACT-Text** vor angezeigt wird, wird er angezeigt, und der **DESCRIPTION-Text wird** überschrieben.


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

Bannerbilder können der Benutzeroberfläche von Windows Media Player. Die Grafik kann für Werbung, Die Bereitstellung von Informationen und den Zugriff auf Websites verwendet werden, um einige Möglichkeiten zu nennen.

Verwenden Sie **das BANNER-Element,** um ein Grafikbild (32 Pixel hoch bis 194 Pixel breit) für die Anzeige durch Windows Media Player. Die Grafik wird unter allen Videoinhalten angezeigt. Mithilfe des untergeordneten **MOREINFO-Elements** kann dem Banner ein Link hinzugefügt werden.

Eine QuickInfo kann durch ein **ABSTRACT-Element** innerhalb des Bereichs des **BANNER-Elements definiert** werden. Jeder definierte QuickInfo-Text kann angezeigt werden, indem der Mauszeiger über der Bannergrafik angezeigt wird. Wenn Sie die Bannergrafik mit dem Mauszeiger auswählen, wird jeder Link aktiviert, der mit dem **MOREINFO-Element definiert** ist.

Das  bevorzugte BANNER-Grafikformat ist das GIF-Format. Das JPG-Format kann verwendet werden, wenn die Grafik richtig dimensioniert ist.

Im vorherigen Beispiel wird die Verwendung des **BANNER-Elements** veranschaulicht.

> [!Note]  
> **BANNER-Images** werden nicht mit DRM-Dateien oder unterstützt, wenn Windows Media Player in eine Webseite eingebettet ist.

 

Weitere Informationen zu Bannern finden Sie unter [Benutzerdefinierte Grafiken in Windows Media Player](custom-graphics-in-windows-media-player.md).

## <a name="moreinfo-properties"></a>MOREINFO-Eigenschaften

Text- und Bildbereiche der Benutzeroberfläche können URLs zugeordnet werden. Während der Wiedergabe können Benutzer einen dieser Abschnitte auswählen, um eine Verbindung mit der url herzustellen, die ihr in ihrem Webbrowser zugeordnet ist. Sie können z. B. die Website eines Geschäftspartners einem Werbebannerbild zuordnen, wie im folgenden Codeausschnitt gezeigt.


```XML
<BANNER HREF="YourPath\2.gif">
    <ABSTRACT>More Information.</ABSTRACT>
    <MOREINFO HREF="https://www.proseware.com" />
</BANNER>

```



## <a name="abstract-text"></a>ABSTRACT-Text

**ABSTRACT-Text** wird verwendet, um eine kurze Popupbeschreibung der Text- oder Bildbereiche der Benutzeroberfläche anzuzeigen, der er zugeordnet ist. Wenn der Mauszeiger während der Wiedergabe auf einen dieser Bereiche zeigt, wird neben dem Mauszeiger eine QuickInfo angezeigt, die den dem Bereich zugeordneten **ABSTRACT-Text** zeigt. **ABSTRACT-Text** wird aus einer Metadatei abgerufen und mit dem **ABSTRACT-Element** definiert. Das **ABSTRACT-Element** kann ein untergeordnetes Element eines **ENTRY-** oder **BANNER-Elements** sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Metafile-Wiedergabelisten**](metafile-playlists.md)
</dt> <dt>

[**Verwenden von Metafile-Wiedergabelisten**](using-metafile-playlists.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Leitfaden zur Medienmetadatei**](windows-media-metafile-guide.md)
</dt> </dl>

 

 




