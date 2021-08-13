---
title: TextureCubeArray-Objekt
description: TextureCubeArray-Typ (wie er in Shader Model 4 vorhanden ist) plus Ressourcenvariablen. Dieses Texturobjekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- TextureCubeArray-Objekt HLSL
- TextureCubeArray-Objekt HLSL , beschrieben
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a0b5687e26ebb8a80dbd75e5849ad95de29dacec90c64e660e59dce71c796b0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118786168"
---
# <a name="texturecubearray-object"></a>TextureCubeArray-Objekt

**TextureCubeArray-Typ** ([wie er in Shader Model 4](dx-graphics-hlsl-to-type.md)vorhanden ist) plus Ressourcenvariablen. Dieses Texturobjekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **TextureCubeArray-Objekt** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**versammeln**](texturecubearray-gather.md)                         | Gibt die vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                                                |
| [**GatherAlpha**](texturecubearray-gatheralpha.md)               | Gibt die Alphakomponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                        |
| [**GatherBlue**](texturecubearray-gatherblue.md)                 | Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                         |
| [**GatherCmp**](texturecubearray-gathercmp.md)                   | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt ihren Vergleich mit einem Vergleichswert zurück.<br/>                      |
| [**GatherCmpAlpha**](texturecubearray-gathercmpalpha.md)         | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zurück.<br/> |
| [**GatherCmpBlue**](texturecubearray-gathercmpblue.md)           | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer blauen Komponente mit einem Vergleichswert zurück.<br/>  |
| [**GatherCmpGreen**](texturecubearray-gathercmpgreen.md)         | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück.<br/> |
| [**GatherCmpRed**](texturecubearray-gathercmpred.md)             | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück.<br/>   |
| [**GatherGreen**](texturecubearray-gathergreen.md)               | Gibt die grünen Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                        |
| [**GatherRed**](texturecubearray-gatherred.md)                   | Gibt die roten Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                          |
| [**Beispiel**](texturecubearray-sample.md)                         | Stichproben einer Textur.<br/>                                                                                                                                  |
| [**SampleBias**](texturecubearray-samplebias.md)                 | Samples a texture, after applying the bias value to the mipmap level.<br/>                                                                               |
| [**SampleCmp**](texturecubearray-samplecmp.md)                   | Samples a texture, using a comparison value to reject samples. (Stichproben werden mithilfe eines Vergleichswerts abgewiesen.)<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecubearray-samplecmplevelzero.md) | Stichproben einer Textur (nur Mipmap-Ebene 0) mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.<br/>                                                                |
| [**SampleGrad**](texturecubearray-samplegrad.md)                 | Samples a texture using a gradient to influence the way the sample location is calculated. (Stichprobenentnahme einer Textur mithilfe eines Farbverlaufs, um die Berechnung der Stichprobenposition zu beeinflussen.)<br/>                                                          |
| [**SampleLevel**](texturecubearray-samplelevel.md)               | Stichproben einer Textur auf der angegebenen Mipmapebene.<br/>                                                                                                    |



 

## <a name="remarks"></a>Hinweise

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ShaderModell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





