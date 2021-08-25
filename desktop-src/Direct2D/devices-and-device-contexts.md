---
title: Rendern mithilfe eines Direct2D-Gerätekontexts
description: In diesem Thema erfahren Sie mehr über das Erstellen von Direct2D \ 32;Gerätekontext in Windows 8.
ms.assetid: D4563FEA-767E-4B16-8F3C-3D548A64B206
keywords:
- Direct2D-Gerät
- Direct2D-Gerätekontext
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 735ad81a5911b16c159ffb8c63173421a55295e20e34090eb483065e1a7d311c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119832995"
---
# <a name="how-to-render-by-using-a-direct2d-device-context"></a>Rendern mithilfe eines Direct2D-Gerätekontexts

In diesem Thema erfahren Sie mehr über das Erstellen des [**Direct2D-Gerätekontexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) in Windows 8. [](./direct2d-portal.md) Diese Informationen gelten für Sie, wenn Sie Windows Store-Apps oder eine Desktop-App mit Direct2D entwickeln. In diesem Thema werden der Zweck von Direct2D-Gerätekontextobjekten, das Erstellen dieses Objekts und eine Schritt-für-Schritt-Anleitung zum Rendern und Anzeigen von Direct2D-Primitiven und -Bildern beschrieben. Außerdem erfahren Sie mehr über das Wechseln von Renderzielen und das Hinzufügen von Effekten zu Ihrer App.

-   [Was ist ein Direct2D-Gerät?](#what-is-a-direct2d-device)
-   [Was ist ein Direct2D-Gerätekontext?](#what-is-a-direct2d-device-context)
-   [Rendern mit Direct2D auf Windows 8](#rendering-with-direct2d-on-windows-8)
-   [Gründe für das Rendern eines Gerätekontexts](#why-use-a-device-context-to-render)
-   [Erstellen eines Direct2D-Gerätekontexts für das Rendering](#how-to-create-a-direct2d-device-context-for-rendering)
-   [Auswählen eines Ziels](#selecting-a-target)
-   [Rendern und Anzeigen](#how-to-render-and-display)

## <a name="what-is-a-direct2d-device"></a>Was ist ein Direct2D-Gerät?

Sie benötigen ein Direct2D-Gerät und ein Direct3D-Gerät, um einen Direct2D-Gerätekontext zu erstellen. Ein [**Direct2D-Gerät**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) (macht einen **ID2D1Device-Schnittstellenzeiger** verfügbar) stellt einen Anzeigeadapter dar. Ein Direct3D-Gerät (macht einen [**ID3D11Device-Schnittstellenzeiger**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) verfügbar) ist einem Direct2D-Gerät zugeordnet. Jede App muss über ein **Direct2D-Gerät** verfügen, kann aber über mehrere **Geräte verfügen.**

## <a name="what-is-a-direct2d-device-context"></a>Was ist ein Direct2D-Gerätekontext?

Ein [Direct2D-Gerätekontext](./direct2d-portal.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) (macht einen **ID2D1DeviceContext-Schnittstellenzeiger** verfügbar) stellt einen Satz von Zustands- und Befehlspuffern dar, die Sie zum Rendern auf ein Ziel verwenden. Sie können Methoden im Gerätekontext aufrufen, um den Pipelinezustand festzulegen und Renderingbefehle zu generieren, indem Sie die Ressourcen verwenden, die sich im Besitz eines Geräts befinden.

## <a name="rendering-with-direct2d-on-windows-8"></a>Rendern mit Direct2D auf Windows 8

Auf Windows 7 und früher verwenden Sie ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) oder eine andere Renderzielschnittstelle, um in einem Fenster oder einer Oberfläche zu rendern. Ab Windows 8 wird das Rendering nicht empfohlen, indem Methoden verwendet werden, die auf Schnittstellen wie **ID2D1HwndRenderTarget** basieren, da sie nicht mit Windows Store-Apps funktionieren. Sie können einen [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) zum Rendern in einem Hwnd verwenden, wenn Sie eine Desktop-App erstellen und dennoch die zusätzlichen Features des **Gerätekontexts** nutzen möchten. Der **Gerätekontext** ist jedoch erforderlich, um Inhalte in einer Windows Store-Apps mit [Direct2D](./direct2d-portal.md)zu rendern.

## <a name="why-use-a-device-context-to-render"></a>Gründe für das Rendern eines Gerätekontexts

-   Sie können für Windows Store-Apps rendern.
-   Sie können das Renderziel jederzeit vor, während und nach dem Rendering ändern. Der Gerätekontext stellt sicher, dass die Aufrufe von Zeichnungsmethoden in der reihenfolge ausgeführt werden, und wendet sie an, wenn Sie das Renderziel wechseln.
-   Sie können mehrere Fenstertypen mit einem Gerätekontext verwenden. Sie können einen [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) und eine [**DXGI-Swapkette**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1) verwenden, um direkt in einem [**Windows::UI::Core::CoreWindow**](/uwp/api/Windows.UI.Core.CoreWindow) oder einem [**Windows::UI::XAML::SwapChainBackgroundPanel zu rendern.**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainBackgroundPanel)
-   Sie können den [Direct2D-Gerätekontext](./direct2d-portal.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) verwenden, um [Direct2D-Effekte](effects-overview.md) zu erstellen und die Ausgabe eines Bildeffekts oder Effektdiagramms in einem Renderziel zu rendern.
-   Sie können über mehrere [**Gerätekontexte**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)verfügen. Dies kann hilfreich sein, um die Leistung in einer Thread-App zu verbessern. Weitere Informationen finden Sie unter [Multithread-Direct2D-Apps.](multi-threaded-direct2d-apps.md)
-   Der [**Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) arbeitet eng mit Direct3D zusammen, sodass Sie mehr Zugriff auf Direct3D-Optionen haben.

## <a name="how-to-create-a-direct2d-device-context-for-rendering"></a>Erstellen eines Direct2D-Gerätekontexts für das Rendering

Der folgende Code zeigt Ihnen, wie Sie ein Direct3D11-Gerät erstellen, das zugehörige DXGI-Gerät abrufen, ein [**Direct2D-Gerät**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)erstellen und schließlich den Direct2D-Gerätekontext für das Rendering erstellen. [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

Hier sehen Sie ein Diagramm der Methodenaufrufe und der Schnittstellen, die dieser Code verwendet.

![Diagramm von direct2d- und direct3d-Geräten und Gerätekontexten.](images/devicecontextdiagram.png)

> [!Note]  
> In diesem Code wird davon ausgegangen, dass Sie bereits über ein [**ID2D1Factory1-Objekt**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1factory1) verfügen. Weitere Informationen finden Sie auf der [**Referenzseite id2D1Factory.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)

 


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



Sehen wir uns die Schritte im vorherigen Codebeispiel an.

1.  Abrufen eines ID3D11Device-Schnittstellenzeigers, den Sie benötigen, um den Gerätekontext zu erstellen.

    -   Deklarieren Sie die Erstellungsflags, um das [Direct3D-Gerät](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) für die BGRA-Unterstützung einzurichten. [Direct2D](./direct2d-portal.md) erfordert die BGRA-Farbreihenfolge.
    -   Deklarieren Sie ein Array von [**D3D \_ FEATURE LEVEL-Einträgen, \_**](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_feature_level) die den Satz von Featureebenen darstellen, die Ihre App unterstützt.
        > [!Note]  
        > [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) durchsucht Ihre Liste, bis die vom Hostsystem unterstützte Funktionsebene gefunden wird.

         

    -   Verwenden Sie die [**D3D11CreateDevice-Funktion,**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) um ein [**ID3D11Device-Objekt**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1) zu erstellen. Die Funktion gibt auch ein [**ID3D11DeviceContext-Objekt**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1) zurück, aber dieses Objekt wird für dieses Beispiel nicht benötigt.

2.  Fragen Sie das [**Direct3D 11-Gerät**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) nach seiner [**DXGI-Geräteschnittstelle**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) ab.
3.  Erstellen Sie ein [**ID2D1Device-Objekt,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) indem Sie die [**ID2D1Factory::CreateDevice-Methode**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) aufrufen und das [**IDXGIDevice-Objekt**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) übergeben.
4.  Erstellen Sie einen [**ID2D1DeviceContext-Zeiger**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) mithilfe der [**ID2D1Device::CreateDeviceContext-Methode.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext)

## <a name="selecting-a-target"></a>Auswählen eines Ziels

Der Code hier zeigt, wie Sie die [**zweidimensionale Direct3D-Textur**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) für den Fensterrückpuffer abrufen und ein Bitmapziel erstellen, das mit dieser Textur verknüpft ist, mit der der [**Direct2D-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) gerendert wird.


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



Sehen wir uns die Schritte im vorherigen Codebeispiel an.

1.  Ordnen Sie eine [**DXGI \_ SWAP CHAIN \_ \_ DESC1-Struktur**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) zu, und definieren Sie die Einstellungen für die [**Swapkette**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

    Diese Einstellungen zeigen ein Beispiel für das Erstellen einer Swapkette, die von einer Windows Store-App verwendet werden kann.

2.  Abrufen des Adapters, auf dem das [**Direct3D-Gerät**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) und das [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) ausgeführt werden, und Abrufen des [**idXGIFactory-Objekts,**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2) das ihnen zugeordnet ist. Sie müssen diese **DXGI-Factory** verwenden, um sicherzustellen, dass die [**Swapkette**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) auf demselben Adapter erstellt wird.

3.  Rufen Sie die [**IDXGIFactory2::CreateSwapChainForCoreWindow-Methode**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow) auf, um die Swapkette zu erstellen. Verwenden Sie die [**Windows::UI::CoreWindow-Klasse**](/uwp/api/Windows.UI.Core.CoreWindow) für das Hauptfenster einer Windows Store-App.

    Stellen Sie sicher, dass Sie die maximale Framelatenz auf 1 festlegen, um den Energieverbrauch zu minimieren.

    Wenn Sie Direct2D-Inhalte in einer Windows Store-App rendern möchten, lesen Sie die [**CreateSwapChainForComposition-Methode.**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)

4.  Abrufen des Hintergrundpuffers aus der [**Swapkette.**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) Der Hintergrundpuffer macht eine [**ID3D11Texture2D-Schnittstelle verfügbar,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) die von der **Swapkette** zugeordnet wird.

5.  Deklarieren Sie eine [**D2D1 \_ BITMAP \_ PROPERTIES1-Struktur,**](/windows/desktop/api/D2D1_1/ns-d2d1_1-d2d1_bitmap_properties1) und legen Sie die Eigenschaftswerte fest. Legen Sie das Pixelformat auf BGRA fest, da dies das Format ist, das das [**Direct3D-Gerät**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) und das [**DXGI-Gerät**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice) verwenden.

6.  Abrufen des Hintergrundpuffers als [**IDXGISurface,**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgisurface2) das an Direct2D übergeben werden soll. Direct2D akzeptiert eine [**ID3D11Texture2D**](/windows/desktop/api/d3d11/nn-d3d11-id3d11texture2d) nicht direkt.

    Erstellen Sie ein [**ID2D1Bitmap-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) aus dem Hintergrundpuffer mithilfe der [**ID2D1DeviceContext::CreateBitmapFromDxgiSurface-Methode.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1))

7.  Jetzt ist die [**Direct2D-Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit dem Hintergrundpuffer verknüpft. Legen Sie das Ziel für den [**Direct2D-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) auf die **Bitmap** fest.

## <a name="how-to-render-and-display"></a>Rendern und Anzeigen

Nachdem Sie nun über eine Zielbitmap verfügen, können Sie primitive Objekte, Bilder, Bildeffekte und Text mithilfe des [**Direct2D-Gerätekontexts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)zeichnen. Der Code hier zeigt, wie Sie ein Rechteck zeichnen.


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



Sehen wir uns die Schritte im vorherigen Codebeispiel an.

1.  Rufen [**Sie CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) auf, um einen Pinsel zum Zeichnen des Rechtecks zu erstellen.
2.  Rufen Sie die [**BeginDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) auf, bevor Sie Zeichnungsbefehle ausgeben.
3.  Rufen Sie die [**DrawRectangle-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) auf, das zu zeichnende Rechteck und den Pinsel.
4.  Rufen Sie die [**EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) auf, nachdem Sie mit dem Ausgeben von Zeichnungsbefehlen fertig sind.
5.  Zeigen Sie das Ergebnis an, indem Sie die [**IDXGISwapChain::P resent-Methode**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present) aufrufen.

Jetzt können Sie den [**Direct2D-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) verwenden, um Primitive, Bilder, Bildeffekte und Text auf dem Bildschirm zu zeichnen.

 

 