---
title: Übersicht über die Direct2D-und GDI-Interoperabilität
description: Beschreibt die gemeinsame Verwendung von Direct2D und GDI.
ms.assetid: 182df2dc-2574-4d8f-a7e1-30d70da1740a
keywords:
- Direct2D, GDI-Interoperation
- Direct2D, Interoperabilität
- Interoperabilität, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- Interoperabilität, Graphics Device Interface (GDI)
- Direct3D, Interoperabilität
- Direct3D, Direct2D Interoperation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 991d94b4460e9130b3353be38d5f749511434eb6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729664"
---
# <a name="direct2d-and-gdi-interoperability-overview"></a><span data-ttu-id="e0465-111">Übersicht über die Direct2D-und GDI-Interoperabilität</span><span class="sxs-lookup"><span data-stu-id="e0465-111">Direct2D and GDI Interoperability Overview</span></span>

<span data-ttu-id="e0465-112">In diesem Thema wird die gemeinsame Verwendung von Direct2D und [GDI](/windows/desktop/gdi/windows-gdi) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e0465-112">This topic describes how to use Direct2D and [GDI](/windows/desktop/gdi/windows-gdi) together.</span></span> <span data-ttu-id="e0465-113">Es gibt zwei Möglichkeiten, Direct2D mit GDI zu kombinieren: Sie können GDI-Inhalte in ein Direct2D GDI-kompatibles Renderziel schreiben, oder Sie können Direct2D-Inhalte in einen [GDI-Gerätekontext (DC)](/windows/desktop/gdi/device-contexts)schreiben.</span><span class="sxs-lookup"><span data-stu-id="e0465-113">There are two ways to combine Direct2D with GDI: you can write GDI content to a Direct2D GDI-compatible render target, or you can write Direct2D content to a [GDI Device Context (DC)](/windows/desktop/gdi/device-contexts).</span></span>

<span data-ttu-id="e0465-114">Dieses Thema enthält folgende Abschnitte:</span><span class="sxs-lookup"><span data-stu-id="e0465-114">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="e0465-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="e0465-115">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="e0465-116">Zeichnen von Direct2D-Inhalt in einen GDI-Gerätekontext</span><span class="sxs-lookup"><span data-stu-id="e0465-116">Draw Direct2D Content to a GDI Device Context</span></span>](#draw-direct2d-content-to-a-gdi-device-context)
-   [<span data-ttu-id="e0465-117">ID2D1DCRenderTargets, GDI-Transformationen und von rechts nach links geschriebene sprach Builds von Windows</span><span class="sxs-lookup"><span data-stu-id="e0465-117">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>](#id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows)
-   [<span data-ttu-id="e0465-118">Ziehen Sie GDI-Inhalte in ein Direct2D-GDI-Compatible Renderziel.</span><span class="sxs-lookup"><span data-stu-id="e0465-118">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>](#draw-gdi-content-to-a-direct2d-gdi-compatible-render-target)
-   [<span data-ttu-id="e0465-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0465-119">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="e0465-120">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="e0465-120">Prerequisites</span></span>

<span data-ttu-id="e0465-121">Diese Übersicht setzt voraus, dass Sie mit grundlegenden Direct2D-Zeichnungs Vorgängen vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="e0465-121">This overview assumes that you are familiar with basic Direct2D drawing operations.</span></span> <span data-ttu-id="e0465-122">Ein Tutorial finden Sie unter [Direct2D Quick Start](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="e0465-122">For a tutorial, see the [Direct2D QuickStart](direct2d-quickstart.md).</span></span> <span data-ttu-id="e0465-123">Außerdem wird davon ausgegangen, dass Sie mit GDI-Zeichnungs Vorgängen vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="e0465-123">It also assumes that you are familiar with GDI drawing operations.</span></span>

## <a name="draw-direct2d-content-to-a-gdi-device-context"></a><span data-ttu-id="e0465-124">Zeichnen von Direct2D-Inhalt in einen GDI-Gerätekontext</span><span class="sxs-lookup"><span data-stu-id="e0465-124">Draw Direct2D Content to a GDI Device Context</span></span>

<span data-ttu-id="e0465-125">Um Direct2D-Inhalte zu einem GDI-DC zu zeichnen, verwenden Sie ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e0465-125">To draw Direct2D content to a GDI DC, you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span> <span data-ttu-id="e0465-126">Wenn Sie ein DC-Renderziel erstellen möchten, verwenden Sie die [**ID2D1Factory::**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e0465-126">To create a DC render target, you use the [**ID2D1Factory::CreateDCRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget) method.</span></span> <span data-ttu-id="e0465-127">Diese Methode nimmt zwei Parameter an.</span><span class="sxs-lookup"><span data-stu-id="e0465-127">This method takes two parameters.</span></span>

<span data-ttu-id="e0465-128">Der erste Parameter, eine [**D2D1 \_ - \_ Renderziel- \_ Eigenschafts**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Struktur, gibt Rendering-, Remoting-, dpi-, Pixel-und Verwendungs Informationen an.</span><span class="sxs-lookup"><span data-stu-id="e0465-128">The first parameter, a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) structure, specifies rendering, remoting, DPI, pixel format, and usage information.</span></span> <span data-ttu-id="e0465-129">Um das DC-Renderziel für die Zusammenarbeit mit GDI zu aktivieren, legen Sie das DXGI-Format auf [DXGI- \_ Format \_ B8G8R8A8 \_ unorm](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) und den Alpha-Modus auf [**D2D1 \_ alpha \_ Modus \_ vorab multipliziert**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) bzw. **D2D1 \_ alpha \_ Mode \_ Ignore** fest.</span><span class="sxs-lookup"><span data-stu-id="e0465-129">To enable the DC render target to work with GDI, set the DXGI format to [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) and the alpha mode to [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="e0465-130">Der zweite Parameter ist die Adresse des Zeigers, der den DC-renderzielverweis empfängt.</span><span class="sxs-lookup"><span data-stu-id="e0465-130">The second parameter is the address of the pointer that receive the DC render target reference.</span></span>

<span data-ttu-id="e0465-131">Der folgende Code erstellt ein DC-Renderziel.</span><span class="sxs-lookup"><span data-stu-id="e0465-131">The following code creates a DC render target.</span></span>


```C++
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);
```



<span data-ttu-id="e0465-132">Im vorangehenden Code ist *m \_ pD2DFactory* ein Zeiger auf [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), und *m \_ pdcrt* ist ein Zeiger auf ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span><span class="sxs-lookup"><span data-stu-id="e0465-132">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pDCRT* is a pointer to an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget).</span></span>

<span data-ttu-id="e0465-133">Bevor Sie das Rendering mit dem DC-Renderziel durchführen können, müssen Sie die [**binddc**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) -Methode verwenden, um Sie einem GDI-DC zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="e0465-133">Before you can render with the DC render target, you must use its [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method to associate it with a GDI DC.</span></span> <span data-ttu-id="e0465-134">Dies geschieht jedes Mal, wenn Sie einen anderen Domänen Controller verwenden oder die Größe des Bereichs, den Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="e0465-134">You do this each time you use a different DC, or the size of the area you want to draw to changes.</span></span>

<span data-ttu-id="e0465-135">Die [**binddc**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) -Methode erfordert zwei Parameter: *hdc* und *psubrect*.</span><span class="sxs-lookup"><span data-stu-id="e0465-135">The [**BindDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc) method takes two parameters, *hDC* and *pSubRect*.</span></span> <span data-ttu-id="e0465-136">Der *hdc* -Parameter stellt ein Handle für den Gerätekontext bereit, der die Ausgabe des Renderziels empfängt.</span><span class="sxs-lookup"><span data-stu-id="e0465-136">The *hDC* parameter provides a handle to the device context that receives the output of the render target.</span></span> <span data-ttu-id="e0465-137">Der *psubrect* -Parameter ist ein Rechteck, das den Teil des Geräte Kontexts beschreibt, in dem der Inhalt gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="e0465-137">The *pSubRect* parameter is a rectangle that describes the portion of the device context to which content is rendered.</span></span> <span data-ttu-id="e0465-138">Das DC-Renderziel aktualisiert seine Größe entsprechend dem von *psubrect* beschriebenen Gerätekontext Bereich, wenn die Größe geändert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0465-138">The DC render target updates its size to match the device context area described by *pSubRect*, should it change size.</span></span>

<span data-ttu-id="e0465-139">Mit dem folgenden Code wird ein DC an ein DC-Renderziel gebunden.</span><span class="sxs-lookup"><span data-stu-id="e0465-139">The following code binds a DC to a DC render target.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{


// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0465-140">C++</span><span class="sxs-lookup"><span data-stu-id="e0465-140">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="e0465-141">Nachdem Sie das DC-Renderziel mit einem DC verknüpft haben, können Sie es zum Zeichnen verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0465-141">After you associate the DC render target with a DC, you can use it to draw.</span></span> <span data-ttu-id="e0465-142">Der folgende Code zeichnet Direct2D-und GDI-Inhalte mithilfe eines DC.</span><span class="sxs-lookup"><span data-stu-id="e0465-142">The following code draws Direct2D and GDI content using a DC.</span></span>


```C++
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

    HRESULT hr;
    RECT rc;

    // Get the dimensions of the client drawing area.
    GetClientRect(m_hwnd, &rc);

    //
    // Draw the pie chart with Direct2D.
    //

    // Create the DC render target.
    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Bind the DC to the DC render target.
        hr = m_pDCRT->BindDC(ps.hdc, &rc);

        m_pDCRT->BeginDraw();

        m_pDCRT->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pDCRT->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pDCRT->DrawEllipse(
            D2D1::Ellipse(
                D2D1::Point2F(150.0f, 150.0f),
                100.0f,
                100.0f),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.15425f),
                (150.0f - 100.0f * 0.988f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f + 100.0f * 0.525f),
                (150.0f + 100.0f * 0.8509f)),
            m_pBlackBrush,
            3.0
            );

        m_pDCRT->DrawLine(
            D2D1::Point2F(150.0f, 150.0f),
            D2D1::Point2F(
                (150.0f - 100.0f * 0.988f),
                (150.0f - 100.0f * 0.15425f)),
            m_pBlackBrush,
            3.0
            );

        hr = m_pDCRT->EndDraw();
        if (SUCCEEDED(hr))
        {
            //
            // Draw the pie chart with GDI.
            //

            // Save the original object.
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(ps.hdc, blackPen);

            Ellipse(ps.hdc, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);


            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(ps.hdc, pntArray1, 2);
            Polyline(ps.hdc, pntArray2, 2);
            Polyline(ps.hdc, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(ps.hdc, original);
        }
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



<span data-ttu-id="e0465-143">Mit diesem Code werden Ausgaben erzeugt, wie in der folgenden Abbildung gezeigt (es wurden Legenden aufgerufen, um den Unterschied zwischen dem Direct2D-und dem GDI-Rendering hervorzuheben).</span><span class="sxs-lookup"><span data-stu-id="e0465-143">This code produces outputs as shown in the following illustration (callouts have been added to highlight the difference between Direct2D and GDI rendering.)</span></span>

![Abbildung von zwei Kreis Diagrammen, die mit Direct2D und GDI gerendert werden](images/gdiinteropcallout.png)

## <a name="id2d1dcrendertargets-gdi-transforms-and-right-to-left-language-builds-of-windows"></a><span data-ttu-id="e0465-145">ID2D1DCRenderTargets, GDI-Transformationen und von rechts nach links geschriebene sprach Builds von Windows</span><span class="sxs-lookup"><span data-stu-id="e0465-145">ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</span></span>

<span data-ttu-id="e0465-146">Wenn Sie ein [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)-Objekt verwenden, wird Direct2D-Inhalt in eine interne Bitmap gerendert, und anschließend wird die Bitmap mit GDI auf dem DC gerendert.</span><span class="sxs-lookup"><span data-stu-id="e0465-146">When you use an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget), it renders Direct2D content to an internal bitmap, and then renders the bitmap to the DC with GDI.</span></span>

<span data-ttu-id="e0465-147">GDI kann eine GDI-Transformation (über die [**setworldtransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) -Methode) oder andere Auswirkungen auf denselben DC anwenden, der vom Renderziel verwendet wird. in diesem Fall transformiert GDI die von Direct2D erstellte Bitmap.</span><span class="sxs-lookup"><span data-stu-id="e0465-147">It's possible for GDI to apply a GDI transform (through the [**SetWorldTransform**](/windows/desktop/api/wingdi/nf-wingdi-setworldtransform) method) or other effect to the same DC used by the render target, in which case GDI transforms the bitmap produced by Direct2D.</span></span> <span data-ttu-id="e0465-148">Die Verwendung einer GDI-Transformation zum Transformieren des Direct2D-Inhalts hat die Möglichkeit, die visuelle Qualität der Ausgabe zu beeinträchtigen, da Sie eine Bitmap transformieren, bei der das Antialiasing und die unter Pixel Positionierung bereits berechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="e0465-148">Using a GDI transform to transform the Direct2D content has the potential to degrade the visual quality of the output, because you're transforming a bitmap for which antialiasing and subpixel positioning have already been calculated.</span></span>

<span data-ttu-id="e0465-149">Nehmen Sie beispielsweise an, Sie verwenden das Renderziel, um eine Szene zu zeichnen, die Antialiasing-Geometrien und Text enthält.</span><span class="sxs-lookup"><span data-stu-id="e0465-149">For example, suppose you use the render target to draw a scene that contains antialiased geometries and text.</span></span> <span data-ttu-id="e0465-150">Wenn Sie eine GDI-Transformation verwenden, um eine Skalierungs Transformation auf den DC anzuwenden und die Szene so zu skalieren, dass Sie zehnmal größer ist, sehen Sie die pixelisierung und die verzweigten Kanten.</span><span class="sxs-lookup"><span data-stu-id="e0465-150">If you use a GDI transform to apply a scale transform to the DC and scale the scene so that it's 10 times larger, you'll see pixelization and jagged edges.</span></span> <span data-ttu-id="e0465-151">(Wenn Sie jedoch eine ähnliche Transformation mithilfe von Direct2D angewendet haben, wird die visuelle Qualität der Szene nicht beeinträchtigt.)</span><span class="sxs-lookup"><span data-stu-id="e0465-151">(If, however, you applied a similar transform using Direct2D, the visual quality of the scene would not be degraded.)</span></span>

<span data-ttu-id="e0465-152">In einigen Fällen ist es möglicherweise nicht offensichtlich, dass GDI zusätzliche Verarbeitungsvorgänge ausführt, die die Qualität des Direct2D-Inhalts beeinträchtigen können.</span><span class="sxs-lookup"><span data-stu-id="e0465-152">In some cases, it might not be obvious that GDI is performing additional processing that might degrade the quality of the Direct2D content.</span></span> <span data-ttu-id="e0465-153">Beispielsweise kann der Inhalt, der von einem [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) gerendert wird, bei einem Windows-Build von rechts nach links (RTL) horizontal invertiert werden, wenn er von GDI in das Ziel kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="e0465-153">For example, on a right-to-left (RTL) build of Windows, content rendered by an [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) might be horizontally inverted when GDI copies it to its destination.</span></span> <span data-ttu-id="e0465-154">Ob der Inhalt tatsächlich invertiert wird, hängt von den aktuellen Einstellungen des DC ab.</span><span class="sxs-lookup"><span data-stu-id="e0465-154">Whether the content is actually inverted depends on the current settings of the DC.</span></span>

<span data-ttu-id="e0465-155">Abhängig vom Typ des gerenderten Inhalts empfiehlt es sich, die Inversion zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="e0465-155">Depending on the type of content being rendered, you might want to prevent the inversion.</span></span> <span data-ttu-id="e0465-156">Wenn der Direct2D-Inhalt Klartext enthält, wird die Qualität des Texts von dieser Inversion herabgestuft.</span><span class="sxs-lookup"><span data-stu-id="e0465-156">If the Direct2D content includes ClearType text, this inversion will degrade the quality of the text.</span></span>

<span data-ttu-id="e0465-157">Sie können das Verhalten von RTL-Rendering mithilfe der [**setLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) -GDI-Funktion steuern.</span><span class="sxs-lookup"><span data-stu-id="e0465-157">You can control RTL rendering behavior by using the [**SetLayout**](/windows/desktop/api/wingdi/nf-wingdi-setlayout) GDI function.</span></span> <span data-ttu-id="e0465-158">Um die Spiegelung zu verhindern, müssen Sie die **setLayout** -GDI-Funktion aufrufen und das **Layout \_ bitmaporientationbeibehaltenes** als einzigen Wert für den zweiten Parameter angeben (kombinieren Sie ihn nicht mit **Layout \_ RTL**), wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="e0465-158">To prevent the mirroring, call the **SetLayout** GDI function and specify **LAYOUT\_BITMAPORIENTATIONPRESERVED** as the only value for the second parameter (do not combine it with **LAYOUT\_RTL**), as shown in the following example:</span></span>


```C++
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## <a name="draw-gdi-content-to-a-direct2d-gdi-compatible-render-target"></a><span data-ttu-id="e0465-159">Ziehen Sie GDI-Inhalte in ein Direct2D-GDI-Compatible Renderziel.</span><span class="sxs-lookup"><span data-stu-id="e0465-159">Draw GDI Content to a Direct2D GDI-Compatible Render Target</span></span>

<span data-ttu-id="e0465-160">Im vorherigen Abschnitt wird beschrieben, wie Sie Direct2D-Inhalte in einen GDI-DC schreiben.</span><span class="sxs-lookup"><span data-stu-id="e0465-160">The previous section describes how to write Direct2D content to a GDI DC.</span></span> <span data-ttu-id="e0465-161">Sie können GDI-Inhalte auch in ein Direct2D GDI-kompatibles Renderziel schreiben.</span><span class="sxs-lookup"><span data-stu-id="e0465-161">You can also write GDI content to a Direct2D GDI-compatible render target.</span></span> <span data-ttu-id="e0465-162">Diese Vorgehensweise ist nützlich für Anwendungen, die in erster Linie mit Direct2D Rendering, aber über ein Erweiterbarkeits Modell oder andere Legacy Inhalte verfügen, die die Fähigkeit zum Rendering mit GDI erfordern.</span><span class="sxs-lookup"><span data-stu-id="e0465-162">This approach is useful for applications that primarily render with Direct2D but have an extensibility model or other legacy content that requires the ability to render with GDI.</span></span>

<span data-ttu-id="e0465-163">Wenn Sie GDI-Inhalte in einem Direct2D GDI-kompatiblen Renderziel Renderziel, verwenden Sie ein [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)-Objekt, das Zugriff auf einen Gerätekontext bietet, der GDI-Draw-Aufrufe akzeptieren kann.</span><span class="sxs-lookup"><span data-stu-id="e0465-163">To render GDI content to a Direct2D GDI-compatible render target, use an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget), which provides access to a device context that can accept GDI draw calls.</span></span> <span data-ttu-id="e0465-164">Anders als bei anderen Schnittstellen wird ein **ID2D1GdiInteropRenderTarget** -Objekt nicht direkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0465-164">Unlike other interfaces, an **ID2D1GdiInteropRenderTarget** object is not created directly.</span></span> <span data-ttu-id="e0465-165">Verwenden Sie stattdessen die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode einer vorhandenen renderzielinstanz.</span><span class="sxs-lookup"><span data-stu-id="e0465-165">Instead, use the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method of an existing render target instance.</span></span> <span data-ttu-id="e0465-166">Dies wird im folgenden Code veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="e0465-166">The following code shows how to do this:</span></span>


```C++
        D2D1_RENDER_TARGET_PROPERTIES rtProps = D2D1::RenderTargetProperties();
        rtProps.usage =  D2D1_RENDER_TARGET_USAGE_GDI_COMPATIBLE;

        // Create a GDI compatible Hwnd render target.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            rtProps,
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );


        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->QueryInterface(__uuidof(ID2D1GdiInteropRenderTarget), (void**)&m_pGDIRT); 
        }
```



<span data-ttu-id="e0465-167">Im vorangehenden Code ist *m \_ pD2DFactory* ein Zeiger auf [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), und *m \_ pgdirt* ist ein Zeiger auf ein [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span><span class="sxs-lookup"><span data-stu-id="e0465-167">In the preceding code, *m\_pD2DFactory* is a pointer to an [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory), and *m\_pGDIRT* is a pointer to an [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget).</span></span>

<span data-ttu-id="e0465-168">Beachten Sie, dass das Flag [**D2D1 \_ Rendering \_ Target \_ Usage \_ GDI \_ Compatible**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) angegeben wird, wenn das HWND-GDI-kompatible Renderziel erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="e0465-168">Notice that the [**D2D1\_RENDER\_TARGET\_USAGE\_GDI\_COMPATIBLE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) flag is specified when creating the Hwnd GDI-compatible render target.</span></span> <span data-ttu-id="e0465-169">Wenn ein Pixel Format erforderlich ist, verwenden Sie das [DXGI- \_ Format \_ B8G8R8A8 \_ unorm](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span><span class="sxs-lookup"><span data-stu-id="e0465-169">If a pixel format is required, use [DXGI\_FORMAT\_B8G8R8A8\_UNORM](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format).</span></span> <span data-ttu-id="e0465-170">Wenn ein Alpha-Modus erforderlich ist, verwenden Sie den [**D2D1- \_ Alpha Modus, der \_ \_ vorab multipliziert**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) ist, oder den **D2D1 \_ alpha \_ \_**-Modus</span><span class="sxs-lookup"><span data-stu-id="e0465-170">If an alpha mode is required, use [**D2D1\_ALPHA\_MODE\_PREMULTIPLIED**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) or **D2D1\_ALPHA\_MODE\_IGNORE**.</span></span>

<span data-ttu-id="e0465-171">Beachten Sie, dass die [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) -Methode immer erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="e0465-171">Note that the [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method always succeeds.</span></span> <span data-ttu-id="e0465-172">Um zu testen, ob die Methoden der [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) -Schnittstelle für ein bestimmtes Renderziel funktionieren, erstellen Sie eine [**D2D1- \_ \_ Renderziel \_**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) Eigenschaft, die GDI-Kompatibilität und das entsprechende Pixel Format angibt, und rufen Sie dann die [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) -Methode des Renderziels auf, um zu überprüfen, ob das Renderziel GDI</span><span class="sxs-lookup"><span data-stu-id="e0465-172">To test whether the [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget) interface's methods will work for a given render target, create a [**D2D1\_RENDER\_TARGET\_PROPERTIES**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties) that specifies GDI compatibility and the appropriate pixel format, and then call the render target's [**IsSupported**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-issupported(constd2d1_render_target_properties)) method to see whether the render target is GDI-compatible.</span></span>

<span data-ttu-id="e0465-173">Im folgenden Beispiel wird gezeigt, wie ein Kreis Diagramm (GDI-Inhalt) in das HWND-GDI-kompatible Renderziel gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="e0465-173">The following example shows how to draw a pie chart (GDI content) to the Hwnd GDI-compatible render target.</span></span>


```C++
        HDC hDC = NULL;
        hr = m_pGDIRT->GetDC(D2D1_DC_INITIALIZE_MODE_COPY, &hDC);

        if (SUCCEEDED(hr))
        {
            // Draw the pie chart to the GDI render target associated with the Hwnd render target.
            HGDIOBJ original = NULL;
            original = SelectObject(
                hDC,
                GetStockObject(DC_PEN)
                );

            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);
            SelectObject(hDC, blackPen);

            Ellipse(hDC, 300, 50, 500, 250);

            POINT pntArray1[2];
            pntArray1[0].x = 400;
            pntArray1[0].y = 150;
            pntArray1[1].x = static_cast<LONG>(400 + 100 * 0.15425);
            pntArray1[1].y = static_cast<LONG>(150 - 100 * 0.9885);

            POINT pntArray2[2];
            pntArray2[0].x = 400;
            pntArray2[0].y = 150;
            pntArray2[1].x = static_cast<LONG>(400 + 100 * 0.525);
            pntArray2[1].y = static_cast<LONG>(150 + 100 * 0.8509);

            POINT pntArray3[2];
            pntArray3[0].x = 400;
            pntArray3[0].y = 150;
            pntArray3[1].x = static_cast<LONG>(400 - 100 * 0.988);
            pntArray3[1].y = static_cast<LONG>(150 - 100 * 0.15425);

            Polyline(hDC, pntArray1, 2);
            Polyline(hDC, pntArray2, 2);
            Polyline(hDC, pntArray3, 2);

            DeleteObject(blackPen);

            // Restore the original object.
            SelectObject(hDC, original);

            m_pGDIRT->ReleaseDC(NULL);
        }

```



<span data-ttu-id="e0465-174">Der Code gibt Diagramme aus, wie in der folgenden Abbildung gezeigt, mit aufrufen, um den Unterschied bei der renderingqualität hervorzuheben.</span><span class="sxs-lookup"><span data-stu-id="e0465-174">The code outputs charts as shown in the following illustration with callouts to highlight the rendering quality difference.</span></span> <span data-ttu-id="e0465-175">Das Rechte Kreis Diagramm (GDI-Inhalt) hat eine niedrigere renderingqualität als das linke Kreis Diagramm (Direct2D Content).</span><span class="sxs-lookup"><span data-stu-id="e0465-175">The right pie chart (GDI content) has lower rendering quality than the left pie chart (Direct2D content).</span></span> <span data-ttu-id="e0465-176">Dies liegt daran, dass Direct2D mit Antialiasing rendern kann.</span><span class="sxs-lookup"><span data-stu-id="e0465-176">This is because Direct2D is capable of rendering with antialiasing</span></span>

![Abbildung von zwei Zirkel Diagrammen, die in einem Direct2D GDI-kompatiblen Renderziel gerendert werden](images/gdicontentind2d.png)

## <a name="related-topics"></a><span data-ttu-id="e0465-178">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0465-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0465-179">**ID2D1Factory:: kreatedcrendertarget**</span><span class="sxs-lookup"><span data-stu-id="e0465-179">**ID2D1Factory::CreateDCRenderTarget**</span></span>](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget)
</dt> <dt>

[<span data-ttu-id="e0465-180">**ID2D1DCRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e0465-180">**ID2D1DCRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget)
</dt> <dt>

[<span data-ttu-id="e0465-181">**ID2D1GdiInteropRenderTarget**</span><span class="sxs-lookup"><span data-stu-id="e0465-181">**ID2D1GdiInteropRenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)
</dt> <dt>

[<span data-ttu-id="e0465-182">**D2D1 \_ \_ Renderziel \_ Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="e0465-182">**D2D1\_RENDER\_TARGET\_PROPERTIES**</span></span>](/windows/desktop/api/d2d1/ns-d2d1-d2d1_render_target_properties)
</dt> <dt>

[<span data-ttu-id="e0465-183">GDI-Geräte Kontexte</span><span class="sxs-lookup"><span data-stu-id="e0465-183">GDI Device Contexts</span></span>](/windows/desktop/gdi/device-contexts)
</dt> <dt>

[<span data-ttu-id="e0465-184">GDI SDK</span><span class="sxs-lookup"><span data-stu-id="e0465-184">GDI SDK</span></span>](/windows/desktop/gdi/windows-gdi)
</dt> </dl>

 

 