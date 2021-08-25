---
title: D2D mit D3D11on12
description: Im Beispiel D3D1211on12 wird veranschaulicht, wie D2D-Inhalt über D3D12-Inhalt gerendert wird, indem Ressourcen zwischen einem 11-basierten Gerät und einem 12-basierten Gerät gemeinsam verwendet werden.
ms.assetid: FAEF1412-053C-4B5F-80FA-85396C2586B4
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84f935ba49df4910aa729c39ae6ac0ce08f3810bf3b0cd75752bbe4c00e9ef1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858015"
---
# <a name="d2d-using-d3d11on12"></a>D2D mit D3D11on12

Im Beispiel **D3D1211on12** wird veranschaulicht, wie D2D-Inhalt über D3D12-Inhalt gerendert wird, indem Ressourcen zwischen einem 11-basierten Gerät und einem 12-basierten Gerät gemeinsam verwendet werden.

-   [Erstellen einer ID3D11On12Device](#create-an-id3d11on12device)
-   [Erstellen einer D2D-Factory](#create-a-d2d-factory)
-   [Erstellen eines Renderziels für D2D](#create-a-render-target-for-d2d)
-   [Erstellen grundlegender D2D-Textobjekte](#create-basic-d2d-text-objects)
-   [Aktualisieren der Hauptrenderschleife](#updating-the-main-render-loop)
-   [Ausführen des Beispiels](#run-the-sample)
-   [Zugehörige Themen](#related-topics)

## <a name="create-an-id3d11on12device"></a>Erstellen einer ID3D11On12Device

Der erste Schritt besteht darin, eine [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) zu erstellen, nachdem [**id3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) erstellt wurde. Dazu gehört das Erstellen einer [**ID3D11Device,**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device) die über die API [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice)um die **ID3D12Device** umschlossen ist. Diese API übernimmt neben anderen Parametern auch eine [**ID3D12CommandQueue,**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) sodass das 11On12-Gerät seine Befehle übermitteln kann. Nachdem **id3D11Device** erstellt wurde, können Sie die **ID3D11On12Device-Schnittstelle** daraus abfragen. Dies ist das primäre Geräteobjekt, das zum Einrichten von D2D verwendet wird.

Richten Sie in der **LoadPipeline-Methode** die Geräte ein.

``` syntax
 // Create an 11 device wrapped around the 12 device and share
    // 12's command queue.
    ComPtr<ID3D11Device> d3d11Device;
    ThrowIfFailed(D3D11On12CreateDevice(
        m_d3d12Device.Get(),
        d3d11DeviceFlags,
        nullptr,
        0,
        reinterpret_cast<IUnknown**>(m_commandQueue.GetAddressOf()),
        1,
        0,
        &d3d11Device,
        &m_d3d11DeviceContext,
        nullptr
        ));

    // Query the 11On12 device from the 11 device.
    ThrowIfFailed(d3d11Device.As(&m_d3d11On12Device));
```



| Aufrufflow                                              | Parameter |
|--------------------------------------------------------|------------|
| [**ID3D11Device**](/windows/desktop/api/d3d11/nn-d3d11-id3d11device)            |            |
| [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice) |            |



 

## <a name="create-a-d2d-factory"></a>Erstellen einer D2D-Factory

Nachdem wir nun über ein 11On12-Gerät verfügen, verwenden wir es, um eine D2D-Factory und ein D2D-Gerät zu erstellen, wie dies normalerweise mit D3D11 der Fall wäre.

Fügen Sie zur **LoadAssets-Methode** hinzu.

``` syntax
 // Create D2D/DWrite components.
    {
        D2D1_DEVICE_CONTEXT_OPTIONS deviceOptions = D2D1_DEVICE_CONTEXT_OPTIONS_NONE;
        ThrowIfFailed(D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, __uuidof(ID2D1Factory3), &d2dFactoryOptions, &m_d2dFactory));
        ComPtr<IDXGIDevice> dxgiDevice;
        ThrowIfFailed(m_d3d11On12Device.As(&dxgiDevice));
        ThrowIfFailed(m_d2dFactory->CreateDevice(dxgiDevice.Get(), &m_d2dDevice));
        ThrowIfFailed(m_d2dDevice->CreateDeviceContext(deviceOptions, &m_d2dDeviceContext));
        ThrowIfFailed(DWriteCreateFactory(DWRITE_FACTORY_TYPE_SHARED, __uuidof(IDWriteFactory), &m_dWriteFactory));
    }
```



| Aufrufflow                                                                        | Parameter                                                   |
|----------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**\_D2D1-GERÄTEKONTEXTOPTIONEN \_ \_**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_device_context_options)     |                                                              |
| [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory)                              | [**D2D1 \_ \_ FACTORY-TYP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)        |
| [**IDXGIDevice**](/windows/desktop/api/dxgi/nn-dxgi-idxgidevice)                                      |                                                              |
| [**ID2D1Factory3::CreateDevice**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1factory3-createdevice)           |                                                              |
| [**ID2D1Device::CreateDeviceContext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1device-createdevicecontext) |                                                              |
| [**DWriteCreateFactory**](/windows/desktop/api/dwrite/nf-dwrite-dwritecreatefactory)                       | [**\_DWRITE-FACTORYTYP \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_factory_type) |



 

## <a name="create-a-render-target-for-d2d"></a>Erstellen eines Renderziels für D2D

D3D12 besitzt die Swapkette. Wenn wir also mit unserem 11On12-Gerät (D2D-Inhalt) in den Hintergrundpuffer rendern möchten, müssen wir umschlossene Ressourcen vom Typ [**ID3D11Resource**](/windows/desktop/api/d3d11/nn-d3d11-id3d11resource) aus den Backpuffern des Typs [**ID3D12Resource**](/windows/desktop/api/d3d12/nn-d3d12-id3d12resource)erstellen. Dadurch wird **ID3D12Resource** mit einer D3D11-basierten Schnittstelle verknüpft, sodass sie mit dem 11On12-Gerät verwendet werden kann. Nachdem wir über eine umschlossene Ressource verfügen, können wir eine Renderzieloberfläche erstellen, auf der D2D gerendert werden kann, auch in der **LoadAssets-Methode.**

``` syntax
 // Query the desktop's dpi settings, which will be used to create
    // D2D's render targets.
    float dpiX;
    float dpiY;
    m_d2dFactory->GetDesktopDpi(&dpiX, &dpiY);
    D2D1_BITMAP_PROPERTIES1 bitmapProperties = D2D1::BitmapProperties1(
        D2D1_BITMAP_OPTIONS_TARGET | D2D1_BITMAP_OPTIONS_CANNOT_DRAW,
        D2D1::PixelFormat(DXGI_FORMAT_UNKNOWN, D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX,
        dpiY
        );  

    // Create frame resources.
    {
        CD3DX12_CPU_DESCRIPTOR_HANDLE rtvHandle(m_rtvHeap->GetCPUDescriptorHandleForHeapStart());

        // Create a RTV, D2D render target, and a command allocator for each frame.
        for (UINT n = 0; n < FrameCount; n++)
        {
            ThrowIfFailed(m_swapChain->GetBuffer(n, IID_PPV_ARGS(&m_renderTargets[n])));
            m_d3d12Device->CreateRenderTargetView(m_renderTargets[n].Get(), nullptr, rtvHandle);

            // Create a wrapped 11On12 resource of this back buffer. Since we are 
            // rendering all D3D12 content first and then all D2D content, we specify 
            // the In resource state as RENDER_TARGET - because D3D12 will have last 
            // used it in this state - and the Out resource state as PRESENT. When 
            // ReleaseWrappedResources() is called on the 11On12 device, the resource 
            // will be transitioned to the PRESENT state.
            D3D11_RESOURCE_FLAGS d3d11Flags = { D3D11_BIND_RENDER_TARGET };
            ThrowIfFailed(m_d3d11On12Device->CreateWrappedResource(
                m_renderTargets[n].Get(),
                &d3d11Flags,
                D3D12_RESOURCE_STATE_RENDER_TARGET,
                D3D12_RESOURCE_STATE_PRESENT,
                IID_PPV_ARGS(&m_wrappedBackBuffers[n])
                ));

            // Create a render target for D2D to draw directly to this back buffer.
            ComPtr<IDXGISurface> surface;
            ThrowIfFailed(m_wrappedBackBuffers[n].As(&surface));
            ThrowIfFailed(m_d2dDeviceContext->CreateBitmapFromDxgiSurface(
                surface.Get(),
                &bitmapProperties,
                &m_d2dRenderTargets[n]
                ));

            rtvHandle.Offset(1, m_rtvDescriptorSize);

            ThrowIfFailed(m_d3d12Device->CreateCommandAllocator(D3D12_COMMAND_LIST_TYPE_DIRECT, IID_PPV_ARGS(&m_commandAllocators[n])));
        }
    }
```



<table>
<thead>
<tr class="header">
<th>Aufrufflow</th>
<th>Parameter</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-getdesktopdpi"><strong>ID2D1Factory::GetDesktopDpi</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_bitmap_properties1"><strong>D2D1_BITMAP_PROPERTIES1</strong></a></td>
<td><dl><a href="/windows/desktop/api/d2d1_1helper/nf-d2d1_1helper-bitmapproperties1"><strong>BitmapProperties1</strong></a><br />
[<strong>D2D1_BITMAP_OPTIONS</strong>] (/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_bitmap_options)<br />
[<strong>PixelFormat</strong>] (/windows/desktop/api/d2d1helper/nf-d2d1helper-pixelformat)<br />
[<strong>DXGI_FORMAT</strong>] (/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format)<br />
[<strong>D2D1_ALPHA_MODE</strong>] (/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)<br />
</dl></td>
</tr>
<tr class="odd">
<td><a href="cd3dx12-cpu-descriptor-handle.md"><strong>CD3DX12_CPU_DESCRIPTOR_HANDLE</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart"><strong>GetCPUDescriptorHandleForHeapStart</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer"><strong>IDXGISwapChain::GetBuffer</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrendertargetview"><strong>CreateRenderTargetView</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d11on12/ns-d3d11on12-d3d11_resource_flags"><strong>D3D11_RESOURCE_FLAGS</strong></a></td>
<td><a href="/windows/desktop/api/d3d11/ne-d3d11-d3d11_bind_flag"><strong>D3D11_BIND_FLAG</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource"><strong>CreateWrappedResource</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states"><strong>D3D12_RESOURCE_STATES</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface"><strong>IDXGISurface</strong></a></td>

</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1__id2d1bitmap1)"><strong>ID2D1DeviceContext::CreateBitmapFromDxgiSurface</strong></a></td>

</tr>
<tr class="even">
<td><a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandallocator"><strong>CreateCommandAllocator</strong></a></td>
<td><a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type"><strong>D3D12_COMMAND_LIST_TYPE</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="create-basic-d2d-text-objects"></a>Erstellen grundlegender D2D-Textobjekte

Nun verfügen wir über eine [**ID3D12Device**](/windows/desktop/api/d3d12/nn-d3d12-id3d12device) zum Rendern von 3D-Inhalten, eine [**ID2D1Device,**](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device) die für unser 12-Gerät über eine [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) freigegeben wird, die wir zum Rendern von 2D-Inhalten verwenden können, und beide sind so konfiguriert, dass sie in derselben Swapkette gerendert werden. In diesem Beispiel wird einfach das D2D-Gerät verwendet, um Text über die 3D-Szene zu rendern, ähnlich wie Spiele ihre Benutzeroberfläche rendern. Dazu müssen wir einige grundlegende D2D-Objekte erstellen, die sich noch in der **LoadAssets-Methode befinden.**

``` syntax
 // Create D2D/DWrite objects for rendering text.
    {
        ThrowIfFailed(m_d2dDeviceContext->CreateSolidColorBrush(D2D1::ColorF(D2D1::ColorF::Black), &m_textBrush));
        ThrowIfFailed(m_dWriteFactory->CreateTextFormat(
            L"Verdana",
            NULL,
            DWRITE_FONT_WEIGHT_NORMAL,
            DWRITE_FONT_STYLE_NORMAL,
            DWRITE_FONT_STRETCH_NORMAL,
            50,
            L"en-us",
            &m_textFormat
            ));
        ThrowIfFailed(m_textFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER));
        ThrowIfFailed(m_textFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER));
    }
```



| Aufrufflow                                                                                           | Parameter                                                                 |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush))    | [**ColorF**](/windows/desktop/api/d2d1helper/nl-d2d1helper-colorf)                                              |
| [**IDWriteFactory::CreateTextFormat**](/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextformat)                 | [**\_DWRITE-SCHRIFTBREITE \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_font_weight)                 |
| [**IDWriteTextFormat::SetTextAlignment**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-settextalignment)           | [**\_DWRITE-TEXTAUSRICHTUNG \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_text_alignment)           |
| [**IDWriteTextFormat::SetParagraphAlignment**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextformat-setparagraphalignment) | [**\_DWRITE-ABSATZAUSRICHTUNG \_**](/windows/desktop/api/dwrite/ne-dwrite-dwrite_paragraph_alignment) |



 

## <a name="updating-the-main-render-loop"></a>Aktualisieren der Hauptrenderschleife

Nachdem die Initialisierung des Beispiels abgeschlossen ist, können wir mit der Hauptrenderingschleife fortschreiten.

``` syntax
// Render the scene.
void D3D1211on12::OnRender()
{
    // Record all the commands we need to render the scene into the command list.
    PopulateCommandList();

    // Execute the command list.
    ID3D12CommandList* ppCommandLists[] = { m_commandList.Get() };
    m_commandQueue->ExecuteCommandLists(_countof(ppCommandLists), ppCommandLists);

    RenderUI();

    // Present the frame.
    ThrowIfFailed(m_swapChain->Present(0, 0));

    MoveToNextFrame();
}
```



| Aufrufflow                                                              | Parameter |
|------------------------------------------------------------------------|------------|
| [**ID3D12CommandList**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandlist)                         |            |
| [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists)  |            |
| [**IDXGISwapChain1::Present1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) |            |



 

Das Einzige, was für unsere Renderschleife neu ist, ist der **RenderUI-Aufruf,** der D2D zum Rendern der Benutzeroberfläche verwendet. Beachten Sie, dass wir zuerst alle D3D12-Befehlslisten ausführen, um unsere 3D-Szene zu rendern, und anschließend die Benutzeroberfläche darüber rendern. Bevor wir uns mit **RenderUI** befassen, müssen wir uns eine Änderung an **PopulateCommandLists** ansehen. In anderen Beispielen wird häufig eine Ressourcenbarriere in der Befehlsliste abgelegt, bevor sie geschlossen wird, um den Backpuffer vom Renderzielzustand in den aktuellen Zustand zu überführen. In diesem Beispiel entfernen wir diese Ressourcenbarriere jedoch, da wir weiterhin in den Hintergrundpuffern mit D2D rendern müssen. Beachten Sie, dass wir beim Erstellen unserer umschlossenen Ressourcen des Hintergrundpuffers den Renderzielzustand als "IN"-Status und den aktuellen Zustand als "OUT"-Zustand angegeben haben.

**RenderUI** ist im Hinblick auf die D2D-Nutzung relativ unkompliziert. Wir legen unser Renderziel fest und rendern unseren Text. Bevor sie jedoch umschlossene Ressourcen auf einem 11On12-Gerät verwenden, z. B. unsere Backpufferrenderziele, müssen wir die [**AcquireWrappedResources-API**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) auf dem 11On12-Gerät aufrufen. Nach dem Rendern rufen wir die [**ReleaseWrappedResources-API**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) auf dem 11On12-Gerät auf. Durch den Aufruf von **ReleaseWrappedResources** entsteht im Hintergrund eine Ressourcenbarriere, die die angegebene Ressource in den zum Zeitpunkt der Erstellung angegebenen OUT-Zustand übergibt. In unserem Fall ist dies der aktuelle Zustand. Um schließlich alle auf dem 11On12-Gerät ausgeführten Befehle an die freigegebene [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue)zu übermitteln, müssen wir [**Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) für [**id3D11DeviceContext**](/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext)aufrufen.

``` syntax
// Render text over D3D12 using D2D via the 11On12 device.
void D3D1211on12::RenderUI()
{
    D2D1_SIZE_F rtSize = m_d2dRenderTargets[m_frameIndex]->GetSize();
    D2D1_RECT_F textRect = D2D1::RectF(0, 0, rtSize.width, rtSize.height);
    static const WCHAR text[] = L"11On12";

    // Acquire our wrapped render target resource for the current back buffer.
    m_d3d11On12Device->AcquireWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Render text directly to the back buffer.
    m_d2dDeviceContext->SetTarget(m_d2dRenderTargets[m_frameIndex].Get());
    m_d2dDeviceContext->BeginDraw();
    m_d2dDeviceContext->SetTransform(D2D1::Matrix3x2F::Identity());
    m_d2dDeviceContext->DrawTextW(
        text,
        _countof(text) - 1,
        m_textFormat.Get(),
        &textRect,
        m_textBrush.Get()
        );
    ThrowIfFailed(m_d2dDeviceContext->EndDraw());

    // Release our wrapped render target resource. Releasing 
    // transitions the back buffer resource to the state specified
    // as the OutState when the wrapped resource was created.
    m_d3d11On12Device->ReleaseWrappedResources(m_wrappedBackBuffers[m_frameIndex].GetAddressOf(), 1);

    // Flush to submit the 11 command list to the shared command queue.
    m_d3d11DeviceContext->Flush();
}
```



| Aufrufflow                                                                                                                                                                                 | Parameter                            |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| [**D2D1 \_ SIZE \_ F**](/windows/desktop/Direct2D/d2d1-size-f)                                                                                                                                                 |                                       |
| [**D2D1 \_ RECT \_ F**](/windows/desktop/Direct2D/d2d1-rect-f)                                                                                                                                                 | [**RectF**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rectf)           |
| [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)                                                                                                               |                                       |
| [**ID2D1DeviceContext::SetTarget**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-settarget)                                                                                                                |                                       |
| [**ID2D1RenderTarget::BeginDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw)                                                                                                                  |                                       |
| [**ID2D1RenderTarget::SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform)                                                                                                            | [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) |
| [**ID2D1RenderTarget::D rawTextW**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) |                                       |
| [**ID2D1RenderTarget::EndDraw**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)                                                                                                                      |                                       |
| [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)                                                                                                               |                                       |
| [**ID3D11DeviceContext::Flush**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush)                                                                                                                    |                                       |



 

## <a name="run-the-sample"></a>Ausführen des Beispiels

![die endgültige Ausgabe des Beispiels "11 on 12"](images/11on12image.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Exemplarische Vorgehensweisen zu D3D12-Code](d3d12-code-walk-throughs.md)
</dt> <dt>

[Direct3D 11 on 12](direct3d-11-on-12.md)
</dt> <dt>

[Direct3D 12-Interop](direct3d-12-interop.md)
</dt> <dt>

[11on12-Referenz](direct3d-11on12-reference.md)
</dt> </dl>

 

 