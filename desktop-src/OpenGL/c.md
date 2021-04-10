---
title: C (OpenGL)
description: Definitionen von OpenGL-Begriffen, die mit dem Buchstaben C beginnen.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- Client Computer
- Client Arbeitsspeicher
- Clip Koordinaten
- Clipping
- Farbindex
- Farb Index Modus
- Farb Zuordnungen
- components
- Kontexte
- konvexe
- konvexe Hülle
- Koordinatensystem
- cullingfunktionsgruppe
- aktuelle Matrix
- aktuelle Raster Position
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104040000"
---
# <a name="c-opengl"></a><span data-ttu-id="cd0af-118">C (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="cd0af-118">C (OpenGL)</span></span>

<span data-ttu-id="cd0af-119">[a](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="cd0af-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="cd0af-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**Client Computer**</span><span class="sxs-lookup"><span data-stu-id="cd0af-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**client computer**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-121">Der Computer, von dem OpenGL-Befehle ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cd0af-121">The computer from which OpenGL commands are issued.</span></span> <span data-ttu-id="cd0af-122">Der Computer, von dem OpenGL-Befehle ausgestellt werden, kann über ein Netzwerk mit einem anderen Computer verbunden werden, auf dem die Befehle ausgeführt werden, oder es können Befehle ausgestellt und auf dem gleichen Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cd0af-122">The computer that issues OpenGL commands can be connected through a network to a different computer that executes the commands, or commands can be issued and executed on the same computer.</span></span> <span data-ttu-id="cd0af-123">Siehe auch [Server](s.md).</span><span class="sxs-lookup"><span data-stu-id="cd0af-123">See also [server](s.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**Client Arbeitsspeicher**</span><span class="sxs-lookup"><span data-stu-id="cd0af-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**client memory**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-125">Der Hauptspeicher (in dem Programmvariablen gespeichert werden) des Client Computers.</span><span class="sxs-lookup"><span data-stu-id="cd0af-125">The main memory (where program variables are stored) of the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**Clip Koordinaten**</span><span class="sxs-lookup"><span data-stu-id="cd0af-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**clip coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-127">Das Koordinatensystem, das der Transformation durch die Projektions Matrix folgt und der Perspektiven Division vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="cd0af-127">The coordinate system that follows transformation by the projection matrix and precedes perspective division.</span></span> <span data-ttu-id="cd0af-128">Ansichts Volumen Clipping erfolgt in Clip Koordinaten, aber das anwendungsspezifische Clipping ist nicht.</span><span class="sxs-lookup"><span data-stu-id="cd0af-128">View-volume clipping is done in clip coordinates, but application-specific clipping is not.</span></span> <span data-ttu-id="cd0af-129">Siehe auch [anwendungsspezifisches Clipping](a.md).</span><span class="sxs-lookup"><span data-stu-id="cd0af-129">See also [application-specific clipping](a.md).</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**Clipping**</span><span class="sxs-lookup"><span data-stu-id="cd0af-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**clipping**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-131">Entfernen des Teils eines geometrischen primitiven, der sich außerhalb des halb Raums befindet, der durch eine Clippingebene definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cd0af-131">Eliminating the portion of a geometric primitive that is outside the half-space defined by a clipping plane.</span></span> <span data-ttu-id="cd0af-132">Punkte werden einfach abgelehnt, wenn außerhalb von.</span><span class="sxs-lookup"><span data-stu-id="cd0af-132">Points are simply rejected if outside.</span></span> <span data-ttu-id="cd0af-133">Der Teil einer Zeile oder eines Polygons, das sich außerhalb des halb Raums befindet, wird entfernt, und zusätzliche Scheitel Punkte werden nach Bedarf generiert, um die primitive innerhalb des Clipping-halb Raums abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cd0af-133">The portion of a line or of a polygon that is outside the half-space is eliminated, and additional vertices are generated as necessary to complete the primitive within the clipping half-space.</span></span> <span data-ttu-id="cd0af-134">Geometrische Primitive und die aktuelle Raster Position (sofern angegeben) werden immer für die sechs halben Leerzeichen abgeschnitten, die durch die linke, Rechte, untere, obere, nahe und weite Ebene des Ansichts Volumens definiert werden.</span><span class="sxs-lookup"><span data-stu-id="cd0af-134">Geometric primitives and the current raster position (when specified) are always clipped against the six half-spaces defined by the left, right, bottom, top, near, and far planes of the view volume.</span></span> <span data-ttu-id="cd0af-135">Anwendungen können optionale anwendungsspezifische Clippingebenen angeben, die in den Augen Koordinaten angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cd0af-135">Applications can specify optional application-specific clipping planes to be applied in eye coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**Farbindex**</span><span class="sxs-lookup"><span data-stu-id="cd0af-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**color index**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-137">Ein einzelner Wert, der eine Farbe anhand des Namens anstelle des Werts darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd0af-137">A single value that represents a color by name, rather than by value.</span></span> <span data-ttu-id="cd0af-138">OpenGL-Farbindizes werden als kontinuierliche Werte (z. b. Gleit Komma Zahlen) behandelt, während Vorgänge wie Interpolations-und Dithering für Sie ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cd0af-138">OpenGL color indexes are treated as continuous values (for example, floating-point numbers) while operations such as interpolation and dithering are performed on them.</span></span> <span data-ttu-id="cd0af-139">Im Frame Puffer gespeicherte Farbindizes sind jedoch immer ganzzahlige Werte.</span><span class="sxs-lookup"><span data-stu-id="cd0af-139">Color indexes stored in the frame buffer are always integer values, however.</span></span> <span data-ttu-id="cd0af-140">Gleit Komma Indizes werden in ganze Zahlen konvertiert, indem auf den nächstgelegenen ganzzahligen Wert gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="cd0af-140">Floating-point indexes are converted to integers by rounding to the nearest integer value.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**Farb Index Modus**</span><span class="sxs-lookup"><span data-stu-id="cd0af-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**color-index mode**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-142">Der Modus eines OpenGL-Kontexts, in dem die Farb Puffer Farbindizes anstelle von rot-, grün-, blau-und Alpha Farbkomponenten speichern.</span><span class="sxs-lookup"><span data-stu-id="cd0af-142">Mode of an OpenGL context in which its color buffers store color indexes, rather than red, green, blue, and alpha color components.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**Farbzuordnung**</span><span class="sxs-lookup"><span data-stu-id="cd0af-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**color map**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-144">Eine Tabelle mit Index-zu-RGB-Zuordnungen, auf die von der Anzeige Hardware zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="cd0af-144">A table of index-to-RGB mappings that is accessed by the display hardware.</span></span> <span data-ttu-id="cd0af-145">Jeder Farbindex wird aus dem Farb Puffer gelesen, von der Suche in der Farb Map in ein RGB-Triple konvertiert und an den Monitor gesendet.</span><span class="sxs-lookup"><span data-stu-id="cd0af-145">Each color index is read from the color buffer, converted to an RGB triple by lookup in the color map, and sent to the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**Zulieferern**</span><span class="sxs-lookup"><span data-stu-id="cd0af-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-147">Ein einzelner, kontinuierlicher (z. b. Gleit Komma Wert), der eine Intensität oder Menge darstellt.</span><span class="sxs-lookup"><span data-stu-id="cd0af-147">A single, continuous (for example, floating-point) value that represents an intensity or quantity.</span></span> <span data-ttu-id="cd0af-148">Normalerweise stellt ein Komponenten Wert von NULL den minimalen Wert bzw. die minimale Intensität dar, und der Komponenten Wert 1 stellt den maximalen Wert bzw. die maximale Intensität dar, obwohl andere Normalisierungen manchmal verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cd0af-148">Usually, a component value of zero represents the minimum value or intensity, and a component value of one represents the maximum value or intensity, though other normalizations are sometimes used.</span></span> <span data-ttu-id="cd0af-149">Da Komponenten Werte in einem normalisierten Bereich interpretiert werden, werden Sie unabhängig von der eigentlichen Auflösung angegeben.</span><span class="sxs-lookup"><span data-stu-id="cd0af-149">Because component values are interpreted in a normalized range, they are specified independently of actual resolution.</span></span> <span data-ttu-id="cd0af-150">Der RGB-Triple (1, 1, 1) ist z. b. weiß, unabhängig davon, ob die Farb Puffer jeweils 4, 8 oder 12 Bits speichern.</span><span class="sxs-lookup"><span data-stu-id="cd0af-150">For example, the RGB triple (1, 1, 1) is white, regardless of whether the color buffers store 4, 8, or 12 bits each.</span></span> <span data-ttu-id="cd0af-151">Außerhalb des gültigen Bereichs befindlichen Komponenten werden in der Regel an den normalisierten Bereich gebunden, nicht abgeschnitten oder anderweitig interpretiert.</span><span class="sxs-lookup"><span data-stu-id="cd0af-151">Out-of-range components are typically clamped to the normalized range, not truncated or otherwise interpreted.</span></span> <span data-ttu-id="cd0af-152">Beispielsweise wird das RGB-Triple (1,4, 1,5, 0,9) an (1,0, 1,0, 0,9) gebunden, bevor es zum Aktualisieren des Farb Puffers verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cd0af-152">For example, the RGB triple (1.4, 1.5, 0.9) is clamped to (1.0, 1.0, 0.9) before it's used to update the color buffer.</span></span> <span data-ttu-id="cd0af-153">Rot, grün, blau, Alpha und Tiefe werden immer als Komponenten und nie als Indizes behandelt.</span><span class="sxs-lookup"><span data-stu-id="cd0af-153">Red, green, blue, alpha, and depth are always treated as components, never as indexes.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**Kontext**</span><span class="sxs-lookup"><span data-stu-id="cd0af-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-155">Ein kompletter Satz von OpenGL-Zustandsvariablen.</span><span class="sxs-lookup"><span data-stu-id="cd0af-155">A complete set of OpenGL state variables.</span></span> <span data-ttu-id="cd0af-156">Beachten Sie, dass der Frame Puffer-Inhalt nicht Teil des OpenGL-Zustands ist, sondern dass die Konfiguration des Frame Puffer ist.</span><span class="sxs-lookup"><span data-stu-id="cd0af-156">Note that framebuffer contents are not part of the OpenGL state, but that the configuration of the framebuffer is.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**konvexe**</span><span class="sxs-lookup"><span data-stu-id="cd0af-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**convex**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-158">Bedingung eines Polygons, bei dem keine gerade Linie in der Ebene des Polygons mehr als zwei Punkte schneidet.</span><span class="sxs-lookup"><span data-stu-id="cd0af-158">Condition of a polygon in which no straight line in the plane of the polygon intersects the polygon more than twice.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**konforme Hülle**</span><span class="sxs-lookup"><span data-stu-id="cd0af-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convex hull**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-160">Der kleinste konforme Bereich, der eine angegebene Gruppe von Punkten einschließt.</span><span class="sxs-lookup"><span data-stu-id="cd0af-160">The smallest convex region enclosing a specified group of points.</span></span> <span data-ttu-id="cd0af-161">In zwei Dimensionen ist die konforme Hülle konzeptionell durch Streckung eines Gummibandes um die Punkte zu finden, sodass alle Punkte innerhalb des Bands liegen.</span><span class="sxs-lookup"><span data-stu-id="cd0af-161">In two dimensions, the convex hull is found conceptually by stretching a rubber band around the points so that all of the points lie within the band.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**Koordinatensystem**</span><span class="sxs-lookup"><span data-stu-id="cd0af-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**coordinate system**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-163">In einem n-dimensionalen Raum ein Satz von n linear unabhängigen Vektoren, die an einem Punkt (Ursprung genannt) verankert sind.</span><span class="sxs-lookup"><span data-stu-id="cd0af-163">In n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="cd0af-164">Eine Gruppe von Koordinaten gibt einen Punkt im ndimensionalen Spacein-Bereich an, einen Satz von n linear unabhängigen Vektoren, die an einem Punkt (dem Ursprungs Ursprung) verankert sind.</span><span class="sxs-lookup"><span data-stu-id="cd0af-164">A group of coordinates specifies a point in spaceIn n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="cd0af-165">Anhand einer Gruppe von Koordinaten wird ein Punkt im Raum (oder ein Vektor vom Ursprung) festgelegt. Dazu wird die Strecke zum Punkt (oder zur Spitze des Vektors) entlang des jeweiligen Vektors angegeben.</span><span class="sxs-lookup"><span data-stu-id="cd0af-165">A group of coordinates specifies a point in space (or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span> <span data-ttu-id="cd0af-166">(oder ein Vektor vom Ursprung), indem Sie angibt, wie weit die einzelnen Vektoren bewegt werden sollen, um den Punkt (oder die Spitze des Vektors) zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="cd0af-166">(or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**cullingfunktionsgruppe**</span><span class="sxs-lookup"><span data-stu-id="cd0af-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**culling**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-168">Der Prozess, bei dem eine Vorder-oder Rückseite eines Polygons eliminiert wird, sodass das Gesicht nicht gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="cd0af-168">The process of eliminating a front face or back face of a polygon so that the face isn't drawn.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**aktuelle Matrix**</span><span class="sxs-lookup"><span data-stu-id="cd0af-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**current matrix**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-170">Eine Matrix, die Koordinaten in einem Koordinatensystem in Koordinaten eines anderen Systems umwandelt.</span><span class="sxs-lookup"><span data-stu-id="cd0af-170">A matrix that transforms coordinates in one coordinate system to coordinates of another system.</span></span> <span data-ttu-id="cd0af-171">OpenGL enthält drei aktuelle Matrizen: die Modelview-Matrix, die Objekt Koordinaten (vom Programmierer angegebene Koordinaten) in die Augen Koordinaten umwandelt. die Perspektiven Matrix, die Eye-Koordinaten in Clip Koordinaten umwandelt. und die Textur Matrix, die angegebene oder generierte Texturkoordinaten transformiert, wie in der Matrix beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cd0af-171">There are three current matrices in OpenGL: the modelview matrix, which transforms object coordinates (coordinates specified by the programmer) to eye coordinates; the perspective matrix, which transforms eye coordinates to clip coordinates; and the texture matrix, which transforms specified or generated texture coordinates as described by the matrix.</span></span> <span data-ttu-id="cd0af-172">Jede aktuelle Matrix ist das oberste Element in einem Stapel von Matrizen.</span><span class="sxs-lookup"><span data-stu-id="cd0af-172">Each current matrix is the top element on a stack of matrices.</span></span> <span data-ttu-id="cd0af-173">Die drei Stapel können mit OpenGL-matrixbearbeitungs Befehlen manipuliert werden.</span><span class="sxs-lookup"><span data-stu-id="cd0af-173">Each of the three stacks can be manipulated with OpenGL matrix-manipulation commands.</span></span>

</dd> <dt>

<span data-ttu-id="cd0af-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**aktuelle Raster Position**</span><span class="sxs-lookup"><span data-stu-id="cd0af-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**current raster position**</span></span>
</dt> <dd>

<span data-ttu-id="cd0af-175">Eine Fenster Koordinaten Position, die die Platzierung eines bilprimitivs angibt, wenn es rasteriert wird.</span><span class="sxs-lookup"><span data-stu-id="cd0af-175">A window coordinate position that specifies the placement of an image primitive when it's rasterized.</span></span> <span data-ttu-id="cd0af-176">Die aktuelle Raster Position und andere aktuelle Raster Parameter werden aktualisiert, wenn glRasterPos aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="cd0af-176">The current raster position, and other current raster parameters, are updated when glRasterpos is called.</span></span>

</dd> </dl>

 

 




