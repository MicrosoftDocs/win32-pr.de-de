---
description: Sie können sich die Projektionstransformation als Steuerung der Internen der Kamera einbilden. sie entspricht der Auswahl einer Brille für die Kamera.
ms.assetid: 09e6e887-7657-4654-be19-2e83dcbc91cf
title: Projektionstransformation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad15ee0f4d23401563a9a51b8767be3da6e47dfee9dc76d580154ef1d524d02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092690"
---
# <a name="projection-transform-direct3d-9"></a>Projektionstransformation (Direct3D 9)

Sie können sich die Projektionstransformation als Steuerung der Internen der Kamera einbilden. sie entspricht der Auswahl einer Brille für die Kamera. Dies ist der komplizierteste der drei Transformationstypen. Diese Erörterung der Projektionstransformation ist in die folgenden Themen organisiert.

Die Projektionsmatrix ist in der Regel eine Skalierungs- und Perspektivprojektion. Die Projektionstransformation konvertiert das Anzeigefrustum in eine Cuboidform. Da das nahe Ende des Frustums kleiner als das ferne Ende ist, hat dies den Effekt, objekte zu erweitern, die sich in der Nähe der Kamera befinden. auf diese Weise wird die Perspektive auf die Szene angewendet.

Im Frustum wird der Abstand zwischen der Kamera und dem Ursprung des [Ansichtstransformationsraums](viewports-and-clipping.md)willkürlich als D definiert, sodass die Projektionsmatrix wie in der folgenden Abbildung aussieht.

![Abbildung der Projektionsmatrix](images/projmat1.png)

Die Anzeigematrix übersetzt die Kamera in den Ursprung, indem sie in z-Richtung um – D übersetzt wird. Die Übersetzungsmatrix ist wie in der folgenden Abbildung dargestellt.

![Abbildung der Übersetzungsmatrix](images/projmat2.png)

Das Multiplizieren der Übersetzungsmatrix mit der Projektionsmatrix (T P) ergibt die zusammengesetzte Projektionsmatrix, wie \* in der folgenden Abbildung dargestellt.

![Abbildung der zusammengesetzten Projektionsmatrix](images/projmat3.png)

Die Perspektivtransformation konvertiert ein Frustum für die Anzeige in einen neuen Koordinatenraum. Beachten Sie, dass das Frustum zu einem Cuboid wird und dass der Ursprung von der oberen rechten Ecke der Szene in die Mitte wechselt, wie im folgenden Diagramm dargestellt.

![Diagramm, das zeigt, wie die Perspektivtransformation das Frustum der Anzeige in einen neuen Koordinatenraum ändert](images/cuboid.png)

In der Perspektiventransformation sind die Grenzwerte der x- und y-Richtungen -1 und 1. Die Grenzwerte der Z-Richtung sind 0 für die front-Ebene und 1 für die Rückebene.

Diese Matrix übersetzt und skaliert Objekte basierend auf einem angegebenen Abstand von der Kamera zur nahe Clippingebene, aber sie betrachtet das Sichtfeld (fov) nicht, und die Z-Werte, die sie für Objekte in der Entfernung erzeugt, können nahezu identisch sein, was Tiefenvergleiche erschwert. Die folgende Matrix behandelt diese Probleme und passt Scheitelpunkte an das Seitenverhältnis des Viewports an und ist damit eine gute Wahl für die Perspektivprojektion.

![Abbildung einer Matrix für die Perspektivprojektion](images/prjmatx1.png)

In dieser Matrix ist Zn der Z-Wert der nah beschneidenden Ebene. Die Variablen w, h und Q haben die folgenden Bedeutungen. Beachten Sie, dass fov<sub>w</sub> und fovk die horizontalen und vertikalen Sichtfelder des Viewports im Bogenmaß darstellen.

![Gleichungen der variablen Bedeutungen](images/prjmatx2.png)

Für Ihre Anwendung ist die Verwendung von Sichtfeldwinkeln zum Definieren der X- und y-Skalierungskoeffizienten möglicherweise nicht so praktisch wie die Verwendung der horizontalen und vertikalen Abmessungen des Viewports (im Kameraraum). Während die Mathematik funktioniert, verwenden die folgenden beiden Gleichungen für w und h die Dimensionen des Viewports und entsprechen den vorherigen Gleichungen.

![Gleichungen der Bedeutungen der Variablen "w" und "h"](images/prjmatx3.png)

In diesen Formeln stellt Zn die Position der nah beschneidenden Ebene dar, und die Variablen V<sub>w</sub> und Vh stellen die Breite und Höhe des Viewports im Kameraraum dar.

Bei einer C++-Anwendung entsprechen diese beiden Dimensionen direkt den Width- und Height-Membern der [**D3DVIEWPORT9-Struktur.**](d3dviewport9.md)

Unabhängig davon, welche Formel Sie verwenden möchten, stellen Sie sicher, dass Zn so groß wie möglich ist, da Z-Werte, die sich extrem nah an der Kamera liegen, nicht stark variieren. Dadurch werden Tiefenvergleiche mit 16-Bit-Z-Puffern etwas kompliziert.

Wie bei den Welt- und Ansichtstransformationen rufen Sie die [**IDirect3DDevice9::SetTransform-Methode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) auf, um die Projektionstransformation festlegen.

## <a name="setting-up-a-projection-matrix"></a>Einrichten einer Projektionsmatrix

Die folgende ProjectionMatrix-Beispielfunktion legt die Vorder- und Rückschneideebenen sowie das horizontale und vertikale Feld der Ansichtswinkel fest. Die Sichtfelder sollten kleiner als pi radians sein.


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



Legen Sie die Matrix nach dem Erstellen mit [**IDirect3DDevice9::SetTransform fest,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) und geben Sie dabei D3DTS \_ PROJECTION an.

Die D3DX-Hilfsprogrammbibliothek bietet die folgenden Funktionen, die Sie beim Einrichten Ihrer Projektionsmatrix unterstützen.

-   [**D3DXMatrixPerspectiveLH**](d3dxmatrixperspectivelh.md)
-   [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md)
-   [**D3DXMatrixPerspectiveFovLH**](d3dxmatrixperspectivefovlh.md)
-   [**D3DXMatrixPerspectiveFovRH**](d3dxmatrixperspectivefovrh.md)
-   [**D3DXMatrixPerspectiveOffCenterLH**](d3dxmatrixperspectiveoffcenterlh.md)
-   [**D3DXMatrixPerspectiveOffCenterRH**](d3dxmatrixperspectiveoffcenterrh.md)

## <a name="a-w-friendly-projection-matrix"></a>Eine W-freundliche Projektionsmatrix

Direct3D kann die w-Komponente eines Scheitelpunkts verwenden, der von den Welt-, Ansichts- und Projektionsmatrizen transformiert wurde, um tiefenbasierte Berechnungen in Tiefenpuffer- oder Effekteffekten durchzuführen. Berechnungen wie diese erfordern, dass ihre Projektionsmatrix w normalisiert, damit sie mit world-space z äquivalent ist. Kurz gesagt: Wenn Ihre Projektionsmatrix einen (3,4) Koeffizienten enthält, der nicht 1 ist, müssen Sie alle Koeffizienten um die Umkehrung des (3,4)-Koeffizienten skalieren, um eine ordnungsgemäße Matrix zu erstellen. Wenn Sie keine konforme Matrix bereitstellen, werden Die Effekten und die Tiefenpufferung nicht ordnungsgemäß angewendet.

Die folgende Abbildung zeigt eine nicht konforme Projektionsmatrix und die gleiche Matrix, die so skaliert wird, dass die augen relative Brille aktiviert wird.

![Abbildungen einer nicht konformen Projektionsmatrix und einer Matrix mit augen relativem Brillen](images/eyerlmx.png)

In den obigen Matrizen wird davon ausgegangen, dass alle Variablen ungleich 0 (null) sind. Weitere Informationen zu augen relativen Brillen finden Sie unter [Eye-Relative vs. Z-Based Depth](pixel-fog.md). Informationen zur w-basierten Tiefenpufferung finden Sie unter [Tiefenpuffer (Direct3D 9).](depth-buffers.md)

Direct3D verwendet die derzeit festgelegte Projektionsmatrix in seinen w-basierten Tiefenberechnungen. Daher müssen Anwendungen eine konforme Projektionsmatrix festlegen, um die gewünschten w-basierten Features zu erhalten, auch wenn sie Direct3D nicht für Transformationen verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Transformationen](transforms.md)
</dt> </dl>

 

 
