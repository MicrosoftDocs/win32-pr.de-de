---
title: m3x4 – ps
description: Multipliziert einen 3-Komponenten-Vektor mit einer 3x4-Matrix. | m3x4 – ps
ms.assetid: b749d3cd-2acf-450c-94f2-fea5e1c8f4d2
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 21c7f5ed65531e4022f503acf1b2ca994c860894824b2614220e16d36743d52b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067930"
---
# <a name="m3x4---ps"></a>m3x4 – ps

Multipliziert einen 3-Komponenten-Vektor mit einer 3x4-Matrix.

## <a name="syntax"></a>Syntax



| m3x4 dst, src0, src1 |
|----------------------|



 

where

-   dst ist das Zielregister. Das Ergebnis ist ein 4-Komponenten-Vektor.
-   src0 ist ein Quellregister, das einen 3-Komponenten-Vektor darstellt.
-   src1 ist ein Quellregister, das eine 3x4-Matrix darstellt, die dem ersten von vier aufeinanderfolgenden Registern entspricht.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| m3x4                  |      |      |      |      | x    | x    | x     | x    | x     |



 

Die Xyzw-Maske (Standardmaske) ist für das Zielregister erforderlich. Negate- und swizzle-Modifizierer sind für src0, aber nicht für src1 zulässig.

Der folgende Codeausschnitt zeigt die ausgeführten Vorgänge.


```
 
dest.x = (src0.x*src1.x) + (src0.y*src1.y) + (src0.z*src1.z);
dest.y = (src0.x*src2.x) + (src0.y*src2.y) + (src0.z*src2.z);
dest.z = (src0.x*src3.x) + (src0.y*src3.y) + (src0.z*src3.z);
dest.w = (src0.x*src4.x) + (src0.y*src4.y) + (src0.z*src4.z);
```



Der Eingabevektor befindet sich im Register src0. Die Eingabematrix 3x4 befindet sich im Register src1 und die nächsten beiden höheren Register, wie in der folgenden Erweiterung gezeigt.

Dieser Vorgang wird häufig zum Transformieren eines Positionsvektors durch eine Matrix verwendet, die einen projektiven Effekt hat, aber keine Übersetzung anwendet. Diese Anweisung wird wie hier gezeigt als Paar von Punktprodukten implementiert.


```
m3x4   r0.xyzw, r1, c0   will be expanded to: 

dp3 r0.x, r1, c0
dp3 r0.y, r1, c1
dp3 r0.z, r1, c2
dp3 r0.w, r1, c3
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




