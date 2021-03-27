---
title: ABS-vs
description: Berechnet den absoluten Wert. | ABS-vs
ms.assetid: d3b4cf06-dc87-4c71-aa2d-5ade4cf98caa
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 07667954de97e2a1da3999237930fb33796d9030
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219128"
---
# <a name="abs---vs"></a>ABS-vs

Berechnet den absoluten Wert.

## <a name="syntax"></a>Syntax



|              |
|--------------|
| ABS DST, src |



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



|                        |      |      |      |       |      |       |
|------------------------|------|------|------|-------|------|-------|
| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
| abs                    |      | x    | x    | x     | x    | x     |



 

Diese Anweisung funktioniert wie hier gezeigt.


```
dest.x = abs(src.x)
dest.y = abs(src.y)
dest.z = abs(src.z)
dest.w = abs(src.w)
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




