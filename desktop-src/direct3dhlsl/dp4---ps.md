---
title: DP4-PS
description: Berechnet das vier-Komponenten-Punktprodukt der Quell Register. | DP4-PS
ms.assetid: 83ef6097-cacf-4498-842b-3eb03e57bd6f
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2562259af164b8680d54e9a120abaa405fd781c5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050772"
---
# <a name="dp4---ps"></a>DP4-PS

Berechnet das vier-Komponenten-Punktprodukt der Quell Register.

## <a name="syntax"></a>Syntax



| DP4 DST, src0, Quelle1 |
|---------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp4                   |      | x    | x    | x    | x    | x    | x     | x    | x     |



 

Der folgende Code Ausschnitt zeigt die Vorgänge, die ausgeführt werden:


```
dest.x = dest.y = dest.z = dest.w = 
    (src0.x * src1.x) + (src0.y * src1.y) + 
    (src0.z * src1.z) + (src0.w * src1.w);
```



Einschränkungen für PS \_ 1 \_ 2 und PS \_ 1 \_ 3:

-   Jeder Shader kann bis zu maximal vier DP4-Anweisungen verwenden.
-   Jede DP4-Anweisung zählt als zwei arithmetische Anweisungen.

Einschränkungen für 1 \_ X-Versionen:

-   Diese Anweisung kann nicht gemeinsam ausgestellt werden, da DP4 sowohl in der Vektor-als auch in der Alpha Pipeline ausgeführt wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




