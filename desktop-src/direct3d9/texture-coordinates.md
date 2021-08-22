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

Die meisten Texturen, wie Bitmaps, sind ein zweidimensionales Array von Farbwerten. Kubische Umgebungszuordnungstexturen sind eine Ausnahme. Weitere Informationen finden Sie unter [Kubische Umgebungszuordnung (Direct3D 9).](cubic-environment-mapping.md) Die einzelnen Farbwerte werden als Texturelement oder Texel bezeichnet. Jedes Texel verfügt über eine eindeutige Adresse in der Textur. Die Adresse kann als Spalte und Zeilennummer angesehen werden, die sie bzw. v in der folgenden Abbildung bezeichnen.

![Abbildung einer Texeladresse als Spalten- und Zeilennummern](images/uvcoordinates.jpg)

Texturkoordinaten befinden sich im Texturraum. Das heißt, sie sind relativ zur Position (0,0) in der Textur. Wenn eine Textur auf einen Primitiven im 3D-Raum angewendet wird, müssen dessen Texeladressen Objektkoordinaten zugeordnet werden. Sie müssen dann in Bildschirmkoordinaten oder Pixelpositionen übersetzt werden.

## <a name="mapping-texels-to-screen-space"></a>Zuordnen von Texels zum Bildschirmbereich

Direct3D ordnet Texel im Texturraum direkt Pixeln im Bildschirmbereich zu und überspringt den Zwischenschritt, um eine höhere Effizienz zu erzielen. Dieser Zuordnungsprozess ist eigentlich eine umgekehrte Zuordnung. Das heißt, für jedes Pixel im Bildschirmbereich wird die entsprechende Texelposition im Texturraum berechnet. Die Texturfarbe an oder um diesen Punkt wird entnommen. Der Samplingprozess wird als Texturfilterung bezeichnet. Weitere Informationen finden Sie unter [Texturfilterung (Direct3D 9).](texture-filtering.md)

Jedes Texel in einer Textur kann durch seine Texelkoordinate angegeben werden. Um Texel jedoch Primitiven zuzuordnen, erfordert Direct3D einen einheitlichen Adressbereich für alle Texel in allen Texturen. Daher wird ein generisches Adressierungsschema verwendet, bei dem sich alle Texeladressen im Bereich von 0,0 bis einschließlich 1,0 befinden. Direct3D-Anwendungen geben Texturkoordinaten in Bezug auf Ihre v-Werte an, ähnlich wie kartesische 2D-Koordinaten in Form von x,y-Koordinaten angegeben werden. Technisch gesehen kann das System Texturkoordinaten außerhalb des Bereichs von 0,0 und 1,0 verarbeiten und verwendet dazu die Parameter, die Sie für die Texturadressierung festlegen. Weitere Informationen finden Sie unter [Texturadressierungsmodi (Direct3D 9).](texture-addressing-modes.md)

Dies führt dazu, dass identische Texturadressen verschiedenen Texelkoordinaten in verschiedenen Texturen zugeordnet werden können. In der folgenden Abbildung lautet die Texturadresse (0,5,1,0). Da die Texturen jedoch unterschiedliche Größen aufweisen, wird die Texturadresse verschiedenen Texeln zugeordnet. Textur 1 auf der linken Seite ist 5x5. Die Texturadresse (0,5,1,0) ist Texel (2,4) zugeordnet. Textur 2 auf der rechten Seite ist 7x7. Die Texturadresse (0,5,1,0) wird Texel (3,6) zugeordnet.

![Abbildung der gleichen Texturadresszuordnung für verschiedene Texel auf verschiedenen Texturen](images/texadr1.png)

Eine vereinfachte Version des Texelzuordnungsprozesses ist in der folgenden Abbildung dargestellt. Dieses Beispiel ist sehr einfach. Ausführlichere Informationen finden Sie unter [Direktes Zuordnen von Texels zu Pixeln (Direct3D 9).](directly-mapping-texels-to-pixels.md)

![Abbildung des Pixels (ein Quadrat der Farbe), das dem Objektraum zugeordnet ist](images/texadr2.png)

In diesem Beispiel wird ein Pixel, das links neben der Abbildung angezeigt wird, in ein Quadrat der Farbe idealisiert. Die Adressen der vier Ecken des Pixels werden dem 3D-Primitiven im Objektraum zugeordnet. Die Form des Pixels wird häufig aufgrund der Form des Primitiven im 3D-Raum und aufgrund des Anzeigewinkels verzerrt. Die Ecken der Oberfläche auf dem Primitiven, die den Ecken des Pixels entsprechen, werden dann dem Texturraum zugeordnet. Der Zuordnungsprozess verzerrt wieder die Form des Pixels, was üblich ist. Der endgültige Farbwert des Pixels wird aus den Texel in der Region berechnet, der das Pixel zugeordnet ist. Sie bestimmen die Methode, die Direct3D verwendet, um die Pixelfarbe zu erreichen, wenn Sie die Texturfilterungsmethode festlegen. Weitere Informationen finden Sie unter [Texturfilterung (Direct3D 9).](texture-filtering.md)

Ihre Anwendung kann Texturkoordinaten direkt Vertices zuweisen. Mit dieser Funktion können Sie steuern, welcher Teil einer Textur einem Primitiven zugeordnet wird. Angenommen, Sie erstellen einen rechteckigen Primitiven, der genau die gleiche Größe wie die Textur in der folgenden Abbildung hat. In diesem Beispiel soll Ihre Anwendung die gesamte Textur der gesamten Wand zuordnen. Die Texturkoordinaten, die Ihre Anwendung den Scheitelpunkten des Primitiven zuweist, sind (0,0,0,0), (1,0,0,0), (1,0,1,0) und (0,0,1,0).

![Abbildung einer texturabbildten Wand](images/texadr3.png)

Wenn Sie sich dafür entscheiden, die Höhe der Wand um die Hälfte zu verringern, können Sie die Textur so verzerren, dass sie auf die kleinere Wand passt, oder Sie können Texturkoordinaten zuweisen, die direct3D dazu veranlassen, die untere Hälfte der Textur zu verwenden.

Wenn Sie die Textur verzerren oder skalieren möchten, um sie an die kleinere Wand anzupassen, wirkt sich die texturfilternde Methode, die Sie verwenden, auf die Qualität des Bilds aus. Weitere Informationen finden Sie unter [Texturfilterung (Direct3D 9).](texture-filtering.md)

Wenn Sie stattdessen Texturkoordinaten zuweisen, damit Direct3D die untere Hälfte der Textur für die kleinere Wand verwendet, sind die Texturkoordinaten, die Ihre Anwendung den Scheitelpunkten des Primitiven in diesem Beispiel zuweist, (0,0,0,5), (1,0,0,5), (1,0,1,0) und (0,0,1,0). Direct3D wendet die untere Hälfte der Textur auf die Wand an.

Texturkoordinaten eines Scheitelpunkts können größer als 1,0 sein. Wenn Sie einem Scheitelpunkt Texturkoordinaten zuweisen, die sich nicht im Bereich von 0,0 bis einschließlich 1,0 befinden, sollten Sie auch den Texturadressierungsmodus festlegen. Weitere Informationen finden Sie unter [Texturadressierungsmodi (Direct3D 9).](texture-addressing-modes.md)

## <a name="texture-coordinates-and-texture-stages"></a>Texturkoordinaten und Texturstufen

Texturkoordinaten werden Texturen über Texturstufen zugeordnet. Texturen werden Texturstufen mit SetTexture(stageIndex, pTexture) zugewiesen. Siehe [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

Ein FVF-Code (Flexible Vertex Format) kann bis zu acht Sätze von Texturkoordinaten definieren. Die Texturkoordinatendaten werden vom Benutzer in den Scheitelpunktdaten erfasst. Auf die Daten wird mit einem nullbasierten Index verwiesen: 0 bis 7. Es gibt bis zu acht Phasen der Texturmischung. Eine Textur wird mit setTexture( stageIndex, pTexture) einer bestimmten Phase zugeordnet.

Sobald dies erfolgt ist, können alle Texturkoordinaten von jeder Phase verwendet werden. Jeder Koordinatensatz wird einer Phase zugeordnet, die SetTextureStageState( stageIndex, D3DTSS \_ TEXCOORDINDEX, textureCoordinateIndex ) verwendet. Siehe [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). Auf diese Weise können die Mischungsstufen so eingerichtet werden, dass sie eine beliebige Textur und texturkoordinaten verwenden. Mehrere Phasen können die gleichen Texturen oder Texturkoordinaten verwenden.

Weitere Informationen finden Sie in den folgenden Themen.

-   [Texturkoordinatenformate (Direct3D 9)](texture-coordinate-formats.md)
-   [Texturkoordinatenverarbeitung (Direct3D 9)](texture-coordinate-processing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
