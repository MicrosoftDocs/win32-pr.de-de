---
title: LRP-vs
description: Interpoliert linear zwischen dem zweiten und dritten Quell Register durch einen im ersten Quell Register angegebenen Anteil. | LRP-vs
ms.assetid: 8438bcf3-9b00-4963-b2a3-54fd1c345961
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 485d7720dc2c71ee599db93d179de8e665bfab77
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995567"
---
# <a name="lrp---vs"></a>LRP-vs

Interpoliert linear zwischen dem zweiten und dritten Quell Register durch einen im ersten Quell Register angegebenen Anteil.

## <a name="syntax"></a>Syntax



| LRP DST, src0, Quelle1, Quelle2 |
|---------------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.
-   Quelle2 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| startet                    |      | x    | x    | x     | x    | x     |



 

Diese Anweisung führt die lineare interpolung basierend auf der folgenden Formel aus.


```
dest.x = src0.x * (src1.x - src2.x) + src2.x;
dest.y = src0.y * (src1.y - src2.y) + src2.y;
dest.z = src0.z * (src1.z - src2.z) + src2.z;
dest.w = src0.w * (src1.w - src2.w) + src2.w;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




