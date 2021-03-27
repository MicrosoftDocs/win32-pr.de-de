---
title: sampleinfo (SM 4.1-ASM)
description: Fragt die Anzahl der Stichproben in einer angegebenen shaderressourcenansicht oder im Rasterizer ab.
ms.assetid: 1F0968D7-01E9-4213-9F83-172B88374C3C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d307dbc8c79618a6401737874a9f6e060a899ccc
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103857812"
---
# <a name="sampleinfo-sm41---asm"></a>sampleinfo (SM 4.1-ASM)

Fragt die Anzahl der Stichproben in einer angegebenen shaderressourcenansicht oder im Rasterizer ab.



| \[\_uint \] dest \[ . mask \] , srkresource \[ . Swizzle\] |
|---------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] der Shader-Ressource.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung gibt die Anzahl von Stichproben für die angegebene Ressource oder den Rasterizer zurück. Dies gilt nur für Ressourcen, die mit [**ld2dms**](ld2dms--sm4-1---asm-.md) geladen werden können, es sei denn, der Raster ist als *srcresource* angegeben. *srkresource* kann ein t- \# Register (eine Shader-Ressourcen Ansicht) oder ein Raster-Register sein.

Die Anweisung berechnet den Vektor (samplecount, 0, 0, 0).

Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden. Der zurückgegebene Wert ist ein Gleit Komma Wert, es sei denn \_ , der uint-Modifizierer wird verwendet. in diesem Fall ist der zurückgegebene Wert Integer. Wenn keine Ressource an den angegebenen Slot gebunden ist, wird 0 zurückgegeben.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
| X             | X               | w            |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Diese Funktion wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                              | Unterstützt |
|-----------------------------------------------------------|-----------|
| [Shader-Modell 5](d3d11-graphics-reference-sm5.md)        | ja       |
| [Shadermodell 4,1](dx-graphics-hlsl-sm4.md)              | ja       |
| [Shadermodell 4](dx-graphics-hlsl-sm4.md)                | nein        |
| [Shader-Modell 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | nein        |
| [Shader-Modell 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | nein        |
| [Shader-Modell 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | nein        |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 4-Assembly (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





