---
description: 'In der Regel verwenden 3D-Grafikanwendungen zwei Arten von kartesischen Koordinatensystemen: Links-und rechtsbündig.'
ms.assetid: 268c3024-85a5-4fd5-b575-e126dd4be97c
title: Koordinatensysteme (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcb9fa389b2bf11bec9ee4f8053bbeb4c822f422
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341122"
---
# <a name="coordinate-systems-direct3d-9"></a>Koordinatensysteme (Direct3D 9)

In der Regel verwenden 3D-Grafikanwendungen zwei Arten von kartesischen Koordinatensystemen: Links-und rechtsbündig. In beiden Koordinatensystemen zeigt die positive x-Achse nach rechts, und die positive y-Achse zeigt nach oben. Sie können merken, welche Richtung die positive z-Achse zeigt, indem Sie die Finger entweder in der linken oder rechten Ecke in der positiven x-Richtung zeigen und Sie in die positive y-Richtung hineinbewegen. Die Richtung, auf die sich der Ziehpunkt von Ihnen befindet, ist die Richtung, auf die die positive z-Achse für dieses Koordinatensystem zeigt. In der folgenden Abbildung werden diese beiden Koordinatensysteme veranschaulicht.

![Abbildung der links gerichteten und rechts gerichteten kartesischen Koordinatensysteme](images/leftrght.png)

Direct3D verwendet ein Links händiges Koordinatensystem. Wenn Sie eine Anwendung portieren, die auf einem rechts gerichteten Koordinatensystem basiert, müssen Sie zwei Änderungen an den Daten vornehmen, die an Direct3D übergeben werden.

-   Kippen Sie die Reihenfolge der Dreiecks Scheitel Punkte, sodass Sie vom System im Uhrzeigersinn nach vorne durchlaufen werden. Anders ausgedrückt: Wenn es sich bei den Scheitel Punkten um v0, v1, v2 handelt, übergeben Sie Sie an Direct3D als v0, v2, v1.
-   Verwenden Sie die Ansichts Matrix, um den Welt Raum um-1 in der z-Richtung zu skalieren. Um dies zu erreichen, kippen Sie das Vorzeichen der \_ Member 31, \_ 32, \_ 33 und \_ 34 der [**D3DMATRIX**](d3dmatrix.md) -Struktur, die Sie für die Sicht Matrix verwenden.

Verwenden Sie die [**D3DXMatrixPerspectiveRH**](d3dxmatrixperspectiverh.md) -Funktion und die [**D3DXMatrixOrthoRH**](d3dxmatrixorthorh.md) -Funktion, um die Projektions Transformation zu definieren. Achten Sie jedoch darauf, dass Sie die entsprechende [**D3DXMatrixLookAtRH**](d3dxmatrixlookatrh.md) -Funktion verwenden, die Backface-cullinger-Reihenfolge umkehren und die Cubemaps entsprechend aufstellen.

Obwohl Links ausgegebene und rechts gerichtete Koordinaten die gängigsten Systeme sind, gibt es eine Vielzahl anderer Koordinatensysteme, die in 3D-Software verwendet werden. Beispielsweise ist es nicht ungewöhnlich, dass 3D-Modellierungs Anwendungen ein Koordinatensystem verwenden, in dem die y-Achse auf den Viewer hin-und Weg zeigt, und die z-Achse zeigt nach oben.

Formal kann die Ausrichtung eines Satzes von Basis Vektoren (d. h. ein Koordinatensystem) durch das Berechnen der Determinanten der Matrix gefunden werden, die durch einen bestimmten Satz von Basis Vektoren definiert wird. Wenn die Determinante positiv ist, wird die Basis als "positiv" (oder Rechtshändig) bezeichnet. Wenn die Determinante negativ ist, wird die Basis als "negativ" (oder linksbündig) bezeichnet. Eine Erläuterung dazu, was eine Determinante ist, finden Sie unter beliebige lineare Algebra-Ressourcen.

Informell können Sie mithilfe der "right/left-Rule"-Regel ermitteln, ob ein bestimmter Satz von Basis Vektoren entweder ein Rechtes oder Links händiges Koordinatensystem bildet.

Die wesentlichen Vorgänge, die für in einem 3D-Koordinatensystem definierte Objekte ausgeführt werden, sind Übersetzung, Drehung und Skalierung. Sie können diese grundlegenden Transformationen kombinieren, um eine Transformationsmatrix zu erstellen. Weitere Informationen finden Sie unter [Transformationen (Direct3D 9)](transforms.md).

Wenn Sie diese Vorgänge kombinieren, sind die Ergebnisse nicht kommutativ. die Reihenfolge, in der Sie Matrizen multiplizieren, ist wichtig.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



