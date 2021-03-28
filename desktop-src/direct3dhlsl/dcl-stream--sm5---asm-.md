---
title: dcl_stream (SM5-ASM)
description: Deklarieren eines Geometry-shaderausgabestreams.
ms.assetid: 0A8B8AB5-B7B0-46BB-91E8-B2E8E3D64B74
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f46903c3257c280788e91c25700743a23c146fe
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389593"
---
# <a name="dcl_stream-sm5---asm"></a>DCL \_ -Stream (SM5-ASM)

Deklarieren eines Geometry-shaderausgabestreams.



| DCL- \_ Stream m\# |
|-----------------|



 



| Element                                                       | BESCHREIBUNG                             |
|------------------------------------------------------------|-----------------------------------------|
| <span id="m_"></span><span id="M_"></span>*800\#*<br/> | \[in \] Stream 0.. 3 (M0... m3).<br/> |



 

## <a name="remarks"></a>Bemerkungen

Ein angegebener Datenstrom kann nur einmal deklariert werden.

Wenn keine Streams deklariert werden, wird angenommen, dass die Deklarationen der Ausgabe-und Ausgabe Topologie für Stream 0 gelten.

Der erste **DCL- \_ Stream** darf nicht nach einer **DCL- \_ Ausgabe** oder **DCL \_ outputtopology** -Anweisungen stehen.

Alle **DCL \_** -Ausgaben oder **DCL \_ outputtoplogie** -Anweisungen nach jeder **DCL \_ Stream** m- \# Anweisung definieren die Ausgaben für Stream m \# .

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        | X        |       |         |



 

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



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





