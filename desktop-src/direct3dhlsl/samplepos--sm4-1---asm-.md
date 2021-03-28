---
title: samplepos (SM 4.1-ASM)
description: Fragt die Position eines Beispiels in einer angegebenen shaderressourcenansicht oder im Rasterizer ab.
ms.assetid: 5A53B342-3A1D-4016-ABF2-CA6236D562C9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 910a542dafddb8b855e218f8702c746220780d6e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389583"
---
# <a name="samplepos-sm41---asm"></a>samplepos (SM 4.1-ASM)

Fragt die Position eines Beispiels in einer angegebenen shaderressourcenansicht oder im Rasterizer ab.



| samplepos dest \[ . mask \] , srkresource \[ . Swizzle \] , sampleindex (skalare Operand) |
|--------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] der Shader-Ressource.<br/>                         |
| <span id="sampleIndex"></span><span id="sampleindex"></span><span id="SAMPLEINDEX"></span>*Sample Index*<br/> | \[im \] Index des Beispiels.<br/>                     |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung gibt die 2D-Beispiel Position von Sample *sampleindex* für die angegebene Ressource zurück. Dies gilt nur für Ressourcen, die mit [**ld2dms**](ld2dms--sm4-1---asm-.md) geladen werden können, es sei denn, der Raster ist als *srcresource* angegeben.

*srkresource* kann ein t- \# Register (eine Shader-Ressourcen Ansicht) oder ein Raster-Register sein.

Die Anweisung berechnet den Gleit Komma Vektor (XPosition, YPosition, 0, 0).

Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden. Die Beispiel Position ist relativ zum Mittelpunkt des Pixels, basierend auf dem Pixelkoordinaten System.

Wenn *sampleingedex* außerhalb des gültigen Bereichs liegt, wird ein Vektor NULL zurückgegeben. Wenn keine Ressource an den angegebenen Slot gebunden ist, wird 0 zurückgegeben.

**samplepos** können für Dinge wie benutzerdefinierte aufgelösten Elemente in Shader-Code verwendet werden.

Diese Anweisung gilt für die folgenden Shader-Phasen:



| Vertexshader | Geometrie-Shader | Pixelshader |
|---------------|-----------------|--------------|
|               |                 | x            |



 

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

 

 





