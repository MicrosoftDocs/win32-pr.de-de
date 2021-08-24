---
title: cnd – ps
description: Wählt basierend auf dem Vergleich src0 0.5 bedingt zwischen src1 und src2.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cb31c873bf3a4e38048f57d75a30cec70021716d2aab43b683cb29aef25f7f23
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726960"
---
# <a name="cnd---ps"></a>cnd – ps

Wählt basierend auf dem Vergleich src0 > 0.5 bedingt zwischen src1 und src2.

## <a name="syntax"></a>Syntax



| cnd dst, src0, src1, src2 |
|---------------------------|



 

where

-   dst ist das Zielregister.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.
-   src2 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Cnd                   | x    | x    | x    | x    |      |      |       |      |       |



 

Für die Versionen \_ 1 1 bis 1 \_ 3 muss src0 r0.a sein.


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



Diese Beispiele zeigen einen Vergleich mit vier Kanälen, der in einem Shader der Version \_ 1 4 durchgeführt wurde, sowie einen möglichen Einzelkanalvergleich in einem Shader der Version \_ 1 1.


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



Version \_ 1 1 bis 1 \_ 3 wird nur mit dem replizierten Alphakanal von r0 verglichen.


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



In diesem Beispiel werden die beiden Werte A und B verglichen. Im Beispiel wird davon ausgegangen, dass A in v0 und B in v1 geladen wird. Sowohl A als auch B müssen im Bereich von -1 bis +1 liegen, und da die Farbregister (vn) als zwischen 0 und 1 definiert sind, wird die Einschränkung in diesem Beispiel erfüllt.


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

 

 




