---
title: Schattierung mit variabler Rate (VRS)
description: Schattierung mit variabler Rate oder grobe Pixelschattierung ist ein Mechanismus, mit dem Sie Renderingleistung/Leistung mit Raten zuordnen können, die in Ihrem gerenderten &mdash; &mdash; Bild variieren.
ms.localizationpriority: high
ms.topic: article
ms.date: 04/08/2019
ms.openlocfilehash: 2f207cddee978915788291fc0ffe55160e6a93c6
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380764"
---
# <a name="variable-rate-shading-vrs"></a>Schattierung mit variabler Rate (VRS)

## <a name="the-motivation-for-vrs"></a>Die Motivation für VRS
Aufgrund von Leistungseinschränkungen kann es sich ein Grafikrenderer nicht immer leisten, jedem Teil seines Ausgabebilds die gleiche Qualität zu bieten. Schattierung mit variabler Rate oder Schattierung mit grobem Pixel ist ein Mechanismus, mit dem Sie Renderingleistung/Leistung mit Raten zuordnen können, die in Ihrem gerenderten &mdash; &mdash; Bild variieren.

In einigen Fällen kann die Schattierungsrate mit geringer oder keiner Verringerung der wahrnehmbaren Ausgabequalität reduziert werden. führt zu einer Leistungsverbesserung, die im Wesentlichen kostenlos ist.

## <a name="without-vrsmdashmulti-sample-anti-aliasing-with-supersampling"></a>Ohne &mdash; VRS-Multi-Sample-Antialiasing mit Supersampling
Ohne Schattierung variabler Rate ist die einzige Möglichkeit, die Schattierungsrate zu steuern, das Multi-Sample Anti-Aliasing (MSAA) mit stichprobenbasierter Ausführung (auch als Supersampling bezeichnet).

MSAA ist ein Mechanismus zum Reduzieren geometrischer Aliasings und Verbessern der Renderingqualität eines Bilds im Vergleich zur Nicht-Verwendung von MSAA. Die MSAA-Stichprobenanzahl, die 1x, 2x, 4x, 8x oder 16x sein kann, bestimmt die Anzahl der pro Renderzielpixel zugeordneten Stichproben. Die MSAA-Stichprobenanzahl muss im Vor-/Nachher bekannt sein, wenn das Ziel zugeordnet wird, und kann danach nicht mehr geändert werden.

Die Übersamplingung bewirkt, dass der Pixel-Shader einmal pro Stichprobe aufgerufen wird, mit einer höheren Qualität, aber auch höheren Leistungskosten im Vergleich zur Ausführung pro Pixel.

Ihre Anwendung kann die Schattierungsrate steuern, indem sie zwischen pixelbasierter Ausführung oder MSAA-with-supersampling wählt. Diese beiden Optionen bieten keine sehr gute Kontrolle. Außerdem können Sie eine niedrigere Schattierungsrate für eine bestimmte Objektklasse im Vergleich zum Rest des Bilds wünschen. Solche Objekte können ein Objekt hinter einem HUD-Element oder eine Transparenz, eine Weichzeichnung (Tiefen des Felds, Bewegung usw.) oder eine optische Verzerrung aufgrund von VR-Brillen umfassen. Dies wäre jedoch nicht möglich, da die Schattierungsqualität und die Kosten für das gesamte Bild festgelegt sind.

## <a name="with-variable-rate-shading-vrs"></a>Mit VariableRate Shading (VRS)
Das VRS-Modell (Variable-Rate Shading) erweitert supersampling-with-MSAA in die entgegengesetzte Richtung "coarse pixel", indem das Konzept der groben Schattierung hinzugefügt wird. Hier kann die Schattierung mit einer Häufigkeit durchgeführt werden, die eher grob als ein Pixel ist. Anders ausgedrückt: Eine Gruppe von Pixeln kann als einzelne Einheit schattiert werden, und das Ergebnis wird dann an alle Stichproben in der Gruppe übertragen.

Mit einer API für die schattierte Schattierung kann Ihre Anwendung die Anzahl der Pixel angeben, die zu einer schattierten Gruppe gehören, oder die Anzahl *der pixeligen Pixel.* Sie können die größe der groben Pixel nach dem Zuordnen des Renderziels variieren. Daher können verschiedene Teile des Bildschirms oder verschiedene Zeichnen-Läufe unterschiedliche Schattierungsraten aufweisen.

Die folgende Tabelle beschreibt, welche MSAA-Ebene mit welcher groben Pixelgröße unterstützt wird. Einige werden auf keiner Plattform unterstützt. während andere basierend auf einer Funktion (*AdditionalShadingRatesSupported*) bedingt aktiviert sind, die durch "Cap" angegeben wird.

![In der Tabelle wird die größe des unausgegreiften Pixels für M S A A-Ebenen angezeigt.](images/CoarsePixelSizeSupport.PNG "Grobe Pixelgrößen")

Für die featureebenen, die im nächsten Abschnitt erläutert werden, gibt es keine Kombination aus größe und Stichprobenanzahl für ungenaue Pixel, bei der hardware mehr als 16 Stichproben pro Aufruf des Pixelshaders nachverfolgen muss. Diese Kombinationen sind in der obigen Tabelle halbtonschattend.

## <a name="feature-tiers"></a>Featureebenen
Es gibt zwei Ebenen für die VRS-Implementierung und zwei Funktionen, die Sie abfragen können. Jede Ebene wird nach der Tabelle ausführlicher beschrieben.

![Die Tabelle zeigt die funktionen, die in Ebene 1 und Ebene 2 verfügbar sind.](images/Tiers.PNG "VRS-Ebenen")

### <a name="tier-1"></a>Ebene 1
- Schattierungsrate kann nur pro Zeichnen angegeben werden. nicht präziser als das.
- Die Schattierungsrate gilt einheitlich für das, was unabhängig davon gezeichnet wird, wo sie sich innerhalb des Renderziels befindet.

### <a name="tier-2"></a>Ebene 2
- Die Schattierungsrate kann wie in Ebene 1 pro Zeichnen angegeben werden. Sie kann auch durch eine Kombination von pro Zeichnen-Basis und von angegeben werden:
  - Semantik von jedem aufrufenden Scheitelpunkt und
  - ein Bildschirmbereichsbild.
- Schattierungsraten aus den drei Quellen werden mithilfe einer Reihe von Kombinationen kombiniert.
- Die Größe der Bildkachel im Bildschirmbereich ist 16 x 16 oder kleiner.
- Die von Ihrer Anwendung angeforderte Schattierungsrate wird garantiert genau übermittelt (um die Genauigkeit von temporalen und anderen Filterfiltern zu gewährleisten).
- SV_ShadingRate PS-Eingabe wird unterstützt.
- Die Schattierungsrate pro Pro-Provoking-Scheitelpunkt (auch als pro primitiv bezeichnet) ist gültig, wenn ein Viewport verwendet und nicht `SV_ViewportArrayIndex` in geschrieben wird.
- Die Pro-Provoking-Vertexrate kann mit mehr als einem Viewport verwendet werden, wenn die *SupportsPerVertexShadingRateWithMultipleViewports-Funktion* auf festgelegt `true` ist. Darüber hinaus kann in diesem Fall diese Rate verwendet werden, wenn `SV_ViewportArrayIndex` in geschrieben wird.

### <a name="list-of-capabilities"></a>Liste der Funktionen
- *AdditionalShadingRatesSupported*
  - Boolescher Typ.
  - Gibt an, ob die Pixelgrößen 2x4, 4x2 und 4 x 4 für das Rendern mit Einzelstichproben unterstützt werden. und ob die grobe Pixelgröße 2x4 für 2-fache MSAA unterstützt wird.
- *SupportsPerVertexShadingRateWithMultipleViewports*
  - Boolescher Typ.
  - Gibt an, ob mehrere Viewports mit der Schattierungsrate pro Scheitelpunkt (auch als pro Primitive bezeichnet) verwendet werden können.

## <a name="specifying-shading-rate"></a>Angeben der Schattierungsrate
Aus Gründen der Flexibilität in Anwendungen stehen verschiedene Mechanismen zur Verfügung, um die Schattierungsrate zu steuern. Je nach Hardwarefeatureebene sind verschiedene Mechanismen verfügbar.

### <a name="command-list"></a>Befehlsliste
Dies ist der einfachste Mechanismus zum Festlegen der Schattierungsrate. Sie ist auf allen Ebenen verfügbar.

Ihre Anwendung kann mithilfe der [ **ID3D12GraphicsCommandList5::RSSetShadingRate-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate)eine grobe Pixelgröße angeben. Diese API nimmt ein einzelnes Enumerationsargument an. Die API bietet eine allgemeine Steuerung des Qualitätsgrads für &mdash; das Rendern, um die Schattierungsrate pro Zeichnen festzulegen.

Werte für diesen Zustand werden durch die [**D3D12_SHADING_RATE-Enumeration**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) ausgedrückt.

#### <a name="coarse-pixel-size-support"></a>Unterstützung für coarse pixel size
Die Schattierungsraten 1x1, 1x2, 2x2 und 2x2 werden auf allen Ebenen unterstützt.

Die Funktion *AdditionalShadingRatesSupported* gibt an, ob 2x4, 4x2 und 4x4 auf dem Gerät unterstützt werden.

### <a name="screen-space-image-image-based"></a>Bildschirmraumbild (bildbasiert)
Auf Ebene 2 und höher können Sie die Pixelschattierungsrate mit einem Bildschirmraumbild angeben.

Mit dem Bildschirmbereichsbild kann Ihre Anwendung ein Bild mit einer LOD-Maske (Level of Detail, Detailebene) erstellen, das Bereiche unterschiedlicher Qualität angibt, z. B. Bereiche, die durch Bewegungsunschärfe, Tiefenbereichsunschärfe, transparente Objekte oder HUD-UI-Elemente abgedeckt werden. Die Auflösung des Bilds befindet sich in Makroblocks. sie ist nicht in der Auflösung des Renderziels. Anders ausgedrückt: Die Schattierungsratedaten werden mit einer Granularität von 8 x 8 oder 16 x 16 Pixeln angegeben, wie durch die VRS-Kachelgröße angegeben.

#### <a name="tile-size"></a>Tile size (Kachelgröße)
Ihre Anwendung kann eine API abfragen, um die unterstützte VRS-Kachelgröße für ihr Gerät abzurufen.

Kacheln sind quadratisch, und die Größe bezieht sich auf die Breite oder Höhe der Kachel in Texel.

Wenn die Hardware die Schattierung mit variabler Ratenebene 2 nicht unterstützt, gibt die Funktionsabfrage für die Kachelgröße 0 zurück.

Wenn die *Hardware* die Schattierung variabler Ebenen 2 unterstützt, ist die Kachelgröße einer dieser Werte.

- 8
- 16
- 32

#### <a name="screen-space-image-size"></a>Bildgröße des Bildschirmbereichs
Für ein Renderziel der Größe {rtWidth, rtHeight}, wobei eine bestimmte Kachelgröße namens **VRSTileSize** verwendet wird, weist das Bildschirmraumbild, das es abdeckt, diese Dimensionen auf.

```cpp
{ ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize) }
```

Das Bild des Bildschirmbereichs oben links (0, 0) ist links oben (0, 0) des Renderziels gesperrt.

Zum Suchen der (x,y)-Koordinate einer Kachel, die einer bestimmten Position im Renderziel entspricht, dividieren Sie die Fensterraumkoordinaten von (x, y) durch die Kachelgröße und ignorieren dabei Bruchbits.

Wenn das Bildschirmbereichsbild größer ist, als es für ein bestimmtes Renderziel sein muss, werden die zusätzlichen Teile rechts und/oder unten nicht verwendet.

Wenn das Bildschirmbereichsbild für ein bestimmtes Renderziel zu klein ist, ergibt jeder Versuch, das Bild über die tatsächlichen Werte zu lesen, eine Standardschattierungsrate von 1x1. Dies liegt daran, dass das Bild oben links im Bildschirmbereich (0, 0) an der oberen linken Seite des Renderziels (0, 0) gesperrt ist und "Lesen über die Renderziel-Werte hinaus" bedeutet, dass die Werte für x und y zu groß gelesen werden.

#### <a name="format-layout-resource-properties"></a>Format, Layout, Ressourceneigenschaften
Das Format dieser Oberfläche ist eine 8-Bit-Einzelkanaloberfläche ([**DXGI_FORMAT_R8_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

Die Ressource ist die **Dimension TEXTURE2D.**

Sie kann nicht arrayiert oder übersprungen werden. Sie muss explizit eine MIP-Ebene haben.

Sie verfügt über die Stichprobenanzahl 1 und die Stichprobenqualität 0.

Es verfügt über das Texturlayout **UNKNOWN**. Es kann implizit kein Zeilen-Hauptlayout sein, da adapterübergreifendes Layout nicht zulässig ist.

Die erwartete Art und Weise, in der die Bilddaten des Bildschirmbereichs aufgefüllt werden, ist entweder
1. Schreiben der Daten mithilfe eines Compute-Shaders; Das Bildschirmbereichsbild ist als UAV gebunden, oder
2. Kopieren Sie die Daten in das Bildschirmbereichsbild.

Beim Erstellen des Bildschirmbereichsbilds sind diese Flags zulässig.

- Keine
- ALLOW_UNORDERED_ACCESS
- DENY_SHADER_RESOURCE

Diese Flags sind nicht zulässig.

- ALLOW_RENDER_TARGET
- ALLOW_DEPTH_STENCIL
- ALLOW_CROSS_ADAPTER
- ALLOW_SIMULTANEOUS_ACCESS
- VIDEO_DECODE_REFERENCE_ONLY

Der Heaptyp der Ressource kann weder UPLOAD noch READBACK sein.

Die Ressource kann nicht SIMULTANEOUS_ACCESS werden. Die Ressource darf nicht adapterübergreifend sein.

#### <a name="data"></a>Daten
Jedes Byte des Bildschirmraumbilds entspricht [](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) einem Wert der D3D12_SHADING_RATE-Enumeration.

#### <a name="resource-state"></a>Ressourcenzustand
Eine Ressource muss in einen schreibgeschützten Zustand übergehen, wenn sie als Bildschirmraumbild verwendet wird. Zu diesem Zweck wird ein schreibgeschützter Zustand [**D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)definiert.

Die Imageressource wird aus diesem Zustand umgestellt, um wieder schreibbar zu werden.

#### <a name="setting-the-image"></a>Festlegen des Bilds
Das Bildschirmraumbild zum Angeben der Shaderrate wird in der Befehlsliste festgelegt.

Eine Ressource, die als Schattierungsratenquelle festgelegt wurde, kann in keiner Shaderphase gelesen oder geschrieben werden.

Ein `null` Bildschirmraumbild kann zum Angeben der Shaderrate festgelegt werden. Dies hat zur Folge, dass 1x1 konsistent als Beitrag aus dem Bildschirmbereichsbild verwendet wird. Das Bildschirmraumbild kann anfänglich als auf festgelegt betrachtet `null` werden.

#### <a name="promotion-and-decay"></a>Heraufstufung und Verfall
Eine Bildressource im Bildschirmbereich hat keine besonderen Auswirkungen auf die Heraufstufung oder den Verfall.

### <a name="per-primitive-attribute"></a>Attribut pro Grundtyp
Ein attributspezifisches Attribut fügt die Möglichkeit hinzu, einen Schattierungsratenbegriff als Attribut aus einem aufrufenden Scheitelpunkt anzugeben. Dieses Attribut ist flach schattiert, d. &nd; es wird an alle Pixel im aktuellen Dreieck oder Linienprimitiven &mdash; propagiert. Die Verwendung eines primitiven Attributs kann im Vergleich zu den anderen Schattierungsratenspezifizierern eine feiner abgrenzende Steuerung der Bildqualität ermöglichen.

Das attributspezifische Attribut ist eine festlegbare Semantik mit dem Namen `SV_ShadingRate` . `SV_ShadingRate`ist als Teil des [HLSL-Shadermodells 6.4 vorhanden.](/windows/desktop/direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12)

Wenn vs oder GS festlegen, VRS jedoch nicht aktiviert ist, hat die `SV_ShadingRate` semantische Einstellung keine Auswirkungen. Wenn kein Wert für pro Primitiv angegeben wird, wird ein Schattierungsratenwert von 1x1 als pro `SV_ShadingRate` primitivem Beitrag angenommen.

### <a name="combining-shading-rate-factors"></a>Kombinieren von Schattierungsratenfaktoren
Die verschiedenen Quellen der Schattierungsrate werden anhand dieses Diagramms nacheinander angewendet.

![Das Diagramm zeigt einen Pipelinezustand mit der Bezeichnung A mit der Provoking-Schattierungsrate des Scheitelpunkts mit der Bezeichnung B, angewendet auf einen Combiner und der bildbasierten Schattierungsrate mit der Bezeichnung B, die auf einen Combiner angewendet wird.](images/Combiners.PNG "Schattieren von Combinern")

Jedes Paar aus A und B wird mithilfe eines Kombinierers kombiniert.

\* Beim Angeben einer Shaderrate nach Scheitelpunktattribut.

- Wenn ein Geometrie-Shader verwendet wird, kann die Schattierungsrate dadurch angegeben werden.
- Wenn kein Geometrie-Shader verwendet wird, wird die Schattierungsrate durch den aufrufenden Scheitelpunkt angegeben.

#### <a name="list-of-combiners"></a>Liste der Kombinierer
Die folgenden Kombinationen werden unterstützt. Verwenden eines Combiners (C) und zweier Eingaben (A und B).

- **Passthrough:**. C.xy = A.xy.
- **Überschreiben Sie**. C.xy = B.xy.
- **Höhere Qualität.** C.xy = min(A.xy, B.xy).
- **Niedrigere Qualität.** C.xy = max(A.xy, B.xy).
- **Wenden Sie Kosten B relativ zu A an.** C.xy = min(maxRate, A.xy + B.xy).

dabei `maxRate` ist die größte zulässige Dimension von grobem Pixel auf dem Gerät. Dies wäre

- **D3D12_AXIS_SHADING_RATE_2X** (d. h. der Wert 1), wenn AdditionalShadingRatesSupported `false` ist.
- **D3D12_AXIS_SHADING_RATE_4X** (d.h. der Wert 2), wenn AdditionalShadingRatesSupported `true` ist.

Die Auswahl des Combiners für die Schattierung variabler Raten wird in der Befehlsliste über [**ID3D12GraphicsCommandList5::RSSetShadingRate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate)festgelegt.

Wenn keine Kombinierer festgelegt werden, bleiben sie bei der Standardeinstellung PASSTHROUGH.

Wenn die Quelle für einen Combiner ein [**D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate)ist, was in der Unterstützungstabelle nicht zulässig ist, wird die Eingabe mit einer *unterstützten* Schattierungsrate bereinigt.

Wenn die Ausgabe eines Combiners keiner schattierungsrate entspricht, die auf der Plattform unterstützt wird, wird das Ergebnis mit einer *unterstützten* Schattierungsrate bereinigt.

### <a name="default-state-and-state-clearing"></a>Standardzustand und Zustandsbereinigung
Alle Schattierungsratequellen, nämlich

- die vom Pipelinezustand angegebene Rate (in der Befehlsliste angegeben),
- die vom Bild angegebene Bildfrequenz im Bildschirmbereich und
- das Pro-Primitive-Attribut

hat den Standardwert **D3D12_SHADING_RATE_1X1**. Die Standard-Combiner sind {PASSTHROUGH, PASSTHROUGH}.

Wenn kein Bildschirmbereichsbild angegeben ist, wird von dieser Quelle eine Schattierungsrate von 1x1 abgeleitet.

Wenn kein primitives Attribut angegeben wird, wird von dieser Quelle eine Schattierungsrate von 1x1 abgeleitet.

[ID3D12CommandList::ClearState](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate) setzt die vom Pipelinezustand angegebene Rate auf den Standardwert und die Auswahl des Bildschirmbereichsbilds auf den Standardwert "Kein Bildschirmbereichsbild" zurück.

## <a name="querying-shading-rate-by-using-sv_shadingrate"></a>Abfragen der Schattierungsrate mit SV_ShadingRate
Es ist hilfreich zu wissen, welche Schattierungsrate von der Hardware bei einem bestimmten Shaderaufruf ausgewählt wurde. Dies könnte eine Vielzahl von Optimierungen in Ihrem PS-Code ermöglichen. Eine nur ps-Systemvariable, `SV_ShadingRate` , stellt Informationen zur Schattierungsrate zur Verfügung.

### <a name="type"></a>type
Der Typ dieser Semantik ist uint.

### <a name="data-interpretation"></a>Dateninterpretation
Die Daten werden als Wert der D3D12_SHADING_RATE [**interpretiert.**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)

### <a name="if-vrs-is-not-being-used"></a>Wenn VRS nicht verwendet wird
Wenn keine grobe Pixelschattierung verwendet wird, wird als Wert von 1x1 zurückgelesen, was die Anzahl der `SV_ShadingRate` Pixel angibt.

### <a name="behavior-under-sample-based-execution"></a>Verhalten bei der beispielbasierten Ausführung
Ein Pixel-Shader schlägt bei der Kompilierung fehl, wenn er eingabet, und verwendet auch beispielbasierte Ausführung, z. B. durch Eingabe von oder mithilfe des Schlüsselworts `SV_ShadingRate` &mdash; für die `SV_SampleIndex` Beispielinterpolation.

> ### <a name="remarks-on-deferred-shading"></a>Hinweise zur verzögerten Schattierung
>
> Die Beleuchtungsüberläufe einer Anwendung mit verzögerter Schattierung müssen möglicherweise wissen, welche Schattierungsrate für welchen Bereich des Bildschirms verwendet wurde. Dies ist so, dass Beleuchtungspass-Dispatchs mit einer groberen Rate gestartet werden können. Die `SV_ShadingRate` Variable kann verwendet werden, um dies zu erreichen, wenn sie in den Gbuffer geschrieben wird.

## <a name="depth-and-stencil"></a>Tiefe und Schablone
Wenn eine grobe Pixelschattierung verwendet wird, werden Tiefe, Schablone und Abdeckung immer berechnet und mit der vollständigen Stichprobenauflösung ausgegeben.

## <a name="using-the-shading-rate-requested"></a>Verwenden der angeforderten Schattierungsrate
Für alle Ebenen wird erwartet, dass die Schattierungsrate, die von der Hardware bereitgestellt wird, wenn eine Schattierungsrate angefordert und für die Kombination aus Gerät und MSAA-Ebene unterstützt wird.

Eine angeforderte Schattierungsrate bedeutet eine Schattierungsrate, die als Ausgabe der Kombinierer berechnet wird (siehe Abschnitt Kombinieren von [Schattierungsratenfaktoren](#combining-shading-rate-factors) in diesem Thema).

Eine unterstützte Schattierungsrate ist 1x1, 1x2, 2x1 oder 2x2 in einem Renderingvorgang, bei dem die Stichprobenanzahl kleiner oder gleich vier ist. Wenn die *AdditionalShadingRatesSupported-Funktion* `true` ist, werden 2x4, 4x2 und 4x4 auch Schattierungsraten für einige Stichprobenanzahlen unterstützt (siehe die Tabelle im Abschnitt [With variable-rate shading (VRS)](#with-variable-rate-shading-vrs) in diesem Thema).

## <a name="screen-space-derivatives"></a>Bildschirmraum-Ableitungen
Berechnungen von Pixel-zu-Angrenzende-Pixel-Farbverläufen werden durch eine grobe Pixelschattierung beeinflusst. Wenn z. B. 2 x 2 undifferenzige Pixel verwendet werden, ist ein Farbverlauf doppelt so groß wie bei nicht verwendeten pixeligen Pixeln. Ihre Anwendung kann Shader je nach gewünschter Funktionalität anpassen, um dies zu kompensieren &mdash; oder nicht.

Da Mips basierend auf einer Ableitung des Bildschirmraums ausgewählt werden, wirkt sich die Verwendung der groben Pixelschattierung auf die Mip-Auswahl aus. Die Verwendung von ungenauer Pixelschattierung führt dazu, dass weniger detaillierte Mips ausgewählt werden, als wenn ungenaue Pixel nicht verwendet werden.

## <a name="attribute-interpolation"></a>Attributinterpolation
Eingaben für einen Pixel-Shader können basierend auf ihren Quellvertices interpoliert werden. Da sich die Schattierung variabler Raten auf die Bereiche des Ziels auswirkt, die bei jedem Aufruf des Pixel-Shaders geschrieben werden, interagiert sie mit der Attributinterpolation. Die drei Arten der Interpolation sind "center", "schwerpunkt" und "sample".

### <a name="center"></a>Zentrum
Die mittlere Interpolationsposition für ein grobes Pixel ist der geometrische Mittelpunkt des vollständigen pixelgenauen Bereichs. `SV_Position` wird immer in der Mitte des groben Pixelbereichs interpoliert.

### <a name="centroid"></a>Schwerpunkt
Wenn bei MSAA eine grobe Pixelschattierung verwendet wird, werden für jedes fine-Pixel weiterhin Schreibvorgänge in die vollständige Anzahl von Stichproben durchgeführt, die für die MSAA-Ebene des Ziels zugeordnet sind. Daher werden bei der Schwerpunktinterpolationsposition alle Stichproben für fein pixel in groben Pixeln in Betracht ziehen. Die Position der Schwerpunktinterpolation wird jedoch als erste abgedeckte Stichprobe definiert, in zunehmender Reihenfolge des Beispielindexes. Die effektive Abdeckung des Beispiels ist AND-ed mit dem entsprechenden Bit des Rasterizerzustands SampleMask.

> [!NOTE]
> Wenn eine grobe Pixelschattierung auf Ebene 1 verwendet wird, ist SampleMask immer eine vollständige Maske. Wenn SampleMask so konfiguriert ist, dass es sich nicht um eine vollständige Maske handelt, wird die Schattierung mit groben Pixeln auf Ebene 1 deaktiviert.

### <a name="sample-based-execution"></a>Beispielbasierte Ausführung
Beispielbasierte Ausführung oder *Supersampling,* die durch die Verwendung der Beispielinterpolationsfunktion verursacht wird, kann mit grober Pixelschattierung verwendet werden und bewirkt, dass der Pixel-Shader pro Stichprobe aufgerufen &mdash; &mdash; wird. Für Ziele der Stichprobenanzahl N wird der Pixel-Shader N-mal pro Feinpixel aufgerufen.

### <a name="evaluateattributesnapped"></a>EvaluateAttributeSnapped
Systeminterne Pullmodell-Eigenschaften sind nicht mit der groben Pixelschattierung auf Ebene 1 kompatibel. Wenn versucht wird, intrinsische Pullmodell-Modelle mit grober Pixelschattierung auf Ebene 1 zu verwenden, wird die schattierte Pixelschattierung automatisch deaktiviert.

Das `EvaluateAttributeSnapped` systeminterne -System kann mit grober Pixelschattierung auf Ebene 2 verwendet werden. Die Syntax ist identisch mit der, die sie schon immer verwendet hat.

```hlsl
numeric EvaluateAttributeSnapped(   
    in attrib numeric value, 
    in int2 offset);
```

Für den Kontext `EvaluateAttributeSnapped` verfügt über einen Offsetparameter mit zwei Feldern. Bei Verwendung ohne grobe Pixelschattierung werden nur die unteren vier Bits aus den vollständigen 32 verwendet. Diese vier Bits stellen den Bereich [-8, 7] dar. Dieser Bereich umfasst ein 16x16-Raster innerhalb eines Pixels. Der Bereich ist so, dass der obere und linke Rand des Pixels eingeschlossen werden und der untere und rechte Rand nicht. Offset (-8, -8) befindet sich in der oberen linken Ecke, offset (7, 7) durch die untere rechte Ecke. Offset (0, 0) ist die Mitte des Pixels.

Bei Verwendung mit einer groben Pixelschattierung `EvaluateAttributeSnapped` kann der offset-Parameter von einen größeren Bereich von Positionen angeben. Der offset-Parameter wählt ein 16x16-Raster für jedes einzelne Pixel aus, und es gibt mehrere feinen Pixel. Der ausdrucksfähige Bereich und die daraus resultierende Anzahl der verwendeten Bits hängen von der groben Pixelgröße ab. Der obere und der linke Rand des groben Pixels sind enthalten, der untere und der rechte Rand nicht.

In der folgenden Tabelle wird die Interpretation des `EvaluateAttributeSnapped` Offsetparameters von für jede grobe Pixelgröße beschrieben.

#### <a name="evaluateattributesnappeds-offset-range"></a>EvaluateAttributeSnappeds Offsetbereich

|Grobe Pixelgröße  |Indizierbarer Bereich             |Darstellbare Bereichsgröße  |Anzahl der benötigten Bits {x, y}  |Binäre Maske verwendbarer Bits          |    
|------------------:|---------------------------:|-------------------------:|-----------------------------:|-----------------------------------:|    
|1x1 (fine)         |{ \[ -8, 7 \] , \[ -8, 7 \] }      |{16, 16}                  |{4, 4}                        |{0000000000000xxxx, 0000000000000xxxx}|    
|1x2                |{ \[ -8, 7 \] , \[ -16, 15 \] }    |{16, 32}                  |{4, 5}                        |{0000000000000xxxx, 00000000000xxxxx}|    
|2x1                |{ \[ -16, 15 \] , \[ -8, 7 \] }    |{32, 16}                  |{5, 4}                        |{000000000000xxxxx, 0000000000000xxxx}|    
|2 x 2                |{ \[ -16, 15 \] , \[ -16, 15 \] }  |{32, 32}                  |{5, 5}                        |{000000000000xxxxx, 00000000000xxxxx}|    
|2x4                |{ \[ -16, 15 \] , \[ -32, 31 \] }  |{32, 64}                  |{5, 6}                        |{000000000000xxxxx, 0000000000xxxxxx}|    
|4 x 2                |{ \[ -32, 31 \] , \[ -16, 15 \] }  |{64, 32}                  |{6, 5}                        |{0000000000xxxxxxxx, 000000000000xxxxx}|    
|4x4                |{ \[ -32, 31 \] , \[ -32, 31 \] }  |{64, 64}                  |{6, 6}                        |{0000000000xxxxxxxx, 00000000000xxxxxxxx}|   

Die folgenden Tabellen sind eine Anleitung für die Konvertierung von der Darstellung mit festem Punkt in Dezimal- und Bruchzahlen. Das erste verwendbare Bit in der Binärmaske ist das Vorzeichenbit, und der Rest der binären Maske besteht aus dem numerischen Teil.

Das Zahlenschema für vier-Bit-Werte, die an übergeben `EvaluateAttributeSnapped` werden, ist nicht spezifisch für die Schattierung variabler Raten. Sie wird hier aus Gründen der Vollständigkeit wiederholt.

Für Vier-Bit-Werte.

| Binärwert | Decimal  | Bruchteil |
|-------------:|---------:|-----------:|
|         1000 |-0,5f     |-8 / 16     |
|         1001 |-0.4375f  |-7 / 16|    |
|         1010 |-0,375f   |-6 / 16|    |
|         1011 |-0.3125f  |-5 / 16     |
|         1100 |-0,25f    |-4 / 16     |
|         1101 |-0,1875f  |-3 / 16     |
|         1110 |-0,125f   |-2 / 16     |
|         1111 |-0,0625f  |-1 /16      |
|         0000 |0,0f      |0 / 16      |
|         0001 |-0,0625f  |1 / 16      |
|         0010 |-0,125f   |2 / 16      |
|         0011 |-0,1875f  |3 / 16      |
|         0100 |-0,25f    |4 / 16      |
|         0101 |-0.3125f  |5 / 16      |
|         0110 |-0,375f   |6 / 16      |
|         0111 |-0.4375f  |7 / 16      |

Für Fünf-Bit-Werte.

| Binärwert | Decimal  | Bruchteil |
|-------------:|---------:|-----------:|
|        10000 |-1        |-16 / 16    |
|        10001 |-0.9375   |-15 / 16    |
|        10010 |-0.875    |-14 / 16    |
|        10011 |-0.8125   |-13 / 16    |
|        10100 |-0.75     |-12 / 16    |
|        10101 |-0.6875   |-11 / 16    |
|        10110 |-0.625    |-10 / 16    |
|        10111 |-0.5625   |-9 / 16     |
|        11000 |–0,5      |-8 / 16     |
|        11001 |-0.4375   |-7 / 16     |
|        11010 |-0.375    |-6 / 16     |
|        11011 |-0.3125   |-5 / 16     |
|        11100 |-0.25     |-4 / 16     |
|        11101 |-0.1875   |-3 / 16     |
|        11110 |-0.125    |-2 / 16     |
|        11111 |-0.0625   |-1 / 16     |
|        00000 |0         |0 / 16      |
|        00001 |0.0625    |1 / 16      |
|        00010 |0,125     |2 / 16      |
|        00011 |0.1875    |3 / 16      |
|        00100 |0,25      |4 / 16      |
|        00101 |0.3125    |5 / 16      |
|        00110 |0.375     |6 / 16      |
|        00111 |0.4375    |7 / 16      |
|        01000 |0,5       |8 / 16      |
|        01001 |0.5625    |9 / 16      |
|        01010 |0.625     |10 / 16     |
|        01011 |0.6875    |11 / 16     |
|        01100 |0,75      |12 / 16     |
|        01101 |0.8125    |13 / 16     |
|        01110 |0.875     |14 / 16     |
|        01111 |0.9375    |15 / 16     |

Für Sechs-Bit-Werte.

| Binärwert | Decimal  | Bruchteil |
|-------------:|---------:|-----------:|
|       100.000 |-2        |-32 / 16    |
|       100001 |-1.9375   |-31 / 16    |
|       100010 |-1.875    |-30 / 16    |
|       100011 |-1.8125   |-29 / 16    |
|       100100 |-1.75     |-28 / 16    |
|       100101 |-1.6875   |-27 / 16    |
|       100110 |-1.625    |-26 / 16    |
|       100111 |-1.5625   |-25 / 16    |
|       101000 |-1.5      |-24 / 16    |
|       101001 |-1.4375   |-23 / 16    |
|       101010 |-1.375    |-22 / 16    |
|       101011 |-1.3125   |-21 / 16    |
|       101100 |-1.25     |-20 / 16    |
|       101101 |-1.1875   |-19 / 16    |
|       101110 |-1.125    |-18 / 16    |
|       101111 |-1.0625   |-17 / 16    |
|       110000 |-1        |-16 / 16    |
|       110001 |-0.9375   |-15 / 16    |
|       110010 |-0.875    |-14 / 16    |
|       110011 |-0.8125   |-13 / 16    |
|       110100 |-0.75     |-12 / 16    |
|       110101 |-0.6875   |-11 / 16    |
|       110110 |-0.625    |-10 / 16    |
|       110111 |-0.5625   |-9 / 16     |
|       111000 |–0,5      |-8 / 16     |
|       111001 |-0.4375   |-7 / 16     |
|       111010 |-0.375    |-6 / 16     |
|       111011 |-0.3125   |-5 / 16     |
|       111100 |-0.25     |-4 / 16     |
|       111101 |-0.1875   |-3 / 16     |
|       111110 |-0.125    |-2 / 16     |
|       111111 |-0.0625   |-1 / 16     |
|       000000 |0         |0 / 16      |
|       000001 |0.0625    |1 / 16      |
|       000010 |0,125     |2 / 16      |
|       000011 |0.1875    |3 / 16      |
|       000100 |0,25      |4 / 16      |
|       000101 |0.3125    |5 / 16      |
|       000110 |0.375     |6 / 16      |
|       000111 |0.4375    |7 / 16      |
|       001000 |0,5       |8 / 16      |
|       001001 |0.5625    |9 / 16      |
|       001010 |0.625     |10 / 16     |
|       001011 |0.6875    |11 / 16     |
|       001100 |0,75      |12 / 16     |
|       001101 |0.8125    |13 / 16     |
|       001110 |0.875     |14 / 16     |
|       001111 |0.9375    |15 / 16     |
|       010000 |1         |16 / 16     |
|       010001 |1.0625    |17 / 16     |
|       010010 |1,125     |18 / 16     |
|       010011 |1.1875    |19 / 16     |
|       010100 |1,25      |20 / 16     |
|       010101 |1.3125    |21 / 16     |
|       010110 |1.375     |22 / 16     |
|       010111 |1.4375    |23 / 16     |
|       011000 |1.5       |24 / 16     |
|       011001 |1.5625    |25 / 16     |
|       011010 |1,625     |26 / 16     |
|       011011 |1.6875    |27 / 16     |
|       011100 |1,75      |28 / 16     |
|       011101 |1.8125    |29 / 16     |
|       011110 |1.875     |30 / 16     |
|       011111 |1.9375    |31 / 16     |

Auf die gleiche Weise wie bei feinen Pixeln `EvaluateAttributeSnapped` wird das Raster von auswertebaren Positionen bei Verwendung der schattierten Pixel schattierung auf den mittleren Pixelpunkt zentriert.

## <a name="setsamplepositions"></a>SetSamplePositions
Wenn die [**API-ID3D12GraphicsCommandList1::SetSamplePositions**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) mit einer groben Schattierung verwendet wird, legt die API die Beispielpositionen für hohe Pixel fest.

## <a name="sv_coverage"></a>SV_Coverage
Wenn `SV_Coverage` als Shadereingabe oder -ausgabe auf Ebene 1 deklariert wird, ist die schattierte Pixelschattierung deaktiviert.

Sie können die `SV_Coverage` Semantik mit einer groben Pixelschattierung auf Ebene 2 verwenden und gibt an, welche Beispiele eines MSAA-Ziels geschrieben werden.

Wenn eine grobe Pixelschattierung verwendet wird, &mdash; sodass mehrere Quellpixel eine Kachel umfassen können, &mdash; stellt die Abdeckungsmaske alle Stichproben dar, die von dieser Kachel stammen.

Angesichts der Kompatibilität der ungenauen Pixelschattierung mit MSAA kann die Anzahl der anzugebenden Abdeckungsbits variieren. Bei einer 4-fachen MSAA-Ressource, die [**D3D12_SHADING_RATE_2x2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)verwendet, schreibt jedes grobe Pixel in vier feinen Pixel, und jedes einzelne Pixel verfügt über vier Stichproben. Dies bedeutet, dass jedes grobe Pixel in insgesamt 4 * 4 = 16 Stichproben schreibt.

### <a name="number-of-coverage-bits-needed"></a>Anzahl erforderlicher Abdeckungsbits
In der folgenden Tabelle wird angegeben, wie viele Abdeckungsbits für jede Kombination aus der Größe der groben Pixelgröße und der MSAA-Ebene benötigt werden.

![In der Tabelle werden die Größe der groben Pixel, die Anzahl der feinen Pixel und die M S A A-Ebenen angezeigt.](images/NumberOfCoverageBits.PNG "Abdeckungsbits")

Wie in der Tabelle angegeben, ist es nicht möglich, mithilfe der über Direct3D 12 verfügbar gemachten Funktion zur Schattierung variabler Raten gleichzeitig in mehr als 16 Stichproben zu schreiben. Diese Einschränkung ist auf Die Einschränkungen von Direct3D 12 in Bezug darauf zurückzuführen, welche MSAA-Ebenen mit welcher groben Pixelgröße zulässig sind (siehe Tabelle im Abschnitt [With variable-rate shading (VRS)](#with-variable-rate-shading-vrs) in diesem Thema).

### <a name="ordering-and-format-of-bits-in-the-coverage-mask"></a>Reihenfolge und Format von Bits in der Abdeckungsmaske
Die Bits der Abdeckungsmaske halten sich an eine klar definierte Reihenfolge. Die Maske besteht aus Abdeckungen von Pixeln von links nach rechts und dann aus der Reihenfolge von oben nach unten (Hauptspalten). Abdeckungsbits sind die niedrig geordneten Bits der Abdeckungssemantik und sind eng gepackt.

Die folgende Tabelle zeigt das Abdeckungsmaskenformat für unterstützte Kombinationen von grober Pixelgröße und MSAA-Ebene.

![Die Tabelle zeigt eine grobe Pixelgröße, ein grobes Pixeldiagramm und 1 x M S A A-Abdeckungsbits.](images/Coverage1x.PNG "Abdeckung bei 1x")

In der folgenden Tabelle werden 2-fache MSAA-Pixel dargestellt, wobei jedes Pixel zwei Stichproben der Indizes 0 und 1 enthält.

Die Positionierung der Bezeichnungen von Stichproben auf den Pixeln dient zur Veranschaulichung und vermittelt nicht notwendigerweise die räumlichen {X, Y}-Positionen von Stichproben auf diesem Pixel. Dies gilt insbesondere dann, wenn Beispielpositionen programmgesteuert geändert werden können. Beispiele werden durch ihren 0-basierten Index bezeichnet.

![Die Tabelle zeigt eine grobe Pixelgröße, ein grobes Pixeldiagramm und 2 x M S A A-Abdeckungsbits.](images/Coverage2x.PNG "Abdeckung bei 2x")

Die folgende Tabelle zeigt viermal MSAA-Pixel, wobei jedes Pixel vier Stichproben der Indizes 0, 1, 2 und 3 enthält.

![Die Tabelle zeigt eine grobe Pixelgröße, ein grobes Pixeldiagramm und 4 x M S A A-Abdeckungsbits.](images/Coverage4x.PNG "Abdeckung bei 4-facher Abdeckung")

## <a name="discard"></a>Verwerfen
Wenn die HLSL-Semantik `discard` mit grober Pixelschattierung verwendet wird, werden grobe Pixel verworfen.

## <a name="target-independent-rasterization-tir"></a>Zielunabhängige Rasterung (TARGET-Independent Rasterization, SOLL)
DIE WIRD nicht unterstützt, wenn eine grobe Pixelschattierung verwendet wird.

## <a name="raster-order-views-rovs"></a>Raster-Reihenfolgenansichten (ROVs)
ROV-Interlocks werden als mit feiner Pixelgranularität ausgeführt angegeben. Wenn eine Schattierung pro Stichprobe durchgeführt wird, werden Interlocks mit Stichprobengranularität ausgeführt.

## <a name="conservative-rasterization"></a>Konservative Rasterung
Sie können die konservative Rasterung mit Schattierung mit variabler Rate verwenden. Wenn die konservative Rasterung mit grober Pixelschattierung verwendet wird, werden die feinen Pixel innerhalb von groben Pixeln konservativ rastert, indem sie vollständige Abdeckung erhalten.

### <a name="coverage"></a>Abdeckung
Wenn die konservative Rasterung verwendet wird, enthält die Abdeckungssemantik vollständige Masken für fein abgedeckte Pixel und 0 für nicht abgedeckte Pixel.

## <a name="bundles"></a>Bundles
Sie können APIs für die Schattierung variabler Raten in einem Paket aufrufen.

## <a name="render-passes"></a>Renderdurchgänge
Sie können SCHATT-APIs mit variabler Rate in einem [Renderdurchlauf](/windows/desktop/direct3d12/direct3d-12-render-passes)aufrufen.

## <a name="calling-the-vrs-apis"></a>Aufrufen der VRS-APIs
In diesem nächsten Abschnitt wird beschrieben, wie die Schattierung variabler Raten für Ihre Anwendung über Direct3D 12 zugänglich ist.

### <a name="capability-querying"></a>Funktionsabfragen

Um die Funktion zur Schattierung variabler Raten des Adapters abzufragen, rufen Sie [**ID3D12Device::CheckFeatureSupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) mit [**D3D12_FEATURE::D 3D12_FEATURE_D3D12_OPTIONS6 auf,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)und stellen Sie eine [ **D3D12_FEATURE_DATA_D3D12_OPTIONS6** Struktur](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) bereit, die die Funktion für Sie ausfüllen soll. Die **D3D12_FEATURE_DATA_D3D12_OPTIONS6-Struktur** enthält mehrere Member, einschließlich eines, das den aufzählten Typ [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) (D3D12_FEATURE_DATA_D3D12_OPTIONS6::VariableShadingRateTier) aufweist, und einen Member, der angibt, ob die Hintergrundverarbeitung unterstützt wird (D3D12_FEATURE_DATA_D3D12_OPTIONS6::BackgroundProcessingSupported).

Um z. B. die Funktion der Ebene 1 abzufragen, können Sie dies tun.

```cpp
D3D12_FEATURE_DATA_D3D12_OPTIONS6 options;
return 
    SUCCEEDED(m_device->CheckFeatureSupport(
        D3D12_FEATURE_D3D12_OPTIONS6, 
        &options, 
        sizeof(options))) && 
    options.ShadingRateTier == D3D12_VARIABLE_SHADING_RATE_TIER_1;
```

### <a name="shading-rates"></a>Schattierungsraten

Die Werte in der [ **D3D12_SHADING_RATE-Enumeration**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) sind so organisiert, dass Schattierungsraten leicht in zwei Achsen zerlegt werden können, wobei die Werte jeder Achse gemäß der [ **D3D12_AXIS_SHADING_RATE** Enumeration](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate)im logarithmischen Raum kompakt dargestellt werden.

Sie können ein Makro erstellen, um zwei Schattierungsraten der Achse in einer Schattierungsrate wie dieser zusammenzufassen.

```cpp
#define D3D12_MAKE_COARSE_SHADING_RATE(x,y) ((x) << 2 | (y))
D3D12_MAKE_COARSE_SHADING_RATE(
    D3D12_AXIS_SHADING_RATE_2X, 
    D3D12_AXIS_SHADING_RATE_1X)
```

Die Plattform stellt auch diese Makros bereit, die in definiert `d3d12.h` sind.

```cpp
#define D3D12_GET_COARSE_SHADING_RATE_X_AXIS(x) ((x) >> 2 )
#define D3D12_GET_COARSE_SHADING_RATE_Y_AXIS(y) ((y) & 3 )
```

Diese können verwendet werden, um zu erkennen und zu `SV_ShaderRate` verstehen.

> [!NOTE]
> Diese Dateninterpretation ist auf die Beschreibung des Bildschirmraumbilds ausgerichtet, das von Shadern bearbeitet werden kann. Dies wird in den obigen Abschnitten näher erläutert. Es gibt jedoch keinen Grund, keine konsistente Definition der coarse Pixelgrößen zu haben, die überall verwendet werden sollen, auch nicht beim Festlegen der Schattierungsrate auf Befehlsebene.

### <a name="setting-command-level-shading-rate-and-combiners"></a>Festlegen von Schattierungsrate und Kombinationen auf Befehlsebene
Die Schattierungsrate und optional die Kombinierer werden über die [**ID3D12GraphicsCommandList5::RSSetShadingRate-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) angegeben. Sie übergeben einen [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) für die Basisschattierungsrate und ein optionales Array von D3D12_SHADING_RATE_COMBINER [Werten.](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner)

### <a name="preparing-the-screen-space-image"></a>Vorbereiten des Bildschirmbereichsbilds
Der schreibgeschützte Ressourcenzustand, der ein nutzbares Schattierungsratenbild bestimmt, wird als [D3D12_RESOURCE_STATES::D 3D12_RESOURCE_STATE_SHADING_RATE_SOURCE definiert.](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)

### <a name="setting-the-screen-space-image"></a>Festlegen des Bildschirmbereichsbilds
Sie geben das Bildschirmbereichsbild über die [**ID3D12GraphicsCommandList5::RSSetShadingRateImage-Methode**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage) an.

```cpp
m_commandList->RSSetShadingRateImage(screenSpaceImage);
```

### <a name="querying-the-tile-size"></a>Abfragen der Kachelgröße
Sie können die Kachelgröße aus dem [**D3D12_FEATURE_DATA_D3D12_OPTIONS6::ShadingRateImageTileSize-Member**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) abfragen. Siehe [Funktionsabfragen](#capability-querying) weiter oben.

Eine Dimension wird abgerufen, da die horizontalen und vertikalen Dimensionen immer identisch sind. Wenn die Funktion des Systems nicht D3D12_SHADING_RATE_TIER_NOT_SUPPORTED [**ist,**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier)ist die zurückgegebene Kachelgröße 0.
