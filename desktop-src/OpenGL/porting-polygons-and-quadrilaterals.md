---
title: Portieren von Polygonen und Quadrieren
description: Beachten Sie beim Portieren von Polygonen und Quadrierten die folgenden Punkte.
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- IRIS GL-Portierung, Quadrierung
- Portieren von IRIS GL,quadralrals
- Portieren von IRIS GL,quadrataterals zu OpenGL
- OpenGL-Portierung von IRIS GL,quadrataterals
- Zeichnungsfunktionen,quadralrals
- quadrals
- IRIS GL-Portierung, Polygone
- Portieren von IRIS GL,Polygonen
- Portieren von IRIS GL,Polygonen zu OpenGL
- OpenGL-Portierung von IRIS GL,Polygonen
- Zeichnungsfunktionen,Polygone
- Polygone,Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7900b44051cab9590be11198c8b01af0b7c10244
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908458"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="d42f8-115">Portieren von Polygonen und Quadrieren</span><span class="sxs-lookup"><span data-stu-id="d42f8-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="d42f8-116">Beachten Sie beim Portieren von Polygonen und Quadrieren die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="d42f8-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="d42f8-117">Es gibt kein direktes Äquivalent für **Konkave**(**TRUE**).</span><span class="sxs-lookup"><span data-stu-id="d42f8-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="d42f8-118">Stattdessen können Sie die Mosaikroutinen in der GLU verwenden, die unter [Mosaikpolygone beschrieben sind.](tessellating-polygons.md)</span><span class="sxs-lookup"><span data-stu-id="d42f8-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="d42f8-119">Polygonmodi werden unterschiedlich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="d42f8-120">Diese Polygonzeichnungsfunktionen haben keine direkten Entsprechungen in OpenGL: die **Polyfamilie** von Routinen; die **Polf-Familie** von Routinen; **pmv**, **pdr** und **pclos**; **rpmv** und **rpdr**; **splf**; und **spclos**.</span><span class="sxs-lookup"><span data-stu-id="d42f8-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="d42f8-121">Wenn Ihr IRIS GL-Code diese Funktionen verwendet, müssen Sie den Code mit [**glBegin**](glbegin.md)( GL \_ POLYGON ) umschreiben.</span><span class="sxs-lookup"><span data-stu-id="d42f8-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="d42f8-122">In der folgenden Tabelle sind die IRIS GL-Polygonzeichnungsfunktionen und ihre entsprechenden OpenGL-Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="d42f8-123">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="d42f8-123">IRIS GL function</span></span>         | <span data-ttu-id="d42f8-124">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="d42f8-124">OpenGL function</span></span>                                                    | <span data-ttu-id="d42f8-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d42f8-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d42f8-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="d42f8-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="d42f8-127">[**glBegin**](glbegin.md) ( GL \_ POLYGON )[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="d42f8-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="d42f8-128">Scheitelpunkte definieren die Grenze eines einfachen konvexen Polygons.</span><span class="sxs-lookup"><span data-stu-id="d42f8-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="d42f8-129">**glBegin**( GL \_ QUADS )**glEnd**</span><span class="sxs-lookup"><span data-stu-id="d42f8-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="d42f8-130">Interpretiert Quadruples von Scheitelpunkten als Quaderaterale.</span><span class="sxs-lookup"><span data-stu-id="d42f8-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="d42f8-131">**bgnqstripendqstrip**</span><span class="sxs-lookup"><span data-stu-id="d42f8-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="d42f8-132">[**glBegin**](glbegin.md) ( GL \_ QUAD STRIP ) \_ **glEnd**</span><span class="sxs-lookup"><span data-stu-id="d42f8-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="d42f8-133">Interpretiert Scheitelpunkte als verknüpfte Stripes von Quaderateralen.</span><span class="sxs-lookup"><span data-stu-id="d42f8-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="d42f8-134">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="d42f8-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="d42f8-135">**polymode**</span><span class="sxs-lookup"><span data-stu-id="d42f8-135">**polymode**</span></span>             | [<span data-ttu-id="d42f8-136">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="d42f8-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="d42f8-137">Legt den Polygonzeichnungsmodus fest.</span><span class="sxs-lookup"><span data-stu-id="d42f8-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="d42f8-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="d42f8-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="d42f8-139">glRect</span><span class="sxs-lookup"><span data-stu-id="d42f8-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="d42f8-140">Zeichnet ein Rechteck.</span><span class="sxs-lookup"><span data-stu-id="d42f8-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="d42f8-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="d42f8-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="d42f8-142">Zeichnet ein am Bildschirm ausgerichtetes Rechteck.</span><span class="sxs-lookup"><span data-stu-id="d42f8-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="d42f8-143">??</span><span class="sxs-lookup"><span data-stu-id="d42f8-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="d42f8-144">Portieren von Polygonmodi</span><span class="sxs-lookup"><span data-stu-id="d42f8-144">Porting Polygon Modes</span></span>

<span data-ttu-id="d42f8-145">Mit der [**OpenGL-Funktion glPolygonMode**](glpolygonmode.md) können Sie angeben, auf welche Seite eines Polygons (die Rückseite oder die Vorderseite) der Modus angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d42f8-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="d42f8-146">Die Syntax sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="d42f8-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="d42f8-147">dabei ist das Gesicht eines der:</span><span class="sxs-lookup"><span data-stu-id="d42f8-147">where face is one of:</span></span>



|<span data-ttu-id="d42f8-148">GLenum-Wert</span><span class="sxs-lookup"><span data-stu-id="d42f8-148">GLenum value</span></span>                      |  <span data-ttu-id="d42f8-149">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d42f8-149">Meaning</span></span>                                                          |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="d42f8-150">GL \_ FRONT</span><span class="sxs-lookup"><span data-stu-id="d42f8-150">GL\_FRONT</span></span>            | <span data-ttu-id="d42f8-151">-Modus, der für nach vorne gerichtete Polygone gilt</span><span class="sxs-lookup"><span data-stu-id="d42f8-151">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="d42f8-152">GL \_ BACK</span><span class="sxs-lookup"><span data-stu-id="d42f8-152">GL\_BACK</span></span>             | <span data-ttu-id="d42f8-153">-Modus, der für nach hinten gerichtete Polygone gilt</span><span class="sxs-lookup"><span data-stu-id="d42f8-153">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="d42f8-154">GL \_ FRONT \_ AND \_ BACK</span><span class="sxs-lookup"><span data-stu-id="d42f8-154">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="d42f8-155">-Modus, der sowohl für front- als auch für hintere Polygone gilt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-155">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="d42f8-156">Der GL \_ FRONT \_ AND \_ BACK-Modus entspricht der **POLYMODE-Funktion** IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="d42f8-156">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="d42f8-157">In der folgenden Tabelle sind die IRIS GL-Polygonmodi und die entsprechenden OpenGL-Modi aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-157">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="d42f8-158">IRIS GL-Modus</span><span class="sxs-lookup"><span data-stu-id="d42f8-158">IRIS GL mode</span></span> | <span data-ttu-id="d42f8-159">OpenGL-Modus</span><span class="sxs-lookup"><span data-stu-id="d42f8-159">OpenGL mode</span></span> | <span data-ttu-id="d42f8-160">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d42f8-160">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="d42f8-161">\_PYM-PUNKT</span><span class="sxs-lookup"><span data-stu-id="d42f8-161">PYM\_POINT</span></span>   | <span data-ttu-id="d42f8-162">GL \_ POINT</span><span class="sxs-lookup"><span data-stu-id="d42f8-162">GL\_POINT</span></span>   | <span data-ttu-id="d42f8-163">Zeichnet Scheitelpunkte als Punkte.</span><span class="sxs-lookup"><span data-stu-id="d42f8-163">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="d42f8-164">PYM \_ LINE</span><span class="sxs-lookup"><span data-stu-id="d42f8-164">PYM\_LINE</span></span>    | <span data-ttu-id="d42f8-165">GL \_ LINE</span><span class="sxs-lookup"><span data-stu-id="d42f8-165">GL\_LINE</span></span>    | <span data-ttu-id="d42f8-166">Zeichnet Begrenzungsränder als Liniensegmente.</span><span class="sxs-lookup"><span data-stu-id="d42f8-166">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="d42f8-167">PYM \_ FILL</span><span class="sxs-lookup"><span data-stu-id="d42f8-167">PYM\_FILL</span></span>    | <span data-ttu-id="d42f8-168">GL \_ FILL</span><span class="sxs-lookup"><span data-stu-id="d42f8-168">GL\_FILL</span></span>    | <span data-ttu-id="d42f8-169">Zeichnet polygoneinnere Flächen.</span><span class="sxs-lookup"><span data-stu-id="d42f8-169">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="d42f8-170">\_PYM-ENTHMUS</span><span class="sxs-lookup"><span data-stu-id="d42f8-170">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="d42f8-171">Füllt nur innere Pixel an den Grenzen aus.</span><span class="sxs-lookup"><span data-stu-id="d42f8-171">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="d42f8-172">Portieren von Polygonstipples</span><span class="sxs-lookup"><span data-stu-id="d42f8-172">Porting Polygon Stipples</span></span>

<span data-ttu-id="d42f8-173">Beachten Sie beim Portieren von IRIS GL-Polygonstipples die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="d42f8-173">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="d42f8-174">OpenGL verwendet keine Tabellen für Polygonstipples. es wird nur ein Stipplemuster beibehalten.</span><span class="sxs-lookup"><span data-stu-id="d42f8-174">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="d42f8-175">Sie können Anzeigelisten verwenden, um verschiedene Stipplemuster zu speichern.</span><span class="sxs-lookup"><span data-stu-id="d42f8-175">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="d42f8-176">Die Bitmapgröße der OpenGL-Polygonstipple ist immer ein 32 x 32-Bit-Muster.</span><span class="sxs-lookup"><span data-stu-id="d42f8-176">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="d42f8-177">Die Stipplecodierung wird von [**glPixelStore**](glpixelstore-functions.md)beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="d42f8-177">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="d42f8-178">Weitere Informationen zum Portieren von Polygonstipples finden Sie unter [Portieren von Pixelvorgängen.](porting-pixel-operations.md)</span><span class="sxs-lookup"><span data-stu-id="d42f8-178">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="d42f8-179">In der folgenden Tabelle sind IRIS GL-Polygonspitzenfunktionen und die entsprechenden OpenGL-Funktionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-179">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="d42f8-180">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="d42f8-180">IRIS GL function</span></span> | <span data-ttu-id="d42f8-181">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="d42f8-181">OpenGL function</span></span>                                    | <span data-ttu-id="d42f8-182">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d42f8-182">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="d42f8-183">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="d42f8-183">**defpattern**</span></span>   | [<span data-ttu-id="d42f8-184">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="d42f8-184">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="d42f8-185">Legt das Stipplemuster fest.</span><span class="sxs-lookup"><span data-stu-id="d42f8-185">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="d42f8-186">**setpattern**</span><span class="sxs-lookup"><span data-stu-id="d42f8-186">**setpattern**</span></span>   |                                                    | <span data-ttu-id="d42f8-187">OpenGL behält nur ein Polygonstipplemuster bei.</span><span class="sxs-lookup"><span data-stu-id="d42f8-187">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="d42f8-188">**getpattern**</span><span class="sxs-lookup"><span data-stu-id="d42f8-188">**getpattern**</span></span>   | [<span data-ttu-id="d42f8-189">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="d42f8-189">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="d42f8-190">Gibt die Ausschnittbitmap zurück (wird verwendet, um einen Index zurückgibt).</span><span class="sxs-lookup"><span data-stu-id="d42f8-190">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="d42f8-191">In OpenGL aktivieren und deaktivieren Sie polygonische Ausschnitte, indem Sie GL POLYGON STIPPLE als Parameter für \_ \_ [**glEnable**](glenable.md) und [**glDisable übergeben.**](gldisable.md)</span><span class="sxs-lookup"><span data-stu-id="d42f8-191">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="d42f8-192">Im folgenden OpenGL-Codebeispiel wird das Ausschnitten von Polygonen veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="d42f8-192">The following OpenGL code sample demonstrates polygon stippling:</span></span>


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="d42f8-193">Portieren von Mosaikpolygonen</span><span class="sxs-lookup"><span data-stu-id="d42f8-193">Porting Tessellated Polygons</span></span>

<span data-ttu-id="d42f8-194">In IRIS GL verwenden Sie **concave**(**TRUE**) und dann **bgnpolygon,** um konkave Polygone zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d42f8-194">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="d42f8-195">OpenGL GLU enthält Funktionen, mit derenHilfe Sie konkave Polygone zeichnen können.</span><span class="sxs-lookup"><span data-stu-id="d42f8-195">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="d42f8-196">**So zeichnen Sie ein konkaves Polygon mit OpenGL**</span><span class="sxs-lookup"><span data-stu-id="d42f8-196">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="d42f8-197">Erstellen Sie ein Mosaikobjekt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-197">Create a tessellation object.</span></span>
2.  <span data-ttu-id="d42f8-198">Definieren Sie Rückrufe, die verwendet werden, um die vom Mosaik generierten Dreiecke zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d42f8-198">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="d42f8-199">Geben Sie das konkave Polygon an, für das ein Mosaik erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d42f8-199">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="d42f8-200">In der folgenden Tabelle sind die OpenGL-Funktionen zum Zeichnen von Mosaikpolygonen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-200">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="d42f8-201">OpenGL-GLU-Funktion</span><span class="sxs-lookup"><span data-stu-id="d42f8-201">OpenGL GLU function</span></span>                        | <span data-ttu-id="d42f8-202">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d42f8-202">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="d42f8-203">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="d42f8-203">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="d42f8-204">Erstellt ein neues Mosaikobjekt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-204">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="d42f8-205">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="d42f8-205">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="d42f8-206">Löscht ein Mosaikobjekt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-206">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="d42f8-207">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="d42f8-207">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="d42f8-208">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="d42f8-208">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="d42f8-209">Beginnt die Polygonspezifikation.</span><span class="sxs-lookup"><span data-stu-id="d42f8-209">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="d42f8-210">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="d42f8-210">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="d42f8-211">Gibt einen Polygonvertex in einer Kontur an.</span><span class="sxs-lookup"><span data-stu-id="d42f8-211">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="d42f8-212">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="d42f8-212">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="d42f8-213">Gibt an, dass die nächste Reihe von Scheitelpunkten eine neue Kontur beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d42f8-213">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="d42f8-214">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="d42f8-214">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="d42f8-215">Beendet die Polygonspezifikation.</span><span class="sxs-lookup"><span data-stu-id="d42f8-215">Ends the polygon specification.</span></span>                                    |



 

 

 





