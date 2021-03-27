---
title: Log-vs
description: Protokoll der vollständigen Genauigkeit (x). | Log-vs
ms.assetid: 53c91825-ec54-4b04-bf08-52d4b1c5122d
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9e0564ab5b38943017e61bde171d0db3060ca0c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219276"
---
# <a name="log---vs"></a>Log-vs

Protokoll der vollständigen Genauigkeit (x).

## <a name="syntax"></a>Syntax



| Log DST, src |
|--------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register. Das Quell Register erfordert die explizite Verwendung von replizierten Strichen, d. h. genau einer der x-, y-,. z-,. w-Swizzle-Komponenten (oder r,. g,. b,. a-äquivalente) muss angegeben werden.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| log                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Code Fragment zeigt die ausgeführten Vorgänge.


```
float v = abs(src);
if (v != 0)
{
    dest.x = dest.y = dest.z = dest.w = 
        (float)(log(v)/log(2));  
}
else
{
    dest.x = dest.y = dest.z = dest.w = -FLT_MAX;
}
```



Diese Anweisung akzeptiert eine skalare Quelle, deren Signier Bit ignoriert wird. Das Ergebnis wird in alle vier Kanäle repliziert.

Diese Anweisung stellt 21 Bits Genauigkeit bereit.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




