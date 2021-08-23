---
title: firstbit (sm5 - asm)
description: Sucht das erste Bit, das in einer Zahl festgelegt ist, entweder von LSB oder MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ea47c8e0674db5dc0349e5d6a8a041fa7d3623e6578eee542edeb1749577d7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511944"
---
# <a name="firstbit-sm5---asm"></a>firstbit (sm5 - asm)

Sucht das erste Bit, das in einer Zahl festgelegt ist, entweder von LSB oder MSB.



| firstbit{ \_ hi\|\_lo\|\_shi} dest \[ .mask \] , src0 \[ .swizzle\] |
|-------------------------------------------------------------|



 



| Element                                                            | Beschreibung                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[in Die ganzzahlige Position des ersten in src0 festgelegten Bits, beginnend mit \] der LSB für firstbit lo oder  \_ MSB für firstbit \_ hi.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] Die ganzzahlige Eingabe.<br/>                                                                                                  |



 

## <a name="remarks"></a>Hinweise

Dieser Vorgang gibt die ganzzahlige Position des ersten in der 32-Bit-Eingabe festgelegten Bits zurück, beginnend mit LSB für firstbit \_ lo oder MSB für firstbit \_ hi. Beispielsweise gibt firstbit \_ lo auf 0x00000001 0 zurück. firstbit \_ hi on 0x10000000 gibt 3 zurück.

firstbit shi (s für signed) gibt die erste 0 aus dem MSB zurück, wenn die Zahl negativ ist. Andernfalls wird die erste 1 vom \_ MSB zurückgegeben.

Alle Varianten der Anweisung geben ~0 zurück (0xffffffff 32-Bit-Register), wenn keine Übereinstimmung gefunden wird.

Verwenden Sie diese Anweisung, um die festgelegten Bits in einem Bitfeld schnell aufzählen oder die größte Leistung von 2 in einer Zahl zu finden.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="mimimum-shader-model"></a>Mimimum-Shadermodell

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

[Shader Model 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





