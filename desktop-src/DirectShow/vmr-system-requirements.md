---
description: VMR-System Anforderungen
ms.assetid: fd50b312-73f0-4c68-a8b1-3497d958bc8f
title: VMR-System Anforderungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99d54d6d1604c3e514f3ceef379eaba4a8fa1ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216775"
---
# <a name="vmr-system-requirements"></a>VMR-System Anforderungen

VMR verwendet die Grafik Verarbeitungsfunktionen der Anzeigekarte des Computers exklusiv. VMR führt keine Vermischung oder das Rendering von Videos mithilfe des Host Prozessors durch, da dies die Frame Rate und die Qualität des angezeigten Videos erheblich beeinträchtigen würde. Wenn Sie die neuen Features von VMR nutzen, insbesondere die Mischung mehrerer Videostreams und/oder Anwendungs Images, ist die Gesamtleistung stark von den Funktionen der Grafikkarte abhängig, die auf dem Computer verwendet wird. Grafikkarten, die sich gut mit VMR ausführen lassen, haben folgende Hardwareunterstützung:

-   Unterstützung für YUV und "Non-Power von 2" Direct3D Textur Oberflächen.
-   Die Möglichkeit der Stretchblt von YUV zu RGB DirectDraw-Oberflächen.
-   Mindestens 16MB Videospeicher, wenn mehrere Videostreams kombiniert werden sollen. Die tatsächliche erforderliche Arbeitsspeicher Menge hängt von der Bildgröße der Videostreams und der Auflösung des verwendeten Anzeigemodus ab.
-   Unterstützung für eine RGB-Überlagerung oder die Möglichkeit, mit einer YUV-über Lagerungs Oberfläche zu mischen.
-   Hardware beschleunigtes Video (Unterstützung für die DirectX-Videobeschleunigung) Decodierung.
-   Hohe Pixel Füll Raten.

> [!Note]  
> Der VMR erfordert, dass der System Monitor für eine Farbtiefe von mindestens 16 Bits festgelegt wird. Der VMR kann nicht in den Zustand "ausführen" versetzt werden, wenn der Monitor für 256 Farben festgelegt ist. Außerdem können von einigen Videokarten keine Direct3D-Vorgänge durchgeführt werden, wenn die Anzeige auf 24 Bits pro Pixel festgelegt ist.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Video Mischungs Rendering](about-the-video-mixing-render.md)
</dt> </dl>

 

 



