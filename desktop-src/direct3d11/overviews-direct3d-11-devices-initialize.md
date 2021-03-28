---
title: Erstellen eines Geräts und unmittelbaren Kontexts
description: In diesem Thema wird gezeigt, wie Sie ein Gerät initialisieren.
ms.assetid: 02a20ada-b3aa-435e-8d66-117a19222f9f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 530f2b9cbc77f5404b4e9e8973d326a8708d6436
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039020"
---
# <a name="how-to-create-a-device-and-immediate-context"></a>Gewusst wie: Erstellen eines Geräts und eines unmittelbaren Kontexts

In diesem Thema wird gezeigt, wie Sie ein [Gerät](overviews-direct3d-11-devices-intro.md)initialisieren. Die Initialisierung eines [Geräts](overviews-direct3d-11-devices-intro.md) ist eine der ersten Aufgaben, die Ihre Anwendung abschließen muss, bevor Sie Ihre Szene Rendering können.

**So erstellen Sie ein Gerät und unmittelbaren Kontext**

Füllen Sie die [**\_ \_ \_ DESC-Struktur der DXGI-Austausch Kette**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) mit Informationen zu Puffer Formaten und-Dimensionen aus. Weitere Informationen finden Sie unter Erstellen einer Austausch Kette.

Im folgenden Codebeispiel wird veranschaulicht, wie die [**\_ \_ \_ DESC-Struktur der DXGI-Swap-Kette**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) ausgefüllt wird.


```
DXGI_SWAP_CHAIN_DESC sd;
ZeroMemory( &sd, sizeof( sd ) );
sd.BufferCount = 1;
sd.BufferDesc.Width = 640;
sd.BufferDesc.Height = 480;
sd.BufferDesc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
sd.BufferDesc.RefreshRate.Numerator = 60;
sd.BufferDesc.RefreshRate.Denominator = 1;
sd.BufferUsage = DXGI_USAGE_RENDER_TARGET_OUTPUT;
sd.OutputWindow = g_hWnd;
sd.SampleDesc.Count = 1;
sd.SampleDesc.Quality = 0;
sd.Windowed = TRUE;
```



Verwenden Sie die [**DXGI- \_ SwapChain \_ \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) -Struktur aus Schritt 1, und nennen Sie [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) , um das Gerät zu initialisieren und die Kette gleichzeitig auszutauschen.


```
D3D_FEATURE_LEVEL  FeatureLevelsRequested = D3D_FEATURE_LEVEL_11_0;
UINT               numLevelsRequested = 1;
D3D_FEATURE_LEVEL  FeatureLevelsSupported;

if( FAILED (hr = D3D11CreateDeviceAndSwapChain( NULL, 
                D3D_DRIVER_TYPE_HARDWARE, 
                NULL, 
                0,
                &FeatureLevelsRequested, 
                numFeatureLevelsRequested, 
                D3D11_SDK_VERSION, 
                &sd, 
                &g_pSwapChain, 
                &g_pd3dDevice, 
                &FeatureLevelsSupported,
                &g_pImmediateContext )))
{
    return hr;
}
```



> [!Note]  
> Wenn Sie auf einem Computer, auf dem nur die Direct3D 11,0-Laufzeit vorhanden ist, ein Gerät der [**D3D- \_ Funktions \_ Ebene \_ 11 \_ 1**](/windows/desktop/api/D3DCommon/ne-d3dcommon-d3d_feature_level) anfordern, wird [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) sofort mit **E \_ invalidArg** beendet. Um alle möglichen featureebenen auf einem Computer mit der DirectX 11,0-oder DirectX 11,1-Laufzeit sicher anzufordern, verwenden Sie den folgenden Code:
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>const D3D_FEATURE_LEVEL lvl[] = { D3D_FEATURE_LEVEL_11_1, D3D_FEATURE_LEVEL_11_0,
> D3D_FEATURE_LEVEL_10_1, D3D_FEATURE_LEVEL_10_0,
> D3D_FEATURE_LEVEL_9_3, D3D_FEATURE_LEVEL_9_2, D3D_FEATURE_LEVEL_9_1 };
>
> UINT createDeviceFlags = 0;
> #ifdef _DEBUG
> createDeviceFlags |= D3D11_CREATE_DEVICE_DEBUG;
> #endif
>
> ID3D11Device* device = nullptr;
> HRESULT hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, lvl, _countof(lvl), D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> if ( hr == E_INVALIDARG )
> {
>     hr = D3D11CreateDeviceAndSwapChain( nullptr, D3D_DRIVER_TYPE_HARDWARE, nullptr, createDeviceFlags, &lvl[1], _countof(lvl) - 1, D3D11_SDK_VERSION, &sd, &g_pSwapChain, &g_pd3ddevice, &FeatureLevelsSupported, &g_pImmediateContext );
> }
>
> if (FAILED(hr))
>     return hr;</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
>  
>
> Erstellen Sie eine renderzielsicht durch Aufrufen von [**ID3D11Device:: createrendertargetview**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createrendertargetview) , und binden Sie den Back Puffer als Renderziel durch Aufrufen von [**Verknüpfung id3d11devicecontext aus:: omstrendertargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets).
>
> <span codelanguage=""></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <tbody>
> <tr class="odd">
> <td><pre><code>ID3D11Texture2D* pBackBuffer;
>
> // Get a pointer to the back buffer
> hr = g_pSwapChain->GetBuffer( 0, __uuidof( ID3D11Texture2D ), 
>                              ( LPVOID* )&pBackBuffer );
>
> // Create a render-target view
> g_pd3dDevice->CreateRenderTargetView( pBackBuffer, NULL,
>                                       &g_pRenderTargetView );
>
> // Bind the view
> g_pImmediateContext->OMSetRenderTargets( 1, &g_pRenderTargetView, NULL );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> Erstellen Sie einen Viewport, um zu definieren, welche Teile des Renderziels sichtbar sind. Definieren Sie den Viewport mithilfe der [**D3D11 \_ Viewport**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) -Struktur, und legen Sie den Viewport mithilfe der [**Verknüpfung id3d11devicecontext aus:: rssetviewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) -Methode fest.
>
> <span codelanguage="ManagedCPlusPlus"></span>
>
> <table>
> <colgroup>
> <col style="width: 100%" />
> </colgroup>
> <thead>
> <tr class="header">
> <th>C++</th>
> </tr>
> </thead>
> <tbody>
> <tr class="odd">
> <td><pre><code>    // Setup the viewport
>     D3D11_VIEWPORT vp;
>     vp.Width = 640;
>     vp.Height = 480;
>     vp.MinDepth = 0.0f;
>     vp.MaxDepth = 1.0f;
>     vp.TopLeftX = 0;
>     vp.TopLeftY = 0;
>     g_pImmediateContext->RSSetViewports( 1, &vp );</code></pre></td>
> </tr>
> </tbody>
> </table> 
>
> ## <a name="related-topics"></a>Zugehörige Themen
>
> <dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>
>
>  
>
>  
>