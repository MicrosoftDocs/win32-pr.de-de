---
title: Ausgabetopologie
description: Definiert den primitiven Ausgabetyp für den Mosaik.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8d718b11c23fcf77f452e224a51439f7d6f422d3c81d5238167cbf87c7c3014a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725414"
---
# <a name="outputtopology"></a>Ausgabetopologie

Definiert den primitiven Ausgabetyp für den Mosaik.


```
outputtopology(X)      
```



## <a name="remarks"></a>Hinweise

X muss entweder ein [**Punkt,**](dx-graphics-hlsl-geometry-shader.md)eine **Zeile,** ein **Dreieck \_ cw** oder ein Dreieck **\_ ccw** sein und in Anführungszeichen stehen. Dies sind die gültigen Optionen für dieses Attribut:


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



Dieses Attribut wird in den folgenden Shadertypen unterstützt:



| Scheitelpunkt | Rumpf | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shadermodell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




