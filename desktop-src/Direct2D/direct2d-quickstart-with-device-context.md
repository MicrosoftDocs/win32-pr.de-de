---
title: Direct2D-Schnellstart für Windows 8
description: Fasst die Schritte zusammen, die zum Zeichnen mit Direct2D für Windows 8 erforderlich sind, und stellt Beispielcode bereit. Direct2D ist eine NATIVE CODE-API zum Erstellen von 2D-Grafiken.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Beispiel für Direct2D,Zeichnen von Rechteckcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43442e57ed0949bdf39fc05ce1a69fded42b4b3d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406143"
---
# <a name="direct2d-quickstart-for-windows-8"></a><span data-ttu-id="26f8e-105">Direct2D-Schnellstart für Windows 8</span><span class="sxs-lookup"><span data-stu-id="26f8e-105">Direct2D Quickstart for Windows 8</span></span>

<span data-ttu-id="26f8e-106">Direct2D ist eine nativ codierte API im Direktmodus zum Erstellen von 2D-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="26f8e-106">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="26f8e-107">In diesem Thema wird veranschaulicht, wie Direct2D verwendet wird, um in ein [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="26f8e-107">This topic illustrates how to use Direct2D to draw to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

<span data-ttu-id="26f8e-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="26f8e-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="26f8e-109">Zeichnen eines einfachen Rechtecks</span><span class="sxs-lookup"><span data-stu-id="26f8e-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="26f8e-110">Schritt 1: Einschließen des Direct2D-Headers</span><span class="sxs-lookup"><span data-stu-id="26f8e-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="26f8e-111">Schritt 2: Erstellen einer ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="26f8e-111">Step 2: Create an ID2D1Factory1</span></span>](#step-2-create-an-id2d1factory1)
-   [<span data-ttu-id="26f8e-112">Schritt 3: Erstellen einer ID2D1Device und eines ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="26f8e-112">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [<span data-ttu-id="26f8e-113">Schritt 4: Erstellen eines Pinsels</span><span class="sxs-lookup"><span data-stu-id="26f8e-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="26f8e-114">Schritt 5: Zeichnen des Rechtecks</span><span class="sxs-lookup"><span data-stu-id="26f8e-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="26f8e-115">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="26f8e-115">Example code</span></span>](#example-code)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="26f8e-116">Zeichnen eines einfachen Rechtecks</span><span class="sxs-lookup"><span data-stu-id="26f8e-116">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="26f8e-117">Um ein Rechteck mithilfe von [GDI](/windows/desktop/gdi/windows-gdi)zu zeichnen, können Sie die [**WM \_ PAINT-Meldung**](/windows/desktop/gdi/wm-paint) behandeln, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="26f8e-117">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



<span data-ttu-id="26f8e-118">Der Code zum Zeichnen desselben Rechtecks mit Direct2D ist ähnlich: Er erstellt Zeichnungsressourcen, beschreibt eine zu zeichnende Form, zeichnet die Form und gibt dann die Zeichnungsressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="26f8e-118">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="26f8e-119">In den folgenden Abschnitten werden die einzelnen Schritte ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="26f8e-119">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="26f8e-120">Schritt 1: Einschließen des Direct2D-Headers</span><span class="sxs-lookup"><span data-stu-id="26f8e-120">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="26f8e-121">Schließen Sie zusätzlich zu den für die Anwendung erforderlichen Headern die Header d2d1.h und d2d1 \_ 1.h ein.</span><span class="sxs-lookup"><span data-stu-id="26f8e-121">In addition to the headers required for the application, include the d2d1.h and d2d1\_1.h headers.</span></span>

## <a name="step-2-create-an-id2d1factory1"></a><span data-ttu-id="26f8e-122">Schritt 2: Erstellen einer ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="26f8e-122">Step 2: Create an ID2D1Factory1</span></span>

<span data-ttu-id="26f8e-123">Eines der ersten Dinge, die ein Direct2D-Beispiel macht, ist das Erstellen einer [**ID2D1Factory1.**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)</span><span class="sxs-lookup"><span data-stu-id="26f8e-123">One of the first things that any Direct2D example does is create an [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span></span>


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



<span data-ttu-id="26f8e-124">Die [**ID2D1Factory1-Schnittstelle**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) ist der Ausgangspunkt für die Verwendung von Direct2D. Verwenden Sie **eine ID2D1Factory1,** um Direct2D-Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="26f8e-124">The [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface is the starting point for using Direct2D; use an **ID2D1Factory1** to create Direct2D resources.</span></span>

<span data-ttu-id="26f8e-125">Wenn Sie eine Factory erstellen, können Sie angeben, ob es sich um multi- oder singlethreaded handelt.</span><span class="sxs-lookup"><span data-stu-id="26f8e-125">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="26f8e-126">(Weitere Informationen zu Multithreadfactorys finden Sie in den Hinweisen auf der [**ID2D1Factory-Referenzseite.)**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) In diesem Beispiel wird eine Singlethreadfactory erstellt.</span><span class="sxs-lookup"><span data-stu-id="26f8e-126">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="26f8e-127">Im Allgemeinen sollte Ihre Anwendung die Factory einmal erstellen und für die Lebensdauer der Anwendung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="26f8e-127">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a><span data-ttu-id="26f8e-128">Schritt 3: Erstellen einer ID2D1Device und eines ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="26f8e-128">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>

<span data-ttu-id="26f8e-129">Nachdem Sie eine Factory erstellt haben, verwenden Sie sie, um ein Direct2D-Gerät zu erstellen, und verwenden Sie dann das Gerät, um einen Direct2D-Gerätekontext zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="26f8e-129">After you create a factory, use it to create a Direct2D device and then use the device to create a Direct2D device context.</span></span> <span data-ttu-id="26f8e-130">Zum Erstellen dieser Direct2D-Objekte benötigen Sie ein [**Direct3D 11-Gerät,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ein [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)und eine [**DXGI-Swapkette.**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)</span><span class="sxs-lookup"><span data-stu-id="26f8e-130">In order to create these Direct2D objects, you must have a [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , a [**DXGI device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice), and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="26f8e-131">Informationen zum Erstellen der erforderlichen Voraussetzungen finden Sie unter [Geräte und Gerätekontexte.](devices-and-device-contexts.md)</span><span class="sxs-lookup"><span data-stu-id="26f8e-131">See [Devices and Device Contexts](devices-and-device-contexts.md) for info on creating the necessary prerequisites.</span></span>


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



<span data-ttu-id="26f8e-132">Ein Gerätekontext ist ein Gerät, das Zeichnungsvorgänge ausführen und geräteabhängige Zeichnungsressourcen wie Pinsel erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="26f8e-132">A device context is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="26f8e-133">Sie verwenden auch den Gerätekontext, um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit einer DXGI-Oberfläche zu verknüpfen, die als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26f8e-133">You also use the device context to link a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) to a DXGI surface to use as a render target.</span></span> <span data-ttu-id="26f8e-134">Der Gerätekontext kann auf verschiedene Arten von Zielen gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="26f8e-134">The device context can render to different types of targets.</span></span>

<span data-ttu-id="26f8e-135">Der Code deklariert hier die Eigenschaften für Bitmaps, die mit einer DXGI-Swapkette verknüpft sind, die in einem [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="26f8e-135">The code here declares the properties for bitmap that links to a DXGI swap chain that renders to a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span> <span data-ttu-id="26f8e-136">Die [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) ruft eine Direct2D-Oberfläche von der DXGI-Oberfläche ab.</span><span class="sxs-lookup"><span data-stu-id="26f8e-136">The [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method gets a Direct2D surface from the DXGI surface.</span></span> <span data-ttu-id="26f8e-137">Dadurch wird alles, was in der [**Ziel-ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) gerendert wird, auf die Oberfläche der Swapkette gerendert.</span><span class="sxs-lookup"><span data-stu-id="26f8e-137">This makes it so anything rendered to the target [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is rendered to the surface of the swap chain.</span></span>

<span data-ttu-id="26f8e-138">Sobald Sie über die Direct2D-Oberfläche verfügen, verwenden Sie die [**ID2D1DeviceContext::SetTarget-Methode,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) um sie als aktives Renderziel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="26f8e-138">Once you have the Direct2D surface, use the [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) method to set it as the active render target.</span></span>


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a><span data-ttu-id="26f8e-139">Schritt 4: Erstellen eines Pinsels</span><span class="sxs-lookup"><span data-stu-id="26f8e-139">Step 4: Create a Brush</span></span>

<span data-ttu-id="26f8e-140">Wie bei einer Factory kann ein Gerätekontext Zeichnungsressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="26f8e-140">Like a factory, a device context can create drawing resources.</span></span> <span data-ttu-id="26f8e-141">In diesem Beispiel erstellt der Gerätekontext einen Pinsel.</span><span class="sxs-lookup"><span data-stu-id="26f8e-141">In this example, the device context creates a brush.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



<span data-ttu-id="26f8e-142">Ein Pinsel ist ein Objekt, das einen Bereich zeichnet, z. B. den Strich einer Form oder die Füllung einer Geometrie.</span><span class="sxs-lookup"><span data-stu-id="26f8e-142">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="26f8e-143">Der Pinsel in diesem Beispiel zeichnet einen Bereich mit einer vordefinierten Volltonfarbe Schwarz.</span><span class="sxs-lookup"><span data-stu-id="26f8e-143">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="26f8e-144">Direct2D bietet auch andere Arten von Pinseln: Farbverlaufspinsel zum Zeichnen linearer und radialer Farbverläufe, ein [**Bitmappinsel**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zum Zeichnen mit Bitmaps und Mustern und beginnend in Windows 8 ein [**Bildpinsel**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) zum Zeichnen mit einem gerenderten Bild.</span><span class="sxs-lookup"><span data-stu-id="26f8e-144">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, a [**bitmap brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) for painting with bitmaps and patterns, and starting in Windows 8, an [**image brush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) for painting with a rendered image.</span></span>

<span data-ttu-id="26f8e-145">Einige Zeichnungs-APIs stellen Stifte zum Zeichnen von Konturen und Pinsel zum Füllen von Formen bereit.</span><span class="sxs-lookup"><span data-stu-id="26f8e-145">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="26f8e-146">Direct2D ist anders: Es stellt kein Stiftobjekt bereit, sondern verwendet einen Pinsel zum Zeichnen von Konturen und Füllen von Formen.</span><span class="sxs-lookup"><span data-stu-id="26f8e-146">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="26f8e-147">Verwenden Sie beim Zeichnen von Konturen die [**ID2D1StrokeStyle-Schnittstelle,**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) oder beginnen Sie in Windows 8 der [**ID2D1StrokeStyle1-Schnittstelle**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) mit einem Pinsel, um Pfad-Strichvorgänge zu steuern.</span><span class="sxs-lookup"><span data-stu-id="26f8e-147">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface, or starting in Windows 8 the [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) interface, with a brush to control path stroking operations.</span></span>

<span data-ttu-id="26f8e-148">Ein Pinsel kann nur mit dem Renderziel, das ihn erstellt hat, und mit anderen Renderzielen in derselben Ressourcendomäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26f8e-148">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="26f8e-149">Im Allgemeinen sollten Sie Pinsel einmal erstellen und für die Lebensdauer des Renderziels beibehalten, das sie erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="26f8e-149">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="26f8e-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ist die einzige Ausnahme. Da die Erstellung relativ kostengünstig ist, können Sie jedes Mal, wenn Sie einen Frame zeichnen, einen **ID2D1SolidColorBrush** erstellen, ohne dass eine spürbare Leistungssteigerung auftritt.</span><span class="sxs-lookup"><span data-stu-id="26f8e-150">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="26f8e-151">Sie können auch einen einzelnen **ID2D1SolidColorBrush** verwenden und bei jeder Verwendung einfach seine Farbe oder Deckkraft ändern.</span><span class="sxs-lookup"><span data-stu-id="26f8e-151">You can also use a single **ID2D1SolidColorBrush** and just change its color or opacity every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="26f8e-152">Schritt 5: Zeichnen des Rechtecks</span><span class="sxs-lookup"><span data-stu-id="26f8e-152">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="26f8e-153">Verwenden Sie als Nächstes den Gerätekontext, um das Rechteck zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="26f8e-153">Next, use the device context to draw the rectangle.</span></span>


```C++
 
m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



<span data-ttu-id="26f8e-154">Die [**DrawRectangle-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) verwendet zwei Parameter: das zu zeichnende Rechteck und den Pinsel, der zum Zeichnen der Kontur des Rechtecks verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="26f8e-154">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="26f8e-155">Optional können Sie auch die Optionen Strichbreite, Bindestrichmuster, Linienverknüpfung und Endendeende angeben.</span><span class="sxs-lookup"><span data-stu-id="26f8e-155">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="26f8e-156">Sie müssen die [**BeginDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) aufrufen, bevor Sie Zeichnungsbefehle ausgeben, und Sie müssen die [**EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) aufrufen, nachdem Sie mit dem Ausgeben von Zeichnungsbefehlen fertig sind.</span><span class="sxs-lookup"><span data-stu-id="26f8e-156">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="26f8e-157">Die **EndDraw-Methode** gibt ein **HRESULT** zurück, das angibt, ob die Zeichnungsbefehle erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="26f8e-157">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span> <span data-ttu-id="26f8e-158">Wenn dies nicht erfolgreich ist, löst die Hilfsfunktion ThrowIfFailed eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="26f8e-158">If it is not successful, the ThrowIfFailed helper function will throw an exception.</span></span>

<span data-ttu-id="26f8e-159">Die [**IDXGISwapChain::P Resent-Methode tauscht**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) die Pufferoberfläche mit der Bildschirmoberfläche aus, um das Ergebnis anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="26f8e-159">The [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method swaps the buffer surface with the on screen surface to display the result.</span></span>

## <a name="example-code"></a><span data-ttu-id="26f8e-160">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="26f8e-160">Example code</span></span>

<span data-ttu-id="26f8e-161">Der Code in diesem Thema zeigt die grundlegenden Elemente einer Direct2D-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="26f8e-161">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="26f8e-162">Aus Gründen der Kürze werden im Thema das Anwendungsframework und der Fehlerbehandlungscode ausgelassen, der ein Merkmal einer gut geschriebenen Anwendung ist.</span><span class="sxs-lookup"><span data-stu-id="26f8e-162">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span>

 

 