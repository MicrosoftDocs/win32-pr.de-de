---
title: Direct2D-Schnellstart
description: Fasst die Schritte zusammen, die zum Zeichnen mit Direct2D erforderlich sind, und stellt Beispielcode bereit.
ms.assetid: 19d9ad76-b1e3-449f-8582-e00287b05874
keywords:
- Direct2D, Codebeispiel zum Zeichnen des Rechtecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa59d7da057a7a9922e270d83937307762b06a40
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101694"
---
# <a name="direct2d-quickstart"></a><span data-ttu-id="f485e-104">Direct2D-Schnellstart</span><span class="sxs-lookup"><span data-stu-id="f485e-104">Direct2D QuickStart</span></span>

<span data-ttu-id="f485e-105">Direct2D ist eine API im einheitlichen Code zum Erstellen von 2D-Grafiken.</span><span class="sxs-lookup"><span data-stu-id="f485e-105">Direct2D is a native-code, immediate-mode API for creating 2D graphics.</span></span> <span data-ttu-id="f485e-106">In diesem Thema wird veranschaulicht, wie Direct2D innerhalb einer typischen Win32-Anwendung verwendet wird, um ein **HWND** zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="f485e-106">This topic illustrates how to use Direct2D within a typical Win32 application to draw to an **HWND**.</span></span>

> [!Note]  
> <span data-ttu-id="f485e-107">Wenn Sie eine Windows Store-App erstellen möchten, die Direct2D verwendet, lesen Sie das Thema [Direct2D Quick Start for Windows 8](direct2d-quickstart-with-device-context.md) .</span><span class="sxs-lookup"><span data-stu-id="f485e-107">If you want to create a Windows Store app that uses Direct2D, see the [Direct2D Quickstart for Windows 8](direct2d-quickstart-with-device-context.md) topic.</span></span>

 

<span data-ttu-id="f485e-108">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="f485e-108">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="f485e-109">Zeichnen eines einfachen Rechtecks</span><span class="sxs-lookup"><span data-stu-id="f485e-109">Drawing a Simple Rectangle</span></span>](#drawing-a-simple-rectangle)
-   [<span data-ttu-id="f485e-110">Schritt 1: einschließen des Direct2D-Headers</span><span class="sxs-lookup"><span data-stu-id="f485e-110">Step 1: Include Direct2D Header</span></span>](#step-1-include-direct2d-header)
-   [<span data-ttu-id="f485e-111">Schritt 2: Erstellen eines ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="f485e-111">Step 2: Create an ID2D1Factory</span></span>](#step-2-create-an-id2d1factory)
-   [<span data-ttu-id="f485e-112">Schritt 3: Erstellen eines ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="f485e-112">Step 3: Create an ID2D1HwndRenderTarget</span></span>](#step-3-create-an-id2d1hwndrendertarget)
-   [<span data-ttu-id="f485e-113">Schritt 4: Erstellen eines Pinsels</span><span class="sxs-lookup"><span data-stu-id="f485e-113">Step 4: Create a Brush</span></span>](#step-4-create-a-brush)
-   [<span data-ttu-id="f485e-114">Schritt 5: Zeichnen des Rechtecks</span><span class="sxs-lookup"><span data-stu-id="f485e-114">Step 5: Draw the Rectangle</span></span>](#step-5-draw-the-rectangle)
-   [<span data-ttu-id="f485e-115">Schritt 6: Freigeben von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f485e-115">Step 6: Release Resources</span></span>](#step-6-release-resources)
-   [<span data-ttu-id="f485e-116">Erstellen einer einfachen Direct2D-Anwendung</span><span class="sxs-lookup"><span data-stu-id="f485e-116">Create a Simple Direct2D Application</span></span>](#create-a-simple-direct2d-application)
-   [<span data-ttu-id="f485e-117">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f485e-117">Related topics</span></span>](#related-topics)

## <a name="drawing-a-simple-rectangle"></a><span data-ttu-id="f485e-118">Zeichnen eines einfachen Rechtecks</span><span class="sxs-lookup"><span data-stu-id="f485e-118">Drawing a Simple Rectangle</span></span>

<span data-ttu-id="f485e-119">Wenn Sie ein Rechteck mithilfe von [GDI](/windows/desktop/gdi/windows-gdi)zeichnen möchten, können Sie die [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung wie im folgenden Code gezeigt verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="f485e-119">To draw a rectangle using [GDI](/windows/desktop/gdi/windows-gdi), you could handle the [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message, as shown in the following code.</span></span>


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



<span data-ttu-id="f485e-120">Der Code zum Zeichnen desselben Rechtecks mit Direct2D ist ähnlich: er erstellt Zeichnungs Ressourcen, beschreibt eine Form, die gezeichnet werden soll, zeichnet die Form und gibt dann die Zeichnungs Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="f485e-120">The code for drawing the same rectangle with Direct2D is similar: it creates drawing resources, describes a shape to draw, draws the shape, then releases the drawing resources.</span></span> <span data-ttu-id="f485e-121">In den folgenden Abschnitten werden die einzelnen Schritte ausführlich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f485e-121">The sections that follow describe each of these steps in detail.</span></span>

## <a name="step-1-include-direct2d-header"></a><span data-ttu-id="f485e-122">Schritt 1: einschließen des Direct2D-Headers</span><span class="sxs-lookup"><span data-stu-id="f485e-122">Step 1: Include Direct2D Header</span></span>

<span data-ttu-id="f485e-123">Fügen Sie zusätzlich zu den Headern, die für eine Win32-Anwendung erforderlich sind, den d2d1. h-Header ein.</span><span class="sxs-lookup"><span data-stu-id="f485e-123">In addition to the headers required for a Win32 application, include the d2d1.h header.</span></span>

## <a name="step-2-create-an-id2d1factory"></a><span data-ttu-id="f485e-124">Schritt 2: Erstellen eines ID2D1Factory</span><span class="sxs-lookup"><span data-stu-id="f485e-124">Step 2: Create an ID2D1Factory</span></span>

<span data-ttu-id="f485e-125">Eines der ersten Dinge, bei denen es sich bei allen Direct2D-Beispielen um das Erstellen eines [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)handelt.</span><span class="sxs-lookup"><span data-stu-id="f485e-125">One of the first things that any Direct2D example does is create an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).</span></span>


```C++
ID2D1Factory* pD2DFactory = NULL;
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_SINGLE_THREADED,
    &pD2DFactory
    );
```



<span data-ttu-id="f485e-126">Die [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle ist der Ausgangspunkt für die Verwendung von Direct2D. Verwenden Sie ein **ID2D1Factory** , um Direct2D-Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f485e-126">The [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) interface is the starting point for using Direct2D; use an **ID2D1Factory** to create Direct2D resources.</span></span>

<span data-ttu-id="f485e-127">Beim Erstellen einer Factory können Sie angeben, ob es sich um einen Multithread oder einen Single Thread handelt.</span><span class="sxs-lookup"><span data-stu-id="f485e-127">When you create a factory, you can specify whether it is multi- or single-threaded.</span></span> <span data-ttu-id="f485e-128">(Weitere Informationen zu Multithread-Factorys finden Sie in den Hinweisen auf der [**ID2D1Factory-Referenzseite**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) In diesem Beispiel wird eine Single Thread Factory erstellt.</span><span class="sxs-lookup"><span data-stu-id="f485e-128">(For more information about multi-threaded factories, see the remarks on the [**ID2D1Factory reference page**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) This example creates a single-threaded factory.</span></span>

<span data-ttu-id="f485e-129">Im Allgemeinen sollte die Anwendung die Factory einmal erstellen und für die Lebensdauer der Anwendung beibehalten.</span><span class="sxs-lookup"><span data-stu-id="f485e-129">In general, your application should create the factory once and retain it for the life of the application.</span></span>

## <a name="step-3-create-an-id2d1hwndrendertarget"></a><span data-ttu-id="f485e-130">Schritt 3: Erstellen eines ID2D1HwndRenderTarget</span><span class="sxs-lookup"><span data-stu-id="f485e-130">Step 3: Create an ID2D1HwndRenderTarget</span></span>

<span data-ttu-id="f485e-131">Nachdem Sie eine Factory erstellt haben, verwenden Sie Sie zum Erstellen eines Renderziels.</span><span class="sxs-lookup"><span data-stu-id="f485e-131">After you create a factory, use it to create a render target.</span></span>


```C++


// Obtain the size of the drawing area.
RECT rc;
GetClientRect(hwnd, &rc);

// Create a Direct2D render target          
ID2D1HwndRenderTarget* pRT = NULL;          
HRESULT hr = pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(
        hwnd,
        D2D1::SizeU(
            rc.right - rc.left,
            rc.bottom - rc.top)
    ),
    &pRT
);
```



<span data-ttu-id="f485e-132">Ein Renderziel ist ein Gerät, das Zeichnungsvorgänge ausführen und Geräte abhängige Zeichnungs Ressourcen erstellen kann, wie z. b. Pinsel.</span><span class="sxs-lookup"><span data-stu-id="f485e-132">A render target is a device that can perform drawing operations and create device-dependent drawing resources such as brushes.</span></span> <span data-ttu-id="f485e-133">Verschiedene Renderingziele werden auf unterschiedliche Geräte Renderingziele.</span><span class="sxs-lookup"><span data-stu-id="f485e-133">Different types of render targets render to different devices.</span></span> <span data-ttu-id="f485e-134">Im vorangehenden Beispiel wird ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)-Wert verwendet, der in einen Teil des Bildschirms gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="f485e-134">The preceding example uses an [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget), which renders to a portion of the screen.</span></span>

<span data-ttu-id="f485e-135">Wenn möglich verwendet ein Renderziel die GPU, um Renderingvorgänge zu beschleunigen und Zeichnungs Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f485e-135">When possible, a render target uses the GPU to accelerate rendering operations and create drawing resources.</span></span> <span data-ttu-id="f485e-136">Andernfalls verwendet das Renderziel die CPU, um Renderingerweiterungen zu verarbeiten und Ressourcen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f485e-136">Otherwise, the render target uses the CPU to process rendering instructions and create resources.</span></span> <span data-ttu-id="f485e-137">(Sie können dieses Verhalten ändern, indem Sie beim Erstellen des Renderziels die [**D2D1 \_ \_ \_ renderzieltyp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) -Flags verwenden.)</span><span class="sxs-lookup"><span data-stu-id="f485e-137">(You can modify this behavior by using the [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) flags when you create the render target.)</span></span>

<span data-ttu-id="f485e-138">Die Methode " [**kreatehwndrendertarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) " erfordert drei Parameter.</span><span class="sxs-lookup"><span data-stu-id="f485e-138">The [**CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method takes three parameters.</span></span> <span data-ttu-id="f485e-139">Der erste Parameter, eine Struktur des [**D2D1- \_ \_ Renderziel \_ Properties**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) , gibt Remote Anzeigeoptionen an, ob das Renderziel zum Renderingziel für Software oder Hardware und für den dpi-Wert erzwungen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f485e-139">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) struct, specifies remote display options, whether to force the render target to render to software or hardware, and the DPI.</span></span> <span data-ttu-id="f485e-140">Der Code in diesem Beispiel verwendet die Hilfsfunktion [**D2D1:: rendertargetproperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) , um die Standardeigenschaften des Renderziels zu akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="f485e-140">The code in this example uses the [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties) helper function to accept default render target properties.</span></span>

<span data-ttu-id="f485e-141">Der zweite Parameter, eine [**D2D1- \_ HWND- \_ \_ Renderziel \_ Eigenschafts**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) Struktur, gibt das **HWND** an, in dem der Inhalt gerendert wird, die anfängliche Größe des Renderziels (in Pixel) und die [**Darstellungs Optionen**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span><span class="sxs-lookup"><span data-stu-id="f485e-141">The second parameter, a [**D2D1\_HWND\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) struct, specifies the **HWND** to which content is rendered, the initial size of the render target (in pixels), and its [**presentation options**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_present_options).</span></span> <span data-ttu-id="f485e-142">In diesem Beispiel wird die Hilfsfunktion [**D2D1:: hwndrendertargetproperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) verwendet, um ein HWND und eine Anfangs Größe anzugeben.</span><span class="sxs-lookup"><span data-stu-id="f485e-142">This example uses the [**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties) helper function to specify an HWND and initial size.</span></span> <span data-ttu-id="f485e-143">Dabei werden Standard Darstellungs Optionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f485e-143">It uses default presentation options.</span></span>

<span data-ttu-id="f485e-144">Der dritte Parameter ist die Adresse des Zeigers, der den renderzielverweis empfängt.</span><span class="sxs-lookup"><span data-stu-id="f485e-144">The third parameter is the address of the pointer that receives the render target reference.</span></span>

<span data-ttu-id="f485e-145">Wenn Sie ein Renderziel erstellen und die Hardwarebeschleunigung verfügbar ist, weisen Sie der GPU des Computers Ressourcen zu.</span><span class="sxs-lookup"><span data-stu-id="f485e-145">When you create a render target and hardware acceleration is available, you allocate resources on the computer's GPU.</span></span> <span data-ttu-id="f485e-146">Wenn Sie ein Renderziel einmal erstellen und so lange wie möglich aufbewahren, profitieren Sie von Leistungsvorteilen.</span><span class="sxs-lookup"><span data-stu-id="f485e-146">By creating a render target once and retaining it as long as possible, you gain performance benefits.</span></span> <span data-ttu-id="f485e-147">Die Anwendung sollte einmal Renderziele erstellen und für die Lebensdauer der Anwendung oder bis zum D2DERR-Erstellungs [**\_ \_ Ziel**](direct2d-error-codes.md) Fehler erhalten.</span><span class="sxs-lookup"><span data-stu-id="f485e-147">Your application should create render targets once and hold on to them for the life of the application or until the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error is received.</span></span> <span data-ttu-id="f485e-148">Wenn Sie diesen Fehler erhalten, müssen Sie das Renderziel (und alle erstellten Ressourcen) neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f485e-148">When you receive this error, you need to recreate the render target (and any resources it created).</span></span>

## <a name="step-4-create-a-brush"></a><span data-ttu-id="f485e-149">Schritt 4: Erstellen eines Pinsels</span><span class="sxs-lookup"><span data-stu-id="f485e-149">Step 4: Create a Brush</span></span>

<span data-ttu-id="f485e-150">Wie eine Factory kann ein Renderziel Zeichnungs Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="f485e-150">Like a factory, a render target can create drawing resources.</span></span> <span data-ttu-id="f485e-151">In diesem Beispiel erstellt das Renderziel einen Pinsel.</span><span class="sxs-lookup"><span data-stu-id="f485e-151">In this example, the render target creates a brush.</span></span>


```C++
ID2D1SolidColorBrush* pBlackBrush = NULL;
if (SUCCEEDED(hr))
{
            
    pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        ); 
}
```



<span data-ttu-id="f485e-152">Ein Pinsel ist ein Objekt, das einen Bereich zeichnet, z. b. den Strich einer Form oder das Ausfüllen einer Geometrie.</span><span class="sxs-lookup"><span data-stu-id="f485e-152">A brush is an object that paints an area, such as the stroke of a shape or the fill of a geometry.</span></span> <span data-ttu-id="f485e-153">Der Pinsel in diesem Beispiel zeichnet einen Bereich mit einer vordefinierten voll Tonfarbe, schwarz.</span><span class="sxs-lookup"><span data-stu-id="f485e-153">The brush in this example paints an area with a predefined solid color, black.</span></span>

<span data-ttu-id="f485e-154">Direct2D bietet auch andere Pinseltypen: Farbverlaufs Pinsel zum Zeichnen von linearen und radialen Farbverläufen und einen bitmappinsel zum Zeichnen mit Bitmaps und Mustern.</span><span class="sxs-lookup"><span data-stu-id="f485e-154">Direct2D also provides other types of brushes: gradient brushes for painting linear and radial gradients, and a bitmap brush for painting with bitmaps and patterns.</span></span>

<span data-ttu-id="f485e-155">Einige Zeichnungs-APIs stellen Stifte zum Zeichnen von Gliederungen und Pinsel zum Auffüllen von Formen bereit.</span><span class="sxs-lookup"><span data-stu-id="f485e-155">Some drawing APIs provide pens for drawing outlines and brushes for filling shapes.</span></span> <span data-ttu-id="f485e-156">Direct2D unterscheidet sich von einem Stift Objekt, es wird jedoch ein Pinsel zum Zeichnen von Gliederungen und Ausfüllen von Formen verwendet.</span><span class="sxs-lookup"><span data-stu-id="f485e-156">Direct2D is different: it does not provide a pen object but uses a brush for drawing outlines and filling shapes.</span></span> <span data-ttu-id="f485e-157">Wenn Sie Gliederungen zeichnen, verwenden Sie die [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) -Schnittstelle mit einem Pinsel zum Steuern von Pfad-Übergängen.</span><span class="sxs-lookup"><span data-stu-id="f485e-157">When drawing outlines, use the [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) interface with a brush to control path stroking operations.</span></span>

<span data-ttu-id="f485e-158">Ein Pinsel kann nur mit dem Renderziel, von dem es erstellt wurde, und mit anderen renderzielen in derselben Ressourcen Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f485e-158">A brush can only be used with the render target that created it and with other render targets in the same resource domain.</span></span> <span data-ttu-id="f485e-159">Im Allgemeinen sollten Sie Pinsel einmal erstellen und Sie für die Lebensdauer des Renderziels aufbewahren, von dem Sie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f485e-159">In general, you should create brushes once and retain them for the life of the render target that created them.</span></span> <span data-ttu-id="f485e-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ist die einzige Ausnahme. Da es relativ preiswert ist, zu erstellen, können Sie jedes Mal, wenn Sie einen Frame zeichnen, ein **ID2D1SolidColorBrush** erstellen, ohne dass eine spürbare Leistungs Beeinträchtigung erzielt wird.</span><span class="sxs-lookup"><span data-stu-id="f485e-160">[**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is the lone exception; because it is relatively inexpensive to create, you can create a **ID2D1SolidColorBrush** every time you draw a frame, without any noticeable performance hit.</span></span> <span data-ttu-id="f485e-161">Sie können auch eine einzelne **ID2D1SolidColorBrush** verwenden und die Farbe jedes Mal ändern, wenn Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="f485e-161">You can also use a single **ID2D1SolidColorBrush** and just change its color every time you use it.</span></span>

## <a name="step-5-draw-the-rectangle"></a><span data-ttu-id="f485e-162">Schritt 5: Zeichnen des Rechtecks</span><span class="sxs-lookup"><span data-stu-id="f485e-162">Step 5: Draw the Rectangle</span></span>

<span data-ttu-id="f485e-163">Verwenden Sie als nächstes das Renderziel zum Zeichnen des Rechtecks.</span><span class="sxs-lookup"><span data-stu-id="f485e-163">Next, use the render target to draw the rectangle.</span></span>


```C++
 
pRT->BeginDraw();

pRT->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

HRESULT hr = pRT->EndDraw();  
```



<span data-ttu-id="f485e-164">Die [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode nimmt zwei Parameter an: das zu zeichnende Rechteck und den Pinsel, der zum Zeichnen der Kontur des Rechtecks verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f485e-164">The [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) method takes two parameters: the rectangle to be drawn, and the brush to be used to paint the rectangle's outline.</span></span> <span data-ttu-id="f485e-165">Optional können Sie auch die Optionen Stroke Width, Dash Pattern, Line Join und End Cap angeben.</span><span class="sxs-lookup"><span data-stu-id="f485e-165">Optionally, you can also specify the stroke width, dash pattern, line join, and end cap options.</span></span>

<span data-ttu-id="f485e-166">Sie müssen die [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufrufen, bevor Sie Zeichenbefehle ausgeben, und Sie müssen die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode aufrufen, nachdem Sie das Ausgeben von Zeichnungs Befehlen abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="f485e-166">You must call the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method before issuing any drawing commands, and you must call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method after you've finished issuing drawing commands.</span></span> <span data-ttu-id="f485e-167">Die **EndDraw** -Methode gibt ein **HRESULT** zurück, das angibt, ob die Zeichnungs Befehle erfolgreich waren.</span><span class="sxs-lookup"><span data-stu-id="f485e-167">The **EndDraw** method returns an **HRESULT** that indicates whether the drawing commands were successful.</span></span>

## <a name="step-6-release-resources"></a><span data-ttu-id="f485e-168">Schritt 6: Freigeben von Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f485e-168">Step 6: Release Resources</span></span>

<span data-ttu-id="f485e-169">Wenn keine weiteren Frames zum Zeichnen vorhanden sind oder wenn Sie den Fehler " [**D2DERR neu \_ Erstellen \_**](direct2d-error-codes.md) " erhalten, geben Sie das Renderziel und alle von ihm erstellten Geräte frei.</span><span class="sxs-lookup"><span data-stu-id="f485e-169">When there are no more frames to draw, or when you receive the [**D2DERR\_RECREATE\_TARGET**](direct2d-error-codes.md) error, release the render target and any devices it created.</span></span>


```C++
 
SafeRelease(pRT);
SafeRelease(pBlackBrush);
```



<span data-ttu-id="f485e-170">Wenn Ihre Anwendung die Verwendung von Direct2D-Ressourcen abgeschlossen hat (z. b. beim Beenden), müssen Sie die Direct2D-Factory freigeben.</span><span class="sxs-lookup"><span data-stu-id="f485e-170">When your application has finished using Direct2D resources (such as when it is about to exit), release the Direct2D factory.</span></span>


```C++
 
SafeRelease(pD2DFactory);
```



## <a name="create-a-simple-direct2d-application"></a><span data-ttu-id="f485e-171">Erstellen einer einfachen Direct2D-Anwendung</span><span class="sxs-lookup"><span data-stu-id="f485e-171">Create a Simple Direct2D Application</span></span>

<span data-ttu-id="f485e-172">Der Code in diesem Thema zeigt die grundlegenden Elemente einer Direct2D-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="f485e-172">The code in this topic shows the basic elements of a Direct2D application.</span></span> <span data-ttu-id="f485e-173">Aus Gründen der Kürze lässt das Thema das Anwendungs Framework und den Fehler Behandlungs Code aus, der für eine gut geschriebene Anwendung typisch ist.</span><span class="sxs-lookup"><span data-stu-id="f485e-173">For brevity, the topic omits the application framework and error handling code that is characteristic of a well-written application.</span></span> <span data-ttu-id="f485e-174">Eine ausführlichere Exemplarische Vorgehensweise, in der der gesamte Code zum Erstellen einer einfachen Direct2D-Anwendung und bewährte Entwurfsmethoden veranschaulicht wird, finden Sie unter [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="f485e-174">For a more detailed walk-through that shows the complete code for creating a simple Direct2D application and demonstrates best design practices, see [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f485e-175">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f485e-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f485e-176">Erstellen einer einfachen Direct2D-Anwendung</span><span class="sxs-lookup"><span data-stu-id="f485e-176">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> </dl>

 

 