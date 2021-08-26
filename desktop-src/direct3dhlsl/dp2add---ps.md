---
title: dp2add – ps
description: Führt ein 2D-Punktprodukt und eine skalare Addition aus.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 39a7cd640de57f2f69c8ee3b46ee6be6e52cbb16f9db39ef902725241d77b9c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068360"
---
# <a name="dp2add---ps"></a>dp2add – ps

Führt ein 2D-Punktprodukt und eine skalare Addition aus.

## <a name="syntax"></a>Syntax


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



Hierbei gilt:

-   dst ist ein Zielregister.
-   src0, src1 und src2 sind drei Quellregister.
-   {x \| y \| z \| w} ist die erforderliche Replizieren von Swizzle auf src2.

## <a name="remarks"></a>Hinweise



| Pixelshaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

Der Skalarwert für add wird von der Replizieren-Swizzle auf src2 ausgewählt.

Der folgende Codeausschnitt zeigt die ausgeführten Vorgänge.


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




