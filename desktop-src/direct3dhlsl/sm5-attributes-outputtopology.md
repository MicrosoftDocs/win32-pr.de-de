---
title: outputtopology
description: Definiert den primitiven Ausgabetyp für den Mosaik-.
ms.assetid: 4aba65e5-b005-43fd-a844-c7fbb1b7406c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 917a927ff80d4abe1b6509fd41281992a998c945
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/20/2019
ms.locfileid: "103948321"
---
# <a name="outputtopology"></a>outputtopology

Definiert den primitiven Ausgabetyp für den Mosaik-.


```
outputtopology(X)      
```



## <a name="remarks"></a>Bemerkungen

X muss entweder [**Point**](dx-graphics-hlsl-geometry-shader.md), **Line**, **Dreieck \_ CW** oder **Dreieck \_ CCW** sein und muss in Anführungszeichen gesetzt werden. Hier sind die gültigen Optionen für dieses Attribut angegeben:


```
[outputtopology("point")]
[outputtopology("line")]
[outputtopology("triangle_cw")]
[outputtopology("triangle_ccw")]
```



Dieses Attribut wird in den folgenden Typen von Shadern unterstützt:



| Scheitelpunkt | Hülle | Domain | Geometrie | Pixel | Compute |
|--------|------|--------|----------|-------|---------|
|        | x    |        |          |       |         |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shader Model 5-Attribute](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[Shader-Modell 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




