---
description: In Windows GDI+ ist eine Farbe ein 32-Bit-Wert mit jeweils 8 Bits für Alpha, Rot, Grün und Blau.
ms.assetid: f8c22d1a-b96b-4d16-928e-20adbae4c4a7
title: Alphablending von Linien und Füllungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64096bbabc632ad7c2b159191ad21b3b09f3801a486f27679118008e4927e88f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977800"
---
# <a name="alpha-blending-lines-and-fills"></a>Alphablending von Linien und Füllungen

In Windows GDI+ ist eine Farbe ein 32-Bit-Wert mit jeweils 8 Bits für Alpha, Rot, Grün und Blau. Der Alphawert gibt die Transparenz der Farbe an– das Ausmaß, in dem die Farbe mit der Hintergrundfarbe gemischt wird. Alphawerte reichen von 0 bis 255, wobei 0 eine vollständig transparente Farbe und 255 eine vollständig deckende Farbe darstellt.

Alphablending ist eine Pixel-für-Pixel-Mischung aus Quell- und Hintergrundfarbdaten. Jede der drei Komponenten (Rot, Grün, Blau) einer bestimmten Quellfarbe wird gemäß der folgenden Formel mit der entsprechenden Komponente der Hintergrundfarbe kombiniert:

displayColor = sourceColor × alpha / 255 + backgroundColor × (255 – alpha) / 255

Angenommen, die rote Komponente der Quellfarbe ist 150 und die rote Komponente der Hintergrundfarbe ist 100. Wenn der Alphawert 200 ist, wird die rote Komponente der resultierenden Farbe wie folgt berechnet:

150 × 200 / 255 + 100 × (255 – 200) / 255 = 139

In den folgenden Themen wird das Alphablending ausführlicher behandelt:

-   [Zeichnen deckender und halb transparenter Linien](-gdiplus-drawing-opaque-and-semitransparent-lines-use.md)
-   [Zeichnen mit nicht transparenten und halbtransparenten Pinseln](-gdiplus-drawing-with-opaque-and-semitransparent-brushes-use.md)
-   [Verwenden des Compositing-Modus zum Steuern des Alphablendings](-gdiplus-using-compositing-mode-to-control-alpha-blending-use.md)
-   [Verwenden einer Farbmatrix zum Festlegen von Alphawerten in Bildern](-gdiplus-using-a-color-matrix-to-set-alpha-values-in-images-use.md)
-   [Festlegen der Alphawerte einzelner Pixel](-gdiplus-setting-the-alpha-values-of-individual-pixels-use.md)

 

 



