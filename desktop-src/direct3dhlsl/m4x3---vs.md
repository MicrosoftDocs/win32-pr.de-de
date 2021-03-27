---
title: m4x3-vs
description: Multipliziert einen 4-Komponenten Vektor mit einer 4X3-Matrix. | m4x3-vs
ms.assetid: 12dd31bd-2078-44a1-912e-72c8f377bc4c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7608b1187cc90cf4914bdd42a197cc6044d53734
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981304"
---
# <a name="m4x3---vs"></a>m4x3-vs

Multipliziert einen 4-Komponenten Vektor mit einer 4X3-Matrix.

## <a name="syntax"></a>Syntax



| m4x3 DST, src0, Quelle1 |
|----------------------|



 

where

-   DST ist das Ziel Register. Das Ergebnis ist ein Vektor mit drei Komponenten.
-   src0 ist ein Quell Register, das einen 4-Komponenten Vektor darstellt.
-   Quelle1 ist ein Quell Register, das eine 4X3-Matrix darstellt, die dem ersten von drei aufeinander folgenden Registern entspricht.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| m4x3                   | x    | x    | x    | x     | x    | x     |



 

Die XYZ-Maske ist für das Ziel Register erforderlich. Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.

Das folgende Code Fragment zeigt die ausgeführten Vorgänge.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z) + (src0.w * src1.w);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z) + (src0.w * src2.w);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z) + (src0.w * src3.w);
```



Der Eingabe Vektor befindet sich im Register src0. Die Eingabe 4X3-Matrix befindet sich im Register Quelle1 und den nächsten zwei höheren Registern, wie in der folgenden Erweiterung gezeigt. Ein 3D-Ergebnis wird erzeugt, wobei das andere Element des Ziel Registers (dest. w) nicht betroffen ist.

Dieser Vorgang wird häufig verwendet, um einen Positions Vektor durch eine Matrix zu transformieren, die keine Projective Auswirkung hat, wie z. b. bei Transformationen im Modellbereich. Diese Anweisung wird als Paar von Punkt Produkten implementiert, wie unten gezeigt.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



Die Modifizierern "Swizzle" und "Negation" sind für das Quelle1 Register ungültig. Das DST-und src0-Register dürfen nicht identisch sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




