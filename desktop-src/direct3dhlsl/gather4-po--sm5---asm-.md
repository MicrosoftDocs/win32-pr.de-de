---
title: gather4_po (SM5-ASM)
description: Eine Variante von gather4, aber anstelle eines unmittelbaren Offsets \-8.. 7 \, wird der Offset als Parameter für die Anweisung und auch als größerer Bereich von \-32.. 31 \ angezeigt.
ms.assetid: A77A32B4-BD4F-46E7-9999-13EAA8A26974
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9197fee97645333d37d589db36c3774852b12229
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "104976425"
---
# <a name="gather4_po-sm5---asm"></a>gather4 \_ Po (SM5-ASM)

Eine Variante von [gather4](gather4--sm5---asm-.md), aber anstelle eines unmittelbaren Offsets \[ -8.. 7, wird \] der Offset als Parameter für die Anweisung und auch als größerer Bereich von \[ -32.. 31 angezeigt \] .



| gather4 \_ po dest \[ . mask \] , srcaddress \[ . Swizzle \] , srcOffset \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler \[ . Select \_ Component\] |
|-------------------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                   |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse des Vorgangs Ergebnisses.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>     | \[in \] einem Satz von Texturkoordinaten.<br/>               |
| <span id="srcOffset"></span><span id="srcoffset"></span><span id="SRCOFFSET"></span>*srcOffset*<br/>         | \[im \] Offset.<br/>                                 |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Textur Register.<br/>                         |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>     | \[in \] einem Samplerregister.<br/>                         |



 

## <a name="remarks"></a>Bemerkungen

Die ersten beiden Komponenten des offset-Parameters "4-Vector" stellen ganzzahlige Offsets von 32 Bit bereit. Die anderen Komponenten dieses Parameters werden ignoriert.

Die 6 geringsten Bits jedes Offset Werts werden als signierter Wert berücksichtigt, der den \[ Bereich-32.. 31 ergibt \] .

Diese Anweisung funktioniert nur mit 2D-Texturen, im Gegensatz zu **gather4**, die auch mit texturecubes funktioniert.

Die einzigen Modi, die im Sampler berücksichtigt werden, sind die Adressierungs Modi. Nur das ausführlichste MIP in der Ressourcen Ansicht wird verwendet.

Wenn die Adresse in ein Textem-Center fällt, bedeutet dies nicht, dass die anderen texeln mit Nullen entfernt werden können.

Der *srcsampler* -Parameter enthält \[ . Select- \_ Komponente \] , sodass jede einzelne Komponente einer Textur abgerufen werden kann, einschließlich der Rückgabe von Standardwerten für fehlende Komponenten.

Bei Formaten mit float32-Komponenten wird der Wert, der abgerufen wird, normalisiert, denormalisiert, +-0 oder +-INF, an den Shader unverändert zurückgegeben. NaN wird als NaN zurückgegeben, aber die genaue Bitdarstellung des Nan kann geändert werden. Bei texturecubes müssen einige Synthese der fehlenden 4. Textteile in Ecken vorkommen, sodass das Konzept der Rückgabe von Bits, die für die synthetische Texttyp unverändert liegen, nicht zutrifft und denorms geleert werden konnte.

Verwenden Sie diese Anweisung, um den Offset Bereich von **gather4** auf einen größeren und programmierbaren Bereich zu erweitern. Das Suffix "Po" im Namen bedeutet "Programmierbarer Offset".

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

 

 





