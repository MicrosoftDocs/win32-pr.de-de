---
title: Rasterisierungsregeln
description: Rasterisierungsregeln definieren, wie Vektordaten in Rasterdaten zugeordnet werden.
ms.assetid: 2b3894eb-dff3-401f-8b14-4af98db86e39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e256c6fc171c1cce9b63b79fac6a480e507a306e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390352"
---
# <a name="rasterization-rules"></a>Rasterisierungsregeln

Rasterisierungsregeln definieren, wie Vektordaten in Rasterdaten zugeordnet werden. Die Rasterdaten werden an ganzzahlige Speicherorte angedockt, die dann durch ein-und abgeschnitten werden (um die Mindestanzahl von Pixeln zu zeichnen), und pro Pixel-Attribute werden interpoliert (von pro-Vertex-Attributen), bevor Sie an einen PixelShader übergeben werden.

Es gibt mehrere Typen von Regeln, die vom Typ des primitiven abhängig sind, das zugeordnet wird, und unabhängig davon, ob die Daten multisamplinggrad verwenden, um Aliasing zu verringern. Die folgenden Abbildungen veranschaulichen, wie die eckfälle behandelt werden.

-   [Dreiecks rasterisierungsregeln (ohne Multisampling)](#triangle-rasterization-rules-without-multisampling)
-   [Linienrasterisierungsregeln (Alias, ohne Multisampling)](#line-rasterization-rules-aliased-without-multisampling)
-   [Linienrasterisierungsregeln (Antialiasing, ohne Multisampling)](#line-rasterization-rules-antialiased-without-multisampling)
-   [Punktrasterisierungsregeln (ohne Multisampling)](#point-rasterization-rules-without-multisampling)
-   [Multisample Anti-Aliasing-rasterisierungsregeln](#multisample-anti-aliasing-rasterization-rules)
    -   [Hardware Unterstützung](#hardware-support)
    -   [Centroid-Stichprobenentnahme von Attributen bei Multisample-Antialiasing](#centroid-sampling-of-attributes-when-multisample-antialiasing)
    -   [Abgeleitete Berechnungen bei Multisampling](#derivative-calculations-when-multisampling)
-   [Zugehörige Themen](#related-topics)

## <a name="triangle-rasterization-rules-without-multisampling"></a>Dreiecks rasterisierungsregeln (ohne Multisampling)

Jedes Pixel Center, das in einem Dreieck liegt, wird gezeichnet. Es wird davon ausgegangen, dass sich ein Pixel in der oberen linken Regel befindet. Die linke obere Regel besteht darin, dass ein Pixel Center so definiert ist, dass es in einem Dreieck liegt, wenn es am oberen Rand oder am linken Rand eines Dreiecks liegt.

Hierbei gilt:

-   Ein oberer Rand ist eine Kante, die exakt horizontal ist und über den anderen Rändern liegt.
-   Ein linker Rand ist ein Rand, der nicht exakt horizontal ist und sich auf der linken Seite des Dreiecks befindet. Ein Dreieck kann über einen oder zwei Linke Kanten verfügen.

Mit der oberen linken Regel wird sichergestellt, dass angrenzende Dreiecke einmal gezeichnet werden.

Diese Abbildung zeigt Beispiele für Pixel, die gezeichnet werden, da Sie entweder innerhalb eines Dreiecks liegen oder der oberen linken Regel folgen.

![Abbildung der Beispiele für die Dreiecks rasterisierung oben links](images/d3d10-rasterrulestriangle.png)

In der hellen und dunklen grauen Abdeckung der Pixel werden Sie als Gruppen von Pixeln angezeigt, um anzugeben, in welchem Dreieck Sie sich befinden.

## <a name="line-rasterization-rules-aliased-without-multisampling"></a>Linienrasterisierungsregeln (Alias, ohne Multisampling)

Zeilenrasterisierungsregeln verwenden einen rautentestbereich, um zu bestimmen, ob eine Linie ein Pixel abdeckt. Bei x-Hauptlinien (Zeilen mit-1 <= Slope <= + 1) umfasst der rautentestbereich den unteren linken Rand, den unteren rechten Rand und die untere Ecke. der Diamant schließt den oberen linken Rand, den oberen rechten Rand, den oberen Rand, die linke Ecke und die Rechte Ecke (dargestellt) aus. Eine y-Hauptlinie ist eine beliebige Zeile, die keine x-Hauptzeile ist. der rautenrautenbereich ist mit der Beschreibung für die x-Hauptlinie identisch, außer die Rechte Ecke ist ebenfalls enthalten.

Wenn der rautenbereich angezeigt wird, deckt eine Linie ein Pixel ab, wenn die Linie den rautentestbereich des Pixels verlässt, wenn Sie entlang der Linie von Anfang bis zum Ende unterwegs ist. Ein Zeilen Streifen verhält sich genauso, wie er als Sequenz von Zeilen gezeichnet wird.

In der folgenden Abbildung sind einige Beispiele dargestellt.

![Abbildung von Beispielen für die Zeilen-rasterisierung mit Alias](images/d3d10-rasterrulesline.png)

## <a name="line-rasterization-rules-antialiased-without-multisampling"></a>Linienrasterisierungsregeln (Antialiasing, ohne Multisampling)

Eine Antialiasing-Linie wird so gerendert, als ob es sich um ein Rechteck (mit Breite = 1) handelt. Das Rechteck überschneidet sich mit einem Renderziel, das pro Pixel Abdeckungs Werte erzeugt, die in Pixel-Shader-Ausgabe-Alpha Komponenten multipliziert werden. Beim Zeichnen von Linien auf einem Multisampling-Renderziel gibt es keine präaliasing.

Es wird davon ausgegangen, dass es keine einzige "beste" Methode zum Ausführen von Zeilen Rendering mit Antialiasing gibt. Direct3D 10 übernimmt die in der folgenden Abbildung gezeigte Methode als Richtlinie. Diese Methode wurde empirisch abgeleitet und stellt eine Reihe von visuellen Eigenschaften dar, die als wünschenswert erachtet werden. Hardware muss mit diesem Algorithmus nicht exakt übereinstimmen. Tests für diesen Verweis sollten über "sinnvolle" Toleranzen verfügen, die durch einige der unten aufgeführten Prinzipien gesteuert werden, die verschiedene Hardware Implementierungen und Filter-Kernel Größen ermöglichen. Keine dieser flexiblen Flexibilität bei der Hardware Implementierung kann jedoch über Direct3D 10 an Anwendungen kommuniziert werden, und zwar über das einfache Zeichnen von Linien und das beobachten/Messen der Art und Weise.

![Abbildung von Beispielen für die Zeilen-rasterisierung mit Antialiasing](images/d3d10-rasterruleslineaa.png)

Dieser Algorithmus generiert relativ glatte Linien mit einheitlicher Intensität und minimalen verzweigten Kanten oder dem Geflecht. Das mugistermuster für schließende Zeilen ist minimiert. Es gibt eine gute Abdeckung für Verbindungen zwischen Zeilen Segmenten, die End-to-End platziert werden. Der Filter-Kernel ist ein angemessener Kompromiss zwischen dem Umfang des edgeblurrings und den durch gammakorrekturen verursachten Änderungen der Intensität. Der Coverage-Wert wird mit Pixel Shader o0. a (srcalpha) gemäß der folgenden Formel von der Output-Merger-Phase multipliziert: srccolor \* srcalpha + destcolor \* (1-srcalpha).

## <a name="point-rasterization-rules-without-multisampling"></a>Punktrasterisierungsregeln (ohne Multisampling)

Ein Punkt wird so interpretiert, als wäre er aus zwei Dreiecken in einem Z-Muster zusammengesetzt, die Dreiecks rasterisierungsregeln verwenden. Die Koordinate identifiziert den Mittelpunkt eines einzelnen Pixel weiten Quadrats. Es gibt keine Berechnungen für Punkte.

In der folgenden Abbildung sind einige Beispiele dargestellt.

![Darstellung von Beispielen für die Punkt-rasterisierung](images/d3d10-rasterrulespoint.png)

## <a name="multisample-anti-aliasing-rasterization-rules"></a>Multisample Anti-Aliasing-rasterisierungsregeln

Multisample Antialiasing (MSAA) reduziert die Geometrie Aliasing mithilfe von Pixel Abdeckung und tiefen Schablone an mehreren unter Stichproben Positionen. Um die Leistung zu verbessern, werden pro Pixel-Berechnungen einmal für jedes abgedeckte Pixel durchgeführt, indem shaderausgaben in abgedeckten unter Pixeln gemeinsam genutzt werden. Multisample-Antialiasing reduziert das Oberflächen Aliasing nicht. Beispiel Speicherorte und-Funktionen sind von der Hardware Implementierung abhängig.

In der folgenden Abbildung sind einige Beispiele dargestellt.

![Abbildung von Beispielen für die AntiAlias-rasterisierung mit mehreren Stichproben](images/d3d10-rasterrulesmsaa.png)

Die Anzahl der Beispiel Speicherorte hängt vom Multisampling-Modus ab. Vertex-Attribute werden in Pixel Centern interpoliert, da hier der Pixelshader aufgerufen wird (Dies wird zur extrapolierungen, wenn der Mittelpunkt nicht abgedeckt ist). Attribute können im Pixelshader gekennzeichnet werden, um einen Schwerpunkt zu erreichen. Dies bewirkt, dass nicht abgedeckte Pixel das Attribut bei Schnittstellen des Pixel Bereichs und des primitiven interpolieren. Ein Pixelshader wird für jeden 2 x 2-Pixel Bereich ausgeführt, um abgeleitete Berechnungen (die x-und y-Delta verwenden) zu unterstützen. Dies bedeutet, dass Shader-Aufrufe mehr vorkommen, als angezeigt wird, um den minimalen 2 x 2-Quanten-Wert (der unabhängig von Multisampling ist) auszufüllen. Das Shader-Ergebnis wird für jedes abgedeckte Beispiel geschrieben, das den Test der tiefen Schablone pro Stichprobe übergibt.

Rasterisierungsregeln für primitive sind im Allgemeinen durch Multisampling-Antialiasing unverändert, ausgenommen:

-   Bei einem Dreieck wird für jeden Beispiel Speicherort ein Abdeckungs Test ausgeführt (nicht für ein Pixel Center). Wenn mehr als ein Beispiel Speicherort abgedeckt ist, wird ein Pixelshader einmal mit Attributen ausgeführt, die im Pixel Center interpoliert werden. Das Ergebnis wird für jeden abgedeckten Beispiel Speicherort im Pixel gespeichert (repliziert), das den tiefen-/Stencil-Test übergibt.

    Eine Linie wird als Rechteck behandelt, das aus zwei Dreiecken besteht und einer Linienbreite von 1,4 entspricht.

-   Für einen Punkt wird ein Abdeckungs Test für jeden Beispiel Speicherort ausgeführt (nicht für ein Pixel Center).

Viele Formate unterstützen multisamplinggrad (siehe [Hardware Unterstützung für Direct3D 10-Formate](/previous-versions//cc627090(v=vs.85))), einige Formate können aufgelöst werden ([**resolvesubresource**](/windows/desktop/api/d3d10/nf-d3d10-id3d10device-resolvesubresource)), die ein Downsampling für ein multisamplinggrad-Format auf eine Stichprobengröße von 1 durchgeführt haben. Multisampling-Formate können in Renderingzielen verwendet werden, die mithilfe von " [Load](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-to-load)" in Shader eingelesen werden können, da für einzelne Beispiele, auf die der Shader zugreift, keine Auflösung erforderlich ist. Tiefen Formate werden für Multisampling-Ressourcen nicht unterstützt. Daher sind die tiefen Formate nur auf Renderziele beschränkt.

Typlose Formate ( \_ z. R8G8B8A8. typlose) unterstützen multisamplinggrad, damit eine Ressourcen Ansicht Daten auf unterschiedliche Weise interpretieren kann. Beispielsweise können Sie eine Multisampling-Ressource mit R8G8B8A8 \_ typless erstellen, Sie mit einer "Rendering-Target-View"-Ressource mit einem R8G8B8A8 \_ uint-Format reneln und dann den Inhalt in eine andere Ressource mit einem R8G8B8A8 \_ unorm-Datenformat auflösen.

### <a name="hardware-support"></a>Hardwareunterstützung

Die API meldet die Hardwareunterstützung für multisamplinggrad über die Anzahl der Qualitätsstufen. Beispielsweise bedeutet der Wert 0 (null), dass die Hardware keine multisamplinggrad-Unterstützung (in einem bestimmten Format und einer Qualitätsstufe) unterstützt. Ein 3 für Qualitätsstufen bedeutet, dass die Hardware drei verschiedene Beispiel Layouts und/oder Auflösungs Algorithmen unterstützt. Sie können auch Folgendes annehmen:

-   Jedes Format, das Multisampling unterstützt, unterstützt die gleiche Anzahl von Qualitäts Ebenen für jedes Format in dieser Familie.
-   Jedes Format, das Multisampling unterstützt und die \_ unorm-, \_ sRGB-, \_ snorm-oder \_ float-Formate unterstützt, unterstützt auch das Auflösen von.

### <a name="centroid-sampling-of-attributes-when-multisample-antialiasing"></a>Centroid-Stichprobenentnahme von Attributen bei Multisample-Antialiasing

Standardmäßig werden Vertex-Attribute bei Multisampling-Antialiasing in ein Pixel Center interpoliert. Wenn das Pixel Center nicht abgedeckt wird, werden Attribute zu einem Pixel Center extrapoliert. Wenn eine Pixel-Shadereingabe, die die Schwerpunkt-Semantik enthält (vorausgesetzt, das Pixel ist nicht vollständig abgedeckt ist), wird eine beliebige Stelle im abgedeckten Bereich des Pixels entnommen, möglicherweise an einem der abgedeckten Beispiel Speicherorte. Eine Beispiel Maske (angegeben durch den Raster-Zustand) wird vor der Schwerpunkt-Berechnung angewendet. Daher wird ein Beispiel, das maskiert wird, nicht als Schwerpunkt Speicherort verwendet.

Der Verweis-Raster wählt einen Beispiel Speicherort für die Schwerpunkt-Stichprobenentnahme ähnlich dem folgenden aus:

-   Die Beispiel Maske lässt alle Beispiele zu. Verwenden Sie ein Pixel Center, wenn das Pixel abgedeckt ist, oder wenn keines der Beispiele abgedeckt wird. Andernfalls wird das erste abgedeckte Beispiel ausgewählt, beginnend mit dem Pixel Center und nach außen.
-   Die Beispiel Maske deaktiviert alle Beispiele, aber einen (ein gängiges Szenario). Eine Anwendung kann Multipass-Supersampling implementieren, indem Sie Einzelbit-Stichproben Masken Werte durchlaufen und die Szene für jede Stichprobe mithilfe der Schwerpunkt-Stichproben Erstellung erneut rendern. Dies erfordert, dass eine Anwendung Ableitungen anpasst, um für die höhere Textur Stichproben Dichte entsprechend ausführlichere Textur MIPS auszuwählen.

### <a name="derivative-calculations-when-multisampling"></a>Abgeleitete Berechnungen bei Multisampling

Pixel-Shader werden immer mit einem minimalen 2 x 2-Pixel Bereich ausgeführt, um abgeleitete Berechnungen zu unterstützen. Diese werden berechnet, indem Delta Einheiten zwischen den Daten aus angrenzenden Pixeln verwendet werden (vorausgesetzt, dass die Daten in jedem Pixel horizontal oder vertikal mit dem Einheiten Abstand abgetastet wurden). Dies ist von Multisampling nicht betroffen.

Wenn für ein Attribut, für das ein Schwerpunkt erstellt wurde, Ableitungen angefordert werden, wird die Hardware Berechnung nicht angepasst, was zu ungenauen Ableitungen führen kann. Ein Shader erwartet einen Einheiten Vektor im renderzielbereich, kann jedoch einen nicht-Einheits Vektor in Bezug auf einen anderen Vektorraum erhalten. Daher ist es für eine Anwendung wichtig, bei der Anforderung von Ableitungen von Attributen, bei denen es sich um eine Stichprobe handelt, eine Vorsicht zu Es wird empfohlen, dass Sie keine Ableitungen und Schwerpunkt-Stichproben kombinieren. Die Centroid-Stichprobenentnahme kann in Situationen nützlich sein, in denen es wichtig ist, dass die interpolierten Attribute eines primitiven nicht extrapoliert werden. Dies ist jedoch mit vor-und Nachteile, wie z. b. Attributen zu tun, bei denen ein primitiver Rand ein Pixel überschreitet (anstatt sich ständig zu ändern) oder Ableitungen, die nicht von Textur-Samplings verwendet werden

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Stufe des Rasterizers](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 