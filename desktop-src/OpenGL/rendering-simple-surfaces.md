---
title: Rendering von einfachen Oberflächen
description: Die glu-Bibliothek enthält eine Reihe von Funktionen zum Zeichnen verschiedener einfacher Oberflächen (Bereiche, Zylinder, Datenträger und Teile von Datenträgern) in einer Vielzahl von Stilen und Ausrichtungen. Diese Funktionen werden im OpenGL-Referenzhandbuch ausführlich beschrieben.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- OpenGL-Hilfsprogramm (GLU), einfache Oberflächen
- GLU (OpenGL-Hilfsprogramm), einfache Oberflächen
- einfache Oberflächen OpenGL
- OpenGL-Hilfsprogramm (GLU), Sphären
- GLU (OpenGL-Hilfsprogramm), Sphären
- Sphären OpenGL
- OpenGL-Hilfsprogramm (GLU), Zylinder
- GLU (OpenGL-Hilfsprogramm), Zylinder
- Zylinder OpenGL
- OpenGL-Hilfsprogramm (GLU), Datenträger
- GLU (OpenGL-Hilfsprogramm), Datenträger
- Datenträger OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388784"
---
# <a name="rendering-simple-surfaces"></a><span data-ttu-id="8510c-116">Rendering von einfachen Oberflächen</span><span class="sxs-lookup"><span data-stu-id="8510c-116">Rendering Simple Surfaces</span></span>

<span data-ttu-id="8510c-117">Die glu-Bibliothek enthält eine Reihe von Funktionen zum Zeichnen verschiedener einfacher Oberflächen (Bereiche, Zylinder, Datenträger und Teile von Datenträgern) in einer Vielzahl von Stilen und Ausrichtungen.</span><span class="sxs-lookup"><span data-stu-id="8510c-117">The GLU library includes a set of functions for drawing various simple surfaces (spheres, cylinders, disks, and parts of disks) in a variety of styles and orientations.</span></span> <span data-ttu-id="8510c-118">Diese Funktionen werden im *OpenGL-Referenzhandbuch* ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8510c-118">These functions are described in detail in the *OpenGL Reference Manual*.</span></span>

<span data-ttu-id="8510c-119">**So erzeugen Sie einfache Oberflächen**</span><span class="sxs-lookup"><span data-stu-id="8510c-119">**To render simple surfaces**</span></span>

1.  <span data-ttu-id="8510c-120">Erstellen Sie ein Quadric-Objekt mit " [**glunewquadric**](glunewquadric.md)".</span><span class="sxs-lookup"><span data-stu-id="8510c-120">Create a quadric object with [**gluNewQuadric**](glunewquadric.md).</span></span>

    <span data-ttu-id="8510c-121">Um dieses Objekt zu zerstören, wenn Sie damit fertig sind, verwenden Sie " [**gludeletequadric**](gludeletequadric.md)".</span><span class="sxs-lookup"><span data-stu-id="8510c-121">To destroy this object when you're finished with it, use [**gluDeleteQuadric**](gludeletequadric.md).</span></span>

2.  <span data-ttu-id="8510c-122">Geben Sie den gewünschten Renderingstil wie unten aufgeführt mit der entsprechenden Funktion an (es sei denn, Sie sind mit den Standardwerten zufrieden):</span><span class="sxs-lookup"><span data-stu-id="8510c-122">Specify the desired rendering style, as listed below, with the appropriate function (unless you're satisfied with the default values):</span></span>
    -   <span data-ttu-id="8510c-123">Gibt an, ob Oberflächen normale generiert werden sollen, und wenn dies der Fall ist, ob eine normale pro Scheitelpunkt oder ein normales pro Gesicht vorhanden sein sollte: [ **gluquadricnormals**](gluquadricnormals.md)</span><span class="sxs-lookup"><span data-stu-id="8510c-123">Whether surface normals should be generated, and if so, whether there should be one normal per vertex or one normal per face: [**gluQuadricNormals**](gluquadricnormals.md)</span></span>
    -   <span data-ttu-id="8510c-124">Gibt an, ob Texturkoordinaten generiert werden sollen: " [ **gluquadrictexture** "](gluquadrictexture.md)</span><span class="sxs-lookup"><span data-stu-id="8510c-124">Whether texture coordinates should be generated: [**gluQuadricTexture**](gluquadrictexture.md)</span></span>
    -   <span data-ttu-id="8510c-125">Welche Seite des quadrands sollte als außen betrachtet werden, und in der-Komponente: " [ **gluquadricorientation** "](gluquadricorientation.md)</span><span class="sxs-lookup"><span data-stu-id="8510c-125">Which side of the quadric should be considered the outside and which the inside: [**gluQuadricOrientation**](gluquadricorientation.md)</span></span>
    -   <span data-ttu-id="8510c-126">Gibt an, ob das Quadric als Satz von Polygonen, Linien oder Punkten gezeichnet werden soll: [ **gluquadricdrawstyle**](gluquadricdrawstyle.md)</span><span class="sxs-lookup"><span data-stu-id="8510c-126">Whether the quadric should be drawn as a set of polygons, lines, or points: [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span></span>
3.  <span data-ttu-id="8510c-127">Nachdem Sie den Renderingstil angegeben haben, rufen Sie die-Renderingfunktion für den gewünschten Typ des Quadric-Objekts auf: " [**glusphere**](glusphere.md)", " [**gluzylinder**](glucylinder.md)", " [**gludisk**](gludisk.md) [**" oder "**](glupartialdisk.md)</span><span class="sxs-lookup"><span data-stu-id="8510c-127">After specifying the rendering style, invoke the rendering function for the desired type of quadric object: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md), or [**gluPartialDisk**](glupartialdisk.md).</span></span>

    <span data-ttu-id="8510c-128">Wenn während des Renderings ein Fehler auftritt, wird die Fehler Behandlungs Funktion aufgerufen, die Sie mit " [*gluvierccallback*](gluquadric.md) " angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="8510c-128">If an error occurs during rendering, the error-handling function you've specified with [*gluQuadricCallBack*](gluquadric.md) is invoked.</span></span>

<span data-ttu-id="8510c-129">Verwenden Sie die Werte *\* RADIUS*, *height* und ähnliche Argumente anstelle der Funktion [**glscale**](glscale.md) , um die viercs zu skalieren, sodass Sie keine normalisierten Einheiten Längen renormalisieren müssen, die generiert werden.</span><span class="sxs-lookup"><span data-stu-id="8510c-129">Use the *\*Radius*, *height*, and similar arguments, rather than the [**glScale**](glscale.md) function, to scale the quadrics, so that you don't have to renormalize any unit-length normals that are generated.</span></span> <span data-ttu-id="8510c-130">Um Beleuchtungsberechnungen mit einer präziserer Granularität zu erzwingen, insbesondere, wenn die Material Spekulation hoch ist, legen Sie die *Schleifen* -und *Stapel* Argumente auf andere Werte als 1 fest.</span><span class="sxs-lookup"><span data-stu-id="8510c-130">To force lighting calculations at a finer granularity, especially if the material specularity is high, set the *loops* and *stacks* arguments to values other than 1.</span></span>

 

 




