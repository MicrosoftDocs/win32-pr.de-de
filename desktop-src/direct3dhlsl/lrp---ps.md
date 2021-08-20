---
title: lrp – ps
description: Interpoliert linear zwischen dem zweiten und dritten Quellregister um einen Im ersten Quellregister angegebenen Anteil. | lrp – ps
ms.assetid: b360f28e-cb2a-4403-a020-180524df6549
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 716cbdd5492f768885b8dd91dca5a17f72c4ba50897274c2d6e11f340f563394
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117906870"
---
# <a name="lrp---ps"></a>lrp – ps

Interpoliert linear zwischen dem zweiten und dritten Quellregister um einen Im ersten Quellregister angegebenen Anteil.

## <a name="syntax"></a>Syntax



| lrp dst, src0, src1, src2 |
|---------------------------|



 

where

-   dst ist das Zielregister.
-   src0 ist ein Quellregister.
-   src1 ist ein Quellregister.
-   src2 ist ein Quellregister.

## <a name="remarks"></a>Hinweise



| Pixel-Shaderversionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| Lrp                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Diese Anweisung führt die lineare Interpolation basierend auf der folgenden Formel aus.


```
 
dest = src0 * src1 + (1-src0) * src2
// which is the same as
dest = src2 + src0 * (src1 - src2)
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anweisungen für Pixel-Shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




