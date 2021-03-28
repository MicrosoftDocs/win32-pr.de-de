---
title: uaddc (SM5-ASM)
description: Ganzzahl ohne Vorzeichen mit "Carry" hinzufügen.
ms.assetid: 1007253C-F920-4003-B266-D124A255F731
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f57f75be617e32c15212207110851520a7a281e2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104516484"
---
# <a name="uaddc-sm5---asm"></a>uaddc (SM5-ASM)

Ganzzahl ohne Vorzeichen mit "Carry" hinzufügen.



| uaddc dest0 \[ . mask \] , dest1 \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\] |
|--------------------------------------------------------------------------|



 



| Element                                                               | BESCHREIBUNG                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| <span id="dest0"></span><span id="DEST0"></span>*dest0*<br/> | \[\]die Adresse des Ergebnisses.<br/>               |
| <span id="dest1"></span><span id="DEST1"></span>*dest1*<br/> | \[in \] 1, wenn "Carry" erstellt wird. andernfalls 0.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>    | \[in \] 32-Bit-Operanden hinzugefügt werden.<br/>          |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/>    | \[in \] 32-Bit-Operanden hinzugefügt werden.<br/>          |



 

## <a name="remarks"></a>Bemerkungen

*dest1* kann NULL sein, wenn der Carry nicht benötigt wird.

Verwenden Sie diese Anweisung für Berechnungen mit hoher Genauigkeit.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





