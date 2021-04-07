---
description: Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine API für die hardwarebeschleunigte Video Verarbeitung.
ms.assetid: 38ebec28-c4fc-4e72-ac87-1e41707d1908
title: DXVA-HD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f8694a28d8d5871112590c90bf166d1aa9246e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749256"
---
# <a name="dxva-hd"></a>DXVA-HD

Microsoft DirectX Video Acceleration High Definition (DXVA-HD) ist eine API für die hardwarebeschleunigte Video Verarbeitung. DXVA-HD verwendet die GPU zum Ausführen von Funktionen wie Deinterlacing, Compositing und Farb Raum Konvertierung.

DXVA-HD ähnelt der [DXVA-Video Verarbeitung](dxva-video-processing.md) (DXVA-VP), bietet jedoch erweiterte Features und ein einfacheres Verarbeitungsmodell. DXVA-HD bietet ein flexibleres Kompositions Modell und unterstützt die nächste Generation von HD-optischen Formaten und Broadcast Standards.

Die DXVA-HD-API erfordert entweder einen WDDM-Anzeigetreiber, der die DXVA-HD-Gerätetreiber Schnittstelle (DDI) unterstützt, oder einen Plug-in-Software Prozessor.

-   [Verbesserungen bei DXVA-VP](#improvements-over-dxva-vp)
-   [Zugehörige Themen](#related-topics)

## <a name="improvements-over-dxva-vp"></a>Verbesserungen bei DXVA-VP

DXVA-HD erweitert den Satz von Features, die von DXVA-VP bereitgestellt werden. Zu den Erweiterungen gehören:

-   RGB-und YUV-Mischung. Jeder Stream kann entweder RGB oder YUV sein. Der primäre Stream und die untergeordneten Datenströme unterscheiden sich nicht länger.
-   Deinterlacing mehrerer Datenströme. Jeder Datenstrom kann entweder progressiv oder Zeilen Sprung sein. Darüber hinaus können der Rhythmus und die Framerate von einem Eingabestream zum nächsten abweichen.
-   RGB-Hintergrundfarben. Bisher wurden nur YUV-Hintergrundfarben unterstützt.
-   Luma-Schlüssel Erstellung. Wenn die Option zum Festlegen von Luma aktiviert ist, werden Luma-Werte, die innerhalb eines bestimmten Bereichs liegen, transparent.
-   Dynamischer Wechsel zwischen Deinterlacing-Modi.

DXVA-HD definiert außerdem einige erweiterte Funktionen, die von Treibern unterstützt werden können. Anwendungen sollten jedoch nicht davon ausgehen, dass diese Features von allen Treibern unterstützt werden. Zu den erweiterten Features gehören:

-   Inverse Telecine (z. b. 60i bis 24p).
-   Umwandlung von Frame Raten (z. b. 24 bis 120P).
-   Alpha Füll Modi.
-   Filter für Rauschunterdrückung und Kanten Erweiterung.
-   Anamorphe nichtlineare Skalierung.
-   Extended YCbCr (xwycc).

In diesem Abschnitt werden die folgenden Themen behandelt:

-   [Erstellen eines DXVA-HD-Video Prozessors](creating-a-dxva-hd-video-processor.md)
-   [Überprüfen unterstützter DXVA-HD-Formate](checking-supported-dxva-hd-formats.md)
-   [Erstellen von DXVA-HD-Video Oberflächen](creating-dxva-hd-video-surfaces.md)
-   [Festlegen von DXVA-HD-Zuständen](setting-dxva-hd-states.md)
-   [Ausführen von DXVA-HD-Blit](performing-the-dxva-hd-blit.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DirectX-Video Beschleunigung 2,0](directx-video-acceleration-2-0.md)
</dt> <dt>

[DXVA-HD-Beispiel](dxva-hd-sample.md)
</dt> </dl>

 

 



