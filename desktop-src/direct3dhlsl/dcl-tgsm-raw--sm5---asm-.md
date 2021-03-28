---
title: dcl_tgsm_raw (SM5-ASM)
description: Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Compute-Shader s-Thread Gruppe verfügbar ist.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103719464"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a>DCL \_ TGSM \_ RAW (SM5-ASM)

Deklarieren Sie einen Verweis auf einen Bereich des freigegebenen Speicherplatzes, der für die Compute-Shader s-Thread Gruppe verfügbar ist.



| DCL \_ TGSM \_ RAW g \# , byteCount |
|-------------------------------|



 



| Element                                                                                                       | BESCHREIBUNG                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*selbst\#*<br/>                                                 | \[in \] einem Verweis auf einen Block der Größe *byteCount* des nicht typisierten freigegebenen Speichers. <br/> |
| <span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*<br/> | \[in \] muss ein Vielfaches von 4 sein. <br/>                                             |



 

## <a name="remarks"></a>Bemerkungen

Der Gesamtspeicher für alle g \# muss <= der pro Thread Gruppe verfügbare freigegebene Arbeitsspeicher (32 KB) sein.

In einem Extremfall können Sie 8192 Gesamt-g s deklarieren \# , jeweils mit einem *byteCount* von 4.

Im umgekehrten Extremfall können Sie ein einzelnes g \# mit einem *byteCount* von 32768 deklarieren.

> [!Note]  
> CS \_ 4 \_ 0 und CS \_ 4 \_ 1 unterstützen die [strukturierte DCL- \_ TGSM \_](dcl-tgsm-structured--sm5---asm-.md), aber nicht die **DCL- \_ TGSM- \_ Rohdaten**.

 

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

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

 

 





