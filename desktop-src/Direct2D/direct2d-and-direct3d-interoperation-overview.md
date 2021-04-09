---
title: Übersicht über die Interoperabilität von Direct2D und Direct3D
description: .
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Direct2D, Direct3D Interoperation
- Direct2D, Interoperabilität
- Interoperabilität, Direct2D
- Interoperabilität, Direct3D
- Direct3D, Interoperabilität
- Direct3D, Direct2D Interoperation
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 6854481ec2a8d869467aa912252e3649e17f2501
ms.sourcegitcommit: 4e4f9e7c90d25af0774deec1d44bd49fa9b6daa9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "104102511"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Übersicht über die Interoperabilität von Direct2D und Direct3D

Hardware beschleunigte 2D-und 3D-Grafiken werden zunehmend zu nicht-Gaming-Anwendungen, und die meisten Spiele Anwendungen verwenden 2D-Grafiken in Form von Menüs und Heads-Up anzeigen (HUDs). Es gibt viel Wert, der hinzugefügt werden kann, indem das herkömmliche 2D-Rendering auf effiziente Weise mit Direct3D Rendering gemischt wird.

In diesem Thema wird beschrieben, wie 2D-und 3D-Grafiken mithilfe von Direct2D und [Direct3D](../graphics-and-multimedia.md)integriert werden.

Der Abschnitt ist wie folgt gegliedert.

-   [Voraussetzungen](#prerequisites)
-   [Unterstützte Direct3D-Versionen](#supported-direct3d-versions)
-   [Interoperabilität durch DXGI](#interoperability-through-dxgi)
-   [Schreiben auf eine Direct3D-Oberfläche mit einem DXGI-Oberflächen Renderziel](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [Erstellen einer DXGI-Oberfläche](#creating-a-dxgi-surface)
-   [Schreiben von Direct2D-Inhalt in einen Austausch Ketten Puffer](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [Beispiel: Zeichnen eines 2D-Hintergrunds](#example-draw-a-2-d-background)
-   [Verwenden von Direct2D-Inhalten als Textur](#using-direct2d-content-as-a-texture)
    -   [Beispiel: Verwenden von Direct2D-Inhalten als Textur](#example-use-direct2d-content-as-a-texture)
-   [Ändern der Größe eines DXGI-Oberflächen Renderziels](#resizing-a-dxgi-surface-render-target)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Diese Übersicht setzt voraus, dass Sie mit grundlegenden Direct2D-Zeichnungs Vorgängen vertraut sind. Ein Tutorial finden Sie unter [Direct2D Quick Start](direct2d-quickstart.md). Außerdem wird davon ausgegangen, dass Sie mit [Direct3D 10,1](/windows/desktop/direct3d10/d3d10-graphics)programmieren können.

## <a name="supported-direct3d-versions"></a>Unterstützte Direct3D-Versionen

Mit DirectX 11,0 unterstützt Direct2D nur die Interoperabilität mit Direct3D 10,1-Geräten. Mit DirectX 11,1 oder höher unterstützt Direct2D auch die Interoperabilität mit Direct3D 11.

## <a name="interoperability-through-dxgi"></a>Interoperabilität durch DXGI

Ab Direct3D 10 verwendet die Direct3D-Laufzeit [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) zur Ressourcenverwaltung. Die DXGI-Lauf Zeit Ebene ermöglicht die prozessübergreifende Freigabe von Videospeicher Oberflächen und dient als Grundlage für andere auf Videos basierende laufzeitplattformen. Direct2D verwendet DXGI, um mit Direct3D zusammenzuarbeiten.

Es gibt zwei Hauptmethoden für die gemeinsame Verwendung von Direct2D und Direct3D:

-   Sie können Direct2D-Inhalte in eine Direct3D-Oberfläche schreiben, indem Sie eine [**idxgisurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) -Schnittstelle abrufen und diese mit dem ""- [**Wert**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) von "" erstellen, um ein [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)-Skript zu erstellen. Sie können dann das Renderziel zum Hinzufügen einer zweidimensionalen Schnittstelle oder eines Hintergrunds zu dreidimensionalen Grafiken verwenden, oder Sie verwenden eine Direct2D-Zeichnung als Textur für ein dreidimensionales Objekt.
-   Wenn Sie mit " [**anatesharedbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) " eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) von einer [**idxgisurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)-Datei erstellen, können Sie eine Direct3D-Szene in eine Bitmap schreiben und Sie mit Direct2D renden.

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>Schreiben auf eine Direct3D-Oberfläche mit einem DXGI-Oberflächen Renderziel

Um in eine Direct3D-Oberfläche zu schreiben, rufen Sie eine [**idxgisurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ab und übergeben Sie an [**die Methode "**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) Methode" von "Methode", um ein DXGI-Oberflächen Renderziel zu erstellen. Sie können dann das DXGI-Oberflächen Renderziel verwenden, um 2D-Inhalt auf die DXGI-Oberfläche zu zeichnen.

Ein DXGI-Oberflächen Renderziel ist eine Art von [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget). Wie andere Direct2D-Renderziele können Sie damit Ressourcen erstellen und Zeichnungs Befehle ausgeben.

Das DXGI-Oberflächen Renderziel und die DXGI-Oberfläche müssen das gleiche DXGI-Format verwenden. Wenn Sie beim Erstellen des Renderziels das [**\_ \_ Unkown-Format des DXGI-Formats**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) angeben, wird automatisch das-Format der Oberfläche verwendet.

Das DXGI-Oberflächen Renderziel führt keine DXGI-Oberflächen Synchronisierung aus.

### <a name="creating-a-dxgi-surface"></a>Erstellen einer DXGI-Oberfläche

Mit Direct3D 10 gibt es mehrere Möglichkeiten, eine DXGI-Oberfläche zu erhalten. Sie können eine [**idxgiswapchain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) für ein Gerät erstellen und dann die [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) -Methode der SwapChain verwenden, um eine DXGI-Oberfläche zu erhalten. Oder Sie können ein Gerät zum Erstellen einer Textur verwenden und diese Textur dann als DXGI-Oberfläche verwenden.

Unabhängig davon, wie Sie die DXGI-Oberfläche erstellen, muss die Oberfläche eines der DXGI-Formate verwenden, die von DXGI-Oberflächen renderzielen unterstützt werden. Eine Liste finden Sie [unter Unterstützte Pixel Formate und Alpha-Modi](supported-pixel-formats-and-alpha-modes.md).

Außerdem muss der [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) , der der DXGI-Oberfläche zugeordnet ist, BGRA DXGI-Formate unterstützen, damit die Oberfläche mit Direct2D verwendet werden kann. Um diese Unterstützung zu gewährleisten, verwenden Sie das Flag [**d3d10 \_ Create \_ Device \_ BGRA \_ Support**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) , wenn Sie die [**D3D10CreateDevice1**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) -Methode zum Erstellen des Geräts aufruft.

Der folgende Code definiert eine Methode, die eine [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1)erstellt. Es wählt die beste verfügbare Featureebene aus und greift auf die [Windows Advanced rasterization Platform (Warp)](./installing-the-direct2d-debug-layer.md) zurück, wenn kein Hardware Rendering verfügbar ist.


```C++
HRESULT DXGISampleApp::CreateD3DDevice(
    IDXGIAdapter *pAdapter,
    D3D10_DRIVER_TYPE driverType,
    UINT flags,
    ID3D10Device1 **ppDevice
    )
{
    HRESULT hr = S_OK;

    static const D3D10_FEATURE_LEVEL1 levelAttempts[] =
    {
        D3D10_FEATURE_LEVEL_10_0,
        D3D10_FEATURE_LEVEL_9_3,
        D3D10_FEATURE_LEVEL_9_2,
        D3D10_FEATURE_LEVEL_9_1,
    };

    for (UINT level = 0; level < ARRAYSIZE(levelAttempts); level++)
    {
        ID3D10Device1 *pDevice = NULL;
        hr = D3D10CreateDevice1(
            pAdapter,
            driverType,
            NULL,
            flags,
            levelAttempts[level],
            D3D10_1_SDK_VERSION,
            &pDevice
            );

        if (SUCCEEDED(hr))
        {
            // transfer reference
            *ppDevice = pDevice;
            pDevice = NULL;
            break;
        }

    }

    return hr;
}
```



Im nächsten Codebeispiel wird die `CreateD3DDevice` im vorherigen Beispiel gezeigte-Methode verwendet, um ein Direct3D-Gerät zu erstellen, mit dem DXGI-Oberflächen für die Verwendung mit Direct2D erstellt werden können.


```C++
// Create device
hr = CreateD3DDevice(
    NULL,
    D3D10_DRIVER_TYPE_HARDWARE,
    nDeviceFlags,
    &pDevice
    );

if (FAILED(hr))
{
    hr = CreateD3DDevice(
        NULL,
        D3D10_DRIVER_TYPE_WARP,
        nDeviceFlags,
        &pDevice
        );
}
```



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a>Schreiben von Direct2D-Inhalt in einen Austausch Ketten Puffer

Die einfachste Möglichkeit zum Hinzufügen von Direct2D-Inhalt zu einer Direct3D-Szene besteht darin, die [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) -Methode von [**idxgiswapchain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) zu verwenden, [**um eine**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) DXGI-Oberfläche zu erhalten, und dann die-Oberfläche mit [**der Methode "**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) Methode" von "Methode" von "Methode" zu verwenden, um den 2D-Inhalt zu zeichnen.

Bei diesem Ansatz werden Ihre Inhalte nicht in drei Dimensionen dargestellt. Sie hat keine Perspektive oder Tiefe. Es ist jedoch für verschiedene häufige Aufgaben nützlich:

-   Erstellen eines 2D-Hintergrunds für eine 3D-Szene.
-   Erstellen einer 2D-Schnittstelle vor einer 3D-Szene.
-   Verwenden von Direct3D multisamplinggrad beim Rendern von Direct2D-Inhalten.

Im nächsten Abschnitt wird gezeigt, wie ein 2D-Hintergrund für eine 3D-Szene erstellt wird.

### <a name="example-draw-a-2-d-background"></a>Beispiel: Zeichnen eines 2D-Hintergrunds

In den folgenden Schritten wird beschrieben, wie ein DXGI-Oberflächen Renderziel erstellt und zum Zeichnen eines Farbverlaufs Hintergrunds verwendet wird.

1.  Verwenden Sie die Methode " [**kreateswapchain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) ", um eine Austausch Kette für eine [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (die *m \_ pdevice* -Variable) zu erstellen. Die Swapkette verwendet das [**DXGI- \_ Format \_ B8G8R8A8 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI-Format, eines der DXGI-Formate, das von Direct2D unterstützt wird.

```C++
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&m_pDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDevice->QueryInterface(&pDXGIDevice);
    }
    if (SUCCEEDED(hr))
    {
        hr = pDXGIDevice->GetAdapter(&pAdapter);
    }
    if (SUCCEEDED(hr))
    {
        hr = pAdapter->GetParent(IID_PPV_ARGS(&pDXGIFactory));
    }
    if (SUCCEEDED(hr))
    {
        DXGI_SWAP_CHAIN_DESC swapDesc;
        ::ZeroMemory(&swapDesc, sizeof(swapDesc));

        swapDesc.BufferDesc.Width = nWidth;
        swapDesc.BufferDesc.Height = nHeight;
        swapDesc.BufferDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
        swapDesc.BufferDesc.RefreshRate.Numerator = 60;
        swapDesc.BufferDesc.RefreshRate.Denominator = 1;
        swapDesc.SampleDesc.Count = 1;
        swapDesc.SampleDesc.Quality = 0;
        swapDesc.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
        swapDesc.BufferCount = 1;
        swapDesc.OutputWindow = m_hwnd;
        swapDesc.Windowed = TRUE;

        hr = pDXGIFactory->CreateSwapChain(m_pDevice, &swapDesc, &m_pSwapChain);
    }
```

    

2.  Verwenden Sie die [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) -Methode der Swapkette zum Abrufen einer DXGI-Oberfläche.

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  Verwenden Sie die DXGI-Oberfläche zum Erstellen eines DXGI-Renderziels.
```C++
    // Create the DXGI Surface Render Target.
    FLOAT dpiX;
    FLOAT dpiY;
    m_pD2DFactory->GetDesktopDpi(&dpiX, &dpiY);

    D2D1_RENDER_TARGET_PROPERTIES props =
        D2D1::RenderTargetProperties(
            D2D1_RENDER_TARGET_TYPE_DEFAULT,
            D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
            dpiX,
            dpiY
            );

    // Create a Direct2D render target which can draw into the surface in the swap chain

    
hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
        pBackBuffer,
        &props,
        &m_pBackBufferRT
        );
    
```



    

4.  Verwenden Sie das Renderziel zum Zeichnen eines Hintergrund Farbverlaufs.

```C++
    // Swap chain will tell us how big the back buffer is
    DXGI_SWAP_CHAIN_DESC swapDesc;
    hr = m_pSwapChain->GetDesc(&swapDesc);

    if (SUCCEEDED(hr))
    {

    
// Draw a gradient background.
    if (m_pBackBufferRT)
    {
        D2D1_SIZE_F targetSize = m_pBackBufferRT->GetSize();

        m_pBackBufferRT->BeginDraw();

        m_pBackBufferGradientBrush->SetTransform(
            D2D1::Matrix3x2F::Scale(targetSize)
            );

        D2D1_RECT_F rect = D2D1::RectF(
            0.0f,
            0.0f,
            targetSize.width,
            targetSize.height
            );

        m_pBackBufferRT->FillRectangle(&rect, m_pBackBufferGradientBrush);

        hr = m_pBackBufferRT->EndDraw();
    }
```



    

Code wird in diesem Beispiel weggelassen.

## <a name="using-direct2d-content-as-a-texture"></a>Verwenden von Direct2D-Inhalten als Textur

Eine andere Möglichkeit, Direct2D-Inhalte mit Direct3D zu verwenden, besteht darin, mithilfe von Direct2D eine 2D-Textur zu generieren und diese Textur dann auf ein 3D-Modell anzuwenden. Zu diesem Zweck erstellen Sie eine [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d), die eine DXGI-Oberfläche aus der Textur erhält, und verwenden dann die-Oberfläche, um ein DXGI-Oberflächen Renderziel zu erstellen. Die **ID3D10Texture2D** -Oberfläche muss [**das \_ d3d10 \_ Bind \_ Renderziel**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) -Bindungs Flag verwenden und ein DXGI-Format verwenden, das von DXGI-Oberflächen renderzielen unterstützt wird Eine Liste der unterstützten DXGI-Formate finden Sie [unter Unterstützte Pixel Formate und Alpha-Modi](supported-pixel-formats-and-alpha-modes.md).

### <a name="example-use-direct2d-content-as-a-texture"></a>Beispiel: Verwenden von Direct2D-Inhalten als Textur

In den folgenden Beispielen wird veranschaulicht, wie ein DXGI-Oberflächen Renderziel erstellt wird, das in eine 2D-Textur (dargestellt durch einen [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)) gerendert wird.

1.  Verwenden Sie zunächst ein Direct3D-Gerät zum Erstellen einer 2D-Textur. In der Textur werden das [**d3d10 \_ Bind- \_ \_ Renderziel**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) und das **d3d10 \_ Bind- \_ Shader- \_ ressourcenbindungsflags** verwendet, und es wird das [**DXGI- \_ Format \_ B8G8R8A8 \_ unorm**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI-Format verwendet, eines der von Direct2D unterstützten DXGI-Formate.

```C++
    // Allocate a offscreen D3D surface for D2D to render our 2D content into
    D3D10_TEXTURE2D_DESC texDesc;
    texDesc.ArraySize = 1;
    texDesc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;
    texDesc.CPUAccessFlags = 0;
    texDesc.Format = DXGI_FORMAT_B8G8R8A8_UNORM;
    texDesc.Height = 512;
    texDesc.Width = 512;
    texDesc.MipLevels = 1;
    texDesc.MiscFlags = 0;
    texDesc.SampleDesc.Count = 1;
    texDesc.SampleDesc.Quality = 0;
    texDesc.Usage = D3D10_USAGE_DEFAULT;

    hr = m_pDevice->CreateTexture2D(&texDesc, NULL, &m_pOffscreenTexture);
```

    

2.  Verwenden Sie die Textur zum Abrufen einer DXGI-Oberfläche.

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  Verwenden Sie die-Oberfläche mit der Methode " [**kreatedxgisurfacerendertarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ", um ein Direct2D-Renderziel abzurufen.

```C++
    if (SUCCEEDED(hr))
    {
        // Create a D2D render target which can draw into our offscreen D3D
        // surface. Given that we use a constant size for the texture, we
        // fix the DPI at 96.
        D2D1_RENDER_TARGET_PROPERTIES props =
            D2D1::RenderTargetProperties(
                D2D1_RENDER_TARGET_TYPE_DEFAULT,
                D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
                96,
                96
                );

    
    hr = m_pD2DFactory->CreateDxgiSurfaceRenderTarget(
            pDxgiSurface,
            &props,
            &m_pRenderTarget
            );
    }
```



    

Nachdem Sie nun ein Direct2D-Renderziel abgerufen und eine Direct3D-Textur zugeordnet haben, können Sie das Renderziel verwenden, um Direct2D-Inhalt in diese Textur zu zeichnen, und Sie können diese Textur auf Direct3D Primitives anwenden.

Code wird in diesem Beispiel weggelassen.

## <a name="resizing-a-dxgi-surface-render-target"></a>Ändern der Größe eines DXGI-Oberflächen Renderziels

DXGI-Oberflächen-Renderziele unterstützen die [**ID2D1RenderTarget:: Resize**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) -Methode nicht. Um die Größe eines DXGI-Oberflächen Renderziels zu ändern, muss die Anwendung Sie freigeben und neu erstellen.

Mit diesem Vorgang können möglicherweise Leistungsprobleme entstehen. Das Renderziel kann die letzte aktive Direct2D-Ressource sein, die einen Verweis auf die [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) beibehält, die der DXGI-Oberfläche des Renderziels zugeordnet ist. Wenn die Anwendung das Renderziel freigibt und der **ID3D10Device1** -Verweis zerstört wird, muss ein neuer neu erstellt werden.

Sie können diesen potenziell teuren Vorgang vermeiden, indem Sie mindestens eine Direct2D-Ressource aufbewahren, die durch das Renderziel erstellt wurde, während Sie das Renderziel neu erstellen. Im folgenden finden Sie einige Direct2D-Ressourcen, die für diesen Ansatz funktionieren:

-   [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (möglicherweise indirekt durch eine [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush))
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

Um diesem Ansatz Rechnung zu tragen, sollte die Größe-Methode prüfen, ob das Direct3D-Gerät verfügbar ist. Wenn Sie verfügbar ist, geben Sie Ihre DXGI-Oberflächen Renderziele frei, und erstellen Sie Sie neu. behalten Sie jedoch alle zuvor erstellten Ressourcen bei, und verwenden Sie Sie erneut. Der Grund hierfür ist, dass Ressourcen, die durch zwei Renderziele erstellt wurden, kompatibel sind, wenn beide Renderziele dem gleichen Direct3D-Gerät zugeordnet sind, wie in der [Ressourcen Übersicht](resources-and-resource-domains.md)beschrieben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Pixelformate und Alpha-Modi](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**"Kreatedxgisurfakerendertarget"**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[Windows-DirectX-Grafiken](../graphics-and-multimedia.md)
</dt> </dl>

 

 