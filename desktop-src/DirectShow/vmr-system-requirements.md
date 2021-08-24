---
description: VMR-Systemanforderungen
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: VMR-Systemanforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d03d5a195f675b911dff85860592c3ec3b5a39ec4f65a51cdc594bc8744906
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633000"
---
# <a name="vmr-system-requirements"></a>VMR-Systemanforderungen

Die VMR verwendet ausschließlich die Grafikverarbeitungsfunktionen der Anzeigekarte des Computers. Der VMR führt keine Videomischung oder -rendering mithilfe des Hostprozessors durch, da dies die Bildfrequenz und Qualität des angezeigten Videos stark beeinflussen würde. Wenn Sie die neuen Features des virtuellen Computers nutzen, insbesondere das Mischen mehrerer Videostreams und/oder Anwendungsbilder, hängt die insgesamt erhaltene Leistung stark von den Funktionen der auf dem Computer verwendeten Grafikkarte ab. Für Grafikkarten, die eine gute Leistung mit vmR haben, ist die folgende Hardwareunterstützung integriert:

-   Unterstützung für YUV- und "Non-Power of 2"-Direct3D-Texturoberflächen.
-   Die Möglichkeit, StretchBlt von YUV zu RGB DirectDraw-Oberflächen zu verwenden.
-   Mindestens 16 MB Videospeicher, wenn mehrere Videostreams kombiniert werden sollen. Die tatsächlich erforderliche Arbeitsspeichermenge hängt von der Bildgröße der Videostreams und der Auflösung des verwendeten Anzeigemodus ab.
-   Unterstützung für eine RGB-Überlagerung oder die Möglichkeit, zu einer YUV-Überlagerungsoberfläche zu überblenden.
-   Hardwarebeschleunigte Videocodierung (Unterstützung für DirectX-Videobeschleunigung).
-   Hohe Pixelfüllraten.

> [!Note]  
> Der VMR erfordert, dass der Systemmonitor für eine Farbtiefe von mindestens 16 Bits festgelegt wird. Die VMR kann nicht in einen Ausführungszustand gesetzt werden, wenn der Monitor auf 256 Farben festgelegt ist. Außerdem können einige Grafikkarten keine Direct3D-Vorgänge ausführen, wenn die Anzeige auf 24 Bits pro Pixel festgelegt ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Rendern von Videos](about-the-video-mixing-render.md)
</dt> </dl>

 

 



