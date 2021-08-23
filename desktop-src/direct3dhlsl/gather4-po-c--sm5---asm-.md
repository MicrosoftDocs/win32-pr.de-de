---
title: gather4_po_c (sm5 – asm)
description: Verhält sich genauso wie gather4 \_ po, führt jedoch einen Vergleich auf Texel aus, ähnlich wie in Beispiel \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83342aed97663c027b0915f612b13b288192d937d29d364257004cfc8966aec9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119743870"
---
# <a name="gather4_po_c-sm5---asm"></a>gather4 \_ po \_ c (sm5 - asm)

Verhält sich wie [**gather4 \_ po,**](gather4-po--sm5---asm-.md)mit dem Unterschied, dass einen Vergleich auf Texel durchführt, ähnlich wie [**bei Beispiel \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ po \_ c dest \[ .mask , \] srcAddress \[ .swizzle \] , srcOffset \[ .swizzle \] , srcResource \[ .swizzle \] , srcSampler \[ . R \] , srcReferenceValue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                       | Beschreibung                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/>                                                                            | \[in \] Die Adresse des Ergebnisses des Vorgangs.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcAddress*<br/>                             | \[in \] Eine Gruppe von Texturkoordinaten.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*Srcoffset*<br/>                                 | \[in \] Der Offset.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/>                         | \[in \] einem Texturregister.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcSampler*<br/>                             | \[in \] einem Samplerregister.<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srcReferenceValue*<br/> | \[in \] Einzelne Komponente ausgewählt.<br/>                  |



 

## <a name="remarks"></a>Hinweise

In [**Beispiel \_ c**](sample-c--sm4---asm-.md) finden Sie Informationen dazu, wie *srcReferenceValue* mit jedem abgerufenen Texel verglichen wird. Im Gegensatz zu **Beispiel \_ c** gibt *gather4 \_ po \_ c* jedes Vergleichsergebnis zurück, anstatt sie zu filtern.

Diese Anweisung funktioniert wie **gather4 \_ po** nur mit 2D-Texturen. Dies ist im Gegensatz zu [**gather4 \_ c**](gather4-c--sm5---asm-.md), das auch mit TextureCubes funktioniert.

Bei Formaten mit float32-Komponenten wird der abgerufene Wert normalisiert oder +-INF im Vergleichsvorgang unverändert verwendet. NaN wird im Vergleichsvorgang als NaN verwendet, aber die genaue Bitdarstellung des NaN kann geändert werden. Denormen werden in den Vergleich auf 0 (null) geleert. Für TextureCubes muss eine Synthese des fehlenden 4. Texels an Ecken auftreten, sodass das Konzept der unveränderten Rückgabe von Bits für das synthetisierte Texel nicht zutrifft.

Für **gather4 \_ po \_ c** unterstützte Formate sind identisch mit denen, die für Beispiel **\_ c** unterstützt werden. Dies sind Einzelkomponentenformate, daher die . R auf srcSampler anstelle einer beliebigen Swizzle.

**gather4 \_ po \_ c** für eine ungebundene Ressource gibt 0 zurück.

Verwenden Sie diese Methode zum Filtern von Schattenkarten.

Diese Anweisung gilt für die folgenden Shaderstufen:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
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

 

 





