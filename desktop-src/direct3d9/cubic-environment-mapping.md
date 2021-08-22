---
description: Kubische Umgebungskarten , die manchmal auch als Cubemaps bezeichnet werden, sind Texturen, die Bilddaten enthalten, die die Szene um ein Objekt darstellen, als ob sich das Objekt in der Mitte eines Cubes befing.
ms.assetid: 4879d59b-e6d3-4811-ab2c-bcce8f214e1c
title: Kubische Umgebungszuordnung (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b02f86528c52c2e8e9376eb92e4452735c2613cc9b7dda08a8a07e8473193ea
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565338"
---
# <a name="cubic-environment-mapping-direct3d-9"></a>Kubische Umgebungszuordnung (Direct3D 9)

Kubische Umgebungskarten , die manchmal auch als Cubemaps bezeichnet werden, sind Texturen, die Bilddaten enthalten, die die Szene um ein Objekt darstellen, als ob sich das Objekt in der Mitte eines Cubes befing. Jedes Gesicht der kubischen Umgebungskarte deckt ein 90-Grad-Sichtfeld in der horizontalen und vertikalen Ansicht ab, und es gibt sechs Gesichter pro Cubemap. Die Ausrichtung der Gesichter wird in der folgenden Abbildung dargestellt.

![Abbildung eines Cubes mit zentralen Koordinatenachsen perpendordiniert zu Würfelgesichter](images/cubemap-cube.png)

Jedes Gesicht des Würfels ist auf die x/y-, y/z- oder x/z-Ebene im Weltraum ausgerichtet. Die folgende Abbildung zeigt, wie jede Ebene einem Gesicht entspricht.

![Abbildung von Würfelflächen mit Koordinatenprojektionen aus Ebenen](images/cube-faces.png)

Kubische Umgebungszuordnungen werden als eine Reihe von Texturobjekten implementiert. Anwendungen können statische Bilder für die kubische Umgebungszuordnung verwenden, oder sie können in den Gesichtern der Cubemap gerendert werden, um eine dynamische Umgebungszuordnung durchzuführen. Diese Technik erfordert, dass es sich bei den Cubezuordnungsoberflächen um gültige Renderzieloberflächen handelt, die mit dem D3DUSAGE \_ RENDERTARGET-Flag erstellt wurden.

Die Gesichter einer Cubemap müssen keine extrem detaillierten Renderings der umgebenden Szene enthalten. In den meisten Fällen werden Umgebungszuordnungen auf gekrümmte Oberflächen angewendet. Angesichts des Umfangs der Von den meisten Anwendungen verwendeten Krümmung macht die resultierende reflektierende Verzerrung extreme Details in der Umgebungszuordnung im Hinblick auf Arbeitsspeicher und Renderingaufwand überflüssig.

## <a name="mipmapped-cubic-environment-maps"></a>Mipmapped Kubische Umgebung Karten

Cubezuordnungen können mipmapped sein. Legen Sie zum Erstellen einer mipmapped-Cubezuordnung den Levels-Parameter der [**CreateCubeTexture-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) auf die gewünschte Anzahl von Ebenen fest. Sie können sich die Topografie dieser Oberflächen wie im folgenden Diagramm dargestellt vorstellen.

![Diagramm einer mipmapped Cube Map mit n MIP-Ebenen](images/cubemap-mipped.png)

Anwendungen, die mipmapped kubische Umgebungszuordnungen erstellen, können auf jedes Gesicht zugreifen, indem sie die [**GetCubeMapSurface-Methode**](/windows/desktop/api) aufrufen. Legen Sie zunächst den entsprechenden Wert des [**D3DCUBEMAP \_ FACES-Enumerationstyps**](./d3dcubemap-faces.md) fest, wie unter [Erstellen von kubischen Umgebungszuordnungsoberflächen (Direct3D 9)](creating-cubic-environment-map-surfaces.md)erläutert. Wählen Sie als Nächstes die abzurufende Ebene aus, indem Sie den **GetCubeMapSurface-Ebenenparameter** auf die gewünschte mipmap-Ebene festlegen. Denken Sie daran, dass 0 dem Bild der obersten Ebene entspricht.

## <a name="texture-coordinates-for-cubic-environment-maps"></a>Texturkoordinaten für kubische Karten

Texturkoordinaten, die eine kubische Umgebungskarte indizieren, sind keine einfachen u-, v-Stilkoordinaten, die verwendet werden, wenn Standardtexturen angewendet werden. Kubische Umgebungskarten verwenden tatsächlich überhaupt keine Texturkoordinaten. Anstelle eines Satzes von Texturkoordinaten benötigen kubische Umgebungskarten einen 3D-Vektor. Sie müssen darauf achten, ein ordnungsgemäßes Scheitelpunktformat anzugeben. Sie müssen dem System nicht nur mitteilen, wie viele Sätze von Texturkoordinaten Ihre Anwendung verwendet, sie müssen auch Informationen darüber bereitstellen, wie viele Elemente in jeder Menge enthalten sind. Direct3D bietet den [**D3DFVF \_ TEXCOORDSIZEN-Makrosatz**](d3dfvf-texcoordsizen.md) für diesen Zweck. Diese Makros akzeptieren einen einzelnen Parameter, der den Index des Texturkoordinatensatzes identifiziert, für den die Größe beschrieben wird. Im Fall eines 3D-Vektors schließen Sie das Bitmuster ein, das vom Makro D3DFVF \_ TEXCOORDSIZE3 erstellt wurde. Das folgende Codebeispiel zeigt, wie dieses Makro verwendet wird.


```
// Create a flexible vertex format descriptor for a vertex that contains
//   a position, normal, and one set of 3D texture coordinates.

DWORD dwFVF = D3DFVF_XYZ | D3DFVF_NORMAL | D3DFVF_TEX1 | D3DFVF_TEXCOORDSIZE3(0); 
```



In einigen Fällen, z. B. bei der Zuordnung von diffusem Licht, verwenden Sie die Vertexnorm des Kameraraums für den Vektor. In anderen Fällen, z. B. bei der Specular Environment Mapping, verwenden Sie einen Reflektionsvektor. Da transformierte Scheitelpunktnormen allgemein verstanden werden, konzentrieren sich die Informationen hier auf das Berechnen eines Reflektionsvektors.

Das Berechnen eines Reflektionsvektors allein erfordert ein Verständnis der Position jedes Scheitelpunkts und eines Vektors vom Standpunkt bis zu diesem Scheitelpunkt. Direct3D kann die Reflektionsvektoren für Ihre Geometrie automatisch berechnen. Die Verwendung dieses Features spart Arbeitsspeicher, da Sie keine Texturkoordinaten für die Umgebungskarte einschließen müssen. Außerdem wird die Bandbreite reduziert, und im Fall eines T&L-GERÄTs kann es erheblich schneller sein als die Berechnungen, die Ihre Anwendung selbst vornehmen kann. Um dieses Feature zu verwenden, legen Sie in der Texturstufe, die die kubische Umgebungszuordnung enthält, den Texturzustand D3DTSS \_ TEXCOORDINDEX auf eine Kombination aus dem D3DTSS \_ TCI \_ CAMERASPACEREFLECTIONVECTOR-Member von [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md) und dem Index eines Texturkoordinatensatzes fest. In einigen Situationen, z. B. bei der Diffuslichtzuordnung, können Sie den D3DTSS \_ TCI \_ CAMERASPACENORMAL-Member von **D3DTEXTURESTAGESTATETYPE** verwenden, wodurch das System den transformierten Kameraraum und den Scheitelpunkt normal als Adressierungsvektor für die Textur verwendet. Der Index wird nur vom System verwendet, um den Umbruchmodus für die Textur zu bestimmen.

Das folgende Codebeispiel zeigt, wie dieser Wert verwendet wird.


```
// The m_d3dDevice variable is a valid pointer
// to an IDirect3DDevice9 interface.

// Automatically generate texture coordinates for stage 2.
// This assumes that stage 2 is assigned a cube map.
// Use the wrap mode from the texture coordinate set at index 1.

m_d3dDevice->SetTextureStageState( 2, D3DTSS_TEXCOORDINDEX,
                                   D3DTSS_TCI_CAMERASPACEREFLECTIONVECTOR | 1); 
```



Wenn Sie die automatische Texturkoordinatengenerierung aktivieren, verwendet das System eine von zwei Formeln, um den Reflektionsvektor für jeden Scheitelpunkt zu berechnen. Wenn der D3DRS \_ LOCALVIEWER-Renderzustand auf **TRUE** festgelegt ist, wird die folgende Formel verwendet.

![Formel des Reflektionsvektors (r = 2(exn)n-e)](images/reflection-vector-local.png)

In der obigen Formel ist R der berechnete Reflektionsvektor, E der normalisierte Positions-zu-Auge-Vektor und N die Kameraraum-Vertexnorm.

Wenn der D3DRS \_ LOCALVIEWER-Renderzustand auf **FALSE** festgelegt ist, verwendet das System die folgende Formel.

![Formel des Reflektionsvektors (r = 2nzn-i)](images/reflection-vector-nonlocal.png)

Die R- und N-Elemente in dieser Formel sind mit der vorherigen Formel identisch. Das N<sub>Z-Element</sub> ist der Weltraum z der Scheitelpunktnorm, und ich ist der Vektor (0,0,1) eines unendlich entfernten Blickpunkts. Das System verwendet den Reflektionsvektor aus beiden Formeln, um das entsprechende Gesicht der Cubemap auszuwählen und zu adressierung.

> [!Note]  
> In den meisten Fällen sollten Anwendungen die automatische Normalisierung von Scheitelpunktnormalisierungen aktivieren. Legen Sie hierzu D3DRS \_ NORMALIZENORMALS auf **TRUE** fest. Wenn Sie diesen Renderzustand nicht aktivieren, unterscheidet sich die Darstellung der Umgebungszuordnung erheblich von der erwarteten Darstellung.

 

Weitere Informationen finden Sie im folgenden Thema.

-   [Erstellen kubischer Umgebungszuordnungsoberflächen (Direct3D 9)](creating-cubic-environment-map-surfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Umgebungszuordnung](environment-mapping.md)
</dt> </dl>

 

 
