---
title: Überlappende Schattenkarten
description: Cascaded Shadow Maps (CSMS) sind die beste Möglichkeit, einen der am häufigsten auftretenden Fehler mit Shadowing-Aliasing zu bekämpfen.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae70433f97f33c3cc28af8e282b14ea1f513cf4d
ms.sourcegitcommit: 54db9e6a00a5c8f68e7c1a16b8c6d4943374498c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "106372802"
---
# <a name="cascaded-shadow-maps"></a>Überlappende Schattenkarten

Cascaded Shadow Maps (CSMS) sind die beste Möglichkeit, einen der am häufigsten auftretenden Fehler mit Shadowing: Perspective Aliasing zu bekämpfen. In diesem technischen Artikel, bei dem davon ausgegangen wird, dass der Reader mit der Schatten Zuordnung vertraut ist, wird das Thema CSMS behandelt. Diese Parameter:

-   erläutert die Komplexität von CSMS.
-   Gibt Details zu den möglichen Variationen der CSM-Algorithmen an.
-   Beschreibt die beiden gängigsten Filtertechniken – PCF-Filter (Prozent) und das Filtern mit Varianz Schatten Maps (VSMs).
-   identifiziert und behandelt einige der häufigen Fehler beim Hinzufügen von Filtern zu CSMS. immer
-   zeigt, wie CSMS Direct3D 10 bis Direct3D 11-Hardware zugeordnet wird.

Den in diesem Artikel verwendeten Code finden Sie im DirectX Software Development Kit (SDK) in den CascadedShadowMaps11-und VarianceShadows11-Beispielen. Dieser Artikel erweist sich nach der Implementierung der Techniken, die im technischen Artikel [zum Verbessern von Schatten tiefen Maps](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps)behandelt werden, am nützlichsten.

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a>Kaskadierbare Schatten Zuordnungen und perspektivische Aliasing

Perspektiven Aliasing in einer Schatten Zuordnung ist eines der schwierigsten Probleme, die gelöst werden müssen. Im technischen Artikel werden allgemeine Techniken zum Verbessern von Schatten tiefen Zuordnungen, Perspektiven Aliasing und einige Ansätze zum Beheben des Problems identifiziert. In der Praxis sind CSMS tendenziell die beste Lösung und werden häufig in modernen Spielen eingesetzt.

Das grundlegende Konzept von CSMS ist leicht verständlich. Für verschiedene Bereiche der Kamera "Frustum" sind Schatten Zuordnungen mit unterschiedlichen Auflösungen erforderlich. Objekte, die sich in der Nähe des Auges befinden, erfordern eine höhere Auflösung als mehr entfernte Objekte. Wenn sich das Auge sehr nahe an der Geometrie bewegt, kann es sein, dass die Pixel, die dem Augenblick am nächsten sind, so viel Auflösung erfordern, dass auch eine 4096 × 4096-Schatten Zuordnung unzureichend ist.

Die grundlegende Idee von CSMS besteht darin, die Frustration in mehrere frusta zu partitionieren. Für jede subfrustum wird eine schattenkarte gerendert. der Pixel-Shader gibt dann eine Stichprobe aus der Zuordnung aus, die am ehesten mit der erforderlichen Auflösung übereinstimmt (Abbildung 2).

**Abbildung 1. Schattenkarten Abdeckung**

![schattenkarten Abdeckung](images/shadow-map-coverage.png)

In Abbildung 1 wird die Qualität (von links nach rechts) von der höchsten zur niedrigsten angezeigt. Die Reihe der Raster, die Schatten Zuordnungen mit einer Ansicht "Frustum" (umgekehrter Kegel in rot) darstellen, zeigt, wie die Pixel Abdeckung von unterschiedlichen Auflösungs schattenkarten betroffen ist. Schatten sind von der höchsten Qualität (weiße Pixel), wenn ein 1:1-Verhältnis für die Zuordnung von Pixeln in einem hellen Raum zu texeln in der schattenkarte vorhanden ist. Perspektivische Aliasing erfolgt in Form von großen Blocktextur Zuordnungen (linkes Bild), wenn zu viele Pixel dem gleichen Schatten Texel zugeordnet werden. Wenn die Schatten Zuordnung zu groß ist, wird Sie untersucht. In diesem Fall werden texeln übersprungen, schimmernde Artefakte werden eingeführt, und die Leistung ist beeinträchtigt.

**Abbildung 2. CSM-Schatten Qualität**

![CSM-Schatten Qualität](images/csm-shadow-quality.png)

Abbildung 2 zeigt Ausschnitte aus dem Abschnitt mit der höchsten Qualität in den einzelnen schattenkarten in Abbildung 1. Die Schatten Zuordnung mit den am weitesten links positionierte Pixel (auf der Spitze) ist das nächste Auge. Technisch gesehen handelt es sich hierbei um Zuordnungen derselben Größe, wobei weiß und grau verwendet werden, um den Erfolg der kaskadierenden schattenkarte zu veranschaulichen. Weiß ist ideal, da es eine gute Abdeckung anzeigt – ein 1:1-Verhältnis für die Augen Raum Pixel und schattenkarten texeln.

CSMS erfordert die folgenden Schritte pro Frame.

1.  Partitionieren Sie den Frustum in subfrusta.
2.  Berechnen Sie eine orthografische Projektion für jede subfrustum.
3.  Rendering einer Schatten Zuordnung für jede subfrustum.
4.  Rendering der Szene.

    1.  Binden der Schatten Zuordnungen und Rendering.
    2.  Der Vertex-Shader führt Folgendes aus:

        -   Berechnet Texturkoordinaten für die einzelnen hellen subfrustum (es sei denn, die erforderliche Textur Koordinate wird im Pixelshader berechnet).
        -   Transformiert und beleuchtet den Scheitelpunkt usw.

    3.  Der Pixelshader führt Folgendes aus:

        -   Bestimmt die richtige Schatten Zuordnung.
        -   Transformiert die Texturkoordinaten bei Bedarf.
        -   Gibt eine Stichprobenentnahme aus.
        -   Leuchtet das Pixel.

## <a name="partitioning-the-frustum"></a>Partitionierung von Frustum

Die Partitionierung von "Frustum" ist das Erstellen von "subfrusta". Ein Verfahren zum Aufteilen der Frustration besteht darin, Intervalle zwischen 0 und 100 Prozent in der Z-Richtung zu berechnen. Jedes Intervall stellt dann eine nahe Ebene und eine weite Ebene als Prozentsatz der Z-Achse dar.

**Abbildung 3. Willkürlich partitionierte Frustums anzeigen**

![willkürlich partitionierte Frustums anzeigen](images/view-frustums-partitioned-arbitrarily.png)

In der Praxis bewirkt das Neuberechnen der Frustum-Teilungen pro Frame, dass Schatten Ränder zu Shimmer werden. Im Allgemeinen wird die Verwendung eines statischen Satzes von kaskadierenden Intervallen pro Szenario empfohlen. In diesem Szenario wird das Intervall entlang der Z-Achse verwendet, um einen subfrustum zu beschreiben, der beim Partitionieren von Frustum auftritt. Das Bestimmen der richtigen Größen Intervalle für eine bestimmte Szene hängt von mehreren Faktoren ab.

### <a name="orientation-of-the-scene-geometry"></a>Ausrichtung der Szene Geometrie

In Bezug auf die Szenen Geometrie wirkt sich die Kameraausrichtung auf die Auswahl der Cascade Interval aus. Beispielsweise hat eine Kamera, wie z. b. eine Boden Kamera in einem Fußballspiel, einen anderen statischen Satz an kaskadierenden Intervallen als eine Kamera im Himmel.

Abbildung 4 zeigt einige verschiedene Kameras und die jeweiligen Partitionen. Wenn der Z-Bereich der Szene sehr groß ist, sind mehr geteilte Ebenen erforderlich. Wenn sich das Auge z. b. sehr nahe der Grundebene befindet, aber entfernte Objekte weiterhin sichtbar sind, können mehrere kaskadierende erforderlich sein. Die Unterteilung der Frustum-Klasse, sodass sich mehr Teilungen in naher Nähe befinden (wobei Perspektiven Aliasing den schnellsten ändert), ist ebenfalls wertvoll. Wenn der größte Teil der Geometrie in einen kleinen Abschnitt (z. b. eine Verwaltungs Ansicht oder ein Flugsimulator) der Ansicht "Frustum" gepuffert wird, sind weniger kaskadierende erforderlich.

**Abbildung 4. Für verschiedene Konfigurationen sind unterschiedliche Frustum-Teilungen erforderlich**

![für verschiedene Konfigurationen sind unterschiedliche Frustum-Teilungen erforderlich](images/different-configurations-require-different-frustum-splits.png)

Linken Wenn Geometry einen hohen dynamischen Bereich in Z hat, sind viele kaskadierende erforderlich. Tagesstätte Wenn die Geometrie einen niedrigen dynamischen Bereich in Z aufweist, gibt es nur wenig Vorteile von mehreren Frustums. Rechten Wenn der dynamische Bereich Mittel ist, werden nur drei Partitionen benötigt.

### <a name="orientation-of-the-light-and-the-camera"></a>Ausrichtung des Lichts und der Kamera

Die Projektions Matrix der einzelnen kaskadieren ist eng um die zugehörige subfrustum-Klasse abgestimmt. In Konfigurationen, in denen die Ansichts Kamera und die Licht Richtungen orthogonal sind, kann das kaskadierende-Objekt eng mit geringem Überlappungs Aufwand angepasst werden. Die Überlappung wird größer, wenn sich das Licht und die Ansichts Kamera in eine parallele Ausrichtung bewegen (Abbildung 5). Wenn das Licht und die Ansichts Kamera fast parallel sind, wird es als "Dueling frusta" bezeichnet und ist ein sehr hartes Szenario für die meisten shadodown-Algorithmen. Es ist nicht ungewöhnlich, das Licht und die Kamera einzuschränken, damit dieses Szenario nicht auftritt. CSMS sind jedoch viel besser als viele andere Algorithmen in diesem Szenario.

**Abbildung 5. Die kaskadierte Überlappung nimmt zu, wenn die Richtung der Kamera parallel verläuft**

![die kaskadierte Überlappung nimmt zu, wenn die Richtung der Kamera parallel verläuft](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

Viele CSM-Implementierungen verwenden "frusta" mit fester Größe. Der Pixelshader kann die Z-Tiefe verwenden, um in das Bytearray zu indizieren, wenn die Frustum in Intervallen fester Größe aufgeteilt wird.

## <a name="calculating-a-view-frustum-bound"></a>Berechnen einer View-Frustum gebundenen

Nachdem die Frustum-Intervalle ausgewählt wurden, wird der subfrusta mit einem von zwei Werten erstellt: an Szene anpassen und an Cascade anpassen.

### <a name="fit-to-scene"></a>An Szene anpassen

Alle Frustrationen können mit der gleichen Nähe erstellt werden. Dies erzwingt eine Überschneidung der kaskadiert. Mit dem CascadedShadowMaps11-Beispiel wird diese Technik an Scene angepasst.

### <a name="fit-to-cascade"></a>An Cascade anpassen

Alternativ kann frusta mit dem tatsächlichen Partitions Intervall erstellt werden, das als near-und Far-Plane verwendet wird. Dies führt zu einer engeren Anpassung, aber degeneriert, damit Sie im Fall von Dueling frusta an die Szene angepasst wird. Mit den CascadedShadowMaps11-Beispielen wird diese Technik an Cascade (CASCADE) angepasst.

Diese beiden Methoden sind in Abbildung 6 dargestellt. An Cascade anpassen verschwendet weniger Auflösung. Das Problem bei der kaskadierenden Verwendung besteht darin, dass die orthografische Projektion basierend auf der Ausrichtung der Ansicht Frust vergrößert und verkleinert wird. Die Methode an Szene anpassen füllt die orthografische Projektion um die maximale Größe der Ansicht aus, um die Artefakte zu entfernen, die beim Verschieben der Ansichts Kamera angezeigt werden. [Häufig auftretende Techniken zum Verbessern von Schatten tiefen](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) Zuordnungen adressiert die Elemente, die angezeigt werden, wenn sich das Licht im Abschnitt "Verschieben des Lichts in in Textteil größeren Schritten" bewegt.

**Abbildung 6. An Szene anpassen und an Cascade anpassen**

![an Szene anpassen und an Cascade anpassen](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a>Schattenmap

Das CascadedShadowMaps11-Beispiel rendert die Schatten Zuordnungen in einem großen Puffer. Dies liegt daran, dass PCF für Textur Arrays eine Direct3D 10,1-Funktion ist. Für jede Cascade wird ein Viewport erstellt, der den Abschnitt des tiefen Puffers abdeckt, der dieser Cascade-Komponente entspricht. Ein NULL-Pixelshader ist gebunden, da nur die Tiefe benötigt wird. Zum Schluss werden die richtigen Viewports und Schatten Matrizen für jede Cascade festgelegt, da die tiefen Zuordnungen nacheinander in den Haupt Schatten Puffer gerendert werden.

## <a name="render-the-scene"></a>Szene Rendering

Der Puffer, der die Schatten enthält, ist nun an den Pixelshader gebunden. Es gibt zwei Methoden, um die im CascadedShadowMaps11-Beispiel implementierte Cascade auszuwählen. Diese beiden Methoden werden mit Shader-Code erläutert.

### <a name="interval-based-cascade-selection"></a>Interval-Based Cascade-Auswahl

**Abbildung 7: Intervall basierte Cascade-Auswahl**

![Intervall basierte Cascade-Auswahl](images/interval-based-cascade-selection.jpg)

In der Intervall basierten Auswahl (Abbildung 7) berechnet der Vertexshader die Position im Raum des Scheitel Punkts.


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



Der Pixelshader empfängt die interinterpolierte Tiefe.


```C++
fCurrentPixelDepth = Input.vDepth;
```



Bei der Intervall basierten kaskadierenden Auswahl werden ein Vektor Vergleich und ein Punktprodukt verwendet, um die richtige cacade zu bestimmen. Das \_ Flag Cascade Count \_ gibt die Anzahl der Cascades an. Mit den m-Werten für die Datei "f" wird \_ \_ die Ansicht "Frustum-Partitionen" eingeschränkt. Nach dem Vergleich enthält der-Vergleichswert den Wert 1, wobei das aktuelle Pixel größer als die Barriere und der Wert 0 ist, wenn die aktuelle Cascade kleiner ist. Ein Punktprodukt fasst diese Werte in einem Array Index zusammen.


```C++
        float4 vCurrentPixelDepth = Input.vDepth;
        float4 fComparison = ( vCurrentPixelDepth > m_fCascadeFrustumsEyeSpaceDepths_data[0]);
        float fIndex = dot(
        float4( CASCADE_COUNT_FLAG > 0,
        CASCADE_COUNT_FLAG > 1,
        CASCADE_COUNT_FLAG > 2,
        CASCADE_COUNT_FLAG > 3)
        , fComparison );

        fIndex = min( fIndex, CASCADE_COUNT_FLAG );
        iCurrentCascadeIndex = (int)fIndex;
```



Nachdem die CASCADE-Option ausgewählt wurde, muss die Textur Koordinate in die korrekte kaskadierte Transformation transformiert werden.


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



Diese Textur Koordinate wird dann verwendet, um eine Stichprobe der Textur mit der X-Koordinate und der Y-Koordinate zu verwenden. Die Z-Koordinate wird für den abschließenden tiefen Vergleich verwendet.

### <a name="map-based-cascade-selection"></a>Map-Based Cascade-Auswahl

Kartenbasierte Auswahl (Abbildung 8) testet die vier Seiten des kaskaders, um die enge Zuordnung zu finden, die das jeweilige Pixel abdeckt. Anstatt die Position im Raum der Welt zu berechnen, berechnet der Vertexshader die Position des Ansichts Raums für jede Cascade. Der Pixelshader durchläuft die kaskadierende, um die Texturkoordinaten zu skalieren und zu verschieben, damit Sie die aktuelle Cascade-Elemente indizieren. Die Textur Koordinate wird dann anhand der Textur Begrenzungen getestet. Wenn die X-und Y-Werte der Textur Koordinate in eine Cascade-Struktur fallen, werden Sie verwendet, um eine Stichprobe der Textur zu verwenden. Die Z-Koordinate wird für den abschließenden tiefen Vergleich verwendet.

**Abbildung 8. Kartenbasierte Cascade-Auswahl**

![kartenbasierte Cascade-Auswahl](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a>Interval-Based Auswahl und Map-Based Auswahl

Die Intervall basierte Auswahl ist etwas schneller als die kartenbasierte Auswahl, da die kaskadierte Auswahl direkt erfolgen kann. Die kartenbasierte Auswahl muss die Textur Koordinate mit den kaskadierenden Begrenzungen überschneiden.

Bei der kartenbasierten Auswahl wird die Cascade-Funktion effizienter verwendet, wenn Schatten Zuordnungen nicht perfekt ausgerichtet werden (siehe Abbildung 8).

## <a name="blend-between-cascades"></a>Blend zwischen Cascades

VSMs (später in diesem Artikel erläutert) und Filtertechniken wie PCF können mit Low-Resolution-CSMS verwendet werden, um weiche Schatten zu schaffen. Leider führt dies zu einer sichtbaren Naht (Abbildung 9) zwischen kaskadierenden Ebenen, da die Auflösung nicht entspricht. Die Lösung besteht darin, ein Band zwischen schattenkarten zu erstellen, bei denen der Schatten Test für beide Cascades ausgeführt wird. Der Shader interpoliert dann linear zwischen den beiden Werten, basierend auf der Position des Pixels im Blend-Band. Die Beispiele CascadedShadowMaps11 und VarianceShadows11 bieten einen GUI-Schieberegler, der zum Vergrößern und verkleinern dieses weichzeichenbandes verwendet werden kann. Der Shader führt einen dynamischen Branch aus, sodass die überwiegende Mehrheit der Pixel nur aus der aktuellen Cascade-Datei gelesen wird.

**Abbildung 9. Kaskadierende Nähte**

![kaskadierende Nähte](images/cascade-seams.jpg)

Linken Eine sichtbare Naht kann angezeigt werden, wenn sich die kaskame überlappen. Rechten Wenn die kaskadierende zwischen gemischt werden, erfolgt keine Naht.

## <a name="filtering-shadow-maps"></a>Filtern von Schatten Zuordnungen

### <a name="pcf"></a>PCF

Das Filtern normaler Schatten Zuordnungen erzeugt keine weichen, unscharfen Schatten. Die Filter Hardware blzte die tiefen Werte aus und vergleicht dann diese verschwommene Werte mit dem Leerraum Texel. Der aus dem bestanden/Fail-Test resultierende hardedge ist weiterhin vorhanden. Das verwischen von Schatten Zuordnungen dient nur zum irrtümlich bewegen des fest Kanten. PCF ermöglicht das Filtern von Schatten Zuordnungen. Die allgemeine Idee von PCF besteht darin, einen Prozentsatz des Pixels im Schatten zu berechnen, der auf der Anzahl von unter Beispielen basiert, die den tiefen Test über die Gesamtzahl von unter Beispielen bestehen.

Mit der Hardware Direct3D 10 und Direct3D 11 kann PCF durchgeführt werden. Die Eingabe für einen PCF-Sampler besteht aus der Textur Koordinate und einem Wert für die Vergleichs Tiefe. Der Einfachheit halber wird PCF mit einem vier-tippen-Filter erläutert. Der Textur Sampler liest die Textur vier Mal, ähnlich wie ein Standardfilter. Das zurückgegebene Ergebnis ist jedoch ein Prozentsatz der Pixel, die den tiefen Test überschritten haben. Abbildung 10 zeigt, wie ein Pixel, das einen der vier tiefen Tests übergibt, im Schatten 25 Prozent ist. Der tatsächliche zurückgegebene Wert ist eine lineare interpolung, die auf den subtexkoordinaten der Textur Lesevorgänge basiert, um einen glatten Farbverlauf zu schaffen. Ohne diese lineare interpolung kann der vier-tippen-PCF nur fünf Werte zurückgeben: {0,0, 0,25, 0,5, 0,75, 1,0}.

**Abbildung 10. PCF-gefiltertes Bild mit 25 Prozent des ausgewählten Pixels**

![PCF-gefiltertes Bild mit 25 Prozent des ausgewählten Pixels](images/pcf-filtered-image.png)

Es ist auch möglich, PCF ohne Hardwareunterstützung durchzuführen oder PCF auf größere Kernel auszuweiten. Einige Techniken sind sogar mit einem gewichteten Kernel Stichprobe. Erstellen Sie zu diesem Zweck einen Kernel (z. b. eine gausische) für ein N × n-Raster. Die Gewichtungen müssen bis zu 1 addieren. Die Textur wird dann mit den N2-Zeiten abgefragt. Jede Stichprobe wird durch die entsprechenden Gewichtungen im Kernel skaliert. Im CascadedShadowMaps11-Beispiel wird dieser Ansatz verwendet.

### <a name="depth-bias"></a>Tiefenausrichtung

Die Tiefe Abweichung wird noch wichtiger, wenn große PCF-Kernel verwendet werden. Es ist nur gültig, die Leerraum Tiefe eines Pixels mit dem Pixel zu vergleichen, dem es in der tiefen Zuordnung zugeordnet ist. Die Nachbarn des tiefen Karten texgs verweisen auf eine andere Position. Diese Tiefe ist wahrscheinlich ähnlich, kann aber abhängig von der Szene sehr unterschiedlich sein. In Abbildung 11 werden die auftretenden Artefakte hervorgehoben. Eine einzelne Tiefe wird mit drei benachbarten texeln in der Schatten Zuordnung verglichen. Einer der tiefen Tests schlägt fälschlicherweise fehl, da seine tiefe nicht mit der berechneten Leerraum Tiefe der aktuellen Geometrie korreliert. Die empfohlene Lösung für dieses Problem ist die Verwendung eines größeren Offsets. Eine zu große Abweichung kann jedoch dazu führen, dass Peter schwenken. Durch das Berechnen einer engen Near-und weitem-Ebene werden die Auswirkungen der Verwendung eines Offsets reduziert.

**Abbildung 11. Fehlerhafter selbst shadodown**

![fehlerhafter selbst shadodown](images/erroneous-self-shadowing.png)

Der fehlerhafte selbst Shadowing ergibt sich aus dem Vergleichen von Pixeln in der Licht leertiefe mit den texeln in der Schatten Zuordnung, die nicht korrelieren. Die Tiefe im Leerraum korreliert mit Shadow Texel 2 in der tiefenkarte. Texel 1 ist größer als die Tiefe des Leerraums, während 2 gleich und 3 kleiner ist. Texels 2 und 3 übergeben den tiefen Test, während bei Texel 1 ein Fehler auftritt.

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a>Berechnen eines Per-Texel tiefen Bias mit DDX und DDY für große PCFS

Das Berechnen eines pro texesequenz mit **DDX** und **ddY** für große PCFS ist eine Technik, die die richtige tiefen Abweichung berechnet – vorausgesetzt, die Oberfläche ist planar – für die angrenzende schattenkarte Texel.

Diese Technik passt die Vergleichs Tiefe mithilfe der abgeleiteten Informationen auf eine Ebene an. Da dieses Verfahren Rechen technisch komplex ist, sollte es nur dann verwendet werden, wenn eine GPU computezyklen zu ersparen hat. Wenn sehr große Kernel verwendet werden, ist dies möglicherweise die einzige Technik, mit der selbst shadonende Artefakte entfernt werden können, ohne dass Peter schwenken.

In Abbildung 12 wird das Problem hervorgehoben. Die Tiefe im Leerraum ist für das eine texespace bekannt, das verglichen wird. Die Leerräume, die den benachbarten texeln in der tiefenkarte entsprechen, sind unbekannt.

**Abbildung 12. Szene-und tiefen Zuordnung**

![Szene-und tiefen Zuordnung](images/scene-and-depth-map.png)

Die gerenderte Szene wird auf der linken Seite angezeigt, und die tiefen Zuordnung mit einem Beispiel-Texblock wird auf der rechten Seite angezeigt. Der Eye Space Texel wird dem Pixel mit der Bezeichnung D in der Mitte des-Blocks zugeordnet. Dieser Vergleich ist genau. Die richtige Tiefe im Auge Bereich korreliert die Pixel, die der benachbarte D unbekannt ist. Das zurück ordnen der benachbarten texeln in den Augenbereich ist nur möglich, wenn angenommen wird, dass sich das Pixel auf dasselbe Dreieck wie D bezieht.

Die Tiefe ist für den texespace bekannt, der mit der Leerraum Position korreliert. Die Tiefe ist für die benachbarten texeln in der tiefen Zuordnung unbekannt.

Auf hoher Ebene werden bei dieser Technik die **DDX** -und die **ddY** HLSL-Vorgänge verwendet, um die Ableitung der Leerraum Position zu ermitteln. Dies ist nicht trivial, da die abgeleiteten Vorgänge den Farbverlauf der hellen Raum Tiefe in Bezug auf den Bildschirmbereich zurückgeben. Um dies in Bezug auf den Leerraum in einen Farbverlauf der Tiefe des Leerraums zu konvertieren, muss eine Konvertierungs Matrix berechnet werden.

### <a name="explanation-with-shader-code"></a>Erläuterung mit shadercode

Die Details des restlichen Algorithmus werden als Erläuterung des Shader-Codes angegeben, der diesen Vorgang ausführt. Diesen Code finden Sie im CascadedShadowMaps11-Beispiel. In Abbildung 13 wird gezeigt, wie die hell Raum Texturkoordinaten der tiefen Zuordnung zugeordnet werden und wie die Ableitungen in X und Y zum Erstellen einer Transformationsmatrix verwendet werden können.

**Abbildung 13. Bildschirm-zu-Leerraum-Matrix**

![Bildschirm-zu-Leerraum-Matrix](images/screen-space-to-light-space-matrix.png)

Die Ableitungen der Leerraum Position in X und Y werden zum Erstellen dieser Matrix verwendet.

Der erste Schritt besteht darin, die Ableitung der Position des hellen Ansichts Raums zu berechnen.


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



Direct3D 11 Class-GPUs berechnen diese Ableitungen durch gleichzeitige Ausführung von 2 × 2 Quad von Pixeln und Subtrahieren der Texturkoordinaten vom benachbarten in X für **DDX** und vom benachbarten in Y für **ddY**. Diese beiden Ableitungen bilden die Zeilen einer 2 × 2-Matrix. In der aktuellen Form könnte diese Matrix verwendet werden, um benachbarte Bildschirme auf Leerraum zu konvertieren. Allerdings ist die Umkehrung dieser Matrix erforderlich. Eine Matrix, die benachbarte Leerraum-Pixel in Bildschirm Leerräume transformiert, wird benötigt.


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



**Abbildung 14. Leerraum bis Bildschirmbereich**

![Leerraum bis Bildschirmbereich](images/light-space-to-screen-space.png)

Diese Matrix wird dann verwendet, um die beiden texeln oberhalb und auf der rechten Seite des aktuellen texeln zu transformieren. Diese Nachbarn werden als Offset des aktuellen Texels dargestellt.


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



Das von der Matrix erstellte Verhältnis wird schließlich mit den tiefen Ableitungen multipliziert, um die tiefen Offsets für die benachbarten Pixel zu berechnen.


```C++
            float fUpTexelDepthDelta =
            vUpTexelDepthRatio.x * vShadowTexDDX.z
            + vUpTexelDepthRatio.y * vShadowTexDDY.z;
            float fRightTexelDepthDelta =
            vRightTexelDepthRatio.x * vShadowTexDDX.z
            + vRightTexelDepthRatio.y * vShadowTexDDY.z;
```



Diese Gewichtungen können jetzt in einer PCF-Schleife verwendet werden, um der Position einen Offset hinzuzufügen.


```C++
    for( int x = m_iPCFBlurForLoopStart; x < m_iPCFBlurForLoopEnd; ++x ) 
    {
        for( int y = m_iPCFBlurForLoopStart; y < m_iPCFBlurForLoopEnd; ++y )
            {
            if ( USE_DERIVATIVES_FOR_DEPTH_OFFSET_FLAG )
            {
            depthcompare += fRightTexelDepthDelta * ( (float) x ) +
            fUpTexelDepthDelta * ( (float) y );
            }
            // Compare the transformed pixel depth to the depth read
            // from the map.
            fPercentLit += g_txShadow.SampleCmpLevelZero( g_samShadow,
            float2(
            vShadowTexCoord.x + ( ( (float) x ) * m_fNativeTexelSizeInX ) ,
            vShadowTexCoord.y + ( ( (float) y ) * m_fTexelSize )
            ),
            depthcompare
            );
            }
     }
```



## <a name="pcf-and-csms"></a>PCF und CSMS

PCF funktioniert nicht in Textur Arrays in Direct3D 10. Zur Verwendung von PCF werden alle kaskadierende in einem großen Textur Atlas gespeichert.

### <a name="derivative-based-offset"></a>Derivative-Based Offset

Das Hinzufügen der abgeleiteten Offsets für CSMS stellt einige Herausforderungen dar. Dies ist auf eine abgeleitete Berechnung innerhalb einer abweichenden Fluss Steuerung zurückzuführen. Das Problem tritt aufgrund einer grundlegenden Methode auf, die GPUs betreiben. Direct3D11-GPUs arbeiten mit 2 × 2 Quads von Pixeln. Um eine Ableitung auszuführen, subtrahieren GPUs in der Regel die Kopie einer Variablen des aktuellen Pixels aus der Kopie der gleichen Variablen des benachbarten Pixels. Wie dies geschieht, variiert von GPU zu GPU. Die Texturkoordinaten werden von der kartenbasierten oder der Intervall basierten kaskadierenden Auswahl bestimmt. Einige Pixel in einem Pixel Quad wählen einen anderen kaskadierenden als den restlichen Pixel aus. Dies führt zu sichtbaren Nähten zwischen Schatten Zuordnungen, da die abgeleiteten Offsets nun vollständig falsch sind. Die Lösung besteht darin, die Ableitung in Licht Ansichts Raum-Texturkoordinaten auszuführen. Diese Koordinaten sind für jede Cascade identisch.

### <a name="padding-for-pcf-kernels"></a>Padding für PCF-Kernel

PCF-Kernel Index außerhalb einer kaskadierenden Partition, wenn der Schatten Puffer nicht aufgefüllt ist. Die Lösung besteht darin, den äußeren Rand der kaskadierenden Ebene um die Hälfte der Größe des PCF-Kernels aufzurufenden. Dies muss im Shader implementiert werden, der die Cascade-und in der Projektions Matrix auswählt, die die Cascade-Darstellung so groß darstellen muss, dass der Rahmen beibehalten wird.

## <a name="variance-shadow-maps"></a>Varianz Schatten Zuordnungen

VSMs (Weitere Informationen finden Sie unter [Varianz Schatten](https://portal.acm.org/citation.cfm?doid=1111411.1111440) Zuordnungen von Donnelly und Lauritzen) aktivieren Sie das Filtern direkter schattenkarten. Bei der Verwendung von VSMs kann die gesamte Leistungsfähigkeit der Textur Filterungs Hardware verwendet werden. Die Filter "trlinear" und "anisotrope" (Abbildung 15) können verwendet werden. Darüber hinaus können VSMs direkt über die-Übertragung verwischt werden. VSMs haben einige Nachteile. Es müssen zwei Kanäle von Tiefendaten gespeichert werden (Tiefe und Tiefe quadriert). Wenn Schatten überlappend sind, kommt es häufig zu Licht Blutungen. Sie funktionieren jedoch mit geringeren Auflösungen und können mit CSMS kombiniert werden.

**Abbildung 15. Anisotrope Filterung**

![anisotrope Filterung](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a>Algorithmusdetails

VSMs funktioniert durch das Rendern der Tiefe und des tiefen Quadrats in eine zwei-Kanal-Schatten Zuordnung. Diese zwei-Kanal-Schatten Zuordnung kann dann wie eine normale textur verschwommen und gefiltert werden. Der Algorithmus verwendet dann die Ungleichheit von Chebychev im Pixelshader, um den Anteil des Pixel Bereichs zu schätzen, der den tiefen Test bestehen würde.

Der Pixelshader Ruft die tiefen Werte und tiefen Quadrat Werte ab.


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



Der tiefen Vergleich wird durchgeführt.


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



Wenn der tiefen Vergleich fehlschlägt, wird der Prozentsatz des beleuchteten Pixels geschätzt. Die Varianz wird als durchschnittliche Anzahl von Quadraten abzüglich Quadrat des Durchschnitts berechnet.


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



Der Wert für "fprozentulit" wird mit der Ungleichheit von Chebychev geschätzt.


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a>Leichte Blutungen

Der größte Nachteil von VSMs ist eine leichte Blutung (Abbildung 16). Leichte Blutungen treten auf, wenn mehrere Schatten-Casters nebeneinander nebeneinander verborgen werden. Die Ränder von Schatten werden von VSMs basierend auf tiefen unterschieden schattiert. Wenn Schatten einander überlappen, gibt es in der Mitte eines Bereichs, der schattiert werden soll, eine Tiefe Abweichung. Dies ist ein Problem bei der Verwendung des VSM-Algorithmus.

**Abbildung 16. VSM-Licht Blutung**

![VSM-Licht Blutung](images/vsm-light-bleeding.png)

Eine partielle Lösung für das Problem besteht darin, den fprozentulit auf einen Strom zu erhöhen. Dies hat den Effekt, dass der weichungs Effekt gedämpft wird. Dies kann zu Artefakten führen, bei denen die tiefe Ungleichheit gering ist. Manchmal gibt es einen magischen Wert, der das Problem behebt.


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



Eine Alternative zum Hervorheben der Stromversorgung in Prozent besteht darin, Konfigurationen zu vermeiden, bei denen sich Schatten überlappen. Sogar hochoptimierte Schatten Konfigurationen haben mehrere Einschränkungen in den hellen, Kameras und Geometrie. Leichte Blutungen werden auch durch die Verwendung von Strukturen mit höherer Auflösung verringert.

Überlappende Varianz Schatten Zuordnungen (lvsms) lösen das Problem, indem Sie die Frustration in Schichten aufteilen, die senkrecht zum Licht stehen. Die Anzahl erforderlicher Zuordnungen wäre sehr groß, wenn auch CSMS verwendet werden.

Darüber hinaus hat Andrew Lauritzen, Co-Autor des Artikels auf VSMs, und Autor eines Artikels zu lvsms erläutert, wie exponentielle Schatten Zuordnungen (eSMS) mit VSMs kombiniert werden, um helle Mischungen in einem [Beyond3D-Forum](https://forum.beyond3d.com/showthread.php?t=47427)entgegenzuwirken.

## <a name="vsms-with-csms"></a>VSMs mit CSMS

Im Beispiel VarianceShadow11 werden VSMs und CSMS kombiniert. Die Kombination ist recht unkompliziert. Das Beispiel folgt denselben Schritten wie das CascadedShadowMaps11-Beispiel. Da PCF nicht verwendet wird, werden die Schatten in einer trennbaren zwei-und trennbaren zusammen Gabe verschwommen. Wenn Sie PCF nicht verwenden, kann das Beispiel auch Textur Arrays anstelle eines Textur Atlas verwenden. PCF für Textur Arrays ist ein Direct3D 10,1-Feature.

### <a name="gradients-with-csms"></a>Farbverläufe mit CSMS

Die Verwendung von Farbverläufen mit CSMS kann entlang des Rahmens zwischen zwei Kaskaden, wie in Abbildung 17 dargestellt, zu einer Grenze führen. Die Beispiel Anweisung verwendet Ableitungen zwischen Pixeln, um Informationen zu berechnen, z. b. die MipMap-Ebene, die vom Filter benötigt wird. Dies verursacht ein bestimmtes Problem bei der Auswahl von MipMap oder der anisotrope Filterung. Wenn Pixel in einem Quad verschiedene Verzweigungen im Shader annehmen, sind die von der GPU-Hardware berechneten Ableitungen ungültig. Dies führt zu einer verzweigten Naht entlang der schattenkarte.

**Abbildung 17. Nähte an kaskadierenden Rahmen aufgrund einer anisotrope Filterung mit abweichender Fluss Steuerung**

![Nähte an kaskadierenden Rahmen aufgrund einer anisotrope Filterung mit abweichender Fluss Steuerung](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

Dieses Problem wird gelöst, indem die Ableitungen an der Position im hellen Raum berechnet werden. die hell Ansichts Raum Koordinate ist nicht spezifisch für die ausgewählte CASCADE-Option. Die berechneten Ableitungen können von dem Skalierungs Teil der Projektions Textur Matrix auf die richtige MipMap-Ebene skaliert werden.


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a>VSMs im Vergleich zu Standard Schatten mit PCF

Sowohl VSMs als auch PCF versuchen, den Bruchteil des Pixel Bereichs zu annähern, der den tiefen Test bestanden hat. VSMs funktioniert mit Filterungs Hardware und kann mit trennbaren Kernels verschwommen werden. Die Implementierung von trennbaren-und-Kernel-Kernels ist erheblich günstiger als ein vollständiger Kernel. Außerdem vergleicht VSMs eine Leerraum Tiefe mit einem Wert in der detaillierten Leertaste. Dies bedeutet, dass VSMs nicht die gleichen Offset Probleme wie PCF haben. Technisch gesehen sind VSMs eine Stichproben Tiefe über einen größeren Bereich und Durchführen einer statistischen Analyse. Dies ist weniger genau als PCF. In der Praxis führt VSMs eine sehr gute Mischung aus, was dazu führt, dass weniger Offset erforderlich ist. Wie oben beschrieben, ist die Zahl ein Nachteil von VSMs eine leichte Blutung.

VSMs und PCF stellen einen Kompromiss zwischen GPU-computeleistung und GPU-Textur Bandbreite dar. VSMs erfordert mehr Berechnungen, um die Varianz zu berechnen. PCF erfordert mehr Texturspeicher Bandbreite. Große PCF-Kernel können durch Textur Bandbreite schnell zu einem Engpass werden. Wenn sich der GPU-Berechnungs Strom schneller als die GPU-Bandbreite vergrößert, werden die beiden Algorithmen von VSMs immer praktischer. VSMs ist auch mit niedrigerer Auflösung von Schatten Zuordnungen aufgrund von Blending und Filterung besser geeignet.

## <a name="summary"></a>Zusammenfassung

CSMS bieten eine Lösung für das Problem der Perspektiven Aliasing. Es gibt mehrere mögliche Konfigurationen, um die benötigte visuelle Genauigkeit für einen Titel zu erhalten. PCF und VSMs werden häufig verwendet und sollten mit CSMS kombiniert werden, um das Aliasing zu verringern.

## <a name="references"></a>References

Donnelly, W. und Lauritzen, A. [Varianz Schatten](https://portal.acm.org/citation.cfm?doid=1111411.1111440)Zuordnungen. In SI3D ' 06: das-Verfahren des 2006-Symposiums zu interaktiven 3D-Grafiken und-spielen. 2006. PP. 161 – 165. New York, NY, USA: ACM Press.

Lauritzen, Andrew und McCool, Michael. [Überlagerte Varianz schattenkarten](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992). Das Verfahren der Grafikschnittstelle 2008, 28. Mai – 30, 2008, Windsor, Ontario, Kanada.

Engel, woflgang F., Abschnitt 4. Kaskadierenden Schatten Zuordnungen. ShaderX5, erweiterte renderingtechniken, Wolfgang F. Engel, Ed. Charles River Media, Boston, Massachusetts. 2006. PP. 197 – 206.

 

 