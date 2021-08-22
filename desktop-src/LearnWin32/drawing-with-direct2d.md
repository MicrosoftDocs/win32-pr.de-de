---
title: Zeichnen mit Direct2D
description: Nachdem Sie Ihre Grafikressourcen erstellt haben, können Sie zeichnen.
ms.assetid: a73f7043-dffc-4688-adfc-16ed9a9e12d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d8a346300b32fe1c716e51efe6bfb8fdbf6220fb2ff17df6de617de27ba1a8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535075"
---
# <a name="drawing-with-direct2d"></a>Zeichnen mit Direct2D

Nachdem Sie Ihre Grafikressourcen erstellt haben, können Sie zeichnen.

## <a name="drawing-an-ellipse"></a>Zeichnen einer Ellipse

Das [Circle-Programm](your-first-direct2d-program.md) führt eine sehr einfache Zeichnungslogik aus:

1.  Füllen Sie den Hintergrund mit einer Volltonfarbe aus.
2.  Zeichnen Sie einen ausgefüllten Kreis.

![Ein Screenshot des Kreisprogramms.](images/graphics08.png)

Da das Renderziel ein Fenster ist (im Gegensatz zu einer Bitmap oder einer anderen Offscreenoberfläche), erfolgt das Zeichnen als Reaktion auf [**WM \_ PAINT-Meldungen.**](/windows/desktop/gdi/wm-paint) Der folgende Code zeigt die Fensterprozedur für das Circle-Programm.


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



Die [**ID2D1RenderTarget-Schnittstelle**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) wird für alle Zeichnungsvorgänge verwendet. Die -Methode `OnPaint` des Programms führt Folgendes aus:

1.  Die [**ID2D1RenderTarget::BeginDraw-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) signalisiert den Beginn des Zeichnens.
2.  Die [**ID2D1RenderTarget::Clear-Methode**](/windows/desktop/Direct2D/id2d1rendertarget-clear) füllt das gesamte Renderziel mit einer Volltonfarbe auf. Die Farbe wird als [**D2D1 \_ COLOR \_ F-Struktur**](/windows/desktop/Direct2D/d2d1-color-f) angegeben. Sie können die [**D2D1::ColorF-Klasse verwenden,**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf) um die -Struktur zu initialisieren. Weitere Informationen finden Sie unter [Verwenden von Farben in Direct2D.](using-color-in-direct2d.md)
3.  Die [**ID2D1RenderTarget::FillEllipse-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) zeichnet eine gefüllte Ellipse unter Verwendung des angegebenen Pinsels für die Füllung. Eine Ellipse wird durch einen Mittelpunkt und die x- und y-radii angegeben. Wenn die x- und y-radii identisch sind, ist das Ergebnis ein Kreis.
4.  Die [**ID2D1RenderTarget::EndDraw-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) signalisiert den Abschluss des Zeichnens für diesen Frame. Alle Zeichnungsvorgänge müssen zwischen Aufrufen von [**BeginDraw und**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) **EndDraw platziert werden.**

Die [**Methoden BeginDraw,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) [**Clear**](/windows/desktop/Direct2D/id2d1rendertarget-clear)und [**FillEllipse haben**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) alle einen **void-Rückgabetyp.** Wenn während der Ausführung einer dieser Methoden ein Fehler auftritt, wird der Fehler über den Rückgabewert der [**EndDraw-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) signalisiert. Die `CreateGraphicsResources` -Methode wird im Thema Creating [Direct2D Resources (Erstellen von Direct2D-Ressourcen) gezeigt.](render-targets--devices--and-resources.md) Diese Methode erstellt das Renderziel und den Volltonfarbpinsel.

Das Gerät kann die Zeichnungsbefehle puffern und deren Ausführung so lange zurückziehen, bis [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) aufgerufen wird. Sie können erzwingen, dass das Gerät alle ausstehenden Zeichnungsbefehle ausführt, indem Sie [**ID2D1RenderTarget::Flush aufrufen.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-flush) Durch Leeren kann jedoch die Leistung reduziert werden.

## <a name="handling-device-loss"></a>Behandeln von Geräteverlusten

Während das Programm ausgeführt wird, ist das von Ihnen verwendete Grafikgerät möglicherweise nicht mehr verfügbar. Beispielsweise kann das Gerät verloren gehen, wenn sich die Anzeigeauflösung ändert, oder wenn der Benutzer den Adapter entfernt. Wenn das Gerät verloren geht, wird auch das Renderziel zusammen mit allen geräteabhängigen Ressourcen, die dem Gerät zugeordnet waren, ungültig. Direct2D signalisiert einem verloren gegangenen Gerät, indem der Fehlercode **D2DERR \_ RECREATE \_ TARGET** von der [**EndDraw-Methode zurückgegeben**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) wird. Wenn Sie diesen Fehlercode erhalten, müssen Sie das Renderziel und alle geräteabhängigen Ressourcen neu erstellen.

Um eine Ressource zu verwerfen, geben Sie einfach die Schnittstelle für diese Ressource frei.


```C++
void MainWindow::DiscardGraphicsResources()
{
    SafeRelease(&pRenderTarget);
    SafeRelease(&pBrush);
}
```



Das Erstellen einer Ressource kann ein aufwendiger Vorgang sein, daher sollten Sie Ihre Ressourcen nicht für jede [**WM \_ PAINT-Nachricht neu**](/windows/desktop/gdi/wm-paint) erstellen. Erstellen Sie einmal eine Ressource, und speichern Sie den Ressourcenzeiger zwischen, bis die Ressource aufgrund eines Geräteverlusts ungültig wird oder Sie diese Ressource nicht mehr benötigen.

## <a name="the-direct2d-render-loop"></a>Die Direct2D-Renderschleife

Unabhängig davon, was Sie zeichnen, sollte Das Programm eine Schleife wie die folgende ausführen.

1.  Erstellen Sie geräteunabhängige Ressourcen.
2.  Rendern Sie die Szene.
    1.  Überprüfen Sie, ob ein gültiges Renderziel vorhanden ist. Falls nicht, erstellen Sie das Renderziel und die geräteabhängigen Ressourcen.
    2.  Rufen [**Sie ID2D1RenderTarget::BeginDraw auf.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)
    3.  Problem beim Zeichnen von Befehlen.
    4.  Rufen [**Sie ID2D1RenderTarget::EndDraw auf.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)
    5.  Wenn [**EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) **D2DERR \_ RECREATE TARGET \_ zurückgibt,** verwerfen Sie das Renderziel und geräteabhängige Ressourcen.
3.  Wiederholen Sie Schritt 2, wenn Sie die Szene aktualisieren oder neu gezeichnet haben.

Wenn das Renderziel ein Fenster ist, wird Schritt 2 immer dann angezeigt, wenn das Fenster eine [**WM \_ PAINT-Nachricht**](/windows/desktop/gdi/wm-paint) empfängt.

Die hier gezeigte Schleife behandelt den Geräteverlust, indem die geräteabhängigen Ressourcen verworfen und zu Beginn der nächsten Schleife neu erstellt werden (Schritt 2a).

## <a name="next"></a>Nächste

[DPI und Device-Independent Pixel](dpi-and-device-independent-pixels.md)

 

 