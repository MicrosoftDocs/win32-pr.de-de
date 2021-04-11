---
title: Portieren von tiefen Cube-und Nebel Befehlen
description: Portieren von tiefen Cube-und Nebel Befehlen
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- IRIS GL portieren, Tiefe Cueing
- Portieren von IRIS GL, Tiefe Cueing
- Portieren auf OpenGL von IRIS GL, Tiefe Cueing
- OpenGL-Portierung von IRIS GL, Tiefe Cueing
- IRIS GL portieren, Nebel
- Portieren von IRIS GL, Nebel
- Portieren auf OpenGL von IRIS GL, Nebel
- OpenGL-Portierung von IRIS GL, Nebel
- tiefen Cueing
- Nebel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207153"
---
# <a name="porting-depth-cueing-and-fog-commands"></a><span data-ttu-id="774f1-113">Portieren von tiefen Cube-und Nebel Befehlen</span><span class="sxs-lookup"><span data-stu-id="774f1-113">Porting Depth Cueing and Fog Commands</span></span>

<span data-ttu-id="774f1-114">Beachten Sie beim Portieren von tiefen-und Nebel Befehlen die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="774f1-114">When porting depth-cueing and fog commands, keep the following points in mind:</span></span>

-   <span data-ttu-id="774f1-115">Der Iris GL-Befehl, **fogvertex**, legt einen Modus und die Parameter fest, die diesen Modus beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="774f1-115">The IRIS GL call, **fogvertex**, sets a mode and the parameters affecting that mode.</span></span> <span data-ttu-id="774f1-116">In OpenGL wird [**glfog**](glfog.md) einmal aufgerufen, um den Modus festzulegen, und dann zweimal oder mehr, um verschiedene Parameter festzulegen.</span><span class="sxs-lookup"><span data-stu-id="774f1-116">In OpenGL, you call [**glFog**](glfog.md) once to set the mode, and then again twice or more to set various parameters.</span></span>
-   <span data-ttu-id="774f1-117">In OpenGL handelt es sich bei der tiefen Kürzung nicht um ein separates Feature.</span><span class="sxs-lookup"><span data-stu-id="774f1-117">In OpenGL, depth cueing is not a separate feature.</span></span> <span data-ttu-id="774f1-118">Verwenden Sie lineare Nebel anstelle der Tiefe der Tiefe.</span><span class="sxs-lookup"><span data-stu-id="774f1-118">Use linear fog instead of depth cueing.</span></span> <span data-ttu-id="774f1-119">(Dieser Abschnitt enthält ein Beispiel dazu, wie Sie dies tun können.) Die folgenden IRIS GL-Funktionen haben keine direkte OpenGL-Entsprechung:</span><span class="sxs-lookup"><span data-stu-id="774f1-119">(This section gives an example of how to do this.) The following IRIS GL functions have no direct OpenGL equivalent:</span></span>

    <span data-ttu-id="774f1-120">**Depthcue**</span><span class="sxs-lookup"><span data-stu-id="774f1-120">**depthcue**</span></span>

    <span data-ttu-id="774f1-121">**lrgbrange**</span><span class="sxs-lookup"><span data-stu-id="774f1-121">**lRGBrange**</span></span>

    <span data-ttu-id="774f1-122">**lshaderange**</span><span class="sxs-lookup"><span data-stu-id="774f1-122">**lshaderange**</span></span>

    <span data-ttu-id="774f1-123">**getdcm**</span><span class="sxs-lookup"><span data-stu-id="774f1-123">**getdcm**</span></span>

-   <span data-ttu-id="774f1-124">Verwenden Sie zum Anpassen der Nebel Qualität [**glhint**](glhint.md)(GL- \_ Nebel \_ Hinweis).</span><span class="sxs-lookup"><span data-stu-id="774f1-124">To adjust fog quality, use [**glHint**](glhint.md)( GL\_FOG\_HINT ).</span></span>

<span data-ttu-id="774f1-125">In der folgenden Tabelle werden die Iris GL-Funktionen für die Verwaltung von Nebel und ihre entsprechenden OpenGL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="774f1-125">The following table lists the IRIS GL functions for managing fog and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="774f1-126">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="774f1-126">IRIS GL function</span></span>         | <span data-ttu-id="774f1-127">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="774f1-127">OpenGL function</span></span>                                     | <span data-ttu-id="774f1-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="774f1-128">Meaning</span></span>                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="774f1-129">**fogvertex**</span><span class="sxs-lookup"><span data-stu-id="774f1-129">**fogvertex**</span></span>            | [<span data-ttu-id="774f1-130">**glnebel**</span><span class="sxs-lookup"><span data-stu-id="774f1-130">**glFog**</span></span>](glfog.md)                              | <span data-ttu-id="774f1-131">Legt verschiedene Nebel Parameter fest.</span><span class="sxs-lookup"><span data-stu-id="774f1-131">Sets various fog parameters.</span></span>      |
| <span data-ttu-id="774f1-132">**fogvertex**(FG \_ auf)</span><span class="sxs-lookup"><span data-stu-id="774f1-132">**fogvertex**( FG\_ON )</span></span>  | <span data-ttu-id="774f1-133">[**glEnable**](glenable.md) (GL- \_ Nebel)</span><span class="sxs-lookup"><span data-stu-id="774f1-133">[**glEnable**](glenable.md) ( GL\_FOG )</span></span>            | <span data-ttu-id="774f1-134">Schaltet den Nebel ein.</span><span class="sxs-lookup"><span data-stu-id="774f1-134">Turns on fog.</span></span>                     |
| <span data-ttu-id="774f1-135">**fogvertex**(FG \_ Off)</span><span class="sxs-lookup"><span data-stu-id="774f1-135">**fogvertex**( FG\_OFF )</span></span> | <span data-ttu-id="774f1-136">[**gldeaktiviert**](gldisable.md) (GL- \_ Nebel)</span><span class="sxs-lookup"><span data-stu-id="774f1-136">[**glDisable**](gldisable.md) ( GL\_FOG )</span></span>          | <span data-ttu-id="774f1-137">Schaltet den Nebel aus.</span><span class="sxs-lookup"><span data-stu-id="774f1-137">Turns off fog.</span></span>                    |
| <span data-ttu-id="774f1-138">**Depthcue**</span><span class="sxs-lookup"><span data-stu-id="774f1-138">**depthcue**</span></span>             | <span data-ttu-id="774f1-139">[**glnebel**](glfog.md) (GL \_ Nebel \_ mod, GL \_ linear)</span><span class="sxs-lookup"><span data-stu-id="774f1-139">[**glFog**](glfog.md) ( GL\_FOG\_MOD, GL\_LINEAR )</span></span> | <span data-ttu-id="774f1-140">Verwendet linearen Nebel zum Durchsuchen der Tiefe.</span><span class="sxs-lookup"><span data-stu-id="774f1-140">Uses linear fog for depth cueing.</span></span> |



 

<span data-ttu-id="774f1-141">In der folgenden Tabelle sind die Parameter aufgeführt, die Sie an **glnebel** übergeben können.</span><span class="sxs-lookup"><span data-stu-id="774f1-141">The following table lists the parameters you can pass to **glFog**.</span></span>



| <span data-ttu-id="774f1-142">Nebel Parameter</span><span class="sxs-lookup"><span data-stu-id="774f1-142">Fog parameter</span></span>    | <span data-ttu-id="774f1-143">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="774f1-143">Meaning</span></span>                       | <span data-ttu-id="774f1-144">Standard</span><span class="sxs-lookup"><span data-stu-id="774f1-144">Default</span></span>                  |
|------------------|-------------------------------|--------------------------|
| <span data-ttu-id="774f1-145">GL- \_ Nebel \_ Dichte</span><span class="sxs-lookup"><span data-stu-id="774f1-145">GL\_FOG\_DENSITY</span></span> | <span data-ttu-id="774f1-146">Nebeldichte.</span><span class="sxs-lookup"><span data-stu-id="774f1-146">Fog density.</span></span>                  | <span data-ttu-id="774f1-147">1.0</span><span class="sxs-lookup"><span data-stu-id="774f1-147">1.0</span></span>                      |
| <span data-ttu-id="774f1-148">GL. \_ Nebel \_ Anfang</span><span class="sxs-lookup"><span data-stu-id="774f1-148">GL\_FOG\_START</span></span>   | <span data-ttu-id="774f1-149">Fast Distance für linearen Nebel.</span><span class="sxs-lookup"><span data-stu-id="774f1-149">Near distance for linear fog.</span></span> | <span data-ttu-id="774f1-150">0,0</span><span class="sxs-lookup"><span data-stu-id="774f1-150">0.0</span></span>                      |
| <span data-ttu-id="774f1-151">GL- \_ Nebel \_ Ende</span><span class="sxs-lookup"><span data-stu-id="774f1-151">GL\_FOG\_END</span></span>     | <span data-ttu-id="774f1-152">Weit Entfernungs Abstand für linearen Nebel.</span><span class="sxs-lookup"><span data-stu-id="774f1-152">Far distance for linear fog.</span></span>  | <span data-ttu-id="774f1-153">1.0</span><span class="sxs-lookup"><span data-stu-id="774f1-153">1.0</span></span>                      |
| <span data-ttu-id="774f1-154">GL- \_ Nebel \_ Index</span><span class="sxs-lookup"><span data-stu-id="774f1-154">GL\_FOG\_INDEX</span></span>   | <span data-ttu-id="774f1-155">Nebel Farbindex.</span><span class="sxs-lookup"><span data-stu-id="774f1-155">Fog color index.</span></span>              | <span data-ttu-id="774f1-156">0,0</span><span class="sxs-lookup"><span data-stu-id="774f1-156">0.0</span></span>                      |
| <span data-ttu-id="774f1-157">GL- \_ Nebel \_ Farbe</span><span class="sxs-lookup"><span data-stu-id="774f1-157">GL\_FOG\_COLOR</span></span>   | <span data-ttu-id="774f1-158">RGBA-Farbe des NEMS.</span><span class="sxs-lookup"><span data-stu-id="774f1-158">Fog RGBA color.</span></span>               | <span data-ttu-id="774f1-159">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="774f1-159">(0, 0, 0, 0)</span></span>             |
| <span data-ttu-id="774f1-160">GL- \_ Nebel \_ Modus</span><span class="sxs-lookup"><span data-stu-id="774f1-160">GL\_FOG\_MODE</span></span>    | <span data-ttu-id="774f1-161">Nebelmodus.</span><span class="sxs-lookup"><span data-stu-id="774f1-161">Fog mode.</span></span>                     | <span data-ttu-id="774f1-162">Siehe hierzu die folgende Tabelle.</span><span class="sxs-lookup"><span data-stu-id="774f1-162">See the following table.</span></span> |



 

<span data-ttu-id="774f1-163">Der Parameter für die Nebeldichte von OpenGL unterscheidet sich von dem in IRIS GL.</span><span class="sxs-lookup"><span data-stu-id="774f1-163">The fog-density parameter of OpenGL differs from the one in IRIS GL.</span></span> <span data-ttu-id="774f1-164">Sie sind wie folgt verknüpft:</span><span class="sxs-lookup"><span data-stu-id="774f1-164">They are related as follows:</span></span>

-   <span data-ttu-id="774f1-165">If *FogMode* = exp2</span><span class="sxs-lookup"><span data-stu-id="774f1-165">if *fogMode* = EXP2</span></span>
     

    <span data-ttu-id="774f1-166">*openglfogdensity* = (*irisglfogdensity* ) ( **sqrt** ( **Log** (1/255)))</span><span class="sxs-lookup"><span data-stu-id="774f1-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** ( 1 / 255 ) ))</span></span>
-   <span data-ttu-id="774f1-167">If *FogMode* = Exp</span><span class="sxs-lookup"><span data-stu-id="774f1-167">if *fogMode* = EXP</span></span>
     

    <span data-ttu-id="774f1-168">*openglfogdensity* = (*irisglfogdensity* ) ( **Protokoll** (1/255))</span><span class="sxs-lookup"><span data-stu-id="774f1-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** ( 1 / 255 ) )</span></span>

<span data-ttu-id="774f1-169">Wenn **sqrt** der Quadratwurzel Vorgang ist, ist **Log** der natürliche Logarithmus, *irisglfogdensity* ist die Schwert Dichte IRIS GL, und *openglfogdensity* ist die OpenGL-Nebeldichte.</span><span class="sxs-lookup"><span data-stu-id="774f1-169">where **sqrt** is the square root operation, **log** is the natural logarithm, *irisGLfogDensity* is the IRIS GL fog density, and *openGLfogDensity* is the OpenGL fog density.</span></span>

<span data-ttu-id="774f1-170">Verwenden Sie [**glhint**](glhint.md)(GL- \_ Nebel \_ Hinweis, *hintmode*), um zwischen dem Berechnen von Nebel im Pixel-und pro-Vertex-Modus zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="774f1-170">To switch between calculating fog in per-pixel mode and per-vertex mode, use [**glHint**](glhint.md)( GL\_FOG\_HINT, *hintMode*).</span></span> <span data-ttu-id="774f1-171">Zwei Hinweis Modi sind verfügbar:</span><span class="sxs-lookup"><span data-stu-id="774f1-171">Two hint modes are available:</span></span>

-   <span data-ttu-id="774f1-172">GL \_ schönste Berechnung pro Pixel-Nebel</span><span class="sxs-lookup"><span data-stu-id="774f1-172">GL\_NICEST per-pixel fog calculation</span></span>
-   <span data-ttu-id="774f1-173">GL \_ schnellste Berechnung pro Vertex-Nebel</span><span class="sxs-lookup"><span data-stu-id="774f1-173">GL\_FASTEST per-vertex fog calculation</span></span>

<span data-ttu-id="774f1-174">In der folgenden Tabelle sind die Iris GL-Nebel Modi und ihre OpenGL-Entsprechungen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="774f1-174">The following table lists the IRIS GL fog modes and their OpenGL equivalents.</span></span>



| <span data-ttu-id="774f1-175">IRIS GL-Nebel Modus</span><span class="sxs-lookup"><span data-stu-id="774f1-175">IRIS GL fog mode</span></span>                       | <span data-ttu-id="774f1-176">OpenGL-Nebel Modus</span><span class="sxs-lookup"><span data-stu-id="774f1-176">OpenGL fog mode</span></span> | <span data-ttu-id="774f1-177">Hinweis Modus</span><span class="sxs-lookup"><span data-stu-id="774f1-177">Hint mode</span></span>                         | <span data-ttu-id="774f1-178">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="774f1-178">Meaning</span></span>                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| <span data-ttu-id="774f1-179">FG \_ VTX \_ Exp, FG \_ pix \_ Exp</span><span class="sxs-lookup"><span data-stu-id="774f1-179">FG\_VTX\_EXP,FG\_PIX\_EXP</span></span><br/>   | <span data-ttu-id="774f1-180">GL- \_ Exp</span><span class="sxs-lookup"><span data-stu-id="774f1-180">GL\_EXP</span></span>         | <span data-ttu-id="774f1-181">GL \_ schnellste, GL am \_ schönsten</span><span class="sxs-lookup"><span data-stu-id="774f1-181">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="774f1-182">Starker Nebel Modus (Standard).</span><span class="sxs-lookup"><span data-stu-id="774f1-182">Heavy fog mode (default).</span></span>                |
| <span data-ttu-id="774f1-183">FG \_ VTX \_ exp2, FG \_ pix \_ exp2</span><span class="sxs-lookup"><span data-stu-id="774f1-183">FG\_VTX\_EXP2,FG\_PIX\_EXP2</span></span><br/> | <span data-ttu-id="774f1-184">GL \_ exp2</span><span class="sxs-lookup"><span data-stu-id="774f1-184">GL\_EXP2</span></span>        | <span data-ttu-id="774f1-185">GL \_ schnellste, GL am \_ schönsten</span><span class="sxs-lookup"><span data-stu-id="774f1-185">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="774f1-186">Dunst Modus.</span><span class="sxs-lookup"><span data-stu-id="774f1-186">Haze mode.</span></span>                               |
| <span data-ttu-id="774f1-187">FG \_ VTX \_ Lin, FG \_ pix \_ Lin</span><span class="sxs-lookup"><span data-stu-id="774f1-187">FG\_VTX\_LIN,FG\_PIX\_LIN</span></span><br/>   | <span data-ttu-id="774f1-188">GL \_ linear</span><span class="sxs-lookup"><span data-stu-id="774f1-188">GL\_LINEAR</span></span>      | <span data-ttu-id="774f1-189">GL \_ schnellste, GL am \_ schönsten</span><span class="sxs-lookup"><span data-stu-id="774f1-189">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="774f1-190">Linearer Nebel Modus.</span><span class="sxs-lookup"><span data-stu-id="774f1-190">Linear fog mode.</span></span> <span data-ttu-id="774f1-191">(Für die tiefen Cube.)</span><span class="sxs-lookup"><span data-stu-id="774f1-191">(Use for depth cueing.)</span></span> |



 

<span data-ttu-id="774f1-192">Im folgenden Codebeispiel wird die Tiefe in OpenGL veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="774f1-192">The following code example demonstrates depth cueing in OpenGL:</span></span>


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





