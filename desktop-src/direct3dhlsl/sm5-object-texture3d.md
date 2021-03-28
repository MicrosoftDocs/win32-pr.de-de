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
ms.openlocfilehash: 50b12f2184f6eca0fd7a68feb3e96d8d6fc65a61
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104037870"
---
# <a name="texture3d"></a>Texture3D

Texture3D Type ([wie er in Shader Model 4 vorhanden](dx-graphics-hlsl-to-type.md)ist) plus Ressourcenvariablen. Dieses Textur Objekt unterstützt zusätzlich zu den Methoden in Shader Model 4 die folgenden Methoden.



| Methode                                                                  | BESCHREIBUNG                                                                                |
|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [**GetDimensions**](sm5-object-texture3d-getdimensions.md)             | Ruft die Ressourcen Dimensionen ab.                                                              |
| [**Laden**](texture3d-load.md)                                          | Liest Textur Daten.                                                                        |
| [**MIPS. KOM\[\]\[\]**](sm5-object-texture3d-mipsoperatorindex.md) | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                        |
| [**KOM\[\]**](sm5-object-texture3d-operatorindex.md)              | Ruft eine schreibgeschützte Ressourcen Variable ab.                                                        |
| [**Beispiel**](texture3d-sample.md)                                      | Stichproben eine Textur.                                                                         |
| [**Samplebias**](texture3d-samplebias.md)                              | Gibt eine Textur aus, nachdem der Bias-Wert auf die MipMap-Ebene angewendet wurde.                      |
| [**Samplegrad**](texture3d-samplegrad.md)                              | Verwendet einen Farbverlauf, um die Art und Weise zu beeinflussen, in der der Beispiel Speicherort berechnet wird |
| [**Samplelevel**](texture3d-samplelevel.md)                            | Prüft eine Textur auf der angegebenen MipMap-Ebene.                                           |



 

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

 

 




