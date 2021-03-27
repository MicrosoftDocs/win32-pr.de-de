---
title: Texture1D
description: Texture1D
ms.assetid: 5f6fd0e4-a73e-4d13-b3a0-c884b7912581
keywords:
- Texture1D HLSL
topic_type:
- apiref
api_name:
- Texture1D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8b8a60706ea2752109cdda9907ffe7c654efe531
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103948245"
---
# <a name="texture1d"></a>Texture1D

Ein 1D-Textur-Typ ([wie er in Shader Model 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen. Dieses Textur Objekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | Ruft die Ressourcen Dimensionen ab.                                                              |
| [**Laden**](texture1d-load.md)                                          | Liest Textur Daten.                                                                        |
| [**KOM\[\]**](sm5-object-texture1d-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                        |
| [**MIPS. KOM\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                        |
| [**Beispiel**](texture1d-sample.md)                                      | Stichproben eine Textur.                                                                         |
| [**Samplebias**](texture1d-samplebias.md)                              | Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.                      |
| [**Samplecmp**](texture1d-samplecmp.md)                                | Abtastungen einer Textur mithilfe eines Vergleichs Werts zum ablehnen von Beispielen.                             |
| [**Samplecmplevelzero**](texture1d-samplecmplevelzero.md)              | Stichproben eine Textur (nur MipMap-Ebene 0) unter Verwendung eines Vergleichs Werts zum ablehnen von Beispielen.       |
| [**Samplegrad**](texture1d-samplegrad.md)                              | Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird |
| [**Samplelevel**](texture1d-samplelevel.md)                            | Prüft eine Textur auf der angegebenen MipMap-Ebene.                                           |



 

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

 

 




