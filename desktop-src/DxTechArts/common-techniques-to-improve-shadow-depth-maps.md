---
title: Allgemeine Artikel zum Verbessern von Tiefenkarten für Schatten
description: Dieser technische Artikel bietet eine Übersicht über einige gängige Shadow depth map-Algorithmen und allgemeine Artefakte und erläutert verschiedene Techniken – von einfach bis zwischengeschaltet – die verwendet werden können, um die Qualität von Standardschattenkarten zu erhöhen.
ms.assetid: bf994838-a261-0379-9301-eb9b250d216c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafff1b537830ae0ee681ed32932cca2b6274a4d9da3e0471ef498e0bef2d483
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102470"
---
# <a name="common-techniques-to-improve-shadow-depth-maps"></a>Allgemeine Artikel zum Verbessern von Tiefenkarten für Schatten

Schattenkarten, die erstmals 1978 eingeführt wurden, sind eine gängige Technik zum Hinzufügen von Schatten zu Spielen. Drei Jahrzehnte später bleiben Schattenartefakte – nämlich schattierende Kanten, Perspektivenaliasing und andere Genauigkeitsprobleme – trotz fortschrittender Hardware und Software bestehen.

Dieser technische Artikel bietet eine Übersicht über einige gängige Shadow depth map-Algorithmen und allgemeine Artefakte und erläutert verschiedene Techniken – von einfach bis zwischengeschaltet – die verwendet werden können, um die Qualität von Standardschattenkarten zu erhöhen. Das Hinzufügen grundlegender Schattenzuordnungen zu einem Titel ist in der Regel einfach, aber das Verständnis der Nuancen von Schattenartefakten kann eine Herausforderung darstellen. Dieser technische Artikel wurde für den fortgeschrittene Grafikentwickler geschrieben, der Schatten implementiert hat, aber nicht vollständig versteht, warum bestimmte Artefakte angezeigt werden, und ist nicht sicher, wie sie umgangen werden sollen.

Die Auswahl der richtigen Techniken zum Mindern bestimmter Artefakte ist nicht spezifisch. Wenn Schattenzuordnungslücken behoben werden, kann der Unterschied in der Qualität beeindruckender sein (Abbildung 1). Durch die ordnungsgemäße Implementierung dieser Techniken werden Standardschatten drastisch verbessert. Die in diesem Artikel erläuterten Verfahren werden im Beispiel CascadedShadowMaps11 im DirectX SDK implementiert.

**Abbildung 1: Schatten mit schwerwiegenden Artefakten (links) und Schatten nach der Implementierung der in diesem Artikel beschriebenen Techniken (rechts)**

![Schatten mit schwerwiegenden Artefakten (links) und Schatten nach der Implementierung der in diesem Artikel beschriebenen Techniken (rechts)](images/shadows-before-and-after.jpg)

## <a name="shadow-depth-maps-review"></a>Shadow Depth Karten Review

Der Shadow Depth Map-Algorithmus ist ein Zwei-Durchlauf-Algorithmus. Der erste Durchlauf generiert eine Tiefenkarte im lichten Raum. Im zweiten Durchlauf wird diese Karte verwendet, um die Tiefe jedes Pixels im Lichtraum mit der entsprechenden Tiefe in der Lichtraum-Tiefenkarte zu vergleichen.

**Abbildung 2. Wichtige Teile einer Schattenszene**

![Wichtige Teile einer Schattenszene](images/key-parts-of-shadow-scene.jpg)

### <a name="pass-1"></a>Pass 1

Die Szene ist in Abbildung 2 dargestellt. Im ersten Durchlauf (Abbildung 3) wird die Geometrie aus Sicht des Lichts in einen Tiefenpuffer gerendert. Genauer gesagt transformiert der Vertex-Shader die Geometrie in einen Lichtansichtsbereich.

Das Endergebnis dieses ersten Durchlaufs ist ein Tiefenpuffer, der die Tiefeninformationen der Szene aus Sicht des Lichts enthält. Dies kann jetzt in Durchlauf 2 verwendet werden, um zu bestimmen, welche Pixel vom Licht verdeckt werden.

**Abbildung 3: Erster Durchlauf der grundlegenden Schattenzuordnung**

![Erster Durchlauf der grundlegenden Schattenzuordnung](images/first-pass-of-basic-hadow-mapping.png)

### <a name="pass-2"></a>Pass 2

Im zweiten Durchlauf (Abbildung 4) transformiert der Vertex-Shader jeden Scheitelpunkt zweimal. Jeder Scheitelpunkt wird in den Ansichtsbereich der Kamera transformiert und als Position an den Pixel-Shader übergeben. Jeder Scheitelpunkt wird auch durch die Ansichtsprojektionstexturmatrix des Lichts transformiert und als Texturkoordinate an den Pixelshader übergeben. Die Matrix view-projection-texture ist die gleiche Matrix, die verwendet wird, um die Szene in Durchlauf 1 mit einer zusätzlichen Transformation zu rendern. Es ist eine Transformation, die die Punkte aus dem Ansichtsbereich (–1 in 1 in X und Y) in den Texturraum (0 bis 1 in X und 1 in 0 in Y) skaliert und übersetzt.

Der Pixelshader empfängt die interpolierte Position und die interpolierten Texturkoordinaten. Alles, was zum Durchführen des Tiefentests erforderlich ist, befindet sich jetzt in dieser Texturkoordinate. Der Tiefentest kann jetzt durchgeführt werden, indem der Tiefenpuffer aus dem ersten Durchlauf mit den X- und Y-Texturkoordinaten indiziert und der resultierende Tiefenwert mit der Z-Texturkoordinate verglichen wird.

**Abbildung 4. Zweiter Durchlauf der grundlegenden Schattenzuordnung**

![Zweiter Durchlauf der grundlegenden Schattenzuordnung](images/second-pass-of-basic-shadow-mapping.png)

## <a name="shadow-map-artifacts"></a>Schattenkarten-Artifacts

Der Shadow Depth Map-Algorithmus ist der am häufigsten verwendete Echtzeitschattenalgorithmus, erzeugt aber trotzdem mehrere Artefakte, die entschärft werden müssen. Als Nächstes werden die Artefakttypen zusammengefasst, die auftreten können.

### <a name="perspective-aliasing"></a>Perspektivenaliasing

Das perspektivische Aliasing, ein allgemeines Artefakt, ist in Abbildung 5 dargestellt. Sie tritt auf, wenn die Zuordnung von Pixeln im Ansichtsbereich zu Texel in der Schattenkarte kein 1:1-Verhältnis ist. Dies liegt daran, dass Pixel in der Nähe der näheren Ebene näher beieinander liegen und eine höhere Schattenbildauflösung erfordern.

Abbildung 6 zeigt eine Schattenkarte und ein Sicht-Frustum. In der Nähe des Auges sind die Pixel näher beieinander, und viele Pixel werden den gleichen Schatten-Texeln zugeordnet. Die Pixel auf der fernen Ebene werden verteilt, wodurch das perspektivische Aliasing reduziert wird.

**Abbildung 5. Aliasing mit hoher Perspektive (links) im Vergleich zu Aliasing mit niedriger Perspektive (rechts)**

![Aliasing mit hoher Perspektive (links) im Vergleich zu Aliasing mit niedriger Perspektive (rechts)](images/high-perspective-aliasing-vs-low-perspective-aliasing.jpg)

Für das Bild auf der linken Seite ist das perspektivische Aliasing höher. Zu viele Eyespacepixel werden den gleichen Schattenkarten-Texeln zugeordnet. Im Bild rechts ist das Perspektivaliasing niedrig, da es eine 1:1-Zuordnung zwischen den Augenbereichspixeln und Schattenkarten-Texeln gibt.

**Abbildung 6: Anzeigen des Frustums mit Schattenkarte**

![Anzeigen des Frustums mit Schattenkarte](images/view-frustum-with-shadow-map.jpg)

Helle Pixel in der fernen Ebene stellen Aliasing mit niedriger Perspektive dar, und dunkle Pixel auf der nahseitigen Ebene stellen aliasing mit hoher Perspektive dar.

Die Auflösung von Schattenkarten kann auch zu hoch sein. Obwohl eine höhere Auflösung weniger wahrnehmbar ist, kann dies dennoch dazu führen, dass kleine Objekte, z. B. Telefonkabel, keine Schatten werfen. Außerdem kann eine zu hohe Auflösung aufgrund von Texturzugriffsmustern zu schwerwiegenden Leistungsproblemen führen.

Perspektivenschattenkarten (Perspective Shadow Maps, PSMs) und LSPSMs (Light Space Perspective Shadow Maps) versuchen, das perspektivische Aliasing zu adressieren, indem sie die Projektionsmatrix des Lichts strichen, um weitere Texel in der Nähe des Auges zu platzieren, wo sie benötigt werden. Leider ist keine der Beiden Methoden in der Lage, das perspektivische Aliasing zu lösen. Die Parametrisierung der Transformation, die zum Zuordnen von Eyespacepixeln zu Texeln in der Schattenkarte erforderlich ist, kann nicht durch eine lineare Schiefe gebunden werden. Eine logarithmische Parametrisierung ist erforderlich. PSMs legen zu viele Details in die Nähe des Auges, was dazu führt, dass entfernte Schatten von niedriger Qualität sind oder sogar verschwinden. LSPSMs verbessern die Suche nach einem Mittelweg zwischen dem Erhöhen der Auflösung in der Nähe des Auges und dem Verlassen ausreichender Details für weit entfernte Objekte. Beide Techniken degenerieren in einigen Szenenkonfigurationen zu orthografischen Schatten. Diese Degeneration kann vermieden werden, indem für jedes Gesicht des Ansichts frustums eine separate Schattenkarte gerendert wird, obwohl dies teuer ist. Logarithmische Perspektivenschattenkarten (LogPSMs) rendern auch eine separate Karte pro Gesicht des Sicht-Frustums. Dieses Verfahren verwendet nicht lineare Rasterung, um weitere Texel in der Nähe des Auges zu platzieren. Hardware der D3D10- und D3D11-Klasse unterstützt keine nicht lineare Rasterung. Weitere Informationen zu diesen Techniken und Algorithmen finden Sie im Abschnitt Verweise.

Kaskadierte Schattenzuordnungen (Cascaded Shadow Maps, CSMs) sind die gängigste Technik für den Umgang mit perspektivischem Aliasing. Obwohl CSMs mit PSMs und LSPSMs kombiniert werden können, ist dies unnötig. Die Verwendung von CSMs zum Beheben von Fehlern beim perspektivischen Aliasing wird im Begleitartikel [Cascaded Shadow Karten](/windows/desktop/DxTechArts/cascaded-shadow-maps)behandelt.

### <a name="projective-aliasing"></a>Projective Aliasing

Projective Aliasing ist schwieriger anzuzeigen als perspektivische Aliase. Die in Abbildung 7 hervorgehobenen unbeaufsichtigten Schatten veranschaulichen projektive Aliasingfehler. Projective Aliasing tritt auf, wenn die Zuordnung zwischen Texel im Kameraraum und Texel im lichten Raum kein 1:1-Verhältnis ist. Dies liegt an der Ausrichtung der Geometrie in Bezug auf die lichte Kamera. Projective Aliasing tritt auf, wenn die Tangentenebene der Geometrie parallel zum Lichtlicht wird.

**Abbildung 7. Hochprojektives Aliasing im Vergleich zu low-projective aliasing**

![High-Projective Aliasing im Vergleich zu low-projective aliasing](images/high-projective-aliasing-vs-low%20projective-aliasing.jpg)

Techniken, die zum Beheben von Fehlern beim Perspektivaliasing verwendet werden, verringern auch das projektive Aliasing. Projective Aliasing tritt auf, wenn die Oberflächennormalität orthogonal zum Licht ist. Diese Oberflächen sollten basierend auf diffusen Beleuchtungsgleichungen weniger Licht empfangen.

### <a name="shadow-acne-and-erroneous-self-shadowing"></a>Schattenschatten und fehlerhafte Self-Shadowing

Schattenschatten (Abbildung 8), ein Begriff, der mit fehlerhaftem Selbstschatten synonym ist, tritt auf, wenn die Schattenkarte die Tiefe über einem gesamten Texel quantitiert. Wenn der Shader eine tatsächliche Tiefe mit diesem Wert vergleicht, ist es so wahrscheinlich, dass er selbstschattend ist, wie er nicht überschattet ist.

Ein weiterer Grund für Schattenstörungen ist, dass das Texel im lichten Raum so nah an der Tiefe des entsprechenden Texels in der Tiefenkarte liegt, dass Genauigkeitsfehler dazu führen, dass der Tiefentest fälschlicherweise fehlschlägt. Ein Grund für diesen Genauigkeitsunterschied ist, dass die Tiefenzuordnung von der Hardware für die Rasterung fester Funktionen berechnet wurde, während die verglichene Tiefe vom Shader berechnet wurde. Projective Aliasing kann auch schattenverursachen.

**Abbildung 8. Schattenartefakt**

![Schattenkopieartefakt](images/shadow-acne-artifact.jpg)

Wie in der linken Abbildung dargestellt, ist bei einigen Pixeln der Tiefentest fehlgeschlagen, und es wurden speckled artifacts und moicreme-Muster erstellt. Um fehlerhaftes Selbstschatten zu reduzieren, sollten die Begrenzungen auf der Nahebene und der fernen Ebene für das Frustum der Lichtraumansicht so eng wie möglich berechnet werden. Die neigungsskaliert-basierte Tiefenabweichung und andere Arten von Verzerrung sind andere Lösungen, die zur Entschärfung von Schattenschattierungen verwendet werden.

### <a name="peter-panning"></a>Peter Panning

Der Begriff *Peter Panning* leitet seinen Namen von einem Buchzeichen eines untergeordneten Benutzers ab, dessen Schatten getrennt wurde und wer flog. Dieses Artefakt bewirkt, dass Objekte mit fehlenden Schatten von und in float über der Oberfläche getrennt zu sein scheinen (Abbildung 9).

**Abbildung 9: Peter Panning-Artefakt**

![Peter schwenkendes Artefakt](images/peter-panning-artifact.jpg)

Im Bild auf der linken Seite wird der Schatten vom -Objekt getrennt, wodurch ein Gleitkommaeffekt entsteht.

Eine Technik zum Entfernen von Oberflächenoberflächen ist das Hinzufügen eines Werts zur Pixelposition im hellen Raum. dies wird als Hinzufügen eines Tiefenoffsets bezeichnet. Peter Panning ergibt, wenn der verwendete Tiefenoffset zu groß ist. In diesem Fall führt der Tiefenoffset dazu, dass der Tiefentest fälschlicherweise bestanden wird. Wie Schattenschatten wird Peter Panning geschwennt, wenn der Tiefenpuffer nicht genau genug ist. Das Berechnen von engen Nah- und Fernebenen hilft auch, Peter Panning zu vermeiden.

## <a name="techniques-to-improve-shadow-maps"></a>Techniken zur Verbesserung der Schatten Karten

Das Hinzufügen von Schatten zu einem Titel ist ein Prozess. Der erste Schritt besteht im Arbeiten mit grundlegenden Schattenkarten. Die zweite besteht in der Sicherstellung, dass alle grundlegenden Berechnungen optimal durchgeführt werden: Frusta passt so eng wie möglich, Nah-/Fernebenen passen eng an, steigungsskalierte Abweichungen werden verwendet und so weiter. Sobald grundlegende Schatten aktiviert sind und so gut wie möglich aussehen, hat der Entwickler eine bessere Vorstellung davon, welche Algorithmen benötigt werden, um die Schatten auf eine ausreichende Genauigkeit zu bringen. Grundlegende Tipps, die möglicherweise erforderlich sind, um grundlegende Schattenkarten zu erhalten, die sich am besten ansehen, finden Sie in diesem Abschnitt.

### <a name="slope-scale-depth-bias"></a>Slope-Scale Tiefenvoreingenommenheit

Wie bereits erwähnt, kann Selbstschatten zu Schattenschatten führen. Das Hinzufügen zu viel Voreingenommenheit kann zu Peter Panning führen. Darüber hinaus sind Polygone mit starker Steigung (relativ zum Licht) stärker von projektiven Aliasen betroffen als Polygone mit flachen Steigungen (relativ zum Licht). Aus diesem Grund benötigt jeder Tiefenzuordnungswert abhängig von der Steigung des Polygons relativ zum Licht möglicherweise einen anderen Offset.

Direct3D 10-Hardware kann ein Polygon basierend auf seiner Steigung in Bezug auf die Ansichtsrichtung vorverzerren. Dies hat den Effekt, dass eine große Verzerrung auf ein Polygon, das am Rand angezeigt wird, auf die Lichtrichtung, aber nicht auf ein Polygon, das direkt auf das Licht ausgerichtet ist, anwendunget. Abbildung 10 zeigt, wie zwei benachbarte Pixel sich beim Testen mit der gleichen unausgeschweiften Steigung zwischen Schatten und unshadowed wechseln können.

**Abbildung 10. Neigungsskalierte Tiefenverzerrung im Vergleich zur unvoreingenommenen Tiefe**

![Steigung skalierte Tiefenverzerrung im Vergleich zur unvoreingenommenen Tiefe](images/slope-scaled-depth-bias-compared-to-unbiased-depth.png)

### <a name="calculating-a-tight-projection"></a>Berechnen einer engen Projektion

Die enge Anpassung der Projektion des Lichts an das Ansichtsfrustum erhöht die Abdeckung der Schattenkarte. Abbildung 11 veranschaulicht, dass die Verwendung einer beliebigen Projektion oder das Anpassen der Projektion an die Szenengrenze zu einem höheren Perspektivaliasing führt.

**Abbildung 11. Beliebiger Schatten frustum und Schatten frustum passen zur Szene**

![Beliebiger Schatten frustum und Schatten frustum passen zur Szene](images/arbitrary-shadow-frustum-and-shadow-frustum-fit-to-scene.jpg)

Die Ansicht ist aus der Sicht des Lichts. Das Trapezoid stellt das Frustum der Ansichtskamera dar. Das über dem Bild gezeichnete Raster stellt die Schattenkarte dar. Das Bild auf der rechten Seite zeigt, dass die gleiche Auflösungsschattenkarte mehr Texelabdeckung erzeugt, wenn sie enger an die Szene passt.

Abbildung 12 veranschaulicht frustums, die richtig passen. Um die Projektion zu berechnen, werden die acht Punkte, aus denen sich das Frustum der Ansicht macht, in einen hellen Raum transformiert. Als Nächstes werden die minimalen und maximalen Werte in X und Y gefunden. Diese Werte machen die Grenzen für eine orthografische Projektion aus.

**Abbildung 12. Shadow projection fit to view frustum (Schattenprojektion passt zum Anzeigen des Frustums)**

![Shadow projection fit to view frustum (Anpassung der Schattenprojektion zum Anzeigen des Frustums)](images/shadow-projection-fit-to-view-frustum.jpg)

Es ist auch möglich, das Frustum an die Szene AABB zu beschneiden, um eine strengere Grenze zu erhalten. Dies wird nicht in allen Fällen empfohlen, da dies die Größe der Projektion der Lichtkamera von Frame zu Frame ändern kann. Viele Techniken, z.B. die im Abschnitt Moving the Light Texel-Sized Increments (Bewegen des Lichts Texel-Sized Inkremente), beschriebenen Verfahren liefern bessere Ergebnisse, wenn die Größe der Projektion des Lichts in jedem Frame konstant bleibt.

### <a name="calculating-the-near-plane-and-far-plane"></a>Berechnen der Nah- und Fernebene

Die nahe ebene und die ferne Ebene sind die letzten Teile, die zum Berechnen der Projektionsmatrix erforderlich sind. Die Werte im Tiefenpuffer werden genauer, wenn die Ebenen enger miteinander verbunden sind.

Der Tiefenpuffer kann 16 Bit, 24 Bit oder 32 Bit mit Werten zwischen 0 und 1 sein. Im Allgemeinen sind Tiefenpuffer ein fester Punkt, bei dem die Werte in der Nähe der nahe liegenden Ebene näher beieinander liegen als die Werte in der Nähe der fernen Ebene. Der für den Tiefenpuffer verfügbare Genauigkeitsgrad wird durch das Verhältnis zwischen der nahe und der fernen Ebene bestimmt. Die Verwendung der engsten nah-/fernen Ebene könnte die Verwendung eines 16-Bit-Tiefenpuffers ermöglichen. Ein 16-Bit-Tiefenpuffer könnte die Speichernutzung reduzieren und gleichzeitig die Verarbeitungsgeschwindigkeit erhöhen.

### <a name="aabb-based-near-plane-and-far-plane"></a>AABB-Based Nah- und Fernebene

Eine einfache und naive Möglichkeit, die nahe ebene und die ferne Ebene zu berechnen, besteht in der Transformation des Begrenzungsvolumens der Szene in lichten Raum. Der kleinste Z-Koordinatenwert ist die nahe Ebene, und der größte Z-Koordinatenwert ist die ferne Ebene. Für viele Konfigurationen der Szene und des Lichts ist dieser Ansatz ausreichend. Das ungünstigste Szenario kann jedoch zu einem erheblichen Genauigkeitsverlust im Tiefenpuffer führen. Abbildung 13 zeigt ein solches Szenario. Hier ist der Bereich der näheren Ebene bis zur fernen Ebene viermal größer als erforderlich.

Das Frustum der Ansicht in Abbildung 13 wurde bewusst als klein ausgewählt. Ein kleines Ansichtsfrustum wird in einer sehr großen Szene dargestellt, die aus Säulen besteht, die sich von der Ansichtskamera aus erstrecken. Die Verwendung des Szenen-AABB für die nah- und fernen Ebenen ist nicht optimal. Der im technischen Artikel [Cascaded Shadow Karten](/windows/desktop/DxTechArts/cascaded-shadow-maps) beschriebene CSM-Algorithmus muss nah- und ferne Ebenen für sehr kleine Frustums berechnen.

**Abbildung 13. Nah- und Fernebenen basierend auf Szenen-AABB**

![Nah- und Fernebenen basierend auf Szenenabb](images/near-far-%20planes-based-on-scene-aabb.jpg)

### <a name="frustum-based-near-plane-and-far-plane"></a>Frustum-Based Nah- und Fernebene

Eine weitere Technik zum Berechnen der nah- und fernen Ebenen besteht in der Transformation des Frustums in den lichten Raum und der Verwendung der minimalen und maximalen Werte in Z als die nahe bzw. die ferne Ebene. Abbildung 14 veranschaulicht die beiden Probleme bei diesem Ansatz. Erstens ist die Berechnung zu konservativ, wie gezeigt, wenn sich das Frustum über die Geometrie der Szene hinaus erstreckt. Zweitens könnte die nahe Ebene zu eng sein, was dazu führt, dass Schattencaster zugeschnitten werden.

**Abbildung 14. Nah- und Fernebenen, die ausschließlich auf Sichtfrustum basieren**

![Nah- und Fernebenen, die ausschließlich auf Sichtfrustum basieren](images/near-far-planes-based-solely-on-view-frustum.jpg)

### <a name="light-frustum-intersected-with-scene-to-calculate-near-and-far-planes"></a>Light Frustum Intersected with Scene to Calculate Near and Far Planes

Die richtige Methode zum Berechnen der Nah- und Fernebenen ist in Abbildung 15 dargestellt. Vier der Ebenen des Frustums für orthografisches Licht wurden mithilfe der Minimal- und Höchstwerte der X- und Y-Koordinaten des Ansichtsfrustums im lichten Raum berechnet. Die letzten beiden Ebenen des Frustums der orthogonalen Ansicht sind die nahe und die ferne Ebene. Um diese Ebenen zu finden, werden die Begrenzungen der Szene an die vier bekannten lichten Frustumebenen abgeschnitten. Die kleinsten und größten Z-Werte aus der neu abgeschnittenen Grenze stellen die nahe bzw. ferne Ebene dar.

Der Code, der diesen Vorgang ausführt, befindet sich im CascadedShadowMaps11-Beispiel. Die acht Punkte, aus denen sich das AABB der Welt formt, werden in lichten Raum transformiert. Das Transformieren der Punkte in einen hellen Raum vereinfacht die Clippingtests. Die vier bekannten Ebenen des lichten Frustums können jetzt als Linien dargestellt werden. Das Umgrenzungsvolumen der Szenen im lichten Raum kann als sechs Quadrieren dargestellt werden. Diese 6 quadrierten Klammern können dann in 12 Dreiecke für dreiecksbasiertes Clipping umgedreht werden. Die Dreiecke werden an den bekannten Ebenen des Ansichtsfastums abgeschnitten (dies sind horizontale und vertikale Linien in X und Y im hellen Raum). Wenn ein Schnittpunkt in X und Y gefunden wird, wird das 3D-Dreieck an diesem Punkt abgeschnitten. Die minimalen und maximalen Z-Werte aller abgeschnittenen Dreiecke sind die nahe ebene und die ferne Ebene. Das CascadedShadowMaps11-Beispiel zeigt, wie diese Clippingfunktion in der **ComputeNearAndFar-Funktion verwendet** wird.

Es gibt zwei weitere Techniken, die verwendet werden können, um die engst mögliche Nah- und Fernebene zu berechnen. Diese Techniken werden im CascadedShadowMaps-Beispiel nicht gezeigt.

-   Sogar eine engere Nah- und Fernebene könnte berechnet werden, indem eine Hierarchie einer Szene oder einzelner Objekte in einer Szene mit dem lichten Frustum überschneidet wird. Dies wäre rechenintensiver. Obwohl dies im CascadedShadowMaps11-Beispiel nicht veranschaulicht wird, kann dies eine gültige Technik für einige Kacheln sein.
-   Die Fernebene kann mit dem Minimum von berechnet werden:

    -   Die größte Tiefe des Ansichtsfrustums in hellem Raum.
    -   Die größte Tiefe der Schnittmenge des Ansichtsfrustums und der Szene AABB.

Dieser Ansatz kann problematisch sein, wenn er mit kaskadierenden Schattenkarten verwendet wird, bei denen eine Indizierung außerhalb eines Ansichtsfrustums möglich ist. In diesem Fall fehlt möglicherweise die Geometrie der Schattenkarte.

**Abbildung 15. Nah- und Fernebenen basierend auf der Schnittmenge der vier berechneten Ebenen des lichten Frustums und der Begrenzungsgeometrie der Szene**

![Nah- und Fernebenen basierend auf der Schnittmenge der vier berechneten Ebenen des lichten Frustums und der Begrenzungsgeometrie der Szene](images/near-far-plane-based-on-intersection-of-four.jpg)

### <a name="moving-the-light-in-texel-sized-increments"></a>Bewegen des Lichts in Texel-Sized Schritten

Ein häufiges Artefakt in Schattenkarten ist der schrumpfende Edgeeffekt. Wenn sich die Kamera bewegt, werden die Pixel entlang der Schattenränder auf- und dunkler. Dies ist in stillen Bildern nicht zu sehen, aber es ist sehr wahrnehmbar und störend in Echtzeit. Abbildung 16 hebt dieses Problem hervor, und Abbildung 17 zeigt, wie die Schattenränder aussehen sollten.

Der Fehler beim Umranden tritt auf, weil die Matrix der Lichtprojektion jedes Mal neu berechnet wird, wenn die Kamera bewegt wird. Dies führt zu feinen Unterschieden in den generierten Schattenkarten. Alle folgenden Faktoren können die Matrix beeinflussen, die zum Umgrenzen der Szene erstellt wurde.

-   Größe des Frustums der Ansicht
-   Ausrichtung des Frustums der Ansicht
-   Position des Lichts
-   Position der Kamera

Jedes Mal, wenn sich diese Matrix ändert, können sich die Schattenränder ändern.

**Abbildung 16. Schatten von Schattenrändern**

![Schrumpfen von Schattenrändern](images/shimmering-shadow-edges.jpg)

Die Pixel am Rahmen des Schattens kommen ein und aus dem Schatten, während die Kamera von links nach rechts bewegt wird.

**Abbildung 17. Schatten ohne umrandende Kanten**

![Schatten ohne umrandende Kanten](images/shadows-without-shimmering-edges.jpg)

Die Schattenränder bleiben konstant, wenn die Kamera von links nach rechts bewegt wird.

Bei direktionalen Beleuchtungen besteht die Lösung für dieses Problem in der Rundung des Minimal-/Höchstwerts in X und Y (die die Orthografischen Projektionsgrenze darstellen) auf Pixelgrößeninkremente. Dies kann mit einem Divisionsvorgang, einem Bodenvorgang und einer Multiplikation erfolgen.


```C++
        vLightCameraOrthographicMin /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMin = XMVectorFloor( vLightCameraOrthographicMin );
        vLightCameraOrthographicMin *= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax = XMVectorFloor( vLightCameraOrthographicMax );
        vLightCameraOrthographicMax *= vWorldUnitsPerTexel;
```



Der vWorldUnitsPerTexel-Wert wird berechnet, indem eine Grenze des Ansichtsfrustums verwendet und durch die Puffergröße dividiert wird.


```C++
        FLOAT fWorldUnitsPerTexel = fCascadeBound /
        (float)m_CopyOfCascadeConfig.m_iBufferSize;
        vWorldUnitsPerTexel = XMVectorSet( fWorldUnitsPerTexel, fWorldUnitsPerTexel,                            0.0f, 0.0f );
```



Die Begrenzung der maximalen Größe des Ansichtsfrustums führt zu einer lockereren Anpassung für die orthografische Projektion.

Es ist wichtig zu beachten, dass die Textur bei Verwendung dieser Technik 1 Pixel größer als Breite und Höhe ist. Dadurch wird verhindert, dass Schattenkoordinaten außerhalb der Schattenkarte indiziert werden.

### <a name="back-face-and-front-face"></a>Zurückgesicht und Frontgesicht

Schattenkarten sollten mit standarder Back-Face-Culling gerendert werden, einem Prozess, der die Rasterung von Objekten überspringt, die der Betrachter nicht sehen kann, und das Rendern der Szene beschleunigt. Eine weitere gängige Option ist das Rendern von Schattenkarten mit aktivierter Gesichtserkennung, was bedeutet, dass Objekte, die dem Betrachter zur Verfügung stehen, entfernt werden. Das Argument dafür ist, dass es bei der Selbstschattenung hilft, da die Geometrie, aus der die Rückseite von Objekten besteht, leicht versetzt ist. Es gibt zwei Probleme mit dieser Idee.

-   Jedes Objekt mit falscher Front-Face- oder Back-Face-Geometrie verursacht Artefakte in der Schattenkarte. Eine falsche Front- oder Back-Face-Geometrie verursacht jedoch andere Probleme, sodass es sicher sein kann, davon auszugehen, dass die Geometrie des Vorder- und Dese gesichts korrekt erfolgt. Es kann unpraktisch sein, Hintergrundgesichter für sprite-basierte Geometrie wie z. B. Foliage zu erstellen.
-   Peter Panning und Schattenlücken in der Nähe der Basis von Objekten wie Wänden treten wahrscheinlicher auf, da die Schattentiefe zu klein ist.

### <a name="shadow-mapfriendly-geometry"></a>Schattenkarte – Benutzerfreundliche Geometrie

Das Erstellen von Geometrie, die gut in Schattenkarten funktioniert, ermöglicht mehr Flexibilität, wenn Artefakte wie Peter Panning und Schattenschatten dargestellt werden.

Harte Kanten sind problematisch für Selbstschatten. Die Tiefenunterschiede in der Nähe der Spitze des Rands sind sehr klein. Selbst ein kleiner Offset kann dazu führen, dass Objekte ihre Schatten verlieren (Abbildung 18).

**Abbildung 18. Spitze Ränder führen zu Artefakten, die von tiefen Unterschieden mit Offsets herstammen.**

![Spitze Ränder führen zu Artefakten, die sich aus tiefen Unterschieden mit Offsets herstammen.](images/sharp-edges-cause%20artifacts.jpg)

Schmale Objekte, wie z. B. Wände, sollten auch dann einen Hintergrund haben, wenn sie nie sichtbar sind. Dies erhöht die Tiefenunterschiede.

Es ist auch wichtig sicherzustellen, dass die Richtung der Geometrie korrekt ist. Das heißt, die Außenseite eines Objekts sollte zurück gerichtet sein, und das Innere eines Objekts sollte vorn ausgerichtet sein. Dies ist wichtig für das Rendern mit aktivierter Back-Face-Culling sowie zum Abfangen der Auswirkungen von Tiefenverzerrung.

## <a name="summary"></a>Zusammenfassung

Die in diesem Artikel beschriebenen Techniken können verwendet werden, um die Qualität von Standardschattenkarten zu erhöhen. Der nächste Schritt besteht im Betrachten von Techniken, die gut mit Standardschattenkarten funktionieren können. CSMs werden als überlegenes Verfahren empfohlen, um perspektivische Aliasing zu kontern. Eine genauere Filterung in Prozent oder Varianzschattenkarten können verwendet werden, um Schattenränder zu härten. Weitere Informationen finden Sie im technischen [Karten Cascaded Shadow](/windows/desktop/DxTechArts/cascaded-shadow-maps) Karten.

Donnelly, W. und Lau wies A. [Variance Shadow Karten.](https://portal.acm.org/citation.cfm?doid=1111411.1111440) Symposium on Interactive 3D Graphics, Proceedings of the 2006 Symposium on Interactive 3D Graphics and Games. 2006, S. 161–165.

Igkeit, Woflgang F. Abschnitt 4. Kaskadierte Schatten Karten. ShaderX5, *Erweiterte Renderingtechniken,Verfahren* für das Rendern von ShaderN, Ef, Ed. Charles River Media, Boston, Bostons. 2006. S. 197–206.

Stamminger, Stamminger, und Drettakis, Seit. [Perspective Shadow Karten](https://portal.acm.org/citation.cfm?id=566616). International Conference on Computer Graphics and Interactive Techniques, *Proceedings of the 29th Annual Conference on Computer Graphics and Interactive Techniques*. 2002, S. 557–562.

Wwel, M., Scherzer, D. und Purgatierer, W. [Light Space Perspective Shadow Karten](https://www.cg.tuwien.ac.at/research/vr/lispsm/shadows_egsr2004_revised.pdf). Eurographics Symposium on Rendering. 2004. Überarbeitet am 10. Juni 2005. [Technische Universität Oder](https://www.cg.tuwien.ac.at/research/vr/lispsm/).

 

 
