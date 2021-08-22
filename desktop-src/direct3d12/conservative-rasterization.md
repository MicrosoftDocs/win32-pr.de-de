---
title: Direct3D 12 Konservative Rasterung
description: Die konservative Rasterung bietet eine gewisse Sicherheit beim Pixelrendering, was insbesondere für Algorithmen zur Kollisionserkennung hilfreich ist.
ms.assetid: 081199AD-1702-4EC8-95AD-B1148C676199
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15bb5893e944c5d495cf91fdb334bd6ab5f755b7f1e200648242cb46b281f695
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119045763"
---
# <a name="direct3d-12-conservative-rasterization"></a>Direct3D 12 Konservative Rasterung

Die konservative Rasterung bietet eine gewisse Sicherheit beim Pixelrendering, was insbesondere für Algorithmen zur Kollisionserkennung hilfreich ist.

-   [Übersicht](#overview)
-   [Interaktionen mit der Pipeline](#interactions-with-the-pipeline)
    -   [Interaktion mit Rasterungsregeln](#rasterization-rules-interaction)
    -   [Multisamplinginteraktion](#multisampling-interaction)
    -   [SampleMask-Interaktion](#samplemask-interaction)
    -   [Tiefen-/Schablonen-Testinteraktion](#depthstencil-test-interaction)
    -   [Pixelinteraktion des Hilfselements](#helper-pixel-interaction)
    -   [Ausgabeabdeckungsinteraktion](#output-coverage-interaction)
    -   [InputCoverage-Interaktion](#inputcoverage-interaction)
    -   [InnerCoverage-Interaktion](#innercoverage-interaction)
    -   [Attributinterpolationsinteraktion](#attribute-interpolation-interaction)
    -   [Clippinginteraktion](#clipping-interaction)
    -   [Clip Distance-Interaktion](#clip-distance-interaction)
    -   [Interaktion mit unabhängiger Rasterung als Ziel](#target-independent-rasterization-interaction)
    -   [IA Primitive Topologieinteraktion](#ia-primitive-topology-interaction)
    -   [Abfrageinteraktion](#query-interaction)
    -   [Cull-Zustandsinteraktion](#cull-state-interaction)
    -   [IsFrontFace-Interaktion](#isfrontface-interaction)
    -   [Interaktion mit Füllmodi](#fill-modes-interaction)
-   [Details zur Implementierung](#implementation-details)
-   [API-Zusammenfassung](#api-summary)
-   [Zugehörige Themen](#related-topics)

## <a name="overview"></a>Übersicht

Die konservative Rasterung bedeutet, dass alle Pixel, die mindestens teilweise von einem gerenderten Primitiven abgedeckt werden, gerastert werden, was bedeutet, dass der Pixelshader aufgerufen wird. Das normale Verhalten ist die Stichprobenentnahme, die nicht verwendet wird, wenn die konservative Rasterung aktiviert ist.

Die konservative Rasterung ist in einer Reihe von Situationen nützlich, z. B. zur Sicherheit bei der Kollisionserkennung, verdeckungs-culling und kachelntem Rendering.

Die folgende Abbildung zeigt beispielsweise ein grünes Dreieck, das mithilfe der konservativen Rasterung gerendert wird, wie es im Rasterizer angezeigt wird (d.h. mit 16,8 Scheitelpunktkoordinaten mit festem Punkt). Der browne Bereich wird als "Unsicherkeitsregion" bezeichnet– ein konzeptioneller Bereich, der die erweiterten Begrenzungen des Dreiecks darstellt, der erforderlich ist, um sicherzustellen, dass der Primitive im Rasterizer hinsichtlich der ursprünglichen Gleitkomma-Scheitelpunktkoordinaten konservativer ist. Die roten Quadrate an jedem Scheitelpunkt zeigen, wie der Unsicherheitsbereich berechnet wird: als ausgeweetetes Quadrat.

Die großen grauen Quadrate zeigen die Pixel an, die gerendert werden. Die rosa quadratischen Quadrate zeigen Pixel, die mithilfe der "Regel oben links" gerendert werden, die ins Spiel kommt, wenn der Rand des Dreiecks den Rand der Pixel überschreitet. Es können falsch positive Ergebnisse (Pixel festgelegt, die nicht vorhanden sein sollten) vorhanden sein, die das System normalerweise, aber nicht immer mit Cull aufweist.

![Die Regel oben links](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interaktionen mit der Pipeline

### <a name="rasterization-rules-interaction"></a>Interaktion mit Rasterungsregeln

Im konservativen Rasterungsmodus gelten Rasterungsregeln auf die gleiche Weise wie, wenn der konservative Rasterungsmodus nicht aktiviert ist, mit Ausnahmen für die oben beschriebene Top-Left-Regel und Pixelabdeckung. 16.8 Fixed-Point Rasterizer-Genauigkeit muss verwendet werden.

Pixel, die nicht abgedeckt würden, wenn Hardware vollständige Gleitkomma-Scheitelpunktkoordinaten verwendet, können nur eingeschlossen werden, wenn sie sich innerhalb eines Unsicherheitsbereichs befinden, der nicht größer als ein halbes Pixel in der Festkommadomäne ist. Es wird erwartet, dass zukünftige Hardware die in Ebene 2 angegebene region mit verstärkter Unsicherheit erreicht. Beachten Sie, dass diese Anforderung verhindert, dass sich sliver Dreiecke weiter als nötig erweitern.

Eine ähnliche gültige Unsicherheitsregion gilt auch für `InnerCoverage` , aber sie ist enger, da keine Implementierungen in diesem Fall eine größere Unsicherheitsregion erfordern. Weitere Informationen finden Sie unter [Interaktion mit InnerCoverage.](#innercoverage-interaction)

Innere und äußere Unsicherkeitsregionen müssen größer oder gleich der Größe der Hälfte des Subpixelrasters oder 1/512 eines Pixels in der Festkommadomäne sein. Dies ist die mindestens gültige Unsicherheitsregion. 1/512 stammt aus der Rasterizer-Koordinatendarstellung mit 16,8 festem Punkt und der Regel für die Rundung auf die nächste, die beim Konvertieren von Gleitkomma-Scheitelpunktkoordinaten in 16,8 Festpunktkoordinaten angewendet wird. 1/512 kann sich ändern, wenn sich die Genauigkeit des Rasterizers ändert. Wenn eine Implementierung diesen Minimalunsicherheitsbereich implementiert, müssen sie der Top-Left Regel folgen, wenn ein Rand oder eine Ecke des Unsicherheitsbereichs entlang der Kante oder Ecke eines Pixels fällt. Die abgeschnittenen Ränder des Unsicherkeitsbereichs sollten als der nächste Scheitelpunkt behandelt werden, was bedeutet, dass sie als zwei Kanten gezählt werden: die beiden, die am zugeordneten Scheitelpunkt verknüpft sind. Top-Left Regel ist erforderlich, wenn der Mindestunsicherheitsbereich verwendet wird. Wenn dies nicht der Fall ist, kann eine konservative Rasterungsimplementierung keine Pixel rastern, die abgedeckt werden könnten, wenn der konservative Rasterungsmodus deaktiviert ist.

Das folgende Diagramm veranschaulicht einen gültigen äußeren Unsicherkeitsbereich, der entsteht, indem ein Quadrat um die Ränder des Primitivs in der Festkommadomäne geleert wird (d. h. die Scheitelpunkte wurden durch die 16,8-Fixpunktdarstellung quantisiert). Die Abmessungen dieses Quadrats basieren auf der gültigen Größe des äußeren Unsicherkeitsbereichs: Für 1/2 eines Pixels ist das Quadrat 1 Pixel breite und höhe, für 1/512 pixel beträgt das Quadrat 1/256 eines Pixels in Breite und Höhe. Das grüne Dreieck stellt ein bestimmtes Primitiv dar, die rote gepunktete Linie stellt die Grenze an der überschätzten konservativen Rasterung dar, die soliden schwarzen Quadrate stellen das Quadrat dar, das entlang der primitiven Ränder gekehrt wird, und der blaue markierte Bereich ist der äußere Unsicherkeitsbereich:

![äußerer Unsicherheitsbereich.](images/outercoverage.jpg)

### <a name="multisampling-interaction"></a>Multisamplinginteraktion

Unabhängig von der Anzahl der Stichproben in **RenderTarget** / **DepthStencil-Oberflächen** (oder ob *ForcedSampleCount* verwendet wird oder nicht), werden alle Stichproben für Pixel abgedeckt, die durch konservative Rasterung gerastet werden. Einzelne Beispielspeicherorte werden nicht getestet, ob sie in den Primitiven fallen oder nicht.

### <a name="samplemask-interaction"></a>SampleMask-Interaktion

Der *SampleMask-Rasterizerstatus* gilt auf die gleiche Weise wie , wenn die konservative Rasterung für nicht aktiviert `InputCoverage` ist, aber keine Auswirkungen hat `InnerCoverage` (d. h. es wird nicht AND in eine Eingabe eingegeben, die mit deklariert `InnerCoverage` wurde). Dies `InnerCoverage` liegt daran, dass nicht mit der Maskierung von MSAA-Stichproben zusammenhängt: 0 `InnerCoverage` bedeutet nur, dass das Pixel nicht garantiert vollständig abgedeckt ist, und nicht, dass keine Stichproben aktualisiert werden.

### <a name="depthstencil-test-interaction"></a>Tiefen-/Schablonen-Testinteraktion

Tiefen-/Schablonentests werden für ein konservatives rasterisiertes Pixel auf die gleiche Weise fortgesetzt, als wären alle Stichproben abgedeckt, wenn die konservative Rasterung nicht aktiviert ist.

Wenn Sie mit allen behandelten Beispielen fortfahren, kann dies zu einer Tiefen extrapolation führen, die gültig ist und wie angegeben an den Viewport angepasst werden muss, wenn die konservative Rasterung nicht aktiviert ist. Dies ähnelt der Verwendung von Pixelfrequenzinterpolationsmodi auf einem **RenderTarget** mit einer Stichprobenanzahl größer als 1. Im Fall der konservativen Rasterung ist es jedoch der Tiefenwert, der in den festen Funktionstiefetest geht, der extrapoliert werden kann.

Early Depth culling behavior with Depth Extrapolation is undefined( Early Depth culling behavior with Depth Extrapolation is undefined. Dies liegt daran, dass einige Hardware für die Frühzeitige Tiefenkeulung extrapolierte Tiefenwerte nicht ordnungsgemäß unterstützen kann. Das Verhalten der frühen Tiefenkeulierung bei der Tiefen extrapolation ist jedoch selbst bei Hardware problematisch, die extrapolierte Tiefenwerte unterstützen kann. Dieses Problem kann behoben werden, indem die Pixel-Shader-Eingabetiefe an die Minimal- und Höchstwerte des Primitiven gebunden wird, der gerastt wird, und diesen Wert in `oDepth` schreibt (das Pixel-Shader-Ausgabetieferegister). Implementierungen sind erforderlich, um early depth culling in diesem Fall aufgrund des `oDepth` Schreibzugriffs zu deaktivieren.

### <a name="helper-pixel-interaction"></a>Pixelinteraktion des Hilfselements

Hilfspixelregeln gelten auf die gleiche Weise wie bei nicht aktivierter konservativer Rasterung. Im Rahmen dieses Abschnitts müssen alle Pixel, einschließlich Der Hilfspixel, `InputCoverage` genau wie im Interaktionsabschnitt angegeben angezeigt `InputCoverage` werden. Daher melden vollständig nicht abgedeckte Pixel eine Abdeckung von 0.

### <a name="output-coverage-interaction"></a>Ausgabeabdeckungsinteraktion

Die Ausgabeabdeckung `oMask` () verhält sich für ein konservatives rasterisiertes Pixel, wie dies der Fall ist, wenn die konservative Rasterung nicht mit allen behandelten Stichproben aktiviert ist.

### <a name="inputcoverage-interaction"></a>InputCoverage-Interaktion

Im konservativen Rasterungsmodus wird dieses Eingaberegister aufgefüllt, als ob alle Stichproben abgedeckt wären, wenn die konservative Rasterung für ein bestimmtes konservatives Rasterpixel nicht aktiviert ist. Das heißt, alle vorhandenen Interaktionen gelten (z.B. *SampleMask* wird angewendet), und die ersten n Bits `InputCoverage` aus dem LSB werden für ein konservatives Rasterpixel auf 1 festgelegt, wenn eine n Stichprobe pro Pixel **renderTarget** und/oder **der DepthStencil-Puffer** an der **Ausgabezusammenführung** gebunden ist, oder ein n Sample *ForcedSampleCount*. Die restlichen Bits sind 0.

Diese Eingabe ist in einem Shader verfügbar, unabhängig von der Verwendung der konservativen Rasterung, obwohl die konservative Rasterung ihr Verhalten so ändert, dass nur alle abgedeckten Stichproben (oder keine für Hilfspixel) angezeigt werden.

### <a name="innercoverage-interaction"></a>InnerCoverage-Interaktion

Dieses Feature ist für Ebene 3 erforderlich und nur in verfügbar. Die Laufzeit schlägt bei der Shadererstellung für Shader fehl, die diesen Modus verwenden, wenn eine Implementierung eine Ebene kleiner als Ebene 3 unterstützt.

Der Pixelshader verfügt über eine 32-Bit-Skalarzahl vom Typ System Generate Value ( Systemgenerierungswert): `InnerCoverage` . Dies ist ein Bitfeld, bei dem Bit 0 vom LSB für ein bestimmtes konservatives Rasterpixel auf 1 festgelegt ist, nur wenn dieses Pixel garantiert vollständig innerhalb des aktuellen Primitiven liegt. Alle anderen Eingaberegisterbits müssen auf 0 festgelegt werden, wenn Bit 0 nicht festgelegt ist, aber nicht definiert sind, wenn Bit 0 auf 1 festgelegt ist (im Wesentlichen stellt dieses Bitfeld einen booleschen Wert dar, wobei false genau 0 sein muss, true kann jedoch ein ungerader Wert (d. h. bit 0 set) ungleich 0 sein). Diese Eingabe wird für geschätzte konservative Rasterungsinformationen verwendet. Sie informiert den Pixelshader darüber, ob das aktuelle Pixel vollständig innerhalb der Geometrie liegt.

Dies muss ausrichtungsfehler bei Auflösungen berücksichtigen, die größer oder gleich der Auflösung sind, mit der das aktuelle Zeichnen funktioniert. Falsch positive Ergebnisse dürfen nicht vorhanden sein (Festlegen von `InnerCoverage` Bits, wenn das Pixel nicht vollständig für Ausrichtungsfehler bei Auflösungen abgedeckt ist, die größer oder gleich der Auflösung sind, bei der das aktuelle Zeichnen funktioniert), aber falsch negative Ergebnisse sind zulässig. Zusammenfassend lässt sich feststellen, dass die Implementierung Pixel nicht fälschlicherweise als vollständig abgedeckt identifizieren darf, die nicht mit vollständigen Gleitkomma-Scheitelpunktkoordinaten im Rasterizer wären.

Pixel, die vollständig abgedeckt wären, wenn Hardware vollständige Gleitkomma-Scheitelpunktkoordinaten verwendet, können nur weggelassen werden, wenn sie den inneren Unsicherkeitsbereich überschneiden, der nicht größer als die Größe des Subpixelrasters oder 1/256 eines Pixels in der Festkommadomäne sein darf. Anders gesagt: Pixel, die sich vollständig innerhalb der inneren Begrenzung des inneren Unsicherkeitsbereichs befinden, müssen als vollständig abgedeckt gekennzeichnet werden. Die innere Grenze des Unsicherheitsbereichs wird im folgenden Diagramm durch die fette schwarze gepunktete Linie dargestellt. 1/256 stammt aus der Rasterizer-Koordinatendarstellung mit festem Punkt 16,8, die sich ändern kann, wenn sich die Genauigkeit des Rasterizers ändert. Dieser Unsicherkeitsbereich reicht aus, um Ausrichtungsfehler zu berücksichtigen, die durch die Konvertierung von Gleitkomma-Scheitelpunktkoordinaten in Scheitelpunktkoordinaten mit festem Punkt im Rasterizer verursacht werden.

Hier gelten auch die gleichen 1/512-Mindestanforderungen für unsichere Regionen, die in der Interaktion mit Rasterungsregeln definiert sind.

Das folgende Diagramm veranschaulicht einen gültigen inneren Unsicherheitsbereich, der durch Sweeping eines Quadrats um die Ränder des Primitiven in der Festen Punktdomäne erzeugt wird (d. h., die Scheitelpunkte wurden durch die 16.8-Festpunktdarstellung quantisiert). Die Abmessungen dieses Quadrats basieren auf der gültigen Größe des inneren Unschärfebereichs: Für 1/256 eines Pixels beträgt das Quadrat 1/128 pixel in Breite und Höhe. Das grüne Dreieck stellt ein bestimmtes Primitiv dar, die fette schwarze gepunktete Linie stellt die Grenze des inneren Unsicherheitsbereichs dar, die soliden schwarzen Quadrate stellen das Quadrat dar, das entlang der primitiven Ränder geschwenkt wird, und der orange gepunktete Bereich ist der innere Unsicherheitsbereich:

![innerer Unsicherheits-Reqion.](images/innercoverage.jpg)

Die Verwendung von wirkt sich nicht darauf aus, ob ein Pixel konservativ rastert wird, d. h. die Verwendung eines dieser Modi wirkt sich nicht darauf aus, welche Pixel rastert werden, wenn der konservative Rasterungsmodus aktiviert `InnerCoverage` `InputCoverage` ist. Wenn verwendet wird und der Pixel-Shader ein Pixel verarbeitet, das nicht vollständig von der Geometrie abgedeckt ist, ist der Wert daher 0, aber beim Aufruf des Pixels shaders werden die Beispiele `InnerCoverage` aktualisiert. Dies ist anders als , `InputCoverage` wenn 0 ist, was bedeutet, dass keine Beispiele aktualisiert werden.

Diese Eingabe schließen sich gegenseitig mit `InputCoverage` aus: Beide können nicht verwendet werden.

Für den Zugriff auf muss es als einzelne Komponente aus einem der `InnerCoverage` Pixel-Shader-Eingaberegister deklariert werden. Der Interpolationsmodus für die Deklaration muss konstant sein (interpolation does not apply).

Das Bitfeld ist weder von Tiefen-/Schablonentests betroffen, noch wird es mit dem `InnerCoverage` *Status SampleMask* Rasterizer anded.

Diese Eingabe ist nur im konservativen Rasterungsmodus gültig. Wenn die konservative Rasterung nicht aktiviert ist, `InnerCoverage` erzeugt einen nicht definierten Wert.

Bei Pixel-Shaderaufrufen, die durch die Notwendigkeit von Hilfspixeln verursacht werden, andernfalls aber nicht durch den Primitiven abgedeckt werden, muss das Register `InnerCoverage` auf 0 festgelegt sein.

### <a name="attribute-interpolation-interaction"></a>Interaktion mit Attributinterpolation

Die Attributinterpolationsmodi bleiben unverändert und gehen genauso vor wie bei nicht aktivierter konservativer Rasterung, bei der die durch viewportskalierten und festpunktkonverkehrten Scheitelzeichen verwendet werden. Da alle Stichproben in einem konservativ rasterisierten Pixel als abgedeckt betrachtet werden, ist es gültig, dass Werte extrapoliert werden, ähnlich wie bei Verwendung von Pixelfrequenzinterpolationsmodi auf einem **RenderTarget-Objekt** mit einer Stichprobenanzahl größer als 1. Schwerpunktinterpolationsmodi erzeugen Ergebnisse, die mit dem entsprechenden Nicht-Schwerpunktinterpolationsmodus identisch sind. das Konzept des Schwerpunkts ist in diesem Szenario bedeutungslos – bei dem die Beispielabdeckung entweder vollständig oder 0 ist.

Die konservative Rasterung ermöglicht degenerierten Dreiecken, Pixel-Shader-Aufrufe zu erzeugen. Daher müssen degenerierte Dreiecke die Werte verwenden, die Vertex 0 für alle interpolierten Werte zugewiesen sind.

### <a name="clipping-interaction"></a>Clippinginteraktion

Wenn der konservative Rasterungsmodus aktiviert und der Tiefenclip deaktiviert ist (wenn *der DepthClipEnable-Rasterizerzustand* auf FALSE festgelegt ist), gibt es möglicherweise Abweichungen bei der Attributinterpolation für Segmente eines Primitivs, die außerhalb des Bereichs 0 <= z <= w liegen, je nach Implementierung: Entweder werden konstante Werte von einem Punkt aus verwendet, an dem der Primitive die relevante Ebene schneidet (nah oder weit), oder die Attributinterpolation verhält sich wie bei deaktivierter konservativer Rasterung. Das Tiefenwertverhalten ist jedoch unabhängig vom konservativen Rasterungsmodus identisch, d. h., primitiven Typen, die außerhalb des Tiefenbereichs liegen, muss weiterhin der Wert des nächsten Grenzwerts des Viewport-Tiefenbereichs zugewiesen werden. Das Attributinterpolationsverhalten innerhalb des Bereichs 0 <= z <= w muss unverändert bleiben.

### <a name="clip-distance-interaction"></a>Clip Distance-Interaktion

Clip Distance ist gültig, wenn der konservative Rasterungsmodus aktiviert ist, und verhält sich für ein konservativ rasterisiertes Pixel wie bei nicht aktivierter konservativer Rasterung mit allen behandelten Stichproben.

Beachten Sie, dass die konservative Rasterung zu einer Extrapolierung der W-Scheitelpunktkoordinate führen kann, was dazu führen kann, dass W <= 0 ist. Dies kann dazu führen, dass Clip Distance-Implementierungen pro Pixel für einen Clip Distance-Wert verwendet werden, der perspektivisch dividiert durch einen ungültigen W-Wert wurde. Clip Distance-Implementierungen müssen vor dem Aufrufen der Rasterung für Pixel schützen, bei denen die Scheitelpunktkoordinate W <= 0 ist (z. B. aufgrund von Extrapolation im konservativen Rasterisierungsmodus).

### <a name="target-independent-rasterization-interaction"></a>Target Independent Rasterization interaction (Interaktion mit der unabhängigen Zielrasterung)

Der konservative Rasterungsmodus ist kompatibel mit target Independent Rasterization (SOLL). ES GELTEN Regeln und Einschränkungen, die sich für ein konservativ rasteriertes Pixel verhalten, als ob alle Stichproben abgedeckt würden.

### <a name="ia-primitive-topology-interaction"></a>Interaktion der primitiven IA-Topologie

Die konservative Rasterung ist für Linien- oder Punktprimitiven nicht definiert. Daher erzeugen primitive Topologien, die Punkte oder Linien angeben, ein nicht definiertes Verhalten, wenn sie an die Rasterizereinheit gespeist werden, wenn die konservative Rasterung aktiviert ist.

Die Überprüfung der Debugebene überprüft, ob Anwendungen diese primitiven Topologien nicht verwenden.

### <a name="query-interaction"></a>Abfrageinteraktion

Bei einem konservativ rasterisierten Pixel verhalten sich Abfragen wie abfragen, wenn die konservative Rasterung nicht aktiviert ist, wenn alle Stichproben behandelt werden. Für ein konservativ rasterisiertes Pixel müssen sich beispielsweise D3D12 \_ QUERY \_ TYPE \_ OCCLUSION und D3D12 \_ QUERY TYPE PIPELINE STATISTICS \_ \_ \_ (von [**D3D12 \_ QUERY \_ TYPE)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)wie bei einer nicht aktivierten konservativen Rasterung verhalten, wenn alle Stichproben behandelt werden.

Pixel-Shader-Aufrufe sollten für jedes konservativ rasterisierte Pixel im konservativen Rasterungsmodus inkrementiert werden.

### <a name="cull-state-interaction"></a>CULL-Zustandsinteraktion

Alle Cull-Zustände sind im konservativen Rasterungsmodus gültig und befolgen die gleichen Regeln wie, wenn die konservative Rasterung nicht aktiviert ist.

Beim Vergleich der konservativen Rasterung über Auflösungen hinweg mit sich selbst oder ohne aktivierte konservative Rasterung besteht die Möglichkeit, dass einige Primitive nicht übereinstimmende Gegenüberheit haben (d. h. eine hintere Seite, die andere nach vorne). Anwendungen können diese Unsicherheit vermeiden, indem sie D3D12 \_ CULL \_ MODE NONE \_ (aus dem [**D3D12 \_ \_ CULL-MODUS)**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)und nicht den `IsFrontFace` vom System generierten Wert verwenden.

### <a name="isfrontface-interaction"></a>IsFrontFace-Interaktion

Der vom System generierte Wert ist für die Verwendung im konservativen Rasterungsmodus gültig und folgt dem Verhalten, das definiert ist, wenn die konservative `IsFrontFace` Rasterung nicht aktiviert ist.

### <a name="fill-modes-interaction"></a>Interaktion mit Füllmodi

Der einzige gültige [**D3D12 \_ \_ FILL-MODUS**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) für die konservative Rasterung ist D3D12 FILL SOLID. Jeder andere Füllmodus ist ein ungültiger Parameter für den \_ \_ Rasterizerzustand.

Dies liegt daran, dass die D3D12-Funktionsspezifikation angibt, dass der Wireframe-Füllmodus Dreiecksränder in Linien konvertieren und den Linienrasterregeln folgen und das verhalten der konservativen Linienrasterung nicht definiert wurde.

## <a name="implementation-details"></a>Details zur Implementierung

Der in Direct3D 12 unterstützte Rasterungstyp wird manchmal als "Überschätzung der konservativen Rasterung" bezeichnet. Es gibt auch das Konzept der "konservativ-konservativen Rasterung", was bedeutet, dass nur Pixel, die vollständig von einem gerenderten Primitiv abgedeckt sind, rasterisiert werden. Über den Pixel-Shader sind über Eingabeabdeckungsdaten nicht über die konservative Rasterung informationen verfügbar, und nur die überschätzte konservative Rasterung ist als Rastermodus verfügbar.

Wenn ein Teil eines Primitiven ein Pixel überlappt, wird dieses Pixel als abgedeckt betrachtet und dann rastert. Wenn ein Rand oder eine Ecke eines Primitivs entlang der Kante oder Ecke eines Pixels fällt, ist die Anwendung der "regel oben links" implementierungsspezifisch. Für Implementierungen, die degenerierte Dreiecke unterstützen, muss ein degeneriertes Dreieck entlang einer Kante oder Ecke jedoch mindestens ein Pixel abdecken.

Konservative Rasterisierungsimplementierungsimplementierungen können auf unterschiedlicher Hardware variieren und falsch positive Ergebnisse erzeugen, was bedeutet, dass sie fälschlicherweise entscheiden können, dass Pixel abgedeckt sind. Dies kann aufgrund von implementierungsspezifischen Details auftreten, z. B. primitivem Wachstum oder Ausrichtungsfehlern, die in den bei der Rasterung verwendeten Scheitelpunktkoordinaten mit festem Punkt auftreten. Falsch positive Ergebnisse (in Bezug auf Punkt-Scheitelpunktkoordinaten) sind gültig, da einige falsch positive Ergebnisse erforderlich sind, damit eine Implementierung eine Abdeckungsauswertung für nachgestellte Scheitelpunkte (d. h. Scheitelpunktkoordinaten, die von Gleitkommakoordinaten in den im Rasterizer verwendeten 16.8-Fixpunkt konvertiert wurden) ermöglicht, aber die abdeckungsbasierte Abdeckung der ursprünglichen Gleitkommavertexkoordinaten beachtet.

Konservative Rasterungsimplementierungsimplementierungen erzeugen keine falsch negativen Ergebnisse in Bezug auf die Gleitkomma-Scheitelpunktkoordinaten für nicht degenerierte Primitive nach dem Andocken: Wenn ein Teil eines primitiv einen beliebigen Teil eines Pixels überlappt, wird dieses Pixel rasterisiert.

Dreiecke, die degeneriert sind (doppelte Indizes in einem Indexpuffer oder collinear in 3D) oder nach der Konvertierung mit festem Punkt (collineare Vertices im Rasterizer) degeneriert werden, können gecullt werden. beide sind gültige Verhaltensweisen. Degenerierte Dreiecke müssen als zurückgesichtet betrachtet werden. Wenn also ein bestimmtes Verhalten für eine Anwendung erforderlich ist, kann sie das Back-Face-Culling verwenden oder für die Vorderseite testen. Degenerierte Dreiecke verwenden die Werte, die Vertex 0 für alle interpolierten Werte zugewiesen sind.

Zusätzlich zur Möglichkeit, dass die Hardware dieses Feature nicht unterstützt, gibt es drei Ebenen der Hardwareunterstützung.

-   Ebene 1 erzwingt einen maximal 1/2 Pixel großen Unklarheitsbereich und unterstützt keine Degeneriert nach dem Andocken. Dies ist gut für gekacheltes Rendering, einen Texturatlas, die Generierung von Lichtkarten und Schattenkarten mit Unterpixeln.
-   Ebene 2 reduziert die maximale Unsicherheitsregion auf 1/256 und erfordert, dass nach dem Snap-Andocken keine Degenerierte gecullt werden. Diese Ebene ist für die CPU-basierte Algorithmusbeschleunigung (z. B. Voxelisierung) hilfreich.
-   Ebene 3 verwaltet eine maximal 1/256 Unsicherheitsregion und fügt Unterstützung für die innere Eingabeabdeckung hinzu. Die innere Eingabeabdeckung fügt den neuen Wert `SV_InnerCoverage` der High Level Shading Language (HLSL) hinzu. Dies ist eine 32-Bit-Skalar-Ganzzahl, die bei der Eingabe in einen Pixel-Shader angegeben werden kann und die unterschätzenden Informationen zur konservativen Rasterung darstellt (d. h., ob ein Pixel garantiert vollständig abgedeckt ist). Diese Ebene ist für das Verdecken von Culling hilfreich.

## <a name="api-summary"></a>API-Zusammenfassung

Die folgenden Methoden, Strukturen, Enums und Hilfsklassen verweisen auf die konservative Rasterung:

-   [**D3D12 \_ RASTERIZER \_ DESC:**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) Struktur mit der Beschreibung des Rasterizers.
-   [**D3D12 \_ \_KONSERVATIVER \_ RASTERISIERUNGSMODUS:**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) Aufzählwerte für den Modus (ein oder aus).
-   [**D3D12 \_ FEATURE \_ DATA \_ D3D12 \_ OPTIONS**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : Struktur, die die Unterstützungsebene auf hält.
-   [**D3D12 \_ CONSERVATIVE \_ RASTERIZATION \_ TIER**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier) : enum values for each tier of support by the hardware.
-   [**CheckFeatureSupport:**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) Methode für den Zugriff auf die unterstützten Features.
-   [**CD3DX12 \_ RASTERIZER \_ DESC:**](cd3dx12-rasterizer-desc.md) Hilfsklasse zum Erstellen von Rasterizerbeschreibungen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videotutorials für erweitertes Lernen mit DirectX: Konservative Rasterung](https://www.youtube.com/watch?v=zL0oSY_YmDY)
</dt> <dt>

[Geordnete Rasterizeransichten](rasterizer-order-views.md)
</dt> <dt>

[Rendering](rendering.md)
</dt> </dl>

 

 




