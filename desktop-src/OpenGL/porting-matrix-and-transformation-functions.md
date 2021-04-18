---
title: Portieren von Matrix-und Transformations Funktionen
description: IRIS GL und OpenGL behandeln Matrizen und Transformationen auf ähnliche Weise.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- IRIS GL portieren, Matrizen
- Portieren von IRIS GL, Matrizen
- Portieren auf OpenGL von IRIS GL, Matrizen
- OpenGL-Portierung von IRIS GL, Matrizen
- Matrizen
- IRIS GL portieren, Transformationen
- Portieren von IRIS GL, Transformationen
- Portieren auf OpenGL von IRIS GL, Transformationen
- OpenGL-Portierung von IRIS GL, Transformationen
- Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310548"
---
# <a name="porting-matrix-and-transformation-functions"></a><span data-ttu-id="f1c6c-113">Portieren von Matrix-und Transformations Funktionen</span><span class="sxs-lookup"><span data-stu-id="f1c6c-113">Porting Matrix and Transformation Functions</span></span>

<span data-ttu-id="f1c6c-114">IRIS GL und OpenGL behandeln Matrizen und Transformationen auf ähnliche Weise.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-114">IRIS GL and OpenGL handle matrices and transformations in a similar manner.</span></span> <span data-ttu-id="f1c6c-115">Beim Portieren von Code von IRIS GL sind jedoch mehrere Unterschiede zu beachten:</span><span class="sxs-lookup"><span data-stu-id="f1c6c-115">But there are several differences to keep in mind when porting code from IRIS GL:</span></span>

-   <span data-ttu-id="f1c6c-116">In OpenGL befinden Sie sich immer im Double-Matrix-Modus. Es gibt keinen Einzel Matrix Modus.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-116">In OpenGL you are always in double-matrix mode; there is no single-matrix mode.</span></span>
-   <span data-ttu-id="f1c6c-117">Winkel werden in Grad gemessen, anstelle von Zehntel Graden.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-117">Angles are measured in degrees, instead of tenths of degrees.</span></span>
-   <span data-ttu-id="f1c6c-118">Projektions Matrix Aufrufe, wie z. b. [**glfrustum**](glfrustum.md) und [**glortho**](glortho.md), werden jetzt auf der aktuellen Matrix multipliziert, anstatt auf die aktuelle Matrix geladen zu werden.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-118">Projection matrix calls, like [**glFrustum**](glfrustum.md) and [**glOrtho**](glortho.md), now multiply onto the current matrix, instead of being loaded onto the current matrix.</span></span>
-   <span data-ttu-id="f1c6c-119">Die OpenGL-Funktion " [**glrotation**](glrotate.md)" unterscheidet sich sehr von der **Drehung**.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-119">The OpenGL function, [**glRotate**](glrotate.md), is very different from **rotate**.</span></span> <span data-ttu-id="f1c6c-120">Sie können sich um jede beliebige Achse drehen, anstatt Sie auf die x-, y-und z-Achsen zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-120">You can rotate around any arbitrary axis, instead of being confined to the x-, y-, and z- axes.</span></span> <span data-ttu-id="f1c6c-121">Beispielsweise können Sie Folgendes übersetzen:</span><span class="sxs-lookup"><span data-stu-id="f1c6c-121">For example, you can translate:</span></span>

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    <span data-ttu-id="f1c6c-122">in:</span><span class="sxs-lookup"><span data-stu-id="f1c6c-122">to:</span></span>

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    <span data-ttu-id="f1c6c-123">Bei der Übersetzung von " **drehen** " in " **glrotation** " wechseln Sie zu Grad von Zehntel Graden, und ersetzen Sie "z" durch einen Vektor für die z-Achse.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-123">When translating from **rotate** to **glRotate** you switch to degrees from tenths of degrees and replace 'z' with a vector for the z-axis.</span></span>

-   <span data-ttu-id="f1c6c-124">OpenGL hat keine Entsprechung zur **Polar View** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-124">OpenGL has no equivalent to the **polarview** function.</span></span> <span data-ttu-id="f1c6c-125">Sie können es problemlos durch eine Übersetzung und drei Umdrehungen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-125">You can replace it easily with a translation and three rotations.</span></span> <span data-ttu-id="f1c6c-126">Beispielsweise können Sie Folgendes übersetzen:</span><span class="sxs-lookup"><span data-stu-id="f1c6c-126">For example, you can translate:</span></span>

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    <span data-ttu-id="f1c6c-127">in:</span><span class="sxs-lookup"><span data-stu-id="f1c6c-127">to:</span></span>

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

<span data-ttu-id="f1c6c-128">In der folgenden Tabelle werden die OpenGL-Matrix Funktionen und ihre entsprechenden IRIS GL-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-128">The following table lists the OpenGL matrix functions and their equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="f1c6c-129">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="f1c6c-129">IRIS GL function</span></span>              | <span data-ttu-id="f1c6c-130">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="f1c6c-130">OpenGL function</span></span>                                                                        | <span data-ttu-id="f1c6c-131">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f1c6c-131">Meaning</span></span>                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1c6c-132">**MMode**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-132">**mmode**</span></span>                     | [<span data-ttu-id="f1c6c-133">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-133">**glMatrixMode**</span></span>](glmatrixmode.md)                                                   | <span data-ttu-id="f1c6c-134">Legt den aktuellen Matrix Modus fest.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-134">Sets current matrix mode.</span></span>                                                                                                                                                      |
|                               | [<span data-ttu-id="f1c6c-135">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-135">**glLoadIdentity**</span></span>](glloadidentity.md)                                               | <span data-ttu-id="f1c6c-136">Ersetzt die aktuelle Matrix durch die Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-136">Replaces current matrix with the identity matrix.</span></span>                                                                                                                              |
| <span data-ttu-id="f1c6c-137">**loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-137">**loadmatrix**</span></span>                | <span data-ttu-id="f1c6c-138">[**glloadmatrixf**](glloadmatrix.md),[**glloadmatrixd**](glloadmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="f1c6c-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span></span><br/> | <span data-ttu-id="f1c6c-139">Ersetzt die aktuelle Matrix durch die angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-139">Replaces current matrix with the specified matrix.</span></span>                                                                                                                             |
| <span data-ttu-id="f1c6c-140">**multmatrix**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-140">**multmatrix**</span></span>                | <span data-ttu-id="f1c6c-141">[**glmultmatrixf**](glmultmatrix.md),[**glmultmatrixd**](glmultmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="f1c6c-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span></span><br/> | <span data-ttu-id="f1c6c-142">Nach dem Multiplizieren der aktuellen Matrix mit der angegebenen Matrix (Beachten Sie, dass **multmatrix** vorab multipliziert ist).</span><span class="sxs-lookup"><span data-stu-id="f1c6c-142">Post-multiplies current matrix with the specified matrix (note that **multmatrix** pre-multiplied).</span></span>                                                                            |
| <span data-ttu-id="f1c6c-143">**mapw**, **mapw2**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-143">**mapw**, **mapw2**</span></span>           | [<span data-ttu-id="f1c6c-144">**"gluunproject"**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-144">**gluUnProject**</span></span>](gluunproject.md)                                                   | <span data-ttu-id="f1c6c-145">Projiziert Raumkoordinaten in den Objekt Raum (siehe auch [**gluproject**](gluproject.md)).</span><span class="sxs-lookup"><span data-stu-id="f1c6c-145">Projects world-space coordinates to object space (see also [**gluProject**](gluproject.md)).</span></span>                                                                                  |
| <span data-ttu-id="f1c6c-146">**Ortho**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-146">**ortho**</span></span>                     | [<span data-ttu-id="f1c6c-147">**glortho**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-147">**glOrtho**</span></span>](glortho.md)                                                             | <span data-ttu-id="f1c6c-148">Multipliziert die aktuelle Matrix mit einer orthografischen Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-148">Multiplies current matrix by an orthographic projection matrix.</span></span>                                                                                                                |
| <span data-ttu-id="f1c6c-149">**ortho2**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-149">**ortho2**</span></span>                    | [<span data-ttu-id="f1c6c-150">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-150">**gluOrtho2D**</span></span>](gluortho2d.md)                                                       | <span data-ttu-id="f1c6c-151">Definiert eine zweidimensionale orthografische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-151">Defines a two-dimensional orthographic projection matrix.</span></span>                                                                                                                      |
| <span data-ttu-id="f1c6c-152">**Schau**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-152">**perspective**</span></span>               | [<span data-ttu-id="f1c6c-153">**gluperspective**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-153">**gluPerspective**</span></span>](gluperspective.md)                                               | <span data-ttu-id="f1c6c-154">Definiert eine perspektivische Projektions Matrix.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-154">Defines a perspective projection matrix.</span></span>                                                                                                                                       |
| <span data-ttu-id="f1c6c-155">**picksize**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-155">**picksize**</span></span>                  | [<span data-ttu-id="f1c6c-156">**glupickmatrix**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-156">**gluPickMatrix**</span></span>](glupickmatrix.md)                                                 | <span data-ttu-id="f1c6c-157">Definiert einen Auswahlbereich.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-157">Defines a picking region.</span></span>                                                                                                                                                      |
| <span data-ttu-id="f1c6c-158">**popmatrix**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-158">**popmatrix**</span></span>                 | [<span data-ttu-id="f1c6c-159">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-159">**glPopMatrix**</span></span>](glpopmatrix.md)                                                     | <span data-ttu-id="f1c6c-160">Holt den aktuellen Matrix Stapel und ersetzt dabei die aktuelle Matrix durch die darunter liegenden Matrix.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-160">Pops current matrix stack, replacing the current matrix with the one below it.</span></span>                                                                                                 |
| <span data-ttu-id="f1c6c-161">**pushmatrix**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-161">**pushmatrix**</span></span>                | [<span data-ttu-id="f1c6c-162">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-162">**glPushMatrix**</span></span>](glpushmatrix.md)                                                   | <span data-ttu-id="f1c6c-163">Überträgt den aktuellen Matrix Stapel um eins und duplizieren die aktuelle Matrix.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-163">Pushes current matrix stack down by one, duplicating the current matrix.</span></span>                                                                                                       |
| <span data-ttu-id="f1c6c-164">**drehen**,**rot**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-164">**rotate**,**rot**</span></span><br/> | <span data-ttu-id="f1c6c-165">[**glrotgedreht**](glrotate.md),[**glrotatef**](glrotate.md)</span><span class="sxs-lookup"><span data-stu-id="f1c6c-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span></span><br/>                 | <span data-ttu-id="f1c6c-166">Rotiert das aktuelle Koordinatensystem um den angegebenen Winkel um den Vektor vom Ursprung bis zum angegebenen Punkt.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-166">Rotates current coordinate system by the given angle about the vector from the origin through the given point.</span></span> <span data-ttu-id="f1c6c-167">Beachten Sie, dass **Drehung** nur um die x-, y-und z-Achsen gedreht wurde.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-167">Note that **rotate** rotated only about the x-, y-, and z-axes.</span></span> |
| <span data-ttu-id="f1c6c-168">**scale**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-168">**scale**</span></span>                     | <span data-ttu-id="f1c6c-169">[](glscale.md)[**glScalef**](glscale.md)</span><span class="sxs-lookup"><span data-stu-id="f1c6c-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span></span><br/>                     | <span data-ttu-id="f1c6c-170">Multipliziert die aktuelle Matrix mit einer Skalierungs Matrix.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-170">Multiplies current matrix by a scaling matrix.</span></span>                                                                                                                                 |
| <span data-ttu-id="f1c6c-171">**Übersetzen**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-171">**translate**</span></span>                 | <span data-ttu-id="f1c6c-172">[**glTranslatef**](gltranslate.md),[**glTranslatef**](gltranslate.md)</span><span class="sxs-lookup"><span data-stu-id="f1c6c-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span></span><br/>     | <span data-ttu-id="f1c6c-173">Verschiebt den Ursprung des Koordinatensystems auf den angegebenen Punkt, indem die aktuelle Matrix mit einer Übersetzungs Matrix multipliziert wird.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-173">Moves coordinate-system origin to the point specified, by multiplying the current matrix by a translation matrix.</span></span>                                                              |
| <span data-ttu-id="f1c6c-174">**ster**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-174">**window**</span></span>                    | [<span data-ttu-id="f1c6c-175">**glfrustum**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-175">**glFrustum**</span></span>](glfrustum.md)                                                         | <span data-ttu-id="f1c6c-176">Bei angegebenen Koordinaten für das Abschneiden von Ebenen multipliziert die aktuelle Matrix mit einer Perspektiven Matrix.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-176">Given coordinates for clipping planes, multiplies the current matrix by a perspective matrix.</span></span>                                                                                  |



 

<span data-ttu-id="f1c6c-177">OpenGL verfügt über drei Matrix Modi, die mit [**glMatrixMode**](glmatrixmode.md)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-177">OpenGL has three matrix modes, which are set with [**glMatrixMode**](glmatrixmode.md).</span></span> <span data-ttu-id="f1c6c-178">In der folgenden Tabelle werden die Modi aufgelistet, die als Parameter für **glMatrixMode** verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-178">The following table lists the modes available as parameters for **glMatrixMode**.</span></span>



| <span data-ttu-id="f1c6c-179">IRIS GL-Matrix Modus</span><span class="sxs-lookup"><span data-stu-id="f1c6c-179">IRIS GL matrix mode</span></span> | <span data-ttu-id="f1c6c-180">OpenGL-Modus</span><span class="sxs-lookup"><span data-stu-id="f1c6c-180">OpenGL mode</span></span>    | <span data-ttu-id="f1c6c-181">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="f1c6c-181">Meaning</span></span>                                  | <span data-ttu-id="f1c6c-182">Minimale Stapel Tiefe</span><span class="sxs-lookup"><span data-stu-id="f1c6c-182">Min stack depth</span></span> |
|---------------------|----------------|------------------------------------------|-----------------|
| <span data-ttu-id="f1c6c-183">**Mtexture**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-183">**MTEXTURE**</span></span>        | <span data-ttu-id="f1c6c-184">GL- \_ Textur</span><span class="sxs-lookup"><span data-stu-id="f1c6c-184">GL\_TEXTURE</span></span>    | <span data-ttu-id="f1c6c-185">Arbeitet auf dem Textur Matrix Stapel.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-185">Operates on the texture matrix stack.</span></span>    | <span data-ttu-id="f1c6c-186">2</span><span class="sxs-lookup"><span data-stu-id="f1c6c-186">2</span></span>               |
| <span data-ttu-id="f1c6c-187">**MVIEW**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-187">**MVIEWING**</span></span>        | <span data-ttu-id="f1c6c-188">GL \_ Modelview</span><span class="sxs-lookup"><span data-stu-id="f1c6c-188">GL\_MODELVIEW</span></span>  | <span data-ttu-id="f1c6c-189">Wird im Modell Ansicht-Matrix Stapel betrieben.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-189">Operates on the model view matrix stack.</span></span> | <span data-ttu-id="f1c6c-190">32</span><span class="sxs-lookup"><span data-stu-id="f1c6c-190">32</span></span>              |
| <span data-ttu-id="f1c6c-191">**Mprojektion**</span><span class="sxs-lookup"><span data-stu-id="f1c6c-191">**MPROJECTION**</span></span>     | <span data-ttu-id="f1c6c-192">GL- \_ Projektion</span><span class="sxs-lookup"><span data-stu-id="f1c6c-192">GL\_PROJECTION</span></span> | <span data-ttu-id="f1c6c-193">Arbeitet auf dem Projektions Matrix Stapel.</span><span class="sxs-lookup"><span data-stu-id="f1c6c-193">Operates on the projection matrix stack.</span></span> | <span data-ttu-id="f1c6c-194">2</span><span class="sxs-lookup"><span data-stu-id="f1c6c-194">2</span></span>               |



 

 

 





