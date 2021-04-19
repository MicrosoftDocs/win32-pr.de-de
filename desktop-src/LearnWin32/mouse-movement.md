---
title: Mausbewegung
description: Mausbewegung
ms.assetid: 54366E9B-470A-4155-8A5F-425BAC8AC1A5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14176310882651cdeb2939d0db55368ff133ea11
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2021
ms.locfileid: "106363826"
---
# <a name="mouse-movement"></a><span data-ttu-id="e1b5c-103">Mausbewegung</span><span class="sxs-lookup"><span data-stu-id="e1b5c-103">Mouse Movement</span></span>

<span data-ttu-id="e1b5c-104">Wenn die Maus bewegt wird, stellt Windows eine [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht zur Folge.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-104">When the mouse moves, Windows posts a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message.</span></span> <span data-ttu-id="e1b5c-105">Standardmäßig wechselt der **WM- \_ mousetmove** -Vorgang in das Fenster, das den Cursor enthält.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-105">By default, **WM\_MOUSEMOVE** goes to the window that contains the cursor.</span></span> <span data-ttu-id="e1b5c-106">Sie können dieses Verhalten überschreiben, indem Sie die Maus *erfassen* , die im nächsten Abschnitt beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-106">You can override this behavior by *capturing* the mouse, which is described in the next section.</span></span>

<span data-ttu-id="e1b5c-107">Die [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht enthält die gleichen Parameter wie die Meldungen für Mausklicks.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-107">The [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message contains the same parameters as the messages for mouse clicks.</span></span> <span data-ttu-id="e1b5c-108">Die niedrigsten 16 Bits von *LPARAM* enthalten die x-Koordinate, und die nächsten 16 Bits enthalten die y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-108">The lowest 16 bits of *lParam* contain the x-coordinate, and the next 16 bits contain the y-coordinate.</span></span> <span data-ttu-id="e1b5c-109">Verwenden Sie die lParam-Makros [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) , um die Koordinaten aus *LPARAM* zu entpacken.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-109">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to unpack the coordinates from *lParam*.</span></span> <span data-ttu-id="e1b5c-110">Der *wParam* -Parameter enthält ein bitweises **or** von-Flags, das den Zustand der anderen Maustasten sowie die UMSCHALTTASTE und die STRG-Taste angibt.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-110">The *wParam* parameter contains a bitwise **OR** of flags, indicating the state of the other mouse buttons plus the SHIFT and CTRL keys.</span></span> <span data-ttu-id="e1b5c-111">Der folgende Code Ruft die Maus Koordinaten aus *LPARAM* ab.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-111">The following code gets the mouse coordinates from *lParam*.</span></span>


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



<span data-ttu-id="e1b5c-112">Beachten Sie, dass sich diese Koordinaten in Pixel befinden, nicht in geräteunabhängigen Pixeln (Dips).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-112">Remember that these coordinates are in pixels, not device-independent pixels (DIPs).</span></span> <span data-ttu-id="e1b5c-113">Weiter unten in diesem Thema betrachten wir den Code, der zwischen den beiden Einheiten konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-113">Later in this topic, we will look at code that converts between the two units.</span></span>

<span data-ttu-id="e1b5c-114">Ein Fenster kann auch eine [**WM- \_ mousetmove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht empfangen, wenn die Position des Cursors relativ zum Fenster geändert wird.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-114">A window can also receive a [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) message if the position of the cursor changes relative to the window.</span></span> <span data-ttu-id="e1b5c-115">Wenn der Cursor z. b. auf einem Fenster positioniert ist und der Benutzer das Fenster verbirgt, empfängt das Fenster **WM- \_ MouseMove** -Meldungen, auch wenn die Maus nicht verschoben wurde.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-115">For example, if the cursor is positioned over a window, and the user hides the window, the window receives **WM\_MOUSEMOVE** messages even if the mouse did not move.</span></span> <span data-ttu-id="e1b5c-116">Eine Folge dieses Verhaltens besteht darin, dass sich die Maus Koordinaten zwischen den **WM- \_ MouseMove** -Meldungen möglicherweise nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-116">One consequence of this behavior is that the mouse coordinates might not change between **WM\_MOUSEMOVE** messages.</span></span>

## <a name="capturing-mouse-movement-outside-the-window"></a><span data-ttu-id="e1b5c-117">Erfassen der Mausbewegung außerhalb des Fensters</span><span class="sxs-lookup"><span data-stu-id="e1b5c-117">Capturing Mouse Movement Outside the Window</span></span>

<span data-ttu-id="e1b5c-118">Standardmäßig beendet ein Fenster den Empfang von [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten, wenn die Maus über den Rand des Client Bereichs bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-118">By default, a window stops receiving [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages if the mouse moves past the edge of the client area.</span></span> <span data-ttu-id="e1b5c-119">Für einige Vorgänge müssen Sie jedoch möglicherweise die Mausposition hinter diesem Punkt nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-119">But for some operations, you might need to track the mouse position beyond this point.</span></span> <span data-ttu-id="e1b5c-120">Beispielsweise kann ein Zeichnungsprogramm es dem Benutzer ermöglichen, das Auswahl Rechteck über den Rand des Fensters hinaus zu ziehen, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-120">For example, a drawing program might enable the user to drag the selection rectangle beyond the edge of the window, as shown in the following diagram.</span></span>

![eine Abbildung der Maus Aufzeichnung.](images/input01.png)

<span data-ttu-id="e1b5c-122">Um Nachrichten mit Mauszeiger über den Rand des Fensters zu empfangen, müssen Sie die Funktion [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-122">To receive mouse-move messages past the edge of the window, call the [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) function.</span></span> <span data-ttu-id="e1b5c-123">Nachdem diese Funktion aufgerufen wurde, empfängt das Fenster weiterhin WM- [**\_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten, solange der Benutzer mindestens eine Maustaste gedrückt hält, auch wenn der Mauszeiger außerhalb des Fensters bewegt wird.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-123">After this function is called, the window will continue to receive [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages for as long as the user holds at least one mouse button down, even if the mouse moves outside the window.</span></span> <span data-ttu-id="e1b5c-124">Das Erfassungsfenster muss das Vordergrund Fenster sein, und nur ein Fenster kann das Erfassungsfenster gleichzeitig sein.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-124">The capture window must be the foreground window, and only one window can be the capture window at a time.</span></span> <span data-ttu-id="e1b5c-125">Um die Maus Aufzeichnung freizugeben, nennen Sie die [**releasecapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-125">To release mouse capture, call the [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) function.</span></span>

<span data-ttu-id="e1b5c-126">In der Regel verwenden Sie [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) und [**releasecapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) wie folgt.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-126">You would typically use [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) and [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) in the following way.</span></span>

1.  <span data-ttu-id="e1b5c-127">Wenn der Benutzer die linke Maustaste drückt, wird [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) aufgerufen, um mit dem Erfassen der Maus zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-127">When the user presses the left mouse button, call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to start capturing the mouse.</span></span>
2.  <span data-ttu-id="e1b5c-128">Reagieren auf Maus Verschiebungs Meldungen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-128">Respond to mouse-move messages.</span></span>
3.  <span data-ttu-id="e1b5c-129">Wenn der Benutzer die linke Maustaste loslässt, wird [**releasecapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture)aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-129">When the user releases the left mouse button, call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture).</span></span>

## <a name="example-drawing-circles"></a><span data-ttu-id="e1b5c-130">Beispiel: Zeichnen von Kreisen</span><span class="sxs-lookup"><span data-stu-id="e1b5c-130">Example: Drawing Circles</span></span>

<span data-ttu-id="e1b5c-131">Erweitern Sie nun das kreisprogramm von [Modul 3](module-3---windows-graphics.md) , indem Sie dem Benutzer das Zeichnen eines Kreises mit der Maus ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-131">Let's extend the Circle program from [Module 3](module-3---windows-graphics.md) by enabling the user to draw a circle with the mouse.</span></span> <span data-ttu-id="e1b5c-132">Beginnen Sie mit dem [Direct2D Circle-Beispiel](direct2d-circle-sample.md) Programm.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-132">Start with the [Direct2D Circle Sample](direct2d-circle-sample.md) program.</span></span> <span data-ttu-id="e1b5c-133">Wir ändern den Code in diesem Beispiel, um einfache Zeichnung hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-133">We will modify the code in this sample to add simple drawing.</span></span> <span data-ttu-id="e1b5c-134">Fügen Sie zunächst der-Klasse eine neue Member-Variable hinzu `MainWindow` .</span><span class="sxs-lookup"><span data-stu-id="e1b5c-134">First, add a new member variable to the `MainWindow` class.</span></span>


```C++
    D2D1_POINT_2F           ptMouse;
```



<span data-ttu-id="e1b5c-135">Diese Variable speichert die Maustaste, während der Benutzer die Maus zieht.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-135">This variable stores the mouse-down position while the user is dragging the mouse.</span></span> <span data-ttu-id="e1b5c-136">`MainWindow`Initialisieren Sie im Konstruktor die Variablen *Ellipse* und *ptmouse* .</span><span class="sxs-lookup"><span data-stu-id="e1b5c-136">In the `MainWindow` constructor, initialize the *ellipse* and *ptMouse* variables.</span></span>


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



<span data-ttu-id="e1b5c-137">Entfernen Sie den Text der- `MainWindow::CalculateLayout` Methode. Dies ist für dieses Beispiel nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-137">Remove the body of the `MainWindow::CalculateLayout` method; it's not required for this example.</span></span>


```C++
    void    CalculateLayout() { }
```



<span data-ttu-id="e1b5c-138">Deklarieren Sie anschließend die Meldungs Handler für die nach-unten-Taste, die nach-links-Taste und die Maus Verschiebungs Meldungen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-138">Next, declare message handlers for the left-button down, left-button up, and mouse-move messages.</span></span>


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



<span data-ttu-id="e1b5c-139">Maus Koordinaten werden in physischen Pixeln angegeben, aber Direct2D erwartet geräteunabhängige Pixel (Dips).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-139">Mouse coordinates are given in physical pixels, but Direct2D expects device-independent pixels (DIPs).</span></span> <span data-ttu-id="e1b5c-140">Um die Einstellungen für hohe DPI-Einstellungen ordnungsgemäß zu verarbeiten, müssen Sie die Pixelkoordinaten in Dips übersetzen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-140">To handle high-DPI settings correctly, you must translate the pixel coordinates into DIPs.</span></span> <span data-ttu-id="e1b5c-141">Weitere Informationen zu dpi finden Sie unter [dpi und Device-Independent Pixel](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-141">For more discussion about DPI, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span> <span data-ttu-id="e1b5c-142">Der folgende Code zeigt eine Hilfsklasse, die Pixel in Dips konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-142">The following code shows a helper class that converts pixels into DIPs.</span></span>


```C++
class DPIScale
{
    static float scaleX;
    static float scaleY;

public:
    static void Initialize(ID2D1Factory *pFactory)
    {
        FLOAT dpiX, dpiY;
        pFactory->GetDesktopDpi(&dpiX, &dpiY);
        scaleX = dpiX/96.0f;
        scaleY = dpiY/96.0f;
    }

    template <typename T>
    static D2D1_POINT_2F PixelsToDips(T x, T y)
    {
        return D2D1::Point2F(static_cast<float>(x) / scaleX, static_cast<float>(y) / scaleY);
    }
};

float DPIScale::scaleX = 1.0f;
float DPIScale::scaleY = 1.0f;
```



<span data-ttu-id="e1b5c-143">Rufen `DPIScale::Initialize` Sie in Ihrem [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Handler auf, nachdem Sie das Direct2D Factory-Objekt erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-143">Call `DPIScale::Initialize` in your [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) handler, after you create the Direct2D factory object.</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        DPIScale::Initialize(pFactory);
        return 0;
```



<span data-ttu-id="e1b5c-144">Gehen Sie folgendermaßen vor, um die Maus Koordinaten in Dips aus den Maus Meldungen abzurufen:</span><span class="sxs-lookup"><span data-stu-id="e1b5c-144">To get the mouse coordinates in DIPs from the mouse messages, do the following:</span></span>

1.  <span data-ttu-id="e1b5c-145">Verwenden Sie die lParam-Makros [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) , um die Pixelkoordinaten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-145">Use the [**GET\_X\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) and [**GET\_Y\_LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) macros to get the pixel coordinates.</span></span> <span data-ttu-id="e1b5c-146">Diese Makros sind in WINDOWSX. h definiert. denken Sie daher daran, diesen Header in das Projekt einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-146">These macros are defined in WindowsX.h, so remember to include that header in your project.</span></span>
2.  <span data-ttu-id="e1b5c-147">`DPIScale::PixelsToDipsX`Mit und können Sie `DPIScale::PixelsToDipsY` Pixel in Dips konvertieren.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-147">Call `DPIScale::PixelsToDipsX` and `DPIScale::PixelsToDipsY` to convert pixels to DIPs.</span></span>

<span data-ttu-id="e1b5c-148">Fügen Sie nun die Meldungs Handler ihrer Fenster Prozedur hinzu.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-148">Now add the message handlers to your window procedure.</span></span>


```C++
    case WM_LBUTTONDOWN: 
        OnLButtonDown(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;

    case WM_LBUTTONUP: 
        OnLButtonUp();
        return 0;

    case WM_MOUSEMOVE: 
        OnMouseMove(GET_X_LPARAM(lParam), GET_Y_LPARAM(lParam), (DWORD)wParam);
        return 0;
```



<span data-ttu-id="e1b5c-149">Implementieren Sie schließlich die Nachrichten Handler selbst.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-149">Finally, implement the message handlers themselves.</span></span>

### <a name="left-button-down"></a><span data-ttu-id="e1b5c-150">Linke Schaltfläche nach unten</span><span class="sxs-lookup"><span data-stu-id="e1b5c-150">Left Button Down</span></span>

<span data-ttu-id="e1b5c-151">Führen Sie für die nach-links-Taste folgende Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="e1b5c-151">For the left-button down message, do the following:</span></span>

1.  <span data-ttu-id="e1b5c-152">Ruft [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) auf, um mit dem Erfassen der Maus zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-152">Call [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) to begin capturing the mouse.</span></span>
2.  <span data-ttu-id="e1b5c-153">Speichert die Position des Mausklicks in der *ptmouse* -Variablen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-153">Store the position of the mouse click in the *ptMouse* variable.</span></span> <span data-ttu-id="e1b5c-154">Diese Position definiert die linke obere Ecke des umgebenden Felds für die Ellipse.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-154">This position defines the upper left corner of the bounding box for the ellipse.</span></span>
3.  <span data-ttu-id="e1b5c-155">Setzen Sie die Ellipse-Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-155">Reset the ellipse structure.</span></span>
4.  <span data-ttu-id="e1b5c-156">Wenden Sie sich an [**invalidatup**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="e1b5c-156">Call [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="e1b5c-157">Diese Funktion erzwingt, dass das Fenster neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-157">This function forces the window to be repainted.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a><span data-ttu-id="e1b5c-158">Mausbewegung</span><span class="sxs-lookup"><span data-stu-id="e1b5c-158">Mouse Move</span></span>

<span data-ttu-id="e1b5c-159">Überprüfen Sie für die Maus Verschiebungs Meldung, ob die linke Maustaste gedrückt ist.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-159">For the mouse-move message, check whether the left mouse button is down.</span></span> <span data-ttu-id="e1b5c-160">Wenn dies der Fall ist, berechnen Sie die Ellipse neu, und zeichnen Sie das Fenster neu.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-160">If it is, recalculate the ellipse and repaint the window.</span></span> <span data-ttu-id="e1b5c-161">In Direct2D wird eine Ellipse durch den Mittelpunkt und x-und y-Radii definiert.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-161">In Direct2D, an ellipse is defined by the center point and x- and y-radii.</span></span> <span data-ttu-id="e1b5c-162">Wir möchten eine Ellipse zeichnen, die dem umgebenden Feld entspricht, das durch den MouseDown-Punkt (*ptmouse*) und die aktuelle Cursorposition (*x*, *y*) definiert wird. Daher ist ein wenig arithmetischer Wert erforderlich, um die Breite, Höhe und Position der Ellipse zu finden.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-162">We want to draw an ellipse that fits the bounding box defined by the mouse-down point (*ptMouse*) and the current cursor position (*x*, *y*), so a bit of arithmetic is needed to find the width, height, and position of the ellipse.</span></span>

<span data-ttu-id="e1b5c-163">Der folgende Code berechnet die Ellipse neu und ruft dann [**invalidateriert**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) auf, um das Fenster neu zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-163">The following code recalculates the ellipse and then calls [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) to repaint the window.</span></span>

![Diagramm, das eine Ellipse mit x-und y-Radien anzeigt.](images/input02.png)


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    if (flags & MK_LBUTTON) 
    { 
        const D2D1_POINT_2F dips = DPIScale::PixelsToDips(pixelX, pixelY);

        const float width = (dips.x - ptMouse.x) / 2;
        const float height = (dips.y - ptMouse.y) / 2;
        const float x1 = ptMouse.x + width;
        const float y1 = ptMouse.y + height;

        ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);

        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



### <a name="left-button-up"></a><span data-ttu-id="e1b5c-165">Linke Schaltfläche nach oben</span><span class="sxs-lookup"><span data-stu-id="e1b5c-165">Left Button Up</span></span>

<span data-ttu-id="e1b5c-166">Wenn Sie die nach-oben-Taste drücken, nennen Sie einfach [**releasecapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) , um die Maus Aufzeichnung freizugeben.</span><span class="sxs-lookup"><span data-stu-id="e1b5c-166">For the left-button-up message, simply call [**ReleaseCapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) to release the mouse capture.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a><span data-ttu-id="e1b5c-167">Nächste</span><span class="sxs-lookup"><span data-stu-id="e1b5c-167">Next</span></span>

[<span data-ttu-id="e1b5c-168">Andere Maus Vorgänge</span><span class="sxs-lookup"><span data-stu-id="e1b5c-168">Other Mouse Operations</span></span>](other-mouse-operations.md)

 

 