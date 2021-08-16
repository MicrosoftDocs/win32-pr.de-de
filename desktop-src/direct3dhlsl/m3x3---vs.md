---
title: m3x3 – im Vergleich
description: Multipliziert einen 3-Komponenten-Vektor mit einer 3x3-Matrix. | m3x3 – im Vergleich
ms.assetid: 6a749ed0-097d-4354-bc70-fbcd879eafab
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 11c1caa682751c3c4d112efd07643233e9cac91392c9e3bb9c575b1f89f5b53f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562060"
---
# <a name="m3x3---vs"></a>m3x3 – im Vergleich

Multipliziert einen 3-Komponenten-Vektor mit einer 3x3-Matrix.

## <a name="syntax"></a>Syntax



| m3x3 dst, src0, src1 |
|----------------------|



 

where

-   dst ist das Zielregister. Das Ergebnis ist ein 3-Komponenten-Vektor.
-   src0 ist ein Quellregister, das einen 3-Komponenten-Vektor darstellt.
-   src1 ist ein Quellregister, das eine 3x3-Matrix darstellt, die dem ersten von drei aufeinanderfolgenden Registern entspricht.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m3x3                   | x    | x    | x    | x     | x    | x     |



 

Die xyz-Maske ist für das Zielregister erforderlich. Negate- und swizzle-Modifizierer sind für src0, aber nicht für src1 zulässig.

Das folgende Codefragment zeigt die ausgeführten Vorgänge.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



Der Eingabevektor befindet sich im Register src0. Die Eingabematrix 3x3 befindet sich im Register src1 und die nächsten beiden höheren Register, wie in der folgenden Erweiterung gezeigt. Ein 3D-Ergebnis wird erzeugt, sodass das andere Element des Zielregisters (dest.w) nicht betroffen ist.

Dieser Vorgang wird häufig zum Transformieren normaler Vektoren während Beleuchtungsberechnungen verwendet. Diese Anweisung wird wie unten gezeigt als Paar von Punktprodukten implementiert.


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




