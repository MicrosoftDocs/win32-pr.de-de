---
title: Überlappende Schattenkarten
description: Kaskadierte Schattenkarten (Cascaded Shadow Maps, CSMs) sind die beste Möglichkeit, einen der häufigsten Fehler beim Shadowing von Perspektivenaliasing zu beheben.
ms.assetid: d3570d0a-74e0-5b9c-6586-c933f630c4ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29498dc882133215c910f3bd6caa5966aa0e141aaf4f7a68051834d33f2a3b16
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118649664"
---
# <a name="cascaded-shadow-maps"></a>Überlappende Schattenkarten

Kaskadierte Schattenkarten (Cascaded Shadow Maps, CSMs) sind die beste Möglichkeit, einen der häufigsten Fehler beim Shadowing zu beheben: Perspektivaliasing. In diesem technischen Artikel, in dem davon ausgegangen wird, dass der Leser mit der Schattenzuordnung vertraut ist, wird das Thema CSMs behandelt. Diese Parameter:

-   erläutert die Komplexität von CSMs.
-   enthält Details zu den möglichen Variationen der CSM-Algorithmen.
-   beschreibt die beiden gängigsten Filtertechniken: PcF (Percentage Closer Filtering) und Filterung mit Varianzschattenkarten (Variance Shadow Maps, VSMs).
-   identifiziert und behebt einige der häufigen Fallstricke im Zusammenhang mit dem Hinzufügen von Filterung zu CSMs. Und
-   zeigt, wie CSMs Direct3D 10 bis Direct3D 11-Hardware zuordnen.

Den in diesem Artikel verwendeten Code finden Sie im DirectX Software Development Kit (SDK) in den Beispielen CascadedShadowMaps11 und VarianceShadows11. Dieser Artikel wird sich als nützlich erweisen, nachdem die im technischen Artikel Common [Techniques to Improve Shadow Depth Karten](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps)(Allgemeine Techniken zur Verbesserung der Schattentiefe) beschriebenen Verfahren implementiert wurden.

## <a name="cascaded-shadow-maps-and-perspective-aliasing"></a>Kaskadierte Karten und Perspektivenaliasing

Das Perspektivaliasing in einer Schattenkarte ist eines der schwierigsten Zu lösenden Probleme. Im technischen Artikel Common Techniques to Improve Shadow Depth Karten(Allgemeine Techniken zur Verbesserung der Schattentiefe) wird das Perspektivaliasing beschrieben, und es werden einige Ansätze zur Lösung des Problems identifiziert. In der Praxis sind CSMs in der Regel die beste Lösung und werden häufig in modernen Spielen eingesetzt.

Das grundlegende Konzept von CSMs ist leicht zu verstehen. Verschiedene Bereiche des Kamera-Frustums erfordern Schattenkarten mit unterschiedlichen Auflösungen. Objekte, die dem Auge am nächsten liegen, erfordern eine höhere Auflösung als entfernte Objekte. Wenn sich das Auge sehr nah an der Geometrie bewegt, können die Pixel, die dem Auge am nächsten sind, so viel Auflösung erfordern, dass selbst eine 4096 × 4096-Schattenkarte nicht ausreicht.

Die Grundidee von CSMs besteht in der Partitionierung des Frustums in mehrere Frustas. Für jedes Unterfrustum wird eine Schattenkarte gerendert. Der Pixel-Shader verwendet dann Stichproben von der Karte, die der erforderlichen Auflösung am besten entspricht (Abbildung 2).

**Abbildung 1: Schattenkartenabdeckung**

![Schattenkartenabdeckung](images/shadow-map-coverage.png)

In Abbildung 1 wird die Qualität (von links nach rechts) von der höchsten zur niedrigsten angezeigt. Die Reihe von Rastern, die Schattenkarten mit einem Ansichtsfrustum (invertierter Kegel in Rot) darstellen, zeigt, wie die Pixelabdeckung mit unterschiedlichen Auflösungsschattenkarten beeinflusst wird. Schatten haben die höchste Qualität (weiße Pixel), wenn ein Verhältnis von 1:1 Pixeln im hellen Raum zu Texeln in der Schattenkarte besteht. Das Perspektivaliasing erfolgt in Form von großen, blockigen Texturzuordnungen (linkes Bild), wenn zu viele Pixel demselben Schattentextel zuordnen. Wenn die Schattenkarte zu groß ist, wird sie unter Stichproben entnommen. In diesem Fall werden Texel übersprungen, shing artifacts eingeführt, und die Leistung wird beeinträchtigt.

**Abbildung 2: CSM-Schattenqualität**

![CSM-Schattenqualität](images/csm-shadow-quality.png)

Abbildung 2 zeigt Ausschnitte aus dem Abschnitt mit der höchsten Qualität in jeder Schattenkarte in Abbildung 1. Die Schattenkarte mit den am besten platzierten Pixeln (am Apex) ist dem Auge am nächsten. Technisch gesehen handelt es sich hierbei um Karten der gleichen Größe, bei der weiß und grau verwendet werden, um den Erfolg der kaskadierten Schattenkarte zu exempeln. Weiß ist ideal, da es eine gute Abdeckung zeigt – ein Verhältnis von 1:1 für Augenraumpixel und Schattenkarten-Texel.

FÜR CSMs sind die folgenden Schritte pro Frame erforderlich.

1.  Partitionieren Sie das Frustum in subfrusta.
2.  Berechnen Sie eine orthografische Projektion für jedes Subfrustum.
3.  Rendern Sie eine Schattenkarte für jedes Unterfrustum.
4.  Rendern Sie die Szene.

    1.  Binden Sie die Schattenkarten, und rendern Sie sie.
    2.  Der Vertex-Shader führt Folgendes aus:

        -   Berechnet Texturkoordinaten für jedes helle Subfrustum (es sei denn, die benötigte Texturkoordinate wird im Pixel-Shader berechnet).
        -   Transformiert und leuchtet den Scheitelpunkt und so weiter.

    3.  Der Pixel-Shader führt folgende Schritte aus:

        -   Bestimmt die richtige Schattenkarte.
        -   Transformiert bei Bedarf die Texturkoordinaten.
        -   Stichproben der Kaskadierung.
        -   Leuchtet das Pixel.

## <a name="partitioning-the-frustum"></a>Partitionieren des Frustums

Das Partitionieren des Frustums ist das Erstellen von Subfrusta. Eine Technik zum Aufteilen des Frustums besteht in der Berechnung von Intervallen von null bis 100 Prozent in Z-Richtung. Jedes Intervall stellt dann eine nahe Ebene und eine Fernebene als Prozentsatz der Z-Achse dar.

**Abbildung 3: Partitionierte Frustums anzeigen**

![Frustums beliebig partitioniert anzeigen](images/view-frustums-partitioned-arbitrarily.png)

In der Praxis führt die Neuberechnung der Frustumteilungen pro Frame dazu, dass Schattenränder schrumpfen. Die allgemein akzeptierte Vorgehensweise besteht in der Verwendung einer statischen Gruppe von kaskadierten Intervallen pro Szenario. In diesem Szenario wird das Intervall entlang der Z-Achse verwendet, um ein Subfrustum zu beschreiben, das beim Partitionieren des Frustums auftritt. Die Bestimmung der richtigen Größenintervalle für eine bestimmte Szene hängt von mehreren Faktoren ab.

### <a name="orientation-of-the-scene-geometry"></a>Ausrichtung der Szenengeometrie

In Bezug auf die Szenengeometrie wirkt sich die Kameraausrichtung auf die Auswahl des kaskadierten Intervalls aus. Eine Kamera in der Nähe des Bodens, z. B. eine Bodenkamera in einem Footballspiel, hat beispielsweise einen anderen statischen Satz kaskadender Intervalle als eine Kamera am Himmel.

Abbildung 4 zeigt einige verschiedene Kameras und ihre jeweiligen Partitionen. Wenn der Z-Bereich der Szene sehr groß ist, sind mehr Teilungsebenen erforderlich. Wenn sich das Auge beispielsweise in der Nähe der Bodenebene befindet, aber entfernte Objekte immer noch sichtbar sind, können mehrere Kaskaden erforderlich sein. Es ist ebenfalls nützlich, das Frustum so zu unterteilen, dass sich mehr Aufteilungen am Auge befinden (wobei sich perspektivische Aliasing am schnellsten ändert). Wenn der größte Teil der Geometrie in einen kleinen Abschnitt (z. B. eine Overheadansicht oder ein Flugsimulator) des Ansichtsfrustums eingeteilt ist, sind weniger Kaskaden erforderlich.

**Abbildung 4. Verschiedene Konfigurationen erfordern unterschiedliche Frustumteilungen.**

![Verschiedene Konfigurationen erfordern unterschiedliche Frustumteilungen.](images/different-configurations-require-different-frustum-splits.png)

(Links) Wenn geometry einen hohen dynamischen Bereich in Z auf hat, sind viele Kaskaden erforderlich. (Mitte) Wenn die Geometrie in Z über einen niedrigen dynamischen Bereich verfügt, gibt es wenig Vorteile von mehreren Frustums. (Rechts) Nur drei Partitionen sind erforderlich, wenn der dynamische Bereich mittel ist.

### <a name="orientation-of-the-light-and-the-camera"></a>Ausrichtung des Lichts und der Kamera

Die Projektionsmatrix jeder Kaskadierung ist eng um das entsprechende Unterfrustum herum geeignet. In Konfigurationen, in denen die Ansichtskamera und die Lichtrichtungen orthogonal sind, können die Kaskaden eng mit wenig Überlappung passen. Die Überlappung wird größer, wenn das Licht und die Ansichtskamera parallel ausgerichtet werden (Abbildung 5). Wenn das Licht und die Ansichtskamera nahezu parallel sind, wird dies als "dueling frusta" bezeichnet und ist ein sehr schwieriges Szenario für die meisten Schattenalgorithmen. Es ist nicht ungewöhnlich, das Licht und die Kamera so zu beschränken, dass dieses Szenario nicht eintritt. CSMs arbeiten jedoch in diesem Szenario viel besser als viele andere Algorithmen.

**Abbildung 5. Die überlappende Überlappung nimmt zu, wenn die Lichtrichtung parallel zur Kamerarichtung wird.**

![Die überlappende Überlappung nimmt zu, wenn die Lichtrichtung parallel zur Kamerarichtung wird.](images/cascade-overlap-increases-as-light-direction-becomes.jpg)

Viele CSM-Implementierungen verwenden Frusta mit fester Größe. Der Pixel-Shader kann die Z-Tiefe verwenden, um in das Array von Kaskadierungen zu indizieren, wenn das Frustum in Intervalle fester Größe aufgeteilt wird.

## <a name="calculating-a-view-frustum-bound"></a>Berechnen einer View-Frustum Gebundenen

Sobald die Frustumintervalle ausgewählt sind, wird der Subfrusta mit einem von zwei Erstellt: an die Szene passen und an kaskadierende Daten passen.

### <a name="fit-to-scene"></a>An Szene passen

Alle Frustas können mit der gleichen Nahebene erstellt werden. Dadurch wird eine Überlappung der Kaskaden erzwingt. Im CascadedShadowMaps11-Beispiel wird diese Technik als für die Szene geeignet bezeichnet.

### <a name="fit-to-cascade"></a>An Cascade passen

Alternativ kann frusta mit dem tatsächlichen Partitionsintervall erstellt werden, das als Nah- und Fernebene verwendet wird. Dies führt zu einer engeren Anpassung, wird aber im Falle eines Frusts an die Szene angepasst. In den CascadedShadowMaps11-Beispielen wird diese Technik als kaskadierend bezeichnet.

Diese beiden Methoden sind in Abbildung 6 dargestellt. Durch die Anpassung an kaskadierte Verschwendung wird weniger Auflösung verschwendet. Das Problem bei der Anpassung an kaskadierende Daten ist, dass die orthografische Projektion basierend auf der Ausrichtung des Ansichtsfrustums wächst und verkleinert wird. Die Anpassung an die Szenentechnik padt die orthografische Projektion um die maximale Größe des Ansichtsfrustums und entfernt die Artefakte, die angezeigt werden, wenn die Kamera bewegt wird. [Common Techniques to Improve Shadow Depth Karten](/windows/desktop/DxTechArts/common-techniques-to-improve-shadow-depth-maps) adressiert die Artefakte, die angezeigt werden, wenn sich das Licht im Abschnitt "Moving the light in texel sized increments" (Bewegen des Lichts in Texelschritten) bewegt.

**Abbildung 6: An Szene anpassen im Vergleich zu "An Kaskading anpassen"**

![An Szene anpassen und an Kaskadation anpassen](images/fit-to-scene-vs-fit-to-cascade.png)

## <a name="render-the-shadow-map"></a>Rendern der Schattenkarte

Im Beispiel CascadedShadowMaps11 werden die Schattenzuordnungen in einem großen Puffer gerendert. Dies liegt daran, dass PCF auf Texturarrays ein Direct3D 10.1-Feature ist. Für jede Kaskadierende wird ein Viewport erstellt, der den Abschnitt des Tiefenpuffers abdeckt, der dieser Kaskadierende entspricht. Ein NULL-Pixel-Shader wird gebunden, da nur die Tiefe benötigt wird. Schließlich werden der richtige Viewport und die Schattenmatrix für jede Kaskadation festgelegt, da die Tiefenzuordnungen einzeln in den Hauptschattenpuffer gerendert werden.

## <a name="render-the-scene"></a>Rendern der Szene

Der Puffer, der die Schatten enthält, ist jetzt an den Pixelshader gebunden. Es gibt zwei Methoden zum Auswählen der kaskadierenden , die im CascadedShadowMaps11-Beispiel implementiert ist. Diese beiden Methoden werden mit Shadercode erläutert.

### <a name="interval-based-cascade-selection"></a>Interval-Based Cascade Selection

**Abbildung 7. Intervallbasierte Kaskadenzauswahl**

![Intervallbasierte Kaskadenzauswahl](images/interval-based-cascade-selection.jpg)

Bei der intervallbasierten Auswahl (Abbildung 7) berechnet der Vertex-Shader die Position im Weltraum des Scheitelpunkts.


```C++
Output.vDepth = mul( Input.vPosition, m_mWorldView ).z;
```



Der Pixelshader empfängt die interpolierte Tiefe.


```C++
fCurrentPixelDepth = Input.vDepth;
```



Bei der intervallbasierten kaskadierenden Auswahl werden ein Vektorvergleich und ein Punktprodukt verwendet, um die richtige Kaktusen zu bestimmen. Das CASCADE \_ COUNT FLAG gibt die Anzahl der \_ Kaskaden an. Die \_ m fCascadeFrustumsEyeSpaceDepths-Daten \_ schränken die Sicht-Frustumpartitionen ein. Nach dem Vergleich enthält fComparison den Wert 1, wobei das aktuelle Pixel größer als die Barriere ist, und einen Wert von 0, wenn die aktuelle Kaskadierung kleiner ist. Ein Punktprodukt summiert diese Werte in einem Arrayindex.


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



Nachdem die kaskadierte ausgewählt wurde, muss die Texturkoordinate in die richtige Kaskadierte transformiert werden.


```C++
vShadowTexCoord = mul( InterpolatedPosition, m_mShadow[iCascadeIndex] );
```



Diese Texturkoordinate wird dann verwendet, um die Textur mit der X-Koordinate und der Y-Koordinate abzutasten. Die Z-Koordinate wird für den abschließenden Tiefenvergleich verwendet.

### <a name="map-based-cascade-selection"></a>Map-Based Cascade Selection

Kartenbasierte Auswahl (Abbildung 8) testet an den vier Seiten der Kaskaden, um die engste Karte zu finden, die das spezifische Pixel abdeckt. Anstatt die Position im Weltraum zu berechnen, berechnet der Vertex-Shader die Ansichtsraumposition für jede Kaskadierung. Der Pixel-Shader durchläuft die Kaskadierungen, um die Texturkoordinaten so zu skalieren und zu verschieben, dass sie die aktuelle Kaskadierung indizieren. Die Texturkoordinate wird dann anhand der Texturgrenzen getestet. Wenn die X- und Y-Werte der Texturkoordinate in eine Kaskadate fallen, werden sie zum Abtasten der Textur verwendet. Die Z-Koordinate wird für den abschließenden Tiefenvergleich verwendet.

**Abbildung 8. Kartenbasierte Kaskadiertenauswahl**

![Kartenbasierte Kaskadiertenauswahl](images/map-based-cascade-selection.jpg)

### <a name="interval-based-selection-vs-map-based-selection"></a>Interval-Based Auswahl im Vergleich zu Map-Based Auswahl

Die intervallbasierte Auswahl ist etwas schneller als die kartenbasierte Auswahl, da die Kaskadenzauswahl direkt erfolgen kann. Die kartenbasierte Auswahl muss die Texturkoordinate mit den kaskadierten Begrenzungen überschneiden.

Die kartenbasierte Auswahl verwendet die Kaskadation effizienter, wenn Schattenkarten nicht perfekt ausgerichtet sind (siehe Abbildung 8).

## <a name="blend-between-cascades"></a>Überblenden zwischen Kaskaden

VSMs (weiter unten in diesem Artikel erläutert) und Filtertechniken wie PCF können mit CSMs mit niedriger Auflösung verwendet werden, um soft shadows zu erzeugen. Leider führt dies zu einer sichtbaren Naht (Abbildung 9) zwischen kaskadierten Schichten, da die Auflösung nicht übereinstimmt. Die Lösung besteht darin, ein Band zwischen Schattenkarten zu erstellen, in dem der Schattentest für beide Kaskaden ausgeführt wird. Der Shader interpoliert dann linear zwischen den beiden Werten basierend auf der Position des Pixels im Blendband. Die Beispiele CascadedShadowMaps11 und VarianceShadows11 bieten einen GUI-Schieberegler, der verwendet werden kann, um dieses Weichzeichnerband zu vergrößern und zu verringern. Der Shader führt einen dynamischen Branch aus, sodass die überwiegende Mehrheit der Pixel nur aus der aktuellen Kaskadierung gelesen wird.

**Abbildung 9: Kaskadierten Nahten**

![Kaskadierten Nahten](images/cascade-seams.jpg)

(Links) Eine sichtbare Naht kann angezeigt werden, wenn kaskadiert überlappen. (Rechts) Wenn die Kaskaden zwischen gemischt werden, tritt keine Naht auf.

## <a name="filtering-shadow-maps"></a>Filtern von Schatten Karten

### <a name="pcf"></a>Pcf

Das Filtern gewöhnlicher Schattenzuordnungen erzeugt keine weichen, unscharfen Schatten. Die Filterhardware verschwommen die Tiefenwerte und vergleicht diese unscharfen Werte dann mit dem Texel des Lichtraums. Der harte Rand, der sich aus dem Bestanden/Fehlschlagen-Test ergibt, ist weiterhin vorhanden. Unscharfe Schattenzuordnungen dienen nur dazu, die harte Kante fälschlicherweise zu verschieben. PCF ermöglicht das Filtern nach Schattenkarten. Die allgemeine Idee von PCF besteht darin, einen Prozentsatz des Pixels im Schatten basierend auf der Anzahl der Untersamples zu berechnen, die den Tiefentest über die Gesamtzahl der Untersamples bestehen.

Direct3D 10- und Direct3D 11-Hardware kann PCF ausführen. Die Eingabe für einen PCF-Sampler besteht aus der Texturkoordinate und einem Vergleichstiefewert. Der Einfachheit halber wird PCF mit einem Filter mit vier Tippen erläutert. Der Textur-Sampler liest die Textur viermal, ähnlich wie ein Standardfilter. Das zurückgegebene Ergebnis ist jedoch ein Prozentsatz der Pixel, die den Tiefentest bestanden haben. Abbildung 10 zeigt, wie ein Pixel, das einen der vier Tiefentests besteht, 25 Prozent im Schatten ist. Der tatsächliche zurückgegebene Wert ist eine lineare Interpolation, die auf den Teiltexelkoordinaten der Texturlesezeichen basiert, um einen reibungslosen Farbverlauf zu erzeugen. Ohne diese lineare Interpolation kann die PCF mit vier Tippen nur fünf Werte zurückgeben: { 0,0, 0,25, 0,5, 0,75, 1,0 }.

**Abbildung 10. PCF-gefiltertes Bild, wobei 25 Prozent des ausgewählten Pixels abgedeckt sind**

![gefiltertes Pcf-Bild, wobei 25 Prozent des ausgewählten Pixels abgedeckt sind](images/pcf-filtered-image.png)

Es ist auch möglich, PCF ohne Hardwareunterstützung zu verwenden oder PCF auf größere Kernels zu erweitern. Einige Techniken können sogar mit einem gewichteten Kernel entnommen werden. Erstellen Sie hierzu einen Kernel (z. B. einen Gaußer) für ein N × N-Raster. Die Gewichtungen müssen bis zu 1 addiert werden. Die Textur wird dann N2-mal entnommen. Jede Stichprobe wird anhand der entsprechenden Gewichtungen im Kernel skaliert. Im CascadedShadowMaps11-Beispiel wird dieser Ansatz verwendet.

### <a name="depth-bias"></a>Tiefenausrichtung

Tiefenvoreingenommenheit wird noch wichtiger, wenn große PCF-Kernel verwendet werden. Es ist nur gültig, die Lichtraumtiefe eines Pixels mit dem Pixel zu vergleichen, dem es in der Tiefenkarte zugeordnet ist. Die Nachbarn des Tiefenzuordnungs-Texels verweisen auf eine andere Position. Diese Tiefe ist wahrscheinlich ähnlich, kann aber je nach Szene sehr unterschiedlich sein. Abbildung 11 zeigt die Artefakte, die auftreten. Eine einzelne Tiefe wird mit drei benachbarten Texeln in der Schattenkarte verglichen. Einer der Tiefentests schlägt fälschlicherweise fehl, da seine Tiefe nicht mit der berechneten Lichtraumtiefe der aktuellen Geometrie korreliert. Die empfohlene Lösung für dieses Problem ist die Verwendung eines größeren Offsets. Zu groß eines Offsets kann jedoch zu Peter Panning führen. Das Berechnen einer engen Nahebene und einer fernen Ebene trägt dazu bei, die Auswirkungen der Verwendung eines Offsets zu reduzieren.

**Abbildung 11. Fehlerhaftes Selbstschatten**

![fehlerhaftes Selbstschatten](images/erroneous-self-shadowing.png)

Das fehlerhafte Selbstschatten ergibt sich aus dem Vergleich von Pixeln in der Lichtraumtiefe mit den Texel in der Schattenkarte, die nicht korrelieren. Die Tiefe im lichten Raum korreliert mit Schatten-Texel 2 in der Tiefenkarte. Texel 1 ist größer als die Lichtraumtiefe, während 2 gleich und 3 kleiner ist. Die Texel 2 und 3 bestehen den Tiefentest, während Texel 1 fehlschlägt.

### <a name="calculating-a-per-texel-depth-bias-with-ddx-and-ddy-for-large-pcfs"></a>Berechnen einer Per-Texel Tiefenabweichung mit DDX und DDY für große PCFs

Das Berechnen einer Tiefenabweichung pro Texel mit **ddx** und **ddy** für große PCFs ist eine Technik, die die richtige Tiefenabweichung für das angrenzende Schattenkarten-Texel berechnet – vorausgesetzt, die Oberfläche ist planar.

Diese Technik passt die Vergleichstiefe mithilfe der abgeleiteten Informationen auf eine Ebene an. Da diese Technik rechenintensiv ist, sollte sie nur verwendet werden, wenn eine GPU über Rechenzyklen verfügt, die ersparen muss. Wenn sehr große Kernel verwendet werden, ist dies möglicherweise die einzige Technik, mit der Artefakte mit Selbstschatten entfernt werden können, ohne dass Peter Panning verursacht wird.

Abbildung 12 zeigt das Problem. Die Tiefe im Lichtbereich ist für das einzige Texel bekannt, das verglichen wird. Die Lichtraumtiefe, die den benachbarten Texel in der Tiefenkarte entspricht, ist unbekannt.

**Abbildung 12. Szenen- und Tiefenzuordnung**

![Szenen- und Tiefenkarte](images/scene-and-depth-map.png)

Die gerenderte Szene wird auf der linken Seite angezeigt, und die Tiefenkarte mit einem Beispiel-Texelblock wird rechts angezeigt. Das Texel für den Augenraum ist dem Pixel mit der Bezeichnung D in der Mitte des Blocks zu erkennen. Dieser Vergleich ist genau. Die richtige Tiefe im Augenbereich, die mit den Pixeln korreliert, in denen nachbar D unbekannt ist. Die Zuordnung der benachbarten Texel zurück zum Augenraum ist nur möglich, wenn angenommen wird, dass das Pixel das gleiche Dreieck wie D betrifft.

Die Tiefe ist für das Texel bekannt, das mit der Lichtraumposition korreliert. Die Tiefe ist für die benachbarten Texel in der Tiefenzuordnung unbekannt.

Auf hoher Ebene verwendet diese Technik die **DDX-** und ddy-HLSL-Vorgänge, um die Ableitung der Lichtraumposition zu finden.  Dies ist nichttrivial, da die ableitungsvorgänge den Farbverlauf der Lichtraumtiefe in Bezug auf den Bildschirmraum zurückgeben. Um dies in einen Farbverlauf der Lichtraumtiefe in Bezug auf den lichten Raum zu konvertieren, muss eine Konvertierungsmatrix berechnet werden.

### <a name="explanation-with-shader-code"></a>Erläuterung mit Shadercode

Die Details des restlichen Algorithmus werden als Erläuterung des Shadercodes angegeben, der diesen Vorgang ausführt. Diesen Code finden Sie im CascadedShadowMaps11-Beispiel. Abbildung 13 zeigt, wie die Texturkoordinaten des lichten Raumes der Tiefenkarte zuordnen und wie die Ableitungen in X und Y verwendet werden können, um eine Transformationsmatrix zu erstellen.

**Abbildung 13. Bildschirmraum-zu-Licht-Raum-Matrix**

![Bildschirmraum-zu-Licht-Raum-Matrix](images/screen-space-to-light-space-matrix.png)

Die Ableitungen der Lichtraumposition in X und Y werden verwendet, um diese Matrix zu erstellen.

Im ersten Schritt wird die Ableitung der Position des Lichtansichtsraums berechnet.


```C++
          float3 vShadowTexDDX = ddx (vShadowMapTextureCoordViewSpace);
          float3 vShadowTexDDY = ddy (vShadowMapTextureCoordViewSpace);
```



GpUs der Direct3D 11-Klasse berechnen diese Ableitungen, indem sie 2 × 2 Vierfachpixel parallel ausführen und die Texturkoordinaten vom Nachbarn in X für **ddx** und vom Nachbarn in Y für **ddy** subtrahieren. Diese beiden Ableitungen machen die Zeilen einer 2 × 2 Matrix aus. In der aktuellen Form könnte diese Matrix verwendet werden, um benachbarte Pixel im Bildschirmbereich in Lichtraumvergrößerungen zu konvertieren. Die Umkehrung dieser Matrix ist jedoch erforderlich. Eine Matrix, die benachbarte Pixel mit hellem Raum in Bildschirmbereichsvergrößerungen transformiert, ist erforderlich.


```C++
          float2x2 matScreentoShadow = float2x2( vShadowTexDDX.xy, vShadowTexDDY.xy );
          float fInvDeterminant = 1.0f / fDeterminant;

          float2x2 matShadowToScreen = float2x2 (
          matScreentoShadow._22 * fInvDeterminant,
          matScreentoShadow._12 * -fInvDeterminant,
          matScreentoShadow._21 * -fInvDeterminant,
          matScreentoShadow._11 * fInvDeterminant );
```



**Abbildung 14. Lichtraum in Bildschirmbereich**

![Lichtraum in Bildschirmbereich](images/light-space-to-screen-space.png)

Diese Matrix wird dann verwendet, um die beiden Texel oben und rechts vom aktuellen Texel zu transformieren. Diese Nachbarn werden als Offset vom aktuellen Texel dargestellt.


```C++
          float2 vRightShadowTexelLocation = float2( m_fTexelSize, 0.0f );
          float2 vUpShadowTexelLocation = float2( 0.0f, m_fTexelSize );
          float2 vRightTexelDepthRatio = mul( vRightShadowTexelLocation,
          matShadowToScreen );
          float2 vUpTexelDepthRatio = mul( vUpShadowTexelLocation,
          matShadowToScreen );
```



Das verhältnis, das die Matrix erstellt, wird schließlich mit den Tiefenentleitungen multipliziert, um die Tiefenoffsets für die benachbarten Pixel zu berechnen.


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



## <a name="pcf-and-csms"></a>PCF und CSMs

PCF funktioniert nicht bei Texturarrays in Direct3D 10. Zur Verwendung von PCF werden alle Kaskaden in einem großen Texturatlas gespeichert.

### <a name="derivative-based-offset"></a>Derivative-Based Offset

Das Hinzufügen der ableitungsbasierten Offsets für CSMs stellt einige Herausforderungen dar. Dies liegt an einer ableitungsberechnung innerhalb der ablaufsteuerung. Das Problem tritt aufgrund einer grundlegenden Art und Weise auf, wie GPUs funktionieren. Direct3D11-GPUs arbeiten mit 2 × 2 Quads von Pixeln. Um eine Ableitung durchzuführen, subtrahieren GPUs im Allgemeinen die Kopie einer Variablen des aktuellen Pixels von der Kopie derselben Variablen des benachbarten Pixels. Wie dies geschieht, variiert von GPU zu GPU. Die Texturkoordinaten werden durch kartenbasierte oder intervallbasierte Kaskadierungsauswahl bestimmt. Einige Pixel in einem Pixelquadment wählen eine andere Kaskadierung als die restlichen Pixel aus. Dies führt zu sichtbaren Nahtungen zwischen Schattenkarten, da die ableitungsbasierten Offsets jetzt völlig falsch sind. Die Lösung besteht in der Durchführung der Ableitung an Texturkoordinaten des Lichtansichtsraums. Diese Koordinaten sind für jede Kaskadierung identisch.

### <a name="padding-for-pcf-kernels"></a>Padding for PCF Kernels

PCF-Kernelindex außerhalb einer kaskadierten Partition, wenn der Schattenpuffer nicht aufschlossen ist. Die Lösung besteht im Aufpadsten des äußeren Rands der Kaskadierung um die Hälfte der Größe des PCF-Kernels. Dies muss in dem Shader implementiert werden, der die Kaskadierung auswählt, und in der Projektionsmatrix, die die Kaskadierung so groß rendern muss, dass der Rahmen beibehalten wird.

## <a name="variance-shadow-maps"></a>Variance Shadow Karten

VSMs (weitere Informationen finden Sie unter [Varianzschattenkarten](https://portal.acm.org/citation.cfm?doid=1111411.1111440) von Donnelly und Lau ? ) ermöglichen die direkte Filterung von Schattenkarten. Bei verwendung von VSMs kann die ganze Leistung der Texturfilterhardware genutzt werden. Trilineare und anisotrope Filterung (Abbildung 15) können verwendet werden. Darüber hinaus können VSMs durch Konvolution direkt unscharf werden. VSMs haben einige Nachteile. Zwei Kanäle mit Tiefendaten müssen gespeichert werden (Tiefe und Tiefe quadratisch). Wenn sich Schatten überlappen, kommt es häufig zu Lichtverurstung. Sie funktionieren jedoch gut mit niedrigeren Auflösungen und können mit CSMs kombiniert werden.

**Abbildung 15. Anisotrope Filterung**

![Anisotrope Filterung](images/anisotropic-filtering.png)

### <a name="algorithm-details"></a>Algorithmusdetails

VSMs rendern die Tiefe und die Tiefe quadratisch in eine Zwei-Kanal-Schattenkarte. Diese Zweikanal-Schattenkarte kann dann unscharf und wie eine normale Textur gefiltert werden. Der Algorithmus verwendet dann die Ungleichheit von Tschebyschev im Pixel-Shader, um den Bruchteil des Pixelbereichs zu schätzen, der den Tiefentest bestanden würde.

Der Pixel-Shader ruft die Tiefen- und Tiefen-Quadratwerte ab.


```C++
        float  fAvgZ  = mapDepth.x; // Filtered z
        float  fAvgZ2 = mapDepth.y; // Filtered z-squared
```



Der Tiefenvergleich wird ausgeführt.


```C++
        if ( fDepth <= fAvgZ )
        {
        fPercentLit = 1;
        }
```



Wenn beim Tiefenvergleich ein Fehler auftritt, wird der Prozentsatz des Pixelwerts geschätzt, der beleuchtet wird. Varianz wird als Mittelwert der Quadrate minus Quadrat des Durchschnitts berechnet.


```C++
        float variance = ( fAvgZ2 ) − ( fAvgZ * fAvgZ );
        variance = min( 1.0f, max( 0.0f, variance + 0.00001f ) );
```



Der fPercentLit-Wert wird mit der Ungleichheit von Tschebyschev geschätzt.


```C++
        float mean           = fAvgZ;
        float d              = fDepth - mean;
        float fPercentLit    = variance / ( variance + d*d );
```



## <a name="light-bleeding"></a>Lichte Glühbirnen

Der größte Nachteil von VSMs ist die leichte Beeinträchtigung (Abbildung 16). Lichtverursuchungen treten auf, wenn sich mehrere Schattencaster entlang der Ränder verdecken. VSMs schatten die Schattenränder basierend auf Tiefenunterschieden. Wenn sich Schatten überlappen, liegt in der Mitte einer Region, die überschattet werden soll, eine Tiefenunterschiede. Dies ist ein Problem bei der Verwendung des VSM-Algorithmus.

**Abbildung 16. VSM Light-Glühbirnen**

![vsm light light 2016](images/vsm-light-bleeding.png)

Eine Teillösung für das Problem besteht in der Auslösung von fPercentLit. Dies wirkt sich auf die Weichheit aus, was zu Artefakten führen kann, bei denen die Tiefenunterschiede gering sind. Manchmal gibt es einen magischen Wert, der das Problem entschärft.


```C++
fPercentLit = pow( p_max, MAGIC_NUMBER );
```



Eine Alternative zum Erhöhen des prozentzeptativen Lichts für eine Energie besteht in der Vermeidung von Konfigurationen, bei denen sich Schatten überlappen. Selbst bei stark optimierten Schattenkonfigurationen gelten mehrere Einschränkungen für Licht, Kamera und Geometrie. Lichtentspricht wird auch durch die Verwendung von Texturen mit höherer Auflösung gehärtet.

Mehrschichtige Varianzschattenkarten (Layered Variance Shadow Maps, LVSMs) lösen das Problem auf Kosten des Frustums in Schichten, die dem Licht durchlässig sind. Die Anzahl der erforderlichen Zuordnungen wäre sehr groß, wenn auch CSMs verwendet werden.

Darüber hinaus erläuterte Andrew Lauätten, Mitautor des Whitepapers zu VSMs und Autor eines Whitepapers zu LVSMs, die Kombination von Exponential Shadow Maps (ESMs) mit VSMs, um lichtblendendes Licht in einem [Beyond3D-Forum](https://forum.beyond3d.com/showthread.php?t=47427)zu überlisten.

## <a name="vsms-with-csms"></a>VSMs mit CSMs

Das Beispiel VarianceShadow11 kombiniert VSMs und CSMs. Die Kombination ist recht einfach. Das Beispiel folgt den gleichen Schritten wie das CascadedShadowMaps11-Beispiel. Da PCF nicht verwendet wird, werden die Schatten in einer trennbaren Konvolution mit zwei Durchgangen unscharf. Ohne PCF kann das Beispiel auch Texturarrays anstelle eines Texturatlas verwenden. PCF für Texturarrays ist ein Direct3D 10.1-Feature.

### <a name="gradients-with-csms"></a>Farbverläufe mit CSMs

Die Verwendung von Farbverläufen mit CSMs kann eine Naht entlang der Grenze zwischen zwei Kaskaden erzeugen, wie in Abbildung 17 dargestellt. Die Beispielanweisung verwendet Ableitungen zwischen Pixeln, um Informationen zu berechnen, z. B. die Mipmapebene, die vom Filter benötigt wird. Dies führt insbesondere bei der Mipmap-Auswahl oder bei anisotroper Filterung zu einem Problem. Wenn Pixel in einem Quader verschiedene Verzweigungen im Shader verwenden, sind die von der GPU-Hardware berechneten Ableitungen ungültig. Dies führt zu einer verkneinten Naht entlang der Schattenkarte.

**Abbildung 17. Naht an kaskadierenden Rahmen aufgrund einer anisotropen Filterung mit abweichender Flusssteuerung**

![Naht an kaskadierenden Rahmen aufgrund einer anisotropen Filterung mit abweichender Flusssteuerung](images/seams-on-cascade-borders-due-to-anisotropic.jpg)

Dieses Problem wird gelöst, indem die Ableitungen auf der Position im Lichtansichtsraum berechnen. Die Raumkoordinate der Lichtansicht ist nicht spezifisch für die ausgewählte Kaskadierung. Die berechneten Ableitungen können durch den Skalierungsteil der Projektionstexturmatrix auf die richtige Mipmapebene skaliert werden.


```C++
        float3 vShadowTexCoordDDX = ddx( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDX *= m_vCascadeScale[iCascade].xyz;
        float3 vShadowTexCoordDDY = ddy( vShadowMapTextureCoordViewSpace );
        vShadowTexCoordDDY *= m_vCascadeScale[iCascade].xyz;

        mapDepth += g_txShadow.SampleGrad( g_samShadow, vShadowTexCoord.xyz,
        vShadowTexCoordDDX, vShadowTexCoordDDY );
```



## <a name="vsms-compared-to-standard-shadows-with-pcf"></a>VSMs im Vergleich zu Standardschatten mit PCF

Sowohl VSMs als auch PCF versuchen, den Bruchteil des Pixelbereichs zu ungefähren, der den Tiefentest bestehen würde. VSMs arbeiten mit Filterhardware und können mit trennbaren Kerneln unscharf sein. Trennbare Konvolutionskernel sind erheblich kostengünstiger zu implementieren als ein vollständiger Kernel. Darüber hinaus vergleichen VSMs eine Lichtraumtiefe mit einem Wert in der Lichtraum-Tiefenkarte. Dies bedeutet, dass VSMs nicht die gleichen Offsetprobleme wie PCF haben. Technisch gesehen sind VSMs Stichprobentiefe über einen größeren Bereich und durchführen eine statistische Analyse. Dies ist weniger präzise als pcf. In der Praxis führen VSMs eine sehr gute Mischung durch, was dazu führt, dass weniger Offset erforderlich ist. Wie oben beschrieben, ist der Nachteil von VSMs die leichte Beeinträchtigung.

VSMs und PCF stellen einen Vergleich zwischen GPU-Computeleistung und GPU-Texturbandbreite dar. VsMs erfordern mehr mathematische Berechnungen, um die Varianz zu berechnen. PCF erfordert mehr Texturspeicherbandbreite. Große PCF-Kernel können durch die Texturbandbreite schnell zu Engpässen führen. Da die GPU-Berechnungsleistung schneller wächst als die GPU-Bandbreite, werden VSMs immer praktischer für die beiden Algorithmen. VSMs sehen auch besser aus, wenn Schattenkarten mit geringerer Auflösung aufgrund von Mischung und Filterung verwendet werden.

## <a name="summary"></a>Zusammenfassung

CSMs bieten eine Lösung für das Problem des Perspektivaliasings. Es gibt mehrere mögliche Konfigurationen, um die benötigte visuelle Genauigkeit für einen Titel zu erhalten. PCF und VSMs werden häufig verwendet und sollten mit CSMs kombiniert werden, um Aliasing zu reduzieren.

## <a name="references"></a>Referenzen

Donnelly, W. und Lauungen, A. [Variance shadow maps](https://portal.acm.org/citation.cfm?doid=1111411.1111440). In SI3D '06: Proceedings of the 2006 symposium on Interactive 3D graphics and games. 2006. S. 161–165. New York, NY, USA: ACM Press.

Laution, Andrew und Mc Wiege, Michael. [Mehrschichtige Varianzschattenkarten](https://portal.acm.org/citation.cfm?id=1375714.1375739&coll=GUIDE&dl=GUIDE&CFID=45360327&CFTOKEN=34578992). Proceedings of graphics interface 2008, May 28-30, 2008, Graphics Interface 2008, Canada.

Igkeit, Woflgang F. Abschnitt 4. Kaskadierte Schatten Karten. ShaderX5 , Erweiterte Renderingtechniken, Beim Rendern F. Beim Shader, Ed. Charles River Media, Boston, Bostons. 2006. S. 197–206.

 

 