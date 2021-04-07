---
description: Definiert die Texturkoordinaten eines Mesh.
ms.assetid: c87eb176-b502-49b6-bc73-401cc46e8412
title: Meshtexturecoords
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 974ec31f4358578277cfac46dc014f34752df46a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745537"
---
# <a name="meshtexturecoords"></a>Meshtexturecoords

Definiert die Texturkoordinaten eines Mesh.

``` syntax
template MeshTextureCoords
{
    < F6F23F40-7686-11cf-8F52-0040333594A3 >
    DWORD nTextureCoords;
    array Coords2d textureCoords[nTextureCoords] ;
} 
```

Hierbei gilt:

-   ntexturecoords-Anzahl der Texturkoordinaten.
-   Array Coords2d texturecoords \[ ntexturecoords \] -Array von 2D-Texturkoordinaten. Siehe [**Coords2d**](coords2d.md).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Vorlagen](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



