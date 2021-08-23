---
title: Übersicht über die Interoperabilität von Direct2D und Direct3D
description: Übersicht über die Interoperabilität von Direct2D und Direct3D
ms.assetid: 27680714-dc68-44eb-ab16-2cae3529b352
keywords:
- Direct2D,Direct3D-Interoperation
- Direct2D, Interoperabilität
- Interoperabilität,Direct2D
- Interoperabilität,Direct3D
- Direct3D, Interoperabilität
- Direct3D,Direct2D-Interoperation
- Direct2D, DXGI
- DXGI
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1aca1eac7218528e897a2a519543d80ab4ae2be3fa5d11a4107b02f1b23f2061
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698190"
---
# <a name="direct2d-and-direct3d-interoperability-overview"></a>Übersicht über die Interoperabilität von Direct2D und Direct3D

Hardwarebeschleunigte 2D- und 3D-Grafiken werden zunehmend Teil von Nicht-Gaming-Anwendungen, und die meisten Gaminganwendungen verwenden 2D-Grafiken in Form von Menüs und Heads-Up Displays (HUDs). Es gibt viele Vorteile, die hinzugefügt werden können, indem herkömmliches 2D-Rendering auf effiziente Weise mit Direct3D-Rendering kombiniert werden kann.

In diesem Thema wird beschrieben, wie 2D- und 3D-Grafiken mithilfe von Direct2D und [Direct3D](../graphics-and-multimedia.md)integriert werden.

Der Abschnitt ist wie folgt gegliedert.

-   [Voraussetzungen](#prerequisites)
-   [Unterstützte Direct3D-Versionen](#supported-direct3d-versions)
-   [Interoperabilität durch DXGI](#interoperability-through-dxgi)
-   [Schreiben in eine Direct3D-Oberfläche mit einem DXGI Surface-Renderziel](#writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target)
    -   [Erstellen einer DXGI-Oberfläche](#creating-a-dxgi-surface)
-   [Schreiben von Direct2D-Inhalten in einen Austauschkettenpuffer](#writing-direct2d-content-to-a-swap-chain-buffer)
    -   [Beispiel: Zeichnen eines 2D-Hintergrunds](#example-draw-a-2-d-background)
-   [Verwenden von Direct2D-Inhalten als Textur](#using-direct2d-content-as-a-texture)
    -   [Beispiel: Verwenden von Direct2D-Inhalten als Textur](#example-use-direct2d-content-as-a-texture)
-   [Ändern der Größe eines DXGI-Oberflächenrenderziels](#resizing-a-dxgi-surface-render-target)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In dieser Übersicht wird davon ausgegangen, dass Sie mit grundlegenden Direct2D-Zeichnungsvorgängen vertraut sind. Ein Tutorial finden Sie im [Direct2D-Schnellstart.](direct2d-quickstart.md) Außerdem wird davon ausgegangen, dass Sie mit [Direct3D 10.1](/windows/desktop/direct3d10/d3d10-graphics)programmieren können.

## <a name="supported-direct3d-versions"></a>Unterstützte Direct3D-Versionen

Mit DirectX 11.0 unterstützt Direct2D nur die Interoperabilität mit Direct3D 10.1-Geräten. Mit DirectX 11.1 oder höher unterstützt Direct2D auch die Interoperabilität mit Direct3D 11.

## <a name="interoperability-through-dxgi"></a>Interoperabilität durch DXGI

Ab Direct3D 10 verwendet die Direct3D-Runtime [DXGI](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) für die Ressourcenverwaltung. Die DXGI-Laufzeitebene ermöglicht die prozessübergreifende Freigabe von Videospeicheroberflächen und dient als Grundlage für andere videospeicherbasierte Laufzeitplattformen. Direct2D verwendet DXGI für die Interoperabilität mit Direct3D.

Es gibt zwei Primäre Möglichkeiten, Direct2D und Direct3D zusammen zu verwenden:

-   Sie können Direct2D-Inhalt in eine Direct3D-Oberfläche schreiben, indem Sie eine [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) abrufen und mit [**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) verwenden, um eine [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)zu erstellen. Sie können dann das Renderziel verwenden, um dreidimensionalen Grafiken eine zweidimensionale Schnittstelle oder einen Hintergrund hinzuzufügen, oder eine Direct2D-Zeichnung als Textur für ein dreidimensionales Objekt verwenden.
-   Indem [**Sie CreateSharedBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) zum Erstellen einer [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) aus einer [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface)verwenden, können Sie eine Direct3D-Szene in eine Bitmap schreiben und mit Direct2D rendern.

## <a name="writing-to-a-direct3d-surface-with-a-dxgi-surface-render-target"></a>Schreiben in eine Direct3D-Oberfläche mit einem DXGI Surface-Renderziel

Um in eine Direct3D-Oberfläche zu schreiben, rufen Sie eine [**IDXGISurface**](/windows/desktop/api/dxgi/nn-dxgi-idxgisurface) ab und übergeben sie an die [**CreateDxgiSurfaceRenderTarget-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) um ein DXGI-Oberflächenrenderziel zu erstellen. Anschließend können Sie das DXGI-Oberflächenrenderingziel verwenden, um 2D-Inhalte auf die DXGI-Oberfläche zu zeichnen.

Ein DXGI-Oberflächenrenderziel ist eine Art von [**ID2D1RenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) Wie andere Direct2D-Renderziele können Sie damit Ressourcen erstellen und Zeichnungsbefehle ausführen.

Das DXGI-Oberflächenrenderziel und die DXGI-Oberfläche müssen dasselbe DXGI-Format verwenden. Wenn Sie beim Erstellen des Renderziels das [**DXGI \_ FORMAT \_ UNMARKEN-Format**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) angeben, wird automatisch das Format der Oberfläche verwendet.

Das DXGI-Oberflächenrenderziel führt keine DXGI-Oberflächensynchronisierung durch.

### <a name="creating-a-dxgi-surface"></a>Erstellen einer DXGI-Oberfläche

Mit Direct3D 10 gibt es mehrere Möglichkeiten, eine DXGI-Oberfläche zu erhalten. Sie können eine [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) für ein Gerät erstellen und dann die [**GetBuffer-Methode**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) der Swapkette verwenden, um eine DXGI-Oberfläche abzurufen. Alternativ können Sie ein Gerät verwenden, um eine Textur zu erstellen, und dann diese Textur als DXGI-Oberfläche verwenden.

Unabhängig davon, wie Sie die DXGI-Oberfläche erstellen, muss die Oberfläche eines der DXGI-Formate verwenden, die von DXGI-Oberflächenrenderingzielen unterstützt werden. Eine Liste finden Sie unter [Unterstützte Pixelformate und Alphamodi.](supported-pixel-formats-and-alpha-modes.md)

Darüber hinaus muss die [**ID3D10Device1,**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) die der DXGI-Oberfläche zugeordnet ist, BGRA DXGI-Formate unterstützen, damit die Oberfläche mit Direct2D funktioniert. Um diese Unterstützung sicherzustellen, verwenden Sie das Flag [**D3D10 \_ CREATE \_ DEVICE \_ BGRA \_ SUPPORT,**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) wenn Sie die [**D3D10CreateDevice1-Methode**](/windows/desktop/api/d3d10_1/nf-d3d10_1-d3d10createdevice1) aufrufen, um das Gerät zu erstellen.

Der folgende Code definiert eine Methode, die eine [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1)erstellt. Sie wählt die beste verfügbare Featureebene aus und greift auf [Windows Advanced Rasterization Platform (WARP)](./installing-the-direct2d-debug-layer.md) zurück, wenn kein Hardwarerendering verfügbar ist.


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



Im nächsten Codebeispiel wird die `CreateD3DDevice` im vorherigen Beispiel gezeigte Methode verwendet, um ein Direct3D-Gerät zu erstellen, das DXGI-Oberflächen für die Verwendung mit Direct2D erstellen kann.


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



## <a name="writing-direct2d-content-to-a-swap-chain-buffer"></a>Schreiben von Direct2D-Inhalten in einen Austauschkettenpuffer

Die einfachste Möglichkeit zum Hinzufügen von Direct2D-Inhalten zu einer Direct3D-Szene besteht darin, die [**GetBuffer-Methode**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) einer [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) zu verwenden, um eine DXGI-Oberfläche abzurufen, und dann die Oberfläche mit der [**CreateDxgiSurfaceRenderTarget-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) zu verwenden, um eine [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) zu erstellen, mit der Sie Ihren 2D-Inhalt zeichnen können.

Bei diesem Ansatz werden Ihre Inhalte nicht in drei Dimensionen gerendert. sie hat keine Perspektive oder Tiefe. Sie ist jedoch für mehrere allgemeine Aufgaben nützlich:

-   Erstellen eines 2D-Hintergrunds für eine 3D-Szene.
-   Erstellen einer 2D-Schnittstelle vor einer 3D-Szene.
-   Verwenden von Direct3D-Multisampling beim Rendern von Direct2D-Inhalten.

Im nächsten Abschnitt wird gezeigt, wie Sie einen 2D-Hintergrund für eine 3D-Szene erstellen.

### <a name="example-draw-a-2-d-background"></a>Beispiel: Zeichnen eines 2D-Hintergrunds

In den folgenden Schritten wird beschrieben, wie Sie ein DXGI-Oberflächenrenderziel erstellen und zum Zeichnen eines Farbverlaufshintergrunds verwenden.

1.  Verwenden Sie die [**CreateSwapChain-Methode,**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) um eine Swapkette für eine [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) (die m *\_ pDevice-Variable)* zu erstellen. Die Swapkette verwendet das [**DXGI \_ FORMAT \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI-Format, eines der von Direct2D unterstützten DXGI-Formate.

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

    

2.  Verwenden Sie die [**GetBuffer-Methode**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) der Swapkette, um eine DXGI-Oberfläche abzurufen.

```C++
    // Get a surface in the swap chain
    hr = m_pSwapChain->GetBuffer(
        0,
        IID_PPV_ARGS(&pBackBuffer)
        );
```

    

3.  Verwenden Sie die DXGI-Oberfläche, um ein DXGI-Renderziel zu erstellen.
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



    

4.  Verwenden Sie das Renderziel, um einen Farbverlaufshintergrund zu zeichnen.

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



    

Code wird in diesem Beispiel ausgelassen.

## <a name="using-direct2d-content-as-a-texture"></a>Verwenden von Direct2D-Inhalten als Textur

Eine weitere Möglichkeit zum Verwenden von Direct2D-Inhalten mit Direct3D ist die Verwendung von Direct2D, um eine 2D-Textur zu generieren und diese Textur dann auf ein 3D-Modell anzuwenden. Hierzu erstellen Sie eine [**ID3D10Texture2D,**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)erhalten eine DXGI-Oberfläche aus der Textur und verwenden dann die Oberfläche, um ein DXGI-Oberflächenrenderziel zu erstellen. Die **ID3D10Texture2D-Oberfläche** muss das Bind-Flag [**D3D10 \_ BIND RENDER \_ \_ TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) verwenden und ein DXGI-Format verwenden, das von DXGI-Oberflächenrenderzielen unterstützt wird. Eine Liste der unterstützten DXGI-Formate finden Sie unter [Unterstützte Pixelformate und Alphamodi.](supported-pixel-formats-and-alpha-modes.md)

### <a name="example-use-direct2d-content-as-a-texture"></a>Beispiel: Verwenden von Direct2D-Inhalten als Textur

Die folgenden Beispiele zeigen, wie Sie ein DXGI-Oberflächenrenderziel erstellen, das in einer 2D-Textur gerendert wird (dargestellt durch eine [**ID3D10Texture2D**](/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d)).

1.  Verwenden Sie zunächst ein Direct3D-Gerät, um eine 2D-Textur zu erstellen. Die Textur verwendet die Bindungsflags [**D3D10 \_ BIND \_ RENDER \_ TARGET**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_bind_flag) und **D3D10 \_ BIND \_ SHADER \_ RESOURCE** und das [**DXGI FORMAT \_ \_ B8G8R8A8 \_ UNORM**](/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format) DXGI-Format, eines der von Direct2D unterstützten DXGI-Formate.

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

    

2.  Verwenden Sie die Textur, um eine DXGI-Oberfläche zu erhalten.

```C++
    IDXGISurface *pDxgiSurface = NULL;

    
hr = m_pOffscreenTexture->QueryInterface(&pDxgiSurface);
```



    

3.  Verwenden Sie die Oberfläche mit der [**CreateDxgiSurfaceRenderTarget-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) um ein Direct2D-Renderziel abzurufen.

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



    

Nachdem Sie nun ein Direct2D-Renderziel erhalten und es einer Direct3D-Textur zugeordnet haben, können Sie das Renderziel verwenden, um Direct2D-Inhalt auf diese Textur zu zeichnen, und Sie können diese Textur auf Direct3D-Primitive anwenden.

Code wird in diesem Beispiel ausgelassen.

## <a name="resizing-a-dxgi-surface-render-target"></a>Ändern der Größe eines DXGI-Oberflächenrenderziels

DXGI-Oberflächenrenderziele unterstützen die [**ID2D1RenderTarget::Resize-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)) nicht. Um die Größe eines DXGI-Oberflächenrenderziels zu ändern, muss die Anwendung es freigeben und neu erstellen.

Dieser Vorgang kann zu Leistungsproblemen führen. Das Renderziel ist möglicherweise die letzte aktive Direct2D-Ressource, die einen Verweis auf die [**ID3D10Device1**](/windows/desktop/api/d3d10_1/nn-d3d10_1-id3d10device1) beibehält, die der DXGI-Oberfläche des Renderziels zugeordnet ist. Wenn die Anwendung das Renderziel freigibt und der **ID3D10Device1-Verweis** zerstört wird, muss ein neues neu erstellt werden.

Sie können diesen potenziell kostspieligen Vorgang vermeiden, indem Sie mindestens eine Direct2D-Ressource behalten, die vom Renderziel erstellt wurde, während Sie dieses Renderziel neu erstellen. Im Folgenden sind einige Direct2D-Ressourcen, die für diesen Ansatz geeignet sind:

-   [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) (die indirekt von einem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)gehalten werden kann)
-   [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer)
-   [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh)

Um diesem Ansatz gerecht zu werden, sollte Ihre Methode zum Ändern der Größe testen, um festzustellen, ob das Direct3D-Gerät verfügbar ist. Falls verfügbar, geben Sie Ihre DXGI-Oberflächenrenderingziele frei, und erstellen Sie sie neu. Behalten Sie jedoch alle zuvor erstellten Ressourcen bei, und verwenden Sie sie wieder. Dies funktioniert, da, wie in der Übersicht über Ressourcen [beschrieben,](resources-and-resource-domains.md)Ressourcen, die von zwei Renderzielen erstellt werden, kompatibel sind, wenn beide Renderziele demselben Direct3D-Gerät zugeordnet sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Unterstützte Pixelformate und Alpha-Modi](supported-pixel-formats-and-alpha-modes.md)
</dt> <dt>

[**CreateDxgiSurfaceRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))
</dt> <dt>

[Windows DirectX-Grafiken](../graphics-and-multimedia.md)
</dt> </dl>

 

 
