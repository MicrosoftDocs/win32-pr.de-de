---
description: 'Alle von der Direct3D-Pipeline verwendeten Ressourcen werden aus zwei grundlegenden Ressourcentypen abgeleitet: Puffer und Texturen. Ein Puffer ist eine Auflistung von Rohdaten (Elemente). eine Textur ist eine Auflistung von texeln (Textur Elemente).'
ms.assetid: c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69
title: Ressourcentypen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec6ec9b57a2e504c137d424b19c61f2353d685e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560471"
---
# <a name="resource-types-direct3d-10"></a>Ressourcentypen (Direct3D 10)

Alle von der Direct3D-Pipeline verwendeten Ressourcen werden aus zwei grundlegenden Ressourcentypen abgeleitet: [Puffer](#buffer-resources) und [Texturen](#texture-resources). Ein Puffer ist eine Auflistung von Rohdaten (Elemente). eine Textur ist eine Auflistung von texeln (Textur Elemente).

-   [Puffer Ressourcen](#buffer-resources)
    -   [Puffer Typen](#buffer-types)
-   [Textur Ressourcen](#texture-resources)
    -   [Textur Typen](#texture-types)
    -   [Unterressourcen](#subresources)
    -   [Starke und schwache Typisierung](#strong-vs-weak-typing)
-   [Zugehörige Themen](#related-topics)

Es gibt zwei Möglichkeiten, das Layout (oder den Speicherbedarf) einer Ressource vollständig anzugeben:



| Element                                                                                                 | BESCHREIBUNG                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>Typ<br/>             | Geben Sie den Typ beim Erstellen der Ressource vollständig an.<br/>               |
| <span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>Typen losen<br/> | Geben Sie den Typ vollständig an, wenn die Ressource an die Pipeline gebunden ist.<br/> |



 

## <a name="buffer-resources"></a>Puffer Ressourcen

Eine Puffer Ressource ist eine Sammlung von vollständig typisierten Daten. intern enthält ein Puffer-Elemente. Ein Element besteht aus 1 bis 4 Komponenten. Beispiele für Element Datentypen: ein gepackter Datenwert (z. b. R8G8B8A8), eine einzelne 8-Bit-Ganzzahl, 4 32-Bit-Float-Werte. Diese Datentypen werden verwendet, um Daten zu speichern, z. b. einen Positions Vektor, einen normalen Vektor, eine Textur Koordinate in einem Vertex-Puffer, einen Index in einem Index Puffer oder einen Gerätezustand.

Ein Puffer wird als unstrukturierte Ressource erstellt. Da es nicht strukturiert ist, kann ein Puffer keine MipMap-Ebenen enthalten, wird beim Lesen nicht gefiltert und kann nicht mit einem Multisampling verwendet werden.

### <a name="buffer-types"></a>Puffer Typen

-   [Vertex-Puffer](#vertex-buffer)
-   [Indexpuffer](#index-buffer)
-   [Konstanter Puffer](#constant-buffer)

### <a name="vertex-buffer"></a>Vertex-Puffer

Ein Puffer ist eine Auflistung von Elementen. ein Vertex-Puffer enthält pro-Vertex-Daten. Das einfachste Beispiel ist ein Vertex-Puffer, der einen Datentyp enthält, z. b. Positionsdaten. Es kann wie in der folgenden Abbildung dargestellt werden.

![Abbildung eines Scheitelpunkt Puffers, der Positionsdaten enthält](images/d3d10-resources-single-element-vb2.png)

Häufig enthält ein Vertex-Puffer alle Daten, die erforderlich sind, um 3D-Vertices vollständig anzugeben. Ein Beispiel hierfür könnte ein Vertex-Puffer sein, der die Position des einzelnen Vertex, die normalen und die Texturkoordinaten enthält. Diese Daten werden in der Regel als Sätze von pro-Vertex-Elementen organisiert, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Scheitelpunkt Puffers, der Positions-, normal-und Textur Daten enthält](images/d3d10-vertex-buffer-element.png)

Dieser Vertex-Puffer enthält pro-Scheitelpunkt Daten für acht Vertices. jeder Scheitelpunkt speichert drei Elemente (Positions-, normal-und Texturkoordinaten). Die Position und normal werden üblicherweise mit 3 32-Bit-Gleit Komma Zahlen (DXGI- \_ Format \_ R32G32B32 \_ float) und den Texturkoordinaten mit 2 32-Bit-Gleit Komma Zahlen (DXGI- \_ Format \_ R32G32 \_ float) angegeben.

Für den Zugriff auf Daten aus einem Vertex-Puffer müssen Sie wissen, auf welchen Scheitelpunkt zugegriffen werden soll, und diese anderen Puffer Parameter angeben:

-   Offset: die Anzahl der Bytes vom Anfang des Puffers bis zu den Daten für den ersten Scheitelpunkt. Der Offset wird für [**iasetvertexbuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)bereitgestellt.
-   Basevertexlocation: die Anzahl der Bytes vom Offset bis zum ersten Vertex, der vom entsprechenden zeichnen-Befehl verwendet wird (siehe [Zeichnen-Methoden](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).

Vor dem Erstellen eines Scheitelpunkt Puffers müssen Sie sein Layout definieren, indem Sie ein [**Eingabe Layoutobjekt**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout)erstellen. Dies wird durch Aufrufen von [**createinputlayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout)erreicht. Nachdem das Eingabe Layout-Objekt erstellt wurde, binden Sie es an die Eingabe-Assembler-Phase durch Aufrufen von [**iasetinputlayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout).

Um einen Vertex-Puffer zu erstellen, rufen Sie " [**kreatebuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)" auf.

### <a name="index-buffer"></a>Indexpuffer

Ein Index Puffer enthält einen sequenziellen Satz von 16-Bit-oder 32-Bit-Indizes. Jeder Index wird zum Identifizieren eines Scheitel Punkts in einem Scheitelpunkt Puffer verwendet. Die Verwendung eines Index Puffers mit einem oder mehreren Scheitel Punkten zum Bereitstellen von Daten für die IA-Phase wird als Indizierung bezeichnet. Ein Index Puffer kann wie in der folgenden Abbildung dargestellt werden.

![Abbildung eines Index Puffers](images/d3d10-index-buffer.png)

Die in einem Index Puffer gespeicherten sequenziellen Indizes befinden sich mit den folgenden Parametern:

-   Offset: die Anzahl von Bytes vom Beginn des Puffers bis zum ersten Index. Der Offset wird für [**iasetindexbuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)bereitgestellt.
-   Startindexlocation: die Anzahl der Bytes vom Offset bis zum ersten Vertex, der vom entsprechenden zeichnen-Befehl verwendet wird (siehe [Zeichnen-Methoden](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).
-   IndexCount: die Anzahl der zu renderenden Indizes.

Um einen Index Puffer zu erstellen, rufen Sie " [**kreatebuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)" auf.

Ein Index Puffer kann mehrere Zeilen- [oder Dreiecks Streifen](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) Durchtrennen der einzelnen Zeilen-oder Dreiecks Bänder zusammenzufügen. Mit einem Strip-Cut-Index können mehrere Zeilen-oder Dreieck Striche mit einem einzelnen zeichnen-Befehl gezeichnet werden. Ein Strip-Ausschneide Index ist einfach der maximal mögliche Wert für den Index (0xFFFF für einen 16-Bit-Index, 0xFFFFFFFF für einen 32-Bit-Index). Der Strip-Cut-Index setzt die aufzurufende Reihenfolge in indizierten primitiven zurück und kann verwendet werden, um den Bedarf an degenerierten Dreiecken zu entfernen, die andernfalls erforderlich sind, um die richtige Sortierreihenfolge in einem Dreiecks Band beizubehalten Die folgende Abbildung zeigt ein Beispiel für einen Index Ausschneide Index.

![Abbildung eines Index Ausschneide Index](images/d3d10-ia-strips-cut-value.png)

### <a name="constant-buffer"></a>Konstanter Puffer

Direct3D 10 hat einen neuen Puffer zum Bereitstellen von Shader-Konstanten eingeführt, die als Shader-Konstantenpuffer oder einfach als konstanter Puffer bezeichnet werden. Konzeptionell sieht es wie ein Einzelelement-Vertexpuffer aus, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Shaders-konstantenpuffers](images/d3d10-shader-resource-buffer.png)

Jedes Element speichert eine 1-zu-4-Komponenten Konstante, die durch das Format der gespeicherten Daten bestimmt wird.

Konstantenpuffer reduzieren die erforderliche Bandbreite, um shaderkonstanten zu aktualisieren, indem Sie zulassen, dass Shader-Konstanten gleichzeitig gruppiert und ein Commit ausgeführt werden, anstatt einzelne Aufrufe zum separaten Commit der einzelnen Konstanten zu erstellen.

Um einen Shader-Konstantenpuffer zu erstellen, rufen Sie " [**kreatebuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) " auf, und geben Sie das Konstante Puffer Bindungs Flag d3d10 \_ Bind \_ Constant \_ buffer (siehe [**d3d10 \_ Bind- \_ Flag**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)) an.

Um einen Shader-Konstantenpuffer an die Pipeline zu binden, können Sie eine der folgenden Methoden aufrufen: [**gssetconstantbuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers), [**pssetconstantbuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers)oder [**vssetconstantbuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers).

Beachten Sie, dass bei Verwendung der [**ID3D10Effect-Schnittstellen**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) Schnittstelle der Prozess des Erstellens, Bindungs-und Auslassen eines konstanten Puffers von der **ID3D10Effect-Schnittstellen** Instanz verarbeitet wird. In diesem Fall ist es nur notwendig, die Variable aus dem Effekt mit einer der GetVariable-Methoden (z. b. [**getvariablebyname**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) ) zu erhalten und die Variable mit einer der SetVariable-Methoden (z. b. [**setMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix)) zu aktualisieren. Ein Beispiel für die Verwendung der **ID3D10Effect-Schnittstelle** zum Verwalten eines konstanten Puffers finden Sie unter [Tutorial 07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

Ein Shader liest weiterhin Variablen in einem konstanten Puffer direkt über den Variablennamen in derselben Weise, wie Variablen, die nicht Teil eines konstanten Puffers sind, gelesen werden.

Jede Shader-Stufe ermöglicht bis zu 15 Shader-Konstante Puffer. jeder Puffer kann bis zu 4096 Konstanten enthalten.

Verwenden Sie einen konstanten Puffer, um die Ergebnisse der Stream-Output-Phase zu speichern.

Ein Beispiel für das Deklarieren eines konstanten Puffers in einem Shader finden Sie unter [Shader-Konstanten (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-constants.md) .

## <a name="texture-resources"></a>Textur Ressourcen

Eine Textur Ressource ist eine strukturierte Sammlung von Daten, die zum Speichern von texeln entwickelt wurden. Im Gegensatz zu puffern können Texturen durch Textur-samplz gefiltert werden, wenn Sie von Shader-Einheiten gelesen werden. Der Typ der Textur wirkt sich darauf aus, wie die Textur gefiltert wird. Ein Texel stellt die kleinste Einheit einer Textur dar, die von der Pipeline gelesen oder geschrieben werden kann. Jeder textextetyp enthält 1 bis 4 Komponenten, die in einem der DXGI-Formate angeordnet sind (siehe [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).

Texturen werden als strukturierte Ressource erstellt, sodass ihre Größe bekannt ist. Allerdings kann jede Textur eingegeben werden, oder Sie wird zur Zeit der Ressourcen Erstellung weniger eingegeben, solange der Typ vollständig mit einer Sicht angegeben wird, wenn die Textur an die Pipeline gebunden ist.

-   [Textur Typen](#texture-types)
-   [Unterressourcen](#subresources)
-   [Starke und schwache Typisierung](#strong-vs-weak-typing)

### <a name="texture-types"></a>Textur Typen

Es gibt mehrere Arten von Texturen: 1D, 2D, 3D, von denen jede mit oder ohne Mipmaps erstellt werden kann. Direct3D 10 unterstützt auch Textur Arrays und Multisampling-Texturen.

-   [1D-Textur](#1d-texture)
-   [1D-Textur Array](#1d-texture-array)
-   [2D-Textur und 2D-Textur Array](#2d-texture-and-2d-texture-array)
-   [3D-Textur](#3d-texture)

### <a name="1d-texture"></a>1D-Textur

Eine 1D-Textur in der einfachsten Form enthält Textur Daten, die mit einer einzelnen Textur Koordinate adressiert werden können. Sie kann als Array von Texels visualisiert werden, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 1D-Textur](images/d3d10-1d-texture.png)

Jede Texel enthält eine Reihe von Farbkomponenten, abhängig vom Format der gespeicherten Daten. Wenn Sie weitere Komplexität hinzufügen, können Sie eine 1D-Textur mit MipMap-Ebenen erstellen, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 1D-Textur mit MipMap-Ebenen](images/d3d10-resource-texture1d.png)

Bei einer MipMap-Ebene handelt es sich um eine Textur, bei der es sich um eine Potenz von zwei kleiner als der darüber liegenden Ebene handelt. Die oberste Ebene enthält die meisten Details, jede nachfolgende Ebene ist kleiner. bei einer 1D-MipMap enthält die kleinste Ebene eine texsebene. Die unterschiedlichen Ebenen werden durch einen Index identifiziert, der als "LOD" (Detailstufe) bezeichnet wird. Sie können den Lod verwenden, um auf eine kleinere Textur zuzugreifen, wenn Sie Geometrie rendern, die nicht so nah wie die Kamera ist.

### <a name="1d-texture-array"></a>1D-Textur Array

Direct3D 10 verfügt auch über eine neue Datenstruktur für ein Array von Texturen. Ein Array von 1D-Texturen sieht konzeptionell wie in der folgenden Abbildung aus.

![Abbildung eines 1D-Textur Arrays](images/d3d10-resource-texture1darray.png)

Dieses Textur Array enthält drei Texturen. Jede der drei Texturen hat eine Textur Breite von 5 (die Anzahl der Elemente in der ersten Ebene). Jede Textur enthält auch eine 3-Ebenen-MipMap.

Alle Textur Arrays in Direct3D sind ein homogenes Array von Texturen. Dies bedeutet, dass jede Textur in einem Textur Array das gleiche Datenformat und die gleiche Größe aufweisen muss (einschließlich der Textur Breite und der Anzahl von MipMap-Ebenen). Sie können Textur Arrays mit unterschiedlichen Größen erstellen, sofern alle Texturen in den einzelnen Arrays in der Größe zueinander passen.

### <a name="2d-texture-and-2d-texture-array"></a>2D-Textur und 2D-Textur Array

Eine Texture2D-Ressource enthält ein 2D-Raster mit texeln. Jedes texttuton ist durch einen u-v-Vektor adressierbar. Da es sich um eine Textur Ressource handelt, kann Sie MipMap-Ebenen und untergeordnete Quellen enthalten. Eine vollständig aufgefüllte 2D-Textur Ressource sieht wie in der folgenden Abbildung aus.

![Abbildung einer 2D-Textur Ressource](images/d3d10-resource-texture2d.png)

Diese Textur Ressource enthält eine einzelne 3x5-Textur mit drei MipMap-Ebenen.

Eine Texture2DArray-Ressource ist ein homogenes Array von 2D-Texturen. Das heißt, jede Textur hat das gleiche Datenformat und die gleichen Dimensionen (einschließlich MipMap-Ebenen). Es verfügt über ein ähnliches Layout wie das 1D-Textur Array, mit dem Unterschied, dass die Texturen nun 2D-Daten enthalten und daher wie in der folgenden Abbildung aussehen.

![Abbildung eines Arrays von 2D-Textur Ressourcen](images/d3d10-resource-texture2darray.png)

Dieses Textur Array enthält drei Texturen. Jede Textur ist 3x5 mit zwei MipMap-Ebenen.

### <a name="using-a-texture2darray-as-a-texture-cube"></a>Verwenden eines Texture2DArray als Textur Cube

Ein Textur Cube ist ein 2D-Textur Array, das 6 Texturen enthält, eine für jedes Gesicht des Cubes. Ein vollständig aufgefüllter Textur Cube sieht wie die folgende Abbildung aus.

![Abbildung eines Arrays von 2D-Textur Ressourcen, die einen Textur Cube darstellen](images/d3d10-resource-texturecube.png)

Ein 2D-Textur Array, das 6 Texturen enthält, kann aus Shader mit den intrinsischen cubemap-Funktionen gelesen werden, nachdem Sie mit einer cubetextansicht an die Pipeline gebunden wurden. Textur Cubes werden vom Shader mit einem 3D-Vektor adressiert, der aus der Mitte des Textur Cubes zeigt.

### <a name="3d-texture"></a>3D-Textur

Eine Texture3D-Ressource (auch als volumetextur bezeichnet) enthält eine 3D-Menge an texeln. Da es sich um eine Textur Ressource handelt, kann Sie MipMap-Ebenen enthalten. Eine vollständig aufgefüllte [**3D-Textur**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) sieht wie in der folgenden Abbildung aus.

![Abbildung einer 3D--Textur Ressource](images/d3d10-resource-texture3d.png)

Wenn ein 3D-Textur-MipMap-Slice als renderzielausgabe (mit einer renderzielansicht) gebunden wird, verhält sich die 3D-Textur identisch mit einem 2D-Textur Array mit n Slices. Der jeweilige renderslice wird aus der Geometrie-Shader-Stufe ausgewählt, indem eine skalare Komponente der Ausgabedaten als der "SV \_ rendertargetarrayindex"-System Wert deklariert wird.

Es gibt kein Konzept eines 3D-Textur Arrays. Daher ist eine 3D-Textur-unter Quelle eine einzelne MipMap-Ebene.

### <a name="subresources"></a>Unterressourcen

Die Direct3D 10-API verweist auf ganze Ressourcen oder Teilmengen von Ressourcen. Um einen Teil der Ressourcen anzugeben, hat Direct3D den Begriff unter Berichte geprägt, was eine Teilmenge einer Ressource bedeutet.

Ein Puffer ist als einzelne untergeordnete Quelle definiert. Texturen sind etwas komplizierter, da einige verschiedene Textur Typen (1D, 2D usw.) enthalten, von denen einige MipMap-Ebenen und/oder Textur Arrays unterstützen. Beginnend mit dem einfachsten Fall wird eine 1D-Textur als einzelne untergeordnete Quelle definiert, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 1D-Textur](images/d3d10-1d-texture.png)

Dies bedeutet, dass das Array von texeln, die eine 1D-Textur bilden, in einer einzelnen untergeordneten Quelle enthalten ist.

Wenn Sie eine 1D-Textur mit drei MipMap-Ebenen erweitern, kann Sie wie folgt visualisiert werden.

![Abbildung einer 1D-Textur mit MipMap-Ebenen](images/d3d10-resource-texture1d.png)

Stellen Sie sich dies als eine einzelne Textur vor, die aus drei unter Texturen besteht. Jede Unterstruktur wird als untergeordnete Quelle gezählt, sodass diese 1D-Textur drei unter Ressourcen enthält. Eine Unterstruktur (oder untergeordnete Quelle) kann mit der Detailgenauigkeit (ausführlich) für eine einzelne Textur indiziert werden. Wenn Sie ein Array von Texturen verwenden, erfordert der Zugriff auf eine bestimmte Teil Textur sowohl die Lod als auch die bestimmte Textur. Alternativ kombiniert die API diese beiden Informationen in einem einzelnen Null basierten unter Quell Index, wie hier gezeigt.

![Abbildung eines NULL basierten unter Quell Indexes](images/d3d10-resource-texture1darray-sub-indexing.png)

### <a name="selecting-subresources"></a>Auswählen von unter Ressourcen

Einige APIs greifen auf eine gesamte Ressource zu (z. b. [**copyresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)), andere greifen auf einen Teil einer Ressource zu (z. b. [**updatesubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) oder [**copysubresourceregion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)). Die API, die auf einen Teil einer Ressource zugreift, verwendet in der Regel eine Ansichts Beschreibung (z. b. [**d3d10 \_ TEX2D \_ array \_ DSV**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)), um die unter Ressourcen anzugeben, auf die zugegriffen werden soll.

Diese Abbildungen veranschaulichen die Begriffe, die durch eine Ansichts Beschreibung beim Zugriff auf ein Array von Texturen verwendet werden.

### <a name="array-slice"></a>Array Slice

Bei einem Array von Texturen enthält jede Textur mit Mipmaps, ein Array Slice (dargestellt durch das weiße Rechteck), eine Textur und alle zugehörigen unter Texturen, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Array Splice](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>MIP-Slice

Ein MIP-Slice (dargestellt durch das weiße Rechteck) enthält eine MipMap-Ebene für jede Textur in einem Array, wie in der folgenden Abbildung dargestellt.

![Abbildung einer MIP-Splice](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Auswählen einer einzelnen untergeordneten Quelle

Sie können diese beiden Arten von Slices verwenden, um eine einzelne untergeordnete Quelle auszuwählen, wie in der folgenden Abbildung dargestellt.

![Abbildung der Auswahl eines unter Berichts mithilfe eines Array Slice und eines MIP-Splice](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Auswählen mehrerer unter Ressourcen

Oder Sie können diese beiden Arten von Slices mit der Anzahl von MipMap-Ebenen und/oder der Anzahl von Texturen verwenden, um mehrere unter Ressourcen auszuwählen.

![Darstellung der Auswahl mehrerer unter Ressourcen](images/d3d10-resource-subresources-2.png)

Unabhängig davon, welchen Arraytyp Sie verwenden, mit oder ohne Mipmaps mit oder ohne ein Textur Array können Sie die Hilfsfunktion [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)verwenden, um den Index einer bestimmten unter Quelle zu berechnen.

### <a name="strong-vs-weak-typing"></a>Starke und schwache Typisierung

Durch das Erstellen einer vollständig typisierten Ressource wird die Ressource auf das Format beschränkt, mit dem Sie erstellt wurde. Dadurch kann die Laufzeit den Zugriff optimieren, insbesondere dann, wenn die Ressource mit Flags erstellt wird, die angeben, dass Sie nicht von der Anwendung [zugeordnet](d3d10-graphics-programming-guide-resources-mapping.md) werden kann. Ressourcen, die mit einem bestimmten Typ erstellt wurden, können nicht mit dem Ansichts Mechanismus neu interpretiert werden.

In einer Ressource vom Typ less ist der Datentyp beim ersten Erstellen der Ressource unbekannt. Die Anwendung muss aus den verfügbaren Typen weniger Formate auswählen (siehe [**DXGI- \_ Format**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Sie müssen die Größe des zuzuordnenden Speichers angeben und angeben, ob die Laufzeit die Unterstrukturen in einer MipMap generieren muss. Allerdings wird das genaue Datenformat (unabhängig davon, ob der Arbeitsspeicher als ganze Zahlen, Gleit Komma Werte, ganze Zahlen ohne Vorzeichen usw. interpretiert wird) erst bestimmt, wenn die Ressource mit einer Ansicht an die Pipeline gebunden ist. Da das Textur Format flexibel bleibt, bis die Textur an die Pipeline gebunden ist, wird die Ressource als schwach typisierter Speicher bezeichnet. Schwach typisierter Speicher hat den Vorteil, dass er wieder verwendet oder erneut interpretiert werden kann (in einem anderen Format), solange das Komponenten Bit des neuen Formats mit der Bitzahl des alten Formats übereinstimmt.

Eine einzelne Ressource kann an mehrere Pipeline Stufen gebunden werden, solange Sie jeweils über eine eindeutige Ansicht verfügen, die die Formate der einzelnen Speicherorte vollständig qualifiziert. Beispielsweise könnte eine Ressource, die mit dem Format DXGI \_ Format \_ R32G32B32A32 typless erstellt wurde, \_ als DXGI \_ \_ -Format R32G32B32A32 \_ float und ein DXGI- \_ Format \_ R32G32B32A32 \_ uint an verschiedenen Positionen in der Pipeline gleichzeitig verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
