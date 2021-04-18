---
title: Die Iris GL Sphere-Bibliothek
description: OpenGL unterstützt die Iris GL Sphere-Bibliothek nicht. Sie können Ihre Sphere-Bibliotheks Aufrufe durch viercs-Routinen aus der glu-Bibliothek ersetzen. Weitere Informationen zur glu-Bibliothek finden Sie im Open GL-Programmier Handbuch und im OpenGL Utility Library.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- IRIS GL Porting, Sphere Library
- Portieren von IRIS GL, Sphere Library
- Portieren auf OpenGL von IRIS GL, Sphere Library
- OpenGL-Portierung von IRIS GL, Sphere Library
- Zeichnungsfunktionen, Sphere-Bibliothek
- Sphere-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310360"
---
# <a name="the-iris-gl-sphere-library"></a><span data-ttu-id="e4d9d-111">Die Iris GL Sphere-Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e4d9d-111">The IRIS GL Sphere Library</span></span>

<span data-ttu-id="e4d9d-112">OpenGL unterstützt die Iris GL Sphere-Bibliothek nicht.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-112">OpenGL does not support the IRIS GL sphere library.</span></span> <span data-ttu-id="e4d9d-113">Sie können Ihre Sphere-Bibliotheks Aufrufe durch viercs-Routinen aus der glu-Bibliothek ersetzen.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-113">You can replace your sphere library calls with quadrics routines from the GLU library.</span></span> <span data-ttu-id="e4d9d-114">Weitere Informationen zur glu-Bibliothek finden Sie im *Open GL-Programmier Handbuch* und im [OpenGL Utility Library](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="e4d9d-114">For more information about the GLU library, see the *Open GL Programming Guide* and [OpenGL Utility Library](opengl-utility-library.md).</span></span>

<span data-ttu-id="e4d9d-115">In der folgenden Tabelle sind die OpenGL viercs-Funktionen aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-115">The following table lists the OpenGL quadrics functions.</span></span>



| <span data-ttu-id="e4d9d-116">OpenGL-Funktion</span><span class="sxs-lookup"><span data-stu-id="e4d9d-116">OpenGL function</span></span>                                        | <span data-ttu-id="e4d9d-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="e4d9d-117">Meaning</span></span>                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="e4d9d-118">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-118">**gluNewQuadric**</span></span>](glunewquadric.md)                 | <span data-ttu-id="e4d9d-119">Erstellt ein neues Quadric-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-119">Creates a new quadric object.</span></span>                                    |
| [<span data-ttu-id="e4d9d-120">**gludeletequadric**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-120">**gluDeleteQuadric**</span></span>](gludeletequadric.md)           | <span data-ttu-id="e4d9d-121">Löscht ein Quadric-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-121">Deletes a quadric object.</span></span>                                        |
| [<span data-ttu-id="e4d9d-122">*gluvierccallback*</span><span class="sxs-lookup"><span data-stu-id="e4d9d-122">*gluQuadricCallback*</span></span>](gluquadric.md)                 | <span data-ttu-id="e4d9d-123">Ordnet einen Rückruf einem quadrischen Objekt zu, um die Fehlerbehandlung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-123">Associates a callback with a quadric object, for error handling.</span></span> |
| [<span data-ttu-id="e4d9d-124">**gluquadricnormals**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-124">**gluQuadricNormals**</span></span>](gluquadricnormals.md)         | <span data-ttu-id="e4d9d-125">Gibt normale an: keine normale, eine pro Gesicht oder eine pro Scheitelpunkt.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-125">Specifies normals: no normals, one per face, or one per vertex.</span></span>  |
| [<span data-ttu-id="e4d9d-126">**gluquadricorientation**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-126">**gluQuadricOrientation**</span></span>](gluquadricorientation.md) | <span data-ttu-id="e4d9d-127">Gibt die Richtung von normalen an: nach außen oder nach innen.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-127">Specifies direction of normals: outward or inward.</span></span>               |
| [<span data-ttu-id="e4d9d-128">**gluquadrictexture**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-128">**gluQuadricTexture**</span></span>](gluquadrictexture.md)         | <span data-ttu-id="e4d9d-129">Wandelt die Generierung der Textur Koordinate ein bzw. aus.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-129">Turns texture-coordinate generation on or off.</span></span>                   |
| [<span data-ttu-id="e4d9d-130">**gluquadricdrawstyle**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-130">**gluQuadricDrawstyle**</span></span>](gluquadricdrawstyle.md)     | <span data-ttu-id="e4d9d-131">Gibt die Zeichnungsart an: Polygone, Linien, Punkte usw.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-131">Specifies drawing style: polygons, lines, points, and so on.</span></span>     |
| [<span data-ttu-id="e4d9d-132">**glusphere**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-132">**gluSphere**</span></span>](glusphere.md)                         | <span data-ttu-id="e4d9d-133">Zeichnet eine Kugel.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-133">Draws a sphere.</span></span>                                                  |
| [<span data-ttu-id="e4d9d-134">**gluzylinder**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-134">**gluCylinder**</span></span>](glucylinder.md)                     | <span data-ttu-id="e4d9d-135">Zeichnet einen Zylinder oder Kegel.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-135">Draws a cylinder or cone.</span></span>                                        |
| [<span data-ttu-id="e4d9d-136">**glupartialdisk**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-136">**gluPartialDisk**</span></span>](glupartialdisk.md)               | <span data-ttu-id="e4d9d-137">Zeichnet einen Bogen.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-137">Draws an arc.</span></span>                                                    |
| [<span data-ttu-id="e4d9d-138">**gludisk**</span><span class="sxs-lookup"><span data-stu-id="e4d9d-138">**gluDisk**</span></span>](gludisk.md)                             | <span data-ttu-id="e4d9d-139">Zeichnet einen Kreis oder einen Datenträger.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-139">Draws a circle or disk.</span></span>                                          |



 

<span data-ttu-id="e4d9d-140">Sie können ein Quadric-Objekt für alle viercs verwenden, die Sie auf ähnliche Weise darstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-140">You can use one quadric object for all quadrics you want to render in similar ways.</span></span> <span data-ttu-id="e4d9d-141">Im folgenden Codebeispiel werden zwei Quadric-Objekte zum Zeichnen von vier vierfachen verwendet, von denen zwei als texturiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e4d9d-141">The following code sample uses two quadric objects to draw four quadrics, two of them textured.</span></span>


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




