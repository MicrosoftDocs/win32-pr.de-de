---
title: Portieren von nursb-Kurven
description: Die OpenGL-Funktionen zum Zeichnen von nursb-Kurven sind den Iris GL-Funktionen sehr ähnlich. Sie geben die-und-Steuerungs Punkte mithilfe einer glunurbscurve-Funktion an, die in einem "glubegincurve/gluendcurve"-paar enthalten sein muss.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- IRIS GL portieren, nursb-Kurven
- Portieren von IRIS GL, nursb-Kurven
- Portieren auf OpenGL von IRIS GL, nursb-Kurven
- OpenGL-Portierung von IRIS GL, nursb-Kurven
- Nursb-Kurven
- Kurven
- IRIS GL portieren, Kurven
- Portieren von IRIS GL, Kurven
- Portieren auf OpenGL von IRIS GL, Kurven
- OpenGL-Portierung von IRIS GL, Kurven
- NURBS (Non-Uniform Rational B-Spline)
- Nicht einheitlicher rationaler B-Spline (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388485"
---
# <a name="porting-nurbs-curves"></a><span data-ttu-id="18da1-116">Portieren von nursb-Kurven</span><span class="sxs-lookup"><span data-stu-id="18da1-116">Porting NURBS Curves</span></span>

<span data-ttu-id="18da1-117">Die OpenGL-Funktionen zum Zeichnen von nursb-Kurven sind den Iris GL-Funktionen sehr ähnlich.</span><span class="sxs-lookup"><span data-stu-id="18da1-117">The OpenGL functions for drawing NURBS curves are very similar to the IRIS GL functions.</span></span> <span data-ttu-id="18da1-118">Sie geben die-und-Steuerungs Punkte mithilfe der Funktion " [**glunurbscurve**](glunurbscurve.md) " an, die in einem " [**glubegincurve**](glubegincurve.md)"-paar "  /  [**gluendcurve**](gluendcurve.md) " enthalten sein muss.</span><span class="sxs-lookup"><span data-stu-id="18da1-118">You specify knot sequences and control points using a [**gluNurbsCurve**](glunurbscurve.md) function, which must be contained within a [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) pair.</span></span>

<span data-ttu-id="18da1-119">In der folgenden Tabelle sind die Iris GL-Funktionen zum Zeichnen von nursb-Kurven und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="18da1-119">The following table lists the IRIS GL functions for drawing NURBS curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="18da1-120">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="18da1-120">IRIS GL function</span></span> | <span data-ttu-id="18da1-121">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="18da1-121">OpenGL function</span></span>                        | <span data-ttu-id="18da1-122">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="18da1-122">Meaning</span></span>                     |
|------------------|----------------------------------------|-----------------------------|
| <span data-ttu-id="18da1-123">**bgncurve**</span><span class="sxs-lookup"><span data-stu-id="18da1-123">**bgncurve**</span></span>     | [<span data-ttu-id="18da1-124">**glubegincurve**</span><span class="sxs-lookup"><span data-stu-id="18da1-124">**gluBeginCurve**</span></span>](glubegincurve.md) | <span data-ttu-id="18da1-125">Beginnt eine Kurven Definition.</span><span class="sxs-lookup"><span data-stu-id="18da1-125">Begins a curve definition.</span></span>  |
| <span data-ttu-id="18da1-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="18da1-126">**nurbscurve**</span></span>   | [<span data-ttu-id="18da1-127">**glunurbscurve**</span><span class="sxs-lookup"><span data-stu-id="18da1-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="18da1-128">Gibt Kurven Attribute an.</span><span class="sxs-lookup"><span data-stu-id="18da1-128">Specifies curve attributes.</span></span> |
| <span data-ttu-id="18da1-129">**endcurve**</span><span class="sxs-lookup"><span data-stu-id="18da1-129">**endcurve**</span></span>     | [<span data-ttu-id="18da1-130">**gluendcurve**</span><span class="sxs-lookup"><span data-stu-id="18da1-130">**gluEndCurve**</span></span>](gluendcurve.md)     | <span data-ttu-id="18da1-131">Beendet eine Kurven Definition.</span><span class="sxs-lookup"><span data-stu-id="18da1-131">Ends a curve definition.</span></span>    |



 

<span data-ttu-id="18da1-132">Ordnen Sie Positionen, Textur und Farbkoordinaten zu, indem Sie diese als separate **glunurbscurve** innerhalb des Begin/End-Paars darstellen.</span><span class="sxs-lookup"><span data-stu-id="18da1-132">Associate position, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** inside the begin/end pair.</span></span> <span data-ttu-id="18da1-133">Sie können für jedes Farb-, Positions-und Textur Datenelement innerhalb eines einzelnen " **glubegincurve/gluendcurve"-** Paars nicht mehr als einen Aufrufen von " **glunurbscurve** " durchführen.</span><span class="sxs-lookup"><span data-stu-id="18da1-133">You can make no more than one call to **gluNurbsCurve** for each piece of color, position, and texture data within a single **gluBeginCurve/gluEndCurve** pair.</span></span> <span data-ttu-id="18da1-134">Sie müssen genau einen-Befehl erstellen, um die Position der Kurve zu beschreiben (a GL \_ zuordnung1 \_ Vertex \_ 3 oder GL \_ zuordnung1 \_ Vertex \_ 4 Description).</span><span class="sxs-lookup"><span data-stu-id="18da1-134">You must make exactly one call to describe the position of the curve (a GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4 description).</span></span> <span data-ttu-id="18da1-135">Wenn Sie " **gluendcurve**" aufgerufen haben, wird die Kurve in Liniensegmente und dann gerendert.</span><span class="sxs-lookup"><span data-stu-id="18da1-135">When you call **gluEndCurve**, the curve is tessellated into line segments and then rendered.</span></span>

<span data-ttu-id="18da1-136">In der folgenden Tabelle sind die Kurven Typen IRIS GL und OpenGL nursb aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="18da1-136">The following table lists IRIS GL and OpenGL NURBS curve types.</span></span>



| <span data-ttu-id="18da1-137">IRIS GL-Typ</span><span class="sxs-lookup"><span data-stu-id="18da1-137">IRIS GL type</span></span> | <span data-ttu-id="18da1-138">OpenGL-Typ</span><span class="sxs-lookup"><span data-stu-id="18da1-138">OpenGL type</span></span>                  | <span data-ttu-id="18da1-139">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="18da1-139">Meaning</span></span>                                 |
|--------------|------------------------------|-----------------------------------------|
| <span data-ttu-id="18da1-140">N \_ v3d</span><span class="sxs-lookup"><span data-stu-id="18da1-140">N\_V3D</span></span>       | <span data-ttu-id="18da1-141">GL \_ zuordnung1 \_ Scheitelpunkt \_ 3</span><span class="sxs-lookup"><span data-stu-id="18da1-141">GL\_MAP1\_VERTEX\_3</span></span>          | <span data-ttu-id="18da1-142">Polynomial-Kurve.</span><span class="sxs-lookup"><span data-stu-id="18da1-142">Polynomial curve.</span></span>                       |
| <span data-ttu-id="18da1-143">N \_ V3DR</span><span class="sxs-lookup"><span data-stu-id="18da1-143">N\_V3DR</span></span>      | <span data-ttu-id="18da1-144">GL \_ zuordnung1 \_ Scheitelpunkt \_ 4</span><span class="sxs-lookup"><span data-stu-id="18da1-144">GL\_MAP1\_VERTEX\_4</span></span>          | <span data-ttu-id="18da1-145">Rationelle Kurve.</span><span class="sxs-lookup"><span data-stu-id="18da1-145">Rational curve.</span></span>                         |
|              | <span data-ttu-id="18da1-146">GL \_ zuordnung1 \_ Textur \_ Koord\_\*</span><span class="sxs-lookup"><span data-stu-id="18da1-146">GL\_MAP1\_TEXTURE\_COORD\_\*</span></span> | <span data-ttu-id="18da1-147">Kontrollpunkte sind Texturkoordinaten.</span><span class="sxs-lookup"><span data-stu-id="18da1-147">Control points are texture coordinates.</span></span> |
|              | <span data-ttu-id="18da1-148">GL \_ zuordnung1 \_ Normal</span><span class="sxs-lookup"><span data-stu-id="18da1-148">GL\_MAP1\_NORMAL</span></span>             | <span data-ttu-id="18da1-149">Kontrollpunkte sind normale.</span><span class="sxs-lookup"><span data-stu-id="18da1-149">Control points are normals.</span></span>             |



 

<span data-ttu-id="18da1-150">Weitere Informationen zu verfügbaren evaluatortypen finden Sie unter [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="18da1-150">For more information on available evaluator types, see [**glMap1**](glmap1.md).</span></span>

<span data-ttu-id="18da1-151">??</span><span class="sxs-lookup"><span data-stu-id="18da1-151">??</span></span>

 

 




