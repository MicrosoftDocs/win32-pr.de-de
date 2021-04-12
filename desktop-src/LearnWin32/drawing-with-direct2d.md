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
# <a name="drawing-with-direct2d"></a>Zeichnen mit Direct2D

Nachdem Sie Ihre Grafik Ressourcen erstellt haben, können Sie Sie zeichnen.

## <a name="drawing-an-ellipse"></a>Zeichnen einer Ellipse

Das [Circle](your-first-direct2d-program.md) -Programm führt eine sehr einfache Zeichnungs Logik durch:

1.  Füllen Sie den Hintergrund mit einer voll Tonfarbe aus.
2.  Zeichnen Sie einen gefüllten Kreis.

![ein Screenshot des Kreises-Programms.](images/graphics08.png)

Da das Renderziel ein Fenster ist (im Gegensatz zu einer Bitmap oder einer anderen Offscreen-Oberfläche), erfolgt das Zeichnen als Reaktion auf WM-Zeichnungs Meldungen. [**\_**](/windows/desktop/gdi/wm-paint) Der folgende Code zeigt die Fenster Prozedur für das kreisprogramm.


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

Hier ist der Code, der den Kreis zeichnet.

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



Die [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle wird für alle Zeichnungsvorgänge verwendet. Die-Methode des Programms `OnPaint` führt Folgendes aus:

1.  Die [**ID2D1RenderTarget:: beginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode signalisiert den Anfang der Zeichnung.
2.  Die [**ID2D1RenderTarget:: Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear) -Methode füllt das gesamte Renderziel mit einer voll Tonfarbe aus. Die Farbe wird als [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) -Struktur angegeben. Sie können die [**D2D1:: colorf**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) -Klasse verwenden, um die Struktur zu initialisieren. Weitere Informationen finden Sie unter [Verwenden von Color in Direct2D](using-color-in-direct2d.md).
3.  Die [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) -Methode zeichnet eine gefüllte Ellipse mit dem angegebenen Pinsel für die Füllung. Eine Ellipse wird von einem Mittelpunkt und dem x-und y-Radii angegeben. Wenn x-und y-Radii identisch sind, ist das Ergebnis ein Kreis.
4.  Die [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode signalisiert den Abschluss der Zeichnung für diesen Frame. Alle Zeichnungsvorgänge müssen zwischen Aufrufen von [**beginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und **EndDraw** eingefügt werden.

Die [**beginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)-, [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)-und [**FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) -Methoden verfügen alle über einen **void** -Rückgabetyp. Wenn während der Ausführung einer dieser Methoden ein Fehler auftritt, wird der Fehler durch den Rückgabewert der [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode signalisiert. Die- `CreateGraphicsResources` Methode wird im Thema [Erstellen von Direct2D-Ressourcen](render-targets--devices--and-resources.md)gezeigt. Diese Methode erstellt das Renderziel und den Pinsel mit voll Tonfarbe.

Das Gerät puffert möglicherweise die Zeichnungs Befehle und verzögert die Ausführung, bis [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) aufgerufen wird. Sie können erzwingen, dass das Gerät ausstehende Zeichnungs Befehle ausführt, indem Sie [**ID2D1RenderTarget:: Flush**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush)aufrufen. Das leeren kann jedoch die Leistung beeinträchtigen.

## <a name="handling-device-loss"></a>Behandeln von Geräte Verlusten

Während das Programm ausgeführt wird, ist das verwendete Grafikgerät möglicherweise nicht mehr verfügbar. Beispielsweise kann das Gerät verloren gehen, wenn sich die Bildschirmauflösung ändert, oder wenn der Benutzer den Anzeige Adapter entfernt. Wenn das Gerät verloren geht, wird auch das Renderziel zusammen mit allen geräteabhängigen Ressourcen, die dem Gerät zugeordnet sind, ungültig. Direct2D signalisiert einem verlorenen Gerät durch das Zurückgeben des Fehlercodes **D2DERR " \_ \_ Ziel neu erstellen** " aus der [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode. Wenn Sie diesen Fehlercode erhalten, müssen Sie das Renderziel und alle geräteabhängigen Ressourcen neu erstellen.

Um eine Ressource zu verwerfen, geben Sie einfach die Schnittstelle für diese Ressource frei.


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



Das Erstellen einer Ressource kann ein kostspieliger Vorgang sein. Erstellen Sie daher ihre Ressourcen nicht für jede WM-Zeichnungs Nachricht neu. [**\_**](/windows/desktop/gdi/wm-paint) Erstellen Sie eine Ressource einmal, und speichern Sie den Ressourcen Zeiger zwischen, bis die Ressource aufgrund eines Geräte Verlusts ungültig wird oder wenn Sie diese Ressource nicht mehr benötigen.

## <a name="the-direct2d-render-loop"></a>Die Direct2D-Renderschleife

Unabhängig davon, was Sie zeichnen, sollte das Programm eine Schleife ähnlich der folgenden ausführen.

1.  Geräteunabhängige Ressourcen erstellen.
2.  Rendering der Szene.
    1.  Prüfen Sie, ob ein gültiges Renderziel vorhanden ist. Wenn dies nicht der Wert ist, erstellen Sie das Renderziel und die geräteabhängigen Ressourcen.
    2.  Aufrufen von [**ID2D1RenderTarget:: beginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw).
    3.  Ausstellen von Zeichnungs Befehlen.
    4.  Aufrufen von [**ID2D1RenderTarget:: EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).
    5.  Wenn [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) das **D2DERR \_ - \_ Ziel neu erstellen** zurückgibt, verwerfen Sie das Renderziel und Geräte abhängige Ressourcen.
3.  Wiederholen Sie Schritt 2, wenn Sie die Szene aktualisieren oder neu zeichnen müssen.

Wenn das Renderziel ein Fenster ist, tritt Schritt 2 auf, wenn das Fenster eine [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung empfängt.

In der hier gezeigten Schleife werden Geräte Verluste behandelt, indem die geräteabhängigen Ressourcen verworfen und zu Beginn der nächsten Schleife neu erstellt werden (Schritt 2a).

## <a name="next"></a>Nächste

[DPI-und Device-Independent Pixel](dpi-and-device-independent-pixels.md)

 

 