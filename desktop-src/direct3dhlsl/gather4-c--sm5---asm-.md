---
title: gather4_c (sm5 – asm)
description: Identisch mit gather4, mit der Ausnahme, dass diese Eindringung einen Vergleich auf Texel durchführt, ähnlich wie bei Beispiel \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b300e27743d08f3bbdf813de200b5a749a4ac25f16ab10458968731b9918c493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488690"
---
# <a name="gather4_c-sm5---asm"></a>gather4 \_ c (sm5 - asm)

Identisch mit [**gather4,**](gather4--sm5---asm-.md)mit ausnahme dieser Eindringung führt einen Vergleich auf Texel durch, ähnlich wie [**in Beispiel \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ c \[ \_ aoffimmi(u,v) \] dest \[ .mask , \] srcAddress \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler \[ . R \] , srcReferenceValue |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                       | Beschreibung                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/>                                    |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] Eine Gruppe von Texturkoordinaten.<br/>                                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] einem Texturregister.<br/>                                                           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] einem Samplerregister.<br/>                                                           |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] Ein Register mit einer einzelnen ausgewählten Komponente, die im Vergleich verwendet wird.<br/> |



 

## <a name="remarks"></a>Hinweise

Im [**Beispiel \_ c**](sample-c--sm4---asm-.md) finden Sie eine Beschreibung, wie *srcReferenceValue* mit jedem abgerufenen Texel verglichen wird. Im Gegensatz zu **Beispiel \_ c** gibt **gather4 \_ c** jedes Vergleichsergebnis zurück, anstatt sie zu filtern.

Bei TextureCube-Ecken, bei denen es drei echte Texel gibt und ein viertes synthetisiert werden muss, muss die Synthese nach dem Vergleichsschritt erfolgen. Dies bedeutet, dass das zurückgegebene Vergleichsergebnis für das syntestische Texel 0, 0,33, 0,66 oder 1 sein kann. Einige Implementierungen geben möglicherweise nur 0 oder 1 für das synthetisierte Texel zurück. Abgesehen von dieser Auflistung möglicher Ergebnisse ist die Methode zum Synthetisieren des Texels nicht angegeben.

Bei Formaten mit float32-Komponenten wird der abgerufene Wert normalisiert oder +-INF im Vergleichsvorgang unverändert verwendet. NaN wird im Vergleichsvorgang als NaN verwendet, aber die genaue Bitdarstellung des NaN kann geändert werden. Denormen werden in den Vergleich auf 0 (null) geleert. Für TextureCubes muss eine Synthese des fehlenden 4. Texels an Ecken auftreten, sodass das Konzept der unveränderten Rückgabe von Bits für das synthetisierte Texel nicht zutrifft.

Für *gather4 \_ c* unterstützte Formate sind identisch mit denen, die für *Beispiel \_ c* unterstützt werden. Dies sind Einzelkomponentenformate, daher die . R auf *srcSampler* anstelle einer beliebigen Swizzle. **gather4 \_ c** für eine ungebundene Ressource gibt 0 zurück.

Verwenden Sie diese Anweisung für die benutzerdefinierte Filterung von Schattenkarten.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

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

[Shadermodell 5-Assembly (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





