---
title: dcl_stream (sm5 – asm)
description: Deklarieren Sie einen Geometry Shader-Ausgabestream.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f53b8226cc9a4d8d2bd980cd26371f9e7b46a5168ec61ff39e425f73a4d7193c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118793041"
---
# <a name="dcl_stream-sm5---asm"></a>dcl \_ stream (sm5 – asm)

Deklarieren Sie einen Geometry Shader-Ausgabestream.



| dcl \_ stream m\# |
|-----------------|



 



| Element                                                       | Beschreibung                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*M\#*<br/> | \[in \] Stream 0..3 (m0.. m3).<br/> |



 

## <a name="remarks"></a>Hinweise

Ein angegebener Stream kann nur einmal deklariert werden.

Wenn keine Streams deklariert werden, wird davon ausgegangen, dass Ausgabe- und Ausgabetopologiedeklarationen für Stream 0 gelten.

Der erste **\_ dcl-Stream** kann nach keiner **\_ dcl-Ausgabe** oder **dcl \_ outputTopology-Anweisungen** angezeigt werden.

Alle **\_ dcl-Ausgabe-** oder **\_ dCL-OutputToptex-Anweisungen** nach einer **dcl \_ stream** m-Anweisung \# definieren die Ausgaben für Stream \# m.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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

 

 





