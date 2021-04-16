---
title: Übersicht über Pfadgeometrien
description: Beschreibt die Verwendung von Pfadgeometrien zum Definieren komplexer Formen.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104551813"
---
# <a name="path-geometries-overview"></a><span data-ttu-id="85767-103">Übersicht über Pfadgeometrien</span><span class="sxs-lookup"><span data-stu-id="85767-103">Path Geometries Overview</span></span>

<span data-ttu-id="85767-104">In diesem Thema wird beschrieben, wie Sie Direct2D Path Geometrien zum Erstellen komplexer Zeichnungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="85767-104">This topic describes how to use Direct2D path geometries to create complex drawings.</span></span> <span data-ttu-id="85767-105">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="85767-105">It contains the following sections.</span></span>

-   [<span data-ttu-id="85767-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="85767-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="85767-107">Pfadgeometrien in Direct2D</span><span class="sxs-lookup"><span data-stu-id="85767-107">Path Geometries in Direct2D</span></span>](#path-geometries-in-direct2d)
-   [<span data-ttu-id="85767-108">Verwenden eines ID2D1GeometrySink zum Auffüllen einer Pfad Geometrie</span><span class="sxs-lookup"><span data-stu-id="85767-108">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [<span data-ttu-id="85767-109">Beispiel: Erstellen einer komplexen Zeichnung</span><span class="sxs-lookup"><span data-stu-id="85767-109">Example: Create a Complex Drawing</span></span>](#example-create-a-complex-drawing)
    -   [<span data-ttu-id="85767-110">Erstellen einer Pfad Geometrie für den linken Berg</span><span class="sxs-lookup"><span data-stu-id="85767-110">Create a Path Geometry for the Left Mountain</span></span>](#create-a-path-geometry-for-the-left-mountain)
    -   [<span data-ttu-id="85767-111">Erstellen einer Pfad Geometrie für den rechten Berg</span><span class="sxs-lookup"><span data-stu-id="85767-111">Create a Path Geometry for the Right Mountain</span></span>](#create-a-path-geometry-for-the-right-mountain)
    -   [<span data-ttu-id="85767-112">Erstellen einer Pfad Geometrie für die Sun</span><span class="sxs-lookup"><span data-stu-id="85767-112">Create a Path Geometry for the Sun</span></span>](#create-a-path-geometry-for-the-sun)
    -   [<span data-ttu-id="85767-113">Erstellen einer Pfad Geometrie für den Fluss</span><span class="sxs-lookup"><span data-stu-id="85767-113">Create a Path Geometry for the River</span></span>](#create-a-path-geometry-for-the-river)
    -   [<span data-ttu-id="85767-114">Rendering der Pfadgeometrien auf der Anzeige</span><span class="sxs-lookup"><span data-stu-id="85767-114">Render the Path Geometries onto the Display</span></span>](#render-the-path-geometries-onto-the-display)
-   [<span data-ttu-id="85767-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85767-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="85767-116">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="85767-116">Prerequisites</span></span>

<span data-ttu-id="85767-117">Diese Übersicht setzt voraus, dass Sie mit dem Erstellen von grundlegenden Direct2D-Anwendungen vertraut sind, wie unter [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="85767-117">This overview assumes that you are familiar with creating basic Direct2D applications, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span> <span data-ttu-id="85767-118">Außerdem wird davon ausgegangen, dass Sie mit den grundlegenden Features von Direct2D Geometries vertraut sind, wie in [Übersicht über Geometrien](direct2d-geometries-overview.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="85767-118">It also assumes that you are familiar with the basic features of Direct2D geometries, as described in the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="path-geometries-in-direct2d"></a><span data-ttu-id="85767-119">Pfadgeometrien in Direct2D</span><span class="sxs-lookup"><span data-stu-id="85767-119">Path Geometries in Direct2D</span></span>

<span data-ttu-id="85767-120">Pfadgeometrien werden durch die [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="85767-120">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="85767-121">Um eine Pfad Geometrie zu instanziieren, müssen Sie die [**ID2D1Factory:: kreatepathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="85767-121">To instantiate a path geometry, call the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span> <span data-ttu-id="85767-122">Diese Objekte können verwendet werden, um komplexe geometrische Abbildungen zu beschreiben, die aus Segmenten wie Arcs, Kurven und Linien bestehen.</span><span class="sxs-lookup"><span data-stu-id="85767-122">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="85767-123">Um eine Pfad Geometrie mit Abbildungen und Segmenten aufzufüllen, rufen Sie die [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) -Methode auf, um ein [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) abzurufen, und verwenden Sie die Methoden der Geometry-Senke, um der Pfad Geometrie Abbildungen und Segmente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="85767-123">To populate a path geometry with figures and segments, call the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) and use the geometry sink's methods to add figures and segments to the path geometry.</span></span>

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a><span data-ttu-id="85767-124">Verwenden eines ID2D1GeometrySink zum Auffüllen einer Pfad Geometrie</span><span class="sxs-lookup"><span data-stu-id="85767-124">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>

<span data-ttu-id="85767-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) beschreibt einen geometrischen Pfad, der Linien, Arcs, kubische Bezier-Kurven und quadratische Bezier-Kurven enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="85767-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) describes a geometric path that can contain lines, arcs, cubic Bezier curves, and quadratic Bezier curves.</span></span>

<span data-ttu-id="85767-126">Eine Geometry-Senke besteht aus einer oder mehreren Abbildungen.</span><span class="sxs-lookup"><span data-stu-id="85767-126">A geometry sink consists of one or more figures.</span></span> <span data-ttu-id="85767-127">Jede Abbildung besteht aus einem oder mehreren Linien-, Kurven-oder Bogen Segmenten.</span><span class="sxs-lookup"><span data-stu-id="85767-127">Each figure is made up of one or more line, curve, or arc segments.</span></span> <span data-ttu-id="85767-128">Rufen Sie zum Erstellen einer Abbildung die [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) -Methode auf, und übergeben Sie den Anfangspunkt der Abbildung. verwenden Sie dann die Add-Methoden (z. b. [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) und [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ), um Segmente hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="85767-128">To create a figure, call the [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) method, passing in the figure's starting point, and then use its Add methods (such as [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) and [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to add segments.</span></span> <span data-ttu-id="85767-129">Wenn Sie das Hinzufügen von Segmenten abgeschlossen haben, müssen Sie die [**endfigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="85767-129">When you are finished adding segments, call the [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) method.</span></span> <span data-ttu-id="85767-130">Sie können diese Sequenz wiederholen, um zusätzliche Abbildungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="85767-130">You can repeat this sequence to create additional figures.</span></span> <span data-ttu-id="85767-131">Wenn Sie mit dem Erstellen von Abbildungen fertig sind, müssen Sie die [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="85767-131">When you are finished creating figures, call the [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) method.</span></span>

## <a name="example-create-a-complex-drawing"></a><span data-ttu-id="85767-132">Beispiel: Erstellen einer komplexen Zeichnung</span><span class="sxs-lookup"><span data-stu-id="85767-132">Example: Create a Complex Drawing</span></span>

<span data-ttu-id="85767-133">Die folgende Abbildung zeigt eine komplexe Zeichnung mit Linien-, Arcs-und Bezier-Kurven.</span><span class="sxs-lookup"><span data-stu-id="85767-133">The following illustration shows a complex drawing with lines, arcs, and Bezier curves.</span></span> <span data-ttu-id="85767-134">Das folgende Codebeispiel zeigt, wie die Zeichnung mithilfe von vier Pfad Geometrie Objekten erstellt wird, eine für den linken Berg, eine für den rechten Berg, eine für den Fluss und eine für die Sonne mit Flares.</span><span class="sxs-lookup"><span data-stu-id="85767-134">The code example that follows shows how to create the drawing by using four path geometry objects, one for the left mountain, one for the right mountain, one for the river, and one for the sun with flares.</span></span>

![Darstellung eines Flusses, Gebirges und der Sonne mithilfe von Pfadgeometrien](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a><span data-ttu-id="85767-136">Erstellen einer Pfad Geometrie für den linken Berg</span><span class="sxs-lookup"><span data-stu-id="85767-136">Create a Path Geometry for the Left Mountain</span></span>

<span data-ttu-id="85767-137">Im Beispiel wird zuerst eine Pfad Geometrie für den linken Berg erstellt, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="85767-137">The example first creates a path geometry for the left mountain as shown in the following illustration.</span></span>

![Zeigt eine komplexe Zeichnung eines Polygons, das einen Berg anzeigt.](images/path-geo-leftmnt.png)

<span data-ttu-id="85767-139">Um den linken Berg zu erstellen, ruft das Beispiel die [**ID2D1Factory:: kreatepathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) -Methode auf, um eine [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="85767-139">To create the left mountain, the example calls the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



<span data-ttu-id="85767-140">Im Beispiel wird dann die [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) -Methode verwendet, um eine Geometry-Senke von einem [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) abzurufen und in der *psink* -Variablen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="85767-140">The example then uses the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to obtain a geometry sink from an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and stores it in the *pSink* variable.</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



<span data-ttu-id="85767-141">Im Beispiel wird dann [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure)aufgerufen, wobei die [**D2D1 \_ Figure \_ Begin \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) Fill-Funktion übergeben wird, die angibt, dass diese Abbildung ausgefüllt ist. Anschließend werden [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines)aufgerufen und ein Array von [**D2D1 \_ Point \_ 2F**](d2d1-point-2f.md) -Punkten, (267, 177), (236, 192), (212, 160), (156, 255) und (346, 255) übergeben.</span><span class="sxs-lookup"><span data-stu-id="85767-141">The example then calls [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passing in [**D2D1\_FIGURE\_BEGIN\_FILLED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) that indicates this figure is filled, then calls [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passing in an array of [**D2D1\_POINT\_2F**](d2d1-point-2f.md) points, (267, 177), (236, 192), (212, 160), (156, 255) and (346, 255).</span></span>

<span data-ttu-id="85767-142">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="85767-142">The following code shows how to do this.</span></span>


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a><span data-ttu-id="85767-143">Erstellen einer Pfad Geometrie für den rechten Berg</span><span class="sxs-lookup"><span data-stu-id="85767-143">Create a Path Geometry for the Right Mountain</span></span>

<span data-ttu-id="85767-144">Im Beispiel wird dann eine weitere Pfad Geometrie für den rechten Berg mit Punkten (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) und (575, 263) erstellt.</span><span class="sxs-lookup"><span data-stu-id="85767-144">The example then creates another path geometry for the right mountain with points (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263), and (575, 263).</span></span> <span data-ttu-id="85767-145">Die folgende Abbildung zeigt, wie der Rechte Berg angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="85767-145">The following illustration shows how the right mountain is displayed.</span></span>

![Abbildung eines Polygons, das einen Berg anzeigt](images/path-geo-rightmnt.png)

<span data-ttu-id="85767-147">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="85767-147">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a><span data-ttu-id="85767-148">Erstellen einer Pfad Geometrie für die Sun</span><span class="sxs-lookup"><span data-stu-id="85767-148">Create a Path Geometry for the Sun</span></span>

<span data-ttu-id="85767-149">Das Beispiel füllt dann eine andere Pfad Geometrie für die Sun, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="85767-149">The example then populates another path geometry for the sun as shown in the following illustration.</span></span>

![Abbildung einer Bogen-und Bézier-Kurven, die die Sonne zeigen](images/path-geo-sun.png)

<span data-ttu-id="85767-151">Zu diesem Zweck erstellt die Pfad Geometrie eine Senke und fügt eine Abbildung für den Bogen und eine Abbildung für jede Fackel der Senke hinzu.</span><span class="sxs-lookup"><span data-stu-id="85767-151">To do this, the path geometry creates a sink, and adds a figure for the arc and a figure for each flare to the sink.</span></span> <span data-ttu-id="85767-152">Durch Wiederholen der Sequenz von [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), der Add-Methode (z. b. [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) und [**endfigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure)werden der Senke mehrere Abbildungen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="85767-152">By repeating the sequence of [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), its Add (such as [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) methods, and [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), multiple figures are added to the sink.</span></span>

<span data-ttu-id="85767-153">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="85767-153">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a><span data-ttu-id="85767-154">Erstellen einer Pfad Geometrie für den Fluss</span><span class="sxs-lookup"><span data-stu-id="85767-154">Create a Path Geometry for the River</span></span>

<span data-ttu-id="85767-155">Im Beispiel wird dann ein weiterer Geometry-Pfad für den Fluss erstellt, der Bezier-Kurven enthält.</span><span class="sxs-lookup"><span data-stu-id="85767-155">The example then creates another geometry path for the river that contains Bezier curves.</span></span> <span data-ttu-id="85767-156">In der folgenden Abbildung wird gezeigt, wie der Fluss angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="85767-156">The following illustration shows how the river is displayed.</span></span>

![Abbildung der Bézier-Kurven, die einen Fluss anzeigen](images/path-geo-river.png)

<span data-ttu-id="85767-158">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="85767-158">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a><span data-ttu-id="85767-159">Rendering der Pfadgeometrien auf der Anzeige</span><span class="sxs-lookup"><span data-stu-id="85767-159">Render the Path Geometries onto the Display</span></span>

<span data-ttu-id="85767-160">Der folgende Code zeigt, wie die aufgefüllten Pfadgeometrien in der Anzeige dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="85767-160">The following code shows how to render the populated path geometries on the display.</span></span> <span data-ttu-id="85767-161">Zuerst wird die Sun-Geometrie gezeichnet und gezeichnet, als nächstes die linke Mountain-Geometrie, dann die flussgeometrie und schließlich die Rechte Mountain-Geometrie.</span><span class="sxs-lookup"><span data-stu-id="85767-161">It first draws and paints the sun geometry, next the left mountain geometry, then the river geometry, and finally the right mountain geometry.</span></span>


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



<span data-ttu-id="85767-162">Im Beispiel wird die folgende Abbildung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="85767-162">The complete example outputs the following illustration.</span></span>

![Darstellung eines Flusses, Gebirges und der Sonne mithilfe von Pfadgeometrien](images/path-geo-mnts.png)

## <a name="related-topics"></a><span data-ttu-id="85767-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85767-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85767-165">Erstellen einer einfachen Direct2D-Anwendung</span><span class="sxs-lookup"><span data-stu-id="85767-165">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> <dt>

[<span data-ttu-id="85767-166">Übersicht über Geometrien</span><span class="sxs-lookup"><span data-stu-id="85767-166">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> </dl>

 

 