---
title: sampleinfo (sm4.1 - asm)
description: Fragt die Anzahl der Stichproben in einer bestimmten Shaderressourcenansicht oder im Rasterizer ab.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2227afbf7a08a0010efc2efb8fcf87bae85c8f5775e596d92b761b556f8bfb93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118510468"
---
# <a name="sampleinfo-sm41---asm"></a>sampleinfo (sm4.1 - asm)

Fragt die Anzahl der Stichproben in einer bestimmten Shaderressourcenansicht oder im Rasterizer ab.



| \[\_uint \] dest \[ .mask \] , srcResource \[ .swizzle\] |
|---------------------------------------------------|



 



| Element                                                                                                               | Beschreibung                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                    | \[in \] Die Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[in \] Die Shaderressource.<br/>                         |



 

## <a name="remarks"></a>Hinweise

Diese Anweisung gibt die Anzahl der Stichproben für die bestimmte Ressource oder den Rasterizer zurück. Er ist nur für Ressourcen gültig, die mit [**ld2dms**](ld2dms--sm4-1---asm-.md) geladen werden können, es sei denn, der Rasterizer ist als *srcResource angegeben.* *srcResource kann* ein \# t-Register (eine Shaderressourcenansicht) oder ein Rasterizerregister sein.

Die Anweisung berechnet den Vektor (SampleCount,0,0,0).

Mit dem Swizzle auf *srcResource* können die zurückgegebenen Werte willkürlich überschwindelt werden, bevor sie in das Ziel geschrieben werden. Der zurückgegebene Wert ist ein Gleitkommawert, es sei denn, der uint-Modifizierer wird verwendet. In diesem Fall ist \_ der zurückgegebene Wert integer. Wenn keine Ressource an den angegebenen Slot gebunden ist, wird 0 zurückgegeben.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| X             | X               | w            |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Diese Funktion wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md)        | Ja       |
| [Shadermodell 4.1](dx-graphics-hlsl-sm4.md)              | Ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | Nein        |
| [Shadermodell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | Nein        |
| [Shadermodell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | Nein        |
| [Shadermodell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | Nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





