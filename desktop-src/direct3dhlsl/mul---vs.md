---
title: mul – vs
description: Multipliziert Quellen mit dem Ziel. | mul – vs
ms.assetid: 0b048cc2-b165-418f-893e-6dee28ca5ad3
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d14603f077ddc61287d8d22580b161b59ddf8c6b67dad62141ecf4afb44d1f04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023760"
---
# <a name="mul---vs"></a>mul – vs

Multipliziert Quellen mit dem Ziel.

## <a name="syntax"></a>Syntax



| mul dst, src0, src1 |
|---------------------|



 

where

-   dst ist das Zielregister.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| mul                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Codefragment zeigt die ausgeführten Vorgänge.


```
dest.x = src0.x * src1.x;
dest.y = src0.y * src1.y;
dest.z = src0.z * src1.z;
dest.w = src0.w * src1.w;
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




