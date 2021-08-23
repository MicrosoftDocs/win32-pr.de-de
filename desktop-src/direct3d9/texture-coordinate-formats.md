---
description: Texturkoordinaten in Direct3D können ein, zwei, drei oder vier Gleitkommaelemente enthalten, um Texturen mit unterschiedlichen Dimensionsebenen zu behandeln.
ms.assetid: d841af62-41b0-4b80-960b-4630b9a7210c
title: Texturkoordinatenformate (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c48ec28b9c99357fe8825f5ff79da3c8869719389c4a4bc4874c5740fc71f42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118519883"
---
# <a name="texture-coordinate-formats-direct3d-9"></a>Texturkoordinatenformate (Direct3D 9)

Texturkoordinaten in Direct3D können ein, zwei, drei oder vier Gleitkommaelemente enthalten, um Texturen mit unterschiedlichen Dimensionsebenen zu behandeln. Eine 1D-Textur – eine Texturoberfläche mit Dimensionen von 1-by-n-Texeln – wird von einer Texturkoordinate adressiert. Der häufigste Fall, 2D-Texturen, wird mit zwei Texturkoordinaten behandelt, die häufig als Sie und v bezeichnet werden. Direct3D unterstützt zwei Arten von 3D-Texturen: kubische Umgebungszuordnungen und Volumentexturen. Kubische Umgebungszuordnungen sind nicht wirklich 3D, aber sie werden mit einem 3-Element-Vektor adressiert. Weitere Informationen finden Sie unter [Kubische Umgebungszuordnung (Direct3D 9).](cubic-environment-mapping.md)

Wie unter [FVF-Codes für feste Funktionen (Direct3D 9)](fixed-function-fvf-codes.md)beschrieben, codieren Anwendungen Texturkoordinaten im Scheitelpunktformat. Das Scheitelpunktformat kann mehrere Sätze von Texturkoordinaten enthalten. Verwenden Sie D3DFVF \_ TEX0 bis D3DFVF \_ TEX8 [D3DFVF,](d3dfvf.md) um ein Scheitelpunktformat zu beschreiben, das keine Texturkoordinaten oder bis zu acht Sätze enthält.

Jeder Texturkoordinatensatz kann zwischen einem und vier Elementen enthalten. Die Flags D3DFVF \_ TEXTUREFORMAT1 bis D3DFVF \_ TEXTUREFORMAT4 beschreiben die Anzahl der Elemente in einer Texturkoordinate in einer Menge, aber diese Flags werden nicht allein verwendet. Stattdessen verwendet der [**D3DFVF \_ TEXCOORDSIZEN-Makrosatz**](d3dfvf-texcoordsizen.md) diese Flags, um Bitmuster zu erstellen, die die Anzahl der Elemente beschreiben, die von einem bestimmten Satz von Texturkoordinaten im Scheitelpunktformat verwendet werden. Diese Makros akzeptieren einen einzelnen Parameter, der den Index des Koordinatensatzes identifiziert, dessen Anzahl von Elementen definiert wird. Im folgenden Beispiel wird veranschaulicht, wie diese Makros verwendet werden.


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
> Mit Ausnahme von kubischen Umgebungszuordnungen und Volumentexturen können Rasterizer Texturen nicht mit mehr als zwei Elementen adressieren. Anwendungen können bis zu drei Elemente für eine Texturkoordinate bereitstellen, aber nur, wenn es sich bei der Textur um eine Cubemap, eine Volumentextur oder das D3DTTFF \_ PROJECTED-Texturtransformationsflag handelt. Das D3DTTFF \_ PROJECTED-Flag bewirkt, dass der Rasterizer die ersten beiden Elemente durch das dritte (oder n) Element dividiert. Weitere Informationen finden Sie unter [Transformationen für Texturkoordinaten (Direct3D 9).](texture-coordinate-transformations.md)

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturkoordinaten](texture-coordinates.md)
</dt> </dl>

 

 



