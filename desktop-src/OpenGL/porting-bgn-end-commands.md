---
title: Portieren von BGN-/End-Befehlen
description: IRIS GL verwendet das Begin/End-Paradigma, verfügt aber über eine andere Funktion für jede Grafik primitive.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- IRIS GL Porting, BGN/End-Befehle
- Portieren von IRIS GL, BGN/End-Befehlen
- Portieren auf OpenGL von IRIS GL, BGN/End-Befehlen
- OpenGL-Portierung von IRIS GL, BGN/End-Befehlen
- Zeichenfunktionen, BGN/End-Befehle
- BGN-/End-Befehle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388631"
---
# <a name="porting-bgnend-commands"></a><span data-ttu-id="beea0-109">Portieren von BGN-/End-Befehlen</span><span class="sxs-lookup"><span data-stu-id="beea0-109">Porting bgn/end Commands</span></span>

<span data-ttu-id="beea0-110">IRIS GL verwendet das Begin/End-Paradigma, verfügt aber über eine andere Funktion für jede Grafik primitive.</span><span class="sxs-lookup"><span data-stu-id="beea0-110">IRIS GL uses the begin/end paradigm but has a different function for each graphics primitive.</span></span> <span data-ttu-id="beea0-111">Beispielsweise verwenden Sie ggf. **bgnpolygon** und **endpolygon** , um Polygone zu zeichnen, und **bgnline** und **EndLine** zum Zeichnen von Linien.</span><span class="sxs-lookup"><span data-stu-id="beea0-111">For example, you probably use **bgnpolygon** and **endpolygon** to draw polygons, and **bgnline** and **endline** to draw lines.</span></span> <span data-ttu-id="beea0-112">In OpenGL verwenden Sie die [**glBegin**](glbegin.md)-  /  [**glEnd**](glend.md) -Struktur für beide.</span><span class="sxs-lookup"><span data-stu-id="beea0-112">In OpenGL, you use the [**glBegin**](glbegin.md) / [**glEnd**](glend.md) structure for both.</span></span> <span data-ttu-id="beea0-113">In OpenGL zeichnen Sie die meisten geometrischen Objekte durch Einschließen einer Reihe von Funktionen, die Scheitel Punkte, normale, Texturen und Farben zwischen Paaren von **glBegin** -und **glEnd** -aufrufen angeben.</span><span class="sxs-lookup"><span data-stu-id="beea0-113">In OpenGL you draw most geometric objects by enclosing a series of functions that specify vertices, normals, textures, and colors between pairs of **glBegin** and **glEnd** calls.</span></span> <span data-ttu-id="beea0-114">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="beea0-114">For example:</span></span>

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

<span data-ttu-id="beea0-115">Die **glBegin** -Funktion nimmt einen einzelnen Parameter an, der den Zeichnungsmodus und somit den primitiven angibt.</span><span class="sxs-lookup"><span data-stu-id="beea0-115">The **glBegin** function takes a single parameter that specifies the drawing mode, and thus the primitive.</span></span> <span data-ttu-id="beea0-116">Hier sehen Sie ein OpenGL-Codebeispiel, das ein Polygon und eine Zeile zeichnet:</span><span class="sxs-lookup"><span data-stu-id="beea0-116">Here's an OpenGL code sample that draws a polygon and then a line:</span></span>

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

<span data-ttu-id="beea0-117">Mit OpenGL zeichnen Sie verschiedene geometrische Objekte, indem Sie verschiedene Parameter für [**glBegin**](glbegin.md)angeben.</span><span class="sxs-lookup"><span data-stu-id="beea0-117">With OpenGL, you draw different geometric objects by specifying different parameters for [**glBegin**](glbegin.md).</span></span> <span data-ttu-id="beea0-118">In der folgenden Tabelle sind die OpenGL- **glBegin** -Parameter aufgeführt, die äquivalenten IRIS GL-Funktionen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="beea0-118">The following table lists the OpenGL **glBegin** parameters that correspond to equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="beea0-119">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="beea0-119">IRIS GL function</span></span>  | <span data-ttu-id="beea0-120">Wert des glBegin-Modus</span><span class="sxs-lookup"><span data-stu-id="beea0-120">Value of glBegin mode</span></span> | <span data-ttu-id="beea0-121">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="beea0-121">Meaning</span></span>                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="beea0-122">**bgnpoint**</span><span class="sxs-lookup"><span data-stu-id="beea0-122">**bgnpoint**</span></span>      | <span data-ttu-id="beea0-123">GL- \_ Punkte</span><span class="sxs-lookup"><span data-stu-id="beea0-123">GL\_POINTS</span></span>            | <span data-ttu-id="beea0-124">Einzelne Punkte.</span><span class="sxs-lookup"><span data-stu-id="beea0-124">Individual points.</span></span>                                                                       |
| <span data-ttu-id="beea0-125">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="beea0-125">**bgnline**</span></span>       | <span data-ttu-id="beea0-126">GL- \_ Zeilen \_ Streifen</span><span class="sxs-lookup"><span data-stu-id="beea0-126">GL\_LINE\_STRIP</span></span>       | <span data-ttu-id="beea0-127">Reihe verbundener Liniensegmente.</span><span class="sxs-lookup"><span data-stu-id="beea0-127">Series of connected line segments.</span></span>                                                       |
| <span data-ttu-id="beea0-128">**bgnclosedline**</span><span class="sxs-lookup"><span data-stu-id="beea0-128">**bgnclosedline**</span></span> | <span data-ttu-id="beea0-129">GL- \_ Zeilen \_ Schleife</span><span class="sxs-lookup"><span data-stu-id="beea0-129">GL\_LINE\_LOOP</span></span>        | <span data-ttu-id="beea0-130">Eine Reihe verbundener Liniensegmente, wobei ein Segment zwischen der ersten und letzten Vertices hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="beea0-130">Series of connected line segments, with a segment added between first and last vertices.</span></span> |
|                   | <span data-ttu-id="beea0-131">GL- \_ Zeilen</span><span class="sxs-lookup"><span data-stu-id="beea0-131">GL\_LINES</span></span>             | <span data-ttu-id="beea0-132">Paare von Vertices, die als einzelne Liniensegmente interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="beea0-132">Pairs of vertices interpreted as individual line segments.</span></span>                               |
| <span data-ttu-id="beea0-133">**bgnpolygon**</span><span class="sxs-lookup"><span data-stu-id="beea0-133">**bgnpolygon**</span></span>    | <span data-ttu-id="beea0-134">GL- \_ Polygon</span><span class="sxs-lookup"><span data-stu-id="beea0-134">GL\_POLYGON</span></span>           | <span data-ttu-id="beea0-135">Grenze eines einfachen, zusammen gevexen Polygons.</span><span class="sxs-lookup"><span data-stu-id="beea0-135">Boundary of a simple convex polygon.</span></span>                                                     |
|                   | <span data-ttu-id="beea0-136">GL- \_ Dreiecke</span><span class="sxs-lookup"><span data-stu-id="beea0-136">GL\_TRIANGLES</span></span>         | <span data-ttu-id="beea0-137">Die als Dreiecke interpretierten Scheitel Punkte.</span><span class="sxs-lookup"><span data-stu-id="beea0-137">Triples of vertices interpreted as triangles.</span></span>                                            |
| <span data-ttu-id="beea0-138">**bgntmesh**</span><span class="sxs-lookup"><span data-stu-id="beea0-138">**bgntmesh**</span></span>      | <span data-ttu-id="beea0-139">GL- \_ Dreiecks \_ Streifen</span><span class="sxs-lookup"><span data-stu-id="beea0-139">GL\_TRIANGLE\_STRIP</span></span>   | <span data-ttu-id="beea0-140">Verknüpfte Streifen von Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="beea0-140">Linked strips of triangles.</span></span>                                                              |
|                   | <span data-ttu-id="beea0-141">GL- \_ Dreiecks \_ Lüfter</span><span class="sxs-lookup"><span data-stu-id="beea0-141">GL\_TRIANGLE\_FAN</span></span>     | <span data-ttu-id="beea0-142">Verknüpfte Fans von Dreiecken.</span><span class="sxs-lookup"><span data-stu-id="beea0-142">Linked fans of triangles.</span></span>                                                                |
|                   | <span data-ttu-id="beea0-143">GL \_ .</span><span class="sxs-lookup"><span data-stu-id="beea0-143">GL\_QUADS</span></span>             | <span data-ttu-id="beea0-144">Vierbeiner von Vertices, die als viereckale interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="beea0-144">Quadruples of vertices interpreted as quadrilaterals.</span></span>                                    |
| <span data-ttu-id="beea0-145">**bgnqstrip**</span><span class="sxs-lookup"><span data-stu-id="beea0-145">**bgnqstrip**</span></span>     | <span data-ttu-id="beea0-146">GL \_ Quad \_ Strip</span><span class="sxs-lookup"><span data-stu-id="beea0-146">GL\_QUAD\_STRIP</span></span>       | <span data-ttu-id="beea0-147">Verknüpfte Streifen von viereckalen.</span><span class="sxs-lookup"><span data-stu-id="beea0-147">Linked strips of quadrilaterals.</span></span>                                                         |



 

<span data-ttu-id="beea0-148">Eine ausführliche Erläuterung der Unterschiede zwischen Dreiecksnetzen, Streifen und Lüfter finden Sie unter [Portieren von Dreiecken](porting-triangles.md).</span><span class="sxs-lookup"><span data-stu-id="beea0-148">For a detailed discussion of the differences between triangle meshes, strips, and fans, see [Porting Triangles](porting-triangles.md).</span></span>

<span data-ttu-id="beea0-149">Es gibt keine Beschränkung für die Anzahl der Scheitel Punkte, die zwischen einem [**glBegin**](glbegin.md)-  /  [**glEnd**](glend.md) -Paar angegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="beea0-149">There is no limit to the number of vertices you can specify between a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair.</span></span>

<span data-ttu-id="beea0-150">Zusätzlich zum Angeben von Vertices in einem **glBegin**-  /  **glEnd** -paar können Sie eine aktuelle normale, aktuelle Textur Koordinate und eine aktuelle Farbe angeben.</span><span class="sxs-lookup"><span data-stu-id="beea0-150">In addition to specifying vertices inside a **glBegin** / **glEnd** pair, you can specify a current normal, current texture coordinates, and a current color.</span></span> <span data-ttu-id="beea0-151">In der folgenden Tabelle sind die in einem **glBegin**-  /  **glEnd** -paar gültigen Befehle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="beea0-151">The following table lists the commands valid inside a **glBegin** / **glEnd** pair.</span></span>



| <span data-ttu-id="beea0-152">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="beea0-152">IRIS GL function</span></span>        | <span data-ttu-id="beea0-153">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="beea0-153">OpenGL function</span></span>                                                      | <span data-ttu-id="beea0-154">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="beea0-154">Meaning</span></span>                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="beea0-155">**v2**, **V3**, **V4**</span><span class="sxs-lookup"><span data-stu-id="beea0-155">**v2**, **v3**, **v4**</span></span>  | [<span data-ttu-id="beea0-156">glVertex</span><span class="sxs-lookup"><span data-stu-id="beea0-156">glVertex</span></span>](glvertex-functions.md)                                   | <span data-ttu-id="beea0-157">Legt Scheitelpunkt Koordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="beea0-157">Sets vertex coordinates.</span></span>                         |
| <span data-ttu-id="beea0-158">**RGBColor**, **CPack**</span><span class="sxs-lookup"><span data-stu-id="beea0-158">**RGBcolor**, **cpack**</span></span> | [<span data-ttu-id="beea0-159">glcolor</span><span class="sxs-lookup"><span data-stu-id="beea0-159">glColor</span></span>](glcolor-functions.md)                                     | <span data-ttu-id="beea0-160">Legt die aktuelle Farbe fest.</span><span class="sxs-lookup"><span data-stu-id="beea0-160">Sets current color.</span></span>                              |
| <span data-ttu-id="beea0-161">**color**</span><span class="sxs-lookup"><span data-stu-id="beea0-161">**color**</span></span>               | [<span data-ttu-id="beea0-162">glindex</span><span class="sxs-lookup"><span data-stu-id="beea0-162">glIndex</span></span>](glindex-functions.md)                                     | <span data-ttu-id="beea0-163">Legt den aktuellen Farbindex fest.</span><span class="sxs-lookup"><span data-stu-id="beea0-163">Sets current color index.</span></span>                        |
| <span data-ttu-id="beea0-164">**n3f**</span><span class="sxs-lookup"><span data-stu-id="beea0-164">**n3f**</span></span>                 | [<span data-ttu-id="beea0-165">glnormal</span><span class="sxs-lookup"><span data-stu-id="beea0-165">glNormal</span></span>](glnormal-functions.md)                                   | <span data-ttu-id="beea0-166">Legt normale Vektor Koordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="beea0-166">Sets normal vector coordinates.</span></span>                  |
|                         | [<span data-ttu-id="beea0-167">glevalcoord</span><span class="sxs-lookup"><span data-stu-id="beea0-167">glEvalCoord</span></span>](glevalcoord-functions.md)                             | <span data-ttu-id="beea0-168">Wertet aktivierte ein-und zweidimensionale Zuordnungen aus.</span><span class="sxs-lookup"><span data-stu-id="beea0-168">Evaluates enabled one- and two-dimensional maps.</span></span> |
| <span data-ttu-id="beea0-169">**czuweisung**</span><span class="sxs-lookup"><span data-stu-id="beea0-169">**callobj**</span></span>             | <span data-ttu-id="beea0-170">[**glCallList**](glcalllist.md), [ **glcalllists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="beea0-170">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="beea0-171">Führt Anzeigelisten aus.</span><span class="sxs-lookup"><span data-stu-id="beea0-171">Executes display list(s).</span></span>                        |
| <span data-ttu-id="beea0-172">**T2**</span><span class="sxs-lookup"><span data-stu-id="beea0-172">**t2**</span></span>                  | [<span data-ttu-id="beea0-173">gltexcoord</span><span class="sxs-lookup"><span data-stu-id="beea0-173">glTexCoord</span></span>](gltexcoord-functions.md)                               | <span data-ttu-id="beea0-174">Legt Texturkoordinaten fest.</span><span class="sxs-lookup"><span data-stu-id="beea0-174">Sets texture coordinates.</span></span>                        |
|                         | [<span data-ttu-id="beea0-175">gledgeflag</span><span class="sxs-lookup"><span data-stu-id="beea0-175">glEdgeFlag</span></span>](gledgeflag-functions.md)                               | <span data-ttu-id="beea0-176">Steuert Zeichnungs Kanten.</span><span class="sxs-lookup"><span data-stu-id="beea0-176">Controls drawing edges.</span></span>                          |
| <span data-ttu-id="beea0-177">**lmbind**</span><span class="sxs-lookup"><span data-stu-id="beea0-177">**lmbind**</span></span>              | [<span data-ttu-id="beea0-178">glmaterial</span><span class="sxs-lookup"><span data-stu-id="beea0-178">glMaterial</span></span>](glmaterial-functions.md)                               | <span data-ttu-id="beea0-179">Legt Materialeigenschaften fest.</span><span class="sxs-lookup"><span data-stu-id="beea0-179">Sets material properties.</span></span>                        |



 

> [!Note]
>
> <span data-ttu-id="beea0-180">Wenn Sie eine andere als die in der obigen Tabelle aufgeführten OpenGL-Funktionen in einem [**glBegin**](glbegin.md)-  /  [**glEnd**](glend.md) -paar verwenden, erhalten Sie unvorhersehbare Ergebnisse oder möglicherweise einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="beea0-180">If you use any OpenGL function other than those listed in the preceding table inside a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair, you'll get unpredictable results, or possibly an error.</span></span>

 

 

 




