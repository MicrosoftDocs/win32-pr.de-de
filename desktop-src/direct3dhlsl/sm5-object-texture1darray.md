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
ms.openlocfilehash: 11573dc84c46149073ca3a7e192ed8541d9cfd4a78494a43f6130a7999534880
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118508676"
---
# <a name="texture1darray"></a>Texture1DArray

Texture1DArray-Typ ([wie in Shadermodell 4 vorhanden)](dx-graphics-hlsl-to-type.md)plus Ressourcenvariablen. Dieses Texturobjekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                       | Beschreibung                                                                                |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1darray-getdimensions.md)             | Ruft die Ressourcendimensionen ab.                                                              |
| [**Laden**](texture1darray-load.md)                                          | Liest Texturdaten.                                                                        |
| [**Mips. Operator\[\]\[\]**](sm5-object-texture1darray-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                        |
| [**Operator\[\]**](sm5-object-texture1darray-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                        |
| [**Beispiel**](texture1darray-sample.md)                                      | Probieren Sie eine Textur aus.                                                                         |
| [**SampleBias**](texture1darray-samplebias.md)                              | Stichproben einer Textur, nachdem der Biaswert auf die Mipmapebene angewendet wurde.                      |
| [**SampleCmp**](texture1darray-samplecmp.md)                                | Stichproben einer Textur mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.                             |
| [**SampleCmpLevelZero**](texture1darray-samplecmplevelzero.md)              | Probieren Sie eine Textur (nur Mipmapebene 0) mithilfe eines Vergleichswerts aus, um Stichproben abzulehnen.       |
| [**SampleGrad**](texture1darray-samplegrad.md)                              | Probieren Sie eine Textur mithilfe eines Farbverlaufs aus, um die Art und Weise zu beeinflussen, wie die Stichprobenposition berechnet wird. |
| [**SampleLevel**](texture1darray-samplelevel.md)                            | Probieren Sie eine Textur auf der angegebenen Mipmapebene aus.                                           |



 

## <a name="minimum-shader-model"></a>Shader-Mindestmodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                                | Unterstützt |
|-----------------------------------------------------------------------------|-----------|
| [Shadermodell 5](d3d11-graphics-reference-sm5.md) und höhere Shadermodelle | Ja       |



 

Dieses Objekt wird für die folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domäne | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Shadermodell 5-Objekte](d3d11-graphics-reference-sm5-objects.md)
</dt> </dl>

 

 




