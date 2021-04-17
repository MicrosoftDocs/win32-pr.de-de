---
title: Erweitertes Beispiel für Benutzereingabe
description: .
ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdde7f14dda356d0f65103c77e3b73c2f0de50a6
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104558216"
---
# <a name="user-input-extended-example"></a><span data-ttu-id="0180c-103">Benutzereingabe: erweitertes Beispiel</span><span class="sxs-lookup"><span data-stu-id="0180c-103">User Input: Extended Example</span></span>

<span data-ttu-id="0180c-104">Wir kombinieren alles, was wir über Benutzereingaben gelernt haben, um ein einfaches Zeichnungsprogramm zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0180c-104">Let's combine everything that we have learned about user input to create a simple drawing program.</span></span> <span data-ttu-id="0180c-105">Im folgenden finden Sie einen Screenshot des Programms:</span><span class="sxs-lookup"><span data-stu-id="0180c-105">Here is a screen shot of the program:</span></span>

![Screenshot des Zeichnungs Programms](images/input03.png)

<span data-ttu-id="0180c-107">Der Benutzer kann Ellipsen in verschiedenen Farben zeichnen und Ellipsen auswählen, verschieben oder löschen.</span><span class="sxs-lookup"><span data-stu-id="0180c-107">The user can draw ellipses in several different colors, and select, move, or delete ellipses.</span></span> <span data-ttu-id="0180c-108">Um die Benutzeroberfläche auf dem neuesten Stand zu halten, lässt das Programm den Benutzer nicht zu, die Ellipse-Farben auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="0180c-108">To keep the UI simple, the program does not let the user select the ellipse colors.</span></span> <span data-ttu-id="0180c-109">Stattdessen durchläuft das Programm automatisch eine vordefinierte Liste von Farben.</span><span class="sxs-lookup"><span data-stu-id="0180c-109">Instead, the program automatically cycles through a predefined list of colors.</span></span> <span data-ttu-id="0180c-110">Das Programm unterstützt keine anderen Formen als Ellipsen.</span><span class="sxs-lookup"><span data-stu-id="0180c-110">The program does not support any shapes other than ellipses.</span></span> <span data-ttu-id="0180c-111">Natürlich gewinnt dieses Programm keine Auszeichnungen für Grafiksoftware.</span><span class="sxs-lookup"><span data-stu-id="0180c-111">Obviously, this program will not win any awards for graphics software.</span></span> <span data-ttu-id="0180c-112">Es ist jedoch immer noch ein nützliches Beispiel, aus dem Sie lernen können.</span><span class="sxs-lookup"><span data-stu-id="0180c-112">However, it is still a useful example to learn from.</span></span> <span data-ttu-id="0180c-113">Sie können den gesamten Quellcode von einem [einfachen Zeichnungs Beispiel](simple-drawing-sample.md)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="0180c-113">You can download the complete source code from [Simple Drawing Sample](simple-drawing-sample.md).</span></span> <span data-ttu-id="0180c-114">In diesem Abschnitt werden nur einige Highlights behandelt.</span><span class="sxs-lookup"><span data-stu-id="0180c-114">This section will just cover some highlights.</span></span>

<span data-ttu-id="0180c-115">Ellipsen werden im Programm durch eine Struktur dargestellt, die die Ellipse ([**D2D1 \_ Ellipse**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) und die Farbe ([**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)) enthält.</span><span class="sxs-lookup"><span data-stu-id="0180c-115">Ellipses are represented in the program by a structure that contains the ellipse data ([**D2D1\_ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) and the color ([**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f)).</span></span> <span data-ttu-id="0180c-116">Die Struktur definiert auch zwei Methoden: eine Methode zum Zeichnen der Ellipse und eine Methode zum Durchführen von Treffer Tests.</span><span class="sxs-lookup"><span data-stu-id="0180c-116">The structure also defines two methods: a method to draw the ellipse, and a method to perform hit testing.</span></span>


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



<span data-ttu-id="0180c-117">Das Programm verwendet denselben Pinsel mit voll Tonfarbe, um die Füllung und Gliederung für jede Ellipse zu zeichnen und die Farbe bei Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0180c-117">The program uses the same solid-color brush to draw the fill and outline for every ellipse, changing the color as needed.</span></span> <span data-ttu-id="0180c-118">In Direct2D ist das Ändern der Farbe eines vollfarbliche Pinsels ein effizienter Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0180c-118">In Direct2D, changing the color of a solid-color brush is an efficient operation.</span></span> <span data-ttu-id="0180c-119">Daher unterstützt das Vollbild-Pinsel Objekt eine [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) -Methode.</span><span class="sxs-lookup"><span data-stu-id="0180c-119">So, the solid-color brush object supports a [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) method.</span></span>

<span data-ttu-id="0180c-120">Die Ellipsen werden in einem STL- **Listen** Container gespeichert:</span><span class="sxs-lookup"><span data-stu-id="0180c-120">The ellipses are stored in an STL **list** container:</span></span>


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> <span data-ttu-id="0180c-121">**Shared \_ ptr** ist eine intelligente Zeiger Klasse, die C++ in TR1 hinzugefügt und in C + + 0x formalisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0180c-121">**shared\_ptr** is a smart-pointer class that was added to C++ in TR1 and formalized in C++0x.</span></span> <span data-ttu-id="0180c-122">Visual Studio 2010 fügt Unterstützung für frei **gegebene \_ PT** r und andere Features von C + + 0x hinzu.</span><span class="sxs-lookup"><span data-stu-id="0180c-122">Visual Studio 2010 adds support for **shared\_pt** r and other C++0x features.</span></span> <span data-ttu-id="0180c-123">Weitere Informationen finden Sie unter unter [Suchen neuer C++-und MFC-Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) im *MSDN Magazine*.</span><span class="sxs-lookup"><span data-stu-id="0180c-123">For more information, see [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*.</span></span> <span data-ttu-id="0180c-124">(Diese Ressource ist möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)</span><span class="sxs-lookup"><span data-stu-id="0180c-124">(This resource may not be available in some languages and countries.)</span></span>

 

<span data-ttu-id="0180c-125">Das Programm verfügt über drei Modi:</span><span class="sxs-lookup"><span data-stu-id="0180c-125">The program has three modes:</span></span>

-   <span data-ttu-id="0180c-126">Zeichnungsmodus.</span><span class="sxs-lookup"><span data-stu-id="0180c-126">Draw mode.</span></span> <span data-ttu-id="0180c-127">Der Benutzer kann neue Ellipsen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="0180c-127">The user can draw new ellipses.</span></span>
-   <span data-ttu-id="0180c-128">Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="0180c-128">Selection mode.</span></span> <span data-ttu-id="0180c-129">Der Benutzer kann eine Ellipse auswählen.</span><span class="sxs-lookup"><span data-stu-id="0180c-129">The user can select an ellipse.</span></span>
-   <span data-ttu-id="0180c-130">Ziehen Sie den Modus.</span><span class="sxs-lookup"><span data-stu-id="0180c-130">Drag mode.</span></span> <span data-ttu-id="0180c-131">Der Benutzer kann eine ausgewählte Ellipse ziehen.</span><span class="sxs-lookup"><span data-stu-id="0180c-131">The user can drag a selected ellipse.</span></span>

<span data-ttu-id="0180c-132">Der Benutzer kann mithilfe derselben Tastenkombinationen, die in Zugriffstasten [Tabellen](accelerator-tables.md)beschrieben werden, zwischen dem Zeichnungsmodus und dem Auswahlmodus wechseln.</span><span class="sxs-lookup"><span data-stu-id="0180c-132">The user can switch between draw mode and selection mode by using the same keyboard shortcuts described in [Accelerator Tables](accelerator-tables.md).</span></span> <span data-ttu-id="0180c-133">Im Auswahlmodus wechselt das Programm in den Zieh Modus, wenn der Benutzer auf eine Ellipse klickt.</span><span class="sxs-lookup"><span data-stu-id="0180c-133">From selection mode, the program switches to drag mode if the user clicks on an ellipse.</span></span> <span data-ttu-id="0180c-134">Wenn der Benutzer die Maustaste loslässt, wechselt er wieder in den Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="0180c-134">It switches back to selection mode when the user releases the mouse button.</span></span> <span data-ttu-id="0180c-135">Die aktuelle Auswahl wird als Iterator in der Liste der Ellipsen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="0180c-135">The current selection is stored as an iterator into the list of ellipses.</span></span> <span data-ttu-id="0180c-136">Die-Hilfsmethode `MainWindow::Selection` gibt einen Zeiger auf die ausgewählte Ellipse oder den Wert **nullptr** zurück, wenn keine Auswahl vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="0180c-136">The helper method `MainWindow::Selection` returns a pointer to the selected ellipse, or the value **nullptr** if there is no selection.</span></span>


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



<span data-ttu-id="0180c-137">In der folgenden Tabelle werden die Auswirkungen von Maus Eingaben in den drei Modi zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="0180c-137">The following table summarizes the effects of mouse input in each of the three modes.</span></span>



| <span data-ttu-id="0180c-138">Mauseingabe</span><span class="sxs-lookup"><span data-stu-id="0180c-138">Mouse Input</span></span>      | <span data-ttu-id="0180c-139">Zeichnungsmodus</span><span class="sxs-lookup"><span data-stu-id="0180c-139">Draw Mode</span></span>                                          | <span data-ttu-id="0180c-140">Auswahlmodus</span><span class="sxs-lookup"><span data-stu-id="0180c-140">Selection Mode</span></span>                                                                                                                               | <span data-ttu-id="0180c-141">Zieh Modus</span><span class="sxs-lookup"><span data-stu-id="0180c-141">Drag Mode</span></span>                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span data-ttu-id="0180c-142">Linke Schaltfläche nach unten</span><span class="sxs-lookup"><span data-stu-id="0180c-142">Left button down</span></span> | <span data-ttu-id="0180c-143">Legen Sie die Maus Aufzeichnung fest, und beginnen Sie mit dem Zeichnen einer neuen Ellipse.</span><span class="sxs-lookup"><span data-stu-id="0180c-143">Set mouse capture and start to draw a new ellipse.</span></span> | <span data-ttu-id="0180c-144">Gibt die aktuelle Auswahl frei und führt einen Treffer Test aus.</span><span class="sxs-lookup"><span data-stu-id="0180c-144">Release the current selection and perform a hit test.</span></span> <span data-ttu-id="0180c-145">Wenn eine Ellipse gedrückt wird, erfassen Sie den Cursor, wählen Sie die Ellipse aus, und wechseln Sie in den Zieh Modus.</span><span class="sxs-lookup"><span data-stu-id="0180c-145">If an ellipse is hit, capture the cursor, select the ellipse, and switch to drag mode.</span></span> | <span data-ttu-id="0180c-146">Keine Aktion.</span><span class="sxs-lookup"><span data-stu-id="0180c-146">No action.</span></span>                 |
| <span data-ttu-id="0180c-147">Mausbewegung</span><span class="sxs-lookup"><span data-stu-id="0180c-147">Mouse move</span></span>       | <span data-ttu-id="0180c-148">Wenn die linke Schaltfläche nicht angezeigt wird, ändern Sie die Größe der Ellipse.</span><span class="sxs-lookup"><span data-stu-id="0180c-148">If the left button is down, resize the ellipse.</span></span>    | <span data-ttu-id="0180c-149">Keine Aktion.</span><span class="sxs-lookup"><span data-stu-id="0180c-149">No action.</span></span>                                                                                                                                   | <span data-ttu-id="0180c-150">Verschiebt die ausgewählte Ellipse.</span><span class="sxs-lookup"><span data-stu-id="0180c-150">Move the selected ellipse.</span></span> |
| <span data-ttu-id="0180c-151">Linke Schaltfläche nach oben</span><span class="sxs-lookup"><span data-stu-id="0180c-151">Left button up</span></span>   | <span data-ttu-id="0180c-152">Das Zeichnen der Ellipse wird beendet.</span><span class="sxs-lookup"><span data-stu-id="0180c-152">Stop drawing the ellipse.</span></span>                          | <span data-ttu-id="0180c-153">Keine Aktion.</span><span class="sxs-lookup"><span data-stu-id="0180c-153">No action.</span></span>                                                                                                                                   | <span data-ttu-id="0180c-154">Wechseln Sie in den Auswahlmodus.</span><span class="sxs-lookup"><span data-stu-id="0180c-154">Switch to selection mode.</span></span>  |



 

<span data-ttu-id="0180c-155">Die folgende Methode in der- `MainWindow` Klasse behandelt [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Meldungen.</span><span class="sxs-lookup"><span data-stu-id="0180c-155">The following method in the `MainWindow` class handles [**WM\_LBUTTONDOWN**](/windows/desktop/inputdev/wm-lbuttondown) messages.</span></span>


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



<span data-ttu-id="0180c-156">Maus Koordinaten werden in Pixel an diese Methode übergeben und dann in Dips konvertiert.</span><span class="sxs-lookup"><span data-stu-id="0180c-156">Mouse coordinates are passed to this method in pixels, and then converted to DIPs.</span></span> <span data-ttu-id="0180c-157">Es ist wichtig, diese beiden Einheiten nicht zu verwechseln.</span><span class="sxs-lookup"><span data-stu-id="0180c-157">It is important not to confuse these two units.</span></span> <span data-ttu-id="0180c-158">Beispielsweise verwendet die [**dragdetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) -Funktion Pixel, aber Zeichnungs-und Treffer Tests verwenden Dips.</span><span class="sxs-lookup"><span data-stu-id="0180c-158">For example, the [**DragDetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) function uses pixels, but drawing and hit-testing use DIPs.</span></span> <span data-ttu-id="0180c-159">Die allgemeine Regel besteht darin, dass Funktionen für Windows-oder Maus Eingaben Pixel verwenden, während Direct2D und DirectWrite Dips verwenden.</span><span class="sxs-lookup"><span data-stu-id="0180c-159">The general rule is that functions related to windows or mouse input use pixels, while Direct2D and DirectWrite use DIPs.</span></span> <span data-ttu-id="0180c-160">Testen Sie Ihr Programm immer bei einer High-dpi-Einstellung, und denken Sie daran, Ihr Programm als dpi-fähig zu markieren.</span><span class="sxs-lookup"><span data-stu-id="0180c-160">Always test your program at a high-DPI setting, and remember to mark your program as DPI-aware.</span></span> <span data-ttu-id="0180c-161">Weitere Informationen finden Sie unter [dpi und Device-Independent Pixel](dpi-and-device-independent-pixels.md).</span><span class="sxs-lookup"><span data-stu-id="0180c-161">For more information, see [DPI and Device-Independent Pixels](dpi-and-device-independent-pixels.md).</span></span>

<span data-ttu-id="0180c-162">Dies ist der Code, der [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="0180c-162">Here is the code that handles [**WM\_MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) messages.</span></span>


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



<span data-ttu-id="0180c-163">Die Logik zur Größenänderung der Ellipse wurde zuvor im Abschnitt [Beispiel: Zeichnen von Kreisen](mouse-movement.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0180c-163">The logic to resize an ellipse was described previously, in the section [Example: Drawing Circles](mouse-movement.md).</span></span> <span data-ttu-id="0180c-164">Beachten Sie auch den- [**aufrufinvalidater.**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)</span><span class="sxs-lookup"><span data-stu-id="0180c-164">Also note the call to [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect).</span></span> <span data-ttu-id="0180c-165">Dadurch wird sichergestellt, dass das Fenster neu gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0180c-165">This makes sure that the window is repainted.</span></span> <span data-ttu-id="0180c-166">Der folgende Code verarbeitet die [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldungen.</span><span class="sxs-lookup"><span data-stu-id="0180c-166">The following code handles [**WM\_LBUTTONUP**](/windows/desktop/inputdev/wm-lbuttonup) messages.</span></span>


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



<span data-ttu-id="0180c-167">Wie Sie sehen können, haben die Meldungs Handler für die Mauseingabe alle Verzweigungs Codes, abhängig vom aktuellen Modus.</span><span class="sxs-lookup"><span data-stu-id="0180c-167">As you can see, the message handlers for mouse input all have branching code, depending on the current mode.</span></span> <span data-ttu-id="0180c-168">Das ist ein akzeptabler Entwurf für dieses Recht einfache Programm.</span><span class="sxs-lookup"><span data-stu-id="0180c-168">That is an acceptable design for this fairly simple program.</span></span> <span data-ttu-id="0180c-169">Es kann jedoch schnell zu komplex werden, wenn neue Modi hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="0180c-169">However, it could quickly become too complex if new modes are added.</span></span> <span data-ttu-id="0180c-170">Bei einem größeren Programm ist eine MVC-Architektur (Model-View-Controller) möglicherweise ein besseres Design.</span><span class="sxs-lookup"><span data-stu-id="0180c-170">For a larger program, a model-view-controller (MVC) architecture might be a better design.</span></span> <span data-ttu-id="0180c-171">Bei dieser Art von Architektur ist der *Controller*, der Benutzereingaben behandelt, vom *Modell* getrennt, das Anwendungsdaten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="0180c-171">In this kind of architecture, the *controller*, which handles user input, is separated from the *model*, which manages application data.</span></span>

<span data-ttu-id="0180c-172">Wenn das Programm die Modi wechselt, wird der Cursor geändert, um dem Benutzer Feedback zu geben.</span><span class="sxs-lookup"><span data-stu-id="0180c-172">When the program switches modes, the cursor changes to give feedback to the user.</span></span>


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



<span data-ttu-id="0180c-173">Und schließlich müssen Sie den Cursor festlegen, wenn das Fenster eine [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Nachricht empfängt:</span><span class="sxs-lookup"><span data-stu-id="0180c-173">And finally, remember to set the cursor when the window receives a [**WM\_SETCURSOR**](/windows/desktop/menurc/wm-setcursor) message:</span></span>


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a><span data-ttu-id="0180c-174">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="0180c-174">Summary</span></span>

<span data-ttu-id="0180c-175">In diesem Modul haben Sie gelernt, wie Maus-und Tastatureingaben behandelt werden. Definieren von Tastenkombinationen und wie das Cursor Bild aktualisiert wird, um den aktuellen Status des Programms widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="0180c-175">In this module, you learned how to handle mouse and keyboard input; how to define keyboard shortcuts; and how to update the cursor image to reflect the current state of the program.</span></span>

 

 