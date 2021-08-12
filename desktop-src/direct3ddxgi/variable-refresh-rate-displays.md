---
description: Variable Aktualisierungsrate zeigt an, dass die Löschung aktiviert werden muss. Dies wird auch als unterstützung für &\# 0034;vsync-off&\# 0034; bezeichnet.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Variable Aktualisierungsrate wird angezeigt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349592ce49d1008f6337b53c7f524ac7303907f75cd99205fe79bf55988b934b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118288923"
---
# <a name="variable-refresh-rate-displays"></a>Variable Aktualisierungsrate wird angezeigt

Variable Aktualisierungsrate zeigt an, dass *das Löschen* aktiviert werden muss. Dies wird auch als "vsync-off"-Unterstützung bezeichnet.

-   [Variable Aktualisierungsrate wird angezeigt/Vsync deaktiviert](#variable-refresh-rate-displaysvsync-off)
-   [Zugehörige Themen](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>Variable Aktualisierungsrate wird angezeigt/Vsync deaktiviert

Die Unterstützung für die Anzeige variabler Aktualisierungsrate wird erreicht, indem bestimmte Flags beim Erstellen und Darstellen der Swapkette festgelegt werden.

Um dieses Feature verwenden zu können, müssen sich App-Benutzer auf Windows 10 Systemen mit [installierten KB3156421-](https://support.microsoft.com/kb/3156421) oder Anniversary Update-Systemen befingen. Das Feature funktioniert für alle Versionen von Direct3D 11 und 12 mit **DXGI \_ SWAP EFFECT \_ \_ \_ \* FLIP-Swapeffekten.**

Informationen zum Hinzufügen von vsync-off-Unterstützung zu Ihren Apps finden Sie in einem vollständig ausgeführten Beispiel für Direct3D 12, **D3D12Fullscreen** (siehe [Working Samples](../direct3d12/working-samples.md)). Es gibt auch einige Punkte, die im Beispielcode nicht explizit erwähnt werden, aber Sie müssen darauf achten.

-   [**Für ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (oder [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) muss dasselbe Flag für die Erstellung der Swapkette (DXGI \_ SWAP CHAIN FLAG ALLOW \_ \_ \_ \_ TEARING) als [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (oder [**Present1)**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)übergeben werden.
-   DXGI \_ PRESENT \_ ALLOW \_ TEARING kann nur mit dem Synchronisierungsintervall 0 verwendet werden. Es wird empfohlen, dieses Löschflag bei Verwendung des Synchronisierungsintervalls 0 immer zu übergeben, wenn [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) meldet, dass das Löschen unterstützt wird *und* sich die App in einem Fenstermodus befindet – einschließlich des rahmenfreien Vollbildmodus. Weitere Informationen finden Sie in den [**DXGI \_ PRESENT-Konstanten.**](dxgi-present.md)
-   Durch das Deaktivieren von vsync wird die Framerate nicht [](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) unbedingt aufgehoben: Entwickler müssen auch sicherstellen, dass Present-Aufrufe nicht durch andere Zeitsteuerungsereignisse gedrosselt werden (z. B. das `CompositionTarget::Rendering` Ereignis in einer XAML-basierten App).

Der folgende Code fasst einige wichtige Teile zusammen, die Sie Ihren Apps hinzufügen müssen.

``` syntax
//--------------------------------------------------------------------------------------------------------
// Check Tearing Support
//--------------------------------------------------------------------------------------------------------

// Determines whether tearing support is available for fullscreen borderless windows.

void DXSample::CheckTearingSupport()
{
// Rather than create the 1.5 factory interface directly, we create the 1.4
// interface and query for the 1.5 interface. This will enable the graphics
// debugging tools which might not support the 1.5 factory interface.

    ComPtr<IDXGIFactory4> factory4;
    HRESULT hr = CreateDXGIFactory1(IID_PPV_ARGS(&factory4));
    BOOL allowTearing = FALSE;
    if (SUCCEEDED(hr))
    { 
        ComPtr<IDXGIFactory5> factory5;
        hr = factory4.As(&factory5);
        if (SUCCEEDED(hr))
        {
            hr = factory5->CheckFeatureSupport(DXGI_FEATURE_PRESENT_ALLOW_TEARING, &allowTearing, sizeof(allowTearing));
        }
    }
    m_tearingSupport = SUCCEEDED(hr) && allowTearing;
}

//--------------------------------------------------------------------------------------------------------
// Set up swapchain properly
//--------------------------------------------------------------------------------------------------------

// It is recommended to always use the tearing flag when it is supported.
swapChainDesc.Flags = m_tearingSupport ? DXGI_SWAP_CHAIN_FLAG_ALLOW_TEARING : 0;

//--------------------------------------------------------------------------------------------------------
// Present
//--------------------------------------------------------------------------------------------------------

UINT presentFlags = (m_tearingSupport && m_windowedMode) ? DXGI_PRESENT_ALLOW_TEARING : 0;

// Present the frame.
ThrowIfFailed(m_swapChain->Present(0, presentFlags));
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DXGI 1.5-Verbesserungen](dxgi-1-5-improvements.md)
</dt> <dt>

[Programmierhandbuch für DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
