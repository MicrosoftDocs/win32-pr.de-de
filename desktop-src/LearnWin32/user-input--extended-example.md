---
title: User Input Extended Example description: User Input: Extended Example ms.assetid: A408E0EC-E0A7-4F18-BFCA-21D28007FACC ms.topic: article ms.date: 05/31/2018
---

# <a name="user-input-extended-example"></a>Benutzereingabe: Erweitertes Beispiel

Kombinieren wir alles, was wir über Benutzereingaben gelernt haben, um ein einfaches Zeichenprogramm zu erstellen. Hier sehen Sie einen Screenshot des Programms:

![Screenshot des Zeichnungsprogramms](images/input03.png)

Der Benutzer kann Ellipsen in verschiedenen Farben zeichnen und Ellipsen auswählen, verschieben oder löschen. Um die Benutzeroberfläche einfach zu halten, lässt das Programm nicht zu, dass der Benutzer die Ellipsefarben auswählt. Stattdessen durchkreist das Programm automatisch eine vordefinierte Liste von Farben. Das Programm unterstützt keine anderen Formen als Ellipsen. Natürlich wird dieses Programm keine Auszeichnungen für Grafiksoftware gewinnen. Es ist jedoch immer noch ein nützliches Beispiel, aus dem Sie lernen können. Sie können den vollständigen Quellcode unter [Simple Drawing Sample (Einfaches Zeichnungsbeispiel)](simple-drawing-sample.md)herunterladen. In diesem Abschnitt werden nur einige Highlights behandelt.

Ellipsen werden im Programm durch eine -Struktur dargestellt, die die Ellipsedaten ([**D2D1 \_ ELLIPSE**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) und die Farbe ([**D2D1 \_ COLOR \_ F**](/windows/desktop/Direct2D/d2d1-color-f)) enthält. Die -Struktur definiert auch zwei Methoden: eine Methode zum Zeichnen der Ellipse und eine Methode zum Ausführen von Treffertests.


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



Das Programm verwendet den gleichen Volltonfarbpinsel, um die Füllung und Kontur für jede Ellipse zu zeichnen und die Farbe nach Bedarf zu ändern. In Direct2D ist das Ändern der Farbe eines Volltonfarbpinsels ein effizienter Vorgang. Das Pinselobjekt mit Volltonfarbe unterstützt daher eine [**SetColor-Methode.**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor)

Die Ausellipsen werden in einem **STL-Listencontainer** gespeichert:


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **shared \_ ptr** ist eine Intelligente-Zeiger-Klasse, die C++ in TR1 hinzugefügt und in C++0x formalisiert wurde. Visual Studio 2010 bietet Unterstützung für **\_ freigegebene pt** r- und andere C++0x-Features. Weitere Informationen finden Sie unter [Exploring New C++ and MFC Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) in *MSDN Magazine*. (Diese Ressource ist in einigen Sprachen und Ländern möglicherweise nicht verfügbar.)

 

Das Programm verfügt über drei Modi:

-   Draw-Modus. Der Benutzer kann neue Ausellipsen zeichnen.
-   Auswahlmodus. Der Benutzer kann eine Ellipse auswählen.
-   Ziehmodus. Der Benutzer kann eine ausgewählte Ellipse ziehen.

Der Benutzer kann zwischen dem Draw-Modus und dem Auswahlmodus wechseln, indem er die gleichen Tastenkombinationen verwendet, die unter [Zugriffstastentabellen](accelerator-tables.md)beschrieben sind. Aus dem Auswahlmodus wechselt das Programm in den Ziehmodus, wenn der Benutzer auf eine Ellipse klickt. Er wechselt zurück in den Auswahlmodus, wenn der Benutzer die Maustaste freigibt. Die aktuelle Auswahl wird als Iterator in der Liste der Auslassungszeichen gespeichert. Die Hilfsmethode `MainWindow::Selection` gibt einen Zeiger auf die ausgewählte Ellipse oder den Wert **nullptr** zurück, wenn keine Auswahl vorhanden ist.


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



In der folgenden Tabelle sind die Auswirkungen von Mauseingaben in jedem der drei Modi zusammengefasst.



| Mauseingabe      | Zeichnen-Modus                                          | Auswahlmodus                                                                                                                               | Ziehmodus                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Linke Schaltfläche nach unten | Legen Sie die Mauserfassung fest, und beginnen Sie, eine neue Ellipse zu zeichnen. | Geben Sie die aktuelle Auswahl frei, und führen Sie einen Treffertest aus. Wenn eine Ellipse erreicht wird, erfassen Sie den Cursor, wählen Sie die Ellipse aus, und wechseln Sie in den Ziehmodus. | Keine Aktion.                 |
| Mauszeigerbewegungen       | Wenn die linke Schaltfläche ausgeschaltet ist, ändern Sie die Größe der Ellipse.    | Keine Aktion.                                                                                                                                   | Verschieben Sie die ausgewählte Ellipse. |
| Linke Schaltfläche nach oben   | Zeichnen Sie die Ellipse nicht mehr.                          | Keine Aktion.                                                                                                                                   | Wechseln Sie in den Auswahlmodus.  |



 

Die folgende Methode in der `MainWindow` -Klasse verarbeitet [**\_ WM-LBUTTONDOWN-Meldungen.**](/windows/desktop/inputdev/wm-lbuttondown)


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



Mauskoordinaten werden in Pixel an diese Methode übergeben und dann in DIPs konvertiert. Es ist wichtig, diese beiden Einheiten nicht zu verwechseln. Die [**DragDetect-Funktion**](/windows/desktop/api/winuser/nf-winuser-dragdetect) verwendet z. B. Pixel, aber Zeichnungs- und Treffertests verwenden DIPs. Die allgemeine Regel ist, dass Funktionen im Zusammenhang mit Fenster- oder Mauseingaben Pixel verwenden, während Direct2D und DirectWrite DIPs verwenden. Testen Sie Ihr Programm immer mit einer Einstellung mit hohem DPI-Anteil, und denken Sie daran, das Programm als DPI-fähiges Programm zu markieren. Weitere Informationen finden Sie unter [DPI und Device-Independent Pixel.](dpi-and-device-independent-pixels.md)

Hier ist der Code, der [**WM \_ MOUSEMOVE-Meldungen**](/windows/desktop/inputdev/wm-mousemove) verarbeitet.


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



Die Logik zum Ändern der Größe einer Ellipse wurde zuvor im Abschnitt [Beispiel: Zeichnen](mouse-movement.md)von Kreisen beschrieben. Beachten Sie auch den Aufruf von [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Dadurch wird sichergestellt, dass das Fenster neu lackiert wird. Der folgende Code verarbeitet [**\_ WM-LBUTTONUP-Nachrichten.**](/windows/desktop/inputdev/wm-lbuttonup)


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



Wie Sie sehen können, verfügen die Meldungshandler für Mauseingaben je nach aktuellem Modus über Verzweigungscode. Dies ist ein akzeptabler Entwurf für dieses recht einfache Programm. Es kann jedoch schnell zu komplex werden, wenn neue Modi hinzugefügt werden. Für ein größeres Programm kann eine MVC-Architektur (Model View Controller) ein besserer Entwurf sein. Bei dieser Art von Architektur ist der *Controller,* der Benutzereingaben verarbeitet, vom *Modell* getrennt, das Anwendungsdaten verwaltet.

Wenn das Programm den Modus wechselt, ändert sich der Cursor, um dem Benutzer Feedback zu geben.


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



Denken Sie abschließend daran, den Cursor festzulegen, wenn das Fenster eine [**WM \_ SETCURSOR-Meldung**](/windows/desktop/menurc/wm-setcursor) empfängt:


```C++
    case WM_SETCURSOR:
        if (LOWORD(lParam) == HTCLIENT)
        {
            SetCursor(hCursor);
            return TRUE;
        }
        break;
```



## <a name="summary"></a>Zusammenfassung

In diesem Modul haben Sie gelernt, wie Maus- und Tastatureingaben behandelt werden. Definieren von Tastenkombinationen und wie das Cursorbild aktualisiert wird, um den aktuellen Zustand des Programms widerzuspiegeln.

 

 
