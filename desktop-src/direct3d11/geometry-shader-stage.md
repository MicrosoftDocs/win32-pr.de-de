---
title: Geometry-Shader-Phase
description: Die Geometry-Shader-Phase (GS) führt den von der Anwendung angegebenen Shader-Code mit Vertices als Eingabe und die Möglichkeit zum Generieren von Scheitel Punkten bei der Ausgabe aus.
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da66b1e3f9abf4e7db8010887f3e78676d02a874
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728385"
---
# <a name="geometry-shader-stage"></a>Geometry-Shader-Phase

Die Geometry-Shader-Phase (GS) führt den von der Anwendung angegebenen Shader-Code mit Vertices als Eingabe und die Möglichkeit zum Generieren von Scheitel Punkten bei der Ausgabe aus.

## <a name="the-geometry-shader"></a>Der Geometry-Shader

Anders als bei Vertex-Shadern, die auf einem einzelnen Scheitelpunkt arbeiten, sind die Eingaben des Geometry-Shaders die Scheitel Punkte für einen vollständigen primitiven (zwei Scheitel Punkte für Linien, drei Scheitel Punkte für Dreiecke oder einzelner Scheitelpunkt für Punkt). Geometry-Shader können auch die Scheitelpunkt Daten für die Rand angrenzenden primitiven als Eingabe (weitere zwei Scheitel Punkte für eine Linie, zusätzliche drei für ein Dreieck). Die folgende Abbildung zeigt ein Dreieck und eine Linie mit angrenzenden Scheitel Punkten.

![Abbildung eines Dreiecks und einer Linie mit angrenzenden Vertices](images/d3d10-gs.png)

|     |                 |
|-----|-----------------|
| TV  | Dreiecks Scheitelpunkt |
| Staff  | Angrenzender Scheitelpunkt |
| LV  | Zeilen Scheitelpunkt     |



 

Die Geometry-Shader-Stufe kann den \_ vom System generierten SV primitiveid [-Wert nutzen](d3d10-graphics-programming-guide-input-assembler-stage-using.md) , der automatisch von der IA generiert wird. Dies ermöglicht das Abrufen und berechnen primitiver Daten, wenn gewünscht.

Die Geometry-Shader-Stufe ist in der Lage, mehrere Vertices auszugeben, die eine einzelne ausgewählte Topologie bilden (die GS-Phasen-ausgabetopologien sind verfügbar: tristrip, linestrip und PointList). Die Anzahl der ausgegebenen primitiven kann in jedem Aufruf des Geometry-Shaders frei variieren, obwohl die maximale Anzahl von Scheitel Punkten, die ausgegeben werden konnten, statisch deklariert werden muss. Von einem Geometry-Shader-Aufruf ausgegebene Bereichs Längen können beliebig sein, und neue Bänder können über die Funktion " [restartstrip](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip) HLSL" erstellt werden.

Die Geometrie-Shader-Ausgabe kann in der Raster-Phase und/oder in einem Vertex-Puffer im Arbeitsspeicher über die Stream-Ausgabe Phase ausgegeben werden. Die Ausgabe in den Arbeitsspeicher wird auf einzelne Punkt-/Linien-/dreiterlisten erweitert (genau so, wie Sie an den Rasterizer übermittelt werden).

Wenn ein Geometry-Shader aktiv ist, wird er einmal für jedes primitive aufgerufen, das in der Pipeline weiter unten oder generiert wurde. Bei jedem Aufruf des Geometry-Shaders werden die Daten für den aufrufenden primitiven als Eingabe angezeigt, unabhängig davon, ob es sich um einen einzelnen Punkt, eine einzelne Zeile oder ein einzelnes Dreieck handelt. Ein Dreiecks Streifen von früheren in der Pipeline führt zu einem Aufruf des Geometry-Shaders für jedes einzelne Dreieck im Strip (als wäre der Strip in eine Dreiecks Liste ausgelagert). Alle Eingabedaten für jeden Scheitelpunkt in der einzelnen primitiven sind verfügbar (d. h. 3 Scheitel Punkte für Dreieck) sowie angrenzende Scheitelpunkt Daten, sofern zutreffend/verfügbar.

Ein Geometry-Shader gibt Daten jeweils einen Scheitelpunkt aus, indem er Vertices an ein ausgabestreamobjekt anfügt. Die Topologie der Streams wird durch eine Fixed-Deklaration bestimmt, wobei eine der folgenden Punkte als Ausgabe für die GS-Stufe ausgewählt wird. Es gibt drei Arten von Streamobjekten, pointstream, LineStream und dreianglestream, bei denen es sich um Vorlagen Objekte handelt. Die Topologie der Ausgabe wird durch den jeweiligen Objekttyp bestimmt, während das Format der Scheitel Punkte, die an den Stream angehängt werden, durch den Vorlagentyp bestimmt wird. Die Ausführung einer Geometry-shaderinstanz ist atomarisch von anderen aufrufen, mit dem Unterschied, dass die den Streams hinzugefügten Daten seriell sind. Die Ausgaben eines gegebenen Aufrufs eines Geometry-Shaders sind von anderen aufrufen unabhängig (obwohl die Reihenfolge beachtet wird). Ein Geometry-Shader, der Dreiecks Streifen erzeugt, startet bei jedem Aufruf einen neuen Strip.

Wenn eine Geometrie-shaderausgabe als vom System interpretierter Wert (z. b. SV \_ rendertargetarrayindex oder SV \_ Position) identifiziert wird, untersucht die Hardware diese Daten und führt ein gewisses Verhalten aus, das von dem Wert abhängt, zusätzlich zur Möglichkeit, die Daten selbst an die nächste Shader-Stufe für die Eingabe zu übergeben. Wenn eine solche Datenausgabe aus dem Geometry-Shader für die Hardware auf primitiver Basis (z. b. SV \_ rendertargetarrayindex oder SV \_ viewportarrayindex) und nicht pro Scheitelpunkt (z. b. SV \_ clipdistance \[ n \] oder SV \_ Position) Bedeutung hat, werden die pro-primitive Daten aus dem führenden Vertex entnommen, der für das primitive ausgegeben wurde

Teilweise abgeschlossene primitive können vom Geometry-Shader generiert werden, wenn der Geometrie-Shader endet und der primitive unvollständig ist. Unvollständige primitive werden automatisch verworfen. Dies ähnelt der Art und Weise, in der die IA teilweise abgeschlossene primitive behandelt.

Der Geometry-Shader kann Lade-und Textur-samplingvorgänge ausführen, bei denen keine Bildschirm breiten Ableitungen erforderlich sind (samplelevel, samplecmplevelzero, samplegrad).

Folgende Algorithmen können im Geometry-Shader implementiert werden:

-   Punkt Sprite-Erweiterung
-   Dynamische Partikelsysteme
-   Pelz/FIN-Generierung
-   Schattenvolumengenerierung
-   Einzelne Pass-to-cubemap
-   Austauschen von Per-Primitive Material
-   Per-Primitive Material-Setup, einschließlich der Generierung von baryzentrierten Koordinaten als primitive Daten, sodass ein Pixelshader eine benutzerdefinierte Attribut interpolung ausführen kann (ein Beispiel für eine normale Interpolations Stufe höherer Ordnung finden Sie unter [cubemapgs Sample](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafik Pipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipeline Stufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 