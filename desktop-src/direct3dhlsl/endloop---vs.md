---
title: ENDLOOP-vs
description: Ende einer Schleife... ENDLOOP-Block.
ms.assetid: fd7df120-a927-4a66-b152-6ce5247446e4
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8a9aec4d1b2c5237a87fae2c0beab4e8d995db97
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389486"
---
# <a name="endloop---vs"></a>ENDLOOP-vs

Ende einer [Schleife](loop---vs.md)... ENDLOOP-Block.

## <a name="syntax"></a>Syntax



| ENDLOOP |
|---------|



 

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| ENDLOOP                |      | x    | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie hier gezeigt.


```
LoopCounter += LoopStep;
LoopInterationCount = LoopIterationCount - 1;
if (LoopIterationCount > 0)
    Continue execution at the StartLoopOffset
```



ENDLOOP muss der letzten Anweisung eines [Schleifen-vs-](loop---vs.md) Blocks folgen.

## <a name="example"></a>Beispiel


```
loop aL, i3
    add r1, r0, c2[ aL ]
endloop
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




