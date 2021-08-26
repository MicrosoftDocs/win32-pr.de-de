---
title: Einführung in Texturen in Direct3D 11
description: Eine Texturressource ist eine strukturierte Sammlung von Daten zum Speichern von Texeln.
ms.assetid: d745093e-2d51-4d45-a88a-caa0ca58b2ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea3bfd19f018ff3f3d9fc8eb1608212a93b4364de2cc24b6213763dfcda4ffe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120027900"
---
# <a name="introduction-to-textures-in-direct3d-11"></a>Einführung in Texturen in Direct3D 11

Eine Texturressource ist eine strukturierte Sammlung von Daten zum Speichern von Texeln. Ein Texel stellt die kleinste Einheit einer Textur dar, die von der Pipeline gelesen oder geschrieben werden kann. Im Gegensatz zu Puffern können Texturen nach Textur-Samplern gefiltert werden, während sie von Shadereinheiten gelesen werden. Der Texturtyp wirkt sich auf die Filterung der Textur aus. Jedes Texel enthält 1 bis 4 Komponenten, die in einem der DXGI-Formate angeordnet sind, die durch die DXGI \_ FORMAT-Enumeration definiert sind.

Texturen werden als strukturierte Ressource mit einer bekannten Größe erstellt. Allerdings kann jede Textur typiert oder typlos sein, wenn die Ressource erstellt wird, solange der Typ vollständig mithilfe einer Ansicht angegeben wird, wenn die Textur an die Pipeline gebunden ist.

## <a name="texture-types"></a>Texturtypen

Es gibt mehrere Arten von Texturen: 1D, 2D, 3D, von denen jede mit oder ohne Mipmaps erstellt werden kann. Direct3D 11 unterstützt auch Texturarrays und Texturen mit mehrerenAmpeln.

-   [1D-Texturen](#1d-textures)
-   [1D-Texturarrays](#1d-texture-arrays)
-   [2D-Texturen und 2D-Texturarrays](#2d-textures-and-2d-texture-arrays)
-   [3D-Texturen](#3d-textures)

### <a name="1d-textures"></a>1D-Texturen

Eine 1D-Textur in ihrer einfachsten Form enthält Texturdaten, die mit einer einzelnen Texturkoordinate adressiert werden können. sie kann wie in der folgenden Abbildung dargestellt als Array von Texeln visualisiert werden. 1D-Texturen werden durch die [**ID3D11Texture1D-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) dargestellt.

![Abbildung einer 1d-Textur](images/d3d10-1d-texture.png)

Jedes Texel enthält abhängig vom Format der gespeicherten Daten eine Reihe von Farbkomponenten. Wenn Sie die Komplexität erhöhen, können Sie eine 1D-Textur mit Mipmap-Ebenen erstellen, wie in der folgenden Abbildung dargestellt.

![Abbildung einer 1d-Textur mit Mipmap-Ebenen](images/d3d10-resource-texture1d.png)

Eine Mipmapebene ist eine Textur, die eine Zweierleistung kleiner ist als die Darüberebene. Die oberste Ebene enthält die meisten Details, jede nachfolgende Ebene ist kleiner. Für eine 1D-Mipmap enthält die kleinste Ebene einen Texel. Darüber hinaus werden MIP-Ebenen immer auf 1:1 reduziert. Wenn Mipmaps für eine Textur mit ungerader Größe generiert werden, ist die nächste niedrigere Ebene immer eine gleichmäßige Größe (außer wenn die niedrigste Ebene 1 erreicht). Das Diagramm veranschaulicht beispielsweise eine 5x1-Textur, deren nächste niedrigste Ebene eine 2x1-Textur ist, deren nächste (und letzte) Mipebene eine Textur der Größe 1x1 ist. Die Ebenen werden durch einen Index identifiziert, der als LOD (Level-of-Detail) bezeichnet wird, der für den Zugriff auf die kleinere Textur verwendet wird, wenn Geometrie gerendert wird, die sich nicht so nah an der Kamera befindet.

### <a name="1d-texture-arrays"></a>1D-Texturarrays

Direct3D 11 unterstützt auch Arrays von Texturen. Ein 1D-Texturarray wird auch durch die [**ID3D11Texture1D-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture1d) dargestellt. Ein Array von 1D-Texturen sieht konzeptionell wie die folgende Abbildung aus.

![Abbildung eines Arrays von 1d-Texturen](images/d3d10-resource-texture1darray.png)

Dieses Texturarray enthält drei Texturen. Jede der drei Texturen hat eine Texturbreite von 5 (dies ist die Anzahl der Elemente in der ersten Ebene). Jede Textur enthält auch eine Mipmap mit drei Ebenen.

Alle Texturarrays in Direct3D sind ein homogenes Array von Texturen. Dies bedeutet, dass jede Textur in einem Texturarray das gleiche Datenformat und dieselbe Größe aufweisen muss (einschließlich Texturbreite und Anzahl von Mipmapebenen). Sie können Texturarrays unterschiedlicher Größe erstellen, solange alle Texturen in jedem Array übereinstimmen.

### <a name="2d-textures-and-2d-texture-arrays"></a>2D-Texturen und 2D-Texturarrays

Eine Texture2D-Ressource enthält ein 2D-Raster mit Texeln. Jedes Texel kann durch einen u,v-Vektor adressiert werden. Da es sich um eine Texturressource handelt, kann sie Mipmapebenen und Unterressourcen enthalten. 2D-Texturen werden durch die [**ID3D11Texture2D-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) dargestellt. Eine vollständig aufgefüllte 2D-Texturressource sieht wie in der folgenden Abbildung aus.

![Abbildung einer 2d-Texturressource](images/d3d10-resource-texture2d.png)

Diese Texturressource enthält eine einzelne 3x5-Textur mit drei Mipmapebenen.

Eine 2D-Texturarrayressource ist ein homogenes Array von 2D-Texturen. Das heißt, jede Textur hat das gleiche Datenformat und die gleichen Dimensionen (einschließlich Mipmapebenen). Ein 2D-Texturarray wird auch durch die [**ID3D11Texture2D-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture2d) dargestellt. Es hat ein ähnliches Layout wie das 1D-Texturarray, außer dass die Texturen jetzt 2D-Daten enthalten, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Arrays von 2d-Texturen](images/d3d10-resource-texture2darray.png)

Dieses Texturarray enthält drei Texturen: Jede Textur ist 3x5 mit zwei Mipmap-Ebenen.

### <a name="using-a-2d-texture-array-as-a-texture-cube"></a>Verwenden eines 2D-Texturarrays als Texturcube

Ein Texturcube ist ein 2D-Texturarray, das 6 Texturen enthält, eine für jedes Gesicht des Würfels. Ein vollständig aufgefüllter Texturcube sieht wie in der folgenden Abbildung aus.

![Abbildung eines Arrays von 2d-Texturen, die einen Texturcube darstellen](images/d3d10-resource-texturecube.png)

Ein 2D-Texturarray, das 6 Texturen enthält, kann mit den systeminternen Funktionen der Cube map aus Shadern gelesen werden, nachdem sie mit einer Cubetexturansicht an die Pipeline gebunden wurden. Texturcubes werden vom Shader mit einem 3D-Vektor adressiert, der von der Mitte des Texturcubes aus aufzeigt.

> [!Note]  
> Geräte, die Sie mit [**10 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) Featureebene und höher erstellen, können Arrays von Texturcubes unterstützen, bei denen die Anzahl der Texturen der Anzahl von Texturcubes in einem Array mal sechs entspricht. Geräte, die Sie mit [**10 \_ 0 Featureebene erstellen,**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) unterstützen nur einen einzelnen Texturcube mit sechs Gesichtern. Außerdem unterstützt Direct3D 11 keine partiellen Cubemaps.

 

### <a name="3d-textures"></a>3D-Texturen

Eine 3D-Texturressource (auch als Volumentextur bezeichnet) enthält ein 3D-Volume von Texeln. Da es sich um eine Texturressource handelt, kann sie Mipmapebenen enthalten. 3D-Texturen werden durch die [**ID3D11Texture3D-Schnittstelle**](/windows/desktop/api/D3D11/nn-d3d11-id3d11texture3d) dargestellt. Eine vollständig aufgefüllte 3D-Textur sieht wie in der folgenden Abbildung aus.

![Abbildung einer 3D-Texturressource](images/d3d10-resource-texture3d.png)

Wenn ein 3D-Textur-Mipmap-Slice als Renderzielausgabe (mit einer Renderzielansicht) gebunden ist, verhält sich die 3D-Textur identisch mit einem 2D-Texturarray mit n Slices. Der bestimmte Renderslice wird aus der Geometry-Shader-Phase ausgewählt, indem eine Skalarkomponente von Ausgabedaten als SV \_ RenderTargetArrayIndex-Systemwert deklariert wird.

Es gibt kein Konzept eines 3D-Texturarrays. Daher ist eine 3D-Texturunterressource eine einzelne Mipmapebene.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturen](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




