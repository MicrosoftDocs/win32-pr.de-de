---
description: 'FaceAdencyency: Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelpunkte im Netz Duplikate voneinander sind.'
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: FaceAdencyency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0508b822f45c6796a793dc4b17caeaa1e30b4c3d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090508"
---
# <a name="faceadjacency"></a><span data-ttu-id="1c07e-103">FaceAdencyency</span><span class="sxs-lookup"><span data-stu-id="1c07e-103">FaceAdjacency</span></span>

<span data-ttu-id="1c07e-104">Diese Vorlage wird pro Gitternetz instanziiert und enthält Informationen darüber, welche Scheitelpunkte im Netz Duplikate voneinander sind.</span><span class="sxs-lookup"><span data-stu-id="1c07e-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="1c07e-105">Duplikate ergeben sich, wenn sich ein Scheitelpunkt an einer Glättungsgruppe oder Materialgrenze befindet.</span><span class="sxs-lookup"><span data-stu-id="1c07e-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="1c07e-106">Der Zweck dieser Vorlage besteht darin, dem Ladeprogramm zu ermöglichen, zu bestimmen, welche Scheitelpunkte mit unterschiedlichen Peripherieparametern tatsächlich die gleichen Scheitelpunkte im Modell sind.</span><span class="sxs-lookup"><span data-stu-id="1c07e-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="1c07e-107">Bestimmte Anwendungen (z. B. Mesh-Vereinfachung) können diese Informationen nutzen.</span><span class="sxs-lookup"><span data-stu-id="1c07e-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="1c07e-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="1c07e-108">Where:</span></span>

-   <span data-ttu-id="1c07e-109">nIndices: Anzahl der Indizes im Gitternetz.</span><span class="sxs-lookup"><span data-stu-id="1c07e-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="1c07e-110">indizes \[ nIndices: \] Array von Indizes.</span><span class="sxs-lookup"><span data-stu-id="1c07e-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="1c07e-111">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="1c07e-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c07e-112">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="1c07e-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



