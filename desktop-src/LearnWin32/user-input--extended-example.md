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
# <a name="user-input-extended-example"></a>Benutzereingabe: erweitertes Beispiel

Wir kombinieren alles, was wir über Benutzereingaben gelernt haben, um ein einfaches Zeichnungsprogramm zu erstellen. Im folgenden finden Sie einen Screenshot des Programms:

![Screenshot des Zeichnungs Programms](images/input03.png)

Der Benutzer kann Ellipsen in verschiedenen Farben zeichnen und Ellipsen auswählen, verschieben oder löschen. Um die Benutzeroberfläche auf dem neuesten Stand zu halten, lässt das Programm den Benutzer nicht zu, die Ellipse-Farben auszuwählen. Stattdessen durchläuft das Programm automatisch eine vordefinierte Liste von Farben. Das Programm unterstützt keine anderen Formen als Ellipsen. Natürlich gewinnt dieses Programm keine Auszeichnungen für Grafiksoftware. Es ist jedoch immer noch ein nützliches Beispiel, aus dem Sie lernen können. Sie können den gesamten Quellcode von einem [einfachen Zeichnungs Beispiel](simple-drawing-sample.md)herunterladen. In diesem Abschnitt werden nur einige Highlights behandelt.

Ellipsen werden im Programm durch eine Struktur dargestellt, die die Ellipse ([**D2D1 \_ Ellipse**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_ellipse)) und die Farbe ([**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f)) enthält. Die Struktur definiert auch zwei Methoden: eine Methode zum Zeichnen der Ellipse und eine Methode zum Durchführen von Treffer Tests.


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



Das Programm verwendet denselben Pinsel mit voll Tonfarbe, um die Füllung und Gliederung für jede Ellipse zu zeichnen und die Farbe bei Bedarf zu ändern. In Direct2D ist das Ändern der Farbe eines vollfarbliche Pinsels ein effizienter Vorgang. Daher unterstützt das Vollbild-Pinsel Objekt eine [**SetColor**](/windows/desktop/Direct2D/id2d1solidcolorbrush-setcolor) -Methode.

Die Ellipsen werden in einem STL- **Listen** Container gespeichert:


```C++
    list<shared_ptr<MyEllipse>>             ellipses;
```



> [!Note]  
> **Shared \_ ptr** ist eine intelligente Zeiger Klasse, die C++ in TR1 hinzugefügt und in C + + 0x formalisiert wurde. Visual Studio 2010 fügt Unterstützung für frei **gegebene \_ PT** r und andere Features von C + + 0x hinzu. Weitere Informationen finden Sie unter unter [Suchen neuer C++-und MFC-Features in Visual Studio 2010](/archive/msdn-magazine/2010/april/visual-c-exploring-new-c-and-mfc-features-in-visual-studio-2010) im *MSDN Magazine*. (Diese Ressource ist möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)

 

Das Programm verfügt über drei Modi:

-   Zeichnungsmodus. Der Benutzer kann neue Ellipsen zeichnen.
-   Auswahlmodus. Der Benutzer kann eine Ellipse auswählen.
-   Ziehen Sie den Modus. Der Benutzer kann eine ausgewählte Ellipse ziehen.

Der Benutzer kann mithilfe derselben Tastenkombinationen, die in Zugriffstasten [Tabellen](accelerator-tables.md)beschrieben werden, zwischen dem Zeichnungsmodus und dem Auswahlmodus wechseln. Im Auswahlmodus wechselt das Programm in den Zieh Modus, wenn der Benutzer auf eine Ellipse klickt. Wenn der Benutzer die Maustaste loslässt, wechselt er wieder in den Auswahlmodus. Die aktuelle Auswahl wird als Iterator in der Liste der Ellipsen gespeichert. Die-Hilfsmethode `MainWindow::Selection` gibt einen Zeiger auf die ausgewählte Ellipse oder den Wert **nullptr** zurück, wenn keine Auswahl vorhanden ist.


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



In der folgenden Tabelle werden die Auswirkungen von Maus Eingaben in den drei Modi zusammengefasst.



| Mauseingabe      | Zeichnungsmodus                                          | Auswahlmodus                                                                                                                               | Zieh Modus                  |
|------------------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| Linke Schaltfläche nach unten | Legen Sie die Maus Aufzeichnung fest, und beginnen Sie mit dem Zeichnen einer neuen Ellipse. | Gibt die aktuelle Auswahl frei und führt einen Treffer Test aus. Wenn eine Ellipse gedrückt wird, erfassen Sie den Cursor, wählen Sie die Ellipse aus, und wechseln Sie in den Zieh Modus. | Keine Aktion.                 |
| Mausbewegung       | Wenn die linke Schaltfläche nicht angezeigt wird, ändern Sie die Größe der Ellipse.    | Keine Aktion.                                                                                                                                   | Verschiebt die ausgewählte Ellipse. |
| Linke Schaltfläche nach oben   | Das Zeichnen der Ellipse wird beendet.                          | Keine Aktion.                                                                                                                                   | Wechseln Sie in den Auswahlmodus.  |



 

Die folgende Methode in der- `MainWindow` Klasse behandelt [**WM \_ lbuttondown**](/windows/desktop/inputdev/wm-lbuttondown) -Meldungen.


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



Maus Koordinaten werden in Pixel an diese Methode übergeben und dann in Dips konvertiert. Es ist wichtig, diese beiden Einheiten nicht zu verwechseln. Beispielsweise verwendet die [**dragdetect**](/windows/desktop/api/winuser/nf-winuser-dragdetect) -Funktion Pixel, aber Zeichnungs-und Treffer Tests verwenden Dips. Die allgemeine Regel besteht darin, dass Funktionen für Windows-oder Maus Eingaben Pixel verwenden, während Direct2D und DirectWrite Dips verwenden. Testen Sie Ihr Programm immer bei einer High-dpi-Einstellung, und denken Sie daran, Ihr Programm als dpi-fähig zu markieren. Weitere Informationen finden Sie unter [dpi und Device-Independent Pixel](dpi-and-device-independent-pixels.md).

Dies ist der Code, der [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten verarbeitet.


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



Die Logik zur Größenänderung der Ellipse wurde zuvor im Abschnitt [Beispiel: Zeichnen von Kreisen](mouse-movement.md)beschrieben. Beachten Sie auch den- [**aufrufinvalidater.**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) Dadurch wird sichergestellt, dass das Fenster neu gezeichnet wird. Der folgende Code verarbeitet die [**WM \_ lbuttonup**](/windows/desktop/inputdev/wm-lbuttonup) -Meldungen.


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



Wie Sie sehen können, haben die Meldungs Handler für die Mauseingabe alle Verzweigungs Codes, abhängig vom aktuellen Modus. Das ist ein akzeptabler Entwurf für dieses Recht einfache Programm. Es kann jedoch schnell zu komplex werden, wenn neue Modi hinzugefügt werden. Bei einem größeren Programm ist eine MVC-Architektur (Model-View-Controller) möglicherweise ein besseres Design. Bei dieser Art von Architektur ist der *Controller*, der Benutzereingaben behandelt, vom *Modell* getrennt, das Anwendungsdaten verwaltet.

Wenn das Programm die Modi wechselt, wird der Cursor geändert, um dem Benutzer Feedback zu geben.


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



Und schließlich müssen Sie den Cursor festlegen, wenn das Fenster eine [**WM- \_ SetCursor**](/windows/desktop/menurc/wm-setcursor) -Nachricht empfängt:


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

In diesem Modul haben Sie gelernt, wie Maus-und Tastatureingaben behandelt werden. Definieren von Tastenkombinationen und wie das Cursor Bild aktualisiert wird, um den aktuellen Status des Programms widerzuspiegeln.

 

 