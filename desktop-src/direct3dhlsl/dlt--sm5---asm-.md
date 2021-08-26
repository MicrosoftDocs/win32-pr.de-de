---
title: dlt (sm5 – asm)
description: Komponentenweiser Kleiner-als-Vergleich mit doppelter Genauigkeit.
ms.assetid: A9DE5007-4ADD-403D-A2B7-EAE475E9DCCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 957037c5168299959e580cbc2ffda100bdac96bdb4fbd9f90242ffa53c416367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120024670"
---
# <a name="dlt-sm5---asm"></a>dlt (sm5 – asm)

Komponentenweiser Kleiner-als-Vergleich mit doppelter Genauigkeit.



| dlt \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten, die mit *src1* verglichen werden sollen.<br/>         |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Komponenten, die mit *src0* verglichen werden sollen.<br/>         |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt den Gleitkommavergleich mit doppelter Genauigkeit (*src0*  <  *src1*) für jede Komponente aus und schreibt das Ergebnis in *dest*.

Wenn der Vergleich true ist, wird 32-Bit-0xFFFFFFFF für diese Komponente zurückgegeben. Andernfalls wird 32-Bit-0x00000000 zurückgegeben.

Der Vergleich mit NaN gibt FALSE zurück.

Die gültigen *Destmasken* sind eine oder zwei Komponenten. Das heißt: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw Die erste *Dest-Komponente* in der Maske empfängt das 32-Bit-Ergebnis für den ersten doppelten Vergleich. Die zweite Komponente in der Maske (sofern vorhanden) empfängt das 32-Bit-Ergebnis für den zweiten doppelten Vergleich.

Die gültigen Swizzles für die Quellparameter sind .xyzw, .xyxy, .zwxy, .zwzw. Die folgenden *src-Zuordnungen* sind post-swizzle:

-   *src0* ist ein double vec2 across (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).
-   *src1* ist ein double vec2 across (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





