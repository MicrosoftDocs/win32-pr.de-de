---
description: Scheitel Punkte im Kamerabereich werden berechnet, indem die Objekt Scheitel Punkte mit der World View Matrix transformiert werden.
ms.assetid: 889dd0d8-1933-4901-9bbc-06c3caa26d3e
title: Kamera Raum Transformationen (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e621fa8318fa45023cee13ffc6fcfc65abcf8f5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126884"
---
# <a name="camera-space-transformations-direct3d-9"></a>Kamera Raum Transformationen (Direct3D 9)

Scheitel Punkte im Kamerabereich werden berechnet, indem die Objekt Scheitel Punkte mit der World View Matrix transformiert werden.

V = v \* wvmatrix

Vertex-Normale werden im Kamerabereich berechnet, indem die Objekt normale mit der umgekehrten Umwandlung der World View Matrix transformiert werden. Die World View Matrix ist möglicherweise orthogonal.

N = n \* (wvmatrix ⁻ ¹)<sup>T</sup>

Die Matrix-Inversion und die Matrix werden in einer 4 x 4-Matrix verarbeitet. Das Multiplizieren kombiniert den normalen mit dem 3X3-Teil der resultierenden 4 x 4-Matrix.

Wenn der Rendering-Zustand, D3DRENDERSTATE \_ normalizenormals auf **true** festgelegt ist, werden Scheitelpunkt normale Vektoren nach der Transformation wie folgt normalisiert:

N = Norm (n)

Die helle Position im Kamerabereich wird berechnet, indem die Licht Quell Position mit der Ansichts Matrix transformiert wird.

LP = LP- \* vmatrix

Die Richtung des Lichts im Kamera Raum für ein Direktionales Licht wird berechnet, indem die Lichtquellen Richtung der Ansichts Matrix multipliziert, das Ergebnis normalisiert und nealisiert wird.

L<sub>dir</sub> =-Norm (l<sub>dir</sub> \* wvmatrix)

Für D3DLIGHT \_ Point und D3DLIGHT \_ wird die Richtung "Light" wie folgt berechnet:

L<sub>dir</sub> = Norm (V \* LP), wobei die Parameter in der folgenden Tabelle definiert sind.



| Parameter       | Standardwert | type      | BESCHREIBUNG                                               |
|-----------------|---------------|-----------|-----------------------------------------------------------|
| L-<sub>dir</sub> | –           | D3DVECTOR | Richtung Vektor vom Objekt Scheitelpunkt zum Licht          |
| V               | –           | D3DVECTOR | Scheitelpunkt Position im Kamerabereich                           |
| wvmatrix        | Identity      | D3DMATRIX | Zusammengesetzte Matrix mit Transformationen der Welt und Ansicht |
| N               | –           | D3DVECTOR | Scheitelpunkt normal                                             |
| LP              | –           | D3DVECTOR | Helle Position im Kamerabereich                            |
| vmatrix         | Identity      | D3DMATRIX | Matrix mit der Ansichts Transformation                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Mathematik der Beleuchtung](mathematics-of-lighting.md)
</dt> </dl>

 

 



