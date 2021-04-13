---
description: Die meisten Texturen, wie z. b. Bitmaps, sind ein zweidimensionales Array von Farbwerten.
ms.assetid: vs|directx_sdk|~\texture_coordinates.htm
title: Texturkoordinaten (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dcf4c886c187aaa2218508a180e23644a544739
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482691"
---
# <a name="texture-coordinates-direct3d-9"></a>Texturkoordinaten (Direct3D 9)

Die meisten Texturen, wie z. b. Bitmaps, sind ein zweidimensionales Array von Farbwerten. Die Struktur der kubischen Umgebungs Zuordnung ist eine Ausnahme. Weitere Informationen finden Sie unter [Zuordnung von kubischen Umgebungen (Direct3D 9)](cubic-environment-mapping.md). Die einzelnen Farbwerte werden als Textur Element oder Texel bezeichnet. Jeder textext hat eine eindeutige Adresse in der Textur. Die Adresse kann als Spalten-und Zeilennummer betrachtet werden, die in der folgenden Abbildung jeweils als bzw. v bezeichnet werden.

![Abbildung einer textsadresse als Spalten-und Zeilennummern](images/uvcoordinates.jpg)

Texturkoordinaten befinden sich im Textur Bereich. Das heißt, Sie sind relativ zum Speicherort (0,0) in der Textur. Wenn eine Textur auf ein primitiv im 3D-Raum angewendet wird, müssen die zugehörigen Texel-Adressen in Objekt Koordinaten zugeordnet werden. Sie müssen dann in Bildschirm Koordinaten oder Pixelpositionen übersetzt werden.

## <a name="mapping-texels-to-screen-space"></a>Zuordnung von texeln zum Bildschirmbereich

Direct3D ordnet texeln im Textur Bereich direkt Pixel im Bildschirmbereich zu und überspringt den Zwischenschritt, um eine höhere Effizienz zu erzielen. Dieser Mapping-Prozess ist tatsächlich eine umgekehrte Zuordnung. Das heißt, für jedes Pixel im Bildschirmbereich wird die zugehörige texturposition im Textur Bereich berechnet. Die Textur Farbe an oder um diesen Punkt wird abgetastet. Der Samplings-Prozess wird als Textur Filterung bezeichnet. Weitere Informationen finden Sie unter [Textur Filterung (Direct3D 9)](texture-filtering.md).

Jede textexin einer Textur kann durch die Texturkoordinate angegeben werden. Um texeln jedoch primitiven zuzuordnen, erfordert Direct3D einen einheitlichen Adressbereich für alle texeln in allen Texturen. Daher wird ein generisches Adressierungs Schema verwendet, bei dem alle texusadressen im Bereich von 0,0 bis 1,0 (einschließlich) liegen. Direct3D-Anwendungen geben Texturkoordinaten in Bezug auf Sie, v-Werte, ähnlich wie 2D-kartesische Koordinaten in Form von x-, y-Koordinaten an. Technisch gesehen kann das System die Texturkoordinaten tatsächlich außerhalb des Bereichs von 0,0 und 1,0 verarbeiten. Dies geschieht mit den Parametern, die Sie für die Textur Adressierung festgelegt haben. Weitere Informationen finden Sie unter [Textur Adressierungs Modi (Direct3D 9)](texture-addressing-modes.md).

Dies hat zur Folge, dass identische Textur Adressen verschiedenen texsekoordinaten in unterschiedlichen Texturen zugeordnet werden können. In der folgenden Abbildung ist die Textur Adresse (0,5, 1.0). Da die Texturen jedoch unterschiedlich groß sind, wird die Textur Adresse anderen texeln zugeordnet. Textur 1, auf der linken Seite, ist 5x5. Die Textur Adresse (0,5, 1.0) ist Texel (2, 4) zugeordnet. Textur 2 auf der rechten Seite ist 7x7. Die Textur Adresse (0,5, 1.0) ist Texel (3, 6) zugeordnet.

![Abbildung der gleichen Textur Adress Zuordnung zu verschiedenen texeln in unterschiedlichen Texturen](images/texadr1.png)

In der folgenden Abbildung ist eine vereinfachte Version des textmapping-Prozesses dargestellt. Zugegeben, dieses Beispiel ist sehr einfach. Ausführlichere Informationen finden Sie unter [direkte Zuordnung von Texels zu Pixeln (Direct3D 9)](directly-mapping-texels-to-pixels.md).

![Abbildung des Pixels (ein quadratisches Zeichen), das dem Objekt Raum zugeordnet ist](images/texadr2.png)

In diesem Beispiel wird ein Pixel, das auf der linken Seite der Abbildung angezeigt wird, in ein quadratisches Quadrat von Farben eingemutet. Die Adressen der vier Ecken des Pixels werden dem 3D-primitiv im Objektbereich zugeordnet. Die Form des Pixels wird häufig aufgrund der Form des primitiven in 3D-Raum und aufgrund des Anzeige Winkels verzerrt. Die Ecken der Oberfläche auf dem primitiven, die den Ecken des Pixels entsprechen, werden dann in den Textur Bereich zugeordnet. Der Mapping-Prozess verzerrt die Form des Pixels, was üblich ist. Der endgültige Farbwert des Pixels wird aus den texeln in dem Bereich berechnet, dem das Pixel zugeordnet ist. Sie bestimmen die Methode, die von Direct3D verwendet wird, um beim Festlegen der Textur Filtermethode die Pixelfarbe zu erreichen. Weitere Informationen finden Sie unter [Textur Filterung (Direct3D 9)](texture-filtering.md).

Die Anwendung kann den Scheitel Punkten Texturkoordinaten direkt zuweisen. Mit dieser Funktion können Sie steuern, welcher Teil einer Textur einem primitiven zugeordnet wird. Nehmen Sie beispielsweise an, Sie erstellen ein rechteckiges primitiv, das exakt der gleichen Größe entspricht wie die Textur in der folgenden Abbildung. In diesem Beispiel möchten Sie, dass Ihre Anwendung die gesamte Textur der ganzen Wand zuordnet. Die Texturkoordinaten, die Ihre Anwendung den Scheitel Punkten des primitiven zuweist, sind (0,0, 0,0), (1.0, 0,0), (1.0, 1.0) und (0,0, 1.0).

![Abbildung einer Textur zugeordneten Wand](images/texadr3.png)

Wenn Sie die Höhe der Wand um eine Hälfte verringern möchten, können Sie die Textur so verzerren, dass Sie auf die kleinere Wand passt, oder Sie können Texturkoordinaten zuweisen, die bewirken, dass Direct3D die untere Hälfte der Textur verwendet.

Wenn Sie sich dazu entschließen, die Textur so zu verzerren, dass Sie an die kleinere Wand angepasst wird, wird die Qualität des Bilds von der verwendeten Textur Filterungs Methode beeinflusst. Weitere Informationen finden Sie unter [Textur Filterung (Direct3D 9)](texture-filtering.md).

Wenn Sie stattdessen Texturkoordinaten zuweisen möchten, damit Direct3D die untere Hälfte der Textur für die kleinere Wand verwenden, werden die Texturkoordinaten Ihrer Anwendung den Scheitel Punkten des primitiven in diesem Beispiel zugewiesen (0,0, 0,5), (1.0, 0,5), (1.0, 1.0) und (0,0, 1.0). Direct3D wendet die untere Hälfte der Textur auf die Wand an.

Es ist möglich, dass die Texturkoordinaten eines Scheitel Punkts größer als 1,0 ist. Wenn Sie einem Scheitelpunkt Texturkoordinaten zuweisen, die sich nicht im Bereich von 0,0 bis 1,0 befinden, sollten Sie auch den Textur Adressierungs Modus festlegen. Weitere Informationen finden Sie unter [Textur Adressierungs Modi (Direct3D 9)](texture-addressing-modes.md).

## <a name="texture-coordinates-and-texture-stages"></a>Texturkoordinaten und Textur Stufen

Texturkoordinaten werden mithilfe von Textur Phasen mit Texturen verknüpft. Texturen werden Textur Stufen mit SetTexture (stageingedex, ptexture) zugewiesen. Siehe [**IDirect3DDevice9:: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture).

Ein FVF-Code (Flexible Vertex-Format) kann bis zu acht Sätze von Texturkoordinaten definieren. Die Texturkoordinaten Daten werden vom Benutzer in den Scheitelpunkt Daten bereitgestellt. Auf die Daten wird mit einem NULL basierten Index verwiesen: 0-7. Es sind bis zu acht Textur Mischungs Phasen vorhanden. Eine Textur ist einer bestimmten Stufe mithilfe von SetTexture (stagumdex, ptexture) zugeordnet.

Sobald dies erfolgt ist, kann jeder beliebige Satz von Texturkoordinaten von jeder Phase verwendet werden. Jeder Satz von Koordinaten wird mithilfe von settexturestagestate (stageindex, D3DTSS \_ texcoordindex, TextureCoordinateIndex) einer Stufe zugeordnet. Weitere Informationen finden Sie unter [**IDirect3DDevice9:: settexturestagestate**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate). Auf diese Weise können die Mischungs Stufen so eingerichtet werden, dass jede Textur und beliebige Texturkoordinaten verwendet werden. In mehr als einer Phase können dieselben Texturen oder Texturkoordinaten verwendet werden.

Weitere Informationen finden Sie in den folgenden Themen.

-   [Texturkoordinaten Formate (Direct3D 9)](texture-coordinate-formats.md)
-   [Verarbeitung von Texturkoordinaten (Direct3D 9)](texture-coordinate-processing.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct3D-Texturen](direct3d-textures.md)
</dt> </dl>

 

 
