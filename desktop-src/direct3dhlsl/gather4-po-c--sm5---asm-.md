---
title: gather4_po_c (SM5-ASM)
description: Verhält sich wie gather4 \_ Po, außer führt einen Vergleich von Texels aus, ähnlich wie in Beispiel \_ c.
ms.assetid: B128EEF3-3440-4F00-9792-20FB1AE075E9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36b07dcad08b4d117a453a3c97e461e6b9b4cab6
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104389571"
---
# <a name="gather4_po_c-sm5---asm"></a>gather4 \_ po \_ c (SM5-ASM)

Verhält sich wie [**gather4 \_ po**](gather4-po--sm5---asm-.md), außer führt einen Vergleich von Texels aus, ähnlich wie in [**Beispiel \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ po \_ c dest \[ . mask \] , srcaddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler \[ . R \] , srkreferencevalue |
|-------------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                       | BESCHREIBUNG                                                   |
|--------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>                             | \[in \] einem Satz von Texturkoordinaten.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>                                 | \[im \] Offset.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/>                         | \[in \] einem Textur Register.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>                             | \[in \] einem Samplerregister.<br/>                         |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srkreferencevalue*<br/> | \[in \] einer einzelnen Komponente ausgewählt.<br/>                  |



 

## <a name="remarks"></a>Bemerkungen

In [**Beispiel \_ c**](sample-c--sm4---asm-.md) finden Sie Informationen dazu, wie *srkreferencevalue* mit den abgerufenen textsabgerufenen verglichen wird. Im Gegensatz zum **Beispiel \_ c** gibt *gather4 \_ po \_ c* die einzelnen Vergleichsergebnisse zurück, anstatt Sie zu filtern.

Diese Anweisung, wie z. b. **gather4 \_ po**, funktioniert nur mit 2D-Texturen. Dies unterscheidet sich von [**gather4 \_ c**](gather4-c--sm5---asm-.md), das auch mit texturecubes funktioniert.

Bei Formaten mit float32-Komponenten wird der Wert, der abgerufen wird, normalisiert, oder +-INF, im Vergleichs Vorgang unverändert verwendet. NaN wird in der Vergleichsoperation als NaN verwendet, aber die genaue Bitdarstellung des Nan kann geändert werden. Denorms werden in den Vergleich auf NULL geleert. Bei texturecubes muss eine Synthese der fehlenden 4. textextteile in Ecken vorkommen, sodass das Konzept der Rückgabe von Bits, die für die synthetische Texttyp unverändert sind, nicht zutrifft.

Die für **gather4 \_ po \_ c** unterstützten Formate sind identisch mit denen, die für **Beispiel \_ c** unterstützt werden. Dabei handelt es sich um Einzelkomponenten Formate und somit um. R auf srcsampler, anstelle eines beliebigen flüchtigen.

**gather4 \_ po \_ c** für eine ungebundene Ressource gibt 0 (null) zurück.

Verwenden Sie diese Methode zum Filtern von schattenkarten.

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

 

 





