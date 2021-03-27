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
ms.openlocfilehash: f1aefa9171ed634934ea5e1306973fe3b22abdfa
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104981000"
---
# <a name="texture2darray"></a>Texture2DArray

Texture2DArray Type ([wie er in Shader Model 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen. Dieses Textur Objekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                                                                         |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Informieren**](texture2darray-gather.md)                                      | Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                                                |
| [**Gatherred**](texture2darray-gatherred.md)                                | Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                          |
| [**Gathergrün**](texture2darray-gathergreen.md)                            | Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                        |
| [**Gatherblue**](texture2darray-gatherblue.md)                              | Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                         |
| [**Gatheralpha**](texture2darray-gatheralpha.md)                            | Gibt die Alpha Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                        |
| [**Gathercmp**](texture2darray-gathercmp.md)                                | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zurückgegeben.                      |
| [**Gathercmpred**](texture2darray-gathercmpred.md)                          | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben.   |
| [**Gathercmpgreen**](texture2darray-gathercmpgreen.md)                      | Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben. |
| [**Gathercmpblue**](texture2darray-gathercmpblue.md)                        | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der blauen Komponente mit einem Vergleichswert zurückgegeben.  |
| [**Gathercmpalpha**](texture2darray-gathercmpalpha.md)                      | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben. |
| [**GetDimensions**](sm5-object-texture2darray-getdimensions.md)             | Ruft die Ressourcen Dimensionen ab.                                                                                                                       |
| [**Laden**](texture2darray-load.md)                                          | Liest Textur Daten.                                                                                                                                 |
| [**MIPS. KOM\[\]\[\]**](sm5-object-texture2darray-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                                                                                 |
| [**KOM\[\]**](sm5-object-texture2darray-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                                                                                 |
| [**Beispiel**](texture2darray-sample.md)                                      | Stichproben eine Textur.                                                                                                                                  |
| [**Samplebias**](texture2darray-samplebias.md)                              | Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.                                                                               |
| [**Samplecmp**](texture2darray-samplecmp.md)                                | Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.                                                                                      |
| [**Samplecmplevelzero**](texture2darray-samplecmplevelzero.md)              | Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.                                                                |
| [**Samplegrad**](texture2darray-samplegrad.md)                              | Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird                                                          |
| [**Samplelevel**](texture2darray-samplelevel.md)                            | Prüft eine Textur auf der angegebenen MipMap-Ebene.                                                                                                    |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shader Model 5](d3d11-graphics-reference-sm5.md) und höhere shadermodelle | ja       |



 

Dieses Objekt wird für die folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Shader Model 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




