---
title: ISHR (SM5-ASM)
description: Arithmetische UMSCHALT Rechte (Zeichen Erweiterung). | ISHR (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995728"
---
# <a name="ishr-sm5---asm"></a>ISHR (SM5-ASM)

Arithmetische UMSCHALT Rechte (Zeichen Erweiterung).



| ishl dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1 \[ . Swizzle\] |
|--------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] enthält die Ergebnisse der Verschiebung.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] der Anzahl von Bits, die verschoben werden sollen.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] den 32-Bit-Werten, die verschoben werden sollen.<br/>        |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine Komponenten Weise arithmetische Verschiebung jedes 32-Bit-Werts in *src0* rechts durch eine ganzzahlige Bitzahl ohne Vorzeichen aus, die von der LSB 5 Bits (0-31 Range) in *Quelle1* bereitgestellt wird, wobei der Wert von Bit 31 replizieren wird. Das 32-Bit pro Komponenten Ergebnis wird in *dest* platziert.

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

 

 





