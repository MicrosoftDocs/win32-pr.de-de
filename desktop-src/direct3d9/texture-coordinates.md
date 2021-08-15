---
description: Die meisten Texturen, wie Bitmaps, sind ein zweidimensionales Array von Farbwerten.
ms.assetid: vs|directx_sdk|~\texture_coordinates.htm
title: Texturkoordinaten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06ff2c2c86eebac77d910b5dc6c583df380f0bbb2ccb3dca2fc65b9e929e7abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519822"
---
# <a name="texture-coordinates-direct3d-9"></a>Texturkoordinaten (Direct3D 9)

Die meisten Texturen, wie Bitmaps, sind ein zweidimensionales Array von Farbwerten. Kubische Umgebungszuordnungstexturen sind eine Ausnahme. Weitere Informationen finden Sie unter [Kubische Umgebungszuordnung (Direct3D 9).](cubic-environment-mapping.md) Die einzelnen Farbwerte werden als Texturelement oder Texel bezeichnet. Jedes Texel verfügt über eine eindeutige Adresse in der Textur. Die Adresse kann als Spalte und Zeilennummer verwendet werden, die sie bzw. v in der folgenden Abbildung bezeichnet.

![Abbildung einer Texeladresse als Spalten- und Zeilennummern](images/uvcoordinates.jpg)

Texturkoordinaten befinden sich im Texturraum. Das heißt, sie sind relativ zur Position (0,0) in der Textur. Wenn eine Textur auf ein Primitiv im 3D-Raum angewendet wird, müssen seine Texeladressen Objektkoordinaten zugeordnet werden. Sie müssen dann in Bildschirmkoordinaten oder Pixelpositionen übersetzt werden.

## <a name="mapping-texels-to-screen-space"></a>Zuordnen von Texeln zum Bildschirmbereich

Direct3D ordnet Texel im Texturraum direkt Pixeln im Bildschirmbereich zu und überspringt den Zwischenschritt zur Steigerung der Effizienz. Dieser Zuordnungsprozess ist tatsächlich eine umgekehrte Zuordnung. Das heißt, für jedes Pixel im Bildschirmbereich wird die entsprechende Texelposition im Texturraum berechnet. Die Texturfarbe an oder um diesen Punkt wird entnommen. Der Samplingprozess wird als Texturfilterung bezeichnet. Weitere Informationen finden Sie unter [Texturfilterung (Direct3D 9).](texture-filtering.md)

Jedes Texel in einer Textur kann durch seine Texelkoordinate angegeben werden. Um Texel primitiven Typen zuordnen zu können, erfordert Direct3D jedoch einen einheitlichen Adressbereich für alle Texel in allen Texturen. Daher wird ein generisches Adressierungsschema verwendet, bei dem alle Texeladressen im Bereich von 0,0 bis einschließlich 1,0 liegen. Direct3D-Anwendungen geben Texturkoordinaten in Bezug auf Ihre,v-Werte an, ähnlich wie kartesische 2D-Koordinaten in Bezug auf x,y-Koordinaten angegeben werden. Technisch gesehen kann das System Texturkoordinaten außerhalb des Bereichs von 0,0 und 1,0 verarbeiten und verwendet dazu die Parameter, die Sie für die Textur adressierung festlegen. Weitere Informationen finden Sie unter [Textur-Adressierungsmodi (Direct3D 9).](texture-addressing-modes.md)

Dies hat zur Folge, dass identische Texturadressen verschiedenen Texelkoordinaten in verschiedenen Texturen zuordnen können. In der folgenden Abbildung ist die Texturadresse (0.5,1.0). Da es sich bei den Texturen jedoch um unterschiedliche Größen handelt, wird die Texturadresse verschiedenen Texeln zu. Textur 1 auf der linken Seite ist 5x5. Die Texturadresse (0.5,1.0) wird Texel (2,4) zu. Textur 2 auf der rechten Seite ist 7x7. Die Texturadresse (0.5,1.0) wird Texel (3,6) zu.

![Abbildung der Zuordnung derselben Texturadresse zu verschiedenen Texeln auf verschiedenen Texturen](images/texadr1.png)

Eine vereinfachte Version des Texelzuordnungsprozesses ist in der folgenden Abbildung dargestellt. Zugegebener weise ist dieses Beispiel sehr einfach. Ausführlichere Informationen finden Sie unter [Direktes Zuordnen von Texeln zu Pixeln (Direct3D 9).](directly-mapping-texels-to-pixels.md)

![Abbildung eines Pixels (ein Quadrat der Farbe), das dem Objektraum zugeordnet ist](images/texadr2.png)

In diesem Beispiel wird ein Pixel, das links von der Abbildung angezeigt wird, in ein Quadrat der Farbe idealisiert. Die Adressen der vier Ecken des Pixels werden dem 3D-Primitiv im Objektraum zugeordnet. Die Form des Pixels wird häufig aufgrund der Form des Primitivs im 3D-Raum und aufgrund des Anzeigewinkels verzerrt. Die Ecken des Oberflächenbereichs auf dem Primitiv, die den Ecken des Pixels entsprechen, werden dann dem Texturraum zugeordnet. Der Zuordnungsprozess verzerrt erneut die Form des Pixels, was üblich ist. Der endgültige Farbwert des Pixels wird aus den Texeln in dem Bereich berechnet, dem das Pixel zu ordnet. Sie bestimmen die Methode, die Direct3D verwendet, um die Pixelfarbe zu erhalten, wenn Sie die Texturfiltermethode festlegen. Weitere Informationen finden Sie unter [Texturfilterung (Direct3D 9).](texture-filtering.md)

Ihre Anwendung kann Texturkoordinaten direkt Vertices zuweisen. Mit dieser Funktion können Sie steuern, welcher Teil einer Textur einem Primitiv zugeordnet wird. Angenommen, Sie erstellen ein rechteckiges Primitiv, das genau die gleiche Größe wie die Textur in der folgenden Abbildung hat. In diesem Beispiel soll Ihre Anwendung die gesamte Textur der gesamten Wand zuordnen. Die Texturkoordinaten, die Ihre Anwendung den Scheitelungen des Primitiven zuträgt, sind (0,0,0,0), (1,0,0,0), (1,0,1,0) und (0,0,1,0).

![Abbildung einer texturierten Wand](images/texadr3.png)

Wenn Sie sich entschließen, die Höhe der Wand um eine Hälfte zu verringern, können Sie die Textur verzerren, damit sie an die kleinere Wand passt, oder Sie können Texturkoordinaten zuweisen, die dazu führen, dass Direct3D die untere Hälfte der Textur verwendet.

Wenn Sie die Textur verzerren oder skalieren möchten, um sie an die kleinere Wand zu passen, beeinflusst die von Ihnen verwendete Texturfiltermethode die Qualität des Bilds. Weitere Informationen finden Sie unter [Texturfilterung (Direct3D 9).](texture-filtering.md)

Wenn Sie stattdessen Texturkoordinaten zuweisen möchten, damit Direct3D die untere Hälfte der Textur für die kleinere Wand verwendet, sind die Texturkoordinaten, die Ihre Anwendung den Scheitelungen des Primitivs in diesem Beispiel zuträgt, (0,0,0,5), (1,0,0,5), (1,0,1,0) und (0,0,1,0). Direct3D wendet die untere Hälfte der Textur auf die Wand an.

Texturkoordinaten eines Scheitelpunkts können größer als 1,0 sein. Wenn Sie einem Scheitelpunkt Texturkoordinaten zuweisen, die nicht im Bereich von 0,0 bis einschließlich 1,0 liegen, sollten Sie auch den Textur adressierungsmodus festlegen. Weitere Informationen finden Sie unter [Textur-Adressierungsmodi (Direct3D 9).](texture-addressing-modes.md)

## <a name="texture-coordinates-and-texture-stages"></a>Texturkoordinaten und Texturstufen

Texturkoordinaten werden Texturen über Texturstufen zugeordnet. Texturen werden Texturstufen mit SetTexture(stageIndex, pTexture) zugewiesen. Siehe [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

Ein FVF-Code (Flexible Vertex Format) kann bis zu acht Sätze von Texturkoordinaten definieren. Die Texturkoordinatendaten werden vom Benutzer in den Scheitelpunktdaten erzeugt. Auf die Daten wird mit einem nullbasierten Index verwiesen: 0 - 7. Es gibt bis zu acht Texturmischungsphasen. Eine Textur wird mithilfe von SetTexture( stageIndex, pTexture) einer bestimmten Phase zugeordnet.

Sobald dies erfolgt ist, können beliebige Texturkoordinaten von jeder Phase verwendet werden. Jeder Satz von Koordinaten wird mithilfe von SetTextureStageState( stageIndex, D3DTSS \_ TEXCOORDINDEX, textureCoordinateIndex ) einer Phase zugeordnet. Siehe [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). Auf diese Weise können die Überblendungsphasen so eingerichtet werden, dass sie eine beliebige Textur und beliebige Texturkoordinaten verwenden. Mehrere Phasen können die gleichen Texturen oder Texturkoordinaten verwenden.

Weitere Informationen finden Sie in den folgenden Themen.

-   [Texturkoordinatenformate (Direct3D 9)](texture-coordinate-formats.md)
-   [Texturkoordinatenverarbeitung (Direct3D 9)](texture-coordinate-processing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
