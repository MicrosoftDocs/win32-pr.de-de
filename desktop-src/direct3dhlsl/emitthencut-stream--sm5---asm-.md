---
title: emitThenCut_stream (sm5 – asm)
description: Entspricht einem Emit-Befehl gefolgt von einem Ausschneidebefehl. | emitThenCut_stream (sm5 – asm)
ms.assetid: E9D84647-E29B-4E31-9E95-9F7A173293D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 522d2be28ae1d63617b8ba775f8f8839c270668aeeded8a4944ef9ae7554d598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120067960"
---
# <a name="emitthencut_stream-sm5---asm"></a>emitThenCut-Stream \_ (sm5 – asm)

Entspricht einem [Emit-Befehl](emit--sm4---asm-.md) gefolgt von einem [Ausschneidebefehl.](cut--sm4---asm-.md)



| emitThenCut \_ stream streamIndex |
|---------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                         |
|--------------------------------------------------------------------------------------------------------------------|-------------------------------------|
| <span id="streamIndex"></span><span id="streamindex"></span><span id="STREAMINDEX"></span>*streamIndex*<br/> | \[in \] Der Streamindex.<br/> |



 

## <a name="remarks"></a>Hinweise

Dieser Vorgang ist nützlich, wenn sie wissentlich den letzten Scheitelpunkt in einer Topologie ausgibt.

Wenn Streams nicht deklariert wurden, müssen Sie [emitThenCut](emitthencut--sm4---asm-.md) anstelle des **emitThenCut-Streams \_** verwenden.

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

 

 





