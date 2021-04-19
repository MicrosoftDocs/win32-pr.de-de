---
description: Top-Down im Vergleich zu
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down im Vergleich zu Bottom-Up Disb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e719bea5923aeccc4a0a92b5f73a253e13d2e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373093"
---
# <a name="top-down-vs-bottom-up-dibs"></a>Top-Down im Vergleich zu Bottom-Up Disb

Wenn Sie mit der Grafik Programmierung noch nicht vertraut sind, können Sie davon ausgehen, dass eine Bitmap im Arbeitsspeicher angeordnet wäre, sodass die obere Zeile des Bilds am Anfang des Puffers, gefolgt von der nächsten Zeile usw. angezeigt wird. Dies ist jedoch nicht unbedingt der Fall. In Windows können geräteunabhängige Bitmaps (Disb) in zwei verschiedenen Ausrichtungen, von unten nach oben und von oben nach unten, in den Arbeitsspeicher eingefügt werden.

In einem Bottom-up-DIB beginnt der Bild Puffer mit der untersten Zeile der Pixel, gefolgt von der nächsten Zeile nach oben usw. Die oberste Zeile des Bilds ist die letzte Zeile im Puffer. Daher ist das erste Byte im Speicher das untere linke Pixel des Bilds. In GDI sind alle Disb im unteren Bereich. Das folgende Diagramm zeigt das physische Layout eines Bottom-up-DIB.

![Unterer DIB](images/pixel-layout-bottomup.png)

In einem DIB von oben nach unten wird die Reihenfolge der Zeilen umgekehrt. Die oberste Zeile des Bilds ist die erste Zeile im Arbeitsspeicher, gefolgt von der nächsten Zeile nach unten. Die untere Zeile des Bilds ist die letzte Zeile im Puffer. Bei einem Top-Down-DIB ist das erste Byte im Speicher das linke obere Pixel des Bilds. DirectDraw verwendet Top-Down-Disb. Das folgende Diagramm zeigt das physische Layout eines Top-Down-DIB:

![DIB von oben nach unten](images/pixel-layout-topdown.png)

Bei RGB-Distributionen wird die Bild Ausrichtung durch den **biheight** -Member der [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur angegeben. Wenn **biheight** positiv ist, wird das Bild von unten nach oben angezeigt. Wenn **biheight** negativ ist, wird das Bild von oben nach unten angezeigt.

Disb in YUV-Formaten sind immer von oben nach unten, und das Vorzeichen des Elements **biheight** wird ignoriert. Decoders sollten YUV-Formaten mit positiver **biheight** anbieten, Sie sollten jedoch auch YUV-Formate mit negativer **biheight** akzeptieren und das Vorzeichen ignorieren.

Außerdem sollte jeder DIB-Typ, der ein **FourCC** im **bicompression** -Member verwendet, seine **biheight** als positive Zahl ausdrücken, unabhängig davon, was seine Ausrichtung ist, da der **FourCC** selbst ein Komprimierungs Schema identifiziert, dessen Bild Ausrichtung von einem beliebigen kompatiblen Filter verstanden werden sollte.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Video Frames](working-with-video-frames.md)
</dt> </dl>

 

 



