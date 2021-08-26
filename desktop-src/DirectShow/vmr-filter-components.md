---
description: VMR-Filterkomponenten
ms.assetid: 86fd8d6f-a742-457d-bb30-d04542431a0a
title: VMR-Filterkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dda6e8d37e1b5ac8c00da024fe78d4e18e38eed1e1735e787284d389769cff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903335"
---
# <a name="vmr-filter-components"></a>VMR-Filterkomponenten

Die VMR verwendet einen modularen Entwurf, mit dem Anwendungen sie für viele verschiedene Renderingszenarien konfigurieren können. Je nach Konfiguration enthält die VMR zwei bis fünf Unterkomponenten (zusätzlich zu den Eingabepins).

![vmr im Fenstermodus mit mehreren Streams](images/vmr-multiple-streams.png)

**Mixer:** Der Mixer ist ein COM-Objekt, das für das Mischen mehrerer Streams zuständig ist. Das Deinterlacing erfolgt auch innerhalb des Mixers. Der Mixer wird von der VMR geladen, wenn mehrere Eingabestreams erkannt werden oder wenn das Eingabevideo übersprungen wird. Der Mixer sammelt Informationen zu jedem Eingabestream und sortiert die Datenströme in der richtigen Z-Reihenfolge. Es ist dafür verantwortlich, zu bestimmen, wann jeder Eingabepin ein Beispiel empfängt, und den Bildkompositor zum richtigen Zeitpunkt anzuweisen, die tatsächliche Mischung durchzuführen. Der Mixer berechnet auch den Zeitstempel, der auf jedes Ausgabebild angewendet werden soll. Wenn die Anwendung eine Bitmap an die Hand gibt, die über dem zusammengesetzten Bild angezeigt werden soll, ist der Mixer dafür verantwortlich, sicherzustellen, dass die Bitmap auch dann oben angezeigt wird, wenn die Z-Reihenfolge der Eingabestreams geändert wird.

**Bild-Compositor:** Der Bild-Compositor ist ein COM-Objekt, das die tatsächliche Mischung der Eingabestreams auf einer einzelnen DirectDraw- oder Direct3D-Oberfläche ausführt, die vom Allocator-Presenter bereitgestellt wird. Die VMR stellt einen Standardimage-Compositor bereit, mit dem Anwendungen 2D-Alphablendingeffekte ausführen können. Anwendungen können einen benutzerdefinierten Bildkompositor bereitstellen, um andere 2D- und 3D-Effekte zu ermöglichen, z. B. das Anwenden von Texturen auf Teile des Bilds, das Pro-Pixel-Alphablending, das Zuordnen des Bilds zu feststehenden oder sich bewegenden 3D-Objekten usw.

**Allocator-Presenter:** Allocator-Presenter ist ein COM-Objekt, das das DirectDraw- oder Direct3D-Objekt zuordnet und die Kommunikation mit der Grafikkarte verarbeitet. Die Zeichnung kann entweder als Flip oder als Blit ausgeführt werden. Sie können Einen eigenen Allocator-Presenter anschließen, um das DirectDraw- oder Direct3D-Objekt zu erstellen und zu steuern und/oder um zur Präsentationszeit Zugriff auf die Videobits zu erhalten.

**Fenster-Manager:** Der Fenster-Manager wird nur im Fenstermodus verwendet. Der Fenster-Manager unterstützt aus Gründen der Abwärtskompatibilität die älteren [**IVideoWindow-**](/windows/desktop/api/Control/nn-control-ivideowindow) und [**IBasicVideo-Schnittstellen.**](/windows/desktop/api/Control/nn-control-ibasicvideo)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zum Rendern von Videomischungen](about-the-video-mixing-render.md)
</dt> </dl>

 

 



