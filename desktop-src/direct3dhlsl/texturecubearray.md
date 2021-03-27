---
title: TextureCubeArray-Objekt
description: Texturecubearray-Typ (wie in Shader-Modell 4 vorhanden) und Ressourcenvariablen. Dieses Textur Objekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.
ms.assetid: 62AAF0F9-D552-4FFA-B681-749D6DC205BD
keywords:
- Texturecubearray-Objekt HLSL
- Texturecubearray-Objekt HLSL, beschrieben
topic_type:
- apiref
api_name:
- TextureCubeArray
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e559214626fadbc08b8e9cd4d5568358f130779c
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104995246"
---
# <a name="texturecubearray-object"></a>TextureCubeArray-Objekt

**Texturecubearray** -Typ ([wie in Shader-Modell 4 vorhanden](dx-graphics-hlsl-to-type.md)) und Ressourcenvariablen. Dieses Textur Objekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **texturecubearray** -Objekt verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                                                                                              |
|:-----------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Informieren**](texturecubearray-gather.md)                         | Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                                                |
| [**Gatheralpha**](texturecubearray-gatheralpha.md)               | Gibt die Alpha Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                        |
| [**Gatherblue**](texturecubearray-gatherblue.md)                 | Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                         |
| [**Gathercmp**](texturecubearray-gathercmp.md)                   | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zurückgegeben.<br/>                      |
| [**Gathercmpalpha**](texturecubearray-gathercmpalpha.md)         | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.<br/> |
| [**Gathercmpblue**](texturecubearray-gathercmpblue.md)           | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der blauen Komponente mit einem Vergleichswert zurückgegeben.<br/>  |
| [**Gathercmpgreen**](texturecubearray-gathercmpgreen.md)         | Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben.<br/> |
| [**Gathercmpred**](texturecubearray-gathercmpred.md)             | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben.<br/>   |
| [**Gathergrün**](texturecubearray-gathergreen.md)               | Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                        |
| [**Gatherred**](texturecubearray-gatherred.md)                   | Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                          |
| [**Beispiel**](texturecubearray-sample.md)                         | Stichproben eine Textur.<br/>                                                                                                                                  |
| [**Samplebias**](texturecubearray-samplebias.md)                 | Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.<br/>                                                                               |
| [**Samplecmp**](texturecubearray-samplecmp.md)                   | Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.<br/>                                                                                      |
| [**Samplecmplevelzero**](texturecubearray-samplecmplevelzero.md) | Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.<br/>                                                                |
| [**Samplegrad**](texturecubearray-samplegrad.md)                 | Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird<br/>                                                          |
| [**Samplelevel**](texturecubearray-samplelevel.md)               | Prüft eine Textur auf der angegebenen MipMap-Ebene.<br/>                                                                                                    |



 

## <a name="remarks"></a>Bemerkungen

### <a name="minimum-shader-model"></a>Minimaler Shader-Modell

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

 

 





