---
title: f32tof16 (SM5-ASM)
description: Konvertierung von Komponenten weiser float16 zu float32. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104982030"
---
# <a name="f32tof16-sm5---asm"></a>f32tof16 (SM5-ASM)

Konvertierung von Komponenten weiser float16 zu float32.



| f32tof16 dest \[ . mask \] , \[ - \] src \[ . Swizzle\] |
|----------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des float16-Ergebnisses.<br/> |
| <span id="src"></span><span id="SRC"></span>*src*<br/>    | \[im \] float32-Wert, der konvertiert werden soll.<br/>  |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung führt eine Komponenten Weise Konvertierung eines float32-Werts in ein float16-Wert Ergebnis in den lsb-16-Bit-Wert aus.

Diese Anweisung folgt den D3D-Regeln für die Gleit Komma Konvertierung.

Verwenden Sie diese Anweisung für die Shader-gesteuerte Datenkomprimierung.

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

 

 





