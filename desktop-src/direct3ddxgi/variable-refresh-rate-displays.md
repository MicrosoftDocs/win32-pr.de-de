---
description: Die Aktualisierung der Variablen Aktualisierungsrate erfordert, dass das Zerreißen aktiviert ist. Dies wird auch als &\# 0034; VSYNC-off&\# 0034;-Unterstützung bezeichnet.
ms.assetid: C5F140DD-5BAF-404A-9253-611831C4D424
title: Variable Aktualisierungsrate anzeigen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da6e658d84c51a6b51bc32855226194b9c22507e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213878"
---
# <a name="variable-refresh-rate-displays"></a>Variable Aktualisierungsrate anzeigen

Die Anzeige der Variablen Aktualisierungsrate erfordert, dass das *zerreißen* aktiviert wird. Dies wird auch als "VSYNC-Off"-Unterstützung bezeichnet.

-   [Variable Aktualisierungsrate wird angezeigt/VSYNC deaktiviert](#variable-refresh-rate-displaysvsync-off)
-   [Zugehörige Themen](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a>Variable Aktualisierungsrate wird angezeigt/VSYNC deaktiviert

Unterstützung für die Anzeige von Variablen Aktualisierungs Raten wird erreicht, indem beim Erstellen und darstellen der Swapkette bestimmte Flags festgelegt werden.

Um dieses Feature verwenden zu können, müssen sich App-Benutzer auf Windows 10-Systemen befinden, auf denen entweder [KB3156421](https://support.microsoft.com/kb/3156421) oder das Anniversary Update installiert ist. Die Funktion funktioniert in allen Versionen von Direct3D 11 und 12 mithilfe von **DXGI \_ Swap \_ Effect \_ Flip \_ \** _ Swap-Effekten.

Weitere Informationen zum Hinzufügen von VSYNC-off für Ihre apps finden Sie in einem Beispiel für eine komplette Ausführung für Direct3D 12, _ *D3D12Fullscreen** (siehe [funktionierende Beispiele](../direct3d12/working-samples.md)). Es gibt auch einige Punkte, die nicht explizit im Beispielcode genannt werden, aber Sie müssen darauf achten.

-   [**Resizebuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (oder [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) muss das gleiche Flag für die Auslagerungs Ketten Erstellung (DXGI- \_ SwapChain- \_ \_ Flag \_ zulassen \_ ) als [**vorhanden**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (oder [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)) erhalten.
-   DXGI \_ Present das Beenden \_ \_ kann nur mit dem Synchronisierungs Intervall 0 verwendet werden. Es wird empfohlen, dieses Tränen Kennzeichen immer zu übergeben, wenn Sie das Synchronisierungs Intervall 0 verwenden, wenn [**checkfeaturesupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) meldet, dass das Zerreißen unterstützt wird *und* sich die APP im Fenstermodus befindet, einschließlich des Modus ohne Rand. Weitere Informationen finden Sie in den [**DXGI \_ Present**](dxgi-present.md) -Konstanten.
-   Durch das Deaktivieren von VSYNC wird Ihre Framerate nicht zwangsläufig aufgehoben: Entwickler müssen auch sicherstellen, dass [**vorhandene**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) Aufrufe nicht durch andere Zeit Steuerungs Ereignisse (z. b. das `CompositionTarget::Rendering` Ereignis in einer XAML-basierten APP) gedrosselt werden.

Mit dem folgenden Code werden einige wichtige Elemente, die Sie Ihren apps hinzufügen müssen, zusammengefasst.

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

[DXGI 1,5-Verbesserungen](dxgi-1-5-improvements.md)
</dt> <dt>

[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
