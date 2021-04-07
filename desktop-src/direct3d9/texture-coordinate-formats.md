---
description: Texturkoordinaten in Direct3D können ein, zwei, drei oder vier Gleit Komma Elemente enthalten, um Texturen mit unterschiedlichen Dimensions Ebenen zu behandeln.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Texturkoordinaten Formate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c95eada1cf21f0a4db38589794b08b88023e72d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747616"
---
# <a name="texture-coordinate-formats-direct3d-9"></a>Texturkoordinaten Formate (Direct3D 9)

Texturkoordinaten in Direct3D können ein, zwei, drei oder vier Gleit Komma Elemente enthalten, um Texturen mit unterschiedlichen Dimensions Ebenen zu behandeln. Eine 1D-Textur: eine Textur Oberfläche mit Dimensionen von 1-nach-n-texeln-wird von einer Textur Koordinate adressiert. Die gängigsten Fälle, 2D-Texturen, werden mit zwei Texturkoordinaten adressiert, die häufig als Sie und v bezeichnet werden. Direct3D unterstützt zwei Arten von 3D-Texturen, kubische Umgebungs Zuordnungen und volumetexturen. Kubische Umgebungs Zuordnungen sind nicht wirklich 3D, aber Sie werden mit einem Vektor mit drei Elementen adressiert. Weitere Informationen finden Sie unter [Zuordnung von kubischen Umgebungen (Direct3D 9)](cubic-environment-mapping.md).

Wie in " [Fixed Function f VF Codes (Direct3D 9)](fixed-function-fvf-codes.md)" beschrieben, codieren Anwendungen Texturkoordinaten im Vertex-Format. Das Vertex-Format kann mehrere Sätze von Texturkoordinaten enthalten. Verwenden Sie die D3DFVF \_ TEX0 bis D3DFVF \_ TEX8 [D3DFVF](d3dfvf.md) , um ein Scheitelpunkt Format zu beschreiben, das keine Texturkoordinaten enthält, oder bis zu acht Sets.

Jeder Texturkoordinaten Satz kann zwischen einem und vier Elementen aufweisen. Die D3DFVF \_ TEXTUREFORMAT1 through D3DFVF \_ TEXTUREFORMAT4-Flags beschreiben die Anzahl von Elementen in einer Textur Koordinate in einer Menge, diese Flags werden jedoch nicht von sich selbst verwendet. Stattdessen verwendet der [**D3DFVF \_ texcoordsizen**](d3dfvf-texcoordsizen.md) -Satz von Makros diese Flags, um Bitmuster zu erstellen, die die Anzahl der Elemente beschreiben, die von einem bestimmten Satz von Texturkoordinaten im Vertex-Format verwendet werden. Diese Makros akzeptieren einen einzelnen Parameter, der den Index des Koordinaten Satzes identifiziert, dessen Anzahl von Elementen definiert wird. Im folgenden Beispiel wird veranschaulicht, wie diese Makros verwendet werden.


```
// This vertex format contains two sets of texture coordinates.
// The first set (index 0) has 2 elements, and the second set 
// has 1 element. The description for this vertex format would be: 
//     dwFVF = D3DFVF_XYZ  | D3DFVF_NORMAL | D3DFVF_DIFFUSE | D3DFVF_TEX2 |
//             D3DFVF_TEXCOORDSIZE2(0) | D3DFVF_TEXCOORDSIZE1(1); 
//
typedef struct CVF
{
    D3DVECTOR position;
    D3DVECTOR normal;
    D3DCOLOR  diffuse;
    float     u, v;   // 1st set, 2D
    float     t;      // 2nd set, 1D
} CustomVertexFormat;
```



> [!Note]  
> Mit Ausnahme von kubischen Umgebungs Zuordnungen und volumetexturen können Rasterizers keine Texturen mithilfe von mehr als zwei Elementen adressieren. Anwendungen können bis zu drei Elemente für eine Textur Koordinate bereitstellen, aber nur, wenn es sich bei der Textur um eine cubemap, eine volumetextur oder das \_ Flag D3DTTFF projiziertes Textur Transform handelt. Das \_ Flag D3DTTFF projibewirkt, dass der Raster die ersten beiden Elemente durch das dritte Element (oder n) dividiert. Weitere Informationen finden Sie unter [Texturkoordinaten Transformationen (Direct3D 9)](texture-coordinate-transformations.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturkoordinaten](texture-coordinates.md)
</dt> </dl>

 

 



