---
title: Mosaik von Polygonen
description: Mosaik von Polygonen
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- OpenGL-Hilfsprogramm (GLU), Mosaik
- GLU (OpenGL-Hilfsprogramm), Mosaik
- OpenGL-Hilfsprogramm (GLU), einfache Polygone
- GLU (OpenGL-Hilfsprogramm), einfache Polygone
- einfache Polygone OpenGL
- OpenGL-Hilfsprogramm (GLU), komplexe Polygone
- GLU (OpenGL-Hilfsprogramm), komplexe Polygone
- komplexe Polygone OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341674"
---
# <a name="tessellating-polygons"></a><span data-ttu-id="d3092-111">Mosaik von Polygonen</span><span class="sxs-lookup"><span data-stu-id="d3092-111">Tessellating Polygons</span></span>

<span data-ttu-id="d3092-112">OpenGL kann direkt nur einfache, konforme Polygone anzeigen.</span><span class="sxs-lookup"><span data-stu-id="d3092-112">OpenGL can directly display only simple convex polygons.</span></span> <span data-ttu-id="d3092-113">Ein Polygon ist einfach, wenn Folgendes gilt:</span><span class="sxs-lookup"><span data-stu-id="d3092-113">A polygon is simple if:</span></span>

-   <span data-ttu-id="d3092-114">Die Ränder schneiden sich nur bei Scheitel Punkten ab.</span><span class="sxs-lookup"><span data-stu-id="d3092-114">The edges intersect only at vertices.</span></span>
-   <span data-ttu-id="d3092-115">Es sind keine doppelten Vertices vorhanden.</span><span class="sxs-lookup"><span data-stu-id="d3092-115">There are no duplicate vertices.</span></span>
-   <span data-ttu-id="d3092-116">An jedem Scheitelpunkt werden genau zwei Ränder angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3092-116">Exactly two edges meet at any vertex.</span></span>

<span data-ttu-id="d3092-117">Um einfache, nicht konvexe Polygone oder einfache Polygone mit Löchern anzuzeigen, müssen Sie zunächst die Polygone auslagern (unterteilen Sie Sie in konvexe Polygone).</span><span class="sxs-lookup"><span data-stu-id="d3092-117">To display simple nonconvex polygons or simple polygons containing holes, you must first triangulate the polygons (subdivide them into convex polygons).</span></span> <span data-ttu-id="d3092-118">Diese Unterteilung *wird als Mosaik* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d3092-118">Such subdivision is called *tessellation*.</span></span> <span data-ttu-id="d3092-119">Glu bietet eine Auflistung von Funktionen, die Mosaik Vorgänge durchführen.</span><span class="sxs-lookup"><span data-stu-id="d3092-119">GLU provides a collection of functions that perform tessellation.</span></span> <span data-ttu-id="d3092-120">Beachten Sie, dass die glu-Mosaik Funktionen nicht einfache Polygone verarbeiten können. Es gibt keine standardmäßige OpenGL-Methode, um solche Polygone zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d3092-120">Note that the GLU tessellation functions can't handle nonsimple polygons; there is no standard OpenGL method to handle such polygons.</span></span>

<span data-ttu-id="d3092-121">Da das Mosaik häufig benötigt wird und ziemlich schwierig sein kann, werden die Funktionen der Funktionen in diesem Abschnitt ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3092-121">Because tessellation is often required and can be rather tricky, this section describes the GLU tessellation functions in detail.</span></span> <span data-ttu-id="d3092-122">Diese Funktionen akzeptieren beliebige einfache Polygone als Eingabe, die möglicherweise Löcher enthalten, und Sie geben eine Kombination von Dreiecken, Dreiecksnetzen und Dreiecks Lüfter zurück.</span><span class="sxs-lookup"><span data-stu-id="d3092-122">These functions take as input arbitrary simple polygons that might include holes, and they return some combination of triangles, triangle meshes, and triangle fans.</span></span> <span data-ttu-id="d3092-123">Wenn Sie keine Netzen oder Lüfter behandeln möchten, können Sie angeben, dass die Mosaik Funktionen nur Dreiecke zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="d3092-123">If you don't want to deal with meshes or fans, you can specify that the tessellation functions return only triangles.</span></span> <span data-ttu-id="d3092-124">Mesh-und Lüfter-Informationen verbessern jedoch die Leistung.</span><span class="sxs-lookup"><span data-stu-id="d3092-124">However, mesh and fan information improves performance.</span></span> <span data-ttu-id="d3092-125">Die Polygon-Mosaik Funktionen unterliegen einem konkaven Polygon mit mindestens einer Kontur.</span><span class="sxs-lookup"><span data-stu-id="d3092-125">The polygon tessellation functions triangulate a concave polygon with one or more contours.</span></span>

<span data-ttu-id="d3092-126">**So verwenden Sie das Polygon-Mosaik**</span><span class="sxs-lookup"><span data-stu-id="d3092-126">**To use polygon tessellation**</span></span>

1.  <span data-ttu-id="d3092-127">Erstellen Sie ein Mosaik Objekt mit [**glunewtess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="d3092-127">Create a tessellation object with [**gluNewTess**](glunewtess.md).</span></span>
2.  <span data-ttu-id="d3092-128">Verwenden Sie " [*glutesscallback*](glutess.md) ", um Rückruf Funktionen zu definieren, die Sie verwenden, um die vom Mosaik Prozess generierten Dreiecke zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="d3092-128">Use [*gluTessCallBack*](glutess.md) to define callback functions you will use to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="d3092-129">Geben Sie mit " [**glubeginpolygon**](glubeginpolygon.md)", " [**glutess Vertex**](glutessvertex.md)", " [**glunextcontour**](glunextcontour.md)" und " [**gluendpolygon**](gluendpolygon.md)" das Polygon mit Löchern oder dem konkaven Polygon an, das im Mosaik Prozess verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3092-129">With [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), specify the polygon with holes or the concave polygon to be tessellated.</span></span>

    <span data-ttu-id="d3092-130">Wenn die Polygon Beschreibung vollständig ist, ruft die Mosaik Funktion die Rückruf Funktionen nach Bedarf auf.</span><span class="sxs-lookup"><span data-stu-id="d3092-130">When the polygon description is complete, the tessellation facility invokes your callback functions as necessary.</span></span>

    <span data-ttu-id="d3092-131">Sie können nicht benötigte Mosaik Objekte mit " [**gludeletetess**](gludeletetess.md)" zerstören.</span><span class="sxs-lookup"><span data-stu-id="d3092-131">You can destroy unneeded tessellation objects with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="d3092-132">Weitere Informationen zum Speichern der Mosaik Daten finden [Sie unter Verwenden von Rückruf Funktionen](using-callback-functions.md).</span><span class="sxs-lookup"><span data-stu-id="d3092-132">For more information on saving the tessellation data, see [Using Callback Functions](using-callback-functions.md).</span></span>

 

 




