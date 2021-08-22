---
title: f16tof32 (sm5 - asm)
description: Komponentenweise Konvertierung von float16 in float32. | f16tof32 (sm5 - asm)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc4456737d5ddaaed351ae2a1cc76418c33af9c498e725099e1912d8fabe7ce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119562651"
---
# <a name="f16tof32-sm5---asm"></a>f16tof32 (sm5 - asm)

Komponentenweise Konvertierung von float16 in float32.



| f16tof32 dest \[ .mask \] , \[ - \] src \[ .swizzle\] |
|----------------------------------------------|



 



| Element                                                            | Beschreibung                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Die Adresse des float32-Ergebnisses.<br/> |
| <span id="src"></span><span id="SRC"></span>*Src*<br/>    | \[in \] Der zu konvertierende float16-Wert.<br/>      |



 

## <a name="remarks"></a>Hinweise

Dieser Vorgang führt eine komponentenbezogene Konvertierung eines float16-Werts von LSB-Bits in ein float32-Ergebnis aus.

Dieser Vorgang folgt D3D-Regeln für die Gleitkommakonvertierung.

Verwenden Sie diese Anweisung für die shadergesteuerte Datendekomprimierung.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
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

 

 





