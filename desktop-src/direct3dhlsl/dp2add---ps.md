---
title: dp2add-PS
description: Führt ein 2D-Punktprodukt und eine skalare Addition aus.
ms.assetid: 4226ee34-2e68-4536-b171-68f3b967182e
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88d3d28cc64bdb7caa1b7456e87711c3dbee2b13
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104101070"
---
# <a name="dp2add---ps"></a>dp2add-PS

Führt ein 2D-Punktprodukt und eine skalare Addition aus.

## <a name="syntax"></a>Syntax


```
dp2add dst, src0, src1, src2.{x|y|z|w}
```



Hierbei gilt:

-   DST ist ein Ziel Register.
-   src0, Quelle1 und Quelle2 sind drei Quell Register.
-   {x \| y \| z \| w} ist das erforderliche Replizieren von Replizieren auf Quelle2.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp2add                |      |      |      |      | x    | x    | x     | x    | x     |



 

Der Skalarwert für Add wird durch das Replizieren von Replizieren auf Quelle2 ausgewählt.

Der folgende Code Ausschnitt zeigt die ausgeführten Vorgänge.


```
dest = src0.r * src1.r + src0.g * src1.g + src2.replicate_swizzle
// The scalar result is replicated to the write mask components
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




