---
title: m4x3 – ps
description: Multipliziert einen 4-Komponenten-Vektor mit einer 4x3-Matrix. | m4x3 – ps
ms.assetid: cf9ae4c3-6cdf-4c6f-b34c-0ebd3c8a4123
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 4e291c268aae4173cb3ace4fc00beb5f1a3aa9f0b3d335f80891a851bcab41b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982030"
---
# <a name="m4x3---ps"></a>m4x3 – ps

Multipliziert einen 4-Komponenten-Vektor mit einer 4x3-Matrix.

## <a name="syntax"></a>Syntax



| m4x3 dst, src0, src1 |
|----------------------|



 

where

-   dst ist das Zielregister. Das Ergebnis ist ein 3-Komponenten-Vektor.
-   src0 ist ein Quellregister, das einen 4-Komponenten-Vektor darstellt.
-   src1 ist ein Quellregister, das eine 4x3-Matrix darstellt, die dem ersten von drei aufeinanderfolgenden Registern entspricht.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x3                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Die xyz-Maske ist für das Zielregister erforderlich. Negate- und Swizzle-Modifizierer sind für src0 zulässig, aber nicht für src1.

Der folgende Codeausschnitt zeigt die ausgeführten Vorgänge.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
```



Der Eingabevektor befindet sich im Register src0. Die 4x3-Eingabematrix befindet sich im Register src1 und die nächsten beiden höheren Register, wie in der folgenden Erweiterung gezeigt. Ein 3D-Ergebnis wird erzeugt, ohne dass das andere Element des Zielregisters (dest.w) davon betroffen ist.

Dieser Vorgang wird häufig zum Transformieren eines Positionsvektors durch eine Matrix verwendet, die keinen projektiven Effekt hat, z. B. bei Modellraumtransformationen. Diese Anweisung wird wie unten gezeigt als Satz von Punktprodukten implementiert.


```
m4x3   r0.xyz, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
```



Swizzle- und negate-Modifizierer sind für das Register src1 ungültig. Das Register dst und src0 dürfen nicht identisch sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




