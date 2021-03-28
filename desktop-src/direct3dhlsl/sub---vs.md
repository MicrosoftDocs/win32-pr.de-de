---
title: Sub-vs
description: Subtrahiert Quellen. | Sub-vs
ms.assetid: ccd7ca57-05a9-4ee8-8bda-c8c875476aaf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a4bf15522798e1da5ec0bde5b729f241ff9dabde
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961423"
---
# <a name="sub---vs"></a>Sub-vs

Subtrahiert Quellen.

## <a name="syntax"></a>Syntax



| Sub DST, src0, Quelle1 |
|---------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| sub                    | x    | x    | x    | x     | x    | x     |



 

Diese Anweisung führt die Subtraktion aus, die in dieser Formel angezeigt wird.


```
dest.x = src0.x - src1.x
dest.y = src0.y - src1.y
dest.z = src0.z - src1.z
dest.w = src0.w - src1.w
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




