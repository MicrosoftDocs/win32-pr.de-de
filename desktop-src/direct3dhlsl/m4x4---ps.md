---
title: M4x4-PS
description: Multipliziert einen 4-Komponenten Vektor mit einer 4 x 4-Matrix. | M4x4-PS
ms.assetid: 2a9915a3-f396-4108-97f7-d70c5262ff59
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 93f2da73c45151f5287f3acf773efb4bd57d21e1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981528"
---
# <a name="m4x4---ps"></a>M4x4-PS

Multipliziert einen 4-Komponenten Vektor mit einer 4 x 4-Matrix.

## <a name="syntax"></a>Syntax



| M4x4 DST, src0, Quelle1 |
|----------------------|



 

where

-   DST ist das Ziel Register. Das Ergebnis ist ein Vektor mit 4 Komponenten.
-   src0 ist ein Quell Register, das einen 4-Komponenten Vektor darstellt.
-   Quelle1 ist ein Quell Register, das eine 4X4-Matrix darstellt, die dem ersten von vier aufeinander folgenden Registern entspricht.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m4x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Die xyzw-Maske (Standard) ist für das Ziel Register erforderlich. Negate-und Swizzle-Modifizierern sind für src0, aber nicht für Quelle1 zulässig.

Die Modifizierern "Swizzle" und "Negation" sind für das src0 Register ungültig. Die DST-und src0-Register dürfen nicht identisch sein.

Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.


```
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z) + (src0.w*src1.w);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z) + (src0.w*src2.w);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z) + (src0.w*src3.w);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z) + (src0.w*src4.w);
```



Der Eingabe Vektor befindet sich im Register src0. Die Eingabe 4X4-Matrix befindet sich in Register Quelle1 und die nächsten drei höheren Register, wie in der folgenden Erweiterung gezeigt.

Dieser Vorgang wird häufig verwendet, um eine Position durch eine Projektions Matrix zu transformieren. Diese Anweisung wird als Satz von Punkt Produkten implementiert, wie hier gezeigt.


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

 

 




