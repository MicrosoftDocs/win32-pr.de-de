---
title: emitThenCut (sm4 – asm)
description: Entspricht einem Emit-Befehl gefolgt von einem Ausschneidebefehl. | emitThenCut (sm4 – asm)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab83fa3eca853a75dca74ef32116e3d13da2dbe76f34fa407f9b0d5f2459d66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023860"
---
# <a name="emitthencut-sm4---asm"></a>emitThenCut (sm4 – asm)

Entspricht einem [Emit-Befehl](emit--sm4---asm-.md) gefolgt von einem [Ausschneidebefehl.](cut--sm4---asm-.md)



| emitThenCut |
|-------------|



 

## <a name="remarks"></a>Hinweise

Dieser Befehl ist nützlich, wenn Sie wissentlich den letzten Scheitelpunkt in einer Topologie ausgeben.

Wenn Streams deklariert wurden, müssen Sie [emitthencut \_ stream](emitthencut-stream--sm5---asm-.md)verwenden.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               | x               |              |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Ja       |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




