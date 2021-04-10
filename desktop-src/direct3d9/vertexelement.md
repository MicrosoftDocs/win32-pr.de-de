---
description: Beschreibt ein einzelnes Vertex-Element in einer Scheitelpunkt Deklaration.
ms.assetid: efe3e98b-938d-4d4c-b790-2b8c8aab0ded
title: Vertexelement
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 049511c89b335c0da31a9f41344082c3b818fa0d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124742"
---
# <a name="vertexelement"></a><span data-ttu-id="70b0c-103">Vertexelement</span><span class="sxs-lookup"><span data-stu-id="70b0c-103">VertexElement</span></span>

<span data-ttu-id="70b0c-104">Beschreibt ein einzelnes Vertex-Element in einer Scheitelpunkt Deklaration.</span><span class="sxs-lookup"><span data-stu-id="70b0c-104">Describes an individual vertex element in a vertex declaration.</span></span>

``` syntax
template VertexElement 
{ 
    < F752461C-1E23-48f6-B9F8-8350850F336F > 
    DWORD Type; 
    DWORD Method; 
    DWORD Usage; 
    DWORD UsageIndex; 
} 
```

<span data-ttu-id="70b0c-105">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="70b0c-105">Where:</span></span>

-   <span data-ttu-id="70b0c-106">Type-Scheitelpunkt Datentyp.</span><span class="sxs-lookup"><span data-stu-id="70b0c-106">Type - Vertex data type.</span></span> <span data-ttu-id="70b0c-107">Siehe [**D3DDECLTYPE**](./d3ddecltype.md).</span><span class="sxs-lookup"><span data-stu-id="70b0c-107">See [**D3DDECLTYPE**](./d3ddecltype.md).</span></span>
-   <span data-ttu-id="70b0c-108">Method-Mosaik Verarbeitungsmethode.</span><span class="sxs-lookup"><span data-stu-id="70b0c-108">Method - Tessellator processing method.</span></span> <span data-ttu-id="70b0c-109">Siehe [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span><span class="sxs-lookup"><span data-stu-id="70b0c-109">See [**D3DDECLMETHOD**](./d3ddeclmethod.md).</span></span>
-   <span data-ttu-id="70b0c-110">Verwendungs orientierte Verwendung der Vertexdaten.</span><span class="sxs-lookup"><span data-stu-id="70b0c-110">Usage - Intended use of the vertex data.</span></span> <span data-ttu-id="70b0c-111">Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="70b0c-111">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>
-   <span data-ttu-id="70b0c-112">"Start": ändert die Verwendungs Daten.</span><span class="sxs-lookup"><span data-stu-id="70b0c-112">UsageIndex - Modifies the usage data.</span></span> <span data-ttu-id="70b0c-113">Siehe [**D3DDECLUSAGE**](./d3ddeclusage.md).</span><span class="sxs-lookup"><span data-stu-id="70b0c-113">See [**D3DDECLUSAGE**](./d3ddeclusage.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="70b0c-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70b0c-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70b0c-115">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="70b0c-115">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> <dt>

[<span data-ttu-id="70b0c-116">**D3DVERTEXELEMENT9**</span><span class="sxs-lookup"><span data-stu-id="70b0c-116">**D3DVERTEXELEMENT9**</span></span>](d3dvertexelement9.md)
</dt> </dl>

 

 
