---
title: ishl (sm5 - asm)
description: Umschalten nach links. | ishl (sm5 - asm)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6908d12824c5aa84e04db38fb2462031bb2ae4a198700f98938456ecbd8619a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854210"
---
# <a name="ishl-sm5---asm"></a>ishl (sm5 - asm)

Umschalten nach links.



| ishl dest \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|--------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in \] Enthält die Ergebnisse der Verschiebung.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die zu verschiebenden 32-Bit-Werte.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] Die Anzahl der zu verschiebenden Bits.<br/>        |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt eine komponentenbezogene Verschiebung jedes 32-Bit-Werts in *src0* durch, der von einer ganzzahligen Bitanzahl ohne Vorzeichen, die von den LSB-5-Bits (0-31-Bereich) in *src1* bereitgestellt wird, und fügt 0 ein. Die 32-Bit-Ergebnisse pro Komponente werden in *dest* platziert.

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

 

 





