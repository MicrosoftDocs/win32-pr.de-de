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
# <a name="mouse-movement"></a>Mausbewegung

Wenn die Maus bewegt wird, stellt Windows eine [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht zur Folge. Standardmäßig wechselt der **WM- \_ mousetmove** -Vorgang in das Fenster, das den Cursor enthält. Sie können dieses Verhalten überschreiben, indem Sie die Maus *erfassen* , die im nächsten Abschnitt beschrieben wird.

Die [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht enthält die gleichen Parameter wie die Meldungen für Mausklicks. Die niedrigsten 16 Bits von *LPARAM* enthalten die x-Koordinate, und die nächsten 16 Bits enthalten die y-Koordinate. Verwenden Sie die lParam-Makros [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) , um die Koordinaten aus *LPARAM* zu entpacken. Der *wParam* -Parameter enthält ein bitweises **or** von-Flags, das den Zustand der anderen Maustasten sowie die UMSCHALTTASTE und die STRG-Taste angibt. Der folgende Code Ruft die Maus Koordinaten aus *LPARAM* ab.


```C++
int xPos = GET_X_LPARAM(lParam); 
int yPos = GET_Y_LPARAM(lParam);
```



Beachten Sie, dass sich diese Koordinaten in Pixel befinden, nicht in geräteunabhängigen Pixeln (Dips). Weiter unten in diesem Thema betrachten wir den Code, der zwischen den beiden Einheiten konvertiert.

Ein Fenster kann auch eine [**WM- \_ mousetmove**](/windows/desktop/inputdev/wm-mousemove) -Nachricht empfangen, wenn die Position des Cursors relativ zum Fenster geändert wird. Wenn der Cursor z. b. auf einem Fenster positioniert ist und der Benutzer das Fenster verbirgt, empfängt das Fenster **WM- \_ MouseMove** -Meldungen, auch wenn die Maus nicht verschoben wurde. Eine Folge dieses Verhaltens besteht darin, dass sich die Maus Koordinaten zwischen den **WM- \_ MouseMove** -Meldungen möglicherweise nicht ändern.

## <a name="capturing-mouse-movement-outside-the-window"></a>Erfassen der Mausbewegung außerhalb des Fensters

Standardmäßig beendet ein Fenster den Empfang von [**WM- \_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten, wenn die Maus über den Rand des Client Bereichs bewegt wird. Für einige Vorgänge müssen Sie jedoch möglicherweise die Mausposition hinter diesem Punkt nachverfolgen. Beispielsweise kann ein Zeichnungsprogramm es dem Benutzer ermöglichen, das Auswahl Rechteck über den Rand des Fensters hinaus zu ziehen, wie im folgenden Diagramm dargestellt.

![eine Abbildung der Maus Aufzeichnung.](images/input01.png)

Um Nachrichten mit Mauszeiger über den Rand des Fensters zu empfangen, müssen Sie die Funktion [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) aufrufen. Nachdem diese Funktion aufgerufen wurde, empfängt das Fenster weiterhin WM- [**\_ MouseMove**](/windows/desktop/inputdev/wm-mousemove) -Nachrichten, solange der Benutzer mindestens eine Maustaste gedrückt hält, auch wenn der Mauszeiger außerhalb des Fensters bewegt wird. Das Erfassungsfenster muss das Vordergrund Fenster sein, und nur ein Fenster kann das Erfassungsfenster gleichzeitig sein. Um die Maus Aufzeichnung freizugeben, nennen Sie die [**releasecapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) -Funktion.

In der Regel verwenden Sie [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) und [**releasecapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) wie folgt.

1.  Wenn der Benutzer die linke Maustaste drückt, wird [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) aufgerufen, um mit dem Erfassen der Maus zu beginnen.
2.  Reagieren auf Maus Verschiebungs Meldungen.
3.  Wenn der Benutzer die linke Maustaste loslässt, wird [**releasecapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture)aufgerufen.

## <a name="example-drawing-circles"></a>Beispiel: Zeichnen von Kreisen

Erweitern Sie nun das kreisprogramm von [Modul 3](module-3---windows-graphics.md) , indem Sie dem Benutzer das Zeichnen eines Kreises mit der Maus ermöglichen. Beginnen Sie mit dem [Direct2D Circle-Beispiel](direct2d-circle-sample.md) Programm. Wir ändern den Code in diesem Beispiel, um einfache Zeichnung hinzuzufügen. Fügen Sie zunächst der-Klasse eine neue Member-Variable hinzu `MainWindow` .


```C++
    D2D1_POINT_2F           ptMouse;
```



Diese Variable speichert die Maustaste, während der Benutzer die Maus zieht. `MainWindow`Initialisieren Sie im Konstruktor die Variablen *Ellipse* und *ptmouse* .


```C++
    MainWindow() : pFactory(NULL), pRenderTarget(NULL), pBrush(NULL),
        ellipse(D2D1::Ellipse(D2D1::Point2F(), 0, 0)),
        ptMouse(D2D1::Point2F())
    {
    }
```



Entfernen Sie den Text der- `MainWindow::CalculateLayout` Methode. Dies ist für dieses Beispiel nicht erforderlich.


```C++
    void    CalculateLayout() { }
```



Deklarieren Sie anschließend die Meldungs Handler für die nach-unten-Taste, die nach-links-Taste und die Maus Verschiebungs Meldungen.


```C++
    void    OnLButtonDown(int pixelX, int pixelY, DWORD flags);
    void    OnLButtonUp();
    void    OnMouseMove(int pixelX, int pixelY, DWORD flags);
```



Maus Koordinaten werden in physischen Pixeln angegeben, aber Direct2D erwartet geräteunabhängige Pixel (Dips). Um die Einstellungen für hohe DPI-Einstellungen ordnungsgemäß zu verarbeiten, müssen Sie die Pixelkoordinaten in Dips übersetzen. Weitere Informationen zu dpi finden Sie unter [dpi und Device-Independent Pixel](dpi-and-device-independent-pixels.md). Der folgende Code zeigt eine Hilfsklasse, die Pixel in Dips konvertiert.


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



Rufen `DPIScale::Initialize` Sie in Ihrem [**WM \_ Create**](/windows/desktop/winmsg/wm-create) -Handler auf, nachdem Sie das Direct2D Factory-Objekt erstellt haben.


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



Gehen Sie folgendermaßen vor, um die Maus Koordinaten in Dips aus den Maus Meldungen abzurufen:

1.  Verwenden Sie die lParam-Makros [**get \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam) und [**get \_ Y \_**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam) , um die Pixelkoordinaten zu erhalten. Diese Makros sind in WINDOWSX. h definiert. denken Sie daher daran, diesen Header in das Projekt einzubeziehen.
2.  `DPIScale::PixelsToDipsX`Mit und können Sie `DPIScale::PixelsToDipsY` Pixel in Dips konvertieren.

Fügen Sie nun die Meldungs Handler ihrer Fenster Prozedur hinzu.


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



Implementieren Sie schließlich die Nachrichten Handler selbst.

### <a name="left-button-down"></a>Linke Schaltfläche nach unten

Führen Sie für die nach-links-Taste folgende Schritte aus:

1.  Ruft [**SetCapture**](/windows/desktop/api/winuser/nf-winuser-setcapture) auf, um mit dem Erfassen der Maus zu beginnen.
2.  Speichert die Position des Mausklicks in der *ptmouse* -Variablen. Diese Position definiert die linke obere Ecke des umgebenden Felds für die Ellipse.
3.  Setzen Sie die Ellipse-Struktur zurück.
4.  Wenden Sie sich an [**invalidatup**](/windows/desktop/api/winuser/nf-winuser-invalidaterect). Diese Funktion erzwingt, dass das Fenster neu gezeichnet wird.


```C++
void MainWindow::OnLButtonDown(int pixelX, int pixelY, DWORD flags)
{
    SetCapture(m_hwnd);
    ellipse.point = ptMouse = DPIScale::PixelsToDips(pixelX, pixelY);
    ellipse.radiusX = ellipse.radiusY = 1.0f; 
    InvalidateRect(m_hwnd, NULL, FALSE);
}
```



### <a name="mouse-move"></a>Mausbewegung

Überprüfen Sie für die Maus Verschiebungs Meldung, ob die linke Maustaste gedrückt ist. Wenn dies der Fall ist, berechnen Sie die Ellipse neu, und zeichnen Sie das Fenster neu. In Direct2D wird eine Ellipse durch den Mittelpunkt und x-und y-Radii definiert. Wir möchten eine Ellipse zeichnen, die dem umgebenden Feld entspricht, das durch den MouseDown-Punkt (*ptmouse*) und die aktuelle Cursorposition (*x*, *y*) definiert wird. Daher ist ein wenig arithmetischer Wert erforderlich, um die Breite, Höhe und Position der Ellipse zu finden.

Der folgende Code berechnet die Ellipse neu und ruft dann [**invalidateriert**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) auf, um das Fenster neu zu zeichnen.

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



### <a name="left-button-up"></a>Linke Schaltfläche nach oben

Wenn Sie die nach-oben-Taste drücken, nennen Sie einfach [**releasecapture**](/windows/desktop/api/winuser/nf-winuser-releasecapture) , um die Maus Aufzeichnung freizugeben.


```C++
void MainWindow::OnLButtonUp()
{
    ReleaseCapture(); 
}
```



## <a name="next"></a>Nächste

[Andere Maus Vorgänge](other-mouse-operations.md)

 

 