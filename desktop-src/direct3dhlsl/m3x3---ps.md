---
title: m3x3 – ps
description: Multipliziert einen 3-Komponenten-Vektor mit einer 3x3-Matrix. | m3x3 – ps
ms.assetid: 71342e05-69a6-41f4-bafb-643f0ceb0a59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: af5f56f659c547d34a61e8bb65ef6cf2730f7e3b0d43f488454e79fe4e02cd33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089286"
---
# <a name="m3x3---ps"></a>m3x3 – ps

Multipliziert einen 3-Komponenten-Vektor mit einer 3x3-Matrix.

## <a name="syntax"></a>Syntax



| m3x3 dst, src0, src1 |
|----------------------|



 

where

-   dst ist das Zielregister. Das Ergebnis ist ein 3-Komponenten-Vektor.
-   src0 ist ein Quellregister, das einen 3-Komponenten-Vektor darstellt.
-   src1 ist ein Quellregister, das eine 3x3-Matrix darstellt, die dem ersten von drei aufeinanderfolgenden Registern entspricht.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x3                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Die xyz-Maske ist für das Zielregister erforderlich. Die Modifizierer Negate und swizzle sind für src0 zulässig, aber nicht für src1.

Der folgende Codeausschnitt zeigt die ausgeführten Vorgänge.


```
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
```



Der Eingabevektor befindet sich im Register src0. Die 3x3-Eingabematrix befindet sich im Register src1 und die nächsten beiden höheren Register, wie in der folgenden Erweiterung gezeigt. Ein 3D-Ergebnis wird erzeugt, ohne dass das andere Element des Zielregisters (dest.w) davon betroffen ist.

Dieser Vorgang wird häufig zum Transformieren normaler Vektoren während Beleuchtungsberechnungen verwendet. Diese Anweisung wird wie unten gezeigt als Satz von Punktprodukten implementiert.


```
m3x3 r0.xyz, r1, c0  which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
dp3   r0.z, r1, c2
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




