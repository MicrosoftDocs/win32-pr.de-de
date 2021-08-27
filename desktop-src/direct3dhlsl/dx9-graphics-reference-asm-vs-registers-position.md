---
title: Positionsregister
description: Dieses Vertex-Shader-Ausgaberegister enthält Daten zur Scheitelpunktposition pro Scheitelpunkt.
ms.assetid: 98f71027-d94b-4dd0-a6b6-4b263954eff9
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: cda82431990ed3ea545adfcc5e6eb2801be0607d8bac45aa1bcd8c0e121f3d68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023900"
---
# <a name="position-register"></a>Positionsregister

Dieses Vertex-Shader-Ausgaberegister enthält Daten zur Scheitelpunktposition pro Scheitelpunkt.



| Vertex-Shaderversionen | 1\_1 | 2 \_ 0 | 2 \_ sw | 2 \_ x | 3 \_ 0 | 3 \_ sw |
|------------------------|------|------|-------|------|------|-------|
| Positionsregister      | x    | x    | x     | x    | x    | x     |



 

Ein Register besteht aus Eigenschaften, die bestimmen, wie sich jedes Register verhält.



| Eigenschaft        | BESCHREIBUNG |
|-----------------|-------------|
| Name            | Opos        |
| Anzahl           | 1 Vektor    |
| E/A-Berechtigungen | Nur Schreibzugriff. |



 

Der Wert ist die Position im homogenen Ausschneidebereich. Dieser Wert muss vom Vertex-Shader geschrieben werden.

Beispiel


```
    dcl_position v0
    
    def c40, 0.0f,0.0f,0.0f,0.0f;
    // transform into projection space
    m4x4 r0,v0,c8
    max r0.z,c40.z,r0.z //clamp to 0
    max r0.w,c12.x,r0.w //clamp to near clip plane
    mov oPos,r0   
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Vertex-Shaderregister](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




