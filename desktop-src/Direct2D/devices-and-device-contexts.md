---
title: Vorgehensweise beim Rendering mithilfe eines Direct2D-Geräte Kontexts
description: In diesem Thema erfahren Sie mehr über das Erstellen von Direct2D \ 32; Gerätekontext in Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Direct2D-Gerät
- Direct2D-Gerätekontext
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 2858861956a40bf969309be474105052e4692cde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104567545"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a>Vorgehensweise beim Rendering mithilfe eines Direct2D-Geräte Kontexts

In diesem Thema erfahren Sie mehr über das Erstellen des [Direct2D](./direct2d-portal.md) - [**Geräte Kontexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8. Diese Informationen gelten für Sie, wenn Sie Windows Store-Apps oder eine Desktop-App mithilfe von Direct2D entwickeln. In diesem Thema wird der Zweck von Direct2D-Gerätekontext Objekten, das Erstellen dieses Objekts und eine Schritt-für-Schritt-Anleitung zum Rendern und Anzeigen von Direct2D Primitives und Bildern beschrieben. Außerdem erfahren Sie mehr über das Wechseln von renderzielen und das Hinzufügen von Effekten zu Ihrer APP.

-   [Was ist ein Direct2D-Gerät?](#what-is-a-direct2d-device)
-   [Was ist ein Direct2D-Gerätekontext?](#what-is-a-direct2d-device-context)
-   [Rendering mit Direct2D unter Windows 8](#rendering-with-direct2d-on-windows-8)
-   [Gründe für die Verwendung eines Geräte Kontexts zum Rendering](#why-use-a-device-context-to-render)
-   [Erstellen eines Direct2D-Geräte Kontexts für das Rendering](#how-to-create-a-direct2d-device-context-for-rendering)
-   [Auswählen eines Ziels](#selecting-a-target)
-   [Rendering und Anzeige](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a>Was ist ein Direct2D-Gerät?

Sie benötigen ein Direct2D-Gerät und ein Direct3D-Gerät, um einen Direct2D-Gerätekontext zu erstellen. Ein [**Direct2D-Gerät**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (das einen **ID2D1Device** -Schnittstellen Zeiger verfügbar macht) stellt einen Anzeige Adapter dar. Ein Direct3D-Gerät (das einen [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) -Schnittstellen Zeiger verfügbar macht) ist einem Direct2D-Gerät zugeordnet. Jede APP muss über ein **Direct2D-Gerät** verfügen, kann aber über mehrere **Geräte** verfügen.

## <a name="what-is-a-direct2d-device-context"></a>Was ist ein Direct2D-Gerätekontext?

Ein [Direct2D](./direct2d-portal.md) - [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (macht einen **ID2D1DeviceContext** -Schnittstellen Zeiger verfügbar) stellt einen Satz von Status-und Befehls Puffern dar, die Sie verwenden, um ein Ziel zu rendieren. Sie können Methoden für den Gerätekontext aufzurufen, um den Pipeline Status festzulegen und renderingbefehle zu generieren, indem Sie die Ressourcen eines Geräts verwenden.

## <a name="rendering-with-direct2d-on-windows-8"></a>Rendering mit Direct2D unter Windows 8

Unter Windows 7 und früher verwenden Sie eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) oder eine andere renderzielschnittstelle, um Sie in einem Fenster oder einer Oberfläche zu renderzielen. Ab Windows 8 empfiehlt es sich nicht, das Rendering mithilfe von Methoden durchzuführen, die auf Schnittstellen wie **ID2D1HwndRenderTarget** basieren, da Sie nicht mit Windows Store-Apps funktionieren. Sie können einen [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) verwenden, um ein HWND zu erzeugen, wenn Sie eine Desktop-App erstellen möchten, und die zusätzlichen Features des **Geräte Kontexts** weiterhin nutzen. Der **Gerätekontext** ist jedoch zum Rendering von Inhalten in Windows Store-Apps mit [Direct2D](./direct2d-portal.md)erforderlich.

## <a name="why-use-a-device-context-to-render"></a>Gründe für die Verwendung eines Geräte Kontexts zum Rendering

-   Sie können für Windows Store-Apps Rendering.
-   Sie können das Renderziel jederzeit vor, während und nach dem Rendering ändern. Der Gerätekontext stellt sicher, dass die Aufrufe von Zeichnungs Methoden in der richtigen Reihenfolge ausgeführt werden, und wendet sie an, wenn Sie das Renderziel wechseln.
-   Sie können mehr als einen Fenstertyp mit einem Gerätekontext verwenden. Sie können einen [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) und eine [**DXGI-SwapChain**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) verwenden, um direkt in ein [**Windows:: UI:: Core:: corewindow**](/uwp/api/Windows.UI.Core.CoreWindow) oder ein [**Windows:: UI:: XAML:: swapchainbackgroundpanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel)-Element gerenstet zu werden.
-   Sie können den [Direct2D](./direct2d-portal.md) - [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) zum Erstellen von [Direct2D-Effekten](effects-overview.md) und zum renderingrendering der Ausgabe eines Bild Effekts oder eines Effekt Diagramms in ein Renderziel verwenden.
-   Sie können über mehrere [**Geräte Kontexte**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)verfügen. Dies kann hilfreich sein, um die Leistung in einer Thread-APP zu verbessern. Weitere Informationen finden Sie unter [Multithreaded Direct2D-apps](multi-threaded-direct2d-apps.md) .
-   Der [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interagiert eng mit Direct3D und bietet Ihnen mehr Zugriff auf Direct3D-Optionen.

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a>Erstellen eines Direct2D-Geräte Kontexts für das Rendering

Der folgende Code zeigt, wie Sie ein Direct3D11-Gerät erstellen, das zugehörige DXGI-Gerät erhalten, ein [**Direct2D-Gerät**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)erstellen und schließlich den Direct2D- [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) für das Rendering erstellen.

Im folgenden finden Sie ein Diagramm der Methodenaufrufe und der von diesem Code verwendeten Schnittstellen.

![Diagramm der Direct2D-und Direct3D-Geräte und-Geräte Kontexte.](images/devicecontextdiagram.png)

> [!Note]  
> Dieser Code setzt voraus, dass Sie bereits über ein [**ID2D1Factory1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) -Objekt verfügen. Weitere Informationen finden Sie auf der [**ID2D1Factory-Referenzseite**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory).

 


```C++
    // This flag adds support for surfaces with a different color channel ordering than the API default.
    // You need it for compatibility with Direct2D.
    UINT creationFlags = D3D11_CREATE_DEVICE_BGRA_SUPPORT;
    
    // This array defines the set of DirectX hardware feature levels this app  supports.
    // The ordering is important and you should  preserve it.
    // Don't forget to declare your app's minimum required feature level in its
    // description.  All apps are assumed to support 9.1 unless otherwise stated.
    D3D_FEATURE_LEVEL featureLevels[] = 
    {
        D3D_FEATURE_LEVEL_11_1,
        D3D_FEATURE_LEVEL_11_0,
        D3D_FEATURE_LEVEL_10_1,
        D3D_FEATURE_LEVEL_10_0,
        D3D_FEATURE_LEVEL_9_3,
        D3D_FEATURE_LEVEL_9_2,
        D3D_FEATURE_LEVEL_9_1
    };

    // Create the DX11 API device object, and get a corresponding context.
    ComPtr<ID3D11Device> device;
    ComPtr<ID3D11DeviceContext> context;

    DX::ThrowIfFailed(
        D3D11CreateDevice(
            nullptr,                    // specify null to use the default adapter
            D3D_DRIVER_TYPE_HARDWARE,
            0,                          
            creationFlags,              // optionally set debug and Direct2D compatibility flags
            featureLevels,              // list of feature levels this app can support
            ARRAYSIZE(featureLevels),   // number of possible feature levels
            D3D11_SDK_VERSION,          
            &device,                    // returns the Direct3D device created
            &m_featureLevel,            // returns feature level of device created
            &context                    // returns the device immediate context
            )
        );

    ComPtr<IDXGIDevice> dxgiDevice;
    // Obtain the underlying DXGI device of the Direct3D11 device.
    DX::ThrowIfFailed(
        device.As(&dxgiDevice)
        );

    // Obtain the Direct2D device for 2-D rendering.
    DX::ThrowIfFailed(
        m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice)
        );

    // Get Direct2D device's corresponding device context object.
    DX::ThrowIfFailed(
        m_d2dDevice->CreateDeviceContext(
            D2D1_DEVICE_CONTEXT_OPTIONS_NONE,
            &m_d2dContext
            )
        );
```



Gehen wir die Schritte im vorangehenden Codebeispiel durch.

1.  Rufen Sie einen ID3D11Device-Schnittstellen Zeiger ab, der zum Erstellen des Geräte Kontexts benötigt wird.

    -   Deklarieren Sie die Erstellungs Flags, um das [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) -Gerät für die BGRA-Unterstützung einzurichten. [Direct2D](./direct2d-portal.md) erfordert die BGRA-Farb Reihenfolge.
    -   Deklarieren Sie ein Array von [**D3D- \_ Funktions \_**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) Ebenen-Einträgen, die den Satz von featureebenen darstellen, die ihre App unterstützt.
        > [!Note]  
        > [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) durchsucht die Liste, bis die von dem Host System unterstützte Funktionsebene gefunden wird.

         

    -   Verwenden Sie die [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) -Funktion zum Erstellen eines [**ID3D11Device**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) -Objekts, die Funktion gibt auch ein [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) -Objekt zurück, aber dieses Objekt ist für dieses Beispiel nicht erforderlich.

2.  Fragen Sie das [**Gerät Direct3D 11**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) nach seiner [**DXGI-Geräte**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) Schnittstelle ab.
3.  Erstellen Sie ein [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) -Objekt, indem Sie die [**ID2D1Factory:: createdevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) -Methode aufrufen und das [**idxgidevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) -Objekt übergeben.
4.  Erstellen Sie mithilfe der Methode [**ID2D1Device:: | atedevicecontext**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) einen [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Zeiger.

## <a name="selecting-a-target"></a>Auswählen eines Ziels

Der folgende Code zeigt, wie Sie die [**2 dimensionale Direct3D-Textur**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) für den Fenster Hintergrund Puffer erhalten und ein bitmapziel erstellen, das mit dieser Textur verknüpft ist, mit der der [**Direct2D-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) gerendert wird.


```C++
        // Allocate a descriptor.
        DXGI_SWAP_CHAIN_DESC1 swapChainDesc = {0};
        swapChainDesc.Width = 0;                           // use automatic sizing
        swapChainDesc.Height = 0;
        swapChainDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM; // this is the most common swapchain format
        swapChainDesc.Stereo = false; 
        swapChainDesc.SampleDesc.Count = 1;                // don't use multi-sampling
        swapChainDesc.SampleDesc.Quality = 0;
        swapChainDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapChainDesc.BufferCount = 2;                     // use double buffering to enable flip
        swapChainDesc.Scaling = DXGI_SCALING_NONE;
        swapChainDesc.SwapEffect = DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL; // all apps must use this SwapEffect
        swapChainDesc.Flags = 0;

        // Identify the physical adapter (GPU or card) this device is runs on.
        ComPtr<IDXGIAdapter> dxgiAdapter;
        DX::ThrowIfFailed(
            dxgiDevice->GetAdapter(&dxgiAdapter)
            );

        // Get the factory object that created the DXGI device.
        ComPtr<IDXGIFactory2> dxgiFactory;
        DX::ThrowIfFailed(
            dxgiAdapter->GetParent(IID_PPV_ARGS(&dxgiFactory))
            );

        // Get the final swap chain for this window from the DXGI factory.
        DX::ThrowIfFailed(
            dxgiFactory->CreateSwapChainForCoreWindow(
                device.Get(),
                reinterpret_cast<IUnknown*>(m_window),
                &swapChainDesc,
                nullptr,    // allow on all displays
                &m_swapChain
                )
            );

        // Ensure that DXGI doesn't queue more than one frame at a time.
        DX::ThrowIfFailed(
            dxgiDevice->SetMaximumFrameLatency(1)
            );

    // Get the backbuffer for this window which is be the final 3D render target.
    ComPtr<ID3D11Texture2D> backBuffer;
    DX::ThrowIfFailed(
        m_swapChain->GetBuffer(0, IID_PPV_ARGS(&backBuffer))
        );

    // Now we set up the Direct2D render target bitmap linked to the swapchain. 
    // Whenever we render to this bitmap, it is directly rendered to the 
    // swap chain associated with the window.
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = 
        BitmapProperties1(
            D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
            PixelFormat(DXGI_FORMAT_B8G8R8A8_UNORM, D2D1_ALPHA_MODE_IGNORE),
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

    // Now we can set the Direct2D render target.
    m_d2dContext->SetTarget(m_d2dTargetBitmap.Get());
```



Gehen wir die Schritte im vorangehenden Codebeispiel durch.

1.  Zuordnen einer [**DXGI \_ - \_ SwapChain \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) -Struktur und Definieren der Einstellungen für die Swapkette. [](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)

    Diese Einstellungen zeigen ein Beispiel für das Erstellen einer Austausch Kette, die von einer Windows Store-App verwendet werden kann.

2.  Holen Sie den Adapter, auf dem das [**Direct3D-Gerät**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) und das [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) ausgeführt werden, und erhalten Sie das [**idxgifactory**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) -Objekt. Sie müssen diese **DXGI-Factory** verwenden, um sicherzustellen, dass die SwapChain auf dem gleichen Adapter erstellt wird. [](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)

3.  Rufen Sie die [**IDXGIFactory2:: kreateswapchainforcorewindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) -Methode auf, um die Swapkette zu erstellen. Verwenden Sie die [**Windows:: UI:: corewindow**](/uwp/api/Windows.UI.Core.CoreWindow) -Klasse für das Hauptfenster einer Windows Store-App.

    Stellen Sie sicher, dass die maximale Frame Latenz auf 1 festgelegt ist, um den Energieverbrauch zu minimieren

    Wenn Sie Direct2D-Inhalt in einer Windows Store-App Rendering möchten, finden Sie weitere Informationen unter der Methode " [**kreateswapchainforcomposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) ".

4.  Den Hintergrund Puffer aus der [**Swapkette**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain)erhalten. Der Hintergrund Puffer macht eine von der **austauschkette** zugeordnete [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) -Schnittstelle verfügbar.

5.  Deklarieren Sie eine [**D2D1 \_ Bitmap \_ PROPERTIES1**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) -Struktur und legen Sie die Eigenschaftswerte fest. Legen Sie das Pixel Format auf BGRA fest, da dies das Format ist, das vom [**Direct3D-Gerät**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) und vom [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) verwendet wird.

6.  Gibt den Hintergrund Puffer als [**idxgisurface**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) an, der an Direct2D übergeben werden soll. Direct2D akzeptiert [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) nicht direkt.

    Erstellen Sie ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Objekt aus dem Hintergrund Puffer mithilfe der [**ID2D1DeviceContext:: deatebitmapfromdxgisurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) -Methode.

7.  Nun ist die [**Direct2D-Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit dem Hintergrund Puffer verknüpft. Legen Sie das Ziel für den [**Direct2D-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) auf die **Bitmap** fest.

## <a name="how-to-render-and-display"></a>Rendering und Anzeige

Nachdem Sie nun über eine Zielbitmap verfügen, können Sie mithilfe des [**Direct2D-Geräte Kontexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)primitive, Bilder, Bildeffekte und Text zeichnen. Der folgende Code zeigt, wie Sie ein Rechteck zeichnen.


```C++
ComPtr<ID2D1SolidColorBrush> pBlackBrush;
DX::ThrowIfFailed(
   m_d2dContext->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        )
);

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



Gehen wir die Schritte im vorangehenden Codebeispiel durch.

1.  Rufen Sie den Befehl " [**kreatesolidcolorbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) " auf, um einen Pinsel zum Zeichnen des Rechtecks erstellen
2.  Aufrufen der [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode vor dem Ausgeben von Zeichnungs Befehlen.
3.  Ruft die [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) -Methode das Rechteck ab, das gezeichnet werden soll, und den Pinsel.
4.  Aufrufen der [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode nach Abschluss der Ausgabe von Zeichnungs Befehlen.
5.  Zeigen Sie das Ergebnis an, indem Sie die [**idxgiswapchain::P Resent**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) -Methode aufrufen.

Nun können Sie den [**Direct2D-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) zeichnen Primitives, Bilder, Bildeffekte und Text auf dem Bildschirm verwenden.

 

 