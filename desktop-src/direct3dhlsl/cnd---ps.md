---
title: CND-PS
description: Wählt bedingt zwischen Quelle1 und Quelle2 basierend auf dem Vergleich src0 0,5 aus.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1fd3a14e2ac4bd283a4e67724fbb42ac965ea707
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101082"
---
# <a name="cnd---ps"></a>CND-PS

Wählt bedingt zwischen Quelle1 und Quelle2 basierend auf dem Vergleich src0 > 0,5 aus.

## <a name="syntax"></a>Syntax



| CND DST, src0, Quelle1, Quelle2 |
|---------------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.
-   Quelle2 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| CND                   | x    | x    | x    | x    |      |      |       |      |       |



 

Für die Versionen 1 \_ 1 bis 1 \_ 3 muss src0 r0. a lauten.


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



Version 1 \_ 4 vergleicht jeden Kanal separat.


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



Diese Beispiele zeigen einen Vergleich mit vier Kanälen, der in einem Shader der Version 1 \_ 4 ausgeführt wird, sowie einen Vergleich mit einem einzelnen Kanal, der in einem Shader der Version 1 1 möglich ist \_ .


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



Version 1 \_ 1 bis 1 \_ 3 vergleicht nur mit dem replizierten Alphakanal von r0.


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



In diesem Beispiel werden zwei Werte verglichen: A und B. Im Beispiel wird davon ausgegangen, dass ein in V0 geladen und B in v1 geladen wird. A und B müssen im Bereich von-1 bis + 1 liegen, und da die Farbregister (VN) zwischen 0 und 1 liegen, wird die Einschränkung in diesem Beispiel erfüllt.


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




