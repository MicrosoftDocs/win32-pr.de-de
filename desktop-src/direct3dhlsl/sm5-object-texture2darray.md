---
title: Texture2DArray
description: Texture2DArray
ms.assetid: 78ab2feb-4d67-4f6f-bffe-48d55183ce28
keywords:
- Texture2DArray HLSL
topic_type:
- apiref
api_name:
- Texture2DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aab6e5c0a500a9f34cbd4e418a35e96687650f3df863e1fe77576c66ade718e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023400"
---
# <a name="texture2darray"></a>Texture2DArray

Texture2DArray-Typ ([wie in Shadermodell 4 vorhanden)](dx-graphics-hlsl-to-type.md)plus Ressourcenvariablen. Dieses Texturobjekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**versammeln**](texture2darray-gather.md)                                      | Gibt die vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden.                                                                |
| [**GatherRed**](texture2darray-gatherred.md)                                | Gibt die roten Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden.                                          |
| [**GatherGreen**](texture2darray-gathergreen.md)                            | Gibt die grünen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden.                                        |
| [**GatherBlue**](texture2darray-gatherblue.md)                              | Gibt die blauen Komponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden.                                         |
| [**GatherAlpha**](texture2darray-gatheralpha.md)                            | Gibt die Alphakomponenten der vier Texelwerte zurück, die in einem bilinearen Filtervorgang verwendet werden.                                        |
| [**GatherCmp**](texture2darray-gathercmp.md)                                | Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt den Vergleich mit einem Vergleichswert zurück.                      |
| [**GatherCmpRed**](texture2darray-gathercmpred.md)                          | Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer roten Komponente mit einem Vergleichswert zurück.   |
| [**GatherCmpGreen**](texture2darray-gathercmpgreen.md)                      | Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer grünen Komponente mit einem Vergleichswert zurück. |
| [**GatherCmpBlue**](texture2darray-gathercmpblue.md)                        | Für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, gibt einen Vergleich ihrer blauen Komponente mit einem Vergleichswert zurück.  |
| [**GatherCmpAlpha**](texture2darray-gathercmpalpha.md)                      | Gibt für vier Texelwerte, die in einem bilinearen Filtervorgang verwendet werden, einen Vergleich ihrer Alphakomponente mit einem Vergleichswert zurück. |
| [**GetDimensions**](sm5-object-texture2darray-getdimensions.md)             | Ruft die Ressourcendimensionen ab.                                                                                                                       |
| [**Laden**](texture2darray-load.md)                                          | Liest Texturdaten.                                                                                                                                 |
| [**Mips. Operator\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                                                                                 |
| [**Operator\[\]**](sm5-object-texture2darray-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                                                                                 |
| [**Beispiel**](texture2darray-sample.md)                                      | Probieren Sie eine Textur aus.                                                                                                                                  |
| [**SampleBias**](texture2darray-samplebias.md)                              | Stichproben einer Textur, nachdem der Biaswert auf die Mipmapebene angewendet wurde.                                                                               |
| [**SampleCmp**](texture2darray-samplecmp.md)                                | Stichproben einer Textur mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.                                                                                      |
| [**SampleCmpLevelZero**](texture2darray-samplecmplevelzero.md)              | Probieren Sie eine Textur (nur Mipmapebene 0) mithilfe eines Vergleichswerts aus, um Stichproben abzulehnen.                                                                |
| [**SampleGrad**](texture2darray-samplegrad.md)                              | Probieren Sie eine Textur mithilfe eines Farbverlaufs aus, um die Art und Weise zu beeinflussen, wie die Stichprobenposition berechnet wird.                                                          |
| [**SampleLevel**](texture2darray-samplelevel.md)                            | Probieren Sie eine Textur auf der angegebenen Mipmapebene aus.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shadermodell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




