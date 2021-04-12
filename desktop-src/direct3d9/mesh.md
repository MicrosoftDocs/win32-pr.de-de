---
description: Definiert ein einfaches Mesh. Das erste Array ist eine Liste von Scheitel Punkten, während das zweite Array die Gesichter des Netzes durch Indizierung in das vertexarray definiert.
ms.assetid: vs|directx_sdk|~\mesh.htm
title: Mesh
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ced60785a5f013db7fc26e4d203119a160953b65
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480699"
---
# <a name="mesh"></a><span data-ttu-id="54a97-104">Mesh</span><span class="sxs-lookup"><span data-stu-id="54a97-104">Mesh</span></span>

<span data-ttu-id="54a97-105">Definiert ein einfaches Mesh.</span><span class="sxs-lookup"><span data-stu-id="54a97-105">Defines a simple mesh.</span></span> <span data-ttu-id="54a97-106">Das erste Array ist eine Liste von Scheitel Punkten, während das zweite Array die Gesichter des Netzes durch Indizierung in das vertexarray definiert.</span><span class="sxs-lookup"><span data-stu-id="54a97-106">The first array is a list of vertices, and the second array defines the faces of the mesh by indexing into the vertex array.</span></span>

``` syntax
template Mesh
{
    <3D82AB44-62DA-11CF-AB39-0020AF71E433>
    DWORD nVertices;
    array Vector vertices[nVertices];
    DWORD nFaces;
    array MeshFace faces[nFaces];
    [...]
}
```

<span data-ttu-id="54a97-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="54a97-107">Where:</span></span>

-   <span data-ttu-id="54a97-108">nvertices-Anzahl der Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="54a97-108">nVertices - Number of vertices.</span></span>
-   <span data-ttu-id="54a97-109">Array Vektor vertices \[ nvertices \] -Array von Vertices, jeweils vom Typ "Vector".</span><span class="sxs-lookup"><span data-stu-id="54a97-109">array Vector vertices\[nVertices\] - Array of vertices, each of type Vector.</span></span> <span data-ttu-id="54a97-110">Siehe [**Vektor**](vector.md).</span><span class="sxs-lookup"><span data-stu-id="54a97-110">See [**Vector**](vector.md).</span></span>
-   <span data-ttu-id="54a97-111">ngesichter: Anzahl der Flächen.</span><span class="sxs-lookup"><span data-stu-id="54a97-111">nFaces - Number of faces.</span></span>
-   <span data-ttu-id="54a97-112">Array meshface Gesichter \[ ngesichter \] -Array von Gesichtern, jeweils vom Typ "meshface".</span><span class="sxs-lookup"><span data-stu-id="54a97-112">array MeshFace faces\[nFaces\] - Array of faces, each of type MeshFace.</span></span> <span data-ttu-id="54a97-113">Siehe [**meshface**](meshface.md).</span><span class="sxs-lookup"><span data-stu-id="54a97-113">See [**MeshFace**](meshface.md).</span></span>
-   <span data-ttu-id="54a97-114">\[ ... \] -Eine beliebige x-Datei Vorlage kann hier verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54a97-114">\[ ... \] - Any .x file template can be used here.</span></span> <span data-ttu-id="54a97-115">Dadurch wird die Architektur erweiterbar.</span><span class="sxs-lookup"><span data-stu-id="54a97-115">This makes the architecture extensible.</span></span> <span data-ttu-id="54a97-116">[**Material**](material.md) -und [**texturefilename**](texturefilename.md) -Vorlagen werden in der Regel verwendet.</span><span class="sxs-lookup"><span data-stu-id="54a97-116">[**Material**](material.md) and [**TextureFilename**](texturefilename.md) templates are typically used.</span></span>

## <a name="see-also"></a><span data-ttu-id="54a97-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54a97-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54a97-118">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="54a97-118">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



