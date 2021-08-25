---
description: 'In der Regel verwenden 3D-Grafikanwendungen zwei Arten kartesischer Koordinatensysteme: linkshändig und rechtshändig.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Koordinatensysteme (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e47b87ae6374d68b8c836dfb4818781e83e77c288f7bf05b121dbb4426c9aad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857575"
---
# <a name="coordinate-systems-direct3d-9"></a>Koordinatensysteme (Direct3D 9)

In der Regel verwenden 3D-Grafikanwendungen zwei Arten kartesischer Koordinatensysteme: linkshändig und rechtshändig. In beiden Koordinatensystemen zeigt die positive X-Achse nach rechts, und die positive Y-Achse zeigt nach oben. Sie können sich merken, in welche Richtung die positive Z-Achse zeigt, indem Sie die Finger ihrer linken oder rechten Hand in die positive x-Richtung zeigen und sie in die positive y-Richtung drehen. Die Richtung, in der Der Daumen zeigt, entweder auf Sie oder von Ihnen weg, ist die Richtung, die die positive Z-Achse für dieses Koordinatensystem zeigt. Die folgende Abbildung zeigt diese beiden Koordinatensysteme.

![Abbildung der linkshändigen und rechtshändigen kartesischen Koordinatensysteme](images/leftrght.png)

Direct3D verwendet ein linkshändiges Koordinatensystem. Wenn Sie eine Anwendung portieren, die auf einem rechtshändigen Koordinatensystem basiert, müssen Sie zwei Änderungen an den an Direct3D übergebenen Daten vornehmen.

-   Kippen Sie die Reihenfolge der Dreiecksvertices, sodass das System sie im Uhrzeigersinn vom Anfang durchläuft. Anders ausgedrückt: Wenn die Scheitelungen v0, v1, v2 sind, übergeben Sie sie als v0, v2, v1 an Direct3D.
-   Verwenden Sie die Ansichtsmatrix, um den Weltraum in Z-Richtung um -1 zu skalieren. Kippen Sie dazu das Vorzeichen des \_ 31-, \_ 32-, \_ 33- und 34-Members der \_ [**D3DMATRIX-Struktur,**](d3dmatrix.md) die Sie für Ihre Ansichtsmatrix verwenden.

Verwenden Sie die Funktionen [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) und [**D3DXMatrixOrthoRH,**](d3dxmatrixorthorh.md) um die Projektionstransformation zu definieren. Achten Sie jedoch darauf, die entsprechende [**D3DXMatrixLookAtRH-Funktion**](d3dxmatrixlookatrh.md) zu verwenden, die Backface-Culling-Reihenfolge umzukehren und die Cubezuordnungen entsprechend zu gestalten.

Obwohl linkshändige und rechtshändige Koordinaten die gängigsten Systeme sind, gibt es eine Vielzahl anderer Koordinatensysteme, die in 3D-Software verwendet werden. Beispielsweise ist es für 3D-Modellierungsanwendungen nicht ungewöhnlich, ein Koordinatensystem zu verwenden, in dem die Y-Achse auf den Viewer zeigt bzw. vom Viewer weg zeigt und die Z-Achse nach oben zeigt.

Formal kann die Ausrichtung eines Sets von Basisvektoren (d. h. eines Koordinatensystems) durch das Berechnen der Determinante der Matrix gefunden werden, die durch den bestimmten Satz von Basisvektoren definiert wird. Wenn die Determinante positiv ist, wird die Basis als "positiv" ausgerichtet (oder rechtshändig) bezeichnet. Wenn die Determinante negativ ist, wird die Basis als "negativ" ausgerichtet (oder linkshändig) bezeichnet. Eine Erläuterung, was eine Determinante ist, finden Sie in jeder linearen Algebraressource.

Informell können Sie mithilfe der "Rechts/Links-Regel" bestimmen, ob ein angegebener Satz von Basisvektoren entweder ein rechts- oder linkshändiges Koordinatensystem bildet.

Die wesentlichen Vorgänge für Objekte, die in einem 3D-Koordinatensystem definiert sind, sind Übersetzung, Drehung und Skalierung. Sie können diese grundlegenden Transformationen kombinieren, um eine Transformationsmatrix zu erstellen. Weitere Informationen finden Sie unter [Transformationen (Direct3D 9).](transforms.md)

Wenn Sie diese Vorgänge kombinieren, sind die Ergebnisse nicht kommutativ. die Reihenfolge, in der Sie Matrizen multiplizieren, ist wichtig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



