---
title: Überblick über die Interoperabilität
description: Fasst die verschiedenen Technologien zusammen, die Sie mit Direct2D verwenden können.
ms.assetid: 41f3b908-d218-4a47-bfc3-6a37d38ca26a
keywords:
- Direct2D, GDI-Interoperation
- Direct2D, GDI+-Interoperation
- Direct2D, Interoperabilität
- Direct2D, DirectWrite-Interoperation
- Interoperabilität, Direct2D
- Interoperabilität, Direct3D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- Interoperabilität, Graphics Device Interface (GDI)
- Interoperabilität, GDI+
- DirectWrite-Interoperabilität
- Interoperabilität, DirectWrite
- Windows Imaging-Komponente (WIC)
- WIC (Windows Imaging-Komponente)
- Interoperabilität, Windows Imaging Component (WIC)
- Direct2D, WIC-Interoperation
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6f56c570a837a541bac9467477d4f6009bda019e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390490"
---
# <a name="interoperability-overview"></a><span data-ttu-id="9bf12-119">Überblick über die Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-119">Interoperability Overview</span></span>

<span data-ttu-id="9bf12-120">Eines der wichtigsten Features von renderingkonventionen ist die Aktivierung der Interoperabilität zwischen Direct2D und anderen renderingplattformen, damit Entwickler die spezifischen Stärken der einzelnen Plattformen nutzen können, ohne dass Sie zu Kompromittierungen gezwungen werden, indem Sie eine Plattform für alle Anforderungen auswählen.</span><span class="sxs-lookup"><span data-stu-id="9bf12-120">One of Direct2D's key features is enabling interoperability between Direct2D and other rendering platforms so that developers can use the specific strengths of each platform without being forced into compromises by choosing one platform for all needs.</span></span> <span data-ttu-id="9bf12-121">In diesem Thema werden die verschiedenen Plattformen zusammengefasst, mit denen Direct2D interoperabel ist.</span><span class="sxs-lookup"><span data-stu-id="9bf12-121">This topic summarizes the different platforms with which Direct2D is interoperable.</span></span> <span data-ttu-id="9bf12-122">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="9bf12-122">It contains the following sections.</span></span>

-   [<span data-ttu-id="9bf12-123">GDI-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-123">GDI Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="9bf12-124">GDI+-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-124">GDI+ Interoperability</span></span>](#gdi-interoperability)
-   [<span data-ttu-id="9bf12-125">Direct3D-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-125">Direct3D Interoperability</span></span>](#direct3d-interoperability)
-   [<span data-ttu-id="9bf12-126">DirectWrite-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-126">DirectWrite Interoperability</span></span>](#directwrite-interoperability)
-   [<span data-ttu-id="9bf12-127">Interoperabilität von Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="9bf12-127">Windows Imaging Component (WIC) Interoperability</span></span>](#windows-imaging-component-wic-interoperability)
-   [<span data-ttu-id="9bf12-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9bf12-128">Related topics</span></span>](#related-topics)

<span data-ttu-id="9bf12-129">Das folgende Diagramm fasst die verschiedenen Plattformen zusammen, mit denen Direct2D interoperabel ist, und listet einige Methoden und Schnittstellen auf, die Interoperabilität bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9bf12-129">The following diagram summarizes the different platforms with which Direct2D is interoperable and lists some methods and interfaces that provide interoperability.</span></span>

![Diagramm der Plattformen, mit denen Direct2D interagiert, einschließlich Direct3D 10,1, DirectWrite, WIC, GDI+ und GDI](images/direct2dinterop.png)

## <a name="gdi-interoperability"></a><span data-ttu-id="9bf12-131">GDI-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-131">GDI Interoperability</span></span>

<span data-ttu-id="9bf12-132">Direct2D ermöglicht die bidirektionale Interoperabilität mit GDI.</span><span class="sxs-lookup"><span data-stu-id="9bf12-132">Direct2D enables two-way interoperability with GDI.</span></span> <span data-ttu-id="9bf12-133">Sie können ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) -Objekt verwenden, um Direct2D-Inhalte in einen GDI- [Gerätekontext](/windows/desktop/gdi/device-contexts) (DC) zu schreiben, oder Sie können [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) verwenden, um eine DC-Darstellung eines Renderziels zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9bf12-133">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to a GDI [device context](/windows/desktop/gdi/device-contexts) (DC), or you can use [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to obtain a DC representation of a render target.</span></span>

<span data-ttu-id="9bf12-134">Weitere Informationen und Beispiele finden Sie in der [Übersicht über die Interoperabilität zwischen Direct2D und GDI](direct2d-and-gdi-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9bf12-134">For more information and examples, see the [Direct2D and GDI Interoperability Overview](direct2d-and-gdi-interoperation-overview.md).</span></span>

## <a name="gdi-interoperability"></a><span data-ttu-id="9bf12-135">GDI+-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-135">GDI+ Interoperability</span></span>

<span data-ttu-id="9bf12-136">Sie können GDI+ mit Direct2D auf die gleiche Weise wie GDI verwenden.</span><span class="sxs-lookup"><span data-stu-id="9bf12-136">You can use GDI+ with Direct2D in the same manner as GDI.</span></span> <span data-ttu-id="9bf12-137">Sie können ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) -Objekt verwenden, um Direct2D-Inhalte auf denselben Domänen Controller wie den GDI+-Inhalt zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="9bf12-137">You can use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) to write Direct2D content to the same DC as your GDI+ content.</span></span> <span data-ttu-id="9bf12-138">Mit diesem Ansatz können Sie Anwendungen hinzufügen, die in erster Linie mithilfe von GDI+ durch Rendering von Direct2D-Inhalten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9bf12-138">This approach enables you to start adding Direct2D content to applications that primarily render by using GDI+.</span></span>

<span data-ttu-id="9bf12-139">Sie können auch einen [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) verwenden, um Zugriff auf einen GDI-Domänen Controller bereitzustellen, der mithilfe von Direct2D schreibt, und dann die [**FromHdc**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) -Methode verwenden, um ein-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bf12-139">You can also use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) to provide access to a GDI DC that writes by using Direct2D, and then use the [**FromHDC**](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-fromhdc(inhdc)) method to create a object.</span></span> <span data-ttu-id="9bf12-140">Diese Vorgehensweise ist nützlich für Anwendungen, die in erster Linie mit Direct2D Rendering, aber über ein Erweiterbarkeits Modell oder andere Legacy Inhalte verfügen, die die Fähigkeit zum Rendering mit GDI+ erfordern.</span><span class="sxs-lookup"><span data-stu-id="9bf12-140">This approach is useful for applications that primarily render with Direct2D, but have an extensibility model or other legacy content that requires the ability to render with GDI+.</span></span>

## <a name="direct3d-interoperability"></a><span data-ttu-id="9bf12-141">Direct3D-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-141">Direct3D Interoperability</span></span>

<span data-ttu-id="9bf12-142">Direct2D kann ein DXGI-Oberflächen Renderziel (erstellt von der Methode " [**kreatedxgisurfacerender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ") verwenden, um in eine [idxgisurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface)zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="9bf12-142">Direct2D can use a DXGI surface render target (created by the [**CreateDxgiSurfaceRender**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) method) to write to an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface).</span></span> <span data-ttu-id="9bf12-143">Diese Aktion ermöglicht Ihnen das Hinzufügen von 2D-Hintergründen und-Schnittstellen zu 3D-Szenen und die Verwendung von Direct2D-Inhalten als Textur für ein 3D-Modell.</span><span class="sxs-lookup"><span data-stu-id="9bf12-143">This action enables you to add 2-D backgrounds and interfaces to 3-D scenes and use Direct2D content as a texture for a 3-D model.</span></span> <span data-ttu-id="9bf12-144">Direct2D kann auch eine [idxgisurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) -Methode verwenden und die Methode " [**kreatesharedbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) " verwenden, um eine Bitmap-Darstellung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9bf12-144">Direct2D can also take an [IDXGISurface](/windows/win32/api/dxgi/nn-dxgi-idxgisurface) and use the [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) method to create a bitmap representation.</span></span>

<span data-ttu-id="9bf12-145">Weitere Informationen und Beispiele finden Sie unter [Übersicht über die Interoperabilität mit Direct2D und Direct3D](direct2d-and-direct3d-interoperation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="9bf12-145">For more information and examples, see the [Direct2D and Direct3D Interoperability Overview](direct2d-and-direct3d-interoperation-overview.md).</span></span>

## <a name="directwrite-interoperability"></a><span data-ttu-id="9bf12-146">DirectWrite-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-146">DirectWrite Interoperability</span></span>

<span data-ttu-id="9bf12-147">Direct2D ist eng in DirectWrite integriert.</span><span class="sxs-lookup"><span data-stu-id="9bf12-147">Direct2D is tightly integrated with DirectWrite.</span></span> <span data-ttu-id="9bf12-148">Direct2D erleichtert das Rendering von DirectWrite-Inhalten durch Bereitstellen der Methoden [**DrawText**](id2d1rendertarget-drawtext.md), [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)und [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) .</span><span class="sxs-lookup"><span data-stu-id="9bf12-148">Direct2D makes it easy to render DirectWrite content by providing the [**DrawText**](id2d1rendertarget-drawtext.md), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout), and [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) methods.</span></span>

## <a name="windows-imaging-component-wic-interoperability"></a><span data-ttu-id="9bf12-149">Interoperabilität von Windows Imaging Component (WIC)</span><span class="sxs-lookup"><span data-stu-id="9bf12-149">Windows Imaging Component (WIC) Interoperability</span></span>

<span data-ttu-id="9bf12-150">Direct2D [**stellt die Methoden**](id2d1rendertarget-createbitmapfromwicbitmap.md)"", "" "" "" "" "" "" "" "" "" "" "" "" "" "," "", "" [**","**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap)"", " [**" und "**](id2d1factory-createwicbitmaprendertarget.md) "</span><span class="sxs-lookup"><span data-stu-id="9bf12-150">Direct2D provides the [**CreateBitmapFromWicBitmap**](id2d1rendertarget-createbitmapfromwicbitmap.md), [**CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap), and [**CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) methods for manipulating WIC bitmaps.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9bf12-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9bf12-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bf12-152">Übersicht über die Direct2D-und GDI-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="9bf12-152">Direct2D and GDI Interoperability Overview</span></span>](direct2d-and-gdi-interoperation-overview.md)
</dt> <dt>

[<span data-ttu-id="9bf12-153">Übersicht über die Interoperabilität von Direct2D und Direct3D</span><span class="sxs-lookup"><span data-stu-id="9bf12-153">Direct2D and Direct3D Interoperability Overview</span></span>](direct2d-and-direct3d-interoperation-overview.md)
</dt> </dl>

 

 