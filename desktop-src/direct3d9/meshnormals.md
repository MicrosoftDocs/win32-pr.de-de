---
description: Definiert normale für ein Mesh.
ms.assetid: 05f17128-dfc9-4a78-b23c-0420a1c3d1bd
title: Meshnormals
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65b9e0ffc89af5a0a55ef7bd1fa2575a4943137e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213929"
---
# <a name="meshnormals"></a>Meshnormals

Definiert normale für ein Mesh. Das erste Array von Vektoren stellt die normalen Vektoren selbst dar, und das zweite Array ist ein Array von Indizes, das angibt, welche normale auf eine bestimmte Fläche angewendet werden sollen. Der Wert des nfakenormals-Members sollte gleich der Anzahl der Gesichter in einem Mesh sein.

``` syntax
template MeshNormals
{
    < F6F23F43-7686-11cf-8F52-0040333594A3 >
    DWORD nNormals;
    array Vector normals[nNormals];
    DWORD nFaceNormals;
    array MeshFace faceNormals[nFaceNormals];
} 
```

Hierbei gilt:

-   nnormals-Anzahl der Normals.
-   Array Vektor normale \[ nnormals \] -Array von normale. Siehe [**Vektor**](vector.md).
-   nfakenormals-Anzahl der Gesichts normale.
-   Array meshface fakenormals \[ nfakenormals \] -Array von Netz Gesicht normalen. Siehe [**meshface**](meshface.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



