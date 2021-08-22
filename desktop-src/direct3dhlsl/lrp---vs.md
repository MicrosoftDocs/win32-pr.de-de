---
title: lrp – vergleicht
description: Interpoliert linear zwischen dem zweiten und dritten Quellregister um einen Anteil, der im ersten Quellregister angegeben ist. | lrp – vergleicht
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d154f78b3e8ae5d3b7b8e553435d962ad3dbea9fe86f8dd772bf165c5eb542be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119184"
---
# <a name="lrp---vs"></a>lrp – vergleicht

Interpoliert linear zwischen dem zweiten und dritten Quellregister um einen Anteil, der im ersten Quellregister angegeben ist.

## <a name="syntax"></a>Syntax



| lrp dst, src0, src1, src2 |
|---------------------------|



 

where

-   dst ist das Zielregister.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.
-   src2 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| Lrp                    |      | x    | x    | x     | x    | x     |



 

Diese Anweisung führt die lineare Interpolation basierend auf der folgenden Formel aus.


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




