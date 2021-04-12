---
description: Beschreibt eine Scheitelpunkt Deklaration.
ms.assetid: 6a95bdf6-8767-4ad3-bcec-b32858d25571
title: Decldata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89a26d667f853db3044db3155c55eb4a6d941c6e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481115"
---
# <a name="decldata"></a><span data-ttu-id="21d2f-103">Decldata</span><span class="sxs-lookup"><span data-stu-id="21d2f-103">DeclData</span></span>

<span data-ttu-id="21d2f-104">Beschreibt eine Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="21d2f-104">Describes a vertex declaration.</span></span>

``` syntax
template DeclData
{
    < BF22E553-292C-4781-9FEA-62BD554BDD93 >
    DWORD nElements;
    array VertexElement Elements[nElements];
    DWORD nDWords;
    array DWORD data[nDWords];
} 
```

<span data-ttu-id="21d2f-105">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="21d2f-105">Where:</span></span>

-   <span data-ttu-id="21d2f-106">nelements: Anzahl der Scheitelpunkt Deklarations Elemente.</span><span class="sxs-lookup"><span data-stu-id="21d2f-106">nElements - Number of vertex declaration elements.</span></span>
-   <span data-ttu-id="21d2f-107">Elemente \[ nelements \] -Array von Vertex-Deklarations Elementen.</span><span class="sxs-lookup"><span data-stu-id="21d2f-107">Elements\[nElements\] - Array of vertex declaration elements.</span></span>
-   <span data-ttu-id="21d2f-108">ndwords: Anzahl der DWORDs.</span><span class="sxs-lookup"><span data-stu-id="21d2f-108">nDWords - Number of DWORDS.</span></span>
-   <span data-ttu-id="21d2f-109">Data \[ ndwords \] : Array von DWords, die die Daten in jedem Scheitelpunkt Element enthalten.</span><span class="sxs-lookup"><span data-stu-id="21d2f-109">data\[nDWords\] - Array of DWORDS that contain the data in each vertex element.</span></span>

## <a name="see-also"></a><span data-ttu-id="21d2f-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21d2f-110">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21d2f-111">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="21d2f-111">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



