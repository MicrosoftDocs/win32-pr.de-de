---
title: m3x2 – im Vergleich
description: Multipliziert einen 3-Komponenten-Vektor mit einer 3x2-Matrix. | m3x2 – im Vergleich
ms.assetid: 4ef3bd47-3e38-4d9d-a8f5-6ee9c08de69c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ad05ef52970e30d2a130279c6109409205acb9615816e3fa0c7e185998f62254
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854140"
---
# <a name="m3x2---vs"></a>m3x2 – im Vergleich

Multipliziert einen 3-Komponenten-Vektor mit einer 3x2-Matrix.

## <a name="syntax"></a>Syntax



| m3x2 dst, src0, src1 |
|----------------------|



 

where

-   dst ist das Zielregister. Das Ergebnis ist ein 2-Komponenten-Vektor.
-   src0 ist ein Quellregister, das einen 3-Komponenten-Vektor darstellt.
-   src1 ist ein Quellregister, das eine 3x2-Matrix darstellt, die dem ersten von zwei aufeinanderfolgenden Registern entspricht.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m3x2                   | x    | x    | x    | x     | x    | x     |



 

Die xy-Maske ist für das Zielregister erforderlich. Negate- und swizzle-Modifizierer sind für src0, aber nicht für src1 zulässig.

Die folgenden Gleichungen zeigen, wie die Anweisung funktioniert:


```
dest.x = (src0.x * src1.x) + (src0.x * src1.y) + (src0.x * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
```



Der Eingabevektor befindet sich im Register src0. Die Eingabematrix 3x2 befindet sich im Register src1 und das nächsthöhere Register in derselben Registerdatei, wie in der folgenden Erweiterung gezeigt. Ein 2D-Ergebnis wird erzeugt, sodass die anderen Elemente des Zielregisters (dest.z und dest.w) nicht betroffen sind.

Dieser Vorgang wird häufig für 2D-Transformationen verwendet. Diese Anweisung wird wie hier gezeigt als Paar von Punktprodukten implementiert.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Swizzle- und negate-Modifizierer sind für das src1-Register ungültig. Das dest- und src0-Register oder eines der src1+i-Register können nicht identisch sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




