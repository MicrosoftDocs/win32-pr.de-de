---
title: Geometry Shader Stage
description: Die Geometry-Shader-Phase (GS) führt anwendungsspezifischen Shadercode mit Scheiteltices als Eingabe und der Möglichkeit aus, Scheitelungen bei der Ausgabe zu generieren.
ms.assetid: F3208862-980E-403F-9154-13B34A882787
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94d568b9eb62b2545721acebfda865f7f2553597fb999a3a647164106c836369
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952910"
---
# <a name="geometry-shader-stage"></a>Geometry Shader Stage

Die Geometry-Shader-Phase (GS) führt anwendungsspezifischen Shadercode mit Scheiteltices als Eingabe und der Möglichkeit aus, Scheitelungen bei der Ausgabe zu generieren.

## <a name="the-geometry-shader"></a>Der Geometrie-Shader

Im Gegensatz zu Vertex-Shadern, die auf einem einzelnen Scheitelpunkt arbeiten, sind die Eingaben des Geometrie-Shaders die Scheitelpunkte für einen vollständigen Primitiven (zwei Scheitelpunkte für Linien, drei Scheitelpunkte für Dreiecke oder ein einzelner Scheitelpunkt für Punkt). Geometrie-Shader können auch die Scheitelpunktdaten für die an den Rand angrenzenden Primitiven als Eingabe (zwei zusätzliche Scheitelpunkte für eine Linie, weitere drei für ein Dreieck) als Eingabe verwenden. Die folgende Abbildung zeigt ein Dreieck und eine Linie mit angrenzenden Scheitellinien.

![Abbildung eines Dreiecks und einer Linie mit angrenzenden Scheitellinien](images/d3d10-gs.png)

|     | type                |
|-----|-----------------|
| **TV**  | Dreiecksvertex |
| **Av**  | Benachbarter Scheitelpunkt |
| **LV**  | Linienvertex     |



 

Die geometry-shader-Phase kann den vom Sv PrimitiveID-System generierten Wert nutzen, der automatisch von der \_ IA generiert [](d3d10-graphics-programming-guide-input-assembler-stage-using.md) wird. Auf diese Weise können primitive Daten abgerufen oder bei Wunsch berechnet werden.

Die Geometry-Shader-Stufe kann mehrere Scheitelpunkts aus einer einzigen ausgewählten Topologie aus geben (ausgabetopologien der GS-Stufe sind verfügbar: tristrip, linestrip und pointlist). Die Anzahl der ausgegebenen Primitive kann bei jedem Aufruf des Geometrie-Shaders frei variieren, obwohl die maximale Anzahl von Scheitelzeichen, die ausgegeben werden könnten, statisch deklariert werden muss. Striplängen, die von einem Aufruf eines Geometrie-Shaders ausgegeben werden, können beliebig sein, und neue Strips können über die RESTARTStrip-HLSL-Funktion erstellt werden. [](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-so-restartstrip)

Die Ausgabe des Geometrie-Shaders kann über die Streamausgabephase an die Rasterizerphase und/oder an einen Scheitelpunktpuffer im Arbeitsspeicher übertragen werden. Die ausgabe, die in den Arbeitsspeicher eingespeist wird, wird auf einzelne Punkt-/ Linien-/Dreieckslisten erweitert (genau wie sie an den Rasterizer übergeben würden).

Wenn ein Geometrie-Shader aktiv ist, wird er einmal für jeden Primitiven aufgerufen, der zuvor in der Pipeline übergeben oder generiert wurde. Jeder Aufruf des Geometrie-Shaders sieht die Daten für den aufrufenden Primitiven als Eingabe, unabhängig davon, ob es sich um einen einzelnen Punkt, eine einzelne Linie oder ein einzelnes Dreieck handelt. Ein Dreiecksstreifen aus einer früheren Pipeline würde zu einem Aufruf des Geometrie-Shaders für jedes einzelne Dreieck im Bereich führen (als ob der Bereich in eine Dreiecksliste erweitert würde). Alle Eingabedaten für jeden Scheitelpunkt in der einzelnen Primitiven sind verfügbar (d. h. drei Scheitelpunkte für Dreiecke) sowie ggf. benachbarte Scheitelpunktdaten.

Ein Geometrie-Shader gibt Daten nach und nach aus, indem er Scheitelpunkte an ein Ausgabestreamobjekt anfügen. Die Topologie der Streams wird durch eine feste Deklaration bestimmt, die eine der folgenden Deklarationen auswählt: PointStream, LineStream oder TriangleStream als Ausgabe für die GS-Phase. Es sind drei Arten von Streamobjekten verfügbar: PointStream, LineStream und TriangleStream, bei denen es sich um Vorlagenobjekte handelt. Die Topologie der Ausgabe wird durch ihren jeweiligen Objekttyp bestimmt, während das Format der Scheitelungen, die an den Stream angefügt werden, durch den Vorlagentyp bestimmt wird. Die Ausführung einer Geometry-Shaderinstanz ist atomar von anderen Aufrufen, mit der Ausnahme, dass den Datenströmen hinzugefügte Daten seriell sind. Die Ausgaben eines angegebenen Aufrufs eines Geometrie-Shaders sind unabhängig von anderen Aufrufen (obwohl die Reihenfolge beachtet wird). Ein Geometrie-Shader, der Dreiecksstreifen generiert, startet bei jedem Aufruf einen neuen Strip.

Wenn eine Geometrie-Shaderausgabe als vom System interpretierter Wert identifiziert wird (z. B. SV RenderTargetArrayIndex oder SV Position), untersucht die Hardware diese Daten und führt ein verhaltenes Verhalten aus, das vom Wert abhängig ist, und kann die Daten nicht nur zur Eingabe an die nächste \_ \_ Shaderstufe übergeben. Wenn eine solche Datenausgabe des Geometrie-Shaders für die Hardware auf primitiver Basis (z. B. SV \_ RenderTargetArrayIndex oder SV ViewportArrayIndex) eine Bedeutung hat, anstatt auf Scheitelpunktbasis (z. B. \_ SV \_ ClipDistance n oder \[ SV Position), \] werden die primitiven Daten aus dem führenden Scheitelpunkt übernommen, der für den primitiven Typ ausgegeben \_ wird.

Teilweise abgeschlossene Primitive können vom Geometrie-Shader generiert werden, wenn der Geometrie-Shader endet und der Primitive unvollständig ist. Unvollständige Primitive werden automatisch verworfen. Dies ähnelt der Behandlung teilweise abgeschlossener Primitive durch die IA.

Der Geometrie-Shader kann Auslastungs- und Texturstastingvorgänge ausführen, bei denen keine Ableitungen des Bildschirmraums erforderlich sind (samplelevel, samplecmplevelzero, samplegrad).

Folgende Algorithmen können im Geometrie-Shader implementiert werden:

-   Punkt-Sprite-Erweiterung
-   Dynamische Partikelsysteme
-   Generierung von "Wild/Ellen"
-   Schattenvolumengenerierung
-   Single Pass Render-to-Cubemap
-   Per-Primitive Materialtausch
-   Per-Primitive MaterialSetup: Einschließlich der Generierung von baryzentrierten Koordinaten als primitive Daten, sodass ein Pixel-Shader eine benutzerdefinierte Attributinterpolation ausführen kann (ein Beispiel für eine höherwertige normaler Interpolation finden Sie unter [CubeMapGS-Beispiel](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Grafikpipeline](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Pipelinestufen (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 