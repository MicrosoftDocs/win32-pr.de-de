---
title: gather4_c (SM5-ASM)
description: Identisch mit gather4, mit dem Unterschied, dass diese instrumention einen Vergleich mit texeln ausführt, ähnlich wie in Beispiel \_ c.
ms.assetid: 6265151A-36CE-4D31-B7B2-233CEEBDCF87
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35414aa2cd4d9f0686ab7a5cc17b94caa960cec1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104993135"
---
# <a name="gather4_c-sm5---asm"></a>gather4 \_ c (SM5-ASM)

Identisch mit [**gather4**](gather4--sm5---asm-.md), mit dem Unterschied, dass diese instrumention einen Vergleich mit texeln ausführt, ähnlich wie in [**Beispiel \_ c**](sample-c--sm4---asm-.md).



| gather4 \_ c \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler \[ . R \] , srkreferencevalue |
|-----------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                                                       | BESCHREIBUNG                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                                            | \[in \] der Adresse des Vorgangs Ergebnisses<br/>                                    |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>                             | \[in \] einem Satz von Texturkoordinaten.<br/>                                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/>                         | \[in \] einem Textur Register.<br/>                                                           |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>                             | \[in \] einem Samplerregister.<br/>                                                           |
| <span id="srcReferenceValue"></span><span id="srcreferencevalue"></span><span id="SRCREFERENCEVALUE"></span>*srkreferencevalue*<br/> | \[in \] einem Register, bei dem eine einzelne Komponente ausgewählt ist, die im Vergleich verwendet wird.<br/> |



 

## <a name="remarks"></a>Bemerkungen

In [**Beispiel \_ c**](sample-c--sm4---asm-.md) finden Sie eine Beschreibung der Art und Weise, wie *srkreferencevalue* mit jedem abgerufenen texaus verglichen wird. Im Gegensatz zum **Beispiel \_ c** gibt **gather4 \_ c** alle Vergleichsergebnisse zurück, anstatt Sie zu filtern.

Bei texturecube-Ecken, in denen es drei echte texeln gibt und ein viertes synthetisiert werden muss, muss die Synthese nach dem Vergleichs Schritt erfolgen. Dies bedeutet, dass das zurückgegebene Vergleichs Ergebnis für den textegroßen Textwert 0, 0,33, 0,66 oder 1 sein kann. Einige Implementierungen geben möglicherweise nur 0 oder 1 für den Textem Textem aus. Abgesehen von dieser Auflistung möglicher Ergebnisse ist die Methode zum synthealisieren des Texel nicht angegeben.

Bei Formaten mit float32-Komponenten wird der Wert, der abgerufen wird, normalisiert, oder +-INF, im Vergleichs Vorgang unverändert verwendet. NaN wird in der Vergleichsoperation als NaN verwendet, aber die genaue Bitdarstellung des Nan kann geändert werden. Denorms werden in den Vergleich auf NULL geleert. Bei texturecubes muss eine Synthese der fehlenden 4. textextteile in Ecken vorkommen, sodass das Konzept der Rückgabe von Bits, die für die synthetische Texttyp unverändert sind, nicht zutrifft.

Die für *gather4 \_ c* unterstützten Formate sind identisch mit denen, die für *Beispiel \_ c* unterstützt werden. Dabei handelt es sich um Einzelkomponenten Formate und somit um. R auf *srcsampler*, anstelle eines beliebigen flüchtigen. **gather4 \_ c** für eine ungebundene Ressource gibt 0 (null) zurück.

Verwenden Sie diese Anweisung zum Filtern von benutzerdefinierten schattenkarten.

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

 

 





