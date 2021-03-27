---
title: emitThenCut_stream (SM5-ASM)
description: Entspricht einem Ausgabe Befehl gefolgt von einem Befehl zum Ausschneiden. | emitThenCut_stream (SM5-ASM)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ae3129f2a3fb50664a5dbf070c7a1dae9bf5d6e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981209"
---
# <a name="emitthencut_stream-sm5---asm"></a>emitthenausschneide Daten \_ Strom (SM5-ASM)

Entspricht einem Ausgabe [Befehl gefolgt von einem Befehl zum](emit--sm4---asm-.md) [Ausschneiden](cut--sm4---asm-.md) .



| emitthencut \_ Stream streamindex |
|---------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[im \] Stream-Index.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Dieser Vorgang ist nützlich, wenn der letzte Scheitelpunkt in einer Topologie wissentlich ausgegeben wird.

Wenn Streams nicht deklariert wurden, müssen Sie [emitthencut](emitthencut--sm4---asm-.md) anstelle des **emitthencut- \_ Streams** verwenden.

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

 

 





