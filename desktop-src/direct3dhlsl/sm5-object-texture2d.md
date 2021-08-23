---
title: Texture2D
description: Texture2D
ms.assetid: e4f9cfd8-65e6-4375-8f87-736bca32cad4
keywords:
- Texture2D HLSL
topic_type:
- apiref
api_name:
- Texture2D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad13843dd74ab7cc188c3ab37d76df978f2a5fbd4bc6c292cfddfdf7c5841b33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118789376"
---
# <a name="texture2d"></a>Texture2D

Texture2D-Typ ([wie er in Shader Model 4](dx-graphics-hlsl-to-type.md)vorhanden ist) plus Ressourcenvariablen. Dieses Texturobjekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**versammeln**](texture2d-gather.md)                                      | Gibt die vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.                                                                |
| [**GatherRed**](texture2d-gatherred.md)                                | Gibt die roten Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.                                          |
| [**GatherGreen**](texture2d-gathergreen.md)                            | Gibt die grünen Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.                                        |
| [**GatherBlue**](texture2d-gatherblue.md)                              | Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.                                         |
| [**GatherAlpha**](texture2d-gatheralpha.md)                            | Gibt die Alphakomponenten der vier Texelwerte zurück, die in einem bilinealen Filtervorgang verwendet werden.                                        |
| [**GatherCmp**](texture2d-gathercmp.md)                                | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt ihren Vergleich mit einem Vergleichswert zurück.                      |
| [**GatherCmpRed**](texture2d-gathercmpred.md)                          | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück.   |
| [**GatherCmpGreen**](texture2d-gathercmpgreen.md)                      | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück. |
| [**GatherCmpBlue**](texture2d-gathercmpblue.md)                        | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer blauen Komponente mit einem Vergleichswert zurück.  |
| [**GatherCmpAlpha**](texture2d-gathercmpalpha.md)                      | Für vier Texelwerte, die in einem bilinealen Filtervorgang verwendet werden, gibt einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zurück. |
| [**GetDimensions**](sm5-object-texture2d-getdimensions.md)             | Ruft die Ressourcendimensionen ab.                                                                                                                       |
| [**Laden**](texture2d-load.md)                                          | Liest Texturdaten.                                                                                                                                 |
| [**Mips. Operator\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                                                                                 |
| [**Operator\[\]**](sm5-object-texture2d-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                                                                                 |
| [**Beispiel**](texture-sample-overload.md)                               | Stichproben einer Textur.                                                                                                                                  |
| [**SampleBias**](texture2d-samplebias.md)                              | Samples a texture, after applying the bias value to the mipmap level.                                                                               |
| [**SampleCmp**](texture2d-samplecmp.md)                                | Samples a texture, using a comparison value to reject samples. (Stichproben werden mithilfe eines Vergleichswerts abgewiesen.)                                                                                      |
| [**SampleCmpLevelZero**](texture2d-samplecmplevelzero.md)              | Stichproben einer Textur (nur Mipmap-Ebene 0) mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.                                                                |
| [**SampleGrad**](texture2d-samplegrad.md)                              | Samples a texture using a gradient to influence the way the sample location is calculated. (Stichprobenentnahme einer Textur mithilfe eines Farbverlaufs, um die Berechnung der Stichprobenposition zu beeinflussen.)                                                          |
| [**SampleLevel**](texture2d-samplelevel.md)                            | Stichproben einer Textur auf der angegebenen Mipmapebene.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höher– Shadermodelle | Ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[ShaderModell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




