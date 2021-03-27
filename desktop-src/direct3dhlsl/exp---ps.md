---
title: Exp-PS
description: Bietet eine exponentielle vollständige Genauigkeit (2X). | Exp-PS
ms.assetid: 09e4446f-4149-4ec8-b3e3-2045b55bd591
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acd7c50c1f0d6ff08ee5d66e50fdd3e56939f0d9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050756"
---
# <a name="exp---ps"></a>Exp-PS

Bietet eine exponentielle vollständige Genauigkeit 2<sup>x</sup>.

## <a name="syntax"></a>Syntax



| Exp DST, src |
|--------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register. Das Quell Register erfordert die explizite Verwendung von "replizieren". Das heißt, es muss genau eine der x-, y-,. z-, w. w-, d. h. die. r-,. g-,. b-,. a-Entsprechungen) angegeben werden. Weitere Informationen finden Sie unter [Quellen Register: schwenken](dx9-graphics-reference-asm-ps-registers-modifiers-source-register-swizzling.md).

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| exp                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Der folgende Code Ausschnitt zeigt die Vorgänge, die ausgeführt werden:


```
dest.x = dest.y = dest.z = dest.w = (float)pow(2, src.replicateSwizzleComponent);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




