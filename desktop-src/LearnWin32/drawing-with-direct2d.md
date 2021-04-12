---
title: Zeichnen mit Direct2D
description: Nachdem Sie Ihre Grafik Ressourcen erstellt haben, können Sie Sie zeichnen.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40f8f3cf82d3ce6f485a7c54700c32c9eb65d054
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472900"
---
# <a name="drawing-with-direct2d"></a><span data-ttu-id="a9330-103">Zeichnen mit Direct2D</span><span class="sxs-lookup"><span data-stu-id="a9330-103">Drawing with Direct2D</span></span>

<span data-ttu-id="a9330-104">Nachdem Sie Ihre Grafik Ressourcen erstellt haben, können Sie Sie zeichnen.</span><span class="sxs-lookup"><span data-stu-id="a9330-104">After you create your graphics resources, you are ready to draw.</span></span>

## <a name="drawing-an-ellipse"></a><span data-ttu-id="a9330-105">Zeichnen einer Ellipse</span><span class="sxs-lookup"><span data-stu-id="a9330-105">Drawing an Ellipse</span></span>

<span data-ttu-id="a9330-106">Das [Circle](your-first-direct2d-program.md) -Programm führt eine sehr einfache Zeichnungs Logik durch:</span><span class="sxs-lookup"><span data-stu-id="a9330-106">The [Circle](your-first-direct2d-program.md) program performs very simple drawing logic:</span></span>

1.  <span data-ttu-id="a9330-107">Füllen Sie den Hintergrund mit einer voll Tonfarbe aus.</span><span class="sxs-lookup"><span data-stu-id="a9330-107">Fill the background with a solid color.</span></span>
2.  <span data-ttu-id="a9330-108">Zeichnen Sie einen gefüllten Kreis.</span><span class="sxs-lookup"><span data-stu-id="a9330-108">Draw a filled circle.</span></span>

![ein Screenshot des Kreises-Programms.](images/graphics08.png)

<span data-ttu-id="a9330-110">Da das Renderziel ein Fenster ist (im Gegensatz zu einer Bitmap oder einer anderen Offscreen-Oberfläche), erfolgt das Zeichnen als Reaktion auf WM-Zeichnungs Meldungen. [**\_**](/windows/desktop/gdi/wm-paint)</span><span class="sxs-lookup"><span data-stu-id="a9330-110">Because the render target is a window (as opposed to a bitmap or other offscreen surface), drawing is done in response to [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) messages.</span></span> <span data-ttu-id="a9330-111">Der folgende Code zeigt die Fenster Prozedur für das kreisprogramm.</span><span class="sxs-lookup"><span data-stu-id="a9330-111">The following code shows the window procedure for the Circle program.</span></span>


```C++
LRESULT MainWindow::HandleMessage(UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    switch (uMsg)
    {
        case WM_PAINT:
            OnPaint();
            return 0;

         // Other messages not shown...
    }
    return DefWindowProc(m_hwnd, uMsg, wParam, lParam);
}
```

<span data-ttu-id="a9330-112">Hier ist der Code, der den Kreis zeichnet.</span><span class="sxs-lookup"><span data-stu-id="a9330-112">Here is the code that draws the circle.</span></span>

```C++
void MainWindow::OnPaint()
{
    HRESULT hr = CreateGraphicsResources();
    if (SUCCEEDED(hr))
    {
        PAINTSTRUCT ps;
        BeginPaint(m_hwnd, &ps);
     
        pRenderTarget->BeginDraw();

        pRenderTarget->Clear( D2D1::ColorF(D2D1::ColorF::SkyBlue) );
        pRenderTarget->FillEllipse(ellipse, pBrush);

        hr = pRenderTarget->EndDraw();
        if (FAILED(hr) || hr == D2DERR_RECREATE_TARGET)
        {
            DiscardGraphicsResources();
        }
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="a9330-113">Die [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle wird für alle Zeichnungsvorgänge verwendet.</span><span class="sxs-lookup"><span data-stu-id="a9330-113">The [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface is used for all drawing operations.</span></span> <span data-ttu-id="a9330-114">Die-Methode des Programms `OnPaint` führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="a9330-114">The program's `OnPaint` method does the following:</span></span>

1.  <span data-ttu-id="a9330-115">Die [**ID2D1RenderTarget:: beginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode signalisiert den Anfang der Zeichnung.</span><span class="sxs-lookup"><span data-stu-id="a9330-115">The [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method signals the start of drawing.</span></span>
2.  <span data-ttu-id="a9330-116">Die [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) -Methode füllt das gesamte Renderziel mit einer voll Tonfarbe aus.</span><span class="sxs-lookup"><span data-stu-id="a9330-116">The [**ID2D1RenderTarget::Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) method fills the entire render target with a solid color.</span></span> <span data-ttu-id="a9330-117">Die Farbe wird als [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) -Struktur angegeben.</span><span class="sxs-lookup"><span data-stu-id="a9330-117">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) structure.</span></span> <span data-ttu-id="a9330-118">Sie können die [**D2D1:: colorf**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) -Klasse verwenden, um die Struktur zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="a9330-118">You can use the [**D2D1::ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) class to initialize the structure.</span></span> <span data-ttu-id="a9330-119">Weitere Informationen finden Sie unter [Verwenden von Color in Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="a9330-119">For more information, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>
3.  <span data-ttu-id="a9330-120">Die [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) -Methode zeichnet eine gefüllte Ellipse mit dem angegebenen Pinsel für die Füllung.</span><span class="sxs-lookup"><span data-stu-id="a9330-120">The [**ID2D1RenderTarget::FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) method draws a filled ellipse, using the specified brush for the fill.</span></span> <span data-ttu-id="a9330-121">Eine Ellipse wird von einem Mittelpunkt und dem x-und y-Radii angegeben.</span><span class="sxs-lookup"><span data-stu-id="a9330-121">An ellipse is specified by a center point and the x- and y-radii.</span></span> <span data-ttu-id="a9330-122">Wenn x-und y-Radii identisch sind, ist das Ergebnis ein Kreis.</span><span class="sxs-lookup"><span data-stu-id="a9330-122">If the x- and y-radii are the same, the result is a circle.</span></span>
4.  <span data-ttu-id="a9330-123">Die [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode signalisiert den Abschluss der Zeichnung für diesen Frame.</span><span class="sxs-lookup"><span data-stu-id="a9330-123">The [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method signals the completion of drawing for this frame.</span></span> <span data-ttu-id="a9330-124">Alle Zeichnungsvorgänge müssen zwischen Aufrufen von [**beginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und **EndDraw** eingefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a9330-124">All drawing operations must be placed between calls to [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and **EndDraw**.</span></span>

<span data-ttu-id="a9330-125">Die [**beginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)-, [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)-und [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) -Methoden verfügen alle über einen **void** -Rückgabetyp.</span><span class="sxs-lookup"><span data-stu-id="a9330-125">The [**BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw), [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear), and [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) methods all have a **void** return type.</span></span> <span data-ttu-id="a9330-126">Wenn während der Ausführung einer dieser Methoden ein Fehler auftritt, wird der Fehler durch den Rückgabewert der [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode signalisiert.</span><span class="sxs-lookup"><span data-stu-id="a9330-126">If an error occurs during the execution of any of these methods, the error is signaled through the return value of the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="a9330-127">Die- `CreateGraphicsResources` Methode wird im Thema [Erstellen von Direct2D-Ressourcen](render-targets--devices--and-resources.md)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="a9330-127">The `CreateGraphicsResources` method is shown in the topic [Creating Direct2D Resources](render-targets--devices--and-resources.md).</span></span> <span data-ttu-id="a9330-128">Diese Methode erstellt das Renderziel und den Pinsel mit voll Tonfarbe.</span><span class="sxs-lookup"><span data-stu-id="a9330-128">This method creates the render target and the solid-color brush.</span></span>

<span data-ttu-id="a9330-129">Das Gerät puffert möglicherweise die Zeichnungs Befehle und verzögert die Ausführung, bis [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a9330-129">The device might buffer the drawing commands and defer executing them until [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) is called.</span></span> <span data-ttu-id="a9330-130">Sie können erzwingen, dass das Gerät ausstehende Zeichnungs Befehle ausführt, indem Sie [**ID2D1RenderTarget:: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a9330-130">You can force the device to execute any pending drawing commands by calling [**ID2D1RenderTarget::Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span> <span data-ttu-id="a9330-131">Das leeren kann jedoch die Leistung beeinträchtigen.</span><span class="sxs-lookup"><span data-stu-id="a9330-131">Flushing can reduce performance, however.</span></span>

## <a name="handling-device-loss"></a><span data-ttu-id="a9330-132">Behandeln von Geräte Verlusten</span><span class="sxs-lookup"><span data-stu-id="a9330-132">Handling Device Loss</span></span>

<span data-ttu-id="a9330-133">Während das Programm ausgeführt wird, ist das verwendete Grafikgerät möglicherweise nicht mehr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a9330-133">While your program is running, the graphics device that you are using might become unavailable.</span></span> <span data-ttu-id="a9330-134">Beispielsweise kann das Gerät verloren gehen, wenn sich die Bildschirmauflösung ändert, oder wenn der Benutzer den Anzeige Adapter entfernt.</span><span class="sxs-lookup"><span data-stu-id="a9330-134">For example, the device can be lost if the display resolution changes, or if the user removes the display adapter.</span></span> <span data-ttu-id="a9330-135">Wenn das Gerät verloren geht, wird auch das Renderziel zusammen mit allen geräteabhängigen Ressourcen, die dem Gerät zugeordnet sind, ungültig.</span><span class="sxs-lookup"><span data-stu-id="a9330-135">If the device is lost, the render target also becomes invalid, along with any device-dependent resources that were associated with the device.</span></span> <span data-ttu-id="a9330-136">Direct2D signalisiert einem verlorenen Gerät durch das Zurückgeben des Fehlercodes **D2DERR " \_ \_ Ziel neu erstellen** " aus der [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a9330-136">Direct2D signals a lost device by returning the error code **D2DERR\_RECREATE\_TARGET** from the [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span> <span data-ttu-id="a9330-137">Wenn Sie diesen Fehlercode erhalten, müssen Sie das Renderziel und alle geräteabhängigen Ressourcen neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9330-137">If you receive this error code, you must re-create the render target and all device-dependent resources.</span></span>

<span data-ttu-id="a9330-138">Um eine Ressource zu verwerfen, geben Sie einfach die Schnittstelle für diese Ressource frei.</span><span class="sxs-lookup"><span data-stu-id="a9330-138">To discard a resource, simply release the interface for that resource.</span></span>


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



<span data-ttu-id="a9330-139">Das Erstellen einer Ressource kann ein kostspieliger Vorgang sein. Erstellen Sie daher ihre Ressourcen nicht für jede WM-Zeichnungs Nachricht neu. [**\_**](/windows/desktop/gdi/wm-paint)</span><span class="sxs-lookup"><span data-stu-id="a9330-139">Creating a resource can be an expensive operation, so do not recreate your resources for every [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="a9330-140">Erstellen Sie eine Ressource einmal, und speichern Sie den Ressourcen Zeiger zwischen, bis die Ressource aufgrund eines Geräte Verlusts ungültig wird oder wenn Sie diese Ressource nicht mehr benötigen.</span><span class="sxs-lookup"><span data-stu-id="a9330-140">Create a resource once, and cache the resource pointer until the resource becomes invalid due to device loss, or until you no longer need that resource.</span></span>

## <a name="the-direct2d-render-loop"></a><span data-ttu-id="a9330-141">Die Direct2D-Renderschleife</span><span class="sxs-lookup"><span data-stu-id="a9330-141">The Direct2D Render Loop</span></span>

<span data-ttu-id="a9330-142">Unabhängig davon, was Sie zeichnen, sollte das Programm eine Schleife ähnlich der folgenden ausführen.</span><span class="sxs-lookup"><span data-stu-id="a9330-142">Regardless of what you draw, your program should perform a loop similar to following.</span></span>

1.  <span data-ttu-id="a9330-143">Geräteunabhängige Ressourcen erstellen.</span><span class="sxs-lookup"><span data-stu-id="a9330-143">Create device-independent resources.</span></span>
2.  <span data-ttu-id="a9330-144">Rendering der Szene.</span><span class="sxs-lookup"><span data-stu-id="a9330-144">Render the scene.</span></span>
    1.  <span data-ttu-id="a9330-145">Prüfen Sie, ob ein gültiges Renderziel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a9330-145">Check if a valid render target exists.</span></span> <span data-ttu-id="a9330-146">Wenn dies nicht der Wert ist, erstellen Sie das Renderziel und die geräteabhängigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a9330-146">If not, create the render target and the device-dependent resources.</span></span>
    2.  <span data-ttu-id="a9330-147">Aufrufen von [**ID2D1RenderTarget:: beginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span><span class="sxs-lookup"><span data-stu-id="a9330-147">Call [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).</span></span>
    3.  <span data-ttu-id="a9330-148">Ausstellen von Zeichnungs Befehlen.</span><span class="sxs-lookup"><span data-stu-id="a9330-148">Issue drawing commands.</span></span>
    4.  <span data-ttu-id="a9330-149">Aufrufen von [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="a9330-149">Call [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>
    5.  <span data-ttu-id="a9330-150">Wenn [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) das **D2DERR \_ - \_ Ziel neu erstellen** zurückgibt, verwerfen Sie das Renderziel und Geräte abhängige Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="a9330-150">If [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) returns **D2DERR\_RECREATE\_TARGET**, discard the render target and device-dependent resources.</span></span>
3.  <span data-ttu-id="a9330-151">Wiederholen Sie Schritt 2, wenn Sie die Szene aktualisieren oder neu zeichnen müssen.</span><span class="sxs-lookup"><span data-stu-id="a9330-151">Repeat step 2 whenever you need to update or redraw the scene.</span></span>

<span data-ttu-id="a9330-152">Wenn das Renderziel ein Fenster ist, tritt Schritt 2 auf, wenn das Fenster eine [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung empfängt.</span><span class="sxs-lookup"><span data-stu-id="a9330-152">If the render target is a window, step 2 occurs whenever the window receives a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span>

<span data-ttu-id="a9330-153">In der hier gezeigten Schleife werden Geräte Verluste behandelt, indem die geräteabhängigen Ressourcen verworfen und zu Beginn der nächsten Schleife neu erstellt werden (Schritt 2a).</span><span class="sxs-lookup"><span data-stu-id="a9330-153">The loop shown here handles device loss by discarding the device-dependent resources and re-creating them at the start of the next loop (step 2a).</span></span>

## <a name="next"></a><span data-ttu-id="a9330-154">Nächste</span><span class="sxs-lookup"><span data-stu-id="a9330-154">Next</span></span>

[<span data-ttu-id="a9330-155">DPI-und Device-Independent Pixel</span><span class="sxs-lookup"><span data-stu-id="a9330-155">DPI and Device-Independent Pixels</span></span>](dpi-and-device-independent-pixels.md)

 

 