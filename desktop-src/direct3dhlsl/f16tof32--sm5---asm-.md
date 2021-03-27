---
title: f16tof32 (SM5-ASM)
description: Konvertierung von Komponenten weiser float16 zu float32. | f16tof32 (SM5-ASM)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53af1f2eab1f50dfded820bf27b2cda8f23e6b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104981536"
---
# <a name="f16tof32-sm5---asm"></a>f16tof32 (SM5-ASM)

Konvertierung von Komponenten weiser float16 zu float32.



| f16tof32 dest \[ . mask \] , \[ - \] src \[ . Swizzle\] |
|----------------------------------------------|



 



| Element                                                            | BESCHREIBUNG                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] der Adresse des float32-Ergebnisses.<br/> |
| <span id="src"></span><span id="SRC"></span>*src*<br/>    | \[im \] float16-Wert, der konvertiert werden soll.<br/>      |



 

## <a name="remarks"></a>Bemerkungen

Mit diesem Vorgang wird eine Komponenten Weise Konvertierung eines float16-Werts von lsb-Bits in ein float32-Ergebnis durchführt.

Dieser Vorgang folgt den D3D-Regeln für die Gleit Komma Konvertierung.

Verwenden Sie diese Anweisung für die Shader-gesteuerte datenentkomprimierung.

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

 

 





