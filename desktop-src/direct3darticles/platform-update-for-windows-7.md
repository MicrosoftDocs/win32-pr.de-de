---
title: Plattformupdate für Windows 7
description: In diesem Thema werden Verbesserungen an Komponenten des grafikstapels Windows 7 beschrieben, die über das Plattformupdate für Windows 7 verfügbar werden.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a577d74613a22a176c038b6c85e53b94f413edbc49d07a886a613ddff5a83b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627580"
---
# <a name="platform-update-for-windows-7"></a>Plattformupdate für Windows 7

In diesem Thema werden Verbesserungen an den Komponenten des Windows 7-Grafikstapels beschrieben, die über das [Plattformupdate für Windows 7](https://support.microsoft.com/kb/2670838)verfügbar werden.

Wenn das Plattformupdate für Windows 7 auf Windows 7 installiert ist, Windows 7 mit funktionen, die in Windows 8 verfügbar sind. Beispielsweise werden diese Windows 8 Komponenten mit voller Funktionalität verfügbar:

-   Direct2D 1.1 (einschließlich Direct2D-Effekte)
-   DirectWrite
-   Windows Imaging-Komponente (WIC)

Diese bieten partielle Funktionen:

-   Direct3D 11.1
-   DXGI 1.2

Diese Komponente ist beispielsweise nicht verfügbar:

-   DirectComposition (DComp)

In diesen Themen finden Sie Informationen zu Direct2D, DirectWrite und WIC mit dem Plattformupdate:

-   [Neuerungen in Direct2D für Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Neuerungen in DirectWrite für Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Neuerungen bei WIC in Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

In diesen Themen finden Sie Informationen zu Direct3D und DXGI mit dem Plattformupdate:

-   [D3D11.1-Features](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [DXGI 1.2-Verbesserungen](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

Nachdem das Plattformupdate installiert wurde, sind die in Direct3D11.1 und DXGI 1.2 eingeführten Schnittstellen mit teilweiser Funktionalität verfügbar. Die Features dieser Grafikkomponenten sind direkt an die Grafikkernelkomponenten, Grafiktreiber und Grafikhardware gebunden. Bevor Sie Direct3D11.1 auf Windows 7 verwenden, müssen Sie mit diesen Besonderheiten vertraut sein:

-   Windows 8 das WDDM 1.2-Treibermodell eingeführt, das Verbesserungen auf der zugeordneten API-Oberfläche für alle [Featureebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)bereitstellte. Wenn Sie die Direct3D11.1-Dokumentation lesen, sollten Sie wissen, dass *neue Treiber* WDDM 1.2-Treiber bedeuten. Diese aktualisierten Treiberversionen sowie die meisten optionalen Features, die über [**CheckFeatureSupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport)verfügbar gemacht werden, sind auf Windows 7 nicht verfügbar. Da es keine Garantie gibt, dass diese optionalen Features verfügbar sind, stellen Sie sicher, dass Ihre Anwendungen über ein geeignetes Fallbackverhalten verfügen, falls die gewünschte Funktionalität nicht verfügbar ist.

    Es gibt eine wichtige Ausnahme. Mehrere Features, z. B. [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) mit konstanten Pufferoffsets, erfordern neue Treiber für [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10 und höher, werden aber tatsächlich für Featureebene 9 emuliert. Diese Emulation ist auf Windows 7 mit dem Plattformupdate verfügbar. Weitere Informationen dazu, welche Features emuliert werden, finden Sie unter [**\_ \_ \_ D3D11 FEATURE DATA D3D11 \_ OPTIONS**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .

-   Das Windows 8 WDDM 1.2-Treibermodell unterstützt eine neue Generation von Hardware, die über die [D3D-Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.1 verfügbar gemacht wird. Windows 7 mit dem Plattformupdate unterstützt nur das WDDM 1.1-Treibermodell. Daher ist die Hardwareunterstützung auf Featureebene 11.1 (über das Plattformupdate) nicht verfügbar. Auf Windows 7 mit dem Plattformupdate gibt [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) immer eine Featureebene von 11.0 oder niedriger zurück, mit Ausnahme von mit einem Referenzgerät, das zum Testen eines 11.1-Codepfads auf Windows 7 verwendet werden kann. Verwenden Sie nur Features, die auf Ihren Zielfunktionsebenen verfügbar sind, wie in der Referenz zur Featureebene beschrieben.
-   Einige neue Methoden, die in DGXI 1.2 eingeführt wurden, werden mit dem Plattformupdate für Windows 7 nicht vollständig unterstützt. Sie können die Verfügbarkeit dieser Funktionen testen, indem Sie sie direkt aufrufen und nach einem Fehlercode suchen. Stellen Sie sicher, dass Ihre Anwendungen, die Windows 7 mit dem Plattformupdate als Ziel verwenden, über einen Fallback verfügen, wenn die gewünschte Funktionalität nicht verfügbar ist. Diese Klassen von Features sind im Plattformupdate für Windows 7 nicht verfügbar:

    -   Stereo
    -   Swapchains, die nicht auf Hwnds ausgerichtet sind
    -   Benachrichtigungen zum Verdeckungsstatus
    -   Desktopduplizierung
    -   NT-Handleressourcen

    Insbesondere geben die folgenden APIs DXGI \_ ERROR \_ UNSUPPORTED, DXGI \_ ERROR INVALID \_ \_ CALL, E \_ NOTIMPL oder E \_ INVALIDARG zurück:

    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForComposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterStereoStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterStereoStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**RegisterOcclusionStatusEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**UnregisterOcclusionStatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**DuplicateOutput**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**EnqueueSetEvent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)::[**CreateSharedHandle**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**GetSharedResourceAdapterLuid**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResourceByName**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   Diese APIs weisen Verhaltensunterschiede auf, wie bereits erwähnt:
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**CreateSwapChainForHwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) verwendet eine [**DXGI \_ SWAP CHAIN \_ \_ DESC1-Struktur,**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) die über ein Feld für **die Skalierung** verfügt. [**DXGI \_ SCALE \_ NONE**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) wird auf Windows 7 mit dem Plattformupdate nicht unterstützt und bewirkt, dass **CreateSwapChainForHwnd** \_ DXGI ERROR INVALID CALL \_ zurückgibt, wenn aufgerufen \_ wird.
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) ist nur nützlich, wenn für eine Swapkette mit DXGI SCALING NONE festgelegt \_ \_ wird. Der Wert wird weiterhin gespeichert und kann abgerufen werden, hat aber keine Auswirkungen.
    -   [**IDXGIDisplayControl**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**IsStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled), [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**IsWindowedStereoEnabled**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)und [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**IsTemporaryMonoSupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) alle geben **FALSE** zurück.
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) und **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) wurden hinzugefügt, um Stereoanzeigemodi zu ermöglichen. Stereo wird im Plattformupdate für Windows 7 nicht unterstützt, daher entspricht diese Methode [**IDXGIOutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**FindClosestMatchingMode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) als [**DXGI \_ MODE \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1). Stereo ist immer FALSE.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**OfferResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) und **IDXGIDevice2**::[**ReclaimResources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) werden im Plattformupdate für Windows 7 nicht unterstützt. Die Runtime lässt jedoch weiterhin den Aufruf zu und überprüft, ob sie für nicht freigegebene Ressourcen ordnungsgemäß verwendet werden.
    -   [WARP-Geräte](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) unterstützen nur [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11.0. Das heißt, WARP-Geräte, die durch Übergeben von [D3D \_ DRIVER \_ TYPE \_ WARP](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) im *DriverType-Parameter* von [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) erstellt wurden, unterstützen weder 11.1 noch freigegebene Oberflächen.
-   Für Entwickler, die derzeit an Anwendungen in Microsoft Visual Studio 2010 oder früher arbeiten und das [**\_ \_ \_ DEBUG-Flag D3D11 CREATE DEVICE**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) verwenden, sollten Sie beachten, dass Aufrufe von [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) fehlschlagen. Dies liegt daran, dass die D3D11.1-Runtime jetzt D3D11 \_1SDKLayers.dll anstelle von D3D11SDKLayers.dll erfordert. Um diese neue DLL (D3D11 \_1SDKLayers.dll) abzurufen, installieren Sie das [Windows 8 SDK](https://dev.windows.com/downloads/windows-8-sdk)oder [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)oder die Visual Studio 2012-Remotedebuggingtools. Weitere Informationen finden Sie in der Dokumentation zur [Debugebene.](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers)

 

 