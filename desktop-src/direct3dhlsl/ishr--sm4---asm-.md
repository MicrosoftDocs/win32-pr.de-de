---
title: ISHR (SM4-ASM)
description: Arithmetische UMSCHALT Rechte (Zeichen Erweiterung). | ISHR (SM4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104995733"
---
# <a name="ishr-sm4---asm"></a>ISHR (SM4-ASM)

Arithmetische UMSCHALT Rechte (Zeichen Erweiterung).



| ISHR dest \[ . mask \] , src0 \[ . Swizzle \] , Quelle1. Select- \_ Komponente |
|--------------------------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] enthält das Ergebnis des Vorgangs.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] enthält den Wert, der verschoben werden soll.<br/>     |
| <span id="src1"></span><span id="SRC1"></span>*Quelle1*<br/> | \[in \] enthält die UMSCHALT Menge.<br/>            |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine Komponenten Weise arithmetische Verschiebung jedes 32-Bit-Werts in *src0* rechts durch eine ganzzahlige Bitzahl ohne Vorzeichen aus, die von der LSB 5 Bits (0-31 Range) in Quelle1 bereitgestellt wird *. Wählen Sie \_ Component* aus, und replizieren Sie den Wert von Bit 31. Das 32-Bit pro Komponenten Ergebnis wird in *dest* platziert. Die Anzahl ist ein Skalarwert, der auf alle Komponenten angewendet wird.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | ja       |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





