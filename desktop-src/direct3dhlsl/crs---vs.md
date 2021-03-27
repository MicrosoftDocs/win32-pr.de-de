---
title: CRS-vs
description: Berechnet ein Kreuz Produkt mit der rechten Regel. | CRS-vs
ms.assetid: 102108f5-acc8-49ce-a84b-b8060decbaa7
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: fee30fab91b4f491efd4311919245ec2cb98b555
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352559"
---
# <a name="crs---vs"></a>CRS-vs

Berechnet ein Kreuz Produkt mit der rechten Regel.

## <a name="syntax"></a>Syntax



| CRS DST, src0, Quelle1 |
|---------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| Renn                    |      | x    | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie hier gezeigt.


```
dest.x = src0.y * src1.z - src0.z * src1.y;
dest.y = src0.z * src1.x - src0.x * src1.z;
dest.z = src0.x * src1.y - src0.y * src1.x;
```



Einige Einschränkungen bei der Verwendung:

-   src0 darf nicht mit dem registrierten Register identisch sein.
-   Quelle1 darf nicht mit dem registrierten Register identisch sein.
-   src0 darf nicht über das standardswizzle (. xyzw) verfügen.
-   Quelle1 darf nicht über das standardswizzle (. xyzw) verfügen.
-   dest muss genau eine der folgenden sieben Masken haben:. x \| . y \| . z \| . XY \| . XZ \| . YZ \| . xyz.
-   dest muss ein temporäres Register sein.
-   "dest" darf nicht identisch mit "src0" oder "Quelle1" sein.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




