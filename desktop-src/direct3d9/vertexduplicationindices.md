---
description: Diese Vorlage wird pro Mesh instanziiert und enthält Informationen darüber, welche Scheitel Punkte im Mesh Duplikate zueinander sind.
ms.assetid: 43417389-69c1-4af6-92c2-75b621f9c165
title: Vertexduplicationindizes
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42d62278c206032c9a2dfed6ce9b2cd36c5e7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106341086"
---
# <a name="vertexduplicationindices"></a><span data-ttu-id="30d16-103">Vertexduplicationindizes</span><span class="sxs-lookup"><span data-stu-id="30d16-103">VertexDuplicationIndices</span></span>

<span data-ttu-id="30d16-104">Diese Vorlage wird pro Mesh instanziiert und enthält Informationen darüber, welche Scheitel Punkte im Mesh Duplikate zueinander sind.</span><span class="sxs-lookup"><span data-stu-id="30d16-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="30d16-105">Dupliziert das Ergebnis, wenn sich ein Scheitelpunkt auf einer Glättungs Gruppe oder Material Grenze befindet.</span><span class="sxs-lookup"><span data-stu-id="30d16-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="30d16-106">Der Zweck dieser Vorlage besteht darin, dem Lade Modul zu gestatten, zu bestimmen, welche Scheitel Punkte, die verschiedene Peripherie Parameter aufweisen, tatsächlich die gleichen vertexen im Modell sind.</span><span class="sxs-lookup"><span data-stu-id="30d16-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="30d16-107">Bestimmte Anwendungen (z. b. die Mesh-Vereinfachung) können diese Informationen nutzen.</span><span class="sxs-lookup"><span data-stu-id="30d16-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template VertexDuplicationIndices 
{ 
    < B8D65549-D7C9-4995-89CF-53A9A8B031E3 > 
    DWORD nIndices; 
    DWORD nOriginalVertices; 
    array DWORD indices[nIndices]; 
}
```

<span data-ttu-id="30d16-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="30d16-108">Where:</span></span>

-   <span data-ttu-id="30d16-109">nindizes-Anzahl der Scheitelpunkt Indizes.</span><span class="sxs-lookup"><span data-stu-id="30d16-109">nIndices - Number of vertex indices.</span></span> <span data-ttu-id="30d16-110">Dies ist die Anzahl der Scheitel Punkte im Mesh.</span><span class="sxs-lookup"><span data-stu-id="30d16-110">This is the number of vertices in the mesh.</span></span>
-   <span data-ttu-id="30d16-111">noriginalvertices: Anzahl der Scheitel Punkte im Mesh, bevor eine Duplizierung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="30d16-111">nOriginalVertices - Number of vertices in the mesh before any duplication occurs.</span></span>
-   <span data-ttu-id="30d16-112">Die Wert Indizes \[ n enthalten \] den Vertexindex, den Vertex \[ n \] im Vertex-Array für das Mesh hätte hätten, wenn keine Duplizierung aufgetreten wäre.</span><span class="sxs-lookup"><span data-stu-id="30d16-112">The value indices\[n\] holds the vertex index that vertex\[n\] in the vertex array for the mesh would have had if no duplication had occurred.</span></span> <span data-ttu-id="30d16-113">Indizes in diesem Array, die gleich sind, weisen auf doppelte Scheitel Punkte hin.</span><span class="sxs-lookup"><span data-stu-id="30d16-113">Indices in this array that are the same, therefore, indicate duplicate vertices.</span></span>

## <a name="see-also"></a><span data-ttu-id="30d16-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30d16-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30d16-115">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="30d16-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



