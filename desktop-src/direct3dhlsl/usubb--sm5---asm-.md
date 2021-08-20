---
title: usubb (sm5 - asm)
description: Ganze Zahl ohne Vorzeichen wird mit borrow subtrahiert.
ms.assetid: 6D42E3CA-5A37-4194-AB42-7A2337C5AB9D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c2f70f39729f5245f7044945e9d3b233ec4f0893be27c5143f5c55989693b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721824"
---
# <a name="usubb-sm5---asm"></a>usubb (sm5 - asm)

Ganze Zahl ohne Vorzeichen wird mit borrow subtrahiert.



| usubb dest0 \[ .mask \] , dest1 \[ .mask \] , src0 \[ .swizzle \] , src1 \[ .swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                               | Beschreibung                                                                                       |
|--------------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[in \] Enthält die LSAB-Ergebnisse der Anweisung.<br/>                                   |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in \] Die entsprechende Komponente von *dest0,* die angibt, ob ein Kredit erstellt wurde.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[in \] Der Wert, von dem subtrahiert werden soll.<br/>                                               |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>    | \[in \] Der Betrag, der von *src0 subtrahiert werden soll.*<br/>                                             |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung führt einen komponentenweisen Subtrahieren von 32-Bit-Operanden *src1* von *src0* aus und platziert den LSB-Teil des 32-Bit-Ergebnisses in *dest0.*

Die entsprechende Komponente in *dest1 wird* mit 1 geschrieben, wenn ein Kredit erstellt wird, andernfalls 0.

*dest1 kann* NULL sein, wenn der Kredit nicht benötigt wird.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

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

 

 





