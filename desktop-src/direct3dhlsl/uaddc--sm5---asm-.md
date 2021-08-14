---
title: uaddc (sm5 – asm)
description: Eine ganze Zahl ohne Vorzeichen wird mit carry hinzugefügt.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f649ed68626e5b3351ee1b3c7d5848c8e42f7ec175b4b76c929571056f48e0c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117722188"
---
# <a name="uaddc-sm5---asm"></a>uaddc (sm5 – asm)

Eine ganze Zahl ohne Vorzeichen wird mit carry hinzugefügt.



| uaddc dest0 \[ .mask \] , dest1 \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                               | BESCHREIBUNG                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in \] Adresse des Ergebnisses.<br/>               |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in \] 1, wenn carry erzeugt wird. andernfalls 0.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[in \] einem hinzuzufügenden 32-Bit-Operanden.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[in \] einem hinzuzufügenden 32-Bit-Operanden.<br/>          |



 

## <a name="remarks"></a>Hinweise

*dest1* kann NULL sein, wenn die Übertragung nicht benötigt wird.

Verwenden Sie diese Anweisung für Arithmetik mit hoher Genauigkeit.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Diese Anweisung wird in den folgenden Shadermodellen unterstützt:



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | nein        |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





