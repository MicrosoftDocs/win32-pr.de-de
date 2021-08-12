---
description: In Direct3D beschreiben Scheitelungen die Position und Ausrichtung. Jeder Scheitelpunkt in einem Primitiven wird durch einen Vektor beschrieben, der seine Position, Farbe, Texturkoordinaten und einen normalen Vektor angibt, der seine Ausrichtung angibt.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Vektoren, Scheitelungen und Quaternionen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 601b6a71dcb00356d4de4637a6aabb1eba5c02e49c62380b32732351d15bfcb4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118290441"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a>Vektoren, Scheitelungen und Quaternionen (Direct3D 9)

In Direct3D beschreiben Scheitelungen die Position und Ausrichtung. Jeder Scheitelpunkt in einem Primitiven wird durch einen Vektor beschrieben, der seine Position, Farbe, Texturkoordinaten und einen normalen Vektor angibt, der seine Ausrichtung angibt.

Quaternionen fügen den \[ x-, y-, z-Werten, die einen \] Drei-Komponenten-Vektor definieren, ein viertes Element hinzu. Quaternionen sind eine Alternative zu den Matrixmethoden, die in der Regel für 3D-Drehungen verwendet werden. Eine Quaternion stellt eine Achse im 3D-Raum und eine Drehung um diese Achse dar. Beispielsweise kann eine Quaternion eine (1,1,2) Achse und eine Drehung von 1 Bogenmaß darstellen. Quaternionen enthalten wertvolle Informationen, aber ihre wahre Leistung geht auf die beiden Vorgänge zurück, die Sie für sie ausführen können: Komposition und Interpolation.

Das Durchführen der Komposition für Quaternionen ähnelt der Kombination dieser Quaternionen. Die Zusammensetzung von zwei Quaternionen wird wie in der folgenden Abbildung dargestellt notiert.

![Abbildung der Quaternions-Notation](images/quateq.png)

Die Zusammensetzung von zwei Quaternionen, die auf eine Geometrie angewendet werden₂ bedeutet "die Geometrie um die Achse drehen₂ durch Drehung₂ und dann um die Achse drehen₁ durch Drehung₁." In diesem Fall stellt Q eine Drehung um eine einzelne Achse dar, die das Ergebnis der Anwendung von q₂ und dann q₁ auf die Geometrie ist.

Mithilfe der Quaternioninterpolation kann eine Anwendung einen reibungslosen und angemessenen Pfad von einer Achse und Ausrichtung zur anderen berechnen. Daher bietet die Interpolation zwischen q₁ und q₂ eine einfache Möglichkeit, von einer Ausrichtung zur anderen zu animieren.

Wenn Sie Komposition und Interpolation zusammen verwenden, bieten sie Ihnen eine einfache Möglichkeit, eine Geometrie auf eine komplexe Weise zu bearbeiten. Angenommen, Sie verfügen über eine Geometrie, die Sie zu einer bestimmten Ausrichtung drehen möchten. Sie wissen, dass Sie es r₂ Grad um die Achse drehen möchten₂ und dann um die Achse drehen möchten₁ Grad um die Achse₁ aber Sie kennen die endgültige Quaternion nicht. Mithilfe der Komposition können Sie die beiden Drehungen der Geometrie kombinieren, um eine einzelne Quaternion zu erhalten, die das Ergebnis ist. Anschließend können Sie von der ursprünglichen zur zusammengesetzten Quaternion interpolieren, um einen reibungslosen Übergang von der einen zur anderen zu erreichen.

Die D3DX-Hilfsprogrammbibliothek enthält Funktionen, die Ihnen bei der Arbeit mit Quaternionen helfen. Beispielsweise fügt die [**D3DXQuaternionRotationAxis-Funktion**](d3dxquaternionrotationaxis.md) einem Vektor, der eine Drehachse definiert, einen Drehungswert hinzu und gibt das Ergebnis in einer Quaternion zurück, die durch eine [**D3DXQUATERNION-Struktur**](d3dxquaternion.md) definiert ist. Darüber hinaus erstellt die [**D3DXQuaternionMultiply-Funktion**](d3dxquaternionmultiply.md) Quaternionen, und [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) führt eine pherische lineare Interpolation zwischen zwei Quaternionen durch.

Direct3D-Anwendungen können die folgenden Funktionen verwenden, um die Arbeit mit Quaternionen zu vereinfachen.

-   [**D3DXQuaternionBaryCentric**](d3dxquaternionbarycentric.md)
-   [**D3DXQuaternionConjugate**](d3dxquaternionconjugate.md)
-   [**D3DXQuaternionDot**](d3dxquaterniondot.md)
-   [**D3DXQuaternionExp**](d3dxquaternionexp.md)
-   [**D3DXQuaternionIdentity**](d3dxquaternionidentity.md)
-   [**D3DXQuaternionInverse**](d3dxquaternioninverse.md)
-   [**D3DXQuaternionIsIdentity**](d3dxquaternionisidentity.md)
-   [**D3DXQuaternionLength**](d3dxquaternionlength.md)
-   [**D3DXQuaternionLengthSq**](d3dxquaternionlengthsq.md)
-   [**D3DXQuaternionLn**](d3dxquaternionln.md)
-   [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md)
-   [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md)
-   [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md)
-   [**D3DXQuaternionRotationMatrix**](d3dxquaternionrotationmatrix.md)
-   [**D3DXQuaternionRotationYawPitchRoll**](d3dxquaternionrotationyawpitchroll.md)
-   [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md)
-   [**D3DXQuaternionSquad**](d3dxquaternionsquad.md)
-   [**D3DXQuaternionToAxisAngle**](d3dxquaterniontoaxisangle.md)

Direct3D-Anwendungen können die folgenden Funktionen verwenden, um die Arbeit mit drei Komponentenvektoren zu vereinfachen.

-   [**D3DXVec3Add**](d3dxvec3add.md)
-   [**D3DXVec3BaryCentric**](d3dxvec3barycentric.md)
-   [**D3DXVec3CatmullRom**](d3dxvec3catmullrom.md)
-   [**D3DXVec3Cross**](d3dxvec3cross.md)
-   [**D3DXVec3Dot**](d3dxvec3dot.md)
-   [**D3DXVec3Hermite**](d3dxvec3hermite.md)
-   [**D3DXVec3Length**](d3dxvec3length.md)
-   [**D3DXVec3LengthSq**](d3dxvec3lengthsq.md)
-   [**D3DXVec3Lerp**](d3dxvec3lerp.md)
-   [**D3DXVec3Maximize**](d3dxvec3maximize.md)
-   [**D3DXVec3Minimize**](d3dxvec3minimize.md)
-   [**D3DXVec3Normalize**](d3dxvec3normalize.md)
-   [**D3DXVec3Project**](d3dxvec3project.md)
-   [**D3DXVec3Scale**](d3dxvec3scale.md)
-   [**D3DXVec3Subtract**](d3dxvec3subtract.md)
-   [**D3DXVec3Transform**](d3dxvec3transform.md)
-   [**D3DXVec3TransformCoord**](d3dxvec3transformcoord.md)
-   [**D3DXVec3TransformNormal**](d3dxvec3transformnormal.md)
-   [**D3DXVec3Unproject**](d3dxvec3unproject.md)

Viele zusätzliche Funktionen, die Aufgaben mit zwei- und vier [](dx9-graphics-reference-d3dx-functions-math.md) Komponentenvektoren vereinfachen, sind in den mathematischen Funktionen enthalten, die von der D3DX-Hilfsprogrammbibliothek bereitgestellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



