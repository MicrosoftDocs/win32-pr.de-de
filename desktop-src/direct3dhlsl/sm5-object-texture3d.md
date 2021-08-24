---
title: Texture3D
description: Texture3D
ms.assetid: a3640aac-b503-4716-8bc6-105e96bea03c
keywords:
- Texture3D HLSL
topic_type:
- apiref
api_name:
- Texture3D
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7b5c715f5f2bb7edfaa149cf0da77db5fbca8d47636b6f84fd07071c3b75186e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788320"
---
# <a name="texture3d"></a>Texture3D

Texture3D-Typ ([wie er in Shader Model 4](dx-graphics-hlsl-to-type.md)vorhanden ist) plus Ressourcenvariablen. Dieses Texturobjekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                  | Beschreibung                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | Ruft die Ressourcendimensionen ab.                                                              |
| [**Laden**](texture3d-load.md)                                          | Liest Texturdaten.                                                                        |
| [**Mips. Operator\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                        |
| [**Operator\[\]**](sm5-object-texture3d-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcenvariable ab.                                                        |
| [**Beispiel**](texture3d-sample.md)                                      | Stichproben einer Textur.                                                                         |
| [**SampleBias**](texture3d-samplebias.md)                              | Samples a texture, after applying the bias value to the mipmap level.                      |
| [**SampleGrad**](texture3d-samplegrad.md)                              | Samples a texture using a gradient to influence the way the sample location is calculated. (Stichprobenentnahme einer Textur mithilfe eines Farbverlaufs, um die Berechnung der Stichprobenposition zu beeinflussen.) |
| [**SampleLevel**](texture3d-samplelevel.md)                            | Stichproben einer Textur auf der angegebenen Mipmapebene.                                           |



 

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

 

 




