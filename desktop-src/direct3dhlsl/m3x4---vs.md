---
title: m3x4 – im Vergleich
description: Multipliziert einen 3-Komponenten-Vektor mit einer 3x4-Matrix. | m3x4 – im Vergleich
ms.assetid: 8bec1ac5-376b-4eae-ba82-b42a6c0e7c4e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 54137f2081a48158d306e882eab0dc912a8e50332b7d66cfb137c3c10b669570
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119457430"
---
# <a name="m3x4---vs"></a>m3x4 – im Vergleich

Multipliziert einen 3-Komponenten-Vektor mit einer 3x4-Matrix.

## <a name="syntax"></a>Syntax



| m3x4 dst, src0, src1 |
|----------------------|



 

where

-   dst ist das Zielregister. Das Ergebnis ist ein 4-Komponenten-Vektor.
-   src0 ist ein Quellregister, das einen 3-Komponenten-Vektor darstellt.
-   src1 ist ein Quellregister, das eine 3x4-Matrix darstellt, die dem ersten von vier aufeinanderfolgenden Registern entspricht.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| m3x4                   | x    | x    | x    | x     | x    | x     |



 

Die Xyzw-Maske (Standardmaske) ist für das Zielregister erforderlich. Negate- und swizzle-Modifizierer sind für src0, aber nicht für src1 zulässig.

Das folgende Codefragment zeigt die ausgeführten Vorgänge.


```
 
dest.x = (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
dest.y = (src0.x * src2.x) + (src0.y * src2.y) + (src0.z * src2.z);
dest.z = (src0.x * src3.x) + (src0.y * src3.y) + (src0.z * src3.z);
dest.w = (src0.x * src4.x) + (src0.y * src4.y) + (src0.z * src4.z);
```



Der Eingabevektor befindet sich im Register src0. Die Eingabematrix 3x4 befindet sich im Register src1 und die nächsten drei höheren Register, wie in der folgenden Erweiterung gezeigt.

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

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




