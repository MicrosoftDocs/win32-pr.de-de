---
description: In Windows GDI+ ist eine Farbe ein 32-Bit-Wert mit 8 Bits für Alpha, rot, grün und blau.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Alphablending von Linien und Füllungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd13fe306dbf31c2a60a0bd38bf71b9e96edb201
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864284"
---
# <a name="alpha-blending-lines-and-fills"></a>Alphablending von Linien und Füllungen

In Windows GDI+ ist eine Farbe ein 32-Bit-Wert mit 8 Bits für Alpha, rot, grün und blau. Der Alpha-Wert gibt die Transparenz der Farbe an – das Ausmaß, in dem die Farbe mit der Hintergrundfarbe gemischt wird. Alpha Werte reichen von 0 bis 255, wobei 0 eine vollständig transparente Farbe darstellt und 255 eine vollständig nicht transparente Farbe darstellt.

Alpha Blending ist eine pixelweise Mischung aus Quell-und Hintergrund Farbdaten. Jede der drei Komponenten (rot, grün, blau) einer angegebenen Quellfarbe wird mit der entsprechenden Komponente der Hintergrundfarbe entsprechend der folgenden Formel gemischt:

Display Color = sourcecolor × Alpha/255 + BackgroundColor × (255 – Alpha)/255

Nehmen wir beispielsweise an, die rote Komponente der Quellfarbe ist 150, und die rote Komponente der Hintergrundfarbe ist 100. Wenn der Alpha-Wert 200 ist, wird die rote Komponente der resultierenden Farbe wie folgt berechnet:

150 × 200 / 255 + 100 × (255 – 200) / 255 = 139

In den folgenden Themen wird die Alpha Mischung ausführlicher behandelt:

-   [Zeichnen deckender und halb transparenter Linien](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [Zeichnen mit nicht transparenten und halbtransparenten Pinseln](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [Verwenden des Compositing-Modus zum Steuern der Alpha Mischung](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [Verwenden einer Farbmatrix zum Festlegen von Alphawerten in Bildern](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [Festlegen der Alpha Werte einzelner Pixel](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



