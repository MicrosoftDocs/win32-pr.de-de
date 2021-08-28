---
title: crs – im Vergleich zu
description: Berechnet ein Kreuzprodukt mithilfe der rechten Regel. | crs – im Vergleich zu
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8b7db94bc3289fee461d8f24dd65798549124957b6bd3b886f1939d8b12c4609
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117908922"
---
# <a name="crs---vs"></a>crs – im Vergleich zu

Berechnet ein Kreuzprodukt mithilfe der rechten Regel.

## <a name="syntax"></a>Syntax



| crs dst, src0, src1 |
|---------------------|



 

where

-   dst ist das Zielregister.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Crs                    |      | x    | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie hier gezeigt.


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



Einige Einschränkungen bei der Verwendung:

-   src0 kann nicht dasselbe Register wie dest sein.
-   src1 kann nicht dasselbe Register wie dest sein.
-   src0 darf keinen anderen Swizzle als den Standard-Swizzle (.xyzw) haben.
-   src1 darf keinen anderen Swizzle als den Standard-Swizzle (.xyzw) haben.
-   dest muss genau eine der folgenden sieben Masken haben: .x \| .y \| .z \| .xy \| .xy \| .xz .yz \| .xyz.
-   dest muss ein temporäres Register sein.
-   dest darf nicht dasselbe Register wie src0 oder src1 sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




