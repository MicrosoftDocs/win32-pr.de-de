---
title: dcl_uav_raw (sm5 - asm)
description: Deklarieren Sie eine ungeordnete Zugriffsansicht (UAV) für die Verwendung durch einen Shader. | dcl_uav_raw (sm5 - asm)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2b7af99a1747d23d6269ffc1b7199fb142277b46e73bfd822d31fd4b0fbf3e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986690"
---
# <a name="dcl_uav_raw-sm5---asm"></a>dcl \_ uav \_ raw (sm5 - asm)

Deklarieren Sie eine ungeordnete Zugriffsansicht (UAV) für die Verwendung durch einen Shader.



| dcl \_ uav \_ raw \[ \_ glc \] dstUAV |
|-------------------------------|



 



| Element                                                                                           | BESCHREIBUNG                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstUAV*<br/> | \[im \] UAV.<br/> |



 

## <a name="remarks"></a>Hinweise

*dstUAV* ist ein U-Register, das als Verweis auf eine UnorderedAccessView eines Puffers deklariert ist, wobei der Puffer als einfaches 1D-Array von nicht typisierten \# 32-Bit-Einträgen angezeigt wird.

Vorgänge, die für den Arbeitsspeicher ausgeführt werden, interpretieren die Daten möglicherweise implizit so, als ob sie einen Typ haben.

Das \_ glc-Flag bedeutet "global zusammenhängende". Das Fehlen von glc bedeutet, dass die UAV im Compute-Shader nur als "gruppenreigent" oder bei einem Aufruf eines Einzelnen Pixel-Shaders \_ als "lokal zusammenhängend" deklariert wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shaderstufen für Direct3D 11.1 verfügbar sind, gilt diese Anweisung für alle Shaderstufen für die Direct3D 11.1-Runtime, die ab Windows 8.



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

> [!Note]  
> Diese Anweisung wird in cs \_ 4 \_ 0 und cs \_ 4 \_ 1 unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





