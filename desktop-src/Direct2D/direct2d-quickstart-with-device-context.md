---
title: Direct2D Schnellstart für Windows 8
description: Fasst die Schritte zusammen, die zum Zeichnen mit Direct2D erforderlich sind, und stellt Beispielcode bereit.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, Codebeispiel zum Zeichnen des Rechtecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e5cfbbf4e63e129a43bec783a64203e20e30a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341315"
---
# <a name="direct2d-quickstart-for-windows-8"></a><span data-ttu-id="620e1-104">Direct2D Schnellstart für Windows 8</span><span class="sxs-lookup"><span data-stu-id="620e1-104">Direct2D Quickstart for Windows 8</span></span>

<span data-ttu-id="620e1-105">Direct2D ist eine API im einheitlichen Code zum Erstellen von 2D-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="620e1-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="620e1-106">In diesem Thema wird veranschaulicht, wie Direct2D verwendet wird, um zu einem [**Windows:: UI:: Core:: corewindow**](/uwp/api/Windows.UI.Core.CoreWindow)zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="620e1-106">This topic illustrates how to use Direct2D to draw to a [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span>

<span data-ttu-id="620e1-107">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="620e1-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="620e1-108">Zeichnen eines einfachen Rechtecks</span><span class="sxs-lookup"><span data-stu-id="620e1-108">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="620e1-109">Schritt 1: einschließen des Direct2D-Headers</span><span class="sxs-lookup"><span data-stu-id="620e1-109">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="620e1-110">Schritt 2: Erstellen eines ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="620e1-110">Step 2: Create an ID2D1Factory1</span></span>](#step-2-create-an-id2d1factory1)
-   [<span data-ttu-id="620e1-111">Schritt 3: Erstellen eines ID2D1Device und eines ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="620e1-111">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [<span data-ttu-id="620e1-112">Schritt 4: Erstellen eines Pinsels</span><span class="sxs-lookup"><span data-stu-id="620e1-112">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="620e1-113">Schritt 5: Zeichnen des Rechtecks</span><span class="sxs-lookup"><span data-stu-id="620e1-113">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="620e1-114">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="620e1-114">Example code</span></span>](#example-code)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="620e1-115">Zeichnen eines einfachen Rechtecks</span><span class="sxs-lookup"><span data-stu-id="620e1-115">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="620e1-116">Wenn Sie ein Rechteck mithilfe von [GDI](/windows/desktop/gdi/windows-gdi)zeichnen möchten, können Sie die [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung wie im folgenden Code gezeigt verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="620e1-116">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="620e1-117">Der Code zum Zeichnen desselben Rechtecks mit Direct2D ist ähnlich: er erstellt Zeichnungs Ressourcen, beschreibt eine Form, die gezeichnet werden soll, zeichnet die Form und gibt dann die Zeichnungs Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="620e1-117">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="620e1-118">In den folgenden Abschnitten werden die einzelnen Schritte ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="620e1-118">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="620e1-119">Schritt 1: einschließen des Direct2D-Headers</span><span class="sxs-lookup"><span data-stu-id="620e1-119">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="620e1-120">Zusätzlich zu den Headern, die für die Anwendung erforderlich sind, schließen Sie die Header d2d1. h und d2d1 \_ 1. h ein.</span><span class="sxs-lookup"><span data-stu-id="620e1-120">In addition to the headers required for the application, include the d2d1.h and d2d1\_1.h headers.</span></span>

## <a name="step-2-create-an-id2d1factory1"></a><span data-ttu-id="620e1-121">Schritt 2: Erstellen eines ID2D1Factory1</span><span class="sxs-lookup"><span data-stu-id="620e1-121">Step 2: Create an ID2D1Factory1</span></span>

<span data-ttu-id="620e1-122">Eines der ersten Dinge, bei denen es sich bei allen Direct2D-Beispielen um das Erstellen eines [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)handelt.</span><span class="sxs-lookup"><span data-stu-id="620e1-122">One of the first things that any Direct2D example does is create an [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1).</span></span>


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



<span data-ttu-id="620e1-123">Die [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) -Schnittstelle ist der Ausgangspunkt für die Verwendung von Direct2D. Verwenden Sie ein **ID2D1Factory1** , um Direct2D-Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="620e1-123">The [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) interface is the starting point for using Direct2D; use an **ID2D1Factory1** to create Direct2D resources.</span></span>

<span data-ttu-id="620e1-124">Beim Erstellen einer Factory können Sie angeben, ob es sich um einen Multithread oder einen Single Thread handelt.</span><span class="sxs-lookup"><span data-stu-id="620e1-124">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="620e1-125">(Weitere Informationen zu Multithread-Factorys finden Sie in den Hinweisen auf der [**ID2D1Factory-Referenzseite**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) In diesem Beispiel wird eine Single Thread Factory erstellt.</span><span class="sxs-lookup"><span data-stu-id="620e1-125">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="620e1-126">Im Allgemeinen sollte die Anwendung die Factory einmal erstellen und für die Lebensdauer der Anwendung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="620e1-126">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a><span data-ttu-id="620e1-127">Schritt 3: Erstellen eines ID2D1Device und eines ID2D1DeviceContext</span><span class="sxs-lookup"><span data-stu-id="620e1-127">Step 3: Create an ID2D1Device and an ID2D1DeviceContext</span></span>

<span data-ttu-id="620e1-128">Nachdem Sie eine Factory erstellt haben, verwenden Sie Sie, um ein Direct2D-Gerät zu erstellen, und verwenden Sie dann das Gerät zum Erstellen eines Direct2D-Geräte Kontexts.</span><span class="sxs-lookup"><span data-stu-id="620e1-128">After you create a factory, use it to create a Direct2D device and then use the device to create a Direct2D device context.</span></span> <span data-ttu-id="620e1-129">Um diese Direct2D-Objekte zu erstellen, müssen Sie über ein [**Direct3D 11-Gerät**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , ein [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)und eine [**DXGI-Swapkette**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)verfügen.</span><span class="sxs-lookup"><span data-stu-id="620e1-129">In order to create these Direct2D objects, you must have a [**Direct3D 11 device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , a [**DXGI device**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice), and a [**DXGI swap chain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1).</span></span> <span data-ttu-id="620e1-130">Informationen zum Erstellen der erforderlichen Voraussetzungen finden Sie unter [Geräte und Geräte Kontexte](devices-and-device-contexts.md) .</span><span class="sxs-lookup"><span data-stu-id="620e1-130">See [Devices and Device Contexts](devices-and-device-contexts.md) for info on creating the necessary prerequisites.</span></span>


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



<span data-ttu-id="620e1-131">Ein Gerätekontext ist ein Gerät, das Zeichnungsvorgänge ausführen und Geräte abhängige Zeichnungs Ressourcen erstellen kann, wie z. b. Pinsel.</span><span class="sxs-lookup"><span data-stu-id="620e1-131">A device context is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="620e1-132">Sie können auch den Gerätekontext verwenden, um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit einer DXGI-Oberfläche zu verknüpfen, die als Renderziel verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="620e1-132">You also use the device context to link a [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) to a DXGI surface to use as a render target.</span></span> <span data-ttu-id="620e1-133">Der Gerätekontext kann in verschiedene Arten von Zielen Rendering.</span><span class="sxs-lookup"><span data-stu-id="620e1-133">The device context can render to different types of targets.</span></span>

<span data-ttu-id="620e1-134">Der Code hier deklariert die Eigenschaften für Bitmap, die mit einer DXGI-SwapChain verknüpft ist, die in ein [**corewindow**](/uwp/api/Windows.UI.Core.CoreWindow)gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="620e1-134">The code here declares the properties for bitmap that links to a DXGI swap chain that renders to a [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow).</span></span> <span data-ttu-id="620e1-135">Die [**ID2D1DeviceContext:: kreatebitmapfromdxgisurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) -Methode ruft eine Direct2D-Oberfläche aus der DXGI-Oberfläche ab.</span><span class="sxs-lookup"><span data-stu-id="620e1-135">The [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) method gets a Direct2D surface from the DXGI surface.</span></span> <span data-ttu-id="620e1-136">Dadurch wird alles, was für das Ziel [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) gerendert wird, auf der Oberfläche der Swapkette gerendert.</span><span class="sxs-lookup"><span data-stu-id="620e1-136">This makes it so anything rendered to the target [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is rendered to the surface of the swap chain.</span></span>

<span data-ttu-id="620e1-137">Nachdem Sie die Direct2D-Oberfläche verwendet haben, verwenden Sie die [**ID2D1DeviceContext:: SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) -Methode, um Sie als aktives Renderziel festzulegen.</span><span class="sxs-lookup"><span data-stu-id="620e1-137">Once you have the Direct2D surface, use the [**ID2D1DeviceContext::SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) method to set it as the active render target.</span></span>


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



## <a name="step-4-create-a-brush"></a><span data-ttu-id="620e1-138">Schritt 4: Erstellen eines Pinsels</span><span class="sxs-lookup"><span data-stu-id="620e1-138">Step 4: Create a Brush</span></span>

<span data-ttu-id="620e1-139">Wie eine Factory kann ein Gerätekontext Zeichnungs Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="620e1-139">Like a factory, a device context can create drawing resources.</span></span> <span data-ttu-id="620e1-140">In diesem Beispiel erstellt der Gerätekontext einen Pinsel.</span><span class="sxs-lookup"><span data-stu-id="620e1-140">In this example, the device context creates a brush.</span></span>


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



<span data-ttu-id="620e1-141">Ein Pinsel ist ein Objekt, das einen Bereich zeichnet, z. b. den Strich einer Form oder das Ausfüllen einer Geometrie.</span><span class="sxs-lookup"><span data-stu-id="620e1-141">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="620e1-142">Der Pinsel in diesem Beispiel zeichnet einen Bereich mit einer vordefinierten voll Tonfarbe, schwarz.</span><span class="sxs-lookup"><span data-stu-id="620e1-142">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="620e1-143">Direct2D bietet auch andere Pinseltypen: Farbverlaufs Pinsel zum Zeichnen von linearen und radialen Farbverläufen, ein [**Bitmap-Pinsel**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zum Zeichnen mit Bitmaps und Mustern und ab Windows 8 ein [**Bild Pinsel**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) zum Zeichnen mit einem gerenderten Bild.</span><span class="sxs-lookup"><span data-stu-id="620e1-143">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, a [**bitmap brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) for painting with bitmaps and patterns, and starting in Windows 8, an [**image brush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) for painting with a rendered image.</span></span>

<span data-ttu-id="620e1-144">Einige Zeichnungs-APIs stellen Stifte zum Zeichnen von Gliederungen und Pinsel zum Auffüllen von Formen bereit.</span><span class="sxs-lookup"><span data-stu-id="620e1-144">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="620e1-145">Direct2D unterscheidet sich von einem Stift Objekt, es wird jedoch ein Pinsel zum Zeichnen von Gliederungen und Ausfüllen von Formen verwendet.</span><span class="sxs-lookup"><span data-stu-id="620e1-145">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="620e1-146">Verwenden Sie beim Zeichnen von Gliederungen die [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) -Schnittstelle oder beginnend mit Windows 8 die [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) -Schnittstelle mit einem Pinsel zum Steuern von Pfad Streifen Vorgängen.</span><span class="sxs-lookup"><span data-stu-id="620e1-146">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface, or starting in Windows 8 the [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) interface, with a brush to control path stroking operations.</span></span>

<span data-ttu-id="620e1-147">Ein Pinsel kann nur mit dem Renderziel, von dem es erstellt wurde, und mit anderen renderzielen in derselben Ressourcen Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="620e1-147">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="620e1-148">Im Allgemeinen sollten Sie Pinsel einmal erstellen und Sie für die Lebensdauer des Renderziels aufbewahren, von dem Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="620e1-148">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="620e1-149">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ist die einzige Ausnahme. Da es relativ preiswert ist, zu erstellen, können Sie jedes Mal, wenn Sie einen Frame zeichnen, ein **ID2D1SolidColorBrush** erstellen, ohne dass eine spürbare Leistungs Beeinträchtigung erzielt wird.</span><span class="sxs-lookup"><span data-stu-id="620e1-149">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="620e1-150">Sie können auch eine einzelne **ID2D1SolidColorBrush** verwenden und die Farbe oder Deckkraft jedes Mal ändern, wenn Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="620e1-150">You can also use a single **ID2D1SolidColorBrush** and just change its color or opacity every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="620e1-151">Schritt 5: Zeichnen des Rechtecks</span><span class="sxs-lookup"><span data-stu-id="620e1-151">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="620e1-152">Verwenden Sie als nächstes den Gerätekontext zum Zeichnen des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="620e1-152">Next, use the device context to draw the rectangle.</span></span>


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



<span data-ttu-id="620e1-153">Die [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode nimmt zwei Parameter an: das zu zeichnende Rechteck und den Pinsel, der zum Zeichnen der Kontur des Rechtecks verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="620e1-153">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="620e1-154">Optional können Sie auch die Optionen Stroke Width, Dash Pattern, Line Join und End Cap angeben.</span><span class="sxs-lookup"><span data-stu-id="620e1-154">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="620e1-155">Sie müssen die [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufrufen, bevor Sie Zeichenbefehle ausgeben, und Sie müssen die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode aufrufen, nachdem Sie das Ausgeben von Zeichnungs Befehlen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="620e1-155">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="620e1-156">Die **EndDraw** -Methode gibt ein **HRESULT** zurück, das angibt, ob die Zeichnungs Befehle erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="620e1-156">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span> <span data-ttu-id="620e1-157">Wenn dies nicht erfolgreich ist, löst die einschränkte Hilfsfunktion eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="620e1-157">If it is not successful, the ThrowIfFailed helper function will throw an exception.</span></span>

<span data-ttu-id="620e1-158">Die [**idxgiswapchain::P Resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) -Methode tauscht die Puffer Oberfläche mit der auf der Bildschirmoberfläche aus, um das Ergebnis anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="620e1-158">The [**IDXGISwapChain::Present**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) method swaps the buffer surface with the on screen surface to display the result.</span></span>

## <a name="example-code"></a><span data-ttu-id="620e1-159">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="620e1-159">Example code</span></span>

<span data-ttu-id="620e1-160">Der Code in diesem Thema zeigt die grundlegenden Elemente einer Direct2D-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="620e1-160">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="620e1-161">Aus Gründen der Kürze lässt das Thema das Anwendungs Framework und den Fehler Behandlungs Code aus, der für eine gut geschriebene Anwendung typisch ist.</span><span class="sxs-lookup"><span data-stu-id="620e1-161">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span>

 

 