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
ms.openlocfilehash: f0c9b73d66f1c5a38b077b241df8e5859b706e2f
ms.sourcegitcommit: 5724b38883e518ac565e1b266defa85ad0941bb2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "104981016"
---
# <a name="texture2d"></a>Texture2D

Texture2D Type ([wie er in Shader Model 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen. Dieses Textur Objekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                 | BESCHREIBUNG                                                                                                                                        |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Informieren**](texture2d-gather.md)                                      | Gibt die vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                                                |
| [**Gatherred**](texture2d-gatherred.md)                                | Gibt die roten Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                          |
| [**Gathergrün**](texture2d-gathergreen.md)                            | Gibt die grünen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                        |
| [**Gatherblue**](texture2d-gatherblue.md)                              | Gibt die blauen Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                         |
| [**Gatheralpha**](texture2d-gatheralpha.md)                            | Gibt die Alpha Komponenten der vier texelwerte zurück, die in einem bilinearen Filter Vorgang verwendet werden.                                        |
| [**Gathercmp**](texture2d-gathercmp.md)                                | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird der Vergleich mit einem Vergleichswert zurückgegeben.                      |
| [**Gathercmpred**](texture2d-gathercmpred.md)                          | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der roten Komponente mit einem Vergleichswert zurückgegeben.   |
| [**Gathercmpgreen**](texture2d-gathercmpgreen.md)                      | Für vier textexwerte, die in einem bilinearen Filterungs Vorgang verwendet werden, wird ein Vergleich der grünen Komponente mit einem Vergleichswert zurückgegeben. |
| [**Gathercmpblue**](texture2d-gathercmpblue.md)                        | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der blauen Komponente mit einem Vergleichswert zurückgegeben.  |
| [**Gathercmpalpha**](texture2d-gathercmpalpha.md)                      | Für vier textexwerte, die in einem bilinearen Filter Vorgang verwendet werden, wird ein Vergleich der Alpha Komponente mit einem Vergleichswert zurückgegeben. |
| [**GetDimensions**](sm5-object-texture2d-getdimensions.md)             | Ruft die Ressourcen Dimensionen ab.                                                                                                                       |
| [**Laden**](texture2d-load.md)                                          | Liest Textur Daten.                                                                                                                                 |
| [**MIPS. KOM\[\]\[\]**](sm5-object-texture2d-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                                                                                 |
| [**KOM\[\]**](sm5-object-texture2d-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                                                                                 |
| [**Beispiel**](texture-sample-overload.md)                               | Stichproben eine Textur.                                                                                                                                  |
| [**Samplebias**](texture2d-samplebias.md)                              | Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.                                                                               |
| [**Samplecmp**](texture2d-samplecmp.md)                                | Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.                                                                                      |
| [**Samplecmplevelzero**](texture2d-samplecmplevelzero.md)              | Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.                                                                |
| [**Samplegrad**](texture2d-samplegrad.md)                              | Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird                                                          |
| [**Samplelevel**](texture2d-samplelevel.md)                            | Prüft eine Textur auf der angegebenen MipMap-Ebene.                                                                                                    |



 

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

 

 




