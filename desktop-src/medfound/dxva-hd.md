---
description: Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine API für die hardwarebeschleunigte Videoverarbeitung.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a40e23d6e91f576f062c52a0f58d0bfe1f769ad3879581b01386333266cb0553
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119958650"
---
# <a name="dxva-hd"></a>DXVA-HD

Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine API für die hardwarebeschleunigte Videoverarbeitung. DXVA-HD verwendet die GPU zum Ausführen von Funktionen wie Deinterlacing, Compositing und Farbraumkonvertierung.

DXVA-HD ähnelt [DXVA Video Processing](dxva-video-processing.md) (DXVA-VP), bietet aber erweiterte Features und ein einfacheres Verarbeitungsmodell. Durch die Bereitstellung eines flexibleren Kompositionsmodells wurde DXVA-HD entwickelt, um die nächste Generation von optischen HD-Formaten und Broadcaststandards zu unterstützen.

Die DXVA-HD-API erfordert entweder einen WDDM-Anzeigetreiber, der die DXVA-HD-Gerätetreiberschnittstelle (DDI) unterstützt, oder einen Plug-In-Softwareprozessor.

-   [Verbesserungen gegenüber DXVA-VP](#improvements-over-dxva-vp)
-   [Zugehörige Themen](#related-topics)

## <a name="improvements-over-dxva-vp"></a>Verbesserungen gegenüber DXVA-VP

DXVA-HD erweitert die von DXVA-VP bereitgestellten Features. Zu den Verbesserungen gehören:

-   RGB- und YUV-Mischung. Jeder Stream kann RGB oder YUV sein. Es gibt keinen Unterschied mehr zwischen dem primären Stream und den Unterstreams.
-   Deinterlacing mehrerer Streams. Jeder Stream kann entweder progressiv oder übersprungen sein. Darüber hinaus kann der Rhythmus und die Bildfrequenz von einem Eingabestream zum nächsten variieren.
-   RGB-Hintergrundfarben. Bisher wurden nur YUV-Hintergrundfarben unterstützt.
-   Luma-Schlüssel. Wenn luma keying aktiviert ist, werden luma-Werte, die innerhalb eines bestimmten Bereichs liegen, transparent.
-   Dynamischer Wechsel zwischen deinterlace-Modi.

DXVA-HD definiert auch einige erweiterte Features, die Treiber unterstützen können. Anwendungen sollten jedoch nicht davon ausgehen, dass alle Treiber diese Features unterstützen. Zu den erweiterten Features gehören:

-   Umgekehrte Telekope (z.B. 60i bis 24p).
-   Bildfrequenzkonvertierung (z.B. 24p in 120p).
-   Alphafüllmodi.
-   Filterung von Rauschunterdrückung und Edgeerweiterung.
-   Anamorphe nicht lineare Skalierung.
-   Extended YCbCr (xvYCC).

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Erstellen eines DXVA-HD-Videoprozessors](creating-a-dxva-hd-video-processor.md)
-   [Überprüfen der unterstützten DXVA-HD-Formate](checking-supported-dxva-hd-formats.md)
-   [Erstellen von DXVA-HD-Videooberflächen](creating-dxva-hd-video-surfaces.md)
-   [Festlegen von DXVA-HD-Zuständen](setting-dxva-hd-states.md)
-   [Ausführen von DXVA-HD Blit](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX Video Acceleration 2.0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA-HD-Beispiel](dxva-hd-sample.md)
</dt> </dl>

 

 



