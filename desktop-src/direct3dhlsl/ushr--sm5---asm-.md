---
title: ushr (SM5-ASM)
description: Nach rechts verschieben. | ushr (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981688"
---
# <a name="ushr-sm5---asm"></a>ushr (SM5-ASM)

Nach rechts verschieben.



| ubfe dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\] |
|--------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] enthält die Ergebnisse der-Anweisung.<br/>                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] den 32-Bit-Werten, die verschoben werden sollen.<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[\]Geben Sie in den lsb 5 Bits die Anzahl der zu Verschiebungs enden Bits (0-31) an.<br/> |



 

Diese Anweisung führt eine Komponenten Weise Verschiebung jedes 32-Bit-Werts in *src0* rechts durch eine ganzzahlige Bitzahl ohne Vorzeichen aus, die von der LSB 5 Bits (0-31 Range) in *Quelle1* bereitgestellt wird, wobei 0 eingefügt wird. Das 32-Bit pro Komponenten Ergebnis wird in *dest* platziert.

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

 

 





