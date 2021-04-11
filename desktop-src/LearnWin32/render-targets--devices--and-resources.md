---
title: Renderziele, Geräte und Ressourcen
description: Renderziele, Geräte und Ressourcen
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314930"
---
# <a name="render-targets-devices-and-resources"></a><span data-ttu-id="43df5-103">Renderziele, Geräte und Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43df5-103">Render Targets, Devices, and Resources</span></span>

<span data-ttu-id="43df5-104">Ein *Renderziel* ist einfach der Speicherort, an dem das Programm gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="43df5-104">A *render target* is simply the location where your program will draw.</span></span> <span data-ttu-id="43df5-105">In der Regel ist das Renderziel ein Fenster (insbesondere der Client Bereich des Fensters).</span><span class="sxs-lookup"><span data-stu-id="43df5-105">Typically, the render target is a window (specifically, the client area of the window).</span></span> <span data-ttu-id="43df5-106">Es kann sich auch um eine Bitmap im Arbeitsspeicher handeln, die nicht angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="43df5-106">It could also be a bitmap in memory that is not displayed.</span></span> <span data-ttu-id="43df5-107">Ein Renderziel wird durch die [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="43df5-107">A render target is represented by the [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span>

<span data-ttu-id="43df5-108">Ein *Gerät* ist eine Abstraktion, die darstellt, was die Pixel tatsächlich zeichnet.</span><span class="sxs-lookup"><span data-stu-id="43df5-108">A *device* is an abstraction that represents whatever actually draws the pixels.</span></span> <span data-ttu-id="43df5-109">Ein Hardware Gerät verwendet die GPU, um die Leistung zu beschleunigen, während ein Software Gerät die CPU verwendet.</span><span class="sxs-lookup"><span data-stu-id="43df5-109">A hardware device uses the GPU for faster performance, whereas a software device uses the CPU.</span></span> <span data-ttu-id="43df5-110">Das Gerät wird von der Anwendung nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="43df5-110">The application does not create the device.</span></span> <span data-ttu-id="43df5-111">Stattdessen wird das Gerät implizit erstellt, wenn die Anwendung das Renderziel erstellt.</span><span class="sxs-lookup"><span data-stu-id="43df5-111">Instead, the device is created implicitly when the application creates the render target.</span></span> <span data-ttu-id="43df5-112">Jedes Renderziel ist einem bestimmten Gerät zugeordnet, entweder Hardware oder Software.</span><span class="sxs-lookup"><span data-stu-id="43df5-112">Each render target is associated with a particular device, either hardware or software.</span></span>

![ein Diagramm, das die Beziehung zwischen einem Renderziel und einem Gerät anzeigt.](images/graphics09.png)

<span data-ttu-id="43df5-114">Eine *Ressource* ist ein Objekt, das das Programm zum Zeichnen verwendet.</span><span class="sxs-lookup"><span data-stu-id="43df5-114">A *resource* is an object that the program uses for drawing.</span></span> <span data-ttu-id="43df5-115">Im folgenden finden Sie einige Beispiele für Ressourcen, die in Direct2D definiert sind:</span><span class="sxs-lookup"><span data-stu-id="43df5-115">Here are some examples of resources that are defined in Direct2D:</span></span>

-   <span data-ttu-id="43df5-116">**Pinsel**.</span><span class="sxs-lookup"><span data-stu-id="43df5-116">**Brush**.</span></span> <span data-ttu-id="43df5-117">Steuert, wie Linien und Bereiche gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="43df5-117">Controls how lines and regions are painted.</span></span> <span data-ttu-id="43df5-118">Pinseltypen enthalten Pinsel mit voll Tonfarbe und Farbverlaufs Pinsel.</span><span class="sxs-lookup"><span data-stu-id="43df5-118">Brush types include solid-color brushes and gradient brushes.</span></span>
-   <span data-ttu-id="43df5-119">**Strich Stil**.</span><span class="sxs-lookup"><span data-stu-id="43df5-119">**Stroke style**.</span></span> <span data-ttu-id="43df5-120">Steuert das Aussehen einer Linie – z. b. gestrichelt oder Solid.</span><span class="sxs-lookup"><span data-stu-id="43df5-120">Controls the appearance of a line—for example, dashed or solid.</span></span>
-   <span data-ttu-id="43df5-121">**Geometrie**.</span><span class="sxs-lookup"><span data-stu-id="43df5-121">**Geometry**.</span></span> <span data-ttu-id="43df5-122">Stellt eine Auflistung von Linien und Kurven dar.</span><span class="sxs-lookup"><span data-stu-id="43df5-122">Represents a collection of lines and curves.</span></span>
-   <span data-ttu-id="43df5-123">**Mesh**.</span><span class="sxs-lookup"><span data-stu-id="43df5-123">**Mesh**.</span></span> <span data-ttu-id="43df5-124">Eine Form, die aus Dreiecken gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="43df5-124">A shape formed out of triangles.</span></span> <span data-ttu-id="43df5-125">Mesh-Daten können direkt von der GPU genutzt werden, im Gegensatz zu Geometry-Daten, die vor dem Rendering konvertiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="43df5-125">Mesh data can be consumed directly by the GPU, unlike geometry data, which must be converted before rendering.</span></span>

<span data-ttu-id="43df5-126">Renderziele werden auch als Ressourcentyp betrachtet.</span><span class="sxs-lookup"><span data-stu-id="43df5-126">Render targets are also considered a type of resource.</span></span>

<span data-ttu-id="43df5-127">Einige Ressourcen profitieren von der Hardwarebeschleunigung.</span><span class="sxs-lookup"><span data-stu-id="43df5-127">Some resources benefit from hardware acceleration.</span></span> <span data-ttu-id="43df5-128">Eine Ressource dieses Typs ist immer einem bestimmten Gerät zugeordnet, entweder Hardware (GPU) oder Software (CPU).</span><span class="sxs-lookup"><span data-stu-id="43df5-128">A resource of this type is always associated with a particular device, either hardware (GPU) or software (CPU).</span></span> <span data-ttu-id="43df5-129">Dieser Ressourcentyp wird als *Geräte abhängig* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="43df5-129">This type of resource is called *device-dependent*.</span></span> <span data-ttu-id="43df5-130">Pinsel und Netzen sind Beispiele für Geräte abhängige Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="43df5-130">Brushes and meshes are examples of device-dependent resources.</span></span> <span data-ttu-id="43df5-131">Wenn das Gerät nicht mehr verfügbar ist, muss die Ressource für ein neues Gerät neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="43df5-131">If the device becomes unavailable, the resource must be re-created for a new device.</span></span>

<span data-ttu-id="43df5-132">Andere Ressourcen werden im CPU-Speicher beibehalten, unabhängig davon, welches Gerät verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43df5-132">Other resources are kept in CPU memory, regardless of what device is used.</span></span> <span data-ttu-id="43df5-133">Diese Ressourcen sind *Geräte unabhängig*, da Sie nicht mit einem bestimmten Gerät verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="43df5-133">These resources are *device-independent*, because they are not associated with a particular device.</span></span> <span data-ttu-id="43df5-134">Geräteunabhängige Ressourcen müssen nicht neu erstellt werden, wenn das Gerät geändert wird.</span><span class="sxs-lookup"><span data-stu-id="43df5-134">It is not necessary to re-create device-independent resources when the device changes.</span></span> <span data-ttu-id="43df5-135">Strich Stile und Geometrien sind geräteunabhängige Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="43df5-135">Stroke styles and geometries are device-independent resources.</span></span>

<span data-ttu-id="43df5-136">In der MSDN-Dokumentation für jede Ressource wird angegeben, ob die Ressource Geräte abhängig oder Geräte unabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="43df5-136">The MSDN documentation for each resource states whether the resource is device-dependent or device-independent.</span></span> <span data-ttu-id="43df5-137">Jeder Ressourcentyp wird durch eine Schnittstelle dargestellt, die von [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource)abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="43df5-137">Every resource type is represented by an interface that derives from [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span></span> <span data-ttu-id="43df5-138">Pinsel werden z. b. durch die [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) -Schnittstelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="43df5-138">For example, brushes are represented by the [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) interface.</span></span>

## <a name="the-direct2d-factory-object"></a><span data-ttu-id="43df5-139">Das Direct2D Factory-Objekt</span><span class="sxs-lookup"><span data-stu-id="43df5-139">The Direct2D Factory Object</span></span>

<span data-ttu-id="43df5-140">Der erste Schritt bei der Verwendung von Direct2D besteht darin, eine Instanz des Direct2D Factory-Objekts zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="43df5-140">The first step when using Direct2D is to create an instance of the Direct2D factory object.</span></span> <span data-ttu-id="43df5-141">Bei der Computerprogrammierung ist eine *Factory* ein Objekt, mit dem andere Objekte erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="43df5-141">In computer programming, a *factory* is an object that creates other objects.</span></span> <span data-ttu-id="43df5-142">Die Direct2D-Factory erstellt die folgenden Objekttypen:</span><span class="sxs-lookup"><span data-stu-id="43df5-142">The Direct2D factory creates the following types of objects:</span></span>

-   <span data-ttu-id="43df5-143">Renderziele.</span><span class="sxs-lookup"><span data-stu-id="43df5-143">Render targets.</span></span>
-   <span data-ttu-id="43df5-144">Geräteunabhängige Ressourcen, z. b. Strich Stile und Geometrien.</span><span class="sxs-lookup"><span data-stu-id="43df5-144">Device-independent resources, such as stroke styles and geometries.</span></span>

<span data-ttu-id="43df5-145">Geräte abhängige Ressourcen, z. b. Pinsel und Bitmaps, werden vom renderzielobjekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="43df5-145">Device-dependent resources, such as brushes and bitmaps, are created by the render target object.</span></span>

![ein Diagramm, das die Direct2D-Factory anzeigt.](images/graphics10.png)

<span data-ttu-id="43df5-147">Um das Direct2D Factory-Objekt zu erstellen, rufen Sie die [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="43df5-147">To create the Direct2D factory object, call the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



<span data-ttu-id="43df5-148">Der erste Parameter ist ein Flag, das Erstellungs Optionen angibt.</span><span class="sxs-lookup"><span data-stu-id="43df5-148">The first parameter is a flag that specifies creation options.</span></span> <span data-ttu-id="43df5-149">Das Flag " **D2D1 \_ Factory \_ Type \_ Single \_ threaded** " bedeutet, dass Sie Direct2D nicht aus mehreren Threads abrufen.</span><span class="sxs-lookup"><span data-stu-id="43df5-149">The **D2D1\_FACTORY\_TYPE\_SINGLE\_THREADED** flag means that you will not call Direct2D from multiple threads.</span></span> <span data-ttu-id="43df5-150">Zum unterstützen von Aufrufen aus mehreren Threads geben Sie den **D2D1 \_ Factory- \_ Typ \_ \_ Multithread** an.</span><span class="sxs-lookup"><span data-stu-id="43df5-150">To support calls from multiple threads, specify **D2D1\_FACTORY\_TYPE\_MULTI\_THREADED**.</span></span> <span data-ttu-id="43df5-151">Wenn das Programm einen einzelnen Thread verwendet, um Direct2D aufzurufen, ist die Single Thread-Option effizienter.</span><span class="sxs-lookup"><span data-stu-id="43df5-151">If your program uses a single thread to call into Direct2D, the single-threaded option is more efficient.</span></span>

<span data-ttu-id="43df5-152">Der zweite Parameter für die [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) -Funktion empfängt einen Zeiger auf die [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="43df5-152">The second parameter to the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function receives a pointer to the [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) interface.</span></span>

<span data-ttu-id="43df5-153">Vor der ersten WM-Zeichnungs Nachricht sollten Sie das [**Direct2D \_**](/windows/desktop/gdi/wm-paint) Factory-Objekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="43df5-153">You should create the Direct2D factory object before the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="43df5-154">Der [**WM \_ Create**](/windows/desktop/winmsg/wm-create) Message-Handler ist ein guter Ort zum Erstellen der Factory:</span><span class="sxs-lookup"><span data-stu-id="43df5-154">The [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message handler is a good place to create the factory:</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a><span data-ttu-id="43df5-155">Erstellen von Direct2D-Ressourcen</span><span class="sxs-lookup"><span data-stu-id="43df5-155">Creating Direct2D Resources</span></span>

<span data-ttu-id="43df5-156">Das Circle-Programm verwendet die folgenden geräteabhängigen Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="43df5-156">The Circle program uses the following device-dependent resources:</span></span>

-   <span data-ttu-id="43df5-157">Ein Renderziel, das dem Anwendungsfenster zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="43df5-157">A render target that is associated with the application window.</span></span>
-   <span data-ttu-id="43df5-158">Ein vollfarbiger Pinsel zum Zeichnen des Kreises.</span><span class="sxs-lookup"><span data-stu-id="43df5-158">A solid-color brush to paint the circle.</span></span>

<span data-ttu-id="43df5-159">Jede dieser Ressourcen wird durch eine COM-Schnittstelle dargestellt:</span><span class="sxs-lookup"><span data-stu-id="43df5-159">Each of these resources is represented by a COM interface:</span></span>

-   <span data-ttu-id="43df5-160">Die [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Schnittstelle stellt das Renderziel dar.</span><span class="sxs-lookup"><span data-stu-id="43df5-160">The [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) interface represents the render target.</span></span>
-   <span data-ttu-id="43df5-161">Die [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Schnittstelle stellt den Pinsel dar.</span><span class="sxs-lookup"><span data-stu-id="43df5-161">The [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interface represents the brush.</span></span>

<span data-ttu-id="43df5-162">Das Circle-Programm speichert Zeiger auf diese Schnittstellen als Element Variablen der- `MainWindow` Klasse:</span><span class="sxs-lookup"><span data-stu-id="43df5-162">The Circle program stores pointers to these interfaces as member variables of the `MainWindow` class:</span></span>


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



<span data-ttu-id="43df5-163">Der folgende Code erstellt diese beiden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="43df5-163">The following code creates these two resources.</span></span>


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



<span data-ttu-id="43df5-164">Um ein Renderziel für ein Fenster zu erstellen, rufen Sie die [**ID2D1Factory:: | atehwndrendertarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) -Methode für die Direct2D-Factory auf.</span><span class="sxs-lookup"><span data-stu-id="43df5-164">To create a render target for a window, call the [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method on the Direct2D factory.</span></span>

-   <span data-ttu-id="43df5-165">Der erste Parameter gibt Optionen an, die für jeden renderzieltyp gelten.</span><span class="sxs-lookup"><span data-stu-id="43df5-165">The first parameter specifies options that are common to any type of render target.</span></span> <span data-ttu-id="43df5-166">Hier werden Standardoptionen durch Aufrufen der Hilfsfunktion [**D2D1:: rendertargetproperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties)übergeben.</span><span class="sxs-lookup"><span data-stu-id="43df5-166">Here, we pass in default options by calling the helper function [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span></span>
-   <span data-ttu-id="43df5-167">Der zweite Parameter gibt das Handle für das Fenster plus die Größe des Renderziels in Pixel an.</span><span class="sxs-lookup"><span data-stu-id="43df5-167">The second parameter specifies the handle to the window plus the size of the render target, in pixels.</span></span>
-   <span data-ttu-id="43df5-168">Der dritte Parameter empfängt einen [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="43df5-168">The third parameter receives an [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pointer.</span></span>

<span data-ttu-id="43df5-169">Um den Pinsel mit voll Tonfarbe zu erstellen, rufen Sie die [**ID2D1RenderTarget:: froatesolidcolorbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) -Methode für das Renderziel auf.</span><span class="sxs-lookup"><span data-stu-id="43df5-169">To create the solid-color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method on the render target.</span></span> <span data-ttu-id="43df5-170">Die Farbe wird als [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) -Wert angegeben.</span><span class="sxs-lookup"><span data-stu-id="43df5-170">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) value.</span></span> <span data-ttu-id="43df5-171">Weitere Informationen zu Farben in Direct2D finden Sie unter [Verwenden von Color in Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="43df5-171">For more information about colors in Direct2D, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>

<span data-ttu-id="43df5-172">Beachten Sie auch Folgendes: Wenn das Renderziel bereits vorhanden ist, `CreateGraphicsResources` gibt die Methode **S \_ OK** zurück, ohne etwas zu tun.</span><span class="sxs-lookup"><span data-stu-id="43df5-172">Also, notice that if the render target already exists, the `CreateGraphicsResources` method returns **S\_OK** without doing anything.</span></span> <span data-ttu-id="43df5-173">Der Grund für diesen Entwurf wird im nächsten Thema deutlich.</span><span class="sxs-lookup"><span data-stu-id="43df5-173">The reason for this design will become clear in the next topic.</span></span>

## <a name="next"></a><span data-ttu-id="43df5-174">Nächste</span><span class="sxs-lookup"><span data-stu-id="43df5-174">Next</span></span>

[<span data-ttu-id="43df5-175">Zeichnen mit Direct2D</span><span class="sxs-lookup"><span data-stu-id="43df5-175">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)

 

 