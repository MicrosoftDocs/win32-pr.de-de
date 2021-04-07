---
description: Diese Vorlage wird pro Mesh instanziiert und enthält Informationen darüber, welche Scheitel Punkte im Mesh Duplikate zueinander sind.
ms.assetid: dd30b3d6-767a-4d87-9b5c-1324738bcbb2
title: Facefaceency
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a2fd0f0b2bb328aa8b5ec39e7481c0b7fd766fc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745569"
---
# <a name="faceadjacency"></a><span data-ttu-id="ab02f-103">Facefaceency</span><span class="sxs-lookup"><span data-stu-id="ab02f-103">FaceAdjacency</span></span>

<span data-ttu-id="ab02f-104">Diese Vorlage wird pro Mesh instanziiert und enthält Informationen darüber, welche Scheitel Punkte im Mesh Duplikate zueinander sind.</span><span class="sxs-lookup"><span data-stu-id="ab02f-104">This template is instantiated on a per-mesh basis, holding information about which vertices in the mesh are duplicates of each other.</span></span> <span data-ttu-id="ab02f-105">Dupliziert das Ergebnis, wenn sich ein Scheitelpunkt auf einer Glättungs Gruppe oder Material Grenze befindet.</span><span class="sxs-lookup"><span data-stu-id="ab02f-105">Duplicates result when a vertex sits on a smoothing group or material boundary.</span></span> <span data-ttu-id="ab02f-106">Der Zweck dieser Vorlage besteht darin, dem Lade Modul zu gestatten, zu bestimmen, welche Scheitel Punkte, die verschiedene Peripherie Parameter aufweisen, tatsächlich die gleichen vertexen im Modell sind.</span><span class="sxs-lookup"><span data-stu-id="ab02f-106">The purpose of this template is to allow the loader to determine which vertices exhibiting different peripheral parameters are actually the same vertexes in the model.</span></span> <span data-ttu-id="ab02f-107">Bestimmte Anwendungen (z. b. die Mesh-Vereinfachung) können diese Informationen nutzen.</span><span class="sxs-lookup"><span data-stu-id="ab02f-107">Certain applications (mesh simplification, for example) can make use of this information.</span></span>

``` syntax
template FaceAdjacency
{
    < A64C844A-E282-4756-8B80-250CDE04398C >
    DWORD nIndices;
    array DWORD indices[nIndices];
} 
```

<span data-ttu-id="ab02f-108">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="ab02f-108">Where:</span></span>

-   <span data-ttu-id="ab02f-109">nindizes: Anzahl der Indizes im Mesh.</span><span class="sxs-lookup"><span data-stu-id="ab02f-109">nIndices - Number of indices in the mesh.</span></span>
-   <span data-ttu-id="ab02f-110">Indizes \[ nindizes \] -Array von Indizes.</span><span class="sxs-lookup"><span data-stu-id="ab02f-110">indices\[nIndices\] - Array of indices.</span></span>

## <a name="see-also"></a><span data-ttu-id="ab02f-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab02f-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab02f-112">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="ab02f-112">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



