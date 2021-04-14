---
description: Gibt Scheitelpunkt Farben für ein Mesh an, anstatt ein Material pro Gesicht oder pro Mesh anzuwenden.
ms.assetid: 9ffd365f-11a5-420b-af5e-6a8be79a304c
title: Meshvertexcolors
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba55d601b29e0962c5d56e86ae052c454bf3adc7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392474"
---
# <a name="meshvertexcolors"></a><span data-ttu-id="87b73-103">Meshvertexcolors</span><span class="sxs-lookup"><span data-stu-id="87b73-103">MeshVertexColors</span></span>

<span data-ttu-id="87b73-104">Gibt Scheitelpunkt Farben für ein Mesh an, anstatt ein Material pro Gesicht oder pro Mesh anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="87b73-104">Specifies vertex colors for a mesh, instead of applying a material per face or per mesh.</span></span>

``` syntax
template MeshVertexColors
{
    <1630B821-7842-11cf-8F52-0040333594A3>
    DWORD nVertexColors;
    array IndexColor vertexColors[nVertexColors];
} 
```

<span data-ttu-id="87b73-105">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="87b73-105">Where:</span></span>

-   <span data-ttu-id="87b73-106">nvertexcolors: Anzahl der Farben.</span><span class="sxs-lookup"><span data-stu-id="87b73-106">nVertexColors - Number of colors.</span></span> <span data-ttu-id="87b73-107">Dies entspricht der Anzahl der Scheitel Punkte im Mesh.</span><span class="sxs-lookup"><span data-stu-id="87b73-107">This matches the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="87b73-108">Array indexcolor vertexcolors \[ nvertexcolors \] -Array von indizierten Farben.</span><span class="sxs-lookup"><span data-stu-id="87b73-108">array IndexColor vertexColors\[nVertexColors\] - Array of indexed colors.</span></span> <span data-ttu-id="87b73-109">Siehe [**indexedcolor**](indexedcolor.md).</span><span class="sxs-lookup"><span data-stu-id="87b73-109">See [**IndexedColor**](indexedcolor.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="87b73-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87b73-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87b73-111">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="87b73-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



