---
title: dcl_uav_raw (SM5-ASM)
description: Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader. | dcl_uav_raw (SM5-ASM)
ms.assetid: D0F43FF8-FF1C-4E42-AF42-F528C98FD680
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f47614d5a9327f2d686a36db6bfe4afeb653788
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995454"
---
# <a name="dcl_uav_raw-sm5---asm"></a>DCL \_ UAV \_ RAW (SM5-ASM)

Deklarieren Sie eine ungeordnete Zugriffs Ansicht (UAV) für die Verwendung durch einen Shader.



| DCL \_ UAV \_ RAW \[ \_ GLC \] dstuav |
|-------------------------------|



 



| Element                                                                                           | BESCHREIBUNG                |
|------------------------------------------------------------------------------------------------|----------------------------|
| <span id="dstUAV"></span><span id="dstuav"></span><span id="DSTUAV"></span>*dstuav*<br/> | \[in \] der UAV.<br/> |



 

## <a name="remarks"></a>Bemerkungen

*dstuav* ist ein u- \# Register, das als Verweis auf eine unorderedaccessview eines Puffers deklariert wird, wobei der Puffer als einfaches 1D-Array von nicht typisierten 32-Bit-Einträgen angezeigt wird.

Für den Arbeitsspeicher ausgeführte Vorgänge können die Daten implizit als Typ interpretieren.

Das \_ GLC-Flag bedeutet "Global kohärent". Das Fehlen von \_ GLC bedeutet, dass die UAV im COMPUTE-Shader nur als "zusammenhängender Gruppe" oder "lokal kohärent" in einem einzelnen Pixelshader-Aufruf deklariert wird.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          | X     | X       |



 

Da UAVs in allen Shader-Phasen für Direct3D 11,1 verfügbar sind, gilt diese Anweisung für alle Shader-Phasen für die Direct3D 11,1-Laufzeit, die ab Windows 8 verfügbar ist.



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Anweisung wird in den folgenden shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

> [!Note]  
> Diese Anweisung wird in CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützt.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





