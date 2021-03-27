---
title: FRC-PS
description: Gibt den Bruchteil der einzelnen Eingabe Komponenten zurück. | FRC-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353418"
---
# <a name="frc---ps"></a>FRC-PS

Gibt den Bruchteil der einzelnen Eingabe Komponenten zurück.

## <a name="syntax"></a>Syntax



| FRC-DST, src |
|--------------|



 

where

-   DST ist das Ziel Register.
-   src ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| FRC                   |      |      |      |      | x    | x    | x     | x    | x     |



 

Der folgende Code Ausschnitt zeigt konzeptionell, wie die Anweisung funktioniert.


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



Die Floor-Funktion konvertiert das Argument, das an die größte Ganzzahl, die kleiner oder gleich dem Argument ist, an die größte Ganzzahl. Diese wird in einen float-Wert konvertiert und dann den ursprünglichen Wert von Abbildung subtrahiert. Der resultierende Bruch Wert liegt zwischen 0,0 und 1,0.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




