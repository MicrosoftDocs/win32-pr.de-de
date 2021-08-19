---
title: Direct2D-Schnellstart für Windows 8
description: Fasst die Schritte zusammen, die zum Zeichnen mit Direct2D für Windows 8 erforderlich sind, und stellt Beispielcode bereit. Direct2D ist eine NATIVE CODE-API zum Erstellen von 2D-Grafiken.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Beispiel für Direct2D,Zeichnen von Rechteckcode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3fd732d1d18cd731f6e6caa46f456f4896f47f778f8edc824442dfee5f6ac4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825431"
---
# <a name="direct2d-quickstart-for-windows-8"></a>Direct2D-Schnellstart für Windows 8

Direct2D ist eine nativ codierte API im Direktmodus zum Erstellen von 2D-Grafiken. In diesem Thema wird veranschaulicht, wie Direct2D verwendet wird, um in eine [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)zu zeichnen.

Dieses Thema enthält folgende Abschnitte:

-   [Zeichnen eines einfachen Rechtecks](#drawing-a-simple-rectangle)
-   [Schritt 1: Einschließen des Direct2D-Headers](#step-1-include-direct2d-header)
-   [Schritt 2: Erstellen einer ID2D1Factory1](#step-2-create-an-id2d1factory1)
-   [Schritt 3: Erstellen eines ID2D1Device und eines ID2D1DeviceContext](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [Schritt 4: Erstellen eines Pinsels](#step-4-create-a-brush)
-   [Schritt 5: Zeichnen des Rechtecks](#step-5-draw-the-rectangle)
-   [Beispielcode](#example-code)

## <a name="drawing-a-simple-rectangle"></a>Zeichnen eines einfachen Rechtecks

Um ein Rechteck mit [GDI](/windows/desktop/gdi/windows-gdi)zu zeichnen, können Sie die [**WM \_ PAINT-Meldung**](/windows/desktop/gdi/wm-paint) behandeln, wie im folgenden Code gezeigt.


```C++
switch(message)
{

    case WM_PAINT:
        {
            PAINTSTRUCT ps;
            BeginPaint(hwnd, &ps);

            // Obtain the size of the drawing area.
            RECT rc;
            GetClientRect(
                hwnd,
                &rc
            );          

            // Save the original object
            HGDIOBJ original = NULL;
            original = SelectObject(
                ps.hdc,
                GetStockObject(DC_PEN)
            );

            // Create a pen.            
            HPEN blackPen = CreatePen(PS_SOLID, 3, 0);

            // Select the pen.
            SelectObject(ps.hdc, blackPen);

            // Draw a rectangle.
            Rectangle(
                ps.hdc, 
                rc.left + 100, 
                rc.top + 100, 
                rc.right - 100, 
                rc.bottom - 100);   

            DeleteObject(blackPen);

            // Restore the original object
            SelectObject(ps.hdc, original);

            EndPaint(hwnd, &ps);
        }
        return 0;

// Code for handling other messages. 
```



Der Code zum Zeichnen des gleichen Rechtecks mit Direct2D ist ähnlich: Er erstellt Zeichnungsressourcen, beschreibt eine zu zeichnende Form, zeichnet die Form und gibt dann die Zeichnungsressourcen frei. In den folgenden Abschnitten werden die einzelnen Schritte ausführlich beschrieben.

## <a name="step-1-include-direct2d-header"></a>Schritt 1: Einschließen des Direct2D-Headers

Schließen Sie zusätzlich zu den für die Anwendung erforderlichen Headern die Header d2d1.h und d2d1 \_ 1.h ein.

## <a name="step-2-create-an-id2d1factory1"></a>Schritt 2: Erstellen einer ID2D1Factory1

Eines der ersten Dinge, die ein Direct2D-Beispiel macht, ist das Erstellen einer [**ID2D1Factory1.**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)


```C++
DX::ThrowIfFailed(
        D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            __uuidof(ID2D1Factory1),
            &options,
            &m_d2dFactory
            )
        );
```



Die [**ID2D1Factory1-Schnittstelle**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) ist der Ausgangspunkt für die Verwendung von Direct2D. Verwenden Sie **eine ID2D1Factory1,** um Direct2D-Ressourcen zu erstellen.

Wenn Sie eine Factory erstellen, können Sie angeben, ob es sich um multi- oder singlethreaded handelt. (Weitere Informationen zu Multithreadfactorys finden Sie in den Hinweisen auf der [**ID2D1Factory-Referenzseite.)**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) In diesem Beispiel wird eine Singlethreadfactory erstellt.

Im Allgemeinen sollte Ihre Anwendung die Factory einmal erstellen und für die Lebensdauer der Anwendung beibehalten.

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a>Schritt 3: Erstellen eines ID2D1Device und eines ID2D1DeviceContext

Nachdem Sie eine Factory erstellt haben, verwenden Sie sie, um ein Direct2D-Gerät zu erstellen, und verwenden Sie dann das Gerät, um einen Direct2D-Gerätekontext zu erstellen. Zum Erstellen dieser Direct2D-Objekte benötigen Sie ein [**Direct3D 11-Gerät,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) ein [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)und eine [**DXGI-Swapkette.**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) Informationen zum Erstellen der erforderlichen Voraussetzungen finden Sie unter [Geräte und Gerätekontexte.](devices-and-device-contexts.md)


```C++

    // Obtain the underlying DXGI device of the Direct3D11.1 device.
    DX::ThrowIfFailed(
        m_d3dDevice.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // And get its corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Ein Gerätekontext ist ein Gerät, das Zeichnungsvorgänge ausführen und geräteabhängige Zeichnungsressourcen wie Pinsel erstellen kann. Sie verwenden auch den Gerätekontext, um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit einer DXGI-Oberfläche zu verknüpfen, die als Renderziel verwendet werden soll. Der Gerätekontext kann auf verschiedene Arten von Zielen gerendert werden.

Der Code deklariert hier die Eigenschaften für Bitmaps, die mit einer DXGI-Swapkette verknüpft sind, die in einem [**CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow)gerendert wird. Die [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) ruft eine Direct2D-Oberfläche von der DXGI-Oberfläche ab. Dadurch wird alles, was in der [**Ziel-ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) gerendert wird, auf die Oberfläche der Swapkette gerendert.

Sobald Sie über die Direct2D-Oberfläche verfügen, verwenden Sie die [**ID2D1DeviceContext::SetTarget-Methode,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) um sie als aktives Renderziel festzulegen.


```C++
    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it will be directly rendered to the 
    // swapchain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_PREMULTIPLIED),
            m_dpi,
            m_dpi
            );

    // Direct2D needs the dxgi version of the backbuffer surface pointer.
    ComPtr<IDXGISurface> dxgiBackBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&dxgiBackBuffer))
        );

    // Get a D2D surface from the DXGI back buffer to use as the D2D render target.
    DX::ThrowIfFailed(
        m_d2dContext->CreateBitmapFromDxgiSurface(
            dxgiBackBuffer.Get(),
            &bitmapProperties,
            &m_d2dTargetBitmap
            )
        );

    // So now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



## <a name="step-4-create-a-brush"></a>Schritt 4: Erstellen eines Pinsels

Wie bei einer Factory kann ein Gerätekontext Zeichnungsressourcen erstellen. In diesem Beispiel erstellt der Gerätekontext einen Pinsel.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



Ein Pinsel ist ein Objekt, das einen Bereich zeichnet, z. B. den Strich einer Form oder die Füllung einer Geometrie. Der Pinsel in diesem Beispiel zeichnet einen Bereich mit einer vordefinierten Volltonfarbe Schwarz.

Direct2D bietet auch andere Arten von Pinseln: Farbverlaufspinsel zum Zeichnen linearer und radialer Farbverläufe, ein [**Bitmappinsel**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zum Zeichnen mit Bitmaps und Mustern und beginnend mit Windows 8, ein [**Bildpinsel**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) zum Zeichnen mit einem gerenderten Bild.

Einige Zeichnungs-APIs stellen Stifte zum Zeichnen von Konturen und Pinsel zum Füllen von Formen bereit. Direct2D ist anders: Es stellt kein Stiftobjekt bereit, sondern verwendet einen Pinsel zum Zeichnen von Konturen und Füllen von Formen. Verwenden Sie beim Zeichnen von Konturen die [**ID2D1StrokeStyle-Schnittstelle,**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) oder beginnen Sie in Windows 8 der [**ID2D1StrokeStyle1-Schnittstelle**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) mit einem Pinsel, um Pfad-Drosselungsvorgänge zu steuern.

Ein Pinsel kann nur mit dem Renderziel, das ihn erstellt hat, und mit anderen Renderzielen in derselben Ressourcendomäne verwendet werden. Im Allgemeinen sollten Sie Pinsel einmal erstellen und für die Lebensdauer des Renderziels beibehalten, das sie erstellt hat. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ist die einzige Ausnahme. da die Erstellung relativ kostengünstig ist, können Sie jedes Mal, wenn Sie einen Frame zeichnen, einen **ID2D1SolidColorBrush** erstellen, ohne dass eine spürbare Leistungssteigerung auftritt. Sie können auch einen einzelnen **ID2D1SolidColorBrush** verwenden und bei jeder Verwendung einfach seine Farbe oder Deckkraft ändern.

## <a name="step-5-draw-the-rectangle"></a>Schritt 5: Zeichnen des Rechtecks

Verwenden Sie als Nächstes den Gerätekontext, um das Rechteck zu zeichnen.


```C++
 
m_d2dContext->BeginDraw();

m_d2dContext->DrawRectangle(
    D2D1::RectF(
        rc.left + 100.0f,
        rc.top + 100.0f,
        rc.right - 100.0f,
        rc.bottom - 100.0f),
        pBlackBrush);

DX::ThrowIfFailed(
    m_d2dContext->EndDraw()
);

DX::ThrowIfFailed(
    m_swapChain->Present1(1, 0, &parameters);
);
```



Die [**DrawRectangle-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) verwendet zwei Parameter: das zu zeichnende Rechteck und den Pinsel, der zum Zeichnen der Kontur des Rechtecks verwendet werden soll. Optional können Sie auch die Optionen Strichbreite, Bindestrichmuster, Linienverknüpfung und Endendeende angeben.

Sie müssen die [**BeginDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) aufrufen, bevor Sie Zeichnungsbefehle ausgeben, und Sie müssen die [**EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) aufrufen, nachdem Sie mit dem Ausgeben von Zeichnungsbefehlen fertig sind. Die **EndDraw-Methode** gibt ein **HRESULT** zurück, das angibt, ob die Zeichnungsbefehle erfolgreich waren. Wenn dies nicht erfolgreich ist, löst die Hilfsfunktion ThrowIfFailed eine Ausnahme aus.

Die [**IDXGISwapChain::P Resent-Methode tauscht**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) die Pufferoberfläche mit der auf der Bildschirmoberfläche aus, um das Ergebnis anzuzeigen.

## <a name="example-code"></a>Beispielcode

Der Code in diesem Thema zeigt die grundlegenden Elemente einer Direct2D-Anwendung. Aus Gründen der Kürze werden im Thema das Anwendungsframework und der Fehlerbehandlungscode ausgelassen, der ein Merkmal einer gut geschriebenen Anwendung ist.

 

 