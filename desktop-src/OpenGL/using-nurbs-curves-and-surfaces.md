---
title: Verwenden von nursb-Kurven und-Oberflächen
description: Non-Uniform rationb-Spline (NURBS)-Funktionen bieten allgemeine und leistungsstarke Beschreibungen von Kurven und Oberflächen in zwei und drei Dimensionen, wobei die Kurven und Oberflächen in OpenGL-Evaluatoren konvertiert werden.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- OpenGL-Hilfsprogramm (GLU), nicht einheitliche Rational B-Spline (NURBS)
- GLU (OpenGL-Hilfsprogramm), nicht einheitliche Rational B-Spline (NURBS)
- Nicht einheitlicher Rational B-Spline (NURBS) OpenGL
- NURBS (Non-Uniform Rational B-Spline) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309640"
---
# <a name="using-nurbs-curves-and-surfaces"></a><span data-ttu-id="97f4e-107">Verwenden von nursb-Kurven und-Oberflächen</span><span class="sxs-lookup"><span data-stu-id="97f4e-107">Using NURBS Curves and Surfaces</span></span>

<span data-ttu-id="97f4e-108">Non-Uniform rationb-Spline (NURBS)-Funktionen bieten allgemeine und leistungsstarke Beschreibungen von Kurven und Oberflächen in zwei und drei Dimensionen, wobei die Kurven und Oberflächen in OpenGL-Evaluatoren konvertiert werden.</span><span class="sxs-lookup"><span data-stu-id="97f4e-108">Non-Uniform Rational B-Spline (NURBS) functions provide general and powerful descriptions of curves and surfaces in two and three dimensions, converting the curves and surfaces to OpenGL evaluators.</span></span> <span data-ttu-id="97f4e-109">Die nursb-Funktionen können Geometrie in vielen Computern unterstützten mechanischen Entwurfs Systemen darstellen.</span><span class="sxs-lookup"><span data-stu-id="97f4e-109">The NURBS functions can represent geometry in many computer-aided mechanical design systems.</span></span> <span data-ttu-id="97f4e-110">Sie können Kurven und Oberflächen in einer Vielzahl von Formaten darstellen, und Sie können automatisch die Adaptive Unterteilung verarbeiten, die die Domäne in kleinere Dreiecke in Regionen mit hoher Krümmung und Near Silhouette-Rändern zerlegt.</span><span class="sxs-lookup"><span data-stu-id="97f4e-110">They can render curves and surfaces in a variety of styles, and they can automatically handle adaptive subdivision that tessellates the domain into smaller triangles in regions of high curvature and near silhouette edges.</span></span> <span data-ttu-id="97f4e-111">Nursb-Funktionen fallen in die folgenden Kategorien.</span><span class="sxs-lookup"><span data-stu-id="97f4e-111">NURBS functions fall into the following categories.</span></span>

<span data-ttu-id="97f4e-112">Verwenden Sie zum Verwalten eines nursb-Objekts Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97f4e-112">To manage a NURBS object, use:</span></span>

-   <span data-ttu-id="97f4e-113">[**glunewnurbsrenderer**](glunewnurbsrenderer.md) (Erstellen eines NURBS-Objekts)</span><span class="sxs-lookup"><span data-stu-id="97f4e-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (create a NURBS object)</span></span>
-   <span data-ttu-id="97f4e-114">[**gludeletenurbsrenderer**](gludeletenurbsrenderer.md) (löscht ein NURBS-Objekt)</span><span class="sxs-lookup"><span data-stu-id="97f4e-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (deletes a NURBS object)</span></span>
-   <span data-ttu-id="97f4e-115">[*glunurbscallback*](glunurbs.md) (stellt eine Fehler Behandlungs Funktion her)</span><span class="sxs-lookup"><span data-stu-id="97f4e-115">[*gluNurbsCallback*](glunurbs.md) (establishes an error-handling function)</span></span>

<span data-ttu-id="97f4e-116">Verwenden Sie zum Angeben der gewünschten Kurven Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97f4e-116">To specify the desired curves, use:</span></span>

-   [<span data-ttu-id="97f4e-117">**glubegincurve**</span><span class="sxs-lookup"><span data-stu-id="97f4e-117">**gluBeginCurve**</span></span>](glubegincurve.md)
-   [<span data-ttu-id="97f4e-118">**glunurbscurve**</span><span class="sxs-lookup"><span data-stu-id="97f4e-118">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="97f4e-119">**gluendcurve**</span><span class="sxs-lookup"><span data-stu-id="97f4e-119">**gluEndCurve**</span></span>](gluendcurve.md)

<span data-ttu-id="97f4e-120">Verwenden Sie zum Angeben der gewünschten Oberflächen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97f4e-120">To specify the desired surfaces, use:</span></span>

-   [<span data-ttu-id="97f4e-121">**glubeginsurface**</span><span class="sxs-lookup"><span data-stu-id="97f4e-121">**gluBeginSurface**</span></span>](glubeginsurface.md)
-   [<span data-ttu-id="97f4e-122">**glunurbssurface**</span><span class="sxs-lookup"><span data-stu-id="97f4e-122">**gluNurbsSurface**</span></span>](glunurbssurface.md)
-   [<span data-ttu-id="97f4e-123">**gluendsurface**</span><span class="sxs-lookup"><span data-stu-id="97f4e-123">**gluEndSurface**</span></span>](gluendsurface.md)

<span data-ttu-id="97f4e-124">Sie können auch einen Kürzungs Bereich angeben, der eine Teilmenge der zu bewertenden nursb-Oberflächen Domäne definiert, damit Sie Oberflächen erstellen können, die über glatte Begrenzungen verfügen oder Löcher enthalten.</span><span class="sxs-lookup"><span data-stu-id="97f4e-124">You can also specify a trimming region, which defines a subset of the NURBS surface domain to be evaluated so you can create surfaces that have smooth boundaries or that contain holes.</span></span>

<span data-ttu-id="97f4e-125">Verwenden Sie zum Angeben der Kürzungs Region Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97f4e-125">To specify the trimming region, use:</span></span>

-   [<span data-ttu-id="97f4e-126">**glubegintrim**</span><span class="sxs-lookup"><span data-stu-id="97f4e-126">**gluBeginTrim**</span></span>](glubegintrim.md)
-   [<span data-ttu-id="97f4e-127">**glupwlcurve**</span><span class="sxs-lookup"><span data-stu-id="97f4e-127">**gluPwlCurve**</span></span>](glupwlcurve.md)
-   [<span data-ttu-id="97f4e-128">**glunurbscurve**</span><span class="sxs-lookup"><span data-stu-id="97f4e-128">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="97f4e-129">**gluendtrim**</span><span class="sxs-lookup"><span data-stu-id="97f4e-129">**gluEndTrim**</span></span>](gluendtrim.md)

<span data-ttu-id="97f4e-130">Wie bei quadrischen Objekten können Sie auch steuern, wie nursb-Kurven und-Oberflächen gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="97f4e-130">As with quadric objects, you can control how NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="97f4e-131">Sie können Folgendes bestimmen:</span><span class="sxs-lookup"><span data-stu-id="97f4e-131">You can determine:</span></span>

-   <span data-ttu-id="97f4e-132">Gibt an, ob eine Kurve oder eine Oberfläche verworfen werden soll, deren Steuerelement Polyhedron außerhalb des aktuellen Viewports liegt.</span><span class="sxs-lookup"><span data-stu-id="97f4e-132">Whether to discard a curve or surface whose control polyhedron lies outside the current viewport.</span></span>
-   <span data-ttu-id="97f4e-133">Die maximale Länge (in Pixel) der Kanten von Polygonen, die zum Rendering von Kurven und Oberflächen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="97f4e-133">The maximum length (in pixels) of edges of polygons used to render curves and surfaces.</span></span>
-   <span data-ttu-id="97f4e-134">Gibt an, ob Sie die Projektions Matrix, die Modelview-Matrix und den Viewport vom OpenGL-Server verwenden oder explizit mit " [**gluloadsamplingmatrices**](gluloadsamplingmatrices.md)" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="97f4e-134">Whether you will take the projection matrix, modelview matrix, and viewport from the OpenGL server or supply them explictly with [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span></span>

<span data-ttu-id="97f4e-135">Verwenden Sie " [**glunurbsproperty**](glunurbsproperty.md) ", um diese Eigenschaften festzulegen, oder verwenden Sie die Standardwerte.</span><span class="sxs-lookup"><span data-stu-id="97f4e-135">Use [**gluNurbsProperty**](glunurbsproperty.md) to set these properties, or use the default values.</span></span> <span data-ttu-id="97f4e-136">Sie können ein nurb-Objekt über den Renderingstil mit " [**glugetnurbsproperty**](glugetnurbsproperty.md)" Abfragen.</span><span class="sxs-lookup"><span data-stu-id="97f4e-136">You can query a NURBS object about its rendering style with [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span></span>

 

 




