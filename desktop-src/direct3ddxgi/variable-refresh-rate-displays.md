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
# <a name="variable-refresh-rate-displays"></a><span data-ttu-id="0256a-103">Variable Aktualisierungsrate anzeigen</span><span class="sxs-lookup"><span data-stu-id="0256a-103">Variable refresh rate displays</span></span>

<span data-ttu-id="0256a-104">Die Anzeige der Variablen Aktualisierungsrate erfordert, dass das *zerreißen* aktiviert wird. Dies wird auch als "VSYNC-Off"-Unterstützung bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="0256a-104">Variable refresh rate displays require *tearing* to be enabled, this is also known as "vsync-off" support.</span></span>

-   [<span data-ttu-id="0256a-105">Variable Aktualisierungsrate wird angezeigt/VSYNC deaktiviert</span><span class="sxs-lookup"><span data-stu-id="0256a-105">Variable refresh rate displays/Vsync off</span></span>](#variable-refresh-rate-displaysvsync-off)
-   [<span data-ttu-id="0256a-106">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0256a-106">Related topics</span></span>](#related-topics)

## <a name="variable-refresh-rate-displaysvsync-off"></a><span data-ttu-id="0256a-107">Variable Aktualisierungsrate wird angezeigt/VSYNC deaktiviert</span><span class="sxs-lookup"><span data-stu-id="0256a-107">Variable refresh rate displays/Vsync off</span></span>

<span data-ttu-id="0256a-108">Unterstützung für die Anzeige von Variablen Aktualisierungs Raten wird erreicht, indem beim Erstellen und darstellen der Swapkette bestimmte Flags festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0256a-108">Support for variable refresh rate displays is achieved by setting certain flags when creating and presenting the swap chain.</span></span>

<span data-ttu-id="0256a-109">Um dieses Feature verwenden zu können, müssen sich App-Benutzer auf Windows 10-Systemen befinden, auf denen entweder [KB3156421](https://support.microsoft.com/kb/3156421) oder das Anniversary Update installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0256a-109">To use this feature, app users need to be on Windows 10 systems with either [KB3156421](https://support.microsoft.com/kb/3156421) or the Anniversary Update installed.</span></span> <span data-ttu-id="0256a-110">Die Funktion funktioniert in allen Versionen von Direct3D 11 und 12 mithilfe von \**DXGI \_ Swap \_ Effect \_ Flip \_ \** _ Swap-Effekten.</span><span class="sxs-lookup"><span data-stu-id="0256a-110">The feature works on all versions of Direct3D 11 and 12 using \**DXGI\_SWAP\_EFFECT\_FLIP\_\** _ swap effects.</span></span>

<span data-ttu-id="0256a-111">Weitere Informationen zum Hinzufügen von VSYNC-off für Ihre apps finden Sie in einem Beispiel für eine komplette Ausführung für Direct3D 12, _ *D3D12Fullscreen*\* (siehe [funktionierende Beispiele](../direct3d12/working-samples.md)).</span><span class="sxs-lookup"><span data-stu-id="0256a-111">To add vsync-off support to your apps, you can refer to a complete running sample for Direct3D 12, _ *D3D12Fullscreen*\* (refer to [Working Samples](../direct3d12/working-samples.md)).</span></span> <span data-ttu-id="0256a-112">Es gibt auch einige Punkte, die nicht explizit im Beispielcode genannt werden, aber Sie müssen darauf achten.</span><span class="sxs-lookup"><span data-stu-id="0256a-112">There are also a few points not explicitly called out in the sample code but you need to pay attention to.</span></span>

-   <span data-ttu-id="0256a-113">[**Resizebuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (oder [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) muss das gleiche Flag für die Auslagerungs Ketten Erstellung (DXGI- \_ SwapChain- \_ \_ Flag \_ zulassen \_ ) als [**vorhanden**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (oder [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)) erhalten.</span><span class="sxs-lookup"><span data-stu-id="0256a-113">[**ResizeBuffers**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-resizebuffers) (or [**ResizeBuffers1**](/windows/desktop/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1)) must have the same swap chain creation flag (DXGI\_SWAP\_CHAIN\_FLAG\_ALLOW\_TEARING) passed to it as [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) (or [**Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)).</span></span>
-   <span data-ttu-id="0256a-114">DXGI \_ Present das Beenden \_ \_ kann nur mit dem Synchronisierungs Intervall 0 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0256a-114">DXGI\_PRESENT\_ALLOW\_TEARING can only be used with sync interval 0.</span></span> <span data-ttu-id="0256a-115">Es wird empfohlen, dieses Tränen Kennzeichen immer zu übergeben, wenn Sie das Synchronisierungs Intervall 0 verwenden, wenn [**checkfeaturesupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) meldet, dass das Zerreißen unterstützt wird *und* sich die APP im Fenstermodus befindet, einschließlich des Modus ohne Rand.</span><span class="sxs-lookup"><span data-stu-id="0256a-115">It is recommended to always pass this tearing flag when using sync interval 0 if [**CheckFeatureSupport**](/windows/desktop/api/DXGI1_5/nf-dxgi1_5-idxgifactory5-checkfeaturesupport) reports that tearing is supported *and* the app is in a windowed mode - including border-less fullscreen mode.</span></span> <span data-ttu-id="0256a-116">Weitere Informationen finden Sie in den [**DXGI \_ Present**](dxgi-present.md) -Konstanten.</span><span class="sxs-lookup"><span data-stu-id="0256a-116">Refer to the [**DXGI\_PRESENT**](dxgi-present.md) constants for more details.</span></span>
-   <span data-ttu-id="0256a-117">Durch das Deaktivieren von VSYNC wird Ihre Framerate nicht zwangsläufig aufgehoben: Entwickler müssen auch sicherstellen, dass [**vorhandene**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) Aufrufe nicht durch andere Zeit Steuerungs Ereignisse (z. b. das `CompositionTarget::Rendering` Ereignis in einer XAML-basierten APP) gedrosselt werden.</span><span class="sxs-lookup"><span data-stu-id="0256a-117">Disabling vsync does not necessarily uncap your frame rate: developers also need to make sure [**Present**](/windows/desktop/api/DXGI/nf-dxgi-idxgiswapchain-present) calls are not throttled by other timing events (such as the `CompositionTarget::Rendering` event in an XAML-based app).</span></span>

<span data-ttu-id="0256a-118">Mit dem folgenden Code werden einige wichtige Elemente, die Sie Ihren apps hinzufügen müssen, zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="0256a-118">The code below recaps a few key pieces you need to add to your apps.</span></span>

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

## <a name="related-topics"></a><span data-ttu-id="0256a-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0256a-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0256a-120">DXGI 1,5-Verbesserungen</span><span class="sxs-lookup"><span data-stu-id="0256a-120">DXGI 1.5 Improvements</span></span>](dxgi-1-5-improvements.md)
</dt> <dt>

[<span data-ttu-id="0256a-121">Programmier Handbuch für DXGI</span><span class="sxs-lookup"><span data-stu-id="0256a-121">Programming Guide for DXGI</span></span>](dx-graphics-dxgi-overviews.md)
</dt> </dl>

 

 
