---
description: In Direct3D beschreiben Vertices Position und Ausrichtung. Jeder Scheitelpunkt in einem primitiven wird durch einen Vektor beschrieben, der seine Position, Farbe, Texturkoordinaten und einen normalen Vektor übergibt, der seine Ausrichtung ermöglicht.
ms.assetid: f18b235c-97ff-4779-8584-8e96b62c7ca3
title: Vektoren, Vertices und Quaternionen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c2e6e6e316b633359205ffd24a64aa349eeec74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521163"
---
# <a name="vectors-vertices-and-quaternions-direct3d-9"></a>Vektoren, Vertices und Quaternionen (Direct3D 9)

In Direct3D beschreiben Vertices Position und Ausrichtung. Jeder Scheitelpunkt in einem primitiven wird durch einen Vektor beschrieben, der seine Position, Farbe, Texturkoordinaten und einen normalen Vektor übergibt, der seine Ausrichtung ermöglicht.

Quaternionen fügen ein viertes Element zu den \[ x-, y-, z- \] Werten hinzu, die einen drei komponentenvektor definieren. Quaternionen stellen eine Alternative zu den Matrix Methoden dar, die in der Regel für 3D-Drehungen verwendet werden. Eine Quaternion stellt eine Achse im 3D-Raum und eine Drehung um diese Achse dar. Beispielsweise kann eine Quaternion eine (1, 1, 2) Achse und eine Drehung von einem Radian darstellen. Quaternions enthalten wertvolle Informationen, aber ihre wahre Leistung ergibt sich aus den beiden Vorgängen, die Sie ausführen können: Komposition und interpolung.

Das Durchführen der Komposition in Quaternionen ähnelt dem kombinieren. Die Komposition von zwei Quaternionen ist wie in der folgenden Abbildung dargestellt.

![Abbildung der Quaternion-Notation](images/quateq.png)

Die Komposition von zwei Quaternionen, die auf eine Geometrie angewendet werden, bedeutet "Drehen der Geometrie um die Achse" durch Drehung, und drehen Sie Sie um die Achse ₁ durch Drehung ₁. " In diesem Fall stellt q eine Drehung um eine einzelne Achse dar, die das Ergebnis der Anwendung von q-Wert ist, und dann q ₁ auf die Geometrie.

Mithilfe der Quaternion-interpolung kann eine Anwendung einen Smooth-und einen angemessenen Pfad von einer Achse und eine Ausrichtung auf eine andere berechnen. Aus diesem Grund bietet die Interpolationsmethode zwischen q ₁ und q-CO2 eine einfache Möglichkeit, um von einer Ausrichtung zu einer anderen zu animieren.

Wenn Sie Komposition und Interpolationen zusammen verwenden, bieten Sie eine einfache Möglichkeit, um eine Geometrie auf eine komplexe Weise zu manipulieren. Stellen Sie sich beispielsweise vor, dass Sie über eine Geometrie verfügen, die Sie zu einer bestimmten Ausrichtung drehen möchten. Sie wissen, dass Sie die r-Grad-um-Achse um die Achse umdrehen und dann den Wert r ₁ Grad um Achse ₁ drehen möchten, aber die endgültige Quaternion ist nicht bekannt. Mithilfe der Komposition können Sie die beiden Rotationen der Geometrie kombinieren, um eine einzelne Quaternion zu erhalten, die das Ergebnis ist. Anschließend könnten Sie von der ursprünglichen zur zusammengesetzten Quaternion interpolieren, um einen reibungslosen Übergang von einem zum anderen zu erzielen.

Die D3DX Utility Library enthält Funktionen, die Ihnen bei der Arbeit mit Quaternionen helfen. Die [**D3DXQuaternionRotationAxis**](d3dxquaternionrotationaxis.md) -Funktion fügt z. b. einen Rotations Wert zu einem Vektor hinzu, der eine Achse der Drehung definiert, und gibt das Ergebnis in einer Quaternion zurück, die durch eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur definiert ist. Außerdem führt die [**D3DXQuaternionMultiply**](d3dxquaternionmultiply.md) -Funktion Quaternionen aus, und [**D3DXQuaternionSlerp**](d3dxquaternionslerp.md) führt eine sphärische lineare interpolung zwischen zwei Quaternionen aus.

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

Direct3D-Anwendungen können die folgenden Funktionen verwenden, um die Aufgabe der Arbeit mit drei-Komponenten-Vektoren zu vereinfachen.

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

Viele zusätzliche Funktionen, die Aufgaben mit zwei-und vier-Komponenten-Vektoren vereinfachen, sind in den [mathematischen Funktionen](dx9-graphics-reference-d3dx-functions-math.md) enthalten, die von der D3DX Utility Library bereitgestellt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Koordinatensysteme und Geometrie](coordinate-systems-and-geometry.md)
</dt> </dl>

 

 



