---
title: Erstellen einer HtmlView-Präsentation
description: Erstellen einer HtmlView-Präsentation
ms.assetid: 70203160-2dd9-4096-be6a-c704db757f7f
keywords:
- Windows Media Metadatei-Wiedergabelisten, HtmlView-Präsentationen
- Wiedergabelisten, HtmlView-Präsentationen
- Metadatei-Wiedergabelisten, HtmlView-Präsentationen
- Windows Media Metadatei-Wiedergabelisten, Erstellen von HtmlView-Präsentationen
- Wiedergabelisten, Erstellen von HtmlView-Präsentationen
- Metadatei-Wiedergabelisten, Erstellen von HtmlView-Präsentationen
- Erstellen von HtmlView-Präsentationen
- Windows Media Player, Erstellen von HtmlView-Präsentationen
- Windows Media Player, HtmlView-Präsentationen
- HtmlView, Erstellen von Präsentationen
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1094ce787e55fbeb98e628389b5fd51ab94ab415
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388464"
---
# <a name="creating-an-htmlview-presentation"></a>Erstellen einer HtmlView-Präsentation

Zum Erstellen einer grundlegenden HtmlView-Präsentation benötigen Sie mindestens drei Elemente:

-   **Digitaler Medieninhalt.** Dies ist eine oder mehrere Audiodateien oder Videodateien, die von Windows Media Player abgespielt werden.
-   **Eine Webseite.** Dies ist der webbasierte Inhalt, der im Feature " **jetzt** wiedergeben" der Player-Benutzeroberfläche angezeigt wird.
-   **Eine Windows Media-Metadatendatei.** Dies ist die Metadatei-Wiedergabeliste, die Windows Media Player anweist, den Inhalt digitaler Medien mit der Webseite zu kombinieren.

Eine. ASX-Datei ist eine Textdatei, die Informationen über einen Dateistream und seine Präsentation bereitstellt. Basierend auf der Syntax von Extensible Markup Language (XML) können. ASX-Dateien eine Vielzahl von Elementen enthalten, die jeweils durch ein Tag mit zugeordneten Attributen identifiziert werden. Das **param** -Element bietet eine Möglichkeit, einen benutzerdefinierten Parameter entweder einem bestimmten Eintrag in einer metadateiwiedergabe Liste oder der gesamten Metadatendatei zuzuordnen. Einer der für ihre Verwendung verfügbaren vordefinierten Parameternamen ist "HtmlView". Dies ist der Parameter, der bewirkt, dass die durch den URL-Wert angegebene Webseite in Windows Media Player angezeigt wird.

Der folgende Beispielcode zeigt eine. ASX-Datei, die eine einzelne digitale Mediendatei mit einer einzelnen Webseite kombiniert:


```XML
<ASX version="3.0">
<PARAM name="HTMLView" value="https://www.proseware.com/htmlview.htm"/>

<ENTRY>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

</ASX>

```



Wenn Windows Media Player die. ASX-Datei im vorangehenden Beispiel öffnet, wird die Audiodatei aus der Datei mit dem Namen Content1. WMA abgespielt und die Webseite mit **dem Namen** htmlview.htm in der Funktion zum Wiedergeben des vollmodusplayers geöffnet. Der Benutzer kann den Audioinhalt mithilfe der Windows Media Player-Steuerelemente anhalten, suchen und anhalten.

Sie können die Webseite, die für jeden Inhalt angezeigt wird, ganz einfach ändern, indem Sie jedem Eintrag ein **param** -Element zuordnen, wie im folgenden Codebeispiel gezeigt:


```XML
<ASX version="3.0">

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview1.htm"/>
   <REF href="rtsp://www.proseware.com/content1.wma"/>
</ENTRY>

<ENTRY>
   <PARAM name="HTMLView" value="https://www.proseware.com/htmlview2.htm"/>
   <REF href="rtsp://www.proseware.com/content2.wma"/>
</ENTRY>

</ASX>

```



Im vorherigen Beispiel zeigt Windows Media Player zuerst die Webseite htmlview1.htm bei der Wiedergabe der digitalen Audiodatei Content1. WMA an. Wenn der Spieler den nächsten Eintrag in der Wiedergabeliste, Content2. WMA, öffnet, gibt die in angezeigte Webseite **nun** Änderungen an htmlview2.htm. Auf diese Weise können Sie angeben, welche Webseite der Benutzer für die einzelnen Digital Media-Inhalte sehen soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Anzeigen von Webseiten in Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Param-Element**](param-element.md)
</dt> </dl>

 

 




