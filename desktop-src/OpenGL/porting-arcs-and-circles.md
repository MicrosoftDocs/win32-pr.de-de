---
title: Portieren von Arcs und Kreisen
description: Bei OpenGL werden gefüllte Bögen und Kreise mit denselben aufrufen wie nicht gefüllte Bögen und Kreise gezeichnet. In der folgenden Tabelle werden die Funktionen "IRIS GL Arc" und "Circle" und ihre entsprechenden OpenGL (GLU)-Funktionen aufgelistet.
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- IRIS GL portieren, Arcs
- Portieren von IRIS GL, Arcs
- Portieren auf OpenGL von IRIS GL, Arcs
- OpenGL-Portierung von IRIS GL, Arcs
- Zeichnungsfunktionen, Arcs
- IRIS GL portieren, Kreise
- Portieren von IRIS GL, Kreisen
- Portieren auf OpenGL von IRIS GL, Kreisen
- OpenGL-Portierung von IRIS GL, Kreisen
- Zeichnungsfunktionen, Kreise
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388734"
---
# <a name="porting-arcs-and-circles"></a><span data-ttu-id="1d82a-114">Portieren von Arcs und Kreisen</span><span class="sxs-lookup"><span data-stu-id="1d82a-114">Porting Arcs and Circles</span></span>

<span data-ttu-id="1d82a-115">Bei OpenGL werden gefüllte Bögen und Kreise mit denselben aufrufen wie nicht gefüllte Bögen und Kreise gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d82a-115">With OpenGL, filled arcs and circles are drawn with the same calls as unfilled arcs and circles.</span></span> <span data-ttu-id="1d82a-116">In der folgenden Tabelle werden die Funktionen "IRIS GL Arc" und "Circle" und ihre entsprechenden OpenGL (GLU)-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="1d82a-116">The following table lists the IRIS GL arc and circle functions and their equivalent OpenGL (GLU) functions.</span></span>



| <span data-ttu-id="1d82a-117">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d82a-117">IRIS GL function</span></span> | <span data-ttu-id="1d82a-118">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="1d82a-118">OpenGL function</span></span>                          | <span data-ttu-id="1d82a-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="1d82a-119">Meaning</span></span>                 |
|------------------|------------------------------------------|-------------------------|
| <span data-ttu-id="1d82a-120">**arcarcf**</span><span class="sxs-lookup"><span data-stu-id="1d82a-120">**arcarcf**</span></span>      | [<span data-ttu-id="1d82a-121">**glupartialdisk**</span><span class="sxs-lookup"><span data-stu-id="1d82a-121">**gluPartialDisk**</span></span>](glupartialdisk.md) | <span data-ttu-id="1d82a-122">Zeichnet einen Bogen.</span><span class="sxs-lookup"><span data-stu-id="1d82a-122">Draws an arc.</span></span>           |
| <span data-ttu-id="1d82a-123">**circcircf**</span><span class="sxs-lookup"><span data-stu-id="1d82a-123">**circcircf**</span></span>    | [<span data-ttu-id="1d82a-124">**gludisk**</span><span class="sxs-lookup"><span data-stu-id="1d82a-124">**gluDisk**</span></span>](gludisk.md)               | <span data-ttu-id="1d82a-125">Zeichnet einen Kreis oder einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="1d82a-125">Draws a circle or disk.</span></span> |



 

<span data-ttu-id="1d82a-126">Sie können einige Dinge mit OpenGL-Bögen und-Kreisen erledigen, die Sie mit Iris GL nicht tun können.</span><span class="sxs-lookup"><span data-stu-id="1d82a-126">You can do some things with OpenGL arcs and circles that you can't do with IRIS GL.</span></span> <span data-ttu-id="1d82a-127">OpenGL ruft Bögen und Kreise, Datenträger und partielle Datenträger auf.</span><span class="sxs-lookup"><span data-stu-id="1d82a-127">OpenGL calls arcs and circles, disks and partial disks respectively.</span></span>

<span data-ttu-id="1d82a-128">Beachten Sie bei der Portierung von Bögen und Kreisen die folgenden Punkte über OpenGL:</span><span class="sxs-lookup"><span data-stu-id="1d82a-128">When porting arcs and circles, keep the following points about OpenGL in mind:</span></span>

-   <span data-ttu-id="1d82a-129">Winkel werden in Grad und nicht in Zehntel Grad gemessen.</span><span class="sxs-lookup"><span data-stu-id="1d82a-129">Angles are measured in degrees, and not in tenths of degrees.</span></span>
-   <span data-ttu-id="1d82a-130">Der Start Winkel wird von der positiven y-Achse und nicht von der x-Achse gemessen.</span><span class="sxs-lookup"><span data-stu-id="1d82a-130">The start angle is measured from the positive y-axis, and not from the x-axis.</span></span>
-   <span data-ttu-id="1d82a-131">Der Mittelpunktswinkel ist nun im Uhrzeigersinn statt gegen den Uhrzeigersinn.</span><span class="sxs-lookup"><span data-stu-id="1d82a-131">The sweep angle is now clockwise instead of counterclockwise.</span></span>

<span data-ttu-id="1d82a-132">??</span><span class="sxs-lookup"><span data-stu-id="1d82a-132">??</span></span>

 

 




