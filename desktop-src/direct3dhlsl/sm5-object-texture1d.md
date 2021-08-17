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
ms.openlocfilehash: 382ac1e436eff4108a2179aeefd4395fbc52c7af304bb719cbadf87a3c1f3d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117724871"
---
# <a name="texture1d"></a>Texture1D

Ein 1D-Texturtyp ([wie er in Shader Model 4](dx-graphics-hlsl-to-type.md)vorhanden ist) plus Ressourcenvariablen. Dieses Texturobjekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                  | Beschreibung                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture1d-getdimensions.md)             | Ruft die Ressourcendimensionen ab.                                                              |
| [**Laden**](texture1d-load.md)                                          | Liest Texturdaten.                                                                        |
| [**Operator\[\]**](sm5-object-texture1d-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                        |
| [**Mips. Operator\[\]\[\]**](sm5-object-texture1d-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                        |
| [**Beispiel**](texture1d-sample.md)                                      | Stichproben einer Textur.                                                                         |
| [**SampleBias**](texture1d-samplebias.md)                              | Samples a texture, after applying the bias value to the mipmap level.                      |
| [**SampleCmp**](texture1d-samplecmp.md)                                | Samples a texture, using a comparison value to reject samples. (Stichproben werden mithilfe eines Vergleichswerts abgewiesen.)                             |
| [**SampleCmpLevelZero**](texture1d-samplecmplevelzero.md)              | Stichproben einer Textur (nur Mipmap-Ebene 0) mithilfe eines Vergleichswerts zum Ablehnen von Stichproben.       |
| [**SampleGrad**](texture1d-samplegrad.md)                              | Samples a texture using a gradient to influence the way the sample location is calculated. (Stichprobenentnahme einer Textur mithilfe eines Farbverlaufs, um die Berechnung der Stichprobenposition zu beeinflussen.) |
| [**SampleLevel**](texture1d-samplelevel.md)                            | Stichproben einer Textur auf der angegebenen Mipmapebene.                                           |



 

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

 

 




