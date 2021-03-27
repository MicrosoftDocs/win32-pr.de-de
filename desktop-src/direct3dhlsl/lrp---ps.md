---
title: LRP-PS
description: Interpoliert linear zwischen dem zweiten und dritten Quell Register durch einen im ersten Quell Register angegebenen Anteil. | LRP-PS
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: aec1ac23cc6c86f768d435e4c8169117c1bbe899
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050816"
---
# <a name="lrp---ps"></a>LRP-PS

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



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| startet                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Diese Anweisung führt die lineare interpolung basierend auf der folgenden Formel aus.


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




