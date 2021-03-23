---
title: Direct3D 12 konservative rasterisierung
description: Die konservative rasterisierung sorgt für ein gewisses Maß an Sicherheit für das Pixel Rendering. Dies ist insbesondere bei Algorithmen zum Erkennen von Kollisionen hilfreich.
ms.assetid: 081199AD-1702-4EC8-95AD-B1148C676199
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e4fae3489d54ab7b6b7abfda56f54dd8d970962
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "104548755"
---
# <a name="direct3d-12-conservative-rasterization"></a>Direct3D 12 konservative rasterisierung

Die konservative rasterisierung sorgt für ein gewisses Maß an Sicherheit für das Pixel Rendering. Dies ist insbesondere bei Algorithmen zum Erkennen von Kollisionen hilfreich.

-   [Übersicht](#overview)
-   [Interaktionen mit der Pipeline](#interactions-with-the-pipeline)
    -   [Interaktion von rasterisierungsregeln](#rasterization-rules-interaction)
    -   [Multisampling-Interaktion](#multisampling-interaction)
    -   [Samplemask-Interaktion](#samplemask-interaction)
    -   [Interaktion mit tiefen/Schablone testen](#depthstencil-test-interaction)
    -   [Hilfspixel Interaktion](#helper-pixel-interaction)
    -   [Interaktion bei der Ausgabe Abdeckung](#output-coverage-interaction)
    -   [Inputcoverage-Interaktion](#inputcoverage-interaction)
    -   [Innercoverage-Interaktion](#innercoverage-interaction)
    -   [Interaktion mit Attribut Interpolations](#attribute-interpolation-interaction)
    -   [Clipping-Interaktion](#clipping-interaction)
    -   [Interaktion bei Clip Distanz](#clip-distance-interaction)
    -   [Ziel unabhängige rasterisierungsinteraktion](#target-independent-rasterization-interaction)
    -   [Interaktion mit primitiver Topologie](#ia-primitive-topology-interaction)
    -   [Abfrage Interaktion](#query-interaction)
    -   [Interaktionsinteraktion](#cull-state-interaction)
    -   [Isfrontface-Interaktion](#isfrontface-interaction)
    -   [Interaktion mit Füll Modi](#fill-modes-interaction)
-   [Implementierungsdetails](#implementation-details)
-   [API-Zusammenfassung](#api-summary)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Überblick

Die konservative rasterisierung bedeutet, dass alle Pixel, die zumindest teilweise von einem gerenderten primitiven abgedeckt werden, rasterisiert sind. Dies bedeutet, dass der Pixelshader aufgerufen wird. Normales Verhalten ist die Stichprobenentnahme, die nicht verwendet wird, wenn die konservative rasterisierung aktiviert ist.

Die konservative rasterisierung ist in einer Reihe von Situationen nützlich, einschließlich der Sicherheit bei der Konflikterkennung, der Okklusions Erkennung und des gekachelten Rendering.

Die folgende Abbildung zeigt z. b. ein grünes Dreieck, das mit konservativer rasterisierung gerendert wird, wie es im Raster (mit 16,8-Scheitelpunkt Koordinaten mit festem Punkt) angezeigt würde. Der braune Bereich wird als "Ungewissheit-Region" bezeichnet. Dies ist ein konzeptioneller Bereich, der die erweiterten Begrenzungen des Dreiecks darstellt. Dies ist erforderlich, um sicherzustellen, dass der primitive im Raster in Bezug auf die ursprünglichen Gleit Komma Koordinaten des Vertex konservativ ist. Die roten Quadrate in den einzelnen Scheitel Punkten zeigen, wie der unsicher-Bereich berechnet wird: als ein gesweep Quadrat.

Die großen grauen Quadrate zeigen die Pixel an, die gerendert werden. In den rosa Quadraten werden Pixel angezeigt, die mit der "Top-Left"-Regel gerendert werden. diese wird wiedergegeben, wenn der Rand des Dreiecks den Rand der Pixel überschreitet. Es können falsch positive Ergebnisse (Pixel festgelegt werden, die nicht vorhanden sein sollten) sein, die das System normalerweise aber nicht immer umschlägt.

![die linke obere Regel](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interaktionen mit der Pipeline

### <a name="rasterization-rules-interaction"></a>Interaktion von rasterisierungsregeln

Im konservativen rasterisierungsmodus gelten rasterisierungsregeln genauso wie, wenn der konservative rasterisierungsmodus nicht mit Ausnahmen für die Top-Left Regel, wie oben beschrieben, und Pixel Abdeckung aktiviert ist. 16,8 Fixed-Point Genauigkeit für den Rasterizer muss verwendet werden.

Pixel, die nicht abgedeckt werden, wenn die Hardware vollständige Gleit Komma Koordinaten verwendet, kann nur eingeschlossen werden, wenn Sie sich innerhalb eines unsicheren Bereichs befinden, der nicht größer als ein Pixel in der fest Komma Domäne ist. Zukünftige Hardware geht davon aus, dass die in Ebene 2 angegebene verschärfte Unsicherheit erreicht werden soll. Beachten Sie, dass diese Anforderung verhindert, dass Farbname Dreiecke weiter als erforderlich erweitert werden.

Ein ähnlicher gültiger Bereich für Ungewissheit gilt `InnerCoverage` auch für, aber es ist strenger, da keine Implementierungen in diesem Fall einen größeren unsicheren Bereich erfordern. Weitere Details finden Sie unter [innercoverage-Interaktion](#innercoverage-interaction) .

Innere und äußere Ungleichheits Bereiche müssen größer oder gleich der Größe der Hälfte des unter-Pixel-Rasters oder 1/512 eines Pixels in der Fixed-Point-Domäne sein. Dies ist der minimale gültige unsicherungsbereich. 1/512 stammt aus der Koordinaten Darstellung von 16,8 Fixed Point Rasterizer und der roundTo-Next-Regel, die angewendet wird, wenn Gleit Komma-Scheitelpunkt Koordinaten in 16,8 festgelegte Punkt Koordinaten umgeschrieben werden. 1/512 kann sich ändern, wenn die Genauigkeit des Rasterizers geändert wird. Wenn eine Implementierung diesen minimalen unsicheren Bereich implementiert, müssen Sie der Top-Left Regel folgen, wenn ein Rand oder eine Ecke des unsicheren Bereichs an der Kante oder Ecke eines Pixels liegt. Die ausgeschnittenen Kanten des unsicheren Bereichs sollten als nächster Scheitelpunkt behandelt werden, was bedeutet, dass Sie als zwei Ränder gezählt werden: die beiden, die am zugeordneten Scheitelpunkt beitreten. Top-Left Regel ist erforderlich, wenn der Bereich für die minimale Ungewissheit verwendet wird. ist dies nicht der Fall, würde eine konservative rasterization-Implementierung die Pixel, die abgedeckt werden können, wenn der konservative rasterisierungsmodus deaktiviert ist, nicht Rasterisieren.

Im folgenden Diagramm wird ein gültiger äußerer unsicher dargestellt, der durch das Durchlaufen eines Quadrats um die Ränder des primitiven in der Fixed-Point-Domäne erzeugt wird (d. h., die Scheitel Punkte wurden mit der 16,8-fest Komma Darstellung quantifisiert). Die Abmessungen dieses Quadrats basieren auf der gültigen Regions Größe für äußere Ungewissheit: für 1/2 eines Pixels beträgt das Quadrat 1 Pixel in Breite und Höhe, bei 1/512 eines Pixels ist das Quadrat 1/256 eines Pixels in Breite und Höhe. Das grüne Dreieck stellt ein bestimmtes primitiv dar, die rote gepunktete Linie stellt die Grenze für die überschätzte konservative rasterisierung dar, die schwarzen Quadrate stellen das Quadrat dar, das entlang der primitiven Ränder gezogen wird, und der blaue aktivierte Bereich ist der äußere unsicher-Bereich:

![äußerer unsicheren Bereich.](images/outercoverage.jpg)

### <a name="multisampling-interaction"></a>Multisampling-Interaktion

Unabhängig von der Anzahl von Beispielen in **renderTarget** / **depthstencil** -Oberflächen (bzw. unabhängig davon, ob *forcedsamplecount* verwendet wird oder nicht) werden alle Beispiele für Pixel behandelt, die durch die konservative rasterisierung gerengt werden. Einzelne Beispiel Speicherorte werden nicht darauf getestet, ob Sie in den primitiven oder nicht.

### <a name="samplemask-interaction"></a>Samplemask-Interaktion

Der Zustand des *samplemask* -Rasterizers wird auf dieselbe Weise angewendet, als wenn die konservative rasterisierung nicht aktiviert ist `InputCoverage` , aber keine Auswirkung hat `InnerCoverage` (d. h. er wird nicht in eine mit deklarierte Eingabe umgewandelt `InnerCoverage` ). Dies liegt daran, `InnerCoverage` dass nicht mit der Maskierung von MSAA-Beispielen in Beziehung steht: "0" `InnerCoverage` bedeutet nur, dass das Pixel nicht vollständig abgedeckt ist und keine Beispiele aktualisiert werden.

### <a name="depthstencil-test-interaction"></a>Interaktion mit tiefen/Schablone testen

Das Testen der Tiefe/Schablone verläuft für ein konservatives rasterisiertes Pixel auf dieselbe Weise, als wenn alle Stichproben behandelt werden, wenn die konservative rasterisierung nicht aktiviert ist.

Wenn Sie mit allen behandelten Beispielen fortfahren, kann dies zu einer tiefen Extrapolierung führen, die gültig ist und wie angegeben an den Viewport gebunden werden muss, wenn die konservative rasterisierung nicht aktiviert ist. Dies ist vergleichbar mit der Verwendung von Pixelfrequenz-Interpolations Modi für ein **renderTarget** mit einer Stichproben Anzahl von mehr als 1. im Fall von konservativer rasterisierung ist es jedoch der tiefen Wert, der in den tiefen Test für die festgelegte Funktion geht, der extrapoliert werden kann.

Das frühe tiefen kulationsverhalten bei tiefen extrapolierungsverhalten ist nicht definiert. Dies ist darauf zurückzuführen, dass einige frühesnapskationshardware die extrapolierten tiefen Werte nicht unterstützen kann Allerdings ist das frühe Verhalten bei der Tiefe der tiefen extrapolierungsverhalten auch bei Hardware, die extrapolierte tiefen Werte unterstützen kann, problematisch. Dieses Problem kann umgangen werden, indem die Pixel-Shader-Eingabe Tiefe auf die minimalen und maximalen tiefen Werte des primitiven, das gerachtelert wird, und das Schreiben dieses Werts in `oDepth` (das Pixel-Shader-Ausgabe tiefen Register) geklammert wird. Zum Deaktivieren der frühen tiefen Erstellung in diesem Fall sind Implementierungen aufgrund des Schreibzugriffs erforderlich `oDepth` .

### <a name="helper-pixel-interaction"></a>Hilfspixel Interaktion

Hilfspixel Regeln gelten genauso wie bei nicht aktivierter konservativer rasterisierung. Im Rahmen dieser Angabe müssen alle Pixel, einschließlich `InputCoverage` der Hilfsskripts, genau wie im `InputCoverage` Interaktions Abschnitt angegeben Berichten. Die Abdeckung für vollständig nicht abgedeckte Pixel Report 0.

### <a name="output-coverage-interaction"></a>Interaktion bei der Ausgabe Abdeckung

Die Ausgabe Abdeckung ( `oMask` ) verhält sich für ein konrechtes geändertes Pixel, wie dies geschieht, wenn die konservative rasterisierung nicht mit allen behandelten Beispielen aktiviert ist.

### <a name="inputcoverage-interaction"></a>Inputcoverage-Interaktion

Im Modus für die konservative rasterisierung wird dieses Eingabe Register aufgefüllt, als ob alle Stichproben abgedeckt werden, wenn die konservative rasterisierung nicht für ein bestimmtes, Geheimnis geändertes Pixel aktiviert ist. Das heißt, dass alle vorhandenen Interaktionen zutreffen (z. b. *samplemask* ), und die ersten n-Bits in `InputCoverage` aus dem lsb werden für ein Modell mit einer geheimnisvollen Schleife auf 1 festgelegt. dabei wird ein n-Beispiel pro Pixel **renderTarget** und/oder **depthstencil** -Puffer, das bei der **Ausgabe** Zusammenführung gebunden ist, bzw Der Rest der Bits ist 0 (null).

Diese Eingabe ist unabhängig von der Verwendung der konservativen rasterisierung in einem Shader verfügbar, obwohl die konservative rasterisierung das Verhalten ändert, sodass nur alle Abtastungen angezeigt werden (oder keine für hilfspixel).

### <a name="innercoverage-interaction"></a>Innercoverage-Interaktion

Diese Funktion ist für und nur in, Ebene 3, erforderlich. Die Laufzeit schlägt die Shader-Erstellung für Shader fehl, die diesen Modus verwenden, wenn eine Implementierung eine Ebene unterstützt, die kleiner als Ebene 3 ist.

Der Pixelshader verfügt über einen 32-Bit-Skalarwert für einen Skalarwert mit skalarem System `InnerCoverage` . Dabei handelt es sich um ein Bitfeld, das Bit 0 vom lsb auf 1 festgelegt ist, und zwar nur dann, wenn das Pixel sicher vollständig innerhalb des aktuellen primitiven liegt. Alle anderen Eingabe Register Bits müssen auf 0 festgelegt werden, wenn Bit 0 nicht festgelegt ist. Sie sind jedoch nicht definiert, wenn Bit 0 auf 1 festgelegt ist (im Grunde stellt dieses Bitfeld einen booleschen Wert dar, bei dem false genau 0 sein muss. true kann jedoch ein beliebiger Wert (d. h. Bit 0 Set) sein, der ungleich NULL ist. Diese Eingabe wird für unterschätzte konservative rasterisierungsinformationen verwendet. Er informiert den Pixelshader darüber, ob das aktuelle Pixel vollständig innerhalb der Geometrie liegt.

Dabei muss ein Ausrichtungsfehler bei Auflösungen auftreten, der größer oder gleich der Auflösung ist, in der die aktuelle Zeichnung ausgeführt wird. Es dürfen keine falsch positiven Ergebnisse auftreten (legen Sie `InnerCoverage` Bits fest, wenn das Pixel nicht vollständig für einen Ausrichtungsfehler bei Auflösungen, die größer oder gleich der Auflösung sind, bei der der aktuelle Zeichnen ausgeführt wird, nicht vollständig abgedeckt ist), aber es sind falsche Negative Werte zulässig. Zusammenfassend lässt sich sagen, dass die-Implementierung Pixel nicht fälschlicherweise als vollständig abgedeckte kennzeichnen muss, die nicht mit vollständigen Gleit Komma Koordinaten im Rasterizer zu tun haben.

Pixel, die vollständig abgedeckt werden, wenn die Hardware vollständige Gleit Komma Koordinaten verwendet, darf nur ausgelassen werden, wenn Sie den inneren unsicheren Bereich überschneiden, der nicht größer als die Größe des unter-Pixel-Rasters oder 1/256 eines Pixels in der Fixed-Point-Domäne sein muss. Anders gesagt: Pixel, die sich vollständig innerhalb der inneren Grenze des inneren unsicheren Bereichs befinden, müssen als vollständig abgedeckt gekennzeichnet werden. Die innere Begrenzung des unsicheren Bereichs wird in der Abbildung unten durch die rote gepunktete Linie dargestellt. 1/256 stammt aus der Koordinaten Darstellung von 16,8 Fixed Point Rasterizer, die sich ändern kann, wenn die Genauigkeit des Rasterizers geändert wird. Diese unsicheren Region ist ausreichend, um den Ausrichtungsfehler zu berücksichtigen, der durch die Konvertierung von Vertex-Gleit Komma Koordinaten in die Scheitelpunkt Koordinaten des Rasterizers verursacht wurde.

Die gleichen 1/512-Mindestanforderungen hinsichtlich der Ungewissheit, die bei der Interaktion mit der rasterisierungsregeln definiert sind, gelten auch hier.

Das folgende Diagramm veranschaulicht einen gültigen inneren unsicheren Bereich, der durch das Durchlaufen eines Quadrats um die Ränder des primitiven in der Fixed-Point-Domäne erzeugt wird (d. h., die Scheitel Punkte wurden mit der 16,8-fest Komma Darstellung quantifisiert). Die Abmessungen dieses Quadrats basieren auf der gültigen Regions Größe für die innere Ungewissheit: für 1/256 eines Pixels ist das Quadrat 1/128 eines Pixels in Breite und Höhe. Das grüne Dreieck stellt ein bestimmtes primitiv dar, die fettrote gepunktete Linie stellt die Grenze des inneren unsicheren Bereichs dar, die schwarzen Quadrate stellen das Quadrat dar, das entlang der primitiven Ränder gezogen wird, und der Orange aktivierte Bereich ist der innere unsicher-Bereich:

![reqion der inneren Ungewissheit.](images/innercoverage.jpg)

Die Verwendung von wirkt sich nicht darauf aus `InnerCoverage` , ob ein Pixel konservativ rasteriert ist, d. h., die Verwendung eines dieser Modi wirkt sich nicht darauf aus, `InputCoverage` welche Pixel gerengt werden, wenn der konservative rasterisierungsmodus aktiviert ist. Wenn `InnerCoverage` verwendet wird und der Pixelshader ein Pixel verarbeitet, das von der Geometrie nicht vollständig abgedeckt ist, ist der Wert 0, aber für den Pixelshader-Aufruf werden Beispiele aktualisiert. Dies unterscheidet sich von, wenn 0 (null) `InputCoverage` ist, was bedeutet, dass keine Beispiele aktualisiert werden.

Diese Eingabe schließt sich gegenseitig aus `InputCoverage` : beide können nicht verwendet werden.

Für den Zugriff auf `InnerCoverage` muss Sie als einzelne Komponente aus einem der Pixel-Shader-Eingabe Register deklariert werden. Der Interpolations Modus für die Deklaration muss konstant sein (Interpolation ist nicht anwendbar).

Das `InnerCoverage` Bitfeld wirkt sich nicht auf tiefen-und Schablonen Tests aus, und es ist nicht mit dem *samplemask* -Rasterizer-Zustand verknüpft.

Diese Eingabe ist nur im konservativen rasterisierungsmodus gültig. Wenn die konservative rasterisierung nicht aktiviert ist, `InnerCoverage` erzeugt einen nicht definierten Wert.

Bei Pixeln-Shader-aufrufen, die durch die Notwendigkeit von Hilfsskripts verursacht werden, aber andernfalls nicht durch die primitive abgedeckt werden, muss das `InnerCoverage` Register auf 0 festgelegt sein.

### <a name="attribute-interpolation-interaction"></a>Interaktion mit Attribut Interpolations

Die Attribut Interpolations Modi sind unverändert und werden auf dieselbe Weise fortgesetzt, wenn die konservative rasterisierung nicht aktiviert ist, in der die mit Viewports skalierten und mit einem Punkt konvertierten Vertices verwendet werden. Da alle Beispiele in einem konservativ erfassten Pixel als abgedeckt angesehen werden, ist es für Werte gültig, die extrapoliert werden, ähnlich wie bei Verwendung von Pixel-Frequency-Interpolations Modi für ein **renderTarget** mit einer Stichproben Anzahl von mehr als 1. Centroid-Interpolations Modi liefern Ergebnisse, die mit dem entsprechenden nicht-Centroid-Interpolations Modus identisch sind. Das Konzept von "Schwerpunkt" ist in diesem Szenario bedeutungslos – wobei die Stichproben Abdeckung nur "Full" oder "0" ist.

Durch die konservative rasterisierung können degenerierte Dreiecke zum Generieren von PixelShader-Aufrufen verwendet werden. Daher müssen degenerierte Dreiecke die Werte, die Vertex 0 zugewiesen sind, für alle interinterpolierten Werte verwenden.

### <a name="clipping-interaction"></a>Clipping-Interaktion

Wenn der konservative rasterisierungsmodus aktiviert und der tiefen Clip deaktiviert ist (wenn der Status des *depthcliutable* -Rasterizers auf false festgelegt ist), es gibt möglicherweise Abweichungen in der Attribut Interpolation für Segmente eines primitiven, die außerhalb des Bereichs 0 <= z <= w liegen, abhängig von der Implementierung: entweder werden Konstante Werte von einem Punkt verwendet, an dem die primitive die relevante Ebene (fast oder weit) überschneidet, oder die Attribut Interpolation verhält sich so, als wäre der konservative rasterisierungsmodus deaktiviert. Allerdings ist das Verhalten des tiefen Werts unabhängig vom Modus für die konservative rasterisierung identisch, d. h., dass primitive, die außerhalb des tiefen Bereichs liegen, immer noch den Wert des nächsten Limits für den Bereich der viewporttiefe erhalten müssen. Das Attribut Interpolations Verhalten im Bereich 0 <= z <= w muss unverändert bleiben.

### <a name="clip-distance-interaction"></a>Interaktion bei Clip Distanz

Die Clip-Distanz ist gültig, wenn der konservative rasterisierungsmodus aktiviert ist, und sich für ein konkales rasterisiertes Pixel verhält, wie es der Fall ist, wenn die konservative rasterisierung nicht mit allen behandelten Beispielen aktiviert ist.

Beachten Sie, dass die konservative rasterisierung eine Extrapolierung der w-Scheitelpunkt Koordinate verursachen kann, was zu einer w <= 0 führen kann. Dies könnte dazu führen, dass pro-Pixel-Clip Entfernungs Implementierungen auf eine Clip Distanz angewendet werden, die durch einen ungültigen W-Wert geteilt wurde. Clip Entfernungs Implementierungen müssen vor dem Aufruf von Rasterung für Pixel stehen, bei denen die Vertex-Koordinate <= 0 (z. b. aufgrund der Extrapolierung im Modus für die konservative rasterisierung).

### <a name="target-independent-rasterization-interaction"></a>Ziel unabhängige rasterisierungsinteraktion

Der konservative rasterisierungsmodus ist mit der Ziel unabhängigen rasterization (TIR) kompatibel. Es gelten die TIR-Regeln und-Einschränkungen, die sich für ein konservatives rasterisiertes Pixel Verhalten, als ob alle Stichproben abgedeckt werden.

### <a name="ia-primitive-topology-interaction"></a>Interaktion mit primitiver Topologie

Die konservative rasterisierung ist für Zeilen-oder Punkt primitiven nicht definiert. Daher wird durch primitive Topologien, die Punkte oder Zeilen angeben, ein nicht definiertes Verhalten erzeugt, wenn Sie in die Raster-Einheit eingespeist werden, wenn die konservative rasterisierung aktiviert ist.

Die debugebenenvalidierung überprüft, ob Anwendungen diese primitiven Topologien nicht verwenden.

### <a name="query-interaction"></a>Abfrage Interaktion

Für ein konformisch Erfassungs Endes Pixel Verhalten sich die Abfragen so, wie Sie es tun, wenn die konservative rasterisierung nicht aktiviert ist, wenn alle Stichproben abgedeckt werden. Beispielsweise müssen Sie für ein konformes rasterisiertes Pixel das D3D12 \_ \_ \_ -Abfragetyp-oksion und den D3D12- \_ \_ \_ Abfragetyp Pipeline \_ Statistiken (aus [**D3D12- \_ Abfragetyp \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_query_type)) so Verhalten, als würden die konservative rasterisierung nicht aktiviert, wenn alle Stichproben abgedeckt werden.

Pixel-Shader-Aufrufe sollten für jedes im konservativ aufgeblenierte Pixel im konservativen rasterisierungsmodus erhöht werden.

### <a name="cull-state-interaction"></a>Interaktionsinteraktion

Alle Statusangaben sind im Modus für die konservative rasterisierung gültig und befolgen dieselben Regeln wie bei aktivierter konservativer rasterisierung.

Wenn Sie die konservative rasterisierung über Auflösungen mit sich selbst oder ohne die konservative rasterisierung hinweg vergleichen, besteht die Möglichkeit, dass einige primitive eine nicht übereinstimmende faktigkeit aufweisen (d. h. ein Back-End, die andere Vorderseite). Anwendungen können diese Ungewissheit vermeiden, indem Sie D3D12 \_ cull \_ Mode \_ None (aus dem [**D3D12 \_ cull- \_ Modus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_cull_mode)) verwenden und nicht den vom `IsFrontFace` System generierten Wert verwenden.

### <a name="isfrontface-interaction"></a>Isfrontface-Interaktion

Der vom `IsFrontFace` System generierte Wert ist für die Verwendung im konservativen rasterisierungsmodus gültig und folgt dem Verhalten, das definiert ist, wenn die konservative rasterisierung nicht aktiviert ist.

### <a name="fill-modes-interaction"></a>Interaktion mit Füll Modi

Der einzige gültige [**D3D12 \_ - \_ Füllmodus**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_fill_mode) für die konservative rasterisierung ist D3D12 \_ Fill \_ Solid, jeder andere Füll Modus ist ein ungültiger Parameter für den Status des Rasterizers.

Dies liegt daran, dass die D3D12-Funktionsspezifikation angibt, dass der Draht Modell-Füllmodus Dreiecks Ränder in Linien konvertieren und die zeilenrasterisierungsregeln und das Verhalten der konservativen Zeilen rasterisierung nicht definiert wurde.

## <a name="implementation-details"></a>Details zur Implementierung

Der Typ der in Direct3D 12 unterstützten rasterisierung wird manchmal als "überschätzte konservative rasterisierung" bezeichnet. Es gibt auch das Konzept der "unterschätzten konservative rasterisierung", was bedeutet, dass nur Pixel, die vollständig von einem gerenderten primitiven abgedeckt werden, rasterisiert werden. Unterschätzte konservative rasterisierungsinformationen sind über den Pixelshader durch die Verwendung von Eingabe Abdeckungs Daten verfügbar, und nur die überschätzte konservative rasterisierung ist als rasterisierungsmodus verfügbar.

Wenn ein beliebiger Teil eines primitiven ein Pixel überlappt, wird dieses Pixel als abgedeckt betrachtet und dann rasteriert. Wenn ein Rand oder eine Ecke eines primitiven entlang der Kante oder Ecke eines Pixels fällt, ist die Anwendung der "Top-Left-Regel" Implementierungs spezifisch. Bei Implementierungen, die degenerierte Dreiecke unterstützen, muss ein degeneriertes Dreieck an einer Kante oder Ecke jedoch mindestens ein Pixel abdecken.

Konservative rasterization-Implementierungen können sich auf unterschiedlichen Hardware unterscheiden, und es werden falsche positiv Ergebnisse erzeugt. Dies bedeutet, dass Sie fälschlicherweise festlegen können, dass Pixel abgedeckt werden. Dies kann aufgrund von Implementierungs spezifischen Details auftreten, wie z. b. primitive ansteigende oder Ausrichtungsfehler, die in den in der rasterisierung verwendeten festen Punkt Vertex-Koordinaten enthalten sind. Der Grund, warum falsch positive Ergebnisse (in Bezug auf Scheitelpunkt Koordinaten mit festem Punkt) gültig sind, liegt darin, dass einige falsch positive Ergebnisse erforderlich sind, damit eine Implementierung die Abdeckungs Auswertung für nach gestellte Scheitel Punkte (d. h. vertexkoordinaten, die von Gleit Komma Zahlen in den in der Rasterizer verwendeten Fixed-Punkt 16,8 konvertiert wurden, berücksichtigen jedoch die Abdeckung, die von den ursprünglichen Gleit Komma Koordinaten des Vertex erzeugt wurde.

Konservative rasterization-Implementierungen generieren keine falschen negativen in Bezug auf die Vertex-Gleit Komma Koordinaten für nicht degenerierte Post-Snap-primitive: Wenn ein beliebiger Teil eines primitiven einen Teil eines Pixels überlappt, wird dieses Pixel rasteriert.

Dreiecke, die deseriell sind (doppelte Indizes in einem Index Puffer oder kollinear in 3D) oder nach der fest Komma Konvertierung (kollinear Vertices in the Rasterizer) deseriell werden. Beide sind ein gültiges Verhalten. Degenerierte Dreiecke müssen als "zurück" betrachtet werden. Wenn also ein bestimmtes Verhalten für eine Anwendung erforderlich ist, kann es die Hintergrund Erkennung oder den Test für die Vorderseite verwenden. Degenerierte Dreiecke verwenden die den Scheitel Punkten 0 zugewiesenen Werte für alle interpoliert-Werte.

Es gibt drei Ebenen von Hardwareunterstützung, zusätzlich zur Möglichkeit, dass die Hardware dieses Feature nicht unterstützt.

-   Ebene 1 erzwingt einen maximalen Bereich von 1/2 Pixel Unsicherheit und unterstützt nicht die Post-Snap-Degenerierung. Dies eignet sich gut für das gekachelte Rendering, einen Textur Atlas, eine Licht Zuordnungs Generierung und unter Pixel Schatten Zuordnungen.
-   Ebene 2 reduziert den Bereich für die maximale Anzahl von Unsicherheiten auf 1/256 und erfordert, dass Post-Snap-Ins nicht durchgeführt werden. Diese Ebene ist für die CPU-basierte Beschleunigung der Algorithmen (z. b. voxelization) hilfreich.
-   Ebene 3 behält einen maximalen Bereich von 1/256-Unsicherheiten bei und bietet Unterstützung für die innere Eingabe Abdeckung. Die innere Eingabe Abdeckung fügt den neuen Wert der `SV_InnerCoverage` High Level Shading Language (HLSL) hinzu. Dies ist eine ganzzahlige 32-Bit-Ganzzahl, die für die Eingabe an einen PixelShader angegeben werden kann, und stellt die unterschätzten Informationen zur konservativen rasterisierung dar (d. h., ob ein Pixel garantiert vollständig abgedeckt ist). Diese Ebene ist für die Verschleierung von Okklusion hilfreich.

## <a name="api-summary"></a>API-Zusammenfassung

Die folgenden Methoden, Strukturen, Enumerationsklassen und Hilfsklassen verweisen auf die konservative rasterisierung:

-   [**D3D12 \_ Raster \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_rasterizer_desc) -Debug: Struktur mit der Beschreibung des Rasterizers.
-   [**D3D12 \_ Konservativer \_ rasterisierungsmodus \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_mode) : Enumeration-Werte für den Modus (ein oder aus).
-   [**D3D12 \_ Feature \_ Data \_ D3D12 \_ Optionen**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_feature_data_d3d12_options) : Struktur, die die Ebene der Unterstützung enthält.
-   [**D3D12 \_ Konservative \_ rasterization- \_ Ebene**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_conservative_rasterization_tier) : Enumerationswerte für jede Ebene der Unterstützung durch die Hardware.
-   [**Checkfeaturesupport**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport) : Methode für den Zugriff auf die unterstützten Funktionen.
-   [**CD3DX12 \_ Raster \_ DESC**](cd3dx12-rasterizer-desc.md) : Hilfsklasse zum Erstellen von Raster-Beschreibungen.

## <a name="related-topics"></a>Verwandte Themen

<dl> <dt>

[Video-Tutorials zu DirectX Advanced Learning: konservative rasterization](https://www.youtube.com/watch?v=zL0oSY_YmDY)
</dt> <dt>

[Geordnete Ansichten des Rasterizers](rasterizer-order-views.md)
</dt> <dt>

[Darstellung](rendering.md)
</dt> </dl>

 

 




