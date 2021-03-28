---
description: Eine Anwendung kombiniert zwei Bereiche durch Aufrufen der combinergn-Funktion.
ms.assetid: d16f9ca5-33e2-4752-900e-743245838377
title: Kombinieren von Regionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f51db22daea448acfb02120844ca2859a5ba11e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563907"
---
# <a name="combining-regions"></a><span data-ttu-id="ce15b-103">Kombinieren von Regionen</span><span class="sxs-lookup"><span data-stu-id="ce15b-103">Combining Regions</span></span>

<span data-ttu-id="ce15b-104">Eine Anwendung kombiniert zwei Bereiche durch Aufrufen der [**combinergn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ce15b-104">An application combines two regions by calling the [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn) function.</span></span> <span data-ttu-id="ce15b-105">Mit dieser Funktion kann eine Anwendung die sich überschneidenden Teile von zwei Regionen kombinieren, wobei es sich um die überschneidenden Teile von zwei Regionen, die beiden ursprünglichen Bereiche in der Gesamtheit usw. handelt.</span><span class="sxs-lookup"><span data-stu-id="ce15b-105">Using this function, an application can combine the intersecting parts of two regions, all but the intersecting parts of two regions, the two original regions in their entirety, and so on.</span></span> <span data-ttu-id="ce15b-106">Im folgenden sind fünf Werte aufgeführt, die die Regions Kombinationen definieren.</span><span class="sxs-lookup"><span data-stu-id="ce15b-106">Following are five values that define the region combinations.</span></span>



| <span data-ttu-id="ce15b-107">Wert</span><span class="sxs-lookup"><span data-stu-id="ce15b-107">Value</span></span>     | <span data-ttu-id="ce15b-108">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ce15b-108">Meaning</span></span>                                                                               |
|-----------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ce15b-109">RGN \_ und</span><span class="sxs-lookup"><span data-stu-id="ce15b-109">RGN\_AND</span></span>  | <span data-ttu-id="ce15b-110">Die sich überschneidenden Teile zweier ursprünglicher Regionen definieren einen neuen Bereich.</span><span class="sxs-lookup"><span data-stu-id="ce15b-110">The intersecting parts of two original regions define a new region.</span></span>                   |
| <span data-ttu-id="ce15b-111">RGN- \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="ce15b-111">RGN\_COPY</span></span> | <span data-ttu-id="ce15b-112">Eine Kopie des ersten (der beiden ursprünglichen Regionen) definiert einen neuen Bereich.</span><span class="sxs-lookup"><span data-stu-id="ce15b-112">A copy of the first (of the two original regions) defines a new region.</span></span>               |
| <span data-ttu-id="ce15b-113">RGN- \_ diff</span><span class="sxs-lookup"><span data-stu-id="ce15b-113">RGN\_DIFF</span></span> | <span data-ttu-id="ce15b-114">Der Teil der ersten Region, der keine Schnittmenge überschneidet, definiert einen neuen Bereich.</span><span class="sxs-lookup"><span data-stu-id="ce15b-114">The part of the first region that does not intersect the second defines a new region.</span></span> |
| <span data-ttu-id="ce15b-115">RGN \_ oder</span><span class="sxs-lookup"><span data-stu-id="ce15b-115">RGN\_OR</span></span>   | <span data-ttu-id="ce15b-116">In den beiden ursprünglichen Regionen wird eine neue Region definiert.</span><span class="sxs-lookup"><span data-stu-id="ce15b-116">The two original regions define a new region.</span></span>                                         |
| <span data-ttu-id="ce15b-117">RGN- \_ Xor</span><span class="sxs-lookup"><span data-stu-id="ce15b-117">RGN\_XOR</span></span>  | <span data-ttu-id="ce15b-118">Die Teile der beiden ursprünglichen Bereiche, die sich nicht überlappen, definieren eine neue Region.</span><span class="sxs-lookup"><span data-stu-id="ce15b-118">Those parts of the two original regions that do not overlap define a new region.</span></span>      |



 

<span data-ttu-id="ce15b-119">Die folgende Abbildung zeigt die fünf möglichen Kombinationen eines Quadrats und einen kreisförmigen Bereich, der sich aus einem Rückruf von [**combinergn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn)ergibt.</span><span class="sxs-lookup"><span data-stu-id="ce15b-119">The following illustration shows the five possible combinations of a square and a circular region resulting from a call to [**CombineRgn**](/windows/desktop/api/Wingdi/nf-wingdi-combinergn).</span></span>

![Abbildung, die die in der vorherigen Tabelle beschriebenen Ergebnisse veranschaulicht](images/csrgn-02.png)

 

 



