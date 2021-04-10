---
description: Definiert den Patch für ein B&\# 233; Zier Steuerelement. Das Array definiert die Steuerungs Punkte für den Patch.
ms.assetid: vs|directx_sdk|~\patch.htm
title: Patch
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 480457b3dd3800aca8b23210e3fe653b4e713e94
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103859977"
---
# <a name="patch"></a><span data-ttu-id="16a91-104">Patch</span><span class="sxs-lookup"><span data-stu-id="16a91-104">Patch</span></span>

<span data-ttu-id="16a91-105">Definiert einen Patch für das Bézier-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="16a91-105">Defines a Bézier control patch.</span></span> <span data-ttu-id="16a91-106">Das Array definiert die Steuerungs Punkte für den Patch.</span><span class="sxs-lookup"><span data-stu-id="16a91-106">The array defines the control points for the patch.</span></span>

``` syntax
template Patch
{
    < A3EB5D44-FC22-429D-9AFB-3221CB9719A6 >
    DWORD nControlIndices;
    array DWORD controlIndices[nControlIndices];
} 
```

<span data-ttu-id="16a91-107">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="16a91-107">Where:</span></span>

-   <span data-ttu-id="16a91-108">ncontrolindices-Anzahl von Steuerungspunkt Indizes.</span><span class="sxs-lookup"><span data-stu-id="16a91-108">nControlIndices - Number of control point indices.</span></span>
-   <span data-ttu-id="16a91-109">Array DWORD controlindices \[ ncontrolindices \] -Array von Steuerungspunkt Indizes.</span><span class="sxs-lookup"><span data-stu-id="16a91-109">array DWORD controlIndices\[nControlIndices\] - Array of control point indices.</span></span>

<span data-ttu-id="16a91-110">Der Typ des Patches wird durch die Anzahl von Kontrollpunkten definiert, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="16a91-110">The type of patch is defined by the number of control points, as shown in the following table.</span></span>



| <span data-ttu-id="16a91-111">Anzahl von Kontrollpunkten</span><span class="sxs-lookup"><span data-stu-id="16a91-111">Number of control points</span></span> | <span data-ttu-id="16a91-112">type</span><span class="sxs-lookup"><span data-stu-id="16a91-112">Type</span></span>                              |
|--------------------------|-----------------------------------|
| <span data-ttu-id="16a91-113">10</span><span class="sxs-lookup"><span data-stu-id="16a91-113">10</span></span>                       | <span data-ttu-id="16a91-114">Eckige, eckige Bézier-Patch</span><span class="sxs-lookup"><span data-stu-id="16a91-114">Cubic Bézier triangular patch</span></span>     |
| <span data-ttu-id="16a91-115">15</span><span class="sxs-lookup"><span data-stu-id="16a91-115">15</span></span>                       | <span data-ttu-id="16a91-116">Dreiecks-Patch für quartic Bézier</span><span class="sxs-lookup"><span data-stu-id="16a91-116">Quartic Bézier triangular patch</span></span>   |
| <span data-ttu-id="16a91-117">16</span><span class="sxs-lookup"><span data-stu-id="16a91-117">16</span></span>                       | <span data-ttu-id="16a91-118">Patch für Quad-Bézier-Quad-Rechteck</span><span class="sxs-lookup"><span data-stu-id="16a91-118">Cubic Bézier quad rectangle patch</span></span> |



 

<span data-ttu-id="16a91-119">Die Reihenfolge der Kontrollpunkte wird in einem Spiralmuster angegeben, wie in den folgenden Diagrammen für dreieckige und rechteckige Patches gezeigt.</span><span class="sxs-lookup"><span data-stu-id="16a91-119">The order of the control points are given in a spiral pattern, as shown in the following diagrams for triangular and rectangular patches.</span></span>

<span data-ttu-id="16a91-120">Für dreieckige Patches wird das folgende Muster verwendet.</span><span class="sxs-lookup"><span data-stu-id="16a91-120">Triangular patches use the following pattern.</span></span>

![Diagramm des Musters für dreieckige Patches](images/tripatch.png)

<span data-ttu-id="16a91-122">Rechteckige Patches verwenden das folgende Muster.</span><span class="sxs-lookup"><span data-stu-id="16a91-122">Rectangular patches use the following pattern.</span></span>

![Diagramm des Musters für rechteckige Patches](images/quadpatch.png)

## <a name="see-also"></a><span data-ttu-id="16a91-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16a91-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16a91-125">Vorlagen</span><span class="sxs-lookup"><span data-stu-id="16a91-125">Templates</span></span>](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



