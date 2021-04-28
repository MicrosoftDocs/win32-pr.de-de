---
<span data-ttu-id="4a6ec-101">title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018</span><span class="sxs-lookup"><span data-stu-id="4a6ec-101">title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018</span></span>
---

# <a name="user-input-extended-example"></a><span data-ttu-id="4a6ec-102">Benutzereingabe: Erweitertes Beispiel</span><span class="sxs-lookup"><span data-stu-id="4a6ec-102">User Input: Extended Example</span></span>

<span data-ttu-id="4a6ec-103">Kombinieren wir alles, was wir über Benutzereingaben gelernt haben, um ein einfaches Zeichenprogramm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-103">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="4a6ec-104">Hier sehen Sie einen Screenshot des Programms:</span><span class="sxs-lookup"><span data-stu-id="4a6ec-104">Here is a screen shot of the program:</span></span>

![Screenshot des Zeichenprogramms](images/input03.png)

<span data-ttu-id="4a6ec-106">Der Benutzer kann Ellipsen in verschiedenen Farben zeichnen und Ellipsen auswählen, verschieben oder löschen.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-106">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="4a6ec-107">Um die Benutzeroberfläche einfach zu halten, lässt das Programm nicht zu, dass der Benutzer die Ellipsefarben auswählt.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-107">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="4a6ec-108">Stattdessen durchkreist das Programm automatisch eine vordefinierte Liste von Farben.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-108">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="4a6ec-109">Das Programm unterstützt keine anderen Formen als Ellipsen.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-109">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="4a6ec-110">Natürlich wird dieses Programm keine Auszeichnungen für Grafiksoftware gewinnen.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-110">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="4a6ec-111">Es ist jedoch immer noch ein nützliches Beispiel, aus dem Sie lernen können.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-111">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="4a6ec-112">Sie können den vollständigen Quellcode unter [Simple Drawing Sample (Einfaches Zeichnungsbeispiel)](simple-drawing-sample.md)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-112">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="4a6ec-113">In diesem Abschnitt werden nur einige Highlights behandelt.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-113">This section will just cover some highlights.</span></span>

<span data-ttu-id="4a6ec-114">Ellipsen werden im Programm durch eine -Struktur dargestellt, die die Ellipsedaten ([**D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) und die Farbe ([**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)) enthält.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-114">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="4a6ec-115">Die -Struktur definiert auch zwei Methoden: eine Methode zum Zeichnen der Ellipse und eine Methode zum Ausführen von Treffertests.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-115">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


```C++
struct MyEllipse
{
    D2D1_ELLIPSE    ellipse;
    D2D1_COLOR_F    color;

    void Draw(ID2D1RenderTarget *pRT, ID2D1SolidColorBrush *pBrush)
    {
        pBrush->SetColor(color);
        pRT->FillEllipse(ellipse, pBrush);
        pBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black));
        pRT->DrawEllipse(ellipse, pBrush, 1.0f);
    }

    BOOL HitTest(float x, float y)
    {
        const float a = ellipse.radiusX;
        const float b = ellipse.radiusY;
        const float x1 = x - ellipse.point.x;
        const float y1 = y - ellipse.point.y;
        const float d = ((x1 * x1) / (a * a)) + ((y1 * y1) / (b * b));
        return d <= 1.0f;
    }
};
```



<span data-ttu-id="4a6ec-116">Das Programm verwendet den gleichen Volltonfarbpinsel, um die Füllung und Kontur für jede Ellipse zu zeichnen und die Farbe nach Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-116">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="4a6ec-117">In Direct2D ist das Ändern der Farbe eines Volltonfarbpinsels ein effizienter Vorgang.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-117">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="4a6ec-118">Das Pinselobjekt mit Volltonfarbe unterstützt daher eine [**SetColor-Methode.**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor)</span><span class="sxs-lookup"><span data-stu-id="4a6ec-118">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="4a6ec-119">Die Ellipsen werden in einem **STL-Listencontainer** gespeichert:</span><span class="sxs-lookup"><span data-stu-id="4a6ec-119">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="4a6ec-120">**shared \_ ptr** ist eine Intelligente-Zeiger-Klasse, die C++ in TR1 hinzugefügt und in C++0x formalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-120">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="4a6ec-121">Visual Studio 2010 fügt Unterstützung für **freigegebene \_ pt** r- und andere C++0x-Features hinzu.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-121">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="4a6ec-122">Weitere Informationen finden Sie unter [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-122">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="4a6ec-123">(Diese Ressource ist in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="4a6ec-123">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="4a6ec-124">Das Programm verfügt über drei Modi:</span><span class="sxs-lookup"><span data-stu-id="4a6ec-124">The program has three modes:</span></span>

-   <span data-ttu-id="4a6ec-125">Zeichnen-Modus.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-125">Draw mode.</span></span> <span data-ttu-id="4a6ec-126">Der Benutzer kann neue Ellipsen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-126">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="4a6ec-127">Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-127">Selection mode.</span></span> <span data-ttu-id="4a6ec-128">Der Benutzer kann eine Ellipse auswählen.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-128">The user can select an ellipse.</span></span>
-   <span data-ttu-id="4a6ec-129">Ziehmodus.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-129">Drag mode.</span></span> <span data-ttu-id="4a6ec-130">Der Benutzer kann eine ausgewählte Ellipse ziehen.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-130">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="4a6ec-131">Der Benutzer kann mithilfe der unter Zugriffstastentabellen beschriebenen Tastenkombinationen zwischen dem Draw-Modus und dem [Auswahlmodus wechseln.](accelerator-tables.md)</span><span class="sxs-lookup"><span data-stu-id="4a6ec-131">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="4a6ec-132">Im Auswahlmodus wechselt das Programm in den Ziehmodus, wenn der Benutzer auf eine Ellipse klickt.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-132">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="4a6ec-133">Sie wechselt wieder in den Auswahlmodus, wenn der Benutzer die Maustaste loslässt.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-133">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="4a6ec-134">Die aktuelle Auswahl wird als Iterator in der Liste der Ellipsen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-134">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="4a6ec-135">Die Hilfsmethode gibt einen Zeiger auf die ausgewählte Ellipse oder den Wert `MainWindow::Selection` **nullptr** zurück, wenn keine Auswahl besteht.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-135">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


```C++
    list<shared_ptr<MyEllipse>>::iterator   selection;
     
    shared_ptr<MyEllipse> Selection() 
    { 
        if (selection == ellipses.end()) 
        { 
            return nullptr;
        }
        else
        {
            return (*selection);
        }
    }

    void    ClearSelection() { selection = ellipses.end(); }
```



<span data-ttu-id="4a6ec-136">In der folgenden Tabelle sind die Auswirkungen der Mauseingabe in jedem der drei Modi zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-136">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="4a6ec-137">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="4a6ec-137">Mouse Input</span></span>      | <span data-ttu-id="4a6ec-138">Draw-Modus</span><span class="sxs-lookup"><span data-stu-id="4a6ec-138">Draw Mode</span></span>                                          | <span data-ttu-id="4a6ec-139">Auswahlmodus</span><span class="sxs-lookup"><span data-stu-id="4a6ec-139">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="4a6ec-140">Ziehmodus</span><span class="sxs-lookup"><span data-stu-id="4a6ec-140">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="4a6ec-141">Linke Schaltfläche nach unten</span><span class="sxs-lookup"><span data-stu-id="4a6ec-141">Left button down</span></span> | <span data-ttu-id="4a6ec-142">Legen Sie die Mauserfassung fest, und beginnen Sie, eine neue Ellipse zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-142">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="4a6ec-143">Geben Sie die aktuelle Auswahl frei, und führen Sie einen Treffertest aus.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-143">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="4a6ec-144">Wenn eine Ellipse erreicht wird, erfassen Sie den Cursor, wählen Sie die Ellipse aus, und wechseln Sie in den Ziehmodus.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-144">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="4a6ec-145">Keine Aktion.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-145">No action.</span></span>                 |
| <span data-ttu-id="4a6ec-146">Mauszeigerbewegungen</span><span class="sxs-lookup"><span data-stu-id="4a6ec-146">Mouse move</span></span>       | <span data-ttu-id="4a6ec-147">Wenn die linke Schaltfläche nicht angezeigt wird, ändern Sie die Größe der Ellipse.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-147">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="4a6ec-148">Keine Aktion.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-148">No action.</span></span>                                                                                                                                   | <span data-ttu-id="4a6ec-149">Verschieben Sie die ausgewählte Ellipse.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-149">Move the selected ellipse.</span></span> |
| <span data-ttu-id="4a6ec-150">Linke Schaltfläche nach oben</span><span class="sxs-lookup"><span data-stu-id="4a6ec-150">Left button up</span></span>   | <span data-ttu-id="4a6ec-151">Zeichnen Sie die Ellipse nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-151">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="4a6ec-152">Keine Aktion.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-152">No action.</span></span>                                                                                                                                   | <span data-ttu-id="4a6ec-153">Wechseln Sie in den Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-153">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="4a6ec-154">Die folgende Methode in der `MainWindow` -Klasse verarbeitet [**\_ WM-LBUTTONDOWN-Meldungen.**](/windows/desktop/inputdev/wm-lbuttondown)</span><span class="sxs-lookup"><span data-stu-id="4a6ec-154">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if (mode == DrawMode)
    {
        POINT pt = { pixelX, pixelY };

        if (DragDetect(m_hwnd, pt))
        {
            SetCapture(m_hwnd);
        
            // Start a new ellipse.
            InsertEllipse(dipX, dipY);
        }
    }
    else
    {
        ClearSelection();

        if (HitTest(dipX, dipY))
        {
            SetCapture(m_hwnd);

            ptMouse = Selection()->ellipse.point;
            ptMouse.x -= dipX;
            ptMouse.y -= dipY;

            SetMode(DragMode);
        }
    }
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



<span data-ttu-id="4a6ec-155">Mauskoordinaten werden in Pixel an diese Methode übergeben und dann in DIPs konvertiert.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-155">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="4a6ec-156">Es ist wichtig, diese beiden Einheiten nicht zu verwechseln.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-156">It is important not to confuse these two units.</span></span> <span data-ttu-id="4a6ec-157">Die [**DragDetect-Funktion**](/windows/desktop/api/winuser/nf-winuser-dragdetect) verwendet z. B. Pixel, aber Zeichnungs- und Treffertests verwenden DIPs.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-157">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="4a6ec-158">Die allgemeine Regel ist, dass Funktionen im Zusammenhang mit Fenster- oder Mauseingaben Pixel verwenden, während Direct2D und DirectWrite DIPs verwenden.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-158">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="4a6ec-159">Testen Sie Ihr Programm immer mit einer Einstellung mit hohem DPI-Anteil, und denken Sie daran, das Programm als DPI-fähiges Programm zu markieren.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-159">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="4a6ec-160">Weitere Informationen finden Sie unter [DPI und Device-Independent Pixel.](dpi-and-device-independent-pixels.md)</span><span class="sxs-lookup"><span data-stu-id="4a6ec-160">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="4a6ec-161">Hier ist der Code, der [**WM \_ MOUSEMOVE-Meldungen**](/windows/desktop/inputdev/wm-mousemove) verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-161">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


```C++
void MainWindow::OnMouseMove(int pixelX, int pixelY, DWORD flags)
{
    const float dipX = DPIScale::PixelsToDipsX(pixelX);
    const float dipY = DPIScale::PixelsToDipsY(pixelY);

    if ((flags & MK_LBUTTON) && Selection())
    { 
        if (mode == DrawMode)
        {
            // Resize the ellipse.
            const float width = (dipX - ptMouse.x) / 2;
            const float height = (dipY - ptMouse.y) / 2;
            const float x1 = ptMouse.x + width;
            const float y1 = ptMouse.y + height;

            Selection()->ellipse = D2D1::Ellipse(D2D1::Point2F(x1, y1), width, height);
        }
        else if (mode == DragMode)
        {
            // Move the ellipse.
            Selection()->ellipse.point.x = dipX + ptMouse.x;
            Selection()->ellipse.point.y = dipY + ptMouse.y;
        }
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
}
```



<span data-ttu-id="4a6ec-162">Die Logik zum Ändern der Größe einer Ellipse wurde zuvor im Abschnitt [Beispiel: Zeichnen](mouse-movement.md)von Kreisen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-162">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="4a6ec-163">Beachten Sie auch den Aufruf von [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span><span class="sxs-lookup"><span data-stu-id="4a6ec-163">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="4a6ec-164">Dadurch wird sichergestellt, dass das Fenster neu gepaint wird.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-164">This makes sure that the window is repainted.</span></span> <span data-ttu-id="4a6ec-165">Der folgende Code verarbeitet [**\_ WM-LBUTTONUP-Nachrichten.**](/windows/desktop/inputdev/wm-lbuttonup)</span><span class="sxs-lookup"><span data-stu-id="4a6ec-165">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


```C++
void MainWindow::OnLButtonUp()
{
    if ((mode == DrawMode) && Selection())
    {
        ClearSelection();
        InvalidateRect(m_hwnd, NULL, FALSE);
    }
    else if (mode == DragMode)
    {
        SetMode(SelectMode);
    }
    ReleaseCapture(); 
}
```



<span data-ttu-id="4a6ec-166">Wie Sie sehen können, verfügen die Meldungshandler für die Mauseingabe je nach aktuellem Modus über Verzweigungscode.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-166">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="4a6ec-167">Dies ist ein akzeptabler Entwurf für dieses recht einfache Programm.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-167">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="4a6ec-168">Es kann jedoch schnell zu komplex werden, wenn neue Modi hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-168">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="4a6ec-169">Bei einem größeren Programm ist eine MVC-Architektur (Model View Controller) möglicherweise ein besserer Entwurf.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-169">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="4a6ec-170">Bei dieser Art von Architektur ist der *Controller,* der Benutzereingaben verarbeitet, vom Modell *getrennt,* das Anwendungsdaten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-170">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="4a6ec-171">Wenn das Programm den Modus wechselt, ändert sich der Cursor, um dem Benutzer Feedback zu geben.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-171">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


```C++
void MainWindow::SetMode(Mode m)
{
    mode = m;

    // Update the cursor
    LPWSTR cursor;
    switch (mode)
    {
    case DrawMode:
        cursor = IDC_CROSS;
        break;

    case SelectMode:
        cursor = IDC_HAND;
        break;

    case DragMode:
        cursor = IDC_SIZEALL;
        break;
    }

    hCursor = LoadCursor(NULL, cursor);
    SetCursor(hCursor);
}
```



<span data-ttu-id="4a6ec-172">Denken Sie abschließend daran, den Cursor zu setzen, wenn das Fenster eine [**WM \_ SETCURSOR-Meldung empfängt:**](/windows/desktop/menurc/wm-setcursor)</span><span class="sxs-lookup"><span data-stu-id="4a6ec-172">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="4a6ec-173">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="4a6ec-173">Summary</span></span>

<span data-ttu-id="4a6ec-174">In diesem Modul haben Sie gelernt, wie Sie Maus- und Tastatureingaben verarbeiten. Definieren von Tastenkombinationen und wie das Cursorbild aktualisiert wird, um den aktuellen Zustand des Programms widerzubilden.</span><span class="sxs-lookup"><span data-stu-id="4a6ec-174">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 
