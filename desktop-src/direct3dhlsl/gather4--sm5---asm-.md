---
title: gather4 (SM5-ASM)
description: Sammelt die vier texeln, die in einem bilinearen Filter Vorgang verwendet werden, und verpackt Sie in ein einzelnes Register. | gather4 (SM5-ASM)
ms.assetid: 5F93BB70-7696-48E4-BCD3-91D5D42FF63E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5657265738f12331afc7596286f02170de2a635
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219206"
---
# <a name="gather4-sm5---asm"></a>gather4 (SM5-ASM)

Sammelt die vier texeln, die in einem bilinearen Filter Vorgang verwendet werden, und verpackt Sie in ein einzelnes Register. Diese Anweisung funktioniert nur mit 2D-oder cubemap-Texturen, einschließlich Arrays. Es werden nur die Adressierungs Modi des Samplers verwendet, und die oberste Ebene jeder MIP-Pyramide wird verwendet.



| gather4 \[ \_ aoffimmi (u, v) \] dest \[ . mask \] , srcaddress \[ . Swizzle \] , srkresource \[ . Swizzle \] , srcsampler \[ . Select- \_ Komponente\] |
|-----------------------------------------------------------------------------------------------------------------------------|



 



| Element                                                                                                               | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[in \] der Adresse der Ergebnisse des Vorgangs.<br/> |
| <span id="srcAddress"></span><span id="srcaddress"></span><span id="SRCADDRESS"></span>*srcaddress*<br/>     | \[in \] einem Satz von Texturkoordinaten.<br/>                |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srkresource*<br/> | \[in \] einem Textur Register.<br/>                          |
| <span id="srcSampler"></span><span id="srcsampler"></span><span id="SRCSAMPLER"></span>*srcsampler*<br/>     | \[in \] einem Samplerregister.<br/>                          |



 

## <a name="remarks"></a>Bemerkungen

Diese Anweisung verhält sich wie die [**Beispiel**](sample--sm4---asm-.md) Anweisung, aber ein gefiltertes Beispiel wird nicht generiert. Die vier Beispiele, die zum Filtern beitragen würden, werden in xyzw im Uhrzeigersinn im Uhrzeigersinn eingefügt, beginnend mit dem Beispiel in der unteren linken Ecke des abgefragten Speicher Orts. Dies ist identisch mit der Punkt Stichprobe mit (u, v) Texturkoordinaten Deltas an den folgenden Positionen: (-, +), (+, +), (+,-), (-,-), wobei die Größe der Deltas immer eine halbe Texturgröße ist.

Bei cubemap-Texturen werden texeln aus dem benachbarten Gesicht verwendet, wenn ein bidirektionale Speicherbedarf einen Rand umfasst. Für Ecken werden dieselben Regeln wie für die [**Beispiel**](sample--sm4---asm-.md) Anweisung verwendet. Das heißt, die unbekannte Ecke wird als Durchschnitt der drei sich Zieh enden Gesichts Ecken betrachtet.

Es gibt Textur Format Einschränkungen, die für **gather4** gelten, die in der Format Liste ausgedrückt werden.

Das Swizzle in *srkresource* ermöglicht es, dass die zurückgegebenen Werte willkürlich durchlaufen werden, bevor Sie in das Ziel geschrieben werden.

Die. Select- \_ Komponente in *srcsampler* wählt die Komponente der Quell Textur (r/g/b/a) aus, von der 4 texeln gelesen werden sollen.

Bei Formaten mit float32-Komponenten wird der Wert, der abgerufen wird, normalisiert, denormalisiert, +-0 oder +-INF, an den Shader unverändert zurückgegeben. NaN wird als NaN zurückgegeben, aber die genaue Bitdarstellung des Nan kann geändert werden. Bei texturecubes müssen einige Synthese der fehlenden 4. Textteile in Ecken vorkommen, sodass das Zurückgeben von Bits, die für die synthetische Texttyp unverändert bleiben, nicht zutrifft und denorms geleert werden konnte.

Bei Hardware Implementierungen können Optimierungen in herkömmlichen bilinearen filtern, die Beispiele direkt in texeln erkennen und das Lesen von texeln überspringen, die eine Gewichtung von 0 haben, nicht mit dieser Anweisung genutzt werden. *gather4* gibt immer alle angeforderten Texels zurück.

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

 

 





