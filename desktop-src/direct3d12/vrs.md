---
title: Schattierung variabler Rate (VRS)
description: Das Schattieren von Variablenraten &mdash; oder grobe Pixel Schattierung &mdash; ist ein Mechanismus, mit dem Sie Renderingleistung/-Leistung zu raten zuweisen können, die in Ihrem gerenderten Bild variieren.
ms.localizationpriority: high
ms.topic: article
ms.date: 04/08/2019
ms.openlocfilehash: be2367ceb72d2e693d86b6f279b627f3bffa9e1c
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104548759"
---
# <a name="variable-rate-shading-vrs"></a>Schattierung variabler Rate (VRS)

## <a name="the-motivation-for-vrs"></a>Die Motivation für VRS
Aufgrund von Leistungseinschränkungen kann ein grafikrenderer sich nicht immer für jeden Teil des Ausgabe Bilds den gleichen Grad an Qualität leisten. Das Schattieren von Variablenraten &mdash; oder grobe Pixel Schattierung &mdash; ist ein Mechanismus, mit dem Sie Renderingleistung/-Leistung zu raten zuweisen können, die in Ihrem gerenderten Bild variieren.

In einigen Fällen kann die Schattierungs Rate mit geringfügigen oder ohne Reduzierung der wahrnehmbaren Ausgabequalität reduziert werden. Dies führt zu einer Leistungsverbesserung, die im wesentlichen kostenlos ist.

## <a name="without-vrsmdashmulti-sample-anti-aliasing-with-supersampling"></a>Ohne VRS &mdash; -Antialiasing mit mehreren Beispielen mit Supersampling
Ohne Schattierung variabler Geschwindigkeit ist die einzige Möglichkeit, die Schattierungs Rate zu steuern, mit Multi-Sample Anti-Aliasing (MSAA) mit Beispiel basierter Ausführung (auch als Supersampling bezeichnet).

MSAA ist ein Mechanismus zum Verringern der geometrischen Aliasing und zum Verbessern der renderingqualität eines Bilds im Vergleich zur Verwendung von MSAA. Die MSAA-Stichproben Anzahl, die 1X, 2X, 4x, 8x oder 16X sein kann, steuert die Anzahl der pro renderzielpixel zugeordneten Stichproben. Die MSAA-Stichproben Anzahl muss im Voraus bekannt sein, wenn das Ziel zugeordnet wird, und kann anschließend nicht mehr geändert werden.

Die Supersampling bewirkt, dass der Pixelshader einmal pro Stichprobe mit höherer Qualität aufgerufen wird, aber auch höhere Leistungskosten im Vergleich zur pro-Pixel-Ausführung.

Ihre Anwendung kann Ihre Schattierungs Rate steuern, indem Sie zwischen pro Pixel basierender Ausführung oder MSAA-with-Supersampling wählen. Diese beiden Optionen bieten keine sehr feine Kontrolle. Außerdem möchten Sie möglicherweise eine niedrigere Schattierungs Rate für eine bestimmte Objektklasse im Vergleich zum Rest des Bilds. Zu diesen Objekten kann ein Objekt hinter einem HUD-Element, eine Transparenz, ein weich Zeichen (Tiefe von Feld, Bewegung usw.) oder eine optische Verzerrung aufgrund von VR-Optiken gehören. Dies wäre jedoch nicht möglich, da die Schattierungs Qualität und die Kosten für das gesamte Image korrigiert werden.

## <a name="with-variable-rate-shading-vrs"></a>Mit Variablen Raten Schattierung (VRS)
Das VRS-Modell (Variable Rate Schattierung) erweitert Supersampling-with-MSAA durch das Konzept der groben Schattierung in das Gegenteil, "grobe Pixel", Richtung. An dieser Stelle kann Schattierung mit einer Häufigkeit von mehr als einem Pixel ausgeführt werden. Anders ausgedrückt: eine Gruppe von Pixeln kann als einzelne Einheit schattiert werden, und das Ergebnis wird dann an alle Beispiele in der Gruppe übertragen.

Eine grobe Schattierungs-API ermöglicht der Anwendung die Angabe der Anzahl von Pixeln, die zu einer schattierten Gruppe oder einem *groben Pixel* gehören. Nachdem Sie das Renderziel zugeordnet haben, können Sie die Größe des groben Pixels verändern. Daher können unterschiedliche Bildschirm Teile oder unterschiedliche Zeichnungs Pässe unterschiedliche Schattierungs Raten aufweisen.

Im folgenden finden Sie eine Tabelle, in der beschrieben wird, welche MSAA-Ebene mit welcher Pixelgröße unterstützt wird Einige werden auf keiner Plattform unterstützt. während andere bedingt basierend auf einer Funktion (*additionalshadingratessupported*), die durch "Cap" angegeben wird, bedingt aktiviert werden.

![coarseepixelsizesupport](images/CoarsePixelSizeSupport.PNG "Grobe Pixelgrößen")

Für die im nächsten Abschnitt erläuterten Funktionsebenen gibt es keine Kombination aus "grob Pixel-Größe und Stichproben Anzahl", bei der Hardware mehr als 16 Stichproben pro Pixel-Shader-Aufruf nachverfolgen muss. Diese Kombinationen sind in der obigen Tabelle durch Halbton schattiert.

## <a name="feature-tiers"></a>Funktionsebenen
Es gibt zwei Ebenen der VRS-Implementierung und zwei Funktionen, die Sie Abfragen können. Jede Ebene wird nach der Tabelle ausführlicher beschrieben.

![wirft](images/Tiers.PNG "VRS-Ebenen")

### <a name="tier-1"></a>Ebene 1
- Die Schattierungs Rate kann nur pro zeichnen angegeben werden. nicht präziser als das.
- Die Schattierungs Rate gilt einheitlich für das, was unabhängig davon gezeichnet wird, wo Sie sich innerhalb des Renderziels befindet.

### <a name="tier-2"></a>Ebene 2
- Die Schattierungs Rate kann pro zeichnen angegeben werden, wie in Ebene 1. Sie kann auch durch eine Kombination aus pro-zeichnen-Basis und von:
  - Semantik aus jedem provozierenden Scheitelpunkt und
  - ein Bild Raum Bild.
- Die Schattierungs Raten aus den drei Quellen werden mithilfe eines Satzes von Combiner kombiniert.
- Die Bild Kachel Größe des Bildschirm Raums ist 16x16 oder kleiner.
- Die von Ihrer Anwendung angeforderte Schattierungs Rate ist garantiert genau (aus Gründen der Genauigkeit Temporaler und anderer erbaufilter).
- SV_ShadingRate PS-Eingabe wird unterstützt.
- Die Schattierungs Rate "pro-provoziert-Vertex" (auch als "pro primitiv" bezeichnet) ist gültig, wenn ein Viewport verwendet wird und `SV_ViewportArrayIndex` nicht in den Wert geschrieben wird.
- Wenn die *supportspervertexshadingratewithmultipleviewports* -Funktion auf festgelegt ist, kann die pro-anregende-Vertex-Rate mit mehr als einem Viewport verwendet werden `true` . Außerdem kann diese Rate in diesem Fall verwendet werden, wenn `SV_ViewportArrayIndex` in geschrieben wird.

### <a name="list-of-capabilities"></a>Liste der Funktionen
- *Additionalshadingratessupported*
  - Boolescher Typ.
  - Gibt an, ob 2x4, 4x2 und 4 x 4 grobe Pixelgrößen für das Rendering mit einem Sampling unterstützt werden. und ob eine grobe Pixelgröße von 2x4 für 2X-MSAA unterstützt wird.
- *Supportspervertexshadingratewithmultipleviewports*
  - Boolescher Typ.
  - Gibt an, ob mehr als ein Viewport mit der Schattierungs Rate pro Scheitelpunkt (auch als pro primitiv bezeichnet) verwendet werden kann.

## <a name="specifying-shading-rate"></a>Angeben der Schattierungs Rate
Aus Gründen der Flexibilität in Anwendungen gibt es eine Reihe von Mechanismen zur Steuerung der Schattierungs Rate. Abhängig von der Hardware Funktionsebene sind unterschiedliche Mechanismen verfügbar.

### <a name="command-list"></a>Befehlsliste
Dies ist der einfachste Mechanismus zum Festlegen der Schattierungs Rate. Es ist auf allen Ebenen verfügbar.

Die Anwendung kann mit der [ **ID3D12GraphicsCommandList5:: rssetshadingrate** -Methode](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate)eine grobe Pixelgröße angeben. Diese API nimmt ein einzelnes Aufzählungs Argument an. Die API bietet eine allgemeine Kontrolle über den Grad an Qualität für das Rendern der &mdash; Möglichkeit, die Schattierungs Rate pro zeichnen festzulegen.

Werte für diesen Zustand werden durch die [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) -Enumeration ausgedrückt.

#### <a name="coarse-pixel-size-support"></a>Unterstützung für grobe Pixelgrößen
Die Schattierungs Raten 1x1, 1X2, 2 x 2 und 2 x 2 werden auf allen Ebenen unterstützt.

Es gibt eine Funktion, *additionalshadingratessupported*, um anzugeben, ob 2x4, 4x2 und 4X4 auf dem Gerät unterstützt werden.

### <a name="screen-space-image-image-based"></a>Bild Raum Bild (Bild basiert)
Auf Ebene 2 und höher können Sie die Pixel Schattierungs Rate mit einem Bild Raum Bild angeben.

Das Bild für den Bildschirm ermöglicht der Anwendung, eine "Detailebene (LOD)" zu erstellen, die Bereiche mit unterschiedlicher Qualität anzeigt, z. b. Bereiche, die von Bewegungsunschärfe, Tiefe, transparente Objekte oder HUD-Benutzeroberflächen Elemente abgedeckt werden. Die Auflösung des Bilds erfolgt in Macroblocks. Sie befindet sich nicht in der Auflösung des Renderziels. Mit anderen Worten, die Daten der Schattierungs Rate werden bei einer Granularität von 8 x 8-oder 16x16-Pixel Kacheln angegeben, wie durch die VRS-Kachel Größe angegeben.

#### <a name="tile-size"></a>Tile size (Kachelgröße)
Ihre Anwendung kann eine API Abfragen, um die unterstützte VRS-Kachel Größe für Ihr Gerät abzurufen.

Kacheln sind quadratisch, und die Größe bezieht sich auf die Breite oder Höhe der Kachel in texeln.

Wenn die Hardware die Schattierung der Variablen der Ebene 2 nicht unterstützt, gibt die Funktions Abfrage für die Kachel Größe 0 zurück.

Wenn die Hardware die Schattierung der Variablen der Ebene 2 unterstützt *, entspricht die* Kachel Größe einem dieser Werte.

- 8
- 16
- 32

#### <a name="screen-space-image-size"></a>Bildspeicher Größe des Bildschirms
Für ein Renderziel der Größe {rtwidth, rtheight} unter Verwendung einer angegebenen Kachel Größe namens **vrstilesize** ist das Bild Raum Bild, das es abdeckt, diese Dimensionen.

```cpp
{ ceil((float)rtWidth / VRSTileSize), ceil((float)rtHeight / VRSTileSize) }
```

Die obere linke Seite des Bildschirms Bilds (0,0) ist an der oberen linken Seite des Renderziels (0,0) gesperrt.

Um die (x, y)-Koordinate einer Kachel zu suchen, die einer bestimmten Position im Renderziel entspricht, unterteilen Sie die fensterraum Koordinaten von (x, y) durch die Kachel Größe, wobei Bruchteile ignoriert werden.

Wenn das Bildschirmraum Bild größer als das angegebene Renderziel sein muss, werden die zusätzlichen Teile rechts und/oder unten nicht verwendet.

Wenn das Bildschirmraum Bild für ein bestimmtes Renderziel zu klein ist, ergibt jeder versuchte Lesevorgang aus dem Image über die tatsächlichen Blöcke hinaus eine Standard Schattierungs Rate von 1x1. Dies liegt daran, dass die obere linke Seite (0,0) des Bildschirm Leerraums für das Renderziel in der oberen linken Ecke (0,0) gesperrt ist, und das Lesen über die Blöcke des Renderziels hinaus bedeutet, dass die Werte für x und y zu groß sind.

#### <a name="format-layout-resource-properties"></a>Format, Layout, Ressourcen Eigenschaften
Das Format dieser Oberfläche ist eine 8-Bit-Oberfläche mit einem einzigen Kanal ([**DXGI_FORMAT_R8_UINT**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)).

Die Ressource ist "Dimension **TEXTURE2D**".

Sie kann nicht in ein-oder falsch eingegeben werden. Sie muss explizit über eine MIP-Ebene verfügen.

Sie enthält die Stichproben Anzahl 1 und die Stichproben Qualität 0.

Das Textur Layout ist **unbekannt**. Es kann implizit kein Zeilen Hauptlayout sein, da Cross-Adapter nicht zulässig ist.

Die erwartete Art und Weise, in der die Bildspeicher Daten aufgefüllt werden, ist entweder
1. Schreiben der Daten mit einem Compute-Shader Das Bildschirmraum Bild ist als UAV gebunden, oder
2. Kopieren Sie die Daten auf das Bildschirm Bild.

Wenn Sie das Bild für den Bildschirm erstellen, sind diese Flags zulässig.

- NONE
- ALLOW_UNORDERED_ACCESS
- DENY_SHADER_RESOURCE

Diese Flags sind nicht zulässig.

- ALLOW_RENDER_TARGET
- ALLOW_DEPTH_STENCIL
- ALLOW_CROSS_ADAPTER
- ALLOW_SIMULTANEOUS_ACCESS
- VIDEO_DECODE_REFERENCE_ONLY

Der heaptyp der Ressource kann nicht hoch-oder eingelesen werden.

Die Ressource kann nicht SIMULTANEOUS_ACCESS werden. Die Ressource darf nicht Adapter übergreifend sein.

#### <a name="data"></a>Daten
Jedes Byte des Bildschirmraum Bilds entspricht einem Wert der [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)  -Enumeration.

#### <a name="resource-state"></a>Ressourcenzustand
Eine Ressource muss in einen schreibgeschützten Status versetzt werden, wenn Sie als Bildspeicher Image verwendet wird. Zu diesem Zweck wird ein Schreib geschützter Zustand, [**D3D12_RESOURCE_STATE_SHADING_RATE_SOURCE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states), definiert.

Die Bildressource ist aus diesem Zustand übergegangen, sodass Sie wiederbeschreibbar ist.

#### <a name="setting-the-image"></a>Festlegen des Bilds
Das Bild Raum Bild zum Angeben der Shader-Rate wird in der Befehlsliste festgelegt.

Eine Ressource, die als Quelle für Schattierungs Raten festgelegt wurde, kann nicht aus einer Shader-Stufe gelesen oder geschrieben werden.

`null`Zum Angeben der shaderrate kann ein Bildschirmraum Bild festgelegt werden. Dies hat den Effekt, dass 1x1 konsistent als Beitrag aus dem Bildschirmraum Bild verwendet wird. Das Bild für den Bildschirmraum kann anfänglich als festgelegt betrachtet werden `null` .

#### <a name="promotion-and-decay"></a>Herauf Stufung und Verfall
Eine Bild-und Bildspeicher Ressource hat keine besonderen Auswirkungen in Bezug auf die herauf Stufung oder den Verfall.

### <a name="per-primitive-attribute"></a>Pro primitiver Attribut
Ein pro Primitives Attribut bietet die Möglichkeit, einen Schattierungs Raten Begriff als Attribut aus einem provogenden Scheitelpunkt anzugeben. Dieses Attribut ist flach schattiert &mdash; , d. h., es wird an alle Pixel im aktuellen Dreieck oder Zeilen primitiven weitergegeben. Die Verwendung eines pro primitiver Attributs kann im Vergleich zu den anderen Schattierungs Raten bezeichlern eine präzisere Steuerung der Bildqualität ermöglichen.

Das pro primitive Attribut ist eine festleg Bare Semantik namens `SV_ShadingRate` . `SV_ShadingRate` ist als Teil des [HLSL-Shader-Modells 6,4](/windows/desktop/direct3dhlsl/hlsl-shader-model-6-4-features-for-direct3d-12)vorhanden.

Wenn vs oder GS festgelegt `SV_ShadingRate` sind, aber VRS nicht aktiviert ist, hat die Semantik Einstellung keine Auswirkungen. Wenn kein Wert für `SV_ShadingRate` pro primitiver Angabe angegeben ist, wird ein Schattierungs Raten Wert von 1x1 als pro primitiver Beitrag angenommen.

### <a name="combining-shading-rate-factors"></a>Kombinieren von Schattierungs Raten Faktoren
Die verschiedenen Quellen der Schattierungs Rate werden mithilfe dieses Diagramms nacheinander angewendet.

![Combiner](images/Combiners.PNG "Schattierungs Kombinatoren")

Jedes Paar von A und B wird mit einem Combiner kombiniert.

\* Beim Angeben einer shaderrate nach Vertex-Attribut.

- Wenn ein Geometry-Shader verwendet wird, kann die Schattierungs Rate über diese festgelegt werden.
- Wenn ein Geometry-Shader nicht verwendet wird, wird die Schattierungs Rate durch den anregenden Scheitelpunkt angegeben.

#### <a name="list-of-combiners"></a>Liste der Combiner
Die folgenden Kombinatoren werden unterstützt. Mit einem Combiner (C) und zwei Eingaben (a und B).

- **Pass-Through**. C. XY = A. XY.
- Über **Schreiben**. C. XY = B. XY.
- **Höhere Qualität**. C. XY = min (A. XY, B. XY).
- **Niedrigere Qualität**. C. XY = Max (A. XY, B. XY).
- **Apply Cost B in Relation zu A**. C. XY = min (maxrate, A. XY + B. XY).

dabei `maxRate` ist die größte zulässige Dimension des groben Pixels auf dem Gerät. Dies wäre

- **D3D12_AXIS_SHADING_RATE_2X** (d. h. ein Wert von 1), wenn additionalshadingratessupported ist `false` .
- **D3D12_AXIS_SHADING_RATE_4X** (d. h. der Wert 2), wenn additionalshadingratessupported ist `true` .

Die Auswahl des Combiners für die Schattierung variabler Rate wird in der Befehlsliste über [**ID3D12GraphicsCommandList5:: rssetshadingrate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate)festgelegt.

Wenn keine Combiner festgelegt ist, behalten Sie den Standardwert bei, der Pass-Through ist.

Wenn die Quelle zu einem Combiner eine [**D3D12_AXIS_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate)ist, die in der Unterstützungs Tabelle nicht zulässig ist *, wird die* Eingabe auf eine unterstützte Schattierungs Rate bereinigt.

Wenn die Ausgabe eines Combiners keiner Schattierungs Rate entspricht, die auf der Plattform unterstützt wird, wird das Ergebnis auf *eine unterstützte* Schattierungs Rate bereinigt.

### <a name="default-state-and-state-clearing"></a>Standardzustand und Status Löschung
Alle Schattierungs Raten Quellen, nämlich

- der vom Pipeline Status angegebene Satz (angegeben in der Befehlsliste),
- das Bild für den Bildschirm, das von einem Bild angezeigt wird, und
- das Attribut pro primitiver

hat den Standardwert **D3D12_SHADING_RATE_1X1**. Die Standard Kombinatoren lauten {Passthrough, Passthrough}.

Wenn kein Bildschirmraum Bild angegeben ist, wird von dieser Quelle eine Schattierungs Rate von 1x1 abgeleitet.

Wenn kein pro Primitives Attribut angegeben ist, wird von dieser Quelle eine Schattierungs Rate von 1x1 abgeleitet.

[ID3D12CommandList:: clearstate](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate) setzt die vom Pipeline Status angegebene Rate auf den Standardwert zurück, und die Auswahl des Bildschirmraum Bilds ist standardmäßig auf "kein Bildschirm-Bild" festgelegt.

## <a name="querying-shading-rate-by-using-sv_shadingrate"></a>Abfragen der Schattierungs Rate mithilfe von SV_ShadingRate
Es ist hilfreich zu wissen, welche Schattierungs Rate von der Hardware bei einem beliebigen Pixel-Shader-Aufruf gewählt wurde. Dies könnte eine Vielzahl von Optimierungen im PS-Code ermöglichen. Eine reine PS-Systemvariable, `SV_ShadingRate` , stellt Informationen zur Schattierungs Rate bereit.

### <a name="type"></a>Typ
Der Typ dieser Semantik ist uint.

### <a name="data-interpretation"></a>Dateninterpretation
Die Daten werden als Wert der [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) -Enumeration interpretiert.

### <a name="if-vrs-is-not-being-used"></a>Wenn VRS nicht verwendet wird
Wenn eine grobe Pixel Schattierung nicht verwendet wird, `SV_ShadingRate` wird als Wert von 1 x 1 zurückgelesen, was feine Pixel angibt.

### <a name="behavior-under-sample-based-execution"></a>Verhalten bei der Beispiel basierten Ausführung
Bei einem Pixelshader tritt bei der Kompilierung ein Fehler auf, wenn er Eingaben erzeugt `SV_ShadingRate` und auch eine Beispiel basierte Ausführung verwendet &mdash; , z. b. durch Einfügen `SV_SampleIndex` oder Verwenden des Sample Interpolation-Schlüssel Worts

> ### <a name="remarks-on-deferred-shading"></a>Hinweise zur verzögerten Schattierung
>
> Die Beleuchtungs Durchläufen einer verzögerten Schattierungs Anwendung müssen möglicherweise wissen, welche Schattierungs Rate für welchen Bereich des Bildschirms verwendet wurde. Dies ist so, dass die Verteilung von Beleuchtungs bestandenen mit einem gröbere-Satz gestartet werden kann. Die- `SV_ShadingRate` Variable kann verwendet werden, um dies zu erreichen, wenn Sie in den gbuffer geschrieben wird.

## <a name="depth-and-stencil"></a>Tiefe und Schablone
Wenn grobe Pixel Schattierung verwendet wird, werden tiefe, Schablone und Abdeckung immer berechnet und bei der vollständigen Stichproben Auflösung ausgegeben.

## <a name="using-the-shading-rate-requested"></a>Verwenden der angeforderten Schattierungs Rate
Bei allen Stufen wird erwartet, dass die von der Hardware bereitgestellte Schattierungs Rate, wenn eine Schattierungs Rate angefordert wird und auf der Kombination von Gerät und MSAA-Level unterstützt wird.

Eine angeforderte Schattierungs Rate bedeutet eine Schattierungs Rate, die als Ausgabe der Combiner berechnet wird (siehe den Abschnitt [Kombinieren von Schattierungs Raten Faktoren](#combining-shading-rate-factors) in diesem Thema).

Eine unterstützte Schattierungs Rate beträgt 1x1, 1X2, 2x1 oder 2 x 2 bei einem Renderingvorgang, bei dem die Stichproben Anzahl kleiner oder gleich vier ist. Wenn die *additionalshadingratessupported* -Funktion ist `true` , werden 2 x 4, 4x2 und 4X4 auch die Schattierungs Raten für einige Stichproben gezählt. (Weitere Informationen finden Sie in der Tabelle im Abschnitt [mit Variablen Raten Schattierung (VRS)](#with-variable-rate-shading-vrs) in diesem Thema).

## <a name="screen-space-derivatives"></a>Bildschirm-Speicher Ableitungen
Berechnungen von Pixel-zu-angrenzende-Pixel-Farbverläufen sind von der groben Pixel Schattierung betroffen. Wenn z. b. 2 x 2 grobe Pixel verwendet werden, ist ein Farbverlauf doppelt so groß wie bei Verwendung von groben Pixeln. Abhängig von der gewünschten Funktionalität kann es sein, dass die Anwendung Shader so anpassen soll, dass dies kompensiert &mdash; wird oder nicht.

Da MIPS basierend auf einer abgeleiteten Bildschirmfläche ausgewählt wird, wirkt sich die Verwendung der groben Pixel Schattierung auf die MIP-Auswahl aus. Die Verwendung der groben Pixel Schattierung bewirkt, dass weniger ausführliche MIPS ausgewählt werden, als wenn grobe Pixel nicht verwendet werden.

## <a name="attribute-interpolation"></a>Attribut Interpolations
Eingaben an einen PixelShader können basierend auf Ihren Quell Vertices interpoliert werden. Da die Schattierung von Variablen Raten sich auf die Bereiche des Ziels auswirkt, die von den einzelnen Aufrufen des Pixel-Shaders geschrieben wurden, interagiert Sie mit der Attribut Interpolation. Die drei Arten von Interpolationen sind Center, Centroid und Sample.

### <a name="center"></a>Zentrum
Die zentrale Interpolations Position eines groben Pixels ist das geometrische Zentrum des vollständigen Pixel Bereichs. `SV_Position` wird immer in der Mitte des groben Pixel Bereichs interpoliert.

### <a name="centroid"></a>Schwerpunkt
Wenn eine grobe Pixel Schattierung mit MSAA verwendet wird, werden für jedes feine Pixel immer noch Schreibvorgänge auf die vollständige Anzahl der für die MSAA-Ebene des Ziels zugeordneten Stichproben durchlaufen. Daher berücksichtigt der Speicherort der Schwerpunkt Interpolation alle Stichproben für feine Pixel in groben Pixeln. Das heißt, der Speicherort der Schwerpunkt-Interpolation ist als erstes abgedecktes Beispiel definiert, und zwar in zunehmender Reihenfolge des Beispiel Index. Die effektive Abdeckung des Beispiels ist und wird mit dem entsprechenden Bit des Raster State Sample Mask festgestellt.

> [!NOTE]
> Wenn eine grobe Pixel Schattierung auf Ebene 1 verwendet wird, ist samplemask immer eine vollständige Maske. Wenn samplemask so konfiguriert ist, dass es keine vollständige Maske ist, ist die grobe Pixel Schattierung auf Ebene 1 deaktiviert.

### <a name="sample-based-execution"></a>Beispiel basierte Ausführung
Eine Beispiel basierte Ausführung oder eine *Supersampling*, &mdash; die durch die Verwendung der Beispiel Interpolations Funktion verursacht wird, &mdash; kann mit grober Pixel Schattierung verwendet werden und bewirkt, dass der Pixelshader pro Stichprobe aufgerufen wird. Für Ziele der Stichproben Anzahl n wird der Pixelshader n-Mal pro feiner Pixel aufgerufen.

### <a name="evaluateattributesnapped"></a>Evaluateattributesnapped
Systeminterne Pull-Modell-Funktionen sind nicht mit groben Pixel Schattierung auf Ebene 1 kompatibel. Wenn versucht wird, systeminterne pullmodellfunktionen mit grober Pixel Schattierung auf Ebene 1 zu verwenden, wird die grobe Pixel Schattierung automatisch deaktiviert.

Die systeminterne Funktion `EvaluateAttributeSnapped` darf mit grober Pixel Schattierung auf Ebene 2 verwendet werden. Die Syntax ist identisch mit der Syntax.

```hlsl
numeric EvaluateAttributeSnapped(   
    in attrib numeric value, 
    in int2 offset);
```

Für den Kontext `EvaluateAttributeSnapped` verfügt über einen Offset-Parameter mit zwei Feldern. Bei Verwendung ohne grobe Pixel Schattierung werden nur die nieder wertigen vier Bits aus dem vollständigen 32 verwendet. Diese vier Bits stellen den Bereich [-8, 7] dar. Dieser Bereich umfasst ein 16x16-Raster innerhalb eines Pixels. Der Bereich gibt an, dass der obere und linke Rand des Pixels eingeschlossen werden, der untere und der Rechte Rand jedoch nicht. Offset (-8,-8) befindet sich in der linken oberen Ecke, und Offset (7, 7) befindet sich in der rechten unteren Ecke. Offset (0,0) ist die Mitte des Pixels.

Bei Verwendung mit grober Pixel Schattierung `EvaluateAttributeSnapped` kann mit dem Offset-Parameter eine größere Anzahl von Positionen angegeben werden. Der Offset-Parameter wählt ein 16x16-Raster für jedes feine Pixel aus, und es sind mehrere feine Pixel vorhanden. Der Ausdrucks Bare Bereich und die resultierende Anzahl von Bits, die verwendet werden, hängen von der groben Pixelgröße ab. Der obere und linke Rand des groben Pixels sind eingeschlossen, der untere und der Rechte Rand hingegen nicht.

In der folgenden Tabelle wird die Interpretation des `EvaluateAttributeSnapped` offset-Parameters für jede grobe Pixelgröße beschrieben.

#### <a name="evaluateattributesnappeds-offset-range"></a>Offset Bereich von evaluateattributesnapped

|Grobe Pixelgröße  |Indexbare Bereiche             |Darstellbare Bereichs Größe  |Erforderliche Anzahl von Bits {x, y}  |Binäre Maske verwendbarer Bits          |    
|------------------:|---------------------------:|-------------------------:|-----------------------------:|-----------------------------------:|    
|1x1 (fein)         |{ \[ -8, 7 \] , \[ -8, 7 \] }      |{16, 16}                  |{4, 4}                        |{000000000000xxxx, 000000000000xxxx}|    
|1X2                |{ \[ -8, 7 \] , \[ -16, 15 \] }    |{16, 32}                  |{4, 5}                        |{000000000000xxxx, 00000000000xxxxx}|    
|2x1                |{ \[ -16, 15 \] , \[ -8, 7 \] }    |{32, 16}                  |{5, 4}                        |{00000000000xxxxx, 000000000000xxxx}|    
|2 x 2                |{ \[ -16, 15 \] , \[ -16, 15 \] }  |{32, 32}                  |{5, 5}                        |{00000000000xxxxx, 00000000000xxxxx}|    
|2 x 4                |{ \[ -16, 15 \] , \[ -32, 31 \] }  |{32, 64}                  |{5, 6}                        |{00000000000xxxxx, 0000000000xxxxxx}|    
|4x2                |{ \[ -32, 31 \] , \[ -16, 15 \] }  |{64, 32}                  |{6, 5}                        |{0000000000xxxxxx, 00000000000xxxxx}|    
|4x4                |{ \[ -32, 31 \] , \[ -32, 31 \] }  |{64, 64}                  |{6, 6}                        |{0000000000xxxxxx, 0000000000xxxxxx}|   

In den folgenden Tabellen finden Sie eine Anleitung für die Konvertierung von in die Dezimal-und dezimal Darstellung. Das erste nutzbare Bit in der Binär Maske ist das Signier Bit, und der Rest der Binär Maske besteht aus dem numerischen Teil.

Das Zahlen Schema für vier-Bit-Werte, die an an übermittelt werden, `EvaluateAttributeSnapped` ist nicht spezifisch für die Schattierung von Variablenraten. Dies wird aus Gründen der Vollständigkeit hier wiederholt.

Für vier-Bit-Werte.

| Binärwert | Decimal  | Bruchteil |
|-------------:|---------:|-----------:|
|         1000 |-0,5 f     |-8/16     |
|         1001 |-0.4375 f  |-7/16|    |
|         1010 |-0,375 f   |-6/16|    |
|         1011 |-0.3125 f  |-5/16     |
|         1100 |0,25 f    |-4/16     |
|         1101 |-0.1875 f  |-3/16     |
|         1110 |-0,125 f   |-2/16     |
|         1111 |-0.0625 f  |-1/16      |
|         0000 |0,0 f      |0 / 16      |
|         0001 |-0.0625 f  |1 / 16      |
|         0010 |-0,125 f   |2 / 16      |
|         0011 |-0.1875 f  |3 / 16      |
|         0100 |0,25 f    |4 / 16      |
|         0101 |-0.3125 f  |5 / 16      |
|         0110 |-0,375 f   |6 / 16      |
|         0111 |-0.4375 f  |7 / 16      |

Für fünf-Bit-Werte.

| Binärwert | Decimal  | Bruchteil |
|-------------:|---------:|-----------:|
|        10000 |-1        |-16/16    |
|        10001 |-0,9375   |-15/16    |
|        10010 |-0,875    |-14/16    |
|        10011 |-0,8125   |-13/16    |
|        10100 |-0.75     |-12/16    |
|        10101 |-0,6875   |-11/16    |
|        10110 |-0,625    |-10/16    |
|        10111 |-0,5625   |-9/16     |
|        11000 |–0,5      |-8/16     |
|        11001 |-0,4375   |-7/16     |
|        11010 |-0,375    |-6/16     |
|        11011 |-0,3125   |-5/16     |
|        11100 |-0.25     |-4/16     |
|        11101 |-0,1875   |-3/16     |
|        11110 |-0,125    |-2/16     |
|        11111 |-0,0625   |-1/16     |
|        00000 |0         |0 / 16      |
|        00001 |0,0625    |1 / 16      |
|        00010 |0,125     |2 / 16      |
|        00011 |0,1875    |3 / 16      |
|        00100 |0,25      |4 / 16      |
|        00101 |0,3125    |5 / 16      |
|        00110 |0,375     |6 / 16      |
|        00111 |0,4375    |7 / 16      |
|        01000 |0.5       |8 / 16      |
|        01001 |0,5625    |9 / 16      |
|        01010 |0,625     |10 / 16     |
|        01011 |0,6875    |11 / 16     |
|        01100 |0,75      |12 / 16     |
|        01101 |0,8125    |13 / 16     |
|        01110 |0,875     |14 / 16     |
|        01111 |0,9375    |15 / 16     |

Für 6-Bit-Werte.

| Binärwert | Decimal  | Bruchteil |
|-------------:|---------:|-----------:|
|       100.000 |-2        |-32/16    |
|       100001 |-1,9375   |-31/16    |
|       100010 |-1,875    |-30/16    |
|       100011 |-1,8125   |-29/16    |
|       100100 |-1,75     |-28/16    |
|       100101 |-1,6875   |-27/16    |
|       100110 |-1,625    |-26/16    |
|       100111 |-1,5625   |-25/16    |
|       101000 |-1,5      |-24/16    |
|       101001 |-1,4375   |-23/16    |
|       101010 |-1,375    |-22/16    |
|       101011 |-1,3125   |-21/16    |
|       101100 |-1.25     |-20/16    |
|       101101 |-1,1875   |-19/16    |
|       101110 |-1,125    |-18/16    |
|       101111 |-1,0625   |-17/16    |
|       110000 |-1        |-16/16    |
|       110001 |-0,9375   |-15/16    |
|       110010 |-0,875    |-14/16    |
|       110011 |-0,8125   |-13/16    |
|       110100 |-0.75     |-12/16    |
|       110101 |-0,6875   |-11/16    |
|       110110 |-0,625    |-10/16    |
|       110111 |-0,5625   |-9/16     |
|       111000 |–0,5      |-8/16     |
|       111001 |-0,4375   |-7/16     |
|       111010 |-0,375    |-6/16     |
|       111011 |-0,3125   |-5/16     |
|       111100 |-0.25     |-4/16     |
|       111101 |-0,1875   |-3/16     |
|       111110 |-0,125    |-2/16     |
|       111111 |-0,0625   |-1/16     |
|       000000 |0         |0 / 16      |
|       000001 |0,0625    |1 / 16      |
|       000010 |0,125     |2 / 16      |
|       000011 |0,1875    |3 / 16      |
|       000100 |0,25      |4 / 16      |
|       000101 |0,3125    |5 / 16      |
|       000110 |0,375     |6 / 16      |
|       000111 |0,4375    |7 / 16      |
|       001000 |0.5       |8 / 16      |
|       001001 |0,5625    |9 / 16      |
|       001010 |0,625     |10 / 16     |
|       001011 |0,6875    |11 / 16     |
|       001100 |0,75      |12 / 16     |
|       001101 |0,8125    |13 / 16     |
|       001110 |0,875     |14 / 16     |
|       001111 |0,9375    |15 / 16     |
|       010000 |1         |16 / 16     |
|       010001 |1,0625    |17 / 16     |
|       010010 |1,125     |18 / 16     |
|       010011 |1,1875    |19 / 16     |
|       010100 |1,25      |20 / 16     |
|       010101 |1,3125    |21 / 16     |
|       010110 |1,375     |22 / 16     |
|       010111 |1,4375    |23 / 16     |
|       011000 |1.5       |24 / 16     |
|       011001 |1,5625    |25 / 16     |
|       011010 |1,625     |26 / 16     |
|       011011 |1,6875    |27 / 16     |
|       011100 |1,75      |28 / 16     |
|       011101 |1,8125    |29 / 16     |
|       011110 |1,875     |30 / 16     |
|       011111 |1,9375    |31 / 16     |

Auf die gleiche Weise wie bei fein Pixeln `EvaluateAttributeSnapped` wird das Raster der auswertbaren Speicherorte bei der Verwendung der groben Pixel Schattierung auf das grobe Pixel Zentrum zentriert.

## <a name="setsamplepositions"></a>Setsamplepositions
Wenn die API [**ID3D12GraphicsCommandList1:: setsamplepositions**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist1-setsamplepositions) mit der groben Schattierung verwendet wird, legt die API die Beispiel Positionen für feine Pixel fest.

## <a name="sv_coverage"></a>SV_Coverage
Wenn `SV_Coverage` als Shader-Eingabe oder-Ausgabe auf Ebene 1 deklariert ist, wird die grobe Pixel Schattierung deaktiviert.

Sie können die `SV_Coverage` Semantik mit grober Pixel Schattierung auf Ebene 2 verwenden, und Sie gibt an, welche Beispiele eines MSAA-Ziels geschrieben werden.

Wenn eine grobe Pixel Schattierung verwendet wird &mdash; , sodass mehrere Quell Pixel eine Kachel bilden, &mdash; stellt die Abdeckungs Maske alle Beispiele dar, die von dieser Kachel stammen.

Wenn die Kompatibilität mit MSAA durch grobe Pixel Schattierung festgelegt wurde, kann die Anzahl der Abdeckungs Bits variieren, die angegeben werden müssen. Beispielsweise wird mit einer 4X-MSAA-Ressource, die [**D3D12_SHADING_RATE_2x2**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate)verwendet, jedes grobe Pixel in vier feine Pixel geschrieben, und jedes feine Pixel hat vier Stichproben. Dies bedeutet, dass jedes grobe Pixel auf insgesamt 4 * 4 = 16 Stichproben schreibt.

### <a name="number-of-coverage-bits-needed"></a>Anzahl der benötigten Abdeckungs Bits
In der folgenden Tabelle wird angegeben, wie viele Abdeckungs Bits für jede Kombination von grober Pixelgröße und MSAA-Ebene benötigt werden.

![Numofcoveragebits](images/NumberOfCoverageBits.PNG "Abdeckungs Bits")

Wie in der Tabelle angegeben, ist es nicht möglich, grobe Pixel zu verwenden, um zu einem Zeitpunkt mehr als 16 Stichproben zu schreiben, indem Sie das durch Direct3D 12 bereitgestellte Schattierungs Feature für Variablen Raten verwenden. Diese Einschränkung ist auf die Einschränkungen von Direct3D 12 in Bezug darauf zurückzuführen, welche MSAA-Ebenen mit welcher groben Pixelgröße zulässig sind (Weitere Informationen finden Sie in der Tabelle im Abschnitt [mit Variablen Raten Schattierung (VRS)](#with-variable-rate-shading-vrs) in diesem Thema).

### <a name="ordering-and-format-of-bits-in-the-coverage-mask"></a>Reihenfolge und Format von Bits in der Abdeckungs Maske
Die Bits der Abdeckungs Maske entsprechen einer klar definierten Reihenfolge. Die Maske besteht aus den Abdeckungen (von links nach rechts und dann von oben nach unten (Spalten-Hauptreihen Folge). Abdeckungs Bits sind die nieder wertigen Bits der Abdeckungs Semantik und sind dicht gepackt.

Die folgende Tabelle zeigt das Abdeckungs Masken Format für unterstützte Kombinationen von grober Pixelgröße und MSAA-Ebene.

![Coverage1x](images/Coverage1x.PNG "Abdeckung bei 1 x")

In der folgenden Tabelle sind 2X-MSAA-Pixel aufgeführt, wobei jedes Pixel zwei Stichproben der Indizes 0 und 1 aufweist.

Die Positionierung der Bezeichnungen von Beispielen in den Pixeln dient zur Veranschaulichung und vermittelt nicht notwendigerweise die räumlichen {X, Y}-Speicherorte von Beispielen auf diesem Pixel. vor allem, wenn Beispiel Positionen Programm gesteuert geändert werden können. Auf die Beispiele wird durch ihren 0-basierten Index verwiesen.

![Coverage2x](images/Coverage2x.PNG "Abdeckung bei 2 x")

In der folgenden Tabelle werden 4X-MSAA-Pixel angezeigt, wobei jedes Pixel vier Stichproben der Indizes 0, 1, 2 und 3 enthält.

![Coverage4x](images/Coverage4x.PNG "Abdeckung bei 4X")

## <a name="discard"></a>Verwerfen
Wenn die HLSL-Semantik `discard` mit grober Pixel Schattierung verwendet wird, werden grobe Pixel verworfen.

## <a name="target-independent-rasterization-tir"></a>Ziel unabhängige rasterisierung (TIR)
TIR wird nicht unterstützt, wenn eine grobe Pixel Schattierung verwendet wird.

## <a name="raster-order-views-rovs"></a>Raster Anordnungs Sichten (ROVs)
Die Rots-Interlocks werden als Betriebs bei feiner Pixel Granularität angegeben. Wenn eine Schattierung pro Stichprobe durchgeführt wird, werden die Interlocks bei der Stichproben Granularität betrieben.

## <a name="conservative-rasterization"></a>Konservative rasterisierung
Sie können die konservative Rasterung mit Schattierung variabler Geschwindigkeit verwenden. Wenn die konservative rasterisierung mit grober Pixel Schattierung verwendet wird, werden feine Pixel in groben Pixeln durch eine vollständige Abdeckung im Rahmen einer vollständigen Abdeckung unregelmäßig gerachtelt.

### <a name="coverage"></a>Abdeckung
Wenn eine konservative rasterisierung verwendet wird, enthält die Abdeckungs Semantik vollständige Masken für feine Pixel, die abgedeckt werden, und 0 für feine Pixel, die nicht abgedeckt werden.

## <a name="bundles"></a>Bundles
Sie können Schattierungs-APIs für Variablen Raten für ein Bündel aufrufen.

## <a name="render-passes"></a>Rendering-Durchlauf
Sie können Schattierungs-APIs für Variablen Raten in einem [renderdurchlauf](/windows/desktop/direct3d12/direct3d-12-render-passes)aufrufen.

## <a name="calling-the-vrs-apis"></a>Aufrufen der VRS-APIs
Im nächsten Abschnitt wird beschrieben, wie Sie mithilfe von Direct3D 12 von Ihrer Anwendung auf Variablen Raten Schattierung zugreifen können.

### <a name="capability-querying"></a>Funktions Abfrage

Um die Schattierungs Funktion für Variablen Raten des Adapters abzufragen, müssen Sie [**ID3D12Device:: checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) mit [**D3D12_FEATURE::D 3D12_FEATURE_D3D12_OPTIONS6**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature)aufrufen und eine [ **D3D12_FEATURE_DATA_D3D12_OPTIONS6** Struktur](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) bereitstellen, die die Funktion ausfüllen kann. Die **D3D12_FEATURE_DATA_D3D12_OPTIONS6** Struktur enthält mehrere Member, einschließlich einer, die vom enumerierten Typ ist [**D3D12_VARIABLE_SHADING_RATE_TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) (D3D12_FEATURE_DATA_D3D12_OPTIONS6:: variableshadingratetier), und eine, die angibt, ob die Hintergrundverarbeitung unterstützt wird (D3D12_FEATURE_DATA_D3D12_OPTIONS6:: backgroundprocessingsupported).

Zum Abfragen der Funktion der Ebene 1 können Sie beispielsweise dies tun.

```cpp
D3D12_FEATURE_DATA_D3D12_OPTIONS6 options;
return 
    SUCCEEDED(m_device->CheckFeatureSupport(
        D3D12_FEATURE_D3D12_OPTIONS6, 
        &options, 
        sizeof(options))) && 
    options.ShadingRateTier == D3D12_VARIABLE_SHADING_RATE_TIER_1;
```

### <a name="shading-rates"></a>Schattierungs Raten

Die Werte in der [ **D3D12_SHADING_RATE** -Enumeration](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) sind so organisiert, dass Schattierungs Raten leicht in zwei Achsen aufgeteilt werden können, wobei die Werte jeder Achse im logarithmischen Raum entsprechend der [ **D3D12_AXIS_SHADING_RATE** -Enumeration](/windows/desktop/api/d3d12/ne-d3d12-d3d12_axis_shading_rate)entsprechend dargestellt werden.

Sie können ein Makro verfassen, um zwei Achsen Schattierungs Raten in eine Schattierungs Rate wie diese zu verfassen.

```cpp
#define D3D12_MAKE_COARSE_SHADING_RATE(x,y) ((x) << 2 | (y))
D3D12_MAKE_COARSE_SHADING_RATE(
    D3D12_AXIS_SHADING_RATE_2X, 
    D3D12_AXIS_SHADING_RATE_1X)
```

Die Plattform stellt auch diese Makros bereit, die in definiert sind `d3d12.h` .

```cpp
#define D3D12_GET_COARSE_SHADING_RATE_X_AXIS(x) ((x) >> 2 )
#define D3D12_GET_COARSE_SHADING_RATE_Y_AXIS(y) ((y) & 3 )
```

Diese können verwendet werden, um sich zu Verschneiden und zu verstehen `SV_ShaderRate` .

> [!NOTE]
> Diese Dateninterpretation ist darauf ausgerichtet, das Bildschirmraum Bild zu beschreiben, das von Shadern manipuliert werden kann. Dies wird in den obigen Abschnitten ausführlicher erläutert. Es gibt jedoch keinen Grund, eine konsistente Definition der groben Pixelgrößen zu verwenden, die überall verwendet werden sollen, einschließlich beim Festlegen der Schattierungs Rate auf Befehls Ebene.

### <a name="setting-command-level-shading-rate-and-combiners"></a>Festlegen von Schattierungs Rate und Kombinatoren auf Befehls Ebene
Die Schattierungs Rate und optional Kombinatoren werden durch die [**ID3D12GraphicsCommandList5:: rssetshadingrate**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrate) -Methode angegeben. Sie übergeben einen [**D3D12_SHADING_RATE**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate) Wert für die Basis Schattierungs Rate und ein optionales Array von [D3D12_SHADING_RATE_COMBINER](/windows/desktop/api/d3d12/ne-d3d12-d3d12_shading_rate_combiner) Werten.

### <a name="preparing-the-screen-space-image"></a>Vorbereiten des Bildschirmraum Bilds
Der schreibgeschützte Ressourcen Status, der ein verwendbares Schattierungs Raten Image angibt, wird als [D3D12_RESOURCE_STATES definiert::D 3D12_RESOURCE_STATE_SHADING_RATE_SOURCE](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states).

### <a name="setting-the-screen-space-image"></a>Festlegen des Bildschirmraum Bilds
Sie geben das Bildschirmraum Bild mithilfe der [**ID3D12GraphicsCommandList5:: rssetshadingrateimage**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist5-rssetshadingrateimage) -Methode an.

```cpp
m_commandList->RSSetShadingRateImage(screenSpaceImage);
```

### <a name="querying-the-tile-size"></a>Abfragen der Kachel Größe
Sie können die Kachel Größe aus dem [**D3D12_FEATURE_DATA_D3D12_OPTIONS6:: shadingrateimagetilesize**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options6) -Member Abfragen. Siehe Funktions [Abfrage](#capability-querying) oben.

Eine Dimension wird abgerufen, da die horizontale und die vertikale Dimension immer identisch sind. Wenn die Funktion des Systems [**D3D12_SHADING_RATE_TIER_NOT_SUPPORTED**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier)ist, ist die zurückgegebene Kachel Größe 0.
