---
description: Diese Vorlage wird pro Mesh instanziiert.
ms.assetid: ac5289c6-989c-43b4-9190-ac8f831a05f0
title: Skingewichtungen
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759239a3a7ec8ebb608cf9ede6624105cee321b4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520883"
---
# <a name="skinweights"></a><span data-ttu-id="597fa-103">Skingewichtungen</span><span class="sxs-lookup"><span data-stu-id="597fa-103">SkinWeights</span></span>

<span data-ttu-id="597fa-104">Diese Vorlage wird pro Mesh instanziiert.</span><span class="sxs-lookup"><span data-stu-id="597fa-104">This template is instantiated on a per-mesh basis.</span></span> <span data-ttu-id="597fa-105">Innerhalb eines Netzes wird eine Sequenz von n Instanzen dieser Vorlage angezeigt, wobei n die Anzahl der Knochen (X-Datei Rahmen) ist, die die Scheitel Punkte im Mesh beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="597fa-105">Within a mesh, a sequence of n instances of this template will appear, where n is the number of bones (X file frames) that influence the vertices in the mesh.</span></span> <span data-ttu-id="597fa-106">Jede Instanz der Vorlage definiert im Grunde den Einfluss eines bestimmten Knochen im Mesh.</span><span class="sxs-lookup"><span data-stu-id="597fa-106">Each instance of the template basically defines the influence of a particular bone on the mesh.</span></span> <span data-ttu-id="597fa-107">Es gibt eine Liste der Scheitelpunkt Indizes und eine entsprechende Liste von Gewichtungen.</span><span class="sxs-lookup"><span data-stu-id="597fa-107">There is a list of vertex indices, and a corresponding list of weights.</span></span>

``` syntax
template SkinWeights 
{ 
    < 6F0D123B-BAD2-4167-A0D0-80224F25FABB > 
    STRING transformNodeName; 
    DWORD nWeights; 
    array DWORD vertexIndices[nWeights]; 
    array float weights[nWeights]; 
    Matrix4x4 matrixOffset; 
} 
```

<span data-ttu-id="597fa-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="597fa-108">Where:</span></span>

-   <span data-ttu-id="597fa-109">Der Name des Knochens, dessen Auswirkung definiert wird, ist transformnodename, und ngewichtet ist die Anzahl der Scheitel Punkte, die von diesem Knochen betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="597fa-109">The name of the bone whose influence is being defined is transformNodeName, and nWeights is the number of vertices affected by this bone.</span></span>
-   <span data-ttu-id="597fa-110">Die Scheitel Punkte, die von diesem Knochen beeinflusst werden, sind in vertexindizes enthalten, und die Gewichtungen für die einzelnen Scheitel Punkte, die von diesem Knochen beeinflusst werden, sind in Gewichtungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="597fa-110">The vertices influenced by this bone are contained in vertexIndices, and the weights for each of the vertices influenced by this bone are contained in weights.</span></span>
-   <span data-ttu-id="597fa-111">Matrix matrixoffset wandelt die Gitter Scheitel Punkte in den Raum des Knochens um.</span><span class="sxs-lookup"><span data-stu-id="597fa-111">The matrix matrixOffset transforms the mesh vertices to the space of the bone.</span></span> <span data-ttu-id="597fa-112">Bei der Verkettung mit der Transformation des Streams werden dadurch die Raumkoordinaten des Netzes bereitstellt, die vom Knochen betroffen sind.</span><span class="sxs-lookup"><span data-stu-id="597fa-112">When concatenated to the bone's transform, this provides the world space coordinates of the mesh as affected by the bone.</span></span> <span data-ttu-id="597fa-113">Siehe [**Matrix4x4**](matrix4x4.md).</span><span class="sxs-lookup"><span data-stu-id="597fa-113">See [**Matrix4x4**](matrix4x4.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="597fa-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="597fa-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="597fa-115">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="597fa-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



