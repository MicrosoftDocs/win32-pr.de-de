---
title: dmax (sm5 - asm)
description: Komponentenweiser Höchstwert mit doppelter Genauigkeit.
ms.assetid: 34ED8B34-2592-4BBB-BCF0-F2222E4D51D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6846da6fbf3ad5d42be5131322e1214fc49fe2627b824775798e4527de3d24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068370"
---
# <a name="dmax-sm5---asm"></a>dmax (sm5 - asm)

Komponentenweiser Höchstwert mit doppelter Genauigkeit.



| dmax \[ \_ sat \] dest \[ .mask \] , \[ - \] src0 \[ \_ abs \] \[ .swizzle \] , \[ - \] src1 abs \[ \_ \] \[ .swizzle\] |
|---------------------------------------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                                                                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> *dest*  =  *src0*  >=  *src1* ? *src0* : *src1*<br/> >= wird anstelle von > verwendet, sodass bei min(x,y) = x dann max(x,y) = y. <br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Der Wert, der mit *src1* verglichen werden soll.<br/>                                                                                                                                                           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Der Wert, der mit *src0* verglichen werden soll.<br/>                                                                                                                                                           |



 

## <a name="remarks"></a>Hinweise

NaN verfügt über eine spezielle Behandlung. Wenn ein Quelloperand NaN ist, wird der andere Quelloperand zurückgegeben. Die Auswahl erfolgt pro Komponente. Wenn beide NaN sind, wird eine beliebige NaN-Darstellung zurückgegeben.

Die gültigen Swizzles für die Quellparameter sind .xyzw, .xyxy, .zwxy, .zwzw. Gültige *Dest-Masken* sind .xy, .zw und .xyzw. Die folgenden *src-Zuordnungen* sind post-swizzle:

-   *dest* ist ein double vec2 across (x 32LSB, y 32MSB) und (z 32LSB, w 32MSB).
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

 

 





