---
title: Texture1DArray
description: Texture1DArray
ms.assetid: 3d793423-3d79-48c1-aa78-f9d93b79e0b6
keywords:
- Texture1DArray HLSL
topic_type:
- apiref
api_name:
- Texture1DArray
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 39cea5692e29ead74ba20c4a35ab8d43a1b19d42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104038100"
---
# <a name="texture1darray"></a>Texture1DArray

Texture1DArray Type ([wie er in Shader Model 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen. Dieses Textur Objekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Ruft die Ressourcen Dimensionen ab.                                                              |
| [**Laden**](texture1darray-load.md)                                          | Liest Textur Daten.                                                                        |
| [**MIPS. KOM\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                        |
| [**KOM\[\]**](sm5-object-texture1darray-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                        |
| [**Beispiel**](texture1darray-sample.md)                                      | Stichproben eine Textur.                                                                         |
| [**Samplebias**](texture1darray-samplebias.md)                              | Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.                      |
| [**Samplecmp**](texture1darray-samplecmp.md)                                | Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.                             |
| [**Samplecmplevelzero**](texture1darray-samplecmplevelzero.md)              | Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.       |
| [**Samplegrad**](texture1darray-samplegrad.md)                              | Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird |
| [**Samplelevel**](texture1darray-samplelevel.md)                            | Prüft eine Textur auf der angegebenen MipMap-Ebene.                                           |



 

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

 

 




