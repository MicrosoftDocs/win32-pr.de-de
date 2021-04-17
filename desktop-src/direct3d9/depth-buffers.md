---
description: Ein tiefen Puffer, der häufig als z-Puffer oder w-Puffer bezeichnet wird, ist eine Eigenschaft des Geräts, das die von Direct3D zu verwendenden Tiefeninformationen speichert.
ms.assetid: vs|directx_sdk|~\depth_buffers.htm
title: Tiefen Puffer (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc1ab41ba98ca5e3b08980ac90a572a19fc8a72a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481550"
---
# <a name="depth-buffers-direct3d-9"></a>Tiefen Puffer (Direct3D 9)

Ein tiefen Puffer, der häufig als z-Puffer oder w-Puffer bezeichnet wird, ist eine Eigenschaft des Geräts, das die von Direct3D zu verwendenden Tiefeninformationen speichert. Wenn Direct3D eine Szene in eine Ziel Oberfläche rendert, kann der Arbeitsspeicher in einer zugeordneten Tiefe Puffer Oberfläche als Arbeitsbereich verwendet werden, um zu bestimmen, wie die Pixel der gerachtelten Polygone einander einlesen. Direct3D verwendet eine Off-Screen Direct3D-Oberfläche als Ziel, auf das endgültige Farbwerte geschrieben werden. Die Tiefe-Puffer-Oberfläche, die der Renderziel-Oberfläche zugeordnet ist, wird zum Speichern von Tiefeninformationen verwendet, die Aufschluss darüber gibt Direct3D wie tief jedes sichtbare Pixel in der Szene ist.

Wenn eine Szene mit aktivierter tiefen Pufferung gerendert wird, wird jeder Punkt auf der Rendering-Oberfläche getestet. Die Werte im tiefen Puffer können die z-Koordinate eines Punkts oder seine homogene w-Koordinate sein, von der Position (x, y, z, w) des Punkts im Projektions Bereich. Ein tiefen Puffer, der z-Werte verwendet, wird häufig als z-Puffer bezeichnet, und ein tiefen Puffer, der w-Werte verwendet, wird als w-Buffer bezeichnet. Jeder Typ von tiefen Puffern hat vor-und Nachteile, die später erläutert werden.

Zu Beginn des Tests wird der tiefen Wert im tiefen Puffer auf den größtmöglichen Wert für die Szene festgelegt. Der Farbwert auf der Rendering-Oberfläche wird entweder auf den Wert der Hintergrundfarbe oder auf den Farbwert der Hintergrundtextur an diesem Punkt festgelegt. Jedes Polygon in der Szene wird getestet, um zu sehen, ob es sich mit der aktuellen Koordinate (x, y) auf der Renderingoberfläche überschneidet. Wenn dies der Fall ist, wird der tiefen Wert, der die z-Koordinate in einem z-Puffer ist, und die w-Koordinate in einem w-buffer-an der aktuellen Stelle getestet, um festzustellen, ob er kleiner als der im tiefen Puffer gespeicherte tiefen Wert ist. Wenn die Tiefe des Polygon Werts kleiner ist, wird Sie im tiefen Puffer gespeichert, und der Farbwert des Polygons wird in den aktuellen Punkt auf der Renderingoberfläche geschrieben. Wenn der tiefen Wert des Polygons zu diesem Zeitpunkt größer ist, wird das nächste Polygon in der Liste getestet. Dieser Vorgang wird in der folgenden Abbildung dargestellt.

![Diagramm der Test tiefen Werte](images/zbuffer.png)

> [!Note]  
> Obwohl die meisten Anwendungen diese Funktion nicht verwenden, können Sie den Vergleich ändern, den Direct3D verwendet, um zu bestimmen, welche Werte im tiefen Puffer und anschließend auf der renderzieloberfläche abgelegt werden. Zu diesem Zweck ändern Sie den Wert für den D3DRS \_ zfunc-Rendering-Zustand. Bei bestimmter Hardware kann das Ändern der Vergleichsfunktion hierarchische z-Tests deaktivieren.

 

Fast alle Accelerators auf dem Markt unterstützen z-Pufferung, sodass z-Puffer heute die häufigste Art von tiefen Puffer ist. Allerdings haben z-Puffer ihre Nachteile. Aufgrund der beteiligten Mathematik werden die generierten z-Werte in einem z-Puffer tendenziell nicht gleichmäßig auf den z-Pufferbereich verteilt (in der Regel 0,0 bis 1,0, einschließlich). Insbesondere wirkt sich das Verhältnis zwischen der weit verbreiteten und der Near Clipping-Ebene stark aus, wie ungleich z-Werte verteilt werden. Durch die Verwendung einer Entfernung der Entfernung zu einem Abstand von 100 (in der Nähe der mittleren Ebene) werden 90 Prozent des tiefen Puffer Bereichs für die ersten 10 Prozent des Bereichs der Szenen Tiefe aufgewendet. Typische Anwendungen für Unterhaltung oder visuelle Simulationen mit äußeren Szenen erfordern häufig ein Verhältnis von einer beliebigen Ebene zwischen 1.000 und 10.000. Bei einem Verhältnis von 1.000 werden 98 Prozent des Bereichs für die ersten 2 Prozent des tiefen Bereichs aufgewendet, und die Verteilung wird mit höheren Verhältnissen schlechter. Dies kann zu verdeckten Oberflächen Artefakten in entfernten Objekten führen, insbesondere bei Verwendung von 16-Bit-Tiefen Puffern, der am häufigsten unterstützten Bittiefe.

Auf der anderen Seite ist ein w-basierter tiefen Puffer oft gleichmäßig gleichmäßig zwischen den Near-und Far-Clip-Flächen verteilt als ein z-Puffer. Der Hauptvorteil besteht darin, dass das Verhältnis der Entfernungen für die weit entfernten und die Near Clipping-Ebene kein Problem mehr ist. Dies ermöglicht es Anwendungen, große maximale Bereiche zu unterstützen, während Sie immer noch relativ präzise Tiefe Pufferung in der Nähe des Augen Punkts erhalten. Ein w-basierter tiefen Puffer ist nicht perfekt und kann manchmal verborgene Oberflächen Artefakte für Near-Objekte aufweisen. Ein weiterer Nachteil des w-gepufferten Ansatzes liegt im Zusammenhang mit der Hardwareunterstützung: w-buffereing wird in Hardware nicht so weit wie z-Pufferung unterstützt.

Die Verwendung eines z-Puffers erfordert mehr Aufwand beim Rendern. Bei der Verwendung von z-Puffern können verschiedene Techniken verwendet werden, um das Rendering zu optimieren. Weitere Informationen finden Sie unter [Z-Puffer Leistung](performance-optimizations.md).

> [!Note]  
> Die tatsächliche Interpretation eines tiefen Werts ist spezifisch für den Renderer.

 

Dieser Abschnitt enthält Informationen zur Verwendung von tiefen Puffern für ausgeblendete und ausgeblendete Oberflächen Entfernungs

-   [Abfragen der Tiefe Puffer Unterstützung (Direct3D 9)](querying-for-depth-buffer-support.md)
-   [Erstellen eines tiefen Puffers (Direct3D 9)](creating-a-depth-buffer.md)
-   [Aktivieren der tiefen Pufferung (Direct3D 9)](enabling-depth-buffering.md)
-   [Abrufen eines tiefen Puffers (Direct3D 9)](retrieving-a-depth-buffer.md)
-   [Löschen von tiefen Puffern (Direct3D 9)](clearing-depth-buffers.md)
-   [Ändern des Schreibzugriffs auf den Lesezugriff (Direct3D 9)](changing-depth-buffer-write-access.md)
-   [Ändern von tiefen Puffer Vergleichsfunktionen (Direct3D 9)](changing-depth-buffer-comparison-functions.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Rendering](direct3d-rendering.md)
</dt> </dl>

 

 



