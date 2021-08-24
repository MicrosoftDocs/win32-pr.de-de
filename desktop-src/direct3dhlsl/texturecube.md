---
title: TextureCube-Objekt
description: TextureCube-Typ (wie er in Shader Model 4 vorhanden ist) plus Ressourcenvariablen. Dieses Texturobjekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- TextureCube-Objekt HLSL
- TextureCube-Objekt HLSL , beschrieben
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d9cab13ec3ca86e17586e2fea27e7e60cf14a552abfdd405d3ea3da8c8195a3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892470"
---
# <a name="texturecube-object"></a>TextureCube-Objekt

**TextureCube-Typ** ([wie er in Shader Model 4](dx-graphics-hlsl-to-type.md)vorhanden ist) plus Ressourcenvariablen. Dieses Texturobjekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **TextureCube-Objekt** verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**versammeln**](texturecube-gather.md)                         | Gibt die vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                                                |
| [**GatherAlpha**](texturecube-gatheralpha.md)               | Gibt die Alphakomponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                        |
| [**GatherBlue**](texturecube-gatherblue.md)                 | Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                         |
| [**GatherCmp**](texturecube-gathercmp.md)                   | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt ihren Vergleich mit einem Vergleichswert zurück.<br/>                      |
| [**GatherCmpAlpha**](texturecube-gathercmpalpha.md)         | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zurück.<br/> |
| [**GatherCmpBlue**](texturecube-gathercmpblue.md)           | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer blauen Komponente mit einem Vergleichswert zurück.<br/>  |
| [**GatherCmpGreen**](texturecube-gathercmpgreen.md)         | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück.<br/> |
| [**GatherCmpRed**](texturecube-gathercmpred.md)             | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück.<br/>   |
| [**GatherGreen**](texturecube-gathergreen.md)               | Gibt die grünen Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                        |
| [**GatherRed**](texturecube-gatherred.md)                   | Gibt die roten Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.<br/>                                          |
| [**Beispiel**](texturecube-sample.md)                         | Stichproben einer Textur.<br/>                                                                                                                                  |
| [**SampleBias**](texturecube-samplebias.md)                 | Samples a texture, after applying the bias value to the mipmap level.<br/>                                                                               |
| [**SampleCmp**](texturecube-samplecmp.md)                   | Samples a texture, using a comparison value to reject samples. (Stichproben werden mithilfe eines Vergleichswerts abgewiesen.)<br/>                                                                                      |
| [**SampleCmpLevelZero**](texturecube-samplecmplevelzero.md) | Stichproben einer Textur (nur Mipmap-Ebene 0) mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.<br/>                                                                |
| [**SampleGrad**](texturecube-samplegrad.md)                 | Samples a texture using a gradient to influence the way the sample location is calculated. (Stichprobenentnahme einer Textur mithilfe eines Farbverlaufs, um die Berechnung der Stichprobenposition zu beeinflussen.)<br/>                                                          |
| [**SampleLevel**](texturecube-samplelevel.md)               | Stichproben einer Textur auf der angegebenen Mipmapebene.<br/>                                                                                                    |



 

## <a name="remarks"></a>Hinweise

### <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[ShaderModell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 





