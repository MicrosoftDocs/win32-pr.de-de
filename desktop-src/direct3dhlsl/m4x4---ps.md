---
title: m4x4 – ps
description: Multipliziert einen Vierkomponentenvektor mit einer 4x4-Matrix. | m4x4 – ps
ms.assetid: 2a9915a3-f396-4108-97f7-d70c5262ff59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f7dfba3713bcd376c369a17d4856b64965e2e83c22ff03b282d4c9880d6c8700
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906859"
---
# <a name="m4x4---ps"></a>m4x4 – ps

Multipliziert einen Vierkomponentenvektor mit einer 4x4-Matrix.

## <a name="syntax"></a>Syntax



| m4x4 dst, src0, src1 |
|----------------------|



 

where

-   dst ist das Zielregister. Das Ergebnis ist ein 4-Komponenten-Vektor.
-   src0 ist ein Quellregister, das einen 4-Komponenten-Vektor darstellt.
-   src1 ist ein Quellregister, das eine 4x4-Matrix darstellt, die dem ersten von vier aufeinanderfolgenden Registern entspricht.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Die Xyzw-Maske (Standardmaske) ist für das Zielregister erforderlich. Negate- und swizzle-Modifizierer sind für src0, aber nicht für src1 zulässig.

Swizzle- und negate-Modifizierer sind für das src0-Register ungültig. Die Register dst und src0 können nicht identisch sein.

Der folgende Codeausschnitt zeigt die ausgeführten Vorgänge.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z) + (src0.w*src4.w);
```



Der Eingabevektor befindet sich im Register src0. Die Eingabematrix 4x4 befindet sich im Register src1 und die nächsten drei höheren Register, wie in der folgenden Erweiterung gezeigt.

Dieser Vorgang wird häufig zum Transformieren einer Position durch eine Projektionsmatrix verwendet. Diese Anweisung wird wie hier gezeigt als Satz von Punktprodukten implementiert.


```
m4x4   r0.xyzw, r1, c0    will be expanded to:

dp4   r0.x, r1, c0
dp4   r0.y, r1, c1
dp4   r0.z, r1, c2
dp4   r0.w, r1, c3
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




