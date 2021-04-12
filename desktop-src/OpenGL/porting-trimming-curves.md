---
title: Portieren von Kürzungs Kurven
description: OpenGL-Kürzungs Kurven sind sehr ähnlich wie IRIS GL-Kürzungs Kurven. In der folgenden Tabelle sind die Iris GL-Funktionen zum Definieren von Kürzungs Kurven und ihre entsprechenden OpenGL-Funktionen aufgeführt.
ms.assetid: 9aeea9ca-5ecd-4be1-853d-45b1566b263b
keywords:
- IRIS GL portieren, Kürzungs Kurven
- Portieren von IRIS GL, kürzen von Kurven
- Portieren auf OpenGL von IRIS GL, kürzen von Kurven
- OpenGL-Portierung von IRIS GL, kürzen von Kurven
- Kürzen von Kurven
- Kurven
- IRIS GL portieren, Kurven
- Portieren von IRIS GL, Kurven
- Portieren auf OpenGL von IRIS GL, Kurven
- OpenGL-Portierung von IRIS GL, Kurven
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cc82822b2e0b9e66729f0cb1a0e939d2775999c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207148"
---
# <a name="porting-trimming-curves"></a><span data-ttu-id="92886-114">Portieren von Kürzungs Kurven</span><span class="sxs-lookup"><span data-stu-id="92886-114">Porting Trimming Curves</span></span>

<span data-ttu-id="92886-115">OpenGL-Kürzungs Kurven sind sehr ähnlich wie IRIS GL-Kürzungs Kurven.</span><span class="sxs-lookup"><span data-stu-id="92886-115">OpenGL trimming curves are very similar to IRIS GL trimming curves.</span></span> <span data-ttu-id="92886-116">In der folgenden Tabelle sind die Iris GL-Funktionen zum Definieren von Kürzungs Kurven und ihre entsprechenden OpenGL-Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="92886-116">The following table lists the IRIS GL functions for defining trimming curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="92886-117">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="92886-117">IRIS GL function</span></span> | <span data-ttu-id="92886-118">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="92886-118">OpenGL function</span></span>                        | <span data-ttu-id="92886-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="92886-119">Meaning</span></span>                              |
|------------------|----------------------------------------|--------------------------------------|
| <span data-ttu-id="92886-120">**bgntrim**</span><span class="sxs-lookup"><span data-stu-id="92886-120">**bgntrim**</span></span>      | [<span data-ttu-id="92886-121">**glubegintrim**</span><span class="sxs-lookup"><span data-stu-id="92886-121">**gluBeginTrim**</span></span>](glubegintrim.md)   | <span data-ttu-id="92886-122">Beginnt die Definition der Kürzungs Kurve.</span><span class="sxs-lookup"><span data-stu-id="92886-122">Begins trimming-curve definition.</span></span>    |
| <span data-ttu-id="92886-123">**pwlcurve**</span><span class="sxs-lookup"><span data-stu-id="92886-123">**pwlcurve**</span></span>     | [<span data-ttu-id="92886-124">**glupwlcurve**</span><span class="sxs-lookup"><span data-stu-id="92886-124">**gluPwlCurve**</span></span>](glupwlcurve.md)     | <span data-ttu-id="92886-125">Definiert eine schrittweise lineare Kurve.</span><span class="sxs-lookup"><span data-stu-id="92886-125">Defines a piecewise linear curve.</span></span>    |
| <span data-ttu-id="92886-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="92886-126">**nurbscurve**</span></span>   | [<span data-ttu-id="92886-127">**glunurbscurve**</span><span class="sxs-lookup"><span data-stu-id="92886-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="92886-128">Gibt Attribute der Kürzungs Kurve an.</span><span class="sxs-lookup"><span data-stu-id="92886-128">Specifies trimming-curve attributes.</span></span> |
| <span data-ttu-id="92886-129">**endtrim**</span><span class="sxs-lookup"><span data-stu-id="92886-129">**endtrim**</span></span>      | [<span data-ttu-id="92886-130">**gluendtrim**</span><span class="sxs-lookup"><span data-stu-id="92886-130">**gluEndTrim**</span></span>](gluendtrim.md)       | <span data-ttu-id="92886-131">Beendet die Definition der Kürzung der Kurve.</span><span class="sxs-lookup"><span data-stu-id="92886-131">Ends trimming-curve definition.</span></span>      |



 

<span data-ttu-id="92886-132">??</span><span class="sxs-lookup"><span data-stu-id="92886-132">??</span></span>

 

 




