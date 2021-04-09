---
title: Video Bild Übergänge
description: Video Bild Übergänge
ms.assetid: 201ddbfb-567b-4893-b754-569f1e7d8466
keywords:
- Windows Media-Format-SDK, Video Bild Übergänge
- Advanced Systems Format (ASF), Video Bild Übergänge
- ASF (Advanced Systems Format), Video Bild Übergänge
- Video Bild Übergänge
- Windows Media Video 9 Abbild v2-Codec
- Codecs, Windows Media Video 9 Abbild v2-Codec
- Videostreams, Windows Media Video 9-Abbild v2-Codec
- Videostreams, Bild Übergänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbfd02628a78196a73750c2c0ff6b9e9c3d6729c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036770"
---
# <a name="video-image-transitions"></a>Video Bild Übergänge

Der Windows Media Video 9-Abbild v2-Codec animiert eine Reihe von Bildern, was zu einem Videostream führt. Der Codec kann zwei Abbilder gleichzeitig bearbeiten, diese miteinander kombinieren und einen Übergang von einem zum anderen entsprechend der von Ihnen bereitgestellten Konfiguration erstellen. In diesem Abschnitt werden die unterstützten Übergänge und die erforderlichen Parameter beschrieben.

Die Übergänge sind in der folgenden Tabelle nach ihren globalen bezeichlern aufgeführt.



| Übergangs Bezeichner                                                                           | BESCHREIBUNG                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**WMT \_ Videoimage- \_ Übergangs \_ Bogen \_ Tie**](wmt-videoimage-transition-bow-tie.md)              | Ein neues Bild wird in einer Reihe von Dreiecken auf gegenüberliegenden Seiten des Frames angezeigt.                                                                  |
| [**WMT \_ Videoimage- \_ Übergangs \_ Kreis**](wmt-videoimage-transition-circle.md)                 | Ein neues Bild wird in einem Kreis angezeigt.                                                                                                           |
| [**Kreuz Ausblenden des WMT- \_ Videobilds \_ \_ \_**](wmt-videoimage-transition-cross-fade.md)        | Kein spezieller Übergang, die Blend-Koeffizienten der beiden Bilder bestimmen das Kreuz ausblenden (auflösen).                                         |
| [**Übergang von WMT \_ Videoimage \_ \_ Diagonal**](wmt-videoimage-transition-diagonal.md)             | Ein neues Bild wird entlang einer diagonalen Linie angezeigt, die in einer Ecke des Frames steht.                                                          |
| [**WMT \_ Videoimage- \_ Übergangs Raute \_**](wmt-videoimage-transition-diamond.md)               | Ein neues Bild wird in einem Rautensymbol angezeigt.                                                                                                          |
| [**WMT \_ Videoimage \_ - \_ Übergang \_ in \_ Farbe ausblenden**](wmt-videoimage-transition-fade-to-color.md) | Löst von dem Bild bis zu einem Frame mit voll Tonfarbe auf.                                                                                          |
| [**WMT \_ Videoimage- \_ Übergang mit \_ ausgefülltem \_ V**](wmt-videoimage-transition-filled-v.md)            | Ein neues Bild wird in einem Dreieck angezeigt, das von einer Seite des Frames stammt.                                                                  |
| [**WMT \_ Videoimage- \_ Übergang \_ kippen**](wmt-videoimage-transition-flip.md)                     | Das alte Bild wird auf einer y-Achse durch die Mitte des Frames gedreht. Das neue Bild wird als Rückseite des alten Bilds angezeigt.                    |
| [**WMT \_ Videoimage- \_ Übergangs \_ inmenge**](wmt-videoimage-transition-inset.md)                   | Ein neues Bild wird durch ein Rechteck angezeigt, das aus einer Ecke des Frames stammt.                                                               |
| [**WMT \_ Videoimage- \_ Übergangs \_ IRIS**](wmt-videoimage-transition-iris.md)                     | Ein neues Bild wird auf einer x-Achse und einer y-Achse angezeigt.                                                                                          |
| [**WMT \_ Videoimage- \_ Übergangs \_ Seite \_ (Rollup)**](wmt-videoimage-transition-page-roll.md)          | Das alte Bild wird in einem Seiten flippingeffekt transformiert und zeigt das neue Bild darunter.                                                      |
| [**WMT \_ Videoimage- \_ Übergangs \_ Rechteck**](wmt-videoimage-transition-rectangle.md)           | Ein neues Bild wird durch ein Rechteck innerhalb des Frames angezeigt.                                                                                       |
| [**WMT \_ Videoimage- \_ Übergang \_ offenlegen**](wmt-videoimage-transition-reveal.md)                 | Ein neues Bild wird an einer geraden Linie angezeigt, die von einer Seite des Frames stammt.                                                          |
| [**Folie für WMT \_ Videoimage- \_ Übergang \_**](wmt-videoimage-transition-slide.md)                   | Das alte Bild wird aus dem Frame heraus bewegt und zeigt das neue Bild unterhalb an.                                                                       |
| [**Teilung des WMT \_ Videoimage- \_ Übergangs \_**](wmt-videoimage-transition-split.md)                   | Ein neues Bild wird durch eine horizontale oder vertikale Aufteilung im alten Bild angezeigt. Die Teilung wird entlang einer geraden Linie angezeigt, beginnend innerhalb des Frames. |
| [**WMT \_ Videoimage \_ \_ -Übergangs Stern**](wmt-videoimage-transition-star.md)                     | Ein neues Bild wird von einem fünf-Spitze-Stern innerhalb des Frames angezeigt.                                                                               |
| [**WMT \_ Videoimage- \_ Übergangs \_ Rad**](wmt-videoimage-transition-wheel.md)                   | Ein neues Bild wird von vier rotierenden Spokes mit einem gemeinsamen Pivotpunkt offengelegt.                                                                     |



 

Jeder Übergang wird in einem eigenen Thema ausführlich beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> <dt>

[**WMT \_ Videoimage \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2)
</dt> </dl>

 

 




