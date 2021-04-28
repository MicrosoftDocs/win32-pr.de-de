---
description: 'VertexDuplicationIndices: Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelpunkte im Gitternetz dupliziert sind.'
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: VertexDuplicationIndices
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b33a8c5fca4f479eec6e9864d4528d4e3e4a1e32
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090178"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="4b92d-103">VertexDuplicationIndices</span><span class="sxs-lookup"><span data-stu-id="4b92d-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="4b92d-104">Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelungen im Gitternetz Duplikate voneinander sind.</span><span class="sxs-lookup"><span data-stu-id="4b92d-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="4b92d-105">Duplikate ergeben sich, wenn sich ein Scheitelpunkt an einer Glättungsgruppe oder Materialgrenze befindet.</span><span class="sxs-lookup"><span data-stu-id="4b92d-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="4b92d-106">Mit dieser Vorlage soll dem Lader ermöglicht werden, zu bestimmen, welche Scheitelpunkte, die verschiedene Peripherieparameter enthalten, tatsächlich dieselben Scheitelpunkte im Modell sind.</span><span class="sxs-lookup"><span data-stu-id="4b92d-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="4b92d-107">Bestimmte Anwendungen (z. B. die Mesh-Vereinfachung) können diese Informationen nutzen.</span><span class="sxs-lookup"><span data-stu-id="4b92d-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="4b92d-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="4b92d-108">Where:</span></span>

-   <span data-ttu-id="4b92d-109">nIndices : Anzahl der Scheitelpunktindizes.</span><span class="sxs-lookup"><span data-stu-id="4b92d-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="4b92d-110">Dies ist die Anzahl der Scheitelzeichen im Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="4b92d-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="4b92d-111">nOriginalVertices: Anzahl der Scheitelzeichen im Netz, bevor dupliziert wird.</span><span class="sxs-lookup"><span data-stu-id="4b92d-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="4b92d-112">Die Wertindizes n enthalten den Scheitelpunktindex, den Scheitelpunkt n im Vertexarray für das Gitternetz hätte, wenn keine \[ \] \[ \] Duplizierung aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="4b92d-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="4b92d-113">Indizes in diesem Array, die identisch sind, weisen daher auf doppelte Scheitelungen hin.</span><span class="sxs-lookup"><span data-stu-id="4b92d-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b92d-114">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="4b92d-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b92d-115">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="4b92d-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



