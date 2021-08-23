---
title: logp – vs
description: Logp mit partieller Genauigkeit₂(x).
ms.assetid: 8547ca8a-7bde-4e41-9e65-f7fcd65454c1
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3c33242ec23070a78e8adee159d35c19121dcc7c3dfe2c013c3d00adceb16477
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119043778"
---
# <a name="logp---vs"></a>logp – vs

Logp mit partieller Genauigkeit₂(x).

## <a name="syntax"></a>Syntax



| logp dst, src |
|---------------|



 

where

-   dst ist das Zielregister.
-   src ist ein Quellregister. Das Quellregister erfordert die explizite Verwendung von "replicate swizzle", d.h. genau eine der .x-, .y-, .z-, .w swizzle-Komponenten (oder die Entsprechungen .r, .g, .b, .a) muss angegeben werden.

## <a name="remarks"></a>Hinweise



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|------|-------|------|-------|
| logp                   | x    | x    | x    | x     | x    | x     |



 

Das folgende Codefragment zeigt die ausgeführten Vorgänge.


```
float f = abs(src);
if (f != 0)
    dest.x = dest.y = dest.z = dest.w = (float)(log(f)/log(2));
else
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;   
```



Diese Anweisung bietet logarithm base 2 partielle Genauigkeit, bis zu 10 Bits.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shader-Anweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




