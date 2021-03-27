---
title: TextureCube-Objekt
description: Texturecube-Typ (wie er in Shader-Modell 4 vorhanden ist) plus Ressourcenvariablen. Dieses Textur Objekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.
ms.assetid: BC96D7BB-992E-48CC-A774-E211E1BB1720
keywords:
- Texturecube-Objekt HLSL
- Texturecube-Objekt HLSL, beschrieben
topic_type:
- apiref
api_name:
- TextureCube
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 939c79895ae1c24665fc70d6b6cf2ced19854e2b
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104132137"
---
# <a name="texturecube-object"></a>TextureCube-Objekt

**Texturecube** -Typ ([wie er in Shader-Modell 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen. Dieses Textur Objekt unterstützt diese Methoden zusätzlich zu den Methoden in Shader Model 4.

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **texturecube** -Objekt verfügt über diese Methoden.



| Methode                                                      | BESCHREIBUNG                                                                                                                                             |
|:------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Informieren**](texturecube-gather.md)                         | Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                                                |
| [**Gatheralpha**](texturecube-gatheralpha.md)               | Gibt die Alpha Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                        |
| [**Gatherblue**](texturecube-gatherblue.md)                 | Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                         |
| [**Gathercmp**](texturecube-gathercmp.md)                   | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zurückgegeben.<br/>                      |
| [**Gathercmpalpha**](texturecube-gathercmpalpha.md)         | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben.<br/> |
| [**Gathercmpblue**](texturecube-gathercmpblue.md)           | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der blauen Komponente mit einem Vergleichswert zurückgegeben.<br/>  |
| [**Gathercmpgreen**](texturecube-gathercmpgreen.md)         | Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben.<br/> |
| [**Gathercmpred**](texturecube-gathercmpred.md)             | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben.<br/>   |
| [**Gathergrün**](texturecube-gathergreen.md)               | Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                        |
| [**Gatherred**](texturecube-gatherred.md)                   | Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.<br/>                                          |
| [**Beispiel**](texturecube-sample.md)                         | Stichproben eine Textur.<br/>                                                                                                                                  |
| [**Samplebias**](texturecube-samplebias.md)                 | Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.<br/>                                                                               |
| [**Samplecmp**](texturecube-samplecmp.md)                   | Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.<br/>                                                                                      |
| [**Samplecmplevelzero**](texturecube-samplecmplevelzero.md) | Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.<br/>                                                                |
| [**Samplegrad**](texturecube-samplegrad.md)                 | Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird<br/>                                                          |
| [**Samplelevel**](texturecube-samplelevel.md)               | Prüft eine Textur auf der angegebenen MipMap-Ebene.<br/>                                                                                                    |



 

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

 

 





