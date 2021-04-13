---
title: Portieren von Bereichen
description: 'Beachten Sie bei der Portierung von Bereichen zu OpenGL die folgenden Punkte:'
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- IRIS GL portieren, Bereiche
- Portieren von IRIS GL, Sphären
- Portieren auf OpenGL von IRIS GL, Sphären
- OpenGL-Portierung von IRIS GL, Sphären
- Zeichnungsfunktionen, Bereiche
- Mikro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388480"
---
# <a name="porting-spheres"></a><span data-ttu-id="ef2a0-109">Portieren von Bereichen</span><span class="sxs-lookup"><span data-stu-id="ef2a0-109">Porting Spheres</span></span>

<span data-ttu-id="ef2a0-110">Beachten Sie beim Portieren von Bereichen zu OpenGL die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="ef2a0-110">When porting spheres to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="ef2a0-111">Der Typ der zum Zeichnen der Kugel verwendeten primitiven kann nicht gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-111">You cannot control the type of primitives used to draw the sphere.</span></span> <span data-ttu-id="ef2a0-112">Sie können die zeichengenauigkeit auf eine andere Weise steuern: Verwenden Sie die Slices und Stapel Parameter.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-112">You can control drawing precision in another way: use the slices and stacks parameters.</span></span> <span data-ttu-id="ef2a0-113">Slices sind länglicher. Stapel sind "latitudini".</span><span class="sxs-lookup"><span data-stu-id="ef2a0-113">Slices are longitudinal; stacks are latitudinal.</span></span>
-   <span data-ttu-id="ef2a0-114">Bereiche werden am Ursprung zentriert gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-114">Spheres are drawn centered at the origin.</span></span> <span data-ttu-id="ef2a0-115">Anstatt den Speicherort anzugeben, führen Sie wie bei der Iris GL **sphdraw** -Funktion einen aufzurufenden Befehl an die Funktion "glu [**glusphere**](glusphere.md) " mit einer Übersetzung aus.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-115">Instead of specifying the location, as you do with the IRIS GL **sphdraw** function, precede a call to the GLU [**gluSphere**](glusphere.md) function with a translation.</span></span>
-   <span data-ttu-id="ef2a0-116">Die Sphere-Bibliothek ist für OpenGL noch nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-116">The sphere library is not yet available for OpenGL.</span></span>

<span data-ttu-id="ef2a0-117">In der folgenden Tabelle sind die Iris GL-Funktionen für Zeichnungs Sphären und ihre entsprechenden glu-Funktionen aufgeführt, sofern verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-117">The following table lists the IRIS GL functions for drawing spheres and their equivalent GLU functions where available.</span></span>



| <span data-ttu-id="ef2a0-118">IRIS GL-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef2a0-118">IRIS GL function</span></span> | <span data-ttu-id="ef2a0-119">Glu-Funktion</span><span class="sxs-lookup"><span data-stu-id="ef2a0-119">GLU function</span></span>                                 | <span data-ttu-id="ef2a0-120">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="ef2a0-120">Meaning</span></span>                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="ef2a0-121">**sphobj**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-121">**sphobj**</span></span>       | [<span data-ttu-id="ef2a0-122">**glunewquadric**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-122">**gluNewQuadric**</span></span>](glunewquadric.md)       | <span data-ttu-id="ef2a0-123">Erstellt ein neues Sphere-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-123">Creates a new sphere object.</span></span>                  |
| <span data-ttu-id="ef2a0-124">**sphfree**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-124">**sphfree**</span></span>      | [<span data-ttu-id="ef2a0-125">**gludeletequadric**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-125">**gluDeleteQuadric**</span></span>](gludeletequadric.md) | <span data-ttu-id="ef2a0-126">Löscht das kugelobjekt und den verwendeten freien Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-126">Deletes sphere object and free memory used.</span></span>   |
| <span data-ttu-id="ef2a0-127">**sphdraw**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-127">**sphdraw**</span></span>      | [<span data-ttu-id="ef2a0-128">**glusphere**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-128">**gluSphere**</span></span>](glusphere.md)               | <span data-ttu-id="ef2a0-129">Zeichnet eine Kugel.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-129">Draws a sphere.</span></span>                               |
| <span data-ttu-id="ef2a0-130">**sphmode**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-130">**sphmode**</span></span>      |                                              | <span data-ttu-id="ef2a0-131">Legt Sphere-Attribute fest.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-131">Sets sphere attributes.</span></span>                       |
| <span data-ttu-id="ef2a0-132">**sphrotmatrix**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-132">**sphrotmatrix**</span></span> |                                              | <span data-ttu-id="ef2a0-133">Steuert die Kugel Ausrichtung.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-133">Controls sphere orientation.</span></span>                  |
| <span data-ttu-id="ef2a0-134">**sphgnpolys**</span><span class="sxs-lookup"><span data-stu-id="ef2a0-134">**sphgnpolys**</span></span>   |                                              | <span data-ttu-id="ef2a0-135">Gibt die Anzahl von Polygonen in der aktuellen Kugel zurück.</span><span class="sxs-lookup"><span data-stu-id="ef2a0-135">Returns number of polygons in current sphere.</span></span> |



 

<span data-ttu-id="ef2a0-136">??</span><span class="sxs-lookup"><span data-stu-id="ef2a0-136">??</span></span>

 

 




