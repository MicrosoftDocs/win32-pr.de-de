---
title: Einführung in Texturen in Direct3D 11
description: Eine Textur Ressource ist eine strukturierte Sammlung von Daten, die zum Speichern von texeln entwickelt wurden.
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71fcafdfb9caf53a27e60956c8182ae3ef95008e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856423"
---
# <a name="introduction-to-textures-in-direct3d-11"></a>Einführung in Texturen in Direct3D 11

Eine Textur Ressource ist eine strukturierte Sammlung von Daten, die zum Speichern von texeln entwickelt wurden. Ein Texel stellt die kleinste Einheit einer Textur dar, die von der Pipeline gelesen oder geschrieben werden kann. Im Gegensatz zu puffern können Texturen durch Textur-samplz gefiltert werden, wenn Sie von Shader-Einheiten gelesen werden. Der Typ der Textur wirkt sich darauf aus, wie die Textur gefiltert wird. Jede texumeration enthält 1 bis 4 Komponenten, die in einem der DXGI-Formate angeordnet sind, die durch die Enumeration des DXGI-Formats definiert werden \_ .

Texturen werden als strukturierte Ressource mit einer bekannten Größe erstellt. Allerdings kann jede Textur typisiert oder typlos sein, wenn die Ressource erstellt wird, solange der Typ vollständig mit einer Sicht angegeben wird, wenn die Textur an die Pipeline gebunden ist.

## <a name="texture-types"></a>Textur Typen

Es gibt mehrere Arten von Texturen: 1D, 2D, 3D, von denen jede mit oder ohne Mipmaps erstellt werden kann. Direct3D 11 unterstützt auch Textur Arrays und Multisampling-Texturen.

-   [1D-Texturen](#1d-textures)
-   [1D-Textur Arrays](#1d-texture-arrays)
-   [2D-Texturen und 2D-Textur Arrays](#2d-textures-and-2d-texture-arrays)
-   [3D-Texturen](#3d-textures)

### <a name="1d-textures"></a>1D-Texturen

Eine 1D-Textur in der einfachsten Form enthält Textur Daten, die mit einer einzelnen Textur Koordinate adressiert werden können. Sie kann als Array von Texels visualisiert werden, wie in der folgenden Abbildung dargestellt. 1D-Texturen werden von der [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) -Schnittstelle dargestellt.

![Abbildung einer 1D-Textur](images/d3d10-1d-texture.png)

Jede Texel enthält eine Reihe von Farbkomponenten, abhängig vom Format der gespeicherten Daten. Wenn Sie weitere Komplexität hinzufügen, können Sie eine 1D-Textur mit MipMap-Ebenen erstellen, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 1D-Textur mit MipMap-Ebenen](images/d3d10-resource-texture1d.png)

Bei einer MipMap-Ebene handelt es sich um eine Textur, bei der es sich um eine Potenz von zwei kleiner als der darüber liegenden Ebene handelt. Die oberste Ebene enthält die meisten Details, jede nachfolgende Ebene ist kleiner. Bei einer 1D-MipMap enthält die kleinste Ebene eine texsebene. Darüber hinaus reduzieren MIP-Ebenen immer auf 1:1. Wenn Mipmaps für eine ganzzahlige Textur generiert werden, ist die nächste untere Ebene immer gerade Größe (es sei denn, die niedrigste Ebene erreicht 1). Das Diagramm veranschaulicht z. b. eine 5x1-Textur, deren nächst niedrigste Ebene eine 2x1-Textur ist, deren nächste (und letzte) MIP-Ebene eine Textur mit einer Größenanpassung von 1 x 1 ist. Die Ebenen werden durch einen Index identifiziert, der als LOD (Detailstufe) bezeichnet wird und für den Zugriff auf die kleinere Textur verwendet wird, wenn Geometrie gerendert wird, die nicht so nah an der Kamera ist.

### <a name="1d-texture-arrays"></a>1D-Textur Arrays

Direct3D 11 unterstützt auch Arrays von Texturen. Ein 1D-Textur Array wird auch von der [**ID3D11Texture1D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) -Schnittstelle dargestellt. Ein Array von 1D-Texturen sieht konzeptionell wie in der folgenden Abbildung aus.

![Abbildung eines Arrays von 1D-Texturen](images/d3d10-resource-texture1darray.png)

Dieses Textur Array enthält drei Texturen. Jede der drei Texturen hat eine Textur Breite von 5 (die Anzahl der Elemente in der ersten Ebene). Jede Textur enthält auch eine 3-Ebenen-MipMap.

Alle Textur Arrays in Direct3D sind ein homogenes Array von Texturen. Dies bedeutet, dass jede Textur in einem Textur Array das gleiche Datenformat und die gleiche Größe aufweisen muss (einschließlich der Textur Breite und der Anzahl von MipMap-Ebenen). Sie können Textur Arrays mit unterschiedlichen Größen erstellen, sofern alle Texturen in den einzelnen Arrays in der Größe zueinander passen.

### <a name="2d-textures-and-2d-texture-arrays"></a>2D-Texturen und 2D-Textur Arrays

Eine Texture2D-Ressource enthält ein 2D-Raster mit texeln. Jedes texttuton ist durch einen u-v-Vektor adressierbar. Da es sich um eine Textur Ressource handelt, kann Sie MipMap-Ebenen und unter Ressourcen enthalten. 2D-Texturen werden von der [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) -Schnittstelle dargestellt. Eine vollständig aufgefüllte 2D-Textur Ressource sieht wie in der folgenden Abbildung aus.

![Abbildung einer 2D-Textur Ressource](images/d3d10-resource-texture2d.png)

Diese Textur Ressource enthält eine einzelne 3x5-Textur mit drei MipMap-Ebenen.

Eine 2D-Textur Array Ressource ist ein homogenes Array von 2D-Texturen. Das heißt, jede Textur hat das gleiche Datenformat und die gleichen Dimensionen (einschließlich MipMap-Ebenen). Ein 2D-Textur Array wird auch von der [**ID3D11Texture2D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) -Schnittstelle dargestellt. Es verfügt über ein ähnliches Layout wie das 1D-Textur Array, mit dem Unterschied, dass die Texturen nun 2D-Daten enthalten, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Arrays von 2D-Texturen](images/d3d10-resource-texture2darray.png)

Dieses Textur Array enthält drei Texturen. Jede Textur ist 3x5 mit zwei MipMap-Ebenen.

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a>Verwenden eines 2D-Textur Arrays als Textur Cube

Ein Textur Cube ist ein 2D-Textur Array, das 6 Texturen enthält, eine für jedes Gesicht des Cubes. Ein vollständig aufgefüllter Textur Cube sieht wie die folgende Abbildung aus.

![Abbildung eines Arrays von 2D-Texturen, die einen Textur Cube darstellen](images/d3d10-resource-texturecube.png)

Ein 2D-Textur Array, das 6 Texturen enthält, kann aus Shader mit den intrinsischen cubemap-Funktionen gelesen werden, nachdem Sie mit einer cubetextansicht an die Pipeline gebunden wurden. Textur Cubes werden vom Shader mit einem 3D-Vektor adressiert, der aus der Mitte des Textur Cubes zeigt.

> [!Note]  
> Geräte, die Sie mit [**\_ einer Funktionsebene von 10 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) und höher erstellen, können Arrays von Textur Cubes unterstützen, bei denen die Anzahl der Texturen gleich der Anzahl der Textur Cubes in einem Array mit der Zeit sechs ist. Geräte, die mit einer [**\_ Funktionsebene von 10 0**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) erstellt werden, unterstützen nur einen einzigen Textur Cube mit sechs Gesichtern. Außerdem unterstützt Direct3D 11 keine partiellen Cubemaps.

 

### <a name="3d-textures"></a>3D-Texturen

Eine 3D-Textur Ressource (auch als volumetextur bezeichnet) enthält eine 3D-Menge an texeln. Da es sich um eine Textur Ressource handelt, kann Sie MipMap-Ebenen enthalten. 3D-Texturen werden von der [**ID3D11Texture3D**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) -Schnittstelle dargestellt. Eine vollständig aufgefüllte 3D-Textur sieht wie in der folgenden Abbildung aus.

![Abbildung einer 3D--Textur Ressource](images/d3d10-resource-texture3d.png)

Wenn ein 3D-Textur-MipMap-Slice als renderzielausgabe (mit einer renderzielansicht) gebunden wird, verhält sich die 3D-Textur identisch mit einem 2D-Textur Array mit n Slices. Der jeweilige renderslice wird aus der Geometrie-Shader-Stufe ausgewählt, indem eine skalare Komponente der Ausgabedaten als der "SV \_ rendertargetarrayindex"-System Wert deklariert wird.

Es gibt kein Konzept eines 3D-Textur Arrays. Daher ist eine 3D-Textur-unter Quelle eine einzelne MipMap-Ebene.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturen](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




