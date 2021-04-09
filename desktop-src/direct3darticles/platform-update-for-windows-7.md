---
title: Platt Form Update für Windows 7
description: In diesem Thema werden die Verbesserungen der Komponenten des Windows 7-Grafik Stapels beschrieben, die über das Platt Form Update für Windows 7 verfügbar werden.
ms.assetid: C6DC0D38-E17C-4924-AF7C-6AE74C6C50D1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49fd1e6e2681673d2bb2bab7a4a6de42f77988eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858423"
---
# <a name="platform-update-for-windows-7"></a>Platt Form Update für Windows 7

In diesem Thema werden die Verbesserungen der Komponenten des Windows 7-Grafik Stapels beschrieben, die über das [Platt Form Update für Windows 7](https://support.microsoft.com/kb/2670838)verfügbar werden.

Bei der Installation unter Windows 7 aktualisiert das Platt Form Update für Windows 7 Windows 7 mit der Funktionalität, die in Windows 8 verfügbar ist. Beispielsweise werden diese Windows 8-Komponenten mit vollständiger Funktionalität verfügbar:

-   Direct2D 1,1 (einschließlich Direct2D-Effekten)
-   DirectWrite
-   Windows Imaging-Komponente (WIC)

Diese stellen partielle Funktionen bereit:

-   Direct3D 11,1
-   DXGI 1,2

Diese Komponente ist beispielsweise nicht verfügbar:

-   Directcomposition (Dcomp)

Informationen zu Direct2D, DirectWrite und WIC mit dem Platt Form Update finden Sie in den folgenden Themen:

-   [Neues in Direct2D für Windows 8 (Windows)](/windows/desktop/Direct2D/what-s-new-in-direct2d-for-windows-8-consumer-preview)
-   [Neues in DirectWrite für Windows 8 (Windows)](/windows/desktop/DirectWrite/what-s-new-in-directwrite-for-windows-8-consumer-preview)
-   [Neuerungen bei WIC in Windows 8 (Windows)](/previous-versions//hh994467(v=vs.85))

Weitere Informationen zu Direct3D und DXGI mit dem Platt Form Update finden Sie in den folgenden Themen:

-   [D3D 11.1-Features](/windows/desktop/direct3d11/direct3d-11-1-features)
-   [DXGI 1,2-Verbesserungen](/windows/desktop/direct3ddxgi/dxgi-1-2-improvements)

Nachdem das Platt Form Update installiert wurde, werden die in Direct3D 11.1 und DXGI 1,2 eingeführten Schnittstellen mit partieller Funktionalität zur Verfügung gestellt. Die Funktionen dieser Grafik Komponenten sind direkt an die Grafik-Kernel Komponenten, Grafiktreiber und Grafikhardware gebunden. Bevor Sie Direct3D 11.1 unter Windows 7 verwenden, sollten Sie sich mit diesen Besonderheiten vertraut machen:

-   In Windows 8 wurde das WDDM 1,2-Treibermodell eingeführt, das in der zugehörigen API-Oberfläche für alle [Funktionsebenen](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)Verbesserungen bereitstellte. Beachten Sie beim Lesen der Dokumentation zu Direct3D 11.1, dass *neue Treiber* WDDM 1,2-Treiber bedeuten. Diese aktualisierten Treiberversionen und die meisten optionalen Features, die über [**checkfeaturesupport**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport)verfügbar gemacht werden, sind unter Windows 7 nicht verfügbar. Da es keine Garantie gibt, dass diese optionalen Features verfügbar sind, sollten Sie sicherstellen, dass Ihre Anwendungen über geeignete Fall Back Verhalten verfügen, wenn die gewünschte Funktionalität nicht verfügbar ist.

    Es gibt eine wichtige Ausnahme. Mehrere Features, wie z. b. [**PSSetConstantBuffers1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-pssetconstantbuffers1) mit Konstanten Puffer Offsets, erfordern neue Treiber für die [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10 und höher, werden aber tatsächlich für Featureebene 9 emuliert. Diese Emulation ist unter Windows 7 mit dem Platt Form Update verfügbar. Weitere Informationen zu den emulierten Funktionen finden Sie unter [**D3D11 \_ Feature \_ Data \_ D3D11 \_ options**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_feature_data_d3d11_options) .

-   Das Windows 8 WDDM 1,2-Treibermodell unterstützt eine neue Generation von Hardware, die über D3D [Feature Level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,1 verfügbar gemacht wird. Windows 7 mit dem Platt Form Update unterstützt nur das WDDM 1,1-Treibermodell. Daher ist die Featureebene 11,1 Hardwareunterstützung nicht verfügbar (über das Platt Form Update). Unter Windows 7 mit dem Platt Form Update gibt [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) stets eine featurestufe von 11,0 oder niedriger zurück, mit Ausnahme von mit einem Referenzgerät, das zum Testen eines 11,1-Codepfade unter Windows 7 verwendet werden kann. Verwenden Sie nur die Funktionen, die auf den Ziel Funktionsebenen verfügbar sind, wie in der featurelevelreferenz beschrieben.
-   Einige neue Methoden, die in DGXI 1,2 eingeführt werden, werden mit dem Platt Form Update für Windows 7 nicht vollständig unterstützt. Sie können die Verfügbarkeit dieser Funktionen testen, indem Sie Sie direkt aufrufen und auf einen Fehlercode überprüfen. Stellen Sie sicher, dass Ihre Anwendungen für Windows 7 mit dem Platt Form Update ein Fall Back haben, wenn die gewünschte Funktionalität nicht verfügbar ist. Diese Funktionsklassen sind für das Platt Form Update für Windows 7 nicht verfügbar:

    -   Stereo
    -   Swapketten, die nicht auf HWNDs abzielen
    -   Status Benachrichtigungen für Okklusion
    -   Desktop Duplizierung
    -   NT-handle-Ressourcen

    Die folgenden APIs geben einen nicht unterstützten DXGI- \_ Fehler \_ , einen ungültigen DXGI- \_ Fehler \_ \_ , E \_ notimpl oder e \_ invalidArg zurück:

    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**kreateswapchadetailcorewindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**kreateswapchainforcomposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**registerstereostatus Window**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**registerstereostatuusevent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**unregisterstereostatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**registeroksionstatus Window**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**registeroksionstatus usevent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**unregisteroksionstatus**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**getcorewindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**segfizierung**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**GetRotation**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**duplicateoutput**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**einqueuesetevent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
    -   [**IDXGIResource1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiresource1)::[**kreatesharedhandle**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**getsharedresourceadapterluid**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**OpenSharedResource1**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
    -   [**ID3D11Device1**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11device1)::[**opensharedresourcebyname**](/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)

-   Diese APIs weisen Verhaltensunterschiede auf, wie bereits erwähnt:
    -   [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**kreateswapchainforhwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) nimmt eine [**DXGI \_ - \_ SwapChain \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1) -Struktur mit einem Feld für die **Skalierung** an. [**DXGI \_ Das \_ skalieren**](/windows/desktop/api/dxgi1_2/ne-dxgi1_2-dxgi_scaling) von "keine" wird unter Windows 7 mit dem Platt Form Update unterstützt und bewirkt, dass " **anateswapchainforhwnd** " einen \_ \_ ungültigen \_ Aufruf von DXGI-Fehlern zurückgibt
    -   [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**SetBackgroundColor**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor) ist nur nützlich, wenn für eine vorhandenes SwapChain mit DXGI- \_ Skalierung None festgelegt wird \_ . Der Wert wird weiterhin gespeichert und kann abgerufen werden, hat jedoch keine Auswirkungen.
    -   [**Idxgidisplaycontrol**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidisplaycontrol)::[**isstereoaktivierte**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled), [**IDXGIFactory2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgifactory2)::[**iswindowedstereoaktivierte**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)und [**IDXGISwapChain1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1)::[**istemporarymonosupported**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported) geben alle den Wert **false** zurück.
    -   [**IDXGIOutput1**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgioutput1)::[**GetDisplayModeList1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1) und **IDXGIOutput1**::[**FindClosestMatchingMode1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1) wurden hinzugefügt, um die Stereo Anzeigemodi zu vereinfachen. Stereo wird auf dem Platt Form Update für Windows 7 nicht unterstützt, sodass diese Methode [**idxgioutput**](/windows/desktop/api/dxgi/nn-dxgi-idxgioutput)::[**findclosestmatchingmode**](/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode) als [**DXGI- \_ Modus \_ DESC1**](/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_mode_desc1)entspricht. Stereo ist immer false.
    -   [**IDXGIDevice2**](/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgidevice2)::[**offerresources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-offerresources) und **IDXGIDevice2**::[**reclaimresources**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) werden für das Platt Form Update für Windows 7 nicht unterstützt. Allerdings können Sie von der Laufzeit weiterhin aufgerufen werden, und es wird überprüft, ob Sie für nicht freigegebene Ressourcen ordnungsgemäß verwendet werden.
    -   [Warp](/windows/desktop/direct3d11/overviews-direct3d-11-devices-create-warp) -Geräte unterstützen nur die [Featureebene](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 11,0. Das heißt, dass Warp-Geräte, die durch Übergeben von [D3D \_ Driver \_ Type \_ Warp](/windows/desktop/api/d3dcommon/ne-d3dcommon-d3d_driver_type) im *DriverType* -Parameter von [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) erstellt werden, nicht 11,1 unterstützen und keine freigegebenen Oberflächen unterstützen.
-   Für Entwickler, die zurzeit an Anwendungen in Microsoft Visual Studio 2010 oder früher mit dem [**D3D11 \_ Create \_ Device \_ Debug**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_create_device_flag) -Flag arbeiten, sollten Sie beachten, dass Aufrufe an [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice) fehlschlagen. Dies liegt daran, dass die D3D 11.1-Laufzeit jetzt D3D11- \_1SDKLayers.dll anstelle D3D11SDKLayers.dll erfordert. Um diese neue dll (D3D11 \_1SDKLayers.dll) zu erhalten, installieren Sie das [Windows 8 SDK](https://dev.windows.com/downloads/windows-8-sdk), [Visual Studio 2012](https://www.microsoft.com/visualstudio/eng/downloads)oder die remotedebuggingtools für Visual Studio 2012. Weitere Informationen finden Sie in der Dokumentation zur [debugschicht](/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers) .

 

 