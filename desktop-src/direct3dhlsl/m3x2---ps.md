---
title: m3x2-PS
description: Multipliziert einen 3-Komponenten Vektor mit einer 3 x 2-Matrix. | m3x2-PS
ms.assetid: a88e6228-a61a-408c-8d89-a5706dd146d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 26532c78fa829b9c2a41f715b814ee8a0f44c879
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982012"
---
# <a name="m3x2---ps"></a>m3x2-PS

Multipliziert einen 3-Komponenten Vektor mit einer 3 x 2-Matrix.

## <a name="syntax"></a>Syntax



| m3x2 DST, src0, Quelle1 |
|----------------------|



 

where

-   DST ist das Ziel Register. Das Ergebnis ist ein Vektor mit zwei Komponenten.
-   src0 ist ein Quell Register, das einen 3-Komponenten Vektor darstellt.
-   Quelle1 ist ein Quell Register, das eine 3 x 2-Matrix darstellt, die dem ersten von 2 aufeinander folgenden Registern entspricht.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x2                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Die XY-Maske ist für das Ziel Register erforderlich. Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.

Die folgenden Gleichungen zeigen die Funktionsweise der Anweisung:


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
```



Der Eingabe Vektor befindet sich im Register src0. Die 3 x 2-Eingabe Matrix befindet sich in Register Quelle1 und das nächste höhere Register in derselben Register Datei, wie in der folgenden Erweiterung gezeigt. Ein 2D-Ergebnis wird erzeugt, wobei die anderen Elemente des Ziel Registers (dest. z und dest. w) nicht betroffen sind.

Dieser Vorgang wird häufig für 2D-Transformationen verwendet. Diese Anweisung wird als Paar von Punkt Produkten implementiert, wie hier gezeigt.


```
m3x2   r0.xy, r1, c0   which will be expanded to:

dp3   r0.x, r1, c0
dp3   r0.y, r1, c1
```



Die Modifizierern "Swizzle" und "Negation" sind für das Quelle1 Register ungültig. Das DST-und src0-Register oder eine beliebige Registrierung von Quelle1 + i dürfen nicht identisch sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




