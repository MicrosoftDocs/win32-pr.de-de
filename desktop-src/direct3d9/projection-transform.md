---
description: Sie können sich die Projektions Transformation als Steuerung der Interna der Kamera vorstellen. Es ist analog zur Auswahl eines Lens für die Kamera.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Projektions Transformation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b518583dd534bec9784590150233847274ca71
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213927"
---
# <a name="projection-transform-direct3d-9"></a>Projektions Transformation (Direct3D 9)

Sie können sich die Projektions Transformation als Steuerung der Interna der Kamera vorstellen. Es ist analog zur Auswahl eines Lens für die Kamera. Dies ist die komplizierteste der drei Transformations Typen. Diese Erörterung der Projektions Transformation ist in die folgenden Themen gegliedert.

Die Projektions Matrix ist in der Regel eine Skalierungs-und Perspektiven Projektion. Die Projektions Transformation konvertiert die Anzeige Frustration in eine Cuboid-Form. Da das Near-Ende der Anzeige von Frustum kleiner als das Ende ist, wirkt sich dies auf das Erweitern von Objekten aus, die sich in der Nähe der Kamera befinden. auf diese Weise wird die Perspektive auf die Szene angewendet.

Beim [Anzeigen von "Frustum](viewports-and-clipping.md)" wird der Abstand zwischen der Kamera und dem Ursprung des Anzeige Transformations Bereichs willkürlich als D definiert, sodass die Projektions Matrix wie in der folgenden Abbildung aussieht.

![Abbildung der Projektions Matrix](images/projmat1.png)

Die Anzeige Matrix übersetzt die Kamera in den Ursprung, indem Sie in die z-Richtung nach-D übersetzt. Die Übersetzungs Matrix ähnelt der folgenden Abbildung.

![Darstellung der Übersetzungs Matrix](images/projmat2.png)

Das Multiplizieren der Übersetzungs Matrix durch die Projektions Matrix (T \* P) liefert die zusammengesetzte Projektions Matrix, wie in der folgenden Abbildung dargestellt.

![Abbildung der zusammengesetzten Projektions Matrix](images/projmat3.png)

Die Transformation für Perspektiven konvertiert ein Anzeige-Frustum in einen neuen Koordinaten Bereich. Beachten Sie, dass die Frustration zu Cuboid wird und dass der Ursprung von der oberen rechten Ecke der Szene in den Mittelpunkt wechselt, wie im folgenden Diagramm dargestellt.

![Diagramm der Art und Weise, in der die perspektivische Transformation die Anzeige Frustration in einen neuen Koordinaten Bereich ändert](images/cuboid.png)

In der Transformation für Perspektiven sind die Begrenzungen der x-und y-Richtungen-1 und 1. Die Grenzwerte für die z-Richtung sind 0 für die Vorderseite und 1 für die Backplane.

Diese Matrix übersetzt und skaliert Objekte auf der Grundlage einer angegebenen Entfernung von der Kamera auf die Near Clipping-Ebene, berücksichtigt jedoch nicht das Sichtfeld (Field of View, FOV), und die z-Werte, die für Objekte in der Entfernung erzeugt werden, können nahezu identisch sein, sodass Tiefe Vergleiche schwierig werden. Die folgende Matrix behandelt diese Probleme und passt die Scheitel Punkte an, um das Seitenverhältnis des Viewports zu berücksichtigen, sodass es eine gute Wahl für die perspektivische Projektion ist.

![Abbildung einer Matrix für die perspektivische Projektion](images/prjmatx1.png)

In dieser Matrix ist "Zn" der z-Wert der Near Clipping-Ebene. Die Variablen "w", "h" und "Q" haben folgende Bedeutungen. Beachten Sie, dass FOV<sub>w</sub> und fovk die horizontalen und vertikalen Ansichts Felder des Viewports im Bogenmaße darstellen.

![Gleichungen der Variablen Bedeutungen](images/prjmatx2.png)

Für Ihre Anwendung ist die Verwendung von Feld-of-View-Winkeln zum Definieren der Koeffizienten für die x-und y-Skalierung möglicherweise nicht so praktisch wie die horizontale und vertikale Abmessungen des Viewports (im Kamerabereich). Wenn die mathematische Funktion funktioniert, verwenden die beiden folgenden Gleichungen für w und h die Abmessungen des Viewports und entsprechen den vorangehenden Gleichungen.

![Gleichungen der w-und h-Variablen Bedeutungen](images/prjmatx3.png)

In diesen Formeln stellt "Zn" die Position der Near Clipping-Ebene dar, und die V<sub>w</sub> -und die VH-Variablen stellen die Breite und Höhe des Viewports im Kamerabereich dar.

Bei einer C++-Anwendung entsprechen diese beiden Dimensionen direkt den Elementen Width und Height der [**D3DVIEWPORT9**](d3dviewport9.md) -Struktur.

Egal, welche Formel Sie verwenden möchten, achten Sie darauf, dass Sie den Wert für "Zn" so groß wie möglich festlegen, da z-Werte, die sich extrem nahe an der Kamera befinden, nicht um viel variieren. Dies macht Tiefe Vergleiche mit 16-Bit-z-Puffern etwas kompliziert.

Wie bei den Transformationen der Welt und Sicht wird die [**IDirect3DDevice9:: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) -Methode aufgerufen, um die Projektions Transformation festzulegen.

## <a name="setting-up-a-projection-matrix"></a>Einrichten einer Projektions Matrix

Mit der folgenden ProjectionMatrix-Beispiel Funktion werden die Front-und Back-clippingflächen sowie das horizontale und vertikale Feld von Sicht Winkeln festgelegt. Die Felder der Ansicht sollten kleiner als PI-Bogenmaße sein.


```
D3DXMATRIX 
ProjectionMatrix(const float near_plane, // Distance to near clipping 
                                         // plane
                 const float far_plane,  // Distance to far clipping 
                                         // plane
                 const float fov_horiz,  // Horizontal field of view 
                                         // angle, in radians
                 const float fov_vert)   // Vertical field of view 
                                         // angle, in radians
{
    float    h, w, Q;

    w = (float)1/tan(fov_horiz*0.5);  // 1/tan(x) == cot(x)
    h = (float)1/tan(fov_vert*0.5);   // 1/tan(x) == cot(x)
    Q = far_plane/(far_plane - near_plane);

    D3DXMATRIX ret;
    ZeroMemory(&ret, sizeof(ret));

    ret(0, 0) = w;
    ret(1, 1) = h;
    ret(2, 2) = Q;
    ret(3, 2) = -Q*near_plane;
    ret(2, 3) = 1;
    return ret;
}   // End of ProjectionMatrix
```



Legen Sie nach dem Erstellen der Matrix mit [**IDirect3DDevice9:: setTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) eine D3DTS- \_ Projektion fest.

Die D3DX Utility Library bietet die folgenden Funktionen, die Ihnen beim Einrichten der Projektions Matrix helfen.

-   [**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
-   [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
-   [**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
-   [**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
-   [**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
-   [**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a>Eine W-freundliche Projektions Matrix

Direct3D kann die w-Komponente eines Scheitel Punkts verwenden, der von der Welt-, Sicht-und Projektions Matrizen transformiert wurde, um Tiefe basierte Berechnungen in tiefen Puffern oder Nebeleffekten auszuführen. Für Berechnungen wie diese ist es erforderlich, dass die Projektions Matrix w normalisiert, damit Sie dem Raum z entspricht. Kurz gesagt, wenn die Projektions Matrix einen (3, 4) Koeffizienten enthält, der nicht 1 ist, müssen Sie alle Koeffizienten mit der Umkehrung des (3, 4) Koeffizienten skalieren, um eine korrekte Matrix zu erstellen. Wenn Sie keine konforme Matrix bereitstellen, werden die Nebeleffekte und die tiefen Pufferung nicht ordnungsgemäß angewendet.

In der folgenden Abbildung ist eine nicht kompatible Projektions Matrix dargestellt, und die gleiche Matrix wird so skaliert, dass der Augen relative Nebel aktiviert wird.

![Abbildungen einer nicht kompatiblen Projektions Matrix und einer Matrix mit augenblickativem Nebel](images/eyerlmx.png)

In den vorangehenden Matrizen werden alle Variablen als ungleich Null angenommen. Weitere Informationen über Eye-relative Nebel finden Sie unter [Eye-relative im Vergleich zu Z-basierter Tiefe](pixel-fog.md). Weitere Informationen zur w-basierten tiefen Pufferung finden Sie unter [tiefen Puffer (Direct3D 9)](depth-buffers.md).

Direct3D verwendet die aktuell festgelegte Projektions Matrix in den w-basierten tiefen Berechnungen. Daher müssen Anwendungen eine konforme Projektions Matrix festlegen, um die gewünschten w-basierten Funktionen zu erhalten, auch wenn Sie keine Direct3D für Transformationen verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transformationen](transforms.md)
</dt> </dl>

 

 
