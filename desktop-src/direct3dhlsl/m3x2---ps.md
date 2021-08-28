---
title: m3x2 – ps
description: Multipliziert einen 3-Komponenten-Vektor mit einer 3x2-Matrix. | m3x2 – ps
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59bf908a2858e46f9c1e339db32d3e6e57062bc280b8223a9fcb66a527380773
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672640"
---
# <a name="m3x2---ps"></a>m3x2 – ps

Multipliziert einen 3-Komponenten-Vektor mit einer 3x2-Matrix.

## <a name="syntax"></a>Syntax



| m3x2 dst, src0, src1 |
|----------------------|



 

where

-   dst ist das Zielregister. Das Ergebnis ist ein Vektor mit zwei Komponenten.
-   src0 ist ein Quellregister, das einen 3-Komponenten-Vektor darstellt.
-   src1 ist ein Quellregister, das eine 3x2-Matrix darstellt, die dem ersten von zwei aufeinanderfolgenden Registern entspricht.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x2                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Die xy-Maske ist für das Zielregister erforderlich. Die Modifizierer Negate und swizzle sind für src0 zulässig, aber nicht für src1.

Die folgenden Gleichungen zeigen, wie die Anweisung funktioniert:


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



Der Eingabevektor befindet sich im Register src0. Die 3x2-Eingabematrix befindet sich im Register src1 und das nächste höhere Register in derselben Registerdatei, wie in der folgenden Erweiterung gezeigt. Es wird ein 2D-Ergebnis erzeugt, ohne dass die anderen Elemente des Zielregisters (dest.z und dest.w) davon betroffen sind.

Dieser Vorgang wird häufig für 2D-Transformationen verwendet. Diese Anweisung wird wie hier gezeigt als Punktproduktepaar implementiert.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Swizzle- und negate-Modifizierer sind für das Register src1 ungültig. Das Register dst und src0 oder eines der Register von src1+i darf nicht identisch sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




