---
title: dne (sm5 - asm)
description: Komponentenweiser Vergleich mit doppelter Genauigkeit ohne Gleichheit.
ms.assetid: 7C69A86D-0820-4640-AF5A-2993EC77D2AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e95b86ea21aa55b3d9f13f414fb5c386c9719eee65bdd62aaea47fa38190a2b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986580"
---
# <a name="dne-sm5---asm"></a>dne (sm5 - asm)

Komponentenweiser Vergleich mit doppelter Genauigkeit ohne Gleichheit.



| dne \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle\] |
|--------------------------------------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die Komponenten, die mit *src1 verglichen werden.*<br/>      |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Komponenten, die mit *src0 verglichen werden.*<br/>      |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt den Gleitkommavergleich mit doppelter Genauigkeit (*src0* != *src1*) für jede Komponente aus und schreibt das Ergebnis in *dest.*

Wenn der Vergleich true ist, wird 32-Bit-0xFFFFFFFF für diese Komponente zurückgegeben. Andernfalls wird 0x00000000 32-Bit-Verschlüsselung zurückgegeben.

Der Vergleich mit NaN gibt true zurück.

Die *gültigen Dest-Masken* sind eine oder zwei Komponenten. Das heißt: .x, .y, .z, .w, .xy, .xz, .xw, .yz, .yw, .zw Die erste *Destkomponente* in der Maske empfängt das 32-Bit-Ergebnis für den ersten doppelten Vergleich. Die zweite Komponente in der Maske empfängt, falls vorhanden, das 32-Bit-Ergebnis für den zweiten doppelten Vergleich.

Die gültigen Swizzles für die Quellparameter sind .xyzw, .xyxy, .zwxy, .zwzw. Die folgenden *src-Zuordnungen* sind post swizzle:

-   *src0* ist eine doppelte Vec2 zwischen (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).
-   *src1* ist ein double-vec2 zwischen (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

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

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





