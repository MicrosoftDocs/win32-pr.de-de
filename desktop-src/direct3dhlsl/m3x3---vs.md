---
title: M3x3-vs
description: Multipliziert einen 3-Komponenten Vektor mit einer 3X3-Matrix. | M3x3-vs
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e75cdb4b098b92ea358c32e40b3948c7ac73e0cf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104394001"
---
# <a name="m3x3---vs"></a>M3x3-vs

Multipliziert einen 3-Komponenten Vektor mit einer 3X3-Matrix.

## <a name="syntax"></a>Syntax



| M3x3 DST, src0, Quelle1 |
|----------------------|



 

where

-   DST ist das Ziel Register. Das Ergebnis ist ein Vektor mit drei Komponenten.
-   src0 ist ein Quell Register, das einen 3-Komponenten Vektor darstellt.
-   Quelle1 ist ein Quell Register, das eine 3X3-Matrix darstellt, die dem ersten von drei aufeinander folgenden Registern entspricht.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| m3x3                   | x    | x    | x    | x     | x    | x     |



 

Die XYZ-Maske ist für das Ziel Register erforderlich. Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.

Das folgende Code Fragment zeigt die ausgeführten Vorgänge.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



Der Eingabe Vektor befindet sich im Register src0. Die 3X3-Eingabe Matrix befindet sich im Register Quelle1 und den nächsten zwei höheren Registern, wie in der folgenden Erweiterung gezeigt. Ein 3D-Ergebnis wird erzeugt, wobei das andere Element des Ziel Registers (dest. w) nicht betroffen ist.

Dieser Vorgang wird häufig verwendet, um normale Vektoren während der Beleuchtungsberechnungen zu transformieren. Diese Anweisung wird als Paar von Punkt Produkten implementiert, wie unten gezeigt.


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




