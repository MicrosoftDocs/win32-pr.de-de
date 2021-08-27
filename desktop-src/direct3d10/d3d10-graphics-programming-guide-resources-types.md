---
description: 'Alle von der Direct3D-Pipeline verwendeten Ressourcen werden von zwei grundlegenden Ressourcentypen ableiten: Puffer und Texturen. Ein Puffer ist eine Sammlung von Rohdaten (Elementen). eine Textur ist eine Sammlung von Texeln (Texturelementen).'
ms.assetid: c5238a2f-d69d-4ce5-a5aa-66a6c18d5f69
title: Ressourcentypen (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b0f757eac93fac8c0ffd49641441fa4570824670dfcca9c3d271f954054548b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120104"
---
# <a name="resource-types-direct3d-10"></a>Ressourcentypen (Direct3D 10)

Alle von der Direct3D-Pipeline verwendeten Ressourcen werden von zwei grundlegenden Ressourcentypen ableiten: [Puffer und](#buffer-resources) [Texturen.](#texture-resources) Ein Puffer ist eine Sammlung von Rohdaten (Elementen). eine Textur ist eine Sammlung von Texeln (Texturelementen).

-   [Pufferressourcen](#buffer-resources)
    -   [Puffertypen](#buffer-types)
-   [Texturressourcen](#texture-resources)
    -   [Texturtypen](#texture-types)
    -   [Unterressourcen](#subresources)
    -   [Starke und schwache Typisierung](#strong-vs-weak-typing)
-   [Zugehörige Themen](#related-topics)

Es gibt zwei Möglichkeiten, das Layout (oder den Speicherbedarf) einer Ressource vollständig anzugeben:



| Element                                                                                                 | Beschreibung                                                                   |
|------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span id="Typed"></span><span id="typed"></span><span id="TYPED"></span>Typisierte<br/>             | Geben Sie den Typ vollständig an, wenn die Ressource erstellt wird.<br/>               |
| <span id="Typeless"></span><span id="typeless"></span><span id="TYPELESS"></span>Typenloses<br/> | Geben Sie den Typ vollständig an, wenn die Ressource an die Pipeline gebunden ist.<br/> |



 

## <a name="buffer-resources"></a>Pufferressourcen

Eine Pufferressource ist eine Sammlung von vollständig typierten Daten. intern enthält ein Puffer Elemente. Ein Element besteht aus 1 bis 4 Komponenten. Beispiele für Elementdatentypen sind: ein gepackter Datenwert (z. B. R8G8B8A8), eine einzelne 8-Bit-Ganzzahl, vier 32-Bit-Gleitkommawerte. Diese Datentypen werden verwendet, um Daten zu speichern, z. B. einen Positionsvektor, einen normalen Vektor, eine Texturkoordinate in einem Scheitelpunktpuffer, einen Index in einem Indexpuffer oder den Gerätezustand.

Ein Puffer wird als unstrukturierte Ressource erstellt. Da er unstrukturiert ist, kann ein Puffer keine Mipmapebenen enthalten, wird beim Lesen nicht gefiltert und kann nicht mehrfach verwendet werden.

### <a name="buffer-types"></a>Puffertypen

-   [Scheitelpunktpuffer](#vertex-buffer)
-   [Indexpuffer](#index-buffer)
-   [Konstanter Puffer](#constant-buffer)

### <a name="vertex-buffer"></a>Scheitelpunktpuffer

Ein Puffer ist eine Auflistung von Elementen. Ein Scheitelpunktpuffer enthält Daten pro Scheitelpunkt. Das einfachste Beispiel ist ein Scheitelpunktpuffer, der einen Datentyp enthält, z. B. Positionsdaten. Sie kann wie in der folgenden Abbildung visualisiert werden.

![Abbildung eines Scheitelpunktpuffers, der Positionsdaten enthält](images/d3d10-resources-single-element-vb2.png)

Häufiger enthält ein Scheitelpunktpuffer alle Daten, die erforderlich sind, um 3D-Scheitelpunkte vollständig anzugeben. Ein Beispiel hierfür ist ein Scheitelpunktpuffer, der die Position pro Scheitelpunkt, normal und Texturkoordinaten enthält. Diese Daten sind in der Regel wie in der folgenden Abbildung dargestellt als Sätze von Elementen pro Scheitelpunkt organisiert.

![Abbildung eines Scheitelpunktpuffers, der Positions-, Normal- und Texturdaten enthält](images/d3d10-vertex-buffer-element.png)

Dieser Scheitelpunktpuffer enthält Pro-Scheitelpunkt-Daten für acht Scheitelpunkte. Jeder Scheitelpunkt speichert drei Elemente (Positions-, Normal- und Texturkoordinaten). Die Position und der Normalwert werden in der Regel mithilfe von drei 32-Bit-Gleitkommaen (DXGI FORMAT R32G32B32 FLOAT) und den Texturkoordinaten mit zwei \_ \_ \_ 32-Bit-Gleitkommaen (DXGI \_ FORMAT \_ R32G32 \_ FLOAT) angegeben.

Um von einem Scheitelpunktpuffer auf Daten zu zugreifen, müssen Sie wissen, auf welchen Scheitelpunkt und auf welche anderen Pufferparameter sie zugreifen müssen:

-   Offset: Die Anzahl der Bytes vom Anfang des Puffers bis zu den Daten für den ersten Scheitelpunkt. Der Offset wird für [**IASetVertexBuffers bereitgestellt.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetvertexbuffers)
-   BaseVertexLocation: Die Anzahl der Bytes vom Offset bis zum ersten Scheitelpunkt, der vom entsprechenden Zeichnen-Aufruf verwendet wird (siehe [Draw-Methoden](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).

Bevor Sie einen Scheitelpunktpuffer erstellen, müssen Sie sein Layout definieren, indem Sie ein [**Eingabelayoutobjekt erstellen.**](/windows/win32/api/d3d10/nn-d3d10-id3d10inputlayout) Dies erfolgt durch Aufrufen [**von CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout). Nachdem das Eingabelayoutobjekt erstellt wurde, binden Sie es an die Eingabe-Assembler-Phase, indem [**Sie IASetInputLayout aufrufen.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetinputlayout)

Um einen Scheitelpunktpuffer zu erstellen, rufen Sie [**CreateBuffer auf.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)

### <a name="index-buffer"></a>Indexpuffer

Ein Indexpuffer enthält einen sequenziellen Satz von 16-Bit- oder 32-Bit-Indizes. Jeder Index wird verwendet, um einen Scheitelpunkt in einem Scheitelpunktpuffer zu identifizieren. Die Verwendung eines Indexpuffers mit einem oder mehr Scheitelpunktpuffern zur Bereitstellung von Daten für die IA-Phase wird als Indizierung bezeichnet. Ein Indexpuffer kann wie in der folgenden Abbildung visualisiert werden.

![Abbildung eines Indexpuffers](images/d3d10-index-buffer.png)

Die sequenziellen Indizes, die in einem Indexpuffer gespeichert sind, befinden sich mit den folgenden Parametern:

-   Offset: Die Anzahl der Bytes vom Anfang des Puffers bis zum ersten Index. Der Offset wird für [**IASetIndexBuffer bereitgestellt.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-iasetindexbuffer)
-   StartIndexLocation: Die Anzahl der Bytes vom Offset bis zum ersten Scheitelpunkt, der vom entsprechenden Zeichnen-Aufruf verwendet wird (siehe [Draw-Methoden](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage-getting-started.md)).
-   IndexCount: Die Anzahl der zu rendernden Indizes.

Um einen Indexpuffer zu erstellen, rufen Sie [**CreateBuffer auf.**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer)

Ein Indexpuffer kann mehrere Linien- oder [Dreiecksstreifen](../direct3d11/d3d10-graphics-programming-guide-primitive-topologies.md) zusammenheften, indem jeder durch einen Striptripindex getrennt wird. Ein Striptripindex ermöglicht das Zeichnen mehrerer Linien- oder Dreiecksstreifen mit einem einzigen Zeichnen-Aufruf. Ein Strip-Cut-Index ist einfach der maximal mögliche Wert für den Index (0xffff für einen 16-Bit-Index, 0xffffffff für einen 32-Bit-Index). Der Strip-Cut-Index setzt die Wickelrichtung in indizierten Primitiven zurück und kann verwendet werden, um die Notwendigkeit von degenerierten Dreiecken zu beseitigen, die andernfalls möglicherweise erforderlich sind, um die richtige Wickelrichtung in einem Dreiecksstreifen zu erhalten. Die folgende Abbildung zeigt ein Beispiel für einen Striptripindex.

![Abbildung eines Strip-Cut-Index](images/d3d10-ia-strips-cut-value.png)

### <a name="constant-buffer"></a>Konstanter Puffer

Direct3D 10 hat einen neuen Puffer für die Bereitstellung von Shaderkonstten eingeführt, die als Shaderkonst constant buffer oder einfach als konstanter Puffer bezeichnet werden. Konzeptionell sieht es wie ein Scheitelpunktpuffer mit einem einzelnen Element aus, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Shaderkonst constant-Puffers](images/d3d10-shader-resource-buffer.png)

Jedes Element speichert eine 1:4-Komponentenkonst konstante, die durch das Format der gespeicherten Daten bestimmt wird.

Konstante Puffer verringern die Bandbreite, die zum Aktualisieren von Shaderkonst constants erforderlich ist, indem shader-Konstanten gleichzeitig gruppiert und commitiert werden können, anstatt einzelne Aufrufe zum getrennten Commit jeder Konstante zu tätigen.

Rufen Sie zum Erstellen eines Shaderkonst constant-Puffers [**CreateBuffer**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createbuffer) auf, und geben Sie das Bindungsflag D3D10 \_ BIND CONSTANT BUFFER an \_ \_ (siehe [**D3D10 \_ BIND \_ FLAG**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_bind_flag)).

Um einen Shaderkonstantenpuffer an die Pipeline zu binden, rufen Sie eine der folgenden Methoden auf: [**GSSetConstantBuffers,**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-gssetconstantbuffers) [**PSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-pssetconstantbuffers)oder [**VSSetConstantBuffers**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-vssetconstantbuffers).

Beachten Sie, dass bei Verwendung der [**ID3D10Effect-Schnittstelle**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect) der Prozess zum Erstellen, Binden und Kompensieren eines konstanten Puffers von der **ID3D10Effect Interface-Instanz verarbeitet** wird. In diesem Fall ist es nur neskesär, die Variable mit einer der GetVariable-Methoden wie [**GetVariableByName**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effect-getvariablebyname) aus dem Effekt zu erhalten und die Variable mit einer der SetVariable-Methoden wie [**SetMatrix**](/windows/desktop/api/D3D10Effect/nf-d3d10effect-id3d10effectmatrixvariable-setmatrix)zu aktualisieren. Ein Beispiel für die Verwendung der **ID3D10Effect-Schnittstelle** zum Verwalten eines konstanten Puffers finden Sie im [Tutorial 07](https://msdn.microsoft.com/library/Ee416442(v=VS.85).aspx).

Ein Shader liest Variablen in einem konstanten Puffer weiterhin direkt über den Variablennamen auf die gleiche Weise, wie Variablen gelesen werden, die nicht Teil eines konstanten Puffers sind.

Jede Shaderstufe lässt bis zu 15 Shaderkonst constant-Puffer zu. Jeder Puffer kann bis zu 4096 Konstanten halten.

Verwenden Sie einen konstanten Puffer, um die Ergebnisse der Streamausgabephase zu speichern.

Ein Beispiel zum Deklarieren eines konstanten Puffers in einem Shader finden Sie unter [Shaderkonstten (DirectX HLSL).](../direct3dhlsl/dx-graphics-hlsl-constants.md)

## <a name="texture-resources"></a>Texturressourcen

Eine Texturressource ist eine strukturierte Sammlung von Daten zum Speichern von Texeln. Im Gegensatz zu Puffern können Texturen nach Textur-Samplern gefiltert werden, während sie von Shadereinheiten gelesen werden. Der Texturtyp wirkt sich auf die Filterung der Textur aus. Ein Texel stellt die kleinste Einheit einer Textur dar, die von der Pipeline gelesen oder geschrieben werden kann. Jedes Texel enthält 1 bis 4 Komponenten, die in einem der DXGI-Formate angeordnet sind (siehe [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).

Texturen werden als strukturierte Ressource erstellt, damit ihre Größe bekannt ist. Allerdings kann jede Textur zum Zeitpunkt der Ressourcenerstellung typiert oder kleiner sein, solange der Typ vollständig mithilfe einer Ansicht angegeben wird, wenn die Textur an die Pipeline gebunden ist.

-   [Texturtypen](#texture-types)
-   [Unterressourcen](#subresources)
-   [Starke und schwache Typisierung](#strong-vs-weak-typing)

### <a name="texture-types"></a>Texturtypen

Es gibt mehrere Arten von Texturen: 1D, 2D, 3D, von denen jede mit oder ohne Mipmaps erstellt werden kann. Direct3D 10 unterstützt auch Texturarrays und Multisampled-Texturen.

-   [1D-Textur](#1d-texture)
-   [1D-Texturarray](#1d-texture-array)
-   [2D-Textur und 2D-Texturarray](#2d-texture-and-2d-texture-array)
-   [3D-Textur](#3d-texture)

### <a name="1d-texture"></a>1D-Textur

Eine 1D-Textur in ihrer einfachsten Form enthält Texturdaten, die mit einer einzelnen Texturkoordinate adressiert werden können. Sie kann wie in der folgenden Abbildung dargestellt als Array von Texel visualisiert werden.

![Abbildung einer 1d-Textur](images/d3d10-1d-texture.png)

Jedes Texel enthält abhängig vom Format der gespeicherten Daten eine Reihe von Farbkomponenten. Wenn Sie die Komplexität erhöhen, können Sie eine 1D-Textur mit Mipmapebenen erstellen, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 1d-Textur mit Mipmapebenen](images/d3d10-resource-texture1d.png)

Eine Mipmapebene ist eine Textur, die eine Potenz von zwei ist, die kleiner als die ebene darüber ist. Die oberste Ebene enthält die meisten Details, jede nachfolgende Ebene ist kleiner. Für ein 1D-Mipmap enthält die kleinste Ebene ein Texel. Die unterschiedlichen Ebenen werden durch einen Index identifiziert, der als LOD (Detailebene) bezeichnet wird. Sie können die LOD verwenden, um beim Rendern von Geometrie, die sich nicht so nah an der Kamera befindet, auf eine kleinere Textur zuzugreifen.

### <a name="1d-texture-array"></a>1D-Texturarray

Direct3D 10 verfügt auch über eine neue Datenstruktur für ein Array von Texturen. Ein Array von 1D-Texturen sieht konzeptionell wie in der folgenden Abbildung aus.

![Abbildung eines 1D-Texturarrays](images/d3d10-resource-texture1darray.png)

Dieses Texturarray enthält drei Texturen. Jede der drei Texturen hat eine Texturbreite von 5 (die Anzahl der Elemente in der ersten Ebene). Jede Textur enthält auch eine Mipmap mit drei Ebenen.

Alle Texturarrays in Direct3D sind ein homogenes Array von Texturen. Dies bedeutet, dass jede Textur in einem Texturarray das gleiche Datenformat und dieselbe Größe aufweisen muss (einschließlich Texturbreite und Anzahl von Mipmapebenen). Sie können Texturarrays unterschiedlicher Größe erstellen, solange alle Texturen in jedem Array in ihrer Größe übereinstimmen.

### <a name="2d-texture-and-2d-texture-array"></a>2D-Textur und 2D-Texturarray

Eine Texture2D-Ressource enthält ein 2D-Raster aus Texel. Jedes Texel kann durch einen u,v-Vektor adressiert werden. Da es sich um eine Texturressource handelt, kann sie Mipmapebenen und Unterressourcen enthalten. Eine vollständig aufgefüllte 2D-Texturressource sieht wie in der folgenden Abbildung aus.

![Abbildung einer 2D-Texturressource](images/d3d10-resource-texture2d.png)

Diese Texturressource enthält eine einzelne 3x5-Textur mit drei Mipmapebenen.

Eine Texture2DArray-Ressource ist ein homogenes Array von 2D-Texturen. Das heißt, jede Textur hat das gleiche Datenformat und die gleichen Dimensionen (einschließlich Mipmapebenen). Es verfügt über ein ähnliches Layout wie das 1D-Texturarray, mit der Ausnahme, dass die Texturen jetzt 2D-Daten enthalten und daher wie in der folgenden Abbildung aussehen.

![Abbildung eines Arrays von 2D-Texturressourcen](images/d3d10-resource-texture2darray.png)

Dieses Texturarray enthält drei Texturen: jede Textur ist 3x5 mit zwei Mipmapebenen.

### <a name="using-a-texture2darray-as-a-texture-cube"></a>Verwenden eines Texture2DArray als Texturcube

Ein Texturcube ist ein 2D-Texturarray, das 6 Texturen enthält, eine für jedes Gesicht des Würfels. Ein vollständig aufgefüllter Texturcube sieht wie in der folgenden Abbildung aus.

![Abbildung eines Arrays von 2d-Texturressourcen, die einen Texturcube darstellen](images/d3d10-resource-texturecube.png)

Ein 2D-Texturarray, das 6 Texturen enthält, kann mit den systeminternen Funktionen der Cubezuordnung aus Shadern gelesen werden, nachdem sie mit einer Cubetexturansicht an die Pipeline gebunden wurden. Texturcubes werden vom Shader mit einem 3D-Vektor adressiert, der von der Mitte des Texturcubes aus verweist.

### <a name="3d-texture"></a>3D-Textur

Eine Texture3D-Ressource (auch als Volumetextur bezeichnet) enthält ein 3D-Volumen von Texel. Da es sich um eine Texturressource handelt, kann sie Mipmapebenen enthalten. Eine vollständig [**aufgefüllte 3D-Textur**](/windows/desktop/api/D3D10/nn-d3d10-id3d10texture3d) sieht wie in der folgenden Abbildung aus.

![Abbildung einer 3D-Texturressource](images/d3d10-resource-texture3d.png)

Wenn ein 3D-Textur-Mipmapslice als Renderzielausgabe gebunden wird (mit einer Renderzielansicht), verhält sich die 3D-Textur identisch mit einem 2D-Texturarray mit n Slices. Der jeweilige Renderslice wird in der Geometry-Shader-Phase ausgewählt, indem eine Skalarkomponente der Ausgabedaten als Systemwert SV \_ RenderTargetArrayIndex deklariert wird.

Es gibt kein Konzept eines 3D-Texturarrays. daher ist eine 3D-Texturunterressource eine einzelne Mipmapebene.

### <a name="subresources"></a>Unterressourcen

Die Direct3D 10-API verweist auf ganze Ressourcen oder Teilmengen von Ressourcen. Um einen Teil der Ressourcen anzugeben, hat Direct3D den Begriff Unterressourcen beeinflusst, was eine Teilmenge einer Ressource bedeutet.

Ein Puffer wird als einzelne Unterressource definiert. Texturen sind etwas komplizierter, da es mehrere verschiedene Texturtypen (1D, 2D usw.) gibt, von denen einige Mipmapebenen und/oder Texturarrays unterstützen. Beginnend mit dem einfachsten Fall wird eine 1D-Textur als einzelne Unterressource definiert, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 1d-Textur](images/d3d10-1d-texture.png)

Dies bedeutet, dass das Array von Texeln, aus denen eine 1D-Textur besteht, in einer einzelnen Unterressource enthalten ist.

Wenn Sie eine 1D-Textur mit drei Mipmapebenen erweitern, kann sie wie folgt visualisiert werden.

![Abbildung einer 1d-Textur mit Mipmapebenen](images/d3d10-resource-texture1d.png)

Stellen Sie sich dies als eine einzelne Textur vor, die aus drei Untertexturen besteht. Jede Untertextur wird als Unterressource gezählt, sodass diese 1D-Textur drei Unterressourcen enthält. Eine Untertextur (oder Unterressource) kann mithilfe der Detailebene (LOD) für eine einzelne Textur indiziert werden. Wenn Sie ein Array von Texturen verwenden, erfordert der Zugriff auf eine bestimmte Untertextur sowohl die LOD als auch die bestimmte Textur. Alternativ kombiniert die API diese beiden Informationen wie hier gezeigt in einem einzelnen nullbasierten Unterressourcenindex.

![Abbildung eines nullbasierten Unterressourcenindexes](images/d3d10-resource-texture1darray-sub-indexing.png)

### <a name="selecting-subresources"></a>Auswählen von Unterressourcen

Einige APIs greifen auf eine gesamte Ressource zu (z.B. [**CopyResource),**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copyresource)andere greifen auf einen Teil einer Ressource zu (z. B. [**UpdateSubresource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-updatesubresource) oder [**CopySubresourceRegion**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-copysubresourceregion)). Die API, die auf einen Teil einer Ressource zugreift, verwendet in der Regel eine Ansichtsbeschreibung (z.B. [**D3D10 \_ TEX2D \_ ARRAY \_ DSV),**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_tex2d_array_dsv)um die zuzugreifenden Unterressourcen anzugeben.

Diese Abbildungen veranschaulichen die Begriffe, die von einer Ansichtsbeschreibung beim Zugriff auf ein Array von Texturen verwendet werden.

### <a name="array-slice"></a>Arrayslice

Bei einem Array von Texturen enthält jede Textur mit Mipmaps ein Arrayslice (dargestellt durch das weiße Rechteck) eine Textur und alle zugehörigen Untertexturen, wie in der folgenden Abbildung dargestellt.

![Abbildung einer Array-Splice](images/d3d10-resource-array-slice.png)

### <a name="mip-slice"></a>Mip-Slice

Ein Mipslice (dargestellt durch das weiße Rechteck) enthält eine Mipmapebene für jede Textur in einem Array, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Mip-Splice](images/d3d10-resource-mip-slice.png)

### <a name="selecting-a-single-subresource"></a>Auswählen einer einzelnen Unterressource

Sie können diese beiden Slicetypen verwenden, um eine einzelne Unterressource auszuwählen, wie in der folgenden Abbildung dargestellt.

![Abbildung der Auswahl einer Unterressource mit einem Arrayslice und einer Mip-Splice](images/d3d10-resource-subresources-1.png)

### <a name="selecting-multiple-subresources"></a>Auswählen mehrerer Unterressourcen

Alternativ können Sie diese beiden Arten von Slices mit der Anzahl der Mipmapebenen und/oder der Anzahl von Texturen verwenden, um mehrere Unterressourcen auszuwählen.

![Abbildung der Auswahl mehrerer Unterressourcen](images/d3d10-resource-subresources-2.png)

Unabhängig davon, welchen Texturtyp Sie verwenden, mit oder ohne Mipmaps, mit oder ohne Texturarray, können Sie die Hilfsfunktion [**D3D10CalcSubresource**](/windows/desktop/api/D3D10/nf-d3d10-d3d10calcsubresource)verwenden, um den Index einer bestimmten Unterressource zu berechnen.

### <a name="strong-vs-weak-typing"></a>Starke und schwache Typisierung

Durch das Erstellen einer vollständig typisierten Ressource wird die Ressource auf das Format beschränkt, mit dem sie erstellt wurde. Dadurch kann die Laufzeit den Zugriff optimieren, insbesondere wenn die Ressource mit Flags erstellt wird, die angeben, dass sie nicht von der Anwendung [zugeordnet](d3d10-graphics-programming-guide-resources-mapping.md) werden kann. Ressourcen, die mit einem bestimmten Typ erstellt wurden, können nicht mithilfe des Ansichtsmechanismus neu interpretiert werden.

In einem Typ ohne Ressource ist der Datentyp unbekannt, wenn die Ressource zum ersten Mal erstellt wird. Die Anwendung muss aus den verfügbaren Typen ohne Formate auswählen (siehe [**DXGI \_ FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)). Sie müssen die Größe des zuzuordnenden Arbeitsspeichers angeben und angeben, ob die Runtime die Untertexturen in einer Mipmap generieren muss. Das genaue Datenformat (ob der Arbeitsspeicher als ganze Zahlen, Gleitkommawerte, ganze Zahlen ohne Vorzeichen usw. interpretiert wird) wird jedoch erst bestimmt, wenn die Ressource mit einer Ansicht an die Pipeline gebunden ist. Da das Texturformat flexibel bleibt, bis die Textur an die Pipeline gebunden ist, wird die Ressource als schwach typisierter Speicher bezeichnet. Schwach typisierter Speicher hat den Vorteil, dass er wiederverwendet oder neu interpretiert werden kann (in einem anderen Format), solange das Komponentenbit des neuen Formats der Bitanzahl des alten Formats entspricht.

Eine einzelne Ressource kann an mehrere Pipelinestufen gebunden werden, solange jede über eine eindeutige Ansicht verfügt, die die Formate an jedem Speicherort vollständig qualifiziert. Beispielsweise könnte eine Ressource, die mit dem Format DXGI \_ FORMAT \_ R32G32B32A32 TYPELESS erstellt \_ wurde, als DXGI \_ FORMAT \_ R32G32B32A32 \_ FLOAT und als DXGI FORMAT \_ \_ R32G32B32A32 \_ UINT an verschiedenen Stellen in der Pipeline gleichzeitig verwendet werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Ressourcen (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
