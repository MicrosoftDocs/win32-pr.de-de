---
title: Allgemeine Artikel zum Verbessern von Tiefenkarten für Schatten
description: Dieser technische Artikel bietet einen Überblick über einige gängige schatteneitenzuordnungs Algorithmen und allgemeine Artefakte und erläutert verschiedene Techniken – im Bereich der Schwierigkeit von Basic bis zwischen –, die verwendet werden können, um die Qualität von standardmäßigen Schatten Zuordnungen zu erhöhen.
ms.assetid: bf994838-a261-0379-9301-eb9b250d216c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8b25507d7f6b8608d4dacf5fab620bc8a3294c7
ms.sourcegitcommit: 218b1ff779402c3ebe1786679e1aa80a5c0d6c95
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730712"
---
# <a name="common-techniques-to-improve-shadow-depth-maps"></a>Allgemeine Artikel zum Verbessern von Tiefenkarten für Schatten

Schatten Zuordnungen, die erstmals in 1978 eingeführt wurden, sind ein gängiges Verfahren zum Hinzufügen von Schatten zu spielen. Drei Jahrzehnte später, trotz der Fortschritte in Hardware und Software, shadoocken von Artefakten – das heißt, dass sich auch die Kanten, perspektivische und andere Genauigkeits Probleme –

Dieser technische Artikel bietet einen Überblick über einige gängige schatteneitenzuordnungs Algorithmen und allgemeine Artefakte und erläutert verschiedene Techniken – im Bereich der Schwierigkeit von Basic bis zwischen –, die verwendet werden können, um die Qualität von standardmäßigen Schatten Zuordnungen zu erhöhen. Das Hinzufügen von grundlegenden Schatten Zuordnungen zu einem Titel ist in der Regel unkompliziert, aber das Verständnis der Nuancen von Schatten Artefakten kann schwierig sein. Dieser technische Artikel ist für den Entwickler von zwischen Grafiken geschrieben, der Shadows implementiert hat, aber nicht vollständig versteht, warum bestimmte Artefakte angezeigt werden und nicht sicher sind, wie Sie diese umgehen können.

Die Auswahl der richtigen Verfahren zum mindern bestimmter Artefakte ist nicht trivial. Wenn schattenkarten Mängel behandelt werden, kann der Unterschied in der Qualität beeindruckend sein (Abbildung 1). Durch eine ordnungsgemäße Implementierung dieser Techniken werden Standard Schatten drastisch verbessert. Die in diesem Artikel erläuterten Verfahren werden im DirectX SDK im Beispiel CascadedShadowMaps11 implementiert.

**Abbildung 1. Schatten mit schweren Artefakten (links) und Schatten nach der Implementierung der in diesem Artikel beschriebenen Verfahren (right)**

![Schatten mit schweren Artefakten (links) und Schatten nach der Implementierung der in diesem Artikel beschriebenen Verfahren (right)](images/shadows-before-and-after.jpg)

## <a name="shadow-depth-maps-review"></a>Überprüfung der Schatten Tiefe-Karten

Der Algorithmus für die Schatten Tiefe ist ein zwei-Pass-Algorithmus. Der erste Durchlauf generiert eine tiefen Zuordnung im Leerraum. Im zweiten Durchlauf wird diese Karte verwendet, um die Tiefe der einzelnen Pixel in einem hellen Raum mit der entsprechenden Tiefe in der tiefenkarte für den hellen Raum zu vergleichen.

**Abbildung 2. Wichtige Teile einer Schatten Szene**

![wichtige Teile einer Schatten Szene](images/key-parts-of-shadow-scene.jpg)

### <a name="pass-1"></a>Durchlauf 1

Die Szene ist in Abbildung 2 dargestellt. Im ersten Durchlauf (Abbildung 3) wird die Geometrie aus der Sicht des Lichts in einen tiefen Puffer gerendert. Genauer gesagt wandelt der Vertex-Shader die Geometrie in einen Licht Ansichts Bereich um.

Das Endergebnis dieses ersten Durchlauf ist ein tiefen Puffer, der die Tiefeninformationen der Szene aus der Sicht des Lichts enthält. Dies kann nun in Pass 2 verwendet werden, um zu bestimmen, welche Pixel aus dem Licht ausgeblendet werden.

**Abbildung 3. Erster Durchlauf der einfachen Schatten Zuordnung**

![erster Durchlauf der einfachen Schatten Zuordnung](images/first-pass-of-basic-hadow-mapping.png)

### <a name="pass-2"></a>Durchlauf 2

Im zweiten Durchlauf (Abbildung 4) transformiert der Vertex-Shader jeden Scheitelpunkt zweimal. Jeder Scheitelpunkt wird in den Ansichts Bereich der Kamera transformiert und als Position an den Pixelshader übermittelt. Jeder Scheitelpunkt wird auch durch die View-Projection-Texture-Matrix des Lichts transformiert und als Textur Koordinate an den Pixelshader übergeben. Die Matrix View-Projection-Texture ist dieselbe Matrix, die zum Rendern der Szene in Pass 1 mit einer zusätzlichen Transformation verwendet wird. Dabei handelt es sich um eine Transformation, mit der die Punkte von Ansichts Raum (– 1 auf 1 in x und Y) skaliert und in den Textur Bereich (0 bis 1 in x und 1 bis 0 in Y) übersetzt werden.

Der Pixelshader empfängt die interinterpolierte Position und die interpoliert-Texturkoordinaten. Alles, was für die Ausführung des tiefen Tests benötigt wird, ist jetzt in dieser Textur Koordinate. Der tiefen Test kann nun ausgeführt werden, indem der tiefen Puffer aus dem ersten Durchlauf mit den X-und Y-Texturkoordinaten indiziert und der resultierende tiefen Wert mit der Z-Textur Koordinate verglichen wird.

**Abbildung 4. Zweiter Durchlauf der grundlegenden Schatten Zuordnung**

![zweiter Durchlauf der grundlegenden Schatten Zuordnung](images/second-pass-of-basic-shadow-mapping.png)

## <a name="shadow-map-artifacts"></a>Schattenkarten Artefakte

Der Algorithmus für die schatteneitenzuordnung ist der am häufigsten verwendete echt zeitalgorithmus für Shadowing, erzeugt jedoch immer noch mehrere Artefakte, die eine Entschärfung erfordern. Die Typen von Artefakten, die auftreten können, werden als nächstes zusammengefasst.

### <a name="perspective-aliasing"></a>Perspektiven Aliasing

Perspektivische Aliasing, ein gängiges artefaktelement, ist in Abbildung 5 dargestellt. Dies tritt auf, wenn die Zuordnung von Pixeln im Anzeigebereich zu texeln in der Schatten Zuordnung kein eins-zu-eins-Verhältnis ist. Dies liegt daran, dass Pixel in der Nähe der nahen Ebene einander näher beieinander liegen und eine höhere schattenkarten Auflösung erfordern.

Abbildung 6 zeigt eine Schatten Zuordnung und eine Ansicht "Frustum". Im Augenblick werden die Pixel näher beieinander angezeigt, und viele Pixel entsprechen denselben Schatten texeln. Die Pixel der äußersten Ebene werden verteilt, wodurch peraliasing der Perspektive reduziert wird.

**Abbildung 5. Aliasing in hoher Perspektive (links) im Vergleich zum Aliasing mit niedriger Perspektive (rechts)**

![Aliasing in hoher Perspektive (links) im Vergleich zum Aliasing mit niedriger Perspektive (rechts)](images/high-perspective-aliasing-vs-low-perspective-aliasing.jpg)

Für das Bild auf der linken Seite ist das Aliasing der Perspektive höher. zu viele Eye-Space-Pixel sind denselben schattenkarten texeln zugeordnet. Im Bild auf der rechten Seite ist das perasing von Perspektiven gering, weil es eine 1:1-Zuordnung zwischen den Augen Raum Pixeln und schattenkarten texeln gibt.

**Abbildung 6. Anzeigen von "Frustum" mit Schatten Zuordnung**

![Anzeigen von "Frustum" mit Schatten Zuordnung](images/view-frustum-with-shadow-map.jpg)

Helle Pixel in der äußersten Ebene stellen ein Aliasing mit niedriger Perspektive dar, und dunkle Pixel in der nahen Ebene stellen ein Aliasing mit hoher Perspektive dar.

Die Auflösung von schattenkarten kann ebenfalls zu hoch sein. Obwohl eine höhere Auflösung weniger bemerkbar ist, kann Sie trotzdem zu kleinen Objekten, wie z. b. Telefonleitungen, führen, die keine Schatten umwandeln. Außerdem kann eine zu hohe Auflösung aufgrund von Textur Zugriffs Mustern schwerwiegende Leistungsprobleme verursachen.

Perspektivische Schatten Zuordnungen (PSMS) und Leerraum-perspektivische Schatten Zuordnungen (lspsms) versuchen, perspektivische Aliasing zu adressieren, indem Sie die Projektions Matrix des Lichts verzerren, um mehr texeln in der Nähe der benötigten Zeit zu platzieren Leider ist keines der beiden Verfahren in der Lage, das Aliasing der Perspektive zu lösen. Die Parametrisierung der Transformation, die erforderlich ist, um den texeln in der Schatten Zuordnung die Augen Raum Pixel zuzuordnen, kann nicht durch eine lineare Neigung gebunden werden. Eine logarithmische Parametrisierung ist erforderlich. Die PSMS-Datei hat zu viele Details in naher Nähe, was dazu führt, dass entfernte Schatten von geringer Qualität oder sogar verschwinden. Lspsms ist eine bessere Aufgabe, einen mittleren Grund zwischen zunehmender Auflösung im Auge zu finden und genug Details für Objekte zu erhalten, die weit entfernt sind. Beide Verfahren werden in manchen Szenen Konfigurationen in orthografischen Schatten entdebugtet. Diese Degeneration kann durch das Rendern einer separaten Schatten Zuordnung für jede Oberfläche der Ansicht "Frustum" ausgeglichen werden, obwohl dies teuer ist. Logarithmische Perspektiven Schatten Zuordnungen (logpsms) erzeugen auch eine separate Zuordnung pro Gesicht der Ansicht. Bei dieser Methode wird die nichtlineare rasterisierung verwendet, um mehr texeln im Auge zu platzieren. Die Hardware der d3d10-und D3D11-Klasse unterstützt keine nichtlineare rasterisierung. Weitere Informationen zu diesen Techniken und Algorithmen finden Sie im Abschnitt "Verweise".

Cascaded Shadow Maps (CSMS) sind die gängigste Technik für den Umgang mit peraliasing von Perspektiven. Obwohl CSMS mit PSMS und lspsms kombiniert werden kann, ist es unnötig. Die Verwendung von CSMS zum Beheben von perspektivischen Aliasing Fehlern wird im Begleitartikel [Cascaded Shadow Maps](/windows/desktop/DxTechArts/cascaded-shadow-maps)behandelt.

### <a name="projective-aliasing"></a>Projektives Aliasing

Das projektives Aliasing ist schwieriger anzusehen als peraliasing von Perspektiven. Die in Abbildung 7 markierten in Abbildung 7 markierten Schatten veranschaulichen Projective Aliasing-Fehler. Das projektives Aliasing tritt auf, wenn die Zuordnung zwischen texeln im Kamera Raum und texeln im Leerraum kein 1: eins-Verhältnis ist. Dies liegt an der Ausrichtung der Geometrie in Bezug auf die helle Kamera. Das projektives Aliasing tritt auf, wenn die tangential Ebene der Geometrie parallel zu den Lichtstrahlen wird.

**Abbildung 7: Hoch projektives Aliasing im Vergleich zu Low-Projective Aliasing**

![hoch projektives Aliasing im Vergleich zu Low-Projective Aliasing](images/high-projective-aliasing-vs-low%20projective-aliasing.jpg)

Techniken zum lindern von perspektivischen Aliasing Fehlern mindern auch das Projective Aliasing. Das Projective Aliasing tritt auf, wenn die Oberflächen normale orthogonal im Licht ist. Diese Oberflächen sollten auf der Grundlage diffuses Beleuchtungs Gleichungen weniger hell empfangen werden.

### <a name="shadow-acne-and-erroneous-self-shadowing"></a>Schatten-Akne und fehlerhafte Self-Shadowing

Schatten-Akne (Abbildung 8), ein Begriff, der mit fehlerhaftem selbst Shadowing Synonym ist, tritt auf, wenn die Schatten Zuordnung die Tiefe über einen ganzen texquantifizierert. Wenn der Shader eine tatsächliche Tiefe mit diesem Wert vergleicht, ist es so wahrscheinlich, dass er sich selbst schattiert, da er unschattiert werden soll.

Ein weiterer Grund für die Schatten-Akne ist, dass sich die texesequenz in einem Leerraum so nah wie die Tiefe der entsprechenden texesequenz in der tiefenkarte befindet, dass bei Genauigkeits Fehlern der tiefen Test fälschlicherweise fehlschlägt Ein Grund für diesen Genauigkeits Unterschied besteht darin, dass die tiefen Zuordnung von der Hardware für die rasterisierung mit fester Funktionsweise berechnet wurde, während die verglichene Tiefe vom Shader berechnet wurde. Projective Aliasing kann auch Schatten-Akne verursachen.

**Abbildung 8. Schatten-Akne-Element**

![Schatten-Akne-Element](images/shadow-acne-artifact.jpg)

Wie im linken Bild gezeigt, haben einige der Pixel den tiefen Test nicht bestanden und die gesprengenen Artefakte und die Muster für das Muster erstellt. Um die fehlerhafte selbst shadonisweise zu reduzieren, sollten die Begrenzungen in der Nähe der Nähe und die weite Ebene für die Leerraum Ansicht Frustum so eng wie möglich berechnet werden. Die auf der Skala basierende Tiefe und andere Typen von Bias sind andere Lösungen, mit denen Schatten-Akne verringert werden.

### <a name="peter-panning"></a>Peter-Panning

Der Begriff *Peter Panning* leitet seinen Namen aus dem Buchstaben eines Children ab, dessen Schatten getrennt wurde und von dem er fliegen konnte. Dieses artefaktelement bewirkt, dass Objekte, die fehlende Schatten haben, von und über der Oberfläche getrennt werden (Abbildung 9).

**Abbildung 9. Peter Panning-artefaktelement**

![Peter schwenken-artefaktelement](images/peter-panning-artifact.jpg)

Im Bild auf der linken Seite wird der Schatten vom Objekt getrennt, wodurch ein Gleit Komma Effekt entsteht.

Eine Methode zum Entfernen von Oberflächen Akne ist das Hinzufügen eines Werts zur Pixelposition im Leerraum. Dies wird als Hinzufügen eines tiefen Offsets bezeichnet. Peter schwenken Ergebnisse, wenn der verwendete tiefen Offset zu groß ist. In diesem Fall bewirkt der tiefen Offset, dass der tiefen Test irrtümlich durchlaufen wird. Wie bei der Schatten-Akne wird Peter Panning erschwert, wenn der tiefen Puffer nicht genügend Genauigkeit hat. Das Berechnen von engen Flächen in naher und weit entfernten Ebenen hilft auch, Peter Panning zu vermeiden.

## <a name="techniques-to-improve-shadow-maps"></a>Techniken zum Verbessern von schattenkarten

Das Hinzufügen von Schatten zu einem Titel ist ein Prozess. Der erste Schritt besteht darin, grundlegende Schatten Zuordnungen zu erhalten. Die zweite Möglichkeit besteht darin sicherzustellen, dass alle grundlegenden Berechnungen optimal durchgeführt werden: frusta passt so eng wie möglich an, nah-und ganz nach Ebenen passen eng an, wenn eine Neigung skaliert ist und so weiter. Nachdem Sie die grundlegenden Schatten aktiviert und so gut wie möglich betrachtet haben, hat der Entwickler eine bessere Vorstellung davon, welche Algorithmen erforderlich sind, um die Schatten in eine ausreichende Treue zu bringen. Grundlegende Tipps, die möglicherweise erforderlich sind, um grundlegende schattenkarten zu erhalten, die sich am besten in diesem Abschnitt befinden.

### <a name="slope-scale-depth-bias"></a>Slope-Scale Tiefe-Abweichung

Wie bereits erwähnt, kann selbst Shadowing zu Schatten-Akne führen. Das Hinzufügen zu einer zu großen Abweichung kann dazu führen, dass Peter schwenken. Außerdem erleiden Polygone mit steilen Pisten (relativ zum Licht) mehr von projectivem Aliasing als Polygone mit flachen Pisten (relativ zum Licht). Daher kann jeder tiefen Zuordnungs Wert abhängig von der Neigung des Polygons relativ zum Licht einen anderen Offset erfordern.

Direct3D 10-Hardware bietet die Möglichkeit, ein Polygon auf der Grundlage der Neigung in Bezug auf die Ansichts Richtung zu überprüfen. Dies hat den Effekt, dass eine große Abweichung auf ein Polygon angewendet wird, das Edge-on in der Lichtrichtung angezeigt wird, aber keine Abweichung auf ein Polygon direkt mit dem Licht anwendet. Abbildung 10 zeigt, wie sich zwei benachbarte Pixel zwischen Schatten und unshadowing beim Testen gegen dieselbe unausgewogene Steigung unterschiedlichen können.

**Abbildung 10. Horizontal skalierte Tiefe-Bias im Vergleich zu einer unausgewogenen Tiefe**

![horizontal skalierte Tiefe-Bias im Vergleich zu einer unausgewogenen Tiefe](images/slope-scaled-depth-bias-compared-to-unbiased-depth.png)

### <a name="calculating-a-tight-projection"></a>Berechnen einer engen Projektion

Durch eine enge Anpassung der Lichtprojektion an die Ansicht Frust wird die schattenkarten Abdeckung vergrößert. Abbildung 11 zeigt, dass die Verwendung einer beliebigen Projektion oder die Anpassung der Projektion an die Szenen Grenzen zu einem höheren perspektivischen Aliasing führt.

**Abbildung 11. Beliebige Schatten-Frustum und Schatten Frust an Szene anpassen**

![beliebige Schatten-Frustum und Schatten Frust an Szene anpassen](images/arbitrary-shadow-frustum-and-shadow-frustum-fit-to-scene.jpg)

Die Ansicht ist aus der Sicht des Lichts entfernt. Der Wert von "Trapez" stellt den Frustum der Ansichts Kamera dar. Das Raster, das über dem Bild gezeichnet wird, stellt die schattenkarte dar. Das Bild auf der rechten Seite zeigt, dass dieselbe Auflösungs Schatten Zuordnung eine größere texesequenz erstellt, wenn diese enger an die Szene angepasst wird.

In Abbildung 12 werden Frustums veranschaulicht, die ordnungsgemäß geeignet sind. Zum Berechnen der Projektion werden die acht Punkte, aus denen die Ansicht hervorgeht, in einen Leerraum transformiert. Als nächstes werden die Mindest-und Höchstwerte in X und Y gefunden. Diese Werte bilden die Begrenzungen für eine orthografische Projektion.

**Abbildung 12. Schatten Projektion passend zum Anzeigen von Frustum**

![Schatten Projektion passend zum Anzeigen von Frustum](images/shadow-projection-fit-to-view-frustum.jpg)

Es ist auch möglich, die Frustration auf die Szene aabb zu setzen, um eine strengere Grenze zu erzielen. Dies wird nicht in allen Fällen empfohlen, da dadurch die Größe der Projektion der hellen Kamera von Frame zu Frame geändert werden kann. Viele Techniken, wie z. b. die, die im Abschnitt Verschieben der hellen Texel-Sized Inkrementen beschrieben werden, führen zu besseren Ergebnissen, wenn die Größe der Lichtprojektion in jedem Frame konstant bleibt.

### <a name="calculating-the-near-plane-and-far-plane"></a>Berechnen der nahen und der äußersten Ebene

Die nahe Ebene und die weite Ebene sind die letzten Elemente, die zum Berechnen der Projektions Matrix erforderlich sind. Umso genauer sind die Ebenen, desto genauer sind die Werte im tiefen Puffer.

Der tiefen Puffer kann ein 16-Bit-, 24-Bit-oder 32-Bit-Wert mit Werten zwischen 0 und 1 sein. Im Allgemeinen sind tiefen Puffer ein fester Punkt, wobei die Werte in der Nähe der Near-Ebene genauer gruppiert sind als die Werte in der Nähe der äußersten Ebene. Der Genauigkeits Grad, der für den tiefen Puffer verfügbar ist, wird durch das Verhältnis zwischen der nahen Ebene und der äußersten Ebene bestimmt. Durch die Verwendung der fast-und Far-Ebene für die enge Prüfung kann die Verwendung eines 16-Bit-Tiefen Puffers ermöglicht werden. Ein 16-Bit-Tiefen Puffer könnte die Verwendung des Arbeitsspeichers verringern und gleichzeitig die Verarbeitungsgeschwindigkeit erhöhen.

### <a name="aabb-based-near-plane-and-far-plane"></a>AABB-Based in der Nähe der Ebene und der äußersten Ebene

Eine einfache und naive Möglichkeit zum Berechnen der Nähe und der äußersten Ebene besteht darin, das umgebende Volume der Szene in Leerraum umzuwandeln. Der kleinste z-Koordinaten Wert ist die nahe Ebene, und der größte z-Koordinaten Wert ist die weite Ebene. Für viele Konfigurationen der Szene und des Lichts ist dieser Ansatz ausreichend. Der schlimmste Fall kann jedoch zu einem erheblichen Genauigkeits Verlust im tiefen Puffer führen. Abbildung 13 zeigt ein solches Szenario. Hier ist der Bereich der Near-Ebene bis hin zur äußersten Ebene viermal größer als notwendig.

Die Ansicht "Frustum" in Abbildung 13 wurde absichtlich als klein gewählt. In einer sehr großen Szene, die aus der Ansichts Kamera reicht, wird eine kleine Ansicht von "Frustum" angezeigt. Die Verwendung der Szene aabb für die Near-und Far-Plane ist nicht optimal. Der CSM-Algorithmus, der im Artikel [Cascaded Shadow Maps (Cascaded Shadow Maps](/windows/desktop/DxTechArts/cascaded-shadow-maps) ) beschrieben wird, muss für sehr kleine Frustrationen fast und weit berechnen.

**Abbildung 13. Near und Far Plane basierend auf der Szene aabb**

![Near und Far Plane basierend auf der Szene aabb](images/near-far-%20planes-based-on-scene-aabb.jpg)

### <a name="frustum-based-near-plane-and-far-plane"></a>Frustum-Based in der Nähe der Ebene und der äußersten Ebene

Ein weiteres Verfahren zum Berechnen der Near-und Far-Ebene besteht darin, die Frustration in Leerraum zu transformieren und die minimalen und maximalen Werte in Z als die Near-und all-Ebenen zu verwenden. In Abbildung 14 werden die beiden Probleme mit diesem Ansatz veranschaulicht. Zuerst ist die Berechnung zu konservativ, wie Sie angezeigt wird, wenn der Frustum die Geometrie der Szene überschreitet. Zweitens könnte die nahe Ebene zu eng sein, was dazu führt, dass Schatten-Caster zugeschnitten werden.

**Abbildung 14. Near und all-Ebenen, die ausschließlich auf der Anzeige von Frustum basieren**

![Near und all-Ebenen, die ausschließlich auf der Anzeige von Frustum basieren](images/near-far-planes-based-solely-on-view-frustum.jpg)

### <a name="light-frustum-intersected-with-scene-to-calculate-near-and-far-planes"></a>Light Frustum mit der Szene, um nahe-und fern Ebenen zu berechnen

Die richtige Methode zum Berechnen der Near-und Far-Ebenen ist in Abbildung 15 dargestellt. Vier der Ebenen der orthografischen hell Frustration wurden mit dem minimal-und Maximalwert der X-und Y-Koordinaten der Ansicht im Leerraum berechnet. Die letzten zwei Ebenen der orthogonalen Ansicht "Frustum" sind die nahe und die äußersten Ebenen. Um diese Ebenen zu finden, werden die Begrenzungen der Szene anhand der vier bekannten hell Frustum-Ebenen abgeschnitten. Die kleinsten und größten Z-Werte aus der neu abgeschnittenen Grenze stellen die Near-Ebene bzw. die weite Ebene dar.

Der Code, der diesen Vorgang ausführt, befindet sich im CascadedShadowMaps11-Beispiel. Die acht Punkte, aus denen die aabb der Welt besteht, werden in einen Leerraum transformiert. Durch das Transformieren der Punkte in den Leerraum werden die clippingtests vereinfacht. Die vier bekannten Flächen der hell Frustration können nun als Linien dargestellt werden. Die Kulissen des umgebenden Volumes im Leerraum können als sechs viereckale dargestellt werden. Diese 6 Vierecke können dann für Dreieck basiertes Clipping in 12 Dreiecke umgewandelt werden. Die Dreiecke werden anhand der bekannten Flächen der Ansicht "Frustum" abgeschnitten (Hierbei handelt es sich um horizontale und vertikale Linien in X und Y im Leerraum). Wenn in X und Y ein Schnittpunkt gefunden wird, wird das 3D-Dreieck an diesem Punkt abgeschnitten. Die minimalen und maximalen Z-Werte aller ausgeschnittenen Dreiecke sind die nahe Ebene und die weite Ebene. Das CascadedShadowMaps11-Beispiel zeigt, wie dieses Clipping in der **computenearandfar** -Funktion durchgeführt wird.

Es gibt zwei weitere Techniken, die verwendet werden können, um die in der Nähe und in der Ferne Anzahl möglicher Ebenen zu berechnen. Diese Techniken werden im caskadetten dshadowmaps-Beispiel nicht angezeigt.

-   Sogar strengere Near-und Far-Ebenen können berechnet werden, indem eine Hierarchie einer Szene oder einzelne Objekte in einer Szene gegen den hellen Frust angezeigt werden. Dies wäre rechnerisch komplexer. Dies ist zwar nicht im CascadedShadowMaps11-Beispiel dargestellt, dies kann jedoch ein gültiges Verfahren für einige Kacheln sein.
-   Die weitaus mögliche Ebene kann berechnet werden, indem Sie die Mindestanzahl von:

    -   Die größte Tiefe der Ansicht für die Frustration im Leerraum.
    -   Die größte Tiefe der Schnittmenge der Ansicht Frustum und der Szene aabb.

Diese Vorgehensweise kann problematisch sein, wenn Sie mit kaskadierenden Schatten Zuordnungen verwendet wird, in denen es möglich ist, außerhalb einer Ansicht zu indizieren. In diesem Fall fehlt in der Schatten Zuordnung die Geometrie.

**Abbildung 15. Near und Far Plane basierend auf der Schnittmenge der vier berechneten Flächen der hellen Frustration und der umgebenden Geometrie der Szene.**

![Near und Far Plane basierend auf der Schnittmenge der vier berechneten Flächen der hellen Frustration und der umgebenden Geometrie der Szene.](images/near-far-plane-based-on-intersection-of-four.jpg)

### <a name="moving-the-light-in-texel-sized-increments"></a>Verschieben des Lichts in Texel-Sized Inkrementen

Ein gängiges Element in Schatten Zuordnungen ist der schimmernde Rand Effekt. Wenn die Kamera bewegt wird, werden die Pixel entlang der Ränder der Shadows heller und Darken. Dies kann in immer noch Bildern nicht angezeigt werden, aber es ist sehr bemerkbar und ablenkend in Echtzeit. In Abbildung 16 wird dieses Problem hervorgehoben, und Abbildung 17 zeigt, wie die Schatten Ränder aussehen sollten.

Der Fehler beim schimmernden Edge tritt auf, wenn die Licht Projektions Matrix bei jedem Verschieben der Kamera neu berechnet wird. Dies erzeugt feine Unterschiede in den generierten Schatten Zuordnungen. Alle folgenden Faktoren können die Matrix beeinflussen, die zum Binden der Szene erstellt wurde.

-   Größe der Ansicht "Frustum"
-   Ausrichtung der Ansicht "Frustum"
-   Speicherort des Lichts
-   Speicherort der Kamera

Jedes Mal, wenn sich diese Matrix ändert, können sich die Schatten Ränder ändern.

**Abbildung 16. Schimmernde Schatten Ränder**

![schimmernde Schatten Ränder](images/shimmering-shadow-edges.jpg)

Die Pixel entlang des Schattens treten ein und aus Schatten, wenn die Kamera von links nach rechts bewegt wird.

**Abbildung 17. Schatten ohne schimmernde Kanten**

![Schatten ohne schimmernde Kanten](images/shadows-without-shimmering-edges.jpg)

Die Schatten Ränder bleiben konstant, wenn die Kamera von links nach rechts bewegt wird.

Bei direktionalen Lichtern besteht die Lösung für dieses Problem darin, den minimalen/maximalen Wert in X und Y (aus den orthografischen Projektions Begrenzungen besteht) auf die Pixelgrößen Inkremente zu runden. Dies kann mit einem Teilungs Vorgang, einem Floor-Vorgang und einem Multiplikations Vorgang durchgeführt werden.


```C++
        vLightCameraOrthographicMin /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMin = XMVectorFloor( vLightCameraOrthographicMin );
        vLightCameraOrthographicMin *= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax /= vWorldUnitsPerTexel;
        vLightCameraOrthographicMax = XMVectorFloor( vLightCameraOrthographicMax );
        vLightCameraOrthographicMax *= vWorldUnitsPerTexel;
```



Der vworldunitspertex-Wert wird berechnet, indem eine Begrenzung der Ansicht "Frustum" verwendet und durch die Puffergröße aufgeteilt wird.


```C++
        FLOAT fWorldUnitsPerTexel = fCascadeBound /
        (float)m_CopyOfCascadeConfig.m_iBufferSize;
        vWorldUnitsPerTexel = XMVectorSet( fWorldUnitsPerTexel, fWorldUnitsPerTexel,                            0.0f, 0.0f );
```



Das umschließende der maximalen Größe der Ansicht "Frustum" führt zu einer lockeren Anpassung der orthografischen Projektion.

Es ist wichtig zu beachten, dass die Textur bei der Verwendung dieses Verfahrens 1 Pixel größer ist als Breite und Höhe. Dadurch werden Schatten Koordinaten von der Indizierung außerhalb der Schatten Zuordnung bewahrt.

### <a name="back-face-and-front-face"></a>Rückseite und Vorderseite

Schatten Zuordnungen sollten mit der standardmäßigen Hintergrund Erkennung gerendert werden, einem Prozess, der die rasterisierung von Objekten überspringt, die der Viewer nicht sehen kann, und das Rendern der Szene beschleunigt. Eine weitere gängige Option besteht darin, Schatten Zuordnungen mit aktiviertem Front-Face-culeln zu Rendering Das Argument hierfür ist, dass es bei selbst shadobau hilfreich ist, da die Geometrie, die die Rückseite von Objekten bilden, etwas ausgeglichen ist. Bei dieser Idee gibt es zwei Probleme.

-   Alle Objekte mit unsachgemäßer Vorder-oder Hintergrund Geometrie verursachen Artefakte in der Schatten Zuordnung. Wenn jedoch eine falsche Vorder-oder Hintergrund Geometrie vorhanden ist, kann dies zu anderen Problemen führen. Daher kann es sicher sein, dass die Front-und Hintergrund Geometrie ordnungsgemäß ausgeführt wird. Es ist möglicherweise nicht praktikabel, Hinterflächen für Sprite-basierte Geometrie wie z. b. Laub zu erstellen.
-   Peter Panning und Schatten Lücken in der Nähe der Basis von Objekten, wie z. b. Wände, treten eher auf, weil die Schatten Tiefe nicht zu klein ist.

### <a name="shadow-mapfriendly-geometry"></a>Schattenmap – freundliche Geometrie

Das Erstellen von Geometrie, die in schattenkarten gut funktioniert, bietet mehr Flexibilität bei der Bekämpfung von Artefakten wie Peter Panning und Schatten-Akne.

Fest Kanten sind für selbst shadobau problematisch. Der tiefen Unterschied in der Nähe der Spitze des Edge ist sehr gering. Selbst ein kleiner Offset kann bewirken, dass Objekte ihre Schatten verlieren (Abbildung 18).

**Abbildung 18. Spitzen Ränder bewirken Artefakte, die aus geringer Tiefe Differenz mit Offsets resultieren**

![Spitzen Ränder bewirken Artefakte, die aus geringer Tiefe Differenz mit Offsets resultieren](images/sharp-edges-cause%20artifacts.jpg)

Schmale Objekte wie z. b. Wände sollten über Backs verfügen, auch wenn Sie nie sichtbar sind. Dadurch wird die Tiefe der Tiefe erhöht.

Außerdem ist es wichtig sicherzustellen, dass die Richtung der Geometrie korrekt ist. Das heißt, der Außenbereich eines Objekts sollte sich im Hintergrund befinden, und der Innere eines Objekts sollte sich im Vordergrund befinden. Dies ist wichtig für das Rendering mit aktivierter Hintergrund Erkennung sowie für die Bekämpfung der Auswirkungen der tiefen Abweichung.

## <a name="summary"></a>Zusammenfassung

Die in diesem Artikel beschriebenen Verfahren können verwendet werden, um die Qualität von Standard Schatten Zuordnungen zu erhöhen. Der nächste Schritt besteht darin, sich mit den standardmäßigen Schatten Zuordnungen Techniken anzusehen, die gut funktionieren. CSMS werden als eine übergeordnete Technik empfohlen, um Perspektiven Aliasing zu bekämpfen. Mit einem Prozentsatz an näherem filtern oder Varianz Schatten Maps können Schatten Ränder weich gezogen werden. Weitere Informationen finden Sie im technischen Artikel [Cascaded Shadow Maps](/windows/desktop/DxTechArts/cascaded-shadow-maps) .

Donnelly, W. und Lauritzen, A. [Varianz Schatten](https://portal.acm.org/citation.cfm?doid=1111411.1111440)Zuordnungen. Symposium für interaktive 3D-Grafiken, Verfahren des 2006-Symposiums zu interaktiven 3D-Grafiken und-spielen. 2006, pp. 161 – 165.

Engel, woflgang F., Abschnitt 4. Kaskadierenden Schatten Zuordnungen. ShaderX5, *Erweiterte renderingtechniken*, Wolfgang F. Engel, Ed. Charles River Media, Boston, Massachusetts. 2006. PP. 197 – 206.

Stamminger, Marc und drettakis, George. [Perspektiven Schatten](https://portal.acm.org/citation.cfm?id=566616)Zuordnungen. Internationale Konferenz zu Computergrafiken und interaktiven Verfahren, *Verfahren der 29. jährlichen Konferenz zu Computergrafiken und interaktiven Techniken*. 2002, PP 557 – 562.

"Wimmer", "M.", "Scherzer", "D." und "Purgathofer", W. [Leerraum-Perspektiven schattenkarten](https://www.cg.tuwien.ac.at/research/vr/lispsm/shadows_egsr2004_revised.pdf) Das Euro graphics-Symposium zum Rendern. 2004. Überarbeitet am 10. Juni 2005. Die [Technische Universität Wien](https://www.cg.tuwien.ac.at/research/vr/lispsm/).

 

 
