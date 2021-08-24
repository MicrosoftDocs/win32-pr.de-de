---
title: Videobildübergänge
description: Videobildübergänge
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Medienformat-SDK, Videobildübergänge
- Advanced Systems Format (ASF), Videobildübergänge
- ASF (Advanced Systems Format), Videobildübergänge
- Videobildübergänge
- Windows Media Video 9– Image v2-Codec
- Codecs,Windows Media Video 9 Image v2-Codec
- Videostreams,Windows Media Video 9 Image v2-Codec
- Videostreams, Bildübergänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b0a915f34ac9a2dcc00f8bcec739d48051361c1744e8e455166d56238529d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771240"
---
# <a name="video-image-transitions"></a>Videobildübergänge

Der Windows Media Video 9 Image v2-Codec animiert eine Reihe von Bildern, was zu einem Videostream führt. Der Codec kann zwei Bilder gleichzeitig bearbeiten, sie miteinander mischen und einen Übergang von einem zum anderen gemäß der von Ihnen verwendeten Konfiguration erstellen. In diesem Abschnitt werden die unterstützten Übergänge und die benötigten Parameter beschrieben.

Die Übergänge sind in der folgenden Tabelle nach ihren globalen Bezeichnern aufgeführt.



| Übergangsbezeichner                                                                           | Beschreibung                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ BOW \_ TIE**](wmt-videoimage-transition-bow-tie.md)              | Ein neues Bild wird in einer Reihe von Dreiecken auf gegenüberliegenden Seiten des Rahmens angezeigt.                                                                  |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ CIRCLE**](wmt-videoimage-transition-circle.md)                 | Ein neues Bild wird in einem Kreis angezeigt.                                                                                                           |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ CROSS \_ FADE**](wmt-videoimage-transition-cross-fade.md)        | Kein spezieller Übergang, die Überblendungskoeffizienten der beiden Bilder bestimmen die Kreuzblendung (Übergänge).                                         |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAGONAL**](wmt-videoimage-transition-diagonal.md)             | Ein neues Bild wird entlang einer diagonalen Linie aus einer Ecke des Rahmens angezeigt.                                                          |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAMOND**](wmt-videoimage-transition-diamond.md)               | Ein neues Bild wird in einer Raute angezeigt.                                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ ÜBERGANG IN \_ FARBE \_ \_ AUSBLENDEN**](wmt-videoimage-transition-fade-to-color.md) | Überrennt das Bild in einen Rahmen mit Volltonfarbe.                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ FILLED \_ V**](wmt-videoimage-transition-filled-v.md)            | Ein neues Bild wird in einem Dreieck angezeigt, das von einer Seite des Rahmens stammt.                                                                  |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ FLIP**](wmt-videoimage-transition-flip.md)                     | Das alte Bild wird auf einer y-Achse durch die Mitte des Rahmens gedreht. Das neue Bild wird als Rückseite des alten Bilds angezeigt.                    |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ INSET**](wmt-videoimage-transition-inset.md)                   | Ein neues Bild wird durch ein Rechteck aus einer Ecke des Rahmens angezeigt.                                                               |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ IRIS**](wmt-videoimage-transition-iris.md)                     | Entlang einer X-Achse und einer y-Achse wird ein neues Bild angezeigt.                                                                                          |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ PAGE \_ ROLL**](wmt-videoimage-transition-page-roll.md)          | Das alte Bild wird in einen Seitenumkehreffekt transformiert, der das neue Bild darunter zeigt.                                                      |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ RECTANGLE**](wmt-videoimage-transition-rectangle.md)           | Ein neues Bild wird durch ein Rechteck innerhalb des Frames angezeigt.                                                                                       |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ REVEAL**](wmt-videoimage-transition-reveal.md)                 | Ein neues Bild wird entlang einer geraden Linie angezeigt, die von einer Seite des Rahmens stammt.                                                          |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ SLIDE**](wmt-videoimage-transition-slide.md)                   | Altes Bild wird aus dem Rahmen geschiebet und zeigt das neue Bild darunter an.                                                                       |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ SPLIT**](wmt-videoimage-transition-split.md)                   | Ein neues Bild wird durch eine horizontale oder vertikale Aufteilung im alten Bild angezeigt. Die Aufteilung wird entlang einer geraden Linie angezeigt, die innerhalb des Rahmens beginnt. |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ STAR**](wmt-videoimage-transition-star.md)                     | Ein neues Bild wird durch einen Fünf-Punkte-Stern innerhalb des Frames angezeigt.                                                                               |
| [**WMT \_ VIDEOIMAGE \_ TRANSITION \_ WHEEL**](wmt-videoimage-transition-wheel.md)                   | Ein neues Bild wird durch vier rotierende Spokes mit einem gemeinsamen Pivotpunkt angezeigt.                                                                     |



 

Jeder Übergang wird vollständig in einem eigenen Thema beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> <dt>

[**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




