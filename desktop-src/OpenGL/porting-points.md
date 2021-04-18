---
title: Portieren von Punkten
description: OpenGL hat keinen Befehl zum Zeichnen eines einzelnen Punkts. Andernfalls ist das Portieren von Punkt Funktionen einfach. In der folgenden Tabelle sind die Funktionen von IRIS GL für Zeichnungs Punkte und ihre entsprechenden OpenGL-Funktionen aufgelistet.
ms.assetid: 348c7767-321a-43c6-bc88-7dc00f426f50
keywords:
- IRIS GL portieren, Punkte
- Portieren von IRIS GL, Points
- Portieren auf OpenGL von IRIS GL, Points
- OpenGL-Portierung von IRIS GL, Points
- Zeichnungsfunktionen, Punkte
- Punkte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 322413cd6a11a589884bce2628e229984c7936ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338602"
---
# <a name="porting-points"></a><span data-ttu-id="7bce9-111">Portieren von Punkten</span><span class="sxs-lookup"><span data-stu-id="7bce9-111">Porting Points</span></span>

<span data-ttu-id="7bce9-112">OpenGL hat keinen Befehl zum Zeichnen eines einzelnen Punkts.</span><span class="sxs-lookup"><span data-stu-id="7bce9-112">OpenGL has no command to draw a single point.</span></span> <span data-ttu-id="7bce9-113">Andernfalls ist das Portieren von Punkt Funktionen einfach.</span><span class="sxs-lookup"><span data-stu-id="7bce9-113">Otherwise, porting point functions is straightforward.</span></span> <span data-ttu-id="7bce9-114">In der folgenden Tabelle sind die Funktionen von IRIS GL für Zeichnungs Punkte und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="7bce9-114">The following table lists IRIS GL functions for drawing points and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="7bce9-115">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bce9-115">IRIS GL function</span></span>           | <span data-ttu-id="7bce9-116">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="7bce9-116">OpenGL function</span></span>                                                   | <span data-ttu-id="7bce9-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7bce9-117">Meaning</span></span>                                                                                                                                              |
|----------------------------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bce9-118">**Pnt**</span><span class="sxs-lookup"><span data-stu-id="7bce9-118">**pnt**</span></span>                    |                                                                   | <span data-ttu-id="7bce9-119">Zeichnet einen einzelnen Punkt.</span><span class="sxs-lookup"><span data-stu-id="7bce9-119">Draws a single point.</span></span>                                                                                                                                |
| <span data-ttu-id="7bce9-120">**bgnpoint**, **Endpunkt**</span><span class="sxs-lookup"><span data-stu-id="7bce9-120">**bgnpoint**, **endpoint**</span></span> | <span data-ttu-id="7bce9-121">[**glBegin**](glbegin.md) (GL- \_ Punkte), [ **glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="7bce9-121">[**glBegin**](glbegin.md) ( GL\_POINTS ), [**glEnd**](glend.md)</span></span> | <span data-ttu-id="7bce9-122">Interpretiert Scheitel Punkte als Punkte.</span><span class="sxs-lookup"><span data-stu-id="7bce9-122">Interprets vertices as points.</span></span>                                                                                                                       |
| <span data-ttu-id="7bce9-123">**pntsize**</span><span class="sxs-lookup"><span data-stu-id="7bce9-123">**pntsize**</span></span>                | [<span data-ttu-id="7bce9-124">**glPointSize**</span><span class="sxs-lookup"><span data-stu-id="7bce9-124">**glPointSize**</span></span>](glpointsize.md)                                | <span data-ttu-id="7bce9-125">Legt die Punktgröße in Pixel fest.</span><span class="sxs-lookup"><span data-stu-id="7bce9-125">Sets point size in pixels.</span></span>                                                                                                                           |
| <span data-ttu-id="7bce9-126">**PNP**</span><span class="sxs-lookup"><span data-stu-id="7bce9-126">**pntsmooth**</span></span>              | <span data-ttu-id="7bce9-127">[**glEnable**](glenable.md) (GL- \_ Punkt \_ glatt)</span><span class="sxs-lookup"><span data-stu-id="7bce9-127">[**glEnable**](glenable.md) ( GL\_POINT\_SMOOTH )</span></span>                | <span data-ttu-id="7bce9-128">Schaltet das Antialiasing von Punkten um.</span><span class="sxs-lookup"><span data-stu-id="7bce9-128">Turns on point antialiasing.</span></span> <span data-ttu-id="7bce9-129">(Weitere Informationen zum Punkt-Antialiasing finden Sie unter [Portieren von Antialiasing-Funktionen](porting-antialiasing-functions.md).)</span><span class="sxs-lookup"><span data-stu-id="7bce9-129">(For more information on point antialiasing, see [Porting Antialiasing Functions](porting-antialiasing-functions.md).)</span></span> |



 

<span data-ttu-id="7bce9-130">Weitere Informationen zu verwandten Get-Funktionen finden Sie unter [**glPointSize**](glpointsize.md).</span><span class="sxs-lookup"><span data-stu-id="7bce9-130">For information about related get functions, see [**glPointSize**](glpointsize.md).</span></span>

<span data-ttu-id="7bce9-131">??</span><span class="sxs-lookup"><span data-stu-id="7bce9-131">??</span></span>

 

 




