---
title: DP3-PS
description: Berechnet das 3-Komponenten-Punktprodukt der Quell Register. | DP3-PS
ms.assetid: a365acd1-89c0-4340-8f51-8e478f84ddc0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 09e4178f6aedbfb5242f4c545d624f1d07796008
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981408"
---
# <a name="dp3---ps"></a>DP3-PS

Berechnet das 3-Komponenten-Punktprodukt der Quell Register.

## <a name="syntax"></a>Syntax



| DP3 DST, src0, Quelle1 |
|---------------------|



 

where

-   DST ist das Ziel Register.
-   src0 ist ein Quell Register.
-   Quelle1 ist ein Quell Register.

## <a name="remarks"></a>Bemerkungen



| Pixel-Shader-Versionen | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| dp3                   | x    | x    | x    | x    | x    | x    | x     | x    | x     |



 

Der folgende Code Ausschnitt zeigt die Vorgänge, die ausgeführt werden:


```
dest.x = dest.y = dest.z = dest.w = 
  (src0.x * src1.x) + (src0.y * src1.y) + (src0.z * src1.z);
```



Diese Anweisung wird in der Vektor Pipeline ausgeführt und schreibt immer in die Farbkanäle. Bei Version 1 \_ 4 verwendet diese Anweisung weiterhin die Vektor Pipeline, kann jedoch in beliebige Kanäle schreiben.

Eine Anweisung mit einer Ziel Register. RGB-Schreib Maske (. XYZ) kann mit DP3, wie unten gezeigt, zusammengestellt werden.


```
dp3 r0.rgb, t0, v0            // Copy scalar result to color components
+mov r2.a, t0                 // Copy alpha component from t0 in parallel 
```



Die DP3-Anweisung kann mithilfe des Quell Registrierungs-Modifizierers für [signierte Skalierung](dx9-graphics-reference-asm-ps-registers-modifiers-signed-scale.md) ( \_ bx2) geändert werden, wenn Sie nicht bereits in einen dynamischen Bereich mit Vorzeichen erweitert wurden. Bei einem Beleuchtungs-Shader wird der Bezeichner für die bearbeitungsanweisungsmodifizierer ( \_ Sat) häufig verwendet, um die negativen Werte an schwarz zu binden, wie im folgenden Beispiel gezeigt.


```
dp3_sat r0, t0_bx2, v0_bx2    // t0 is a bump map, v0 contains the light direction
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Pixelshaderanweisungen](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




