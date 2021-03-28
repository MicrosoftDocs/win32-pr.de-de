---
title: FRC-vs
description: Gibt den Bruchteil der einzelnen Eingabe Komponenten zurück. | FRC-vs
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353409"
---
# <a name="frc---vs"></a>FRC-vs

Gibt den Bruchteil der einzelnen Eingabe Komponenten zurück.

## <a name="syntax"></a>Syntax



| FRC-DST, src |
|--------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Vertex-Shader-Versionen | 1\_1 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|------------------------|------|------|------|-------|------|-------|
| FRC                    | x    | x    | x    | x     | x    | x     |



 

Das folgende Code Fragment zeigt konzeptionell, wie die Anweisung funktioniert.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



Die Floor-Funktion konvertiert das Argument, das an die größte Ganzzahl, die kleiner oder gleich dem Argument ist, an die größte Ganzzahl. Diese wird in einen float-Wert konvertiert und dann den ursprünglichen Wert von Abbildung subtrahiert. Der resultierende Bruch Wert liegt zwischen 0,0 und 1,0.

Bei Version 1 \_ 1 sind die zulässigen Schreib Masken. y und. XY (. x ist nicht zulässig).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-shaderanweisungen](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




