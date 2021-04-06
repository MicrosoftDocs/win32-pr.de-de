---
title: Portieren von Polygonen und vier eckalen
description: 'Beachten Sie beim Portieren von Polygonen und Vierecken die folgenden Punkte:'
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- IRIS GL portieren, viereckale
- Portieren von IRIS GL, viereckals
- Portieren auf OpenGL von IRIS GL, viereckals
- OpenGL-Portierung von IRIS GL, viereckals
- Zeichnungsfunktionen, viereckale
- viereckale
- IRIS GL portieren, Polygone
- Portieren von IRIS GL, Polygone
- Portieren auf OpenGL von IRIS GL, Polygone
- OpenGL-Portierung von IRIS GL, Polygone
- Zeichnungsfunktionen, Polygone
- Polygone, Portieren von IRIS GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712503"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="c4197-115">Portieren von Polygonen und vier eckalen</span><span class="sxs-lookup"><span data-stu-id="c4197-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="c4197-116">Beachten Sie beim Portieren von Polygonen und Vierecken die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="c4197-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="c4197-117">Es gibt keine direkte Entsprechung für die **Konstante (\*\*\*\*true**).</span><span class="sxs-lookup"><span data-stu-id="c4197-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="c4197-118">Stattdessen können Sie die Mosaik Routinen in der-Datei verwenden, die unter Mosaik [Polygone](tessellating-polygons.md)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="c4197-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="c4197-119">Polygon Modi werden unterschiedlich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c4197-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="c4197-120">Diese Polygon Zeichnungsfunktionen verfügen über keine direkten Entsprechungen in OpenGL: die **polyfamilie** von Routinen. die **POLF** -Familie von Routinen. **pmv**, **PDR** und **PCLOS**; **rpmv** und **rpdr**; **splf**; und **spclos**.</span><span class="sxs-lookup"><span data-stu-id="c4197-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="c4197-121">Wenn Ihr IRIS GL-Code diese Funktionen verwendet, müssen Sie den Code mithilfe von [**glBegin**](glbegin.md)(GL \_ Polygon) neu schreiben.</span><span class="sxs-lookup"><span data-stu-id="c4197-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="c4197-122">In der folgenden Tabelle sind die Funktionen des IRIS GL-Polygons und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c4197-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="c4197-123">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4197-123">IRIS GL function</span></span>         | <span data-ttu-id="c4197-124">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4197-124">OpenGL function</span></span>                                                    | <span data-ttu-id="c4197-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4197-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="c4197-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="c4197-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="c4197-127">[**glBegin**](glbegin.md) (GL \_ Polygon)[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="c4197-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="c4197-128">Vertices definieren die Begrenzung eines einfachen, zusammen gevexen Polygons.</span><span class="sxs-lookup"><span data-stu-id="c4197-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="c4197-129">**glBegin**(GL \_ QUADS)**glEnd**</span><span class="sxs-lookup"><span data-stu-id="c4197-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="c4197-130">Interpretiert Vierbeiner von Vertices als viereckale.</span><span class="sxs-lookup"><span data-stu-id="c4197-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="c4197-131">**bgnqstripdqstrip**</span><span class="sxs-lookup"><span data-stu-id="c4197-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="c4197-132">[**glBegin**](glbegin.md) (GL \_ Quad \_ Strip)</span><span class="sxs-lookup"><span data-stu-id="c4197-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="c4197-133">Interpretiert Scheitel Punkte als verknüpfte Streifen von Vierecken.</span><span class="sxs-lookup"><span data-stu-id="c4197-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="c4197-134">gledgeflag</span><span class="sxs-lookup"><span data-stu-id="c4197-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="c4197-135">**polymode**</span><span class="sxs-lookup"><span data-stu-id="c4197-135">**polymode**</span></span>             | [<span data-ttu-id="c4197-136">**glpolygonmode**</span><span class="sxs-lookup"><span data-stu-id="c4197-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="c4197-137">Legt den Polygon Zeichnungsmodus fest.</span><span class="sxs-lookup"><span data-stu-id="c4197-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="c4197-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="c4197-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="c4197-139">glrect</span><span class="sxs-lookup"><span data-stu-id="c4197-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="c4197-140">Zeichnet ein Rechteck.</span><span class="sxs-lookup"><span data-stu-id="c4197-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="c4197-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="c4197-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="c4197-142">Zeichnet ein Bildschirm gerichtetes Rechteck.</span><span class="sxs-lookup"><span data-stu-id="c4197-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="c4197-143">??</span><span class="sxs-lookup"><span data-stu-id="c4197-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="c4197-144">Portieren von Polygon Modi</span><span class="sxs-lookup"><span data-stu-id="c4197-144">Porting Polygon Modes</span></span>

<span data-ttu-id="c4197-145">Mit der OpenGL-Funktion " [**glpolygonmode**](glpolygonmode.md) " können Sie angeben, für welche Seite eines Polygons der Modus gilt.</span><span class="sxs-lookup"><span data-stu-id="c4197-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="c4197-146">Die Syntax sieht wie folgt aus:</span><span class="sxs-lookup"><span data-stu-id="c4197-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="c4197-147">Dabei ist "Face" eines von:</span><span class="sxs-lookup"><span data-stu-id="c4197-147">where face is one of:</span></span>



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="c4197-148">GL. \_ Front</span><span class="sxs-lookup"><span data-stu-id="c4197-148">GL\_FRONT</span></span>            | <span data-ttu-id="c4197-149">Modus, der sich auf Front-on-Polygone bezieht</span><span class="sxs-lookup"><span data-stu-id="c4197-149">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="c4197-150">GL \_ zurück</span><span class="sxs-lookup"><span data-stu-id="c4197-150">GL\_BACK</span></span>             | <span data-ttu-id="c4197-151">Modus, der auf Polygone mit Rückstand angewendet wird</span><span class="sxs-lookup"><span data-stu-id="c4197-151">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="c4197-152">GL \_ vor \_ und \_ zurück</span><span class="sxs-lookup"><span data-stu-id="c4197-152">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="c4197-153">der Modus, der sowohl für Front-als auch für rückwärts gerichtete Polygone gilt.</span><span class="sxs-lookup"><span data-stu-id="c4197-153">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="c4197-154">Der GL \_ \_ -Front-und- \_ Back-Modus entspricht der Iris GL **polymode** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="c4197-154">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="c4197-155">In der folgenden Tabelle sind die Iris GL-Polygon Modi und ihre entsprechenden OpenGL-Modi aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4197-155">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="c4197-156">IRIS GL-Modus</span><span class="sxs-lookup"><span data-stu-id="c4197-156">IRIS GL mode</span></span> | <span data-ttu-id="c4197-157">OpenGL-Modus</span><span class="sxs-lookup"><span data-stu-id="c4197-157">OpenGL mode</span></span> | <span data-ttu-id="c4197-158">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4197-158">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="c4197-159">Pym- \_ Punkt</span><span class="sxs-lookup"><span data-stu-id="c4197-159">PYM\_POINT</span></span>   | <span data-ttu-id="c4197-160">GL- \_ Punkt</span><span class="sxs-lookup"><span data-stu-id="c4197-160">GL\_POINT</span></span>   | <span data-ttu-id="c4197-161">Zeichnet Vertices als Punkte.</span><span class="sxs-lookup"><span data-stu-id="c4197-161">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="c4197-162">Pym- \_ Linie</span><span class="sxs-lookup"><span data-stu-id="c4197-162">PYM\_LINE</span></span>    | <span data-ttu-id="c4197-163">GL- \_ Zeile</span><span class="sxs-lookup"><span data-stu-id="c4197-163">GL\_LINE</span></span>    | <span data-ttu-id="c4197-164">Zeichnet Begrenzungs Kanten als Liniensegmente.</span><span class="sxs-lookup"><span data-stu-id="c4197-164">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="c4197-165">Pym- \_ Füllung</span><span class="sxs-lookup"><span data-stu-id="c4197-165">PYM\_FILL</span></span>    | <span data-ttu-id="c4197-166">Ausfüllen von GL \_</span><span class="sxs-lookup"><span data-stu-id="c4197-166">GL\_FILL</span></span>    | <span data-ttu-id="c4197-167">Zeichnet Polygon-innere, gefüllt.</span><span class="sxs-lookup"><span data-stu-id="c4197-167">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="c4197-168">Pym- \_ hohl</span><span class="sxs-lookup"><span data-stu-id="c4197-168">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="c4197-169">Füllt nur innere Pixel an den Grenzen.</span><span class="sxs-lookup"><span data-stu-id="c4197-169">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="c4197-170">Portieren von Polygon-Stipeln</span><span class="sxs-lookup"><span data-stu-id="c4197-170">Porting Polygon Stipples</span></span>

<span data-ttu-id="c4197-171">Beachten Sie beim Portieren von IRIS GL-Polygon-Stipeln die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="c4197-171">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="c4197-172">OpenGL verwendet keine Tabellen für Polygon-Stippel. Es wird nur ein stippingmuster beibehalten.</span><span class="sxs-lookup"><span data-stu-id="c4197-172">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="c4197-173">Mit Anzeigelisten können Sie unterschiedliche stippmuster speichern.</span><span class="sxs-lookup"><span data-stu-id="c4197-173">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="c4197-174">Die Größe des OpenGL-Polygon-stippingbitmusters ist immer ein 32-Bit-32-Bit-Bit</span><span class="sxs-lookup"><span data-stu-id="c4197-174">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="c4197-175">Die Stippel Codierung ist von [**glpixelstore**](glpixelstore-functions.md)betroffen.</span><span class="sxs-lookup"><span data-stu-id="c4197-175">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="c4197-176">Weitere Informationen zum Portieren von Polygon-Stipeln finden Sie unter [Portieren von Pixel Vorgängen](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="c4197-176">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="c4197-177">In der folgenden Tabelle sind die Funktionen von IRIS GL Polygon Stippel und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c4197-177">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="c4197-178">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4197-178">IRIS GL function</span></span> | <span data-ttu-id="c4197-179">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4197-179">OpenGL function</span></span>                                    | <span data-ttu-id="c4197-180">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4197-180">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="c4197-181">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="c4197-181">**defpattern**</span></span>   | [<span data-ttu-id="c4197-182">**glpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="c4197-182">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="c4197-183">Legt das Stippel Muster fest.</span><span class="sxs-lookup"><span data-stu-id="c4197-183">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="c4197-184">**SetPattern**</span><span class="sxs-lookup"><span data-stu-id="c4197-184">**setpattern**</span></span>   |                                                    | <span data-ttu-id="c4197-185">OpenGL behält nur ein Polygon-stippingmuster bei.</span><span class="sxs-lookup"><span data-stu-id="c4197-185">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="c4197-186">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="c4197-186">**getpattern**</span></span>   | [<span data-ttu-id="c4197-187">**glgetpolygonstippel**</span><span class="sxs-lookup"><span data-stu-id="c4197-187">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="c4197-188">Gibt die Stippel Bitmap zurück (die zum Zurückgeben eines Indexes verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="c4197-188">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="c4197-189">In OpenGL aktivieren und deaktivieren Sie Polygon-stippling, indem Sie den GL \_ \_ -Polygon-Stippel als Parameter für [**glEnable**](glenable.md) und [**gldeaktiviert**](gldisable.md)übergeben.</span><span class="sxs-lookup"><span data-stu-id="c4197-189">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="c4197-190">Im folgenden OpenGL-Codebeispiel wird das Polygon-stippling veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="c4197-190">The following OpenGL code sample demonstrates polygon stippling:</span></span>


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



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="c4197-191">Portieren von Mosaik Polygonen</span><span class="sxs-lookup"><span data-stu-id="c4197-191">Porting Tessellated Polygons</span></span>

<span data-ttu-id="c4197-192">In IRIS GL verwenden Sie die **Konfigurations**-und **bgnpolygon-Objekte** (**true**) und dann bgnpolygon.</span><span class="sxs-lookup"><span data-stu-id="c4197-192">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="c4197-193">Der OpenGL-glu enthält Funktionen, die Sie zum Zeichnen von zwischen-Polygonen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="c4197-193">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="c4197-194">**So zeichnen Sie ein-und-Polygon-Polygon**</span><span class="sxs-lookup"><span data-stu-id="c4197-194">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="c4197-195">Erstellen Sie ein Mosaik Objekt.</span><span class="sxs-lookup"><span data-stu-id="c4197-195">Create a tessellation object.</span></span>
2.  <span data-ttu-id="c4197-196">Definieren Sie Rückrufe, die zum Verarbeiten der vom Mosaik Prozess generierten Dreiecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4197-196">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="c4197-197">Geben Sie das zu Mosaik Ende Konstante Polygon an.</span><span class="sxs-lookup"><span data-stu-id="c4197-197">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="c4197-198">In der folgenden Tabelle werden die OpenGL-Funktionen zum Zeichnen von Mosaik Polygonen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="c4197-198">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="c4197-199">OpenGL glu-Funktion</span><span class="sxs-lookup"><span data-stu-id="c4197-199">OpenGL GLU function</span></span>                        | <span data-ttu-id="c4197-200">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4197-200">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="c4197-201">**glunewtess**</span><span class="sxs-lookup"><span data-stu-id="c4197-201">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="c4197-202">Erstellt ein neues Mosaik Objekt.</span><span class="sxs-lookup"><span data-stu-id="c4197-202">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="c4197-203">**gludeletetess**</span><span class="sxs-lookup"><span data-stu-id="c4197-203">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="c4197-204">Löscht ein Mosaik Objekt.</span><span class="sxs-lookup"><span data-stu-id="c4197-204">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="c4197-205">*glutesscallback*</span><span class="sxs-lookup"><span data-stu-id="c4197-205">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="c4197-206">**glubeginpolygon**</span><span class="sxs-lookup"><span data-stu-id="c4197-206">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="c4197-207">Beginnt die Polygon Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="c4197-207">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="c4197-208">**glutess Vertex**</span><span class="sxs-lookup"><span data-stu-id="c4197-208">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="c4197-209">Gibt einen Polygon Scheitelpunkt in einer Kontur an.</span><span class="sxs-lookup"><span data-stu-id="c4197-209">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="c4197-210">**glunextcontour**</span><span class="sxs-lookup"><span data-stu-id="c4197-210">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="c4197-211">Gibt an, dass die nächste Reihe von Vertices eine neue Kontur beschreiben.</span><span class="sxs-lookup"><span data-stu-id="c4197-211">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="c4197-212">**gluendpolygon**</span><span class="sxs-lookup"><span data-stu-id="c4197-212">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="c4197-213">Beendet die Polygon Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="c4197-213">Ends the polygon specification.</span></span>                                    |



 

 

 





