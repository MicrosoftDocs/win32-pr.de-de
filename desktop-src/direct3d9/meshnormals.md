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
# <a name="meshnormals"></a><span data-ttu-id="c30ab-103">Meshnormals</span><span class="sxs-lookup"><span data-stu-id="c30ab-103">MeshNormals</span></span>

<span data-ttu-id="c30ab-104">Definiert normale für ein Mesh.</span><span class="sxs-lookup"><span data-stu-id="c30ab-104">Defines normals for a mesh.</span></span> <span data-ttu-id="c30ab-105">Das erste Array von Vektoren stellt die normalen Vektoren selbst dar, und das zweite Array ist ein Array von Indizes, das angibt, welche normale auf eine bestimmte Fläche angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c30ab-105">The first array of vectors is the normal vectors themselves, and the second array is an array of indexes specifying which normals should be applied to a given face.</span></span> <span data-ttu-id="c30ab-106">Der Wert des nfakenormals-Members sollte gleich der Anzahl der Gesichter in einem Mesh sein.</span><span class="sxs-lookup"><span data-stu-id="c30ab-106">The value of the nFaceNormals member should be equal to the number of faces in a mesh.</span></span>

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

<span data-ttu-id="c30ab-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="c30ab-107">Where:</span></span>

-   <span data-ttu-id="c30ab-108">nnormals-Anzahl der Normals.</span><span class="sxs-lookup"><span data-stu-id="c30ab-108">nNormals - Number of normals.</span></span>
-   <span data-ttu-id="c30ab-109">Array Vektor normale \[ nnormals \] -Array von normale.</span><span class="sxs-lookup"><span data-stu-id="c30ab-109">array Vector normals\[nNormals\] - Array of normals.</span></span> <span data-ttu-id="c30ab-110">Siehe [**Vektor**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="c30ab-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="c30ab-111">nfakenormals-Anzahl der Gesichts normale.</span><span class="sxs-lookup"><span data-stu-id="c30ab-111">nFaceNormals - Number of face normals.</span></span>
-   <span data-ttu-id="c30ab-112">Array meshface fakenormals \[ nfakenormals \] -Array von Netz Gesicht normalen.</span><span class="sxs-lookup"><span data-stu-id="c30ab-112">array MeshFace faceNormals\[nFaceNormals\] - Array of mesh face normals.</span></span> <span data-ttu-id="c30ab-113">Siehe [**meshface**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="c30ab-113">See [**MeshFace**](meshface.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="c30ab-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c30ab-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c30ab-115">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="c30ab-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



