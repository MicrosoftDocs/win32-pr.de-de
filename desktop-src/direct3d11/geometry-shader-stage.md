---
title: Geometry Shader Stage
description: Die Geometry-Shader-Phase (GS) führt anwendungsspezifischen Shadercode mit Scheiteltices als Eingabe und der Möglichkeit aus, Scheitelungen bei der Ausgabe zu generieren.
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3099ed5ede8dd89dc607ed838ff6e3fabfb16a69
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335364"
---
# <a name="geometry-shader-stage"></a>Geometry Shader Stage

Die Geometry-Shader-Phase (GS) führt anwendungsspezifischen Shadercode mit Scheiteltices als Eingabe und der Möglichkeit aus, Scheitelungen bei der Ausgabe zu generieren.

## <a name="the-geometry-shader"></a>Der Geometrie-Shader

Im Gegensatz zu Vertex-Shadern, die auf einem einzelnen Scheitelpunkt arbeiten, sind die Eingaben des Geometrie-Shaders die Scheitelpunkte für einen vollständigen Primitiven (zwei Scheitelpunkte für Linien, drei Scheitelpunkte für Dreiecke oder ein scheitelpunkt für Punkt). Geometrie-Shader können auch die Scheitelpunktdaten für die an den Rand angrenzenden Primitiven als Eingabe (zwei zusätzliche Scheitelpunkte für eine Linie, weitere drei für ein Dreieck) als Eingabe verwenden. Die folgende Abbildung zeigt ein Dreieck und eine Linie mit angrenzenden Scheitellinien.

![Abbildung eines Dreiecks und einer Linie mit angrenzenden Scheitellinien](images/d3d10-gs.png)

|     | type                |
|-----|-----------------|
| **TV**  | Dreiecksvertex |
| **Av**  | Benachbarter Scheitelpunkt |
| **Lv**  | Linienvertex     |



 

Die Geometry-Shader-Stufe kann den vom SV PrimitiveID-System generierten Wert nutzen, der automatisch von der \_ IA generiert [](d3d10-graphics-programming-guide-input-assembler-stage-using.md) wird. Auf diese Weise können primitive Daten abgerufen oder bei Wunsch berechnet werden.

Die geometry-shader-Stufe kann mehrere Scheitelpunkts aus einer einzigen ausgewählten Topologie aus geben (ausgabetopologien der GS-Stufe sind verfügbar: tristrip, linestrip und pointlist). Die Anzahl der ausgegebenen Primitive kann bei jedem Aufruf des Geometrie-Shaders frei variieren, obwohl die maximale Anzahl von Scheitelzeichen, die ausgegeben werden könnten, statisch deklariert werden muss. Striplängen, die von einem Aufruf eines Geometrie-Shaders ausgegeben werden, können beliebig sein, und neue Strips können über die RESTARTStrip-HLSL-Funktion erstellt werden. [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip)

Die Ausgabe des Geometrie-Shaders kann über die Streamausgabephase an die Rasterizerphase und/oder an einen Scheitelpunktpuffer im Arbeitsspeicher übertragen werden. Die an den Arbeitsspeicher gespeiste Ausgabe wird auf einzelne Punkt-/Linien-/Dreieckslisten erweitert (genau so, wie sie an den Rasterizer übergeben würden).

Wenn ein Geometrie-Shader aktiv ist, wird er einmal für jeden Primitiven aufgerufen, der zuvor in der Pipeline übergeben oder generiert wurde. Jeder Aufruf des geometry-Shaders betrachtet die Daten für den aufrufende Primitiven als Eingabe, unabhängig davon, ob es sich um einen einzelnen Punkt, eine einzelne Linie oder ein einzelnes Dreieck handelt. Ein Dreiecksstreifen von früher in der Pipeline würde zu einem Aufruf des Geometrie-Shaders für jedes einzelne Dreieck im Strip führen (so, als ob der Strip in eine Dreiecksliste erweitert würde). Alle Eingabedaten für jeden Scheitelpunkt im einzelnen Primitiven sind verfügbar (d. h. drei Scheitelpunkte für Dreieck) sowie ggf. angrenzende Scheitelpunktdaten.

Ein Geometry-Shader gibt Daten nacheinander nacheinander aus, indem Scheitelpunkte an ein Ausgabestreamobjekt angefügt werden. Die Topologie der Datenströme wird durch eine feste Deklaration bestimmt, bei der folgendes ausgewählt wird: PointStream, LineStream oder TriangleStream als Ausgabe für die GS-Phase. Es sind drei Arten von Streamobjekten verfügbar: PointStream, LineStream und TriangleStream, bei denen es sich um Objekte mit Vorlagen handelt. Die Topologie der Ausgabe wird durch ihren jeweiligen Objekttyp bestimmt, während das Format der an den Stream angefügten Scheitelpunkte vom Vorlagentyp bestimmt wird. Die Ausführung einer geometry-Shaderinstanz ist atomar aus anderen Aufrufen, mit der Ausnahme, dass den Streams hinzugefügte Daten seriell sind. Die Ausgaben eines angegebenen Aufrufs eines Geometry-Shaders sind unabhängig von anderen Aufrufen (obwohl die Reihenfolge beachtet wird). Ein Geometrie-Shader, der Dreiecksstreifen generiert, startet bei jedem Aufruf einen neuen Strip.

Wenn eine Geometrie-Shaderausgabe als vom System interpretierter Wert identifiziert wird (z. B. SV \_ RenderTargetArrayIndex oder SV Position), untersucht die Hardware diese Daten und führt abhängig \_ vom Wert ein Verhalten aus, zusätzlich zur Möglichkeit, die Daten selbst zur Eingabe an die nächste Shaderphase zu übergeben. Wenn eine solche Datenausgabe des Geometrie-Shaders für die Hardware auf primitiver Basis (z. B. SV \_ RenderTargetArrayIndex oder SV ViewportArrayIndex) eine Bedeutung hat, anstatt auf Scheitelpunktbasis (z. B. \_ SV \_ ClipDistance n oder \[ SV Position), \] werden die pro \_ primitiven Daten aus dem für den primitiven Typ ausgegebenen führenden Scheitelpunkt übernommen.

Teilweise abgeschlossene Primitive können vom Geometrie-Shader generiert werden, wenn der Geometrie-Shader endet und der Grundtyp unvollständig ist. Unvollständige Primitive werden automatisch verworfen. Dies ähnelt der Behandlung teilweise abgeschlossener Primitive durch die IA.

Der Geometrie-Shader kann Auslastungs- und Texturstastingvorgänge ausführen, bei denen keine Ableitungen des Bildschirmbereichs erforderlich sind (samplelevel, samplecmplevelzero, samplegrad).

Folgende Algorithmen können im Geometrie-Shader implementiert werden:

-   Punkt-Sprite-Erweiterung
-   Dynamische Partikelsysteme
-   Generierung von"/"Ellen"
-   Schattenvolumengenerierung
-   Single Pass Render-to-Cubemap
-   Per-Primitive Materialtausch
-   Per-Primitive MaterialSetup: Einschließlich der Generierung von baryzentrierten Koordinaten als primitive Daten, sodass ein Pixel-Shader eine benutzerdefinierte Attributinterpolation ausführen kann (ein Beispiel für eine höherwertige Normalinterpolation finden Sie unter [CubeMapGS-Beispiel](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipelinestufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 