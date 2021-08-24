---
description: Scheitelpunkte im Kameraraum werden berechnet, indem die Objektvertices mit der Weltansichtsmatrix transformiert werden.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Kameraraumtransformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: effb7af72decad711d9fc392e53f7aba05f48b3c69394dbfb3ae5f9f06e2def7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119241850"
---
# <a name="camera-space-transformations-direct3d-9"></a>Kameraraumtransformationen (Direct3D 9)

Scheitelpunkte im Kameraraum werden berechnet, indem die Objektvertices mit der Weltansichtsmatrix transformiert werden.

V = V \* wvMatrix

Vertexnormalen werden im Kameraraum berechnet, indem die Objektnormalen mit der umgekehrten Transponierung der Weltansichtsmatrix transformiert werden. Die Weltansichtsmatrix kann orthogonal sein.

N = N \* (wvMatrix⁻¹)<sup>T</sup>

Die Matrixumkehr und matrix transponieren arbeiten mit einer 4x4-Matrix. Die Multiplikation kombiniert die Normale mit dem 3x3-Teil der resultierenden 4x4-Matrix.

Wenn der Renderzustand D3DRENDERSTATE \_ NORMALIZENORMALS auf **TRUE** festgelegt ist, werden vertexnormale Vektoren nach der Transformation in den Kameraraum wie folgt normalisiert:

N = norm(N)

Die Lichtposition im Kameraraum wird berechnet, indem die Position der Lichtquelle mit der Ansichtsmatrix transformiert wird.

Lp = Lp \* vMatrix

Die Richtung zum Licht im Kameraraum für ein gerichtetes Licht wird berechnet, indem die Lichtquellenrichtung mit der Ansichtsmatrix multipliziert, normalisiert und das Ergebnis negiert wird.

L<sub>dir</sub> = -norm(L<sub>dir</sub> \* wvMatrix)

Für D3DLIGHT \_ POINT und D3DLIGHT \_ SPOT wird die Richtung zum Licht wie folgt berechnet:

L<sub>dir</sub> = norm(V \* Lp), wobei die Parameter in der folgenden Tabelle definiert sind.



| Parameter       | Standardwert | Typ      | Beschreibung                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| L<sub>dir</sub> | Nicht zutreffend           | D3DVECTOR | Richtungsvektor vom Objektvertex zum Licht          |
| V               | Nicht zutreffend           | D3DVECTOR | Vertexposition im Kameraraum                           |
| wvMatrix        | Identität      | D3DMATRIX | Zusammengesetzte Matrix, die die Welt- und Ansichtstransformationen enthält |
| N               | Nicht zutreffend           | D3DVECTOR | Vertex normal                                             |
| Lp              | Nicht zutreffend           | D3DVECTOR | Lichtposition im Kameraraum                            |
| vMatrix         | Identität      | D3DMATRIX | Matrix, die die Ansichtstransformation enthält                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



