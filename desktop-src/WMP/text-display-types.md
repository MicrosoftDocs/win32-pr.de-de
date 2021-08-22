---
title: Textanzeigetypen
description: Textanzeigetypen
ms.assetid: 6aa3fc89-e5f5-420f-82e0-c605676078cb
keywords:
- Windows Media Player Mobile Skins, Text
- Text in Skins, Anzeigetypen
- Skins, Text
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01826f35db0d3877a3ecd34c351315872760b1b9b0713a36955bb3161ed6ba8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134603"
---
# <a name="text-display-types"></a>Textanzeigetypen

Sie müssen keine Textanzeigen in Ihre Skin einfügen, aber es gibt viele Instanzen, in denen Sie dies möglicherweise wünschen. Sie können z. B. eine Seek-Trackleiste einschließen, damit der Benutzer zu einer beliebigen Position im Medienelement wechseln kann. Sie können aber auch eine Textanzeige einschließen, die die Anzahl der Sekunden anzeigt, die seit der Wiedergabe des aktuellen Medienelements verstrichen sind.

**Anzeigefelder**

Es folgen mehrere Attribute, die ein Textelement anzeigen kann:

-   Time
-   Wiedergabeliste
-   Track\#
-   \#Spuren
-   Titel
-   Autor
-   Copyright
-   Dateiname
-   DateinameExt
-   Bitrate
-   Häufigkeit
-   Status
-   VolPercent

Weitere Informationen zu Textanzeigetypen finden Sie im Abschnitt [Text](text.md) der Skin Reference.

**Scrollen in Marquee**

Zusätzlich zur Verwendung der einzelnen Textelemente können Sie ein oder mehrere Attribute in einem scrollenden Textzelt kombinieren. Dies ist nützlich, wenn Sie eine Gruppierung verwandter Textinformationen in einem kleinen Bereich anzeigen möchten. Beispielsweise können Sie Titel-, Autor- und Copyrightinformationen in einer Marquee anzeigen.

Weitere Informationen zum Erstellen eines Textzeltes finden Sie im Abschnitt ["Marquee"](marquee.md) der Skin Reference.

**Statusanzeige**

Ein anderer Textanzeigetyp ist die Statusanzeige. Dadurch können Sie automatisch Informationen zum aktuellen Status von Windows Media Player Mobile anzeigen. Beispielsweise informiert die Statusanzeige den Benutzer, wenn ein Medienelement gepuffert wird, sodass offensichtlich ist, dass der Player funktioniert.

Die folgenden Meldungen werden in der Statusanzeige angezeigt:

-   Pufferung
-   Verbindung
-   Angehalten
-   Wiedergabe
-   Bereit
-   Beendet

> [!Note]  
> Wenn ein Medienelement wiedergegeben wird, wird die Statusanzeige durch Untertitel, Interpret, Album, Genre und aktuelle Bitrate gedreht.

 

Informationen zum Erstellen einer Statusanzeige über das Status-Element finden Sie im Abschnitt [Status](status.md) der Skin Reference. Es wird jedoch bevorzugt, das Statusattribut im Text-Element anstelle des Status-Elements zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Media Player Mobile Funktionalität**](windows-media-player-mobile-functionality.md)
</dt> </dl>

 

 




