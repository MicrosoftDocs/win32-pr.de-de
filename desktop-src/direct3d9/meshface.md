---
description: Wird von der Mesh-Vorlage verwendet, um die Gesichter eines Netzes zu definieren. Jedes Element des nfakevertexindices-Arrays verweist auf einen Mesh-Vertex, der zum Erstellen der Vorderseite verwendet wird.
ms.assetid: 38c40ebe-eca2-4dd9-95b8-b396225e3050
title: Meshface
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a9e8b73efb214f7a767d986830cccc83ee6cbc1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123445"
---
# <a name="meshface"></a><span data-ttu-id="46996-104">Meshface</span><span class="sxs-lookup"><span data-stu-id="46996-104">MeshFace</span></span>

<span data-ttu-id="46996-105">Wird von der [**Mesh**](mesh.md) -Vorlage verwendet, um die Gesichter eines Netzes zu definieren.</span><span class="sxs-lookup"><span data-stu-id="46996-105">Used by the [**Mesh**](mesh.md) template to define a mesh's faces.</span></span> <span data-ttu-id="46996-106">Jedes Element des nfakevertexindices-Arrays verweist auf einen Mesh-Vertex, der zum Erstellen der Vorderseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="46996-106">Each element of the nFaceVertexIndices array references a mesh vertex used to build the face.</span></span>

``` syntax
template MeshFace
{
    < 3D82AB5F-62DA-11cf-AB39-0020AF71E433 >
    DWORD nFaceVertexIndices;
    array DWORD faceVertexIndices[nFaceVertexIndices];
} 
```

<span data-ttu-id="46996-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="46996-107">Where:</span></span>

-   <span data-ttu-id="46996-108">nfakevertexindices: Anzahl der Indizes.</span><span class="sxs-lookup"><span data-stu-id="46996-108">nFaceVertexIndices - Number of indices.</span></span>
-   <span data-ttu-id="46996-109">Array DWORD Facetten Index \[ nfakevertexindices \] -Array von Indizes.</span><span class="sxs-lookup"><span data-stu-id="46996-109">array DWORD faceVertexIndices\[nFaceVertexIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="46996-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46996-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46996-111">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="46996-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



