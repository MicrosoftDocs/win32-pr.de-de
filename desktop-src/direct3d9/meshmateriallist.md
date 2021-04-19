---
description: Wird in einem Mesh-Objekt verwendet, um anzugeben, welches Material für welche Gesichter gilt. Der nmaterials-Member gibt an, wie viele Materialien vorhanden sind, und Materialien geben an, welches Material angewendet werden soll.
ms.assetid: b38fd445-1a31-41ed-abbe-084abfe1c221
title: Meshmateriallist
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b746802dc3ef54a8feacc8ddfdaa0db1e45112b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106339645"
---
# <a name="meshmateriallist"></a><span data-ttu-id="234f4-104">Meshmateriallist</span><span class="sxs-lookup"><span data-stu-id="234f4-104">MeshMaterialList</span></span>

<span data-ttu-id="234f4-105">Wird in einem Mesh-Objekt verwendet, um anzugeben, welches Material für welche Gesichter gilt.</span><span class="sxs-lookup"><span data-stu-id="234f4-105">Used in a mesh object to specify which material applies to which faces.</span></span> <span data-ttu-id="234f4-106">Der nmaterials-Member gibt an, wie viele Materialien vorhanden sind, und Materialien geben an, welches Material angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="234f4-106">The nMaterials member specifies how many materials are present, and materials specify which material to apply.</span></span>

``` syntax
template MeshMaterialList
{
    < F6F23F42-7686-11CF-8F52-0040333594A3 >
    DWORD nMaterials;
    DWORD nFaceIndexes;
    array DWORD faceIndexes[nFaceIndexes];
    [Material <3D82AB4D-62DA-11CF-AB39-0020AF71E433>]
} 
```

<span data-ttu-id="234f4-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="234f4-107">Where:</span></span>

-   <span data-ttu-id="234f4-108">nmaterials: ein DWORD.</span><span class="sxs-lookup"><span data-stu-id="234f4-108">nMaterials - A DWORD.</span></span> <span data-ttu-id="234f4-109">Die Anzahl der Materialien.</span><span class="sxs-lookup"><span data-stu-id="234f4-109">The number of materials.</span></span>
-   <span data-ttu-id="234f4-110">nfakeindexes: ein DWORD.</span><span class="sxs-lookup"><span data-stu-id="234f4-110">nFaceIndexes - A DWORD.</span></span> <span data-ttu-id="234f4-111">Die Anzahl der Indizes.</span><span class="sxs-lookup"><span data-stu-id="234f4-111">The number of indices.</span></span>
-   <span data-ttu-id="234f4-112">fakeindexes \[ nfakeindexes \] : ein Array von DWords, das die Gesichts Indizes enthält.</span><span class="sxs-lookup"><span data-stu-id="234f4-112">faceIndexes\[nFaceIndexes\] - An array of DWORDs containing the face indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="234f4-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="234f4-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="234f4-114">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="234f4-114">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



