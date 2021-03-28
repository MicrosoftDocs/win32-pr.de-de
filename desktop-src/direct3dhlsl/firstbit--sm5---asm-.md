---
title: firstbit (SM5-ASM)
description: Sucht das erste Bit, das in einer Zahl festgelegt ist, entweder von der LSB oder von MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104313746"
---
# <a name="firstbit-sm5---asm"></a>firstbit (SM5-ASM)

Sucht das erste Bit, das in einer Zahl festgelegt ist, entweder von der LSB oder von MSB.



| firstbit { \_ Hi \|\_Siehe|\_Shi} dest \[ . mask \] , src0 \[ . Swizzle\] |
|-------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[an \] der ganzzahligen Position des ersten Bits, das in *src0* beginnt, beginnend mit dem LSB für firstbit \_ Lo oder MSB für firstbit \_ Hi.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Eingabe Ganzzahl.<br/>                                                                                                  |



 

## <a name="remarks"></a>Bemerkungen

Mit diesem Vorgang wird die ganzzahlige Position des ersten Bits in der 32-Bit-Eingabe ab dem LSB für firstbit \_ Lo oder MSB für firstbit Hi zurückgegeben \_ . Beispielsweise gibt firstbit \_ Lo on 0x00000001 den Wert 0 zurück. firstbit \_ HI auf 0x10000000 gibt 3 zurück.

firstbit \_ Shi (s für signed) gibt das erste 0 aus dem MSB zurück, wenn die Zahl negativ ist. andernfalls wird die erste 1 vom MSB zurückgegeben.

Alle Varianten der Anweisung geben ~ 0 (0xFFFFFFFF in 32-Bit-Register) zurück, wenn keine Entsprechung gefunden wird.

Verwenden Sie diese Anweisung, um in einem Bitfeld schnell festgelegte Bits aufzulisten oder die größte Potenz von 2 in einer Zahl zu ermitteln.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="mimimum-shader-model"></a>Imies Shader-Modell

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

 

 





