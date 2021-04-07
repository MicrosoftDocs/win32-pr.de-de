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
# <a name="meshtexturecoords"></a><span data-ttu-id="7bd22-103">Meshtexturecoords</span><span class="sxs-lookup"><span data-stu-id="7bd22-103">MeshTextureCoords</span></span>

<span data-ttu-id="7bd22-104">Definiert die Texturkoordinaten eines Mesh.</span><span class="sxs-lookup"><span data-stu-id="7bd22-104">Defines a mesh's texture coordinates.</span></span>

``` syntax
template MeshTextureCoords
{
    < F6F23F40-7686-11cf-8F52-0040333594A3 >
    DWORD nTextureCoords;
    array Coords2d textureCoords[nTextureCoords] ;
} 
```

<span data-ttu-id="7bd22-105">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="7bd22-105">Where:</span></span>

-   <span data-ttu-id="7bd22-106">ntexturecoords-Anzahl der Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="7bd22-106">nTextureCoords - Number of texture coordinates.</span></span>
-   <span data-ttu-id="7bd22-107">Array Coords2d texturecoords \[ ntexturecoords \] -Array von 2D-Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="7bd22-107">array Coords2d textureCoords\[nTextureCoords\] - Array of 2D texture coordinates.</span></span> <span data-ttu-id="7bd22-108">Siehe [**Coords2d**](coords2d.md).</span><span class="sxs-lookup"><span data-stu-id="7bd22-108">See [**Coords2d**](coords2d.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="7bd22-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7bd22-109">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bd22-110">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="7bd22-110">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



