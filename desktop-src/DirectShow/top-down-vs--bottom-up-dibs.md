---
description: Top-Down im Vergleich zu
ms.assetid: c292f145-f385-4f18-8f98-e414d86860e2
title: Top-Down im Vergleich zu Bottom-Up DIBs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adff1d525423ef8590a3656a5e63f7541be180e2dcc5c70307f93298eb9ce991
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951567"
---
# <a name="top-down-vs-bottom-up-dibs"></a>Top-Down im Vergleich zu Bottom-Up DIBs

Wenn Sie noch keine Grafikprogrammierung haben, erwarten Sie möglicherweise, dass eine Bitmap im Arbeitsspeicher angeordnet wird, sodass die oberste Zeile des Bilds am Anfang des Puffers, gefolgt von der nächsten Zeile usw. angezeigt wird. Dies ist jedoch nicht unbedingt der Fall. In Windows können geräteunabhängige Bitmaps (DIBs) in zwei verschiedenen Ausrichtungen im Arbeitsspeicher platziert werden: von unten nach oben und von oben nach unten.

In einem DIB von unten nach oben beginnt der Bildpuffer mit der unteren Zeile von Pixeln, gefolgt von der nächsten Zeile nach oben usw. Die oberste Zeile des Bilds ist die letzte Zeile im Puffer. Aus diesem Grund ist das erste Byte im Arbeitsspeicher das unten links angezeigte Pixel des Bilds. In GDI befinden sich alle DIBs von unten nach oben. Das folgende Diagramm zeigt das physische Layout eines DIB von unten nach oben.

![bottom-up dib](images/pixel-layout-bottomup.png)

In einem DIB von oben nach unten wird die Reihenfolge der Zeilen umgekehrt. Die oberste Zeile des Bilds ist die erste Zeile im Arbeitsspeicher, gefolgt von der nächsten Zeile nach unten. Die untere Zeile des Bilds ist die letzte Zeile im Puffer. Bei einem DIB von oben nach unten ist das erste Byte im Arbeitsspeicher das obere linke Pixel des Bilds. DirectDraw verwendet DIBs von oben nach unten. Das folgende Diagramm zeigt das physische Layout eines diB von oben nach unten:

![top-down dib](images/pixel-layout-topdown.png)

Für RGB-DIBs wird die Bildausrichtung durch den **biHeight-Member** der [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) angegeben. Wenn **biHeight** positiv ist, befindet sich das Bild von unten nach oben. Wenn **biHeight** negativ ist, befindet sich das Bild von oben nach unten.

DIBs in YUV-Formaten befinden sich immer von oben nach unten, und das Vorzeichen des **biHeight-Members** wird ignoriert. Decoder sollten YUV-Formate mit positivem **biHeight** anbieten, aber sie sollten auch YUV-Formate mit negativem **biHeight** akzeptieren und das Vorzeichen ignorieren.

Darüber hinaus sollte jeder DIB-Typ, der **eine FOURCC** im **biCompression-Member** verwendet, **biHeight** als positive Zahl ausdrücken, unabhängig von seiner Ausrichtung, da **FOURCC** selbst ein Komprimierungsschema identifiziert, dessen Bildausrichtung von jedem kompatiblen Filter verstanden werden soll.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Videoframes](working-with-video-frames.md)
</dt> </dl>

 

 



