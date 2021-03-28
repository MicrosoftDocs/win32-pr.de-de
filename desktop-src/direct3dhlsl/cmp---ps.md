---
title: CMP-PS
description: Wählen Sie Quelle1 if src0 0 aus. Andernfalls wählen Sie Quelle2 aus. Der Vergleich erfolgt pro Kanal.
ms.assetid: 8fabd548-3f5e-4b78-bf1e-16e4f1548ccd
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: da3da1062d02e995876a1f67e5c4e19518774760
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104038329"
---
# <a name="cmp---ps"></a>CMP-PS

Wählen Sie Quelle1, wenn src0 >= 0 aus. Andernfalls wählen Sie Quelle2 aus. Der Vergleich erfolgt pro Kanal.

## <a name="syntax"></a>Syntax



| CMP DST, src0, Quelle1, Quelle2 |
|---------------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.
-   Quelle2 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| CMP                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

Für die Versionen 1 \_ 2 und 1 3 gelten einige zusätzliche Einschränkungen \_ :

-   Jeder Shader kann bis zu maximal drei CMP-Anweisungen verwenden.
-   Das Ziel Register darf nicht mit einem der Quell Register identisch sein.

In diesem Beispiel wird ein Vergleich mit vier Kanälen durchführt.


```
ps_1_4
def c0, -0.6, 0.6, 0, 0.6
def c1  0,0,0,0
def c2  1,1,1,1

mov r1, c1
mov r2, c2

cmp r0, c0, r1, r2   // r0 is assigned 1,0,0,0 based on the following:

// r0.x = c2.x because c0.x < 0
// r0.y = c1.y because c0.y >= 0
// r0.z = c1.z because c0.z >= 0
// r0.w = c1.w because c0.w >= 0
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




