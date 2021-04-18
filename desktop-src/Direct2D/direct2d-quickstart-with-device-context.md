---
title: Direct2D Schnellstart für Windows 8
description: Fasst die Schritte zusammen, die zum Zeichnen mit Direct2D erforderlich sind, und stellt Beispielcode bereit.
ms.assetid: FF4623FA-CA60-4637-9EE6-34C4EC84E51A
keywords:
- Direct2D, Codebeispiel zum Zeichnen des Rechtecks
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28e5cfbbf4e63e129a43bec783a64203e20e30a0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341315"
---
# <a name="direct2d-quickstart-for-windows-8"></a>Direct2D Schnellstart für Windows 8

Direct2D ist eine API im einheitlichen Code zum Erstellen von 2D-Grafiken. In diesem Thema wird veranschaulicht, wie Direct2D verwendet wird, um zu einem [**Windows:: UI:: Core:: corewindow**](/uwp/api/Windows.UI.Core.CoreWindow)zu zeichnen.

Dieses Thema enthält folgende Abschnitte:

-   [Zeichnen eines einfachen Rechtecks](#drawing-a-simple-rectangle)
-   [Schritt 1: einschließen des Direct2D-Headers](#step-1-include-direct2d-header)
-   [Schritt 2: Erstellen eines ID2D1Factory1](#step-2-create-an-id2d1factory1)
-   [Schritt 3: Erstellen eines ID2D1Device und eines ID2D1DeviceContext](#step-3-create-an-id2d1device-and-an-id2d1devicecontext)
-   [Schritt 4: Erstellen eines Pinsels](#step-4-create-a-brush)
-   [Schritt 5: Zeichnen des Rechtecks](#step-5-draw-the-rectangle)
-   [Beispielcode](#example-code)

## <a name="drawing-a-simple-rectangle"></a>Zeichnen eines einfachen Rechtecks

Wenn Sie ein Rechteck mithilfe von [GDI](/windows/desktop/gdi/windows-gdi)zeichnen möchten, können Sie die [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) -Meldung wie im folgenden Code gezeigt verarbeiten.


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



Der Code zum Zeichnen desselben Rechtecks mit Direct2D ist ähnlich: er erstellt Zeichnungs Ressourcen, beschreibt eine Form, die gezeichnet werden soll, zeichnet die Form und gibt dann die Zeichnungs Ressourcen frei. In den folgenden Abschnitten werden die einzelnen Schritte ausführlich beschrieben.

## <a name="step-1-include-direct2d-header"></a>Schritt 1: einschließen des Direct2D-Headers

Zusätzlich zu den Headern, die für die Anwendung erforderlich sind, schließen Sie die Header d2d1. h und d2d1 \_ 1. h ein.

## <a name="step-2-create-an-id2d1factory1"></a>Schritt 2: Erstellen eines ID2D1Factory1

Eines der ersten Dinge, bei denen es sich bei allen Direct2D-Beispielen um das Erstellen eines [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1)handelt.


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



Die [**ID2D1Factory1**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1factory1) -Schnittstelle ist der Ausgangspunkt für die Verwendung von Direct2D. Verwenden Sie ein **ID2D1Factory1** , um Direct2D-Ressourcen zu erstellen.

Beim Erstellen einer Factory können Sie angeben, ob es sich um einen Multithread oder einen Single Thread handelt. (Weitere Informationen zu Multithread-Factorys finden Sie in den Hinweisen auf der [**ID2D1Factory-Referenzseite**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).) In diesem Beispiel wird eine Single Thread Factory erstellt.

Im Allgemeinen sollte die Anwendung die Factory einmal erstellen und für die Lebensdauer der Anwendung beibehalten.

## <a name="step-3-create-an-id2d1device-and-an-id2d1devicecontext"></a>Schritt 3: Erstellen eines ID2D1Device und eines ID2D1DeviceContext

Nachdem Sie eine Factory erstellt haben, verwenden Sie Sie, um ein Direct2D-Gerät zu erstellen, und verwenden Sie dann das Gerät zum Erstellen eines Direct2D-Geräte Kontexts. Um diese Direct2D-Objekte zu erstellen, müssen Sie über ein [**Direct3D 11-Gerät**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) , ein [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)und eine [**DXGI-Swapkette**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)verfügen. Informationen zum Erstellen der erforderlichen Voraussetzungen finden Sie unter [Geräte und Geräte Kontexte](devices-and-device-contexts.md) .


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



Ein Gerätekontext ist ein Gerät, das Zeichnungsvorgänge ausführen und Geräte abhängige Zeichnungs Ressourcen erstellen kann, wie z. b. Pinsel. Sie können auch den Gerätekontext verwenden, um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit einer DXGI-Oberfläche zu verknüpfen, die als Renderziel verwendet werden soll. Der Gerätekontext kann in verschiedene Arten von Zielen Rendering.

Der Code hier deklariert die Eigenschaften für Bitmap, die mit einer DXGI-SwapChain verknüpft ist, die in ein [**corewindow**](/uwp/api/Windows.UI.Core.CoreWindow)gerendert wird. Die [**ID2D1DeviceContext:: kreatebitmapfromdxgisurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) -Methode ruft eine Direct2D-Oberfläche aus der DXGI-Oberfläche ab. Dadurch wird alles, was für das Ziel [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) gerendert wird, auf der Oberfläche der Swapkette gerendert.

Nachdem Sie die Direct2D-Oberfläche verwendet haben, verwenden Sie die [**ID2D1DeviceContext:: SetTarget**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget) -Methode, um Sie als aktives Renderziel festzulegen.


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

Wie eine Factory kann ein Gerätekontext Zeichnungs Ressourcen erstellen. In diesem Beispiel erstellt der Gerätekontext einen Pinsel.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);
```



Ein Pinsel ist ein Objekt, das einen Bereich zeichnet, z. b. den Strich einer Form oder das Ausfüllen einer Geometrie. Der Pinsel in diesem Beispiel zeichnet einen Bereich mit einer vordefinierten voll Tonfarbe, schwarz.

Direct2D bietet auch andere Pinseltypen: Farbverlaufs Pinsel zum Zeichnen von linearen und radialen Farbverläufen, ein [**Bitmap-Pinsel**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zum Zeichnen mit Bitmaps und Mustern und ab Windows 8 ein [**Bild Pinsel**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush) zum Zeichnen mit einem gerenderten Bild.

Einige Zeichnungs-APIs stellen Stifte zum Zeichnen von Gliederungen und Pinsel zum Auffüllen von Formen bereit. Direct2D unterscheidet sich von einem Stift Objekt, es wird jedoch ein Pinsel zum Zeichnen von Gliederungen und Ausfüllen von Formen verwendet. Verwenden Sie beim Zeichnen von Gliederungen die [**ID2D1StrokeStyle**](/windows/win32/api/d2d1/nn-d2d1-id2d1strokestyle) -Schnittstelle oder beginnend mit Windows 8 die [**ID2D1StrokeStyle1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1strokestyle1) -Schnittstelle mit einem Pinsel zum Steuern von Pfad Streifen Vorgängen.

Ein Pinsel kann nur mit dem Renderziel, von dem es erstellt wurde, und mit anderen renderzielen in derselben Ressourcen Domäne verwendet werden. Im Allgemeinen sollten Sie Pinsel einmal erstellen und Sie für die Lebensdauer des Renderziels aufbewahren, von dem Sie erstellt wurden. [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ist die einzige Ausnahme. Da es relativ preiswert ist, zu erstellen, können Sie jedes Mal, wenn Sie einen Frame zeichnen, ein **ID2D1SolidColorBrush** erstellen, ohne dass eine spürbare Leistungs Beeinträchtigung erzielt wird. Sie können auch eine einzelne **ID2D1SolidColorBrush** verwenden und die Farbe oder Deckkraft jedes Mal ändern, wenn Sie Sie verwenden.

## <a name="step-5-draw-the-rectangle"></a>Schritt 5: Zeichnen des Rechtecks

Verwenden Sie als nächstes den Gerätekontext zum Zeichnen des Rechtecks.


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



Die [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode nimmt zwei Parameter an: das zu zeichnende Rechteck und den Pinsel, der zum Zeichnen der Kontur des Rechtecks verwendet werden soll. Optional können Sie auch die Optionen Stroke Width, Dash Pattern, Line Join und End Cap angeben.

Sie müssen die [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufrufen, bevor Sie Zeichenbefehle ausgeben, und Sie müssen die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode aufrufen, nachdem Sie das Ausgeben von Zeichnungs Befehlen abgeschlossen haben. Die **EndDraw** -Methode gibt ein **HRESULT** zurück, das angibt, ob die Zeichnungs Befehle erfolgreich waren. Wenn dies nicht erfolgreich ist, löst die einschränkte Hilfsfunktion eine Ausnahme aus.

Die [**idxgiswapchain::P Resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) -Methode tauscht die Puffer Oberfläche mit der auf der Bildschirmoberfläche aus, um das Ergebnis anzuzeigen.

## <a name="example-code"></a>Beispielcode

Der Code in diesem Thema zeigt die grundlegenden Elemente einer Direct2D-Anwendung. Aus Gründen der Kürze lässt das Thema das Anwendungs Framework und den Fehler Behandlungs Code aus, der für eine gut geschriebene Anwendung typisch ist.

 

 