---
description: Die folgende Funktionalität wurde in der Microsoft DirectX Graphics Infrastructure (DXGI) 1,2 hinzugefügt.
ms.assetid: E2D8DA99-4EA2-4847-B699-80A6994C66C0
title: DXGI 1.2-Verbesserungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bd274918d179bc7adeb8dd132fe604cf56d80f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346387"
---
# <a name="dxgi-12-improvements"></a>DXGI 1.2-Verbesserungen

Die folgende Funktionalität wurde in der Microsoft DirectX Graphics Infrastructure (DXGI) 1,2 hinzugefügt.

## <a name="presentation-enhancements-and-optimizations"></a>Verbesserungen und Optimierungen der Präsentation

DXGI 1,2 verbessert die Präsentation mit einer neuen Swap-Kette des Flip-Modells, Inhalts Schutz, fensterlosen Darstellung und optimierter Präsentation, bei der Sie modifizierte Rechtecke und gescrollt Bereiche angeben. Die Präsentation wird auch durch das Verhalten der Stereotyp-3D angezeigt.

Zum Verbessern der Darstellung können Sie die folgende DXGI 1,2-API verwenden.

-   [**Idxgidisplaycontrol:: isstereoaktivierte**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-isstereoenabled)
-   [**Idxgidisplaycontrol:: setstereoaktivierte**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgidisplaycontrol-setstereoenabled)
-   [**IDXGIFactory2:: kreateswapchainforhwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)
-   [**IDXGIFactory2:: kreateswapchadetailcorewindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)
-   [**IDXGIFactory2:: kreateswapchainforcomposition**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition)
-   [**IDXGIFactory2:: iswindowedstereoaktivierte**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-iswindowedstereoenabled)
-   [**IDXGIFactory2:: registerstereostatus Window**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatuswindow)
-   [**IDXGIFactory2:: registerstereostatuusevent**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-registerstereostatusevent)
-   [**IDXGIFactory2:: unregisterstereostatus**](/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-unregisterstereostatus)
-   [**IDXGIFactory2:: registeroksionstatus Window**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatuswindow)
-   [**IDXGIFactory2:: registeroksionstatus usevent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-registerocclusionstatusevent)
-   [**IDXGIFactory2:: unregisteroksionstatus**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-unregisterocclusionstatus)
-   [**IDXGIOutput1::GetDisplayModeList1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaymodelist1)
-   [**IDXGIOutput1::GetDisplaySurfaceData1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-getdisplaysurfacedata1)
-   [**IDXGIOutput1::FindClosestMatchingMode1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-findclosestmatchingmode1)
-   [**IDXGIResource1:: kreatesubresourcesurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsubresourcesurface)
-   [**IDXGISurface2:: GetResource**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgisurface2-getresource)
-   [**IDXGISwapChain1::GetDesc1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1)
-   [**IDXGISwapChain1:: getfullscreendebug**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getfullscreendesc)
-   [**IDXGISwapChain1:: GetHwnd**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-gethwnd)
-   [**IDXGISwapChain1:: getcorewindow**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getcorewindow)
-   [**IDXGISwapChain1::Present1**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-present1)
-   [**IDXGISwapChain1:: istemporarymonosupported**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported)
-   [**IDXGISwapChain1:: getrestrictdeoutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrestricttooutput)
-   [**IDXGISwapChain1:: SetBackgroundColor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setbackgroundcolor)
-   [**IDXGISwapChain1:: getbackgroundcolor**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getbackgroundcolor)
-   [**IDXGISwapChain1:: segfizierung**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-setrotation)
-   [**IDXGISwapChain1:: GetRotation**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiswapchain1-getrotation)

Weitere Informationen zur Verwendung der DXGI 1,2-API für die erweiterte Darstellung finden Sie unter [verbessern der Präsentation mit dem Flip-Modell, Dirty Rechtecke und scrollt](dxgi-1-2-presentation-improvements.md).

Informationen dazu, wie Sie bestimmen können, ob Sie in Stereo rendern können, finden Sie unter [Rendering in Stereo und Benachrichtigen von Stereo Status](stereo-rendering-stereo-status-notifying.md).

Informationen zum Bestimmen von Änderungen im Status der APP-oksion finden Sie unter [warten auf ein Ereignis, wenn das Rendering unnötig ist](waiting-when-occluded.md).

Informationen dazu, wie sich Datenwerte ändern, wenn Sie Inhalte auf dem Bildschirm darstellen, finden Sie unter [umwandeln von Daten für den Farbraum](converting-data-color-space.md).

## <a name="desktop-duplication"></a>Desktop Duplizierung

Windows 8 deaktiviert standardmäßige Windows 2000-Anzeigetreiber Modell-Spiegel Treiber (XDDM). DXGI 1,2 stellt die desktopduplizierungs-API als Alternative bereit. Die Desktop Duplizierungs-API bietet Remote Zugriff auf das Desktop Image für Zusammenarbeits Szenarien.

Die Desktop Duplizierungs-API besteht aus den folgenden Methoden.

-   [**IDXGIOutput1::D uplicateoutput**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutput1-duplicateoutput)
-   [**Idxgioutputduplizierung:: getdebug**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getdesc)
-   [**Idxgioutputduplizierung:: acquunesextframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-acquirenextframe)
-   [**Idxgioutputduplizierung:: getframedirtyrects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframedirtyrects)
-   [**Idxgioutputduplizierung:: getframemuverects**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframemoverects)
-   [**Idxgioutputduplizierung:: getframepointershape**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-getframepointershape)
-   [**Idxgioutputduplizierung:: mapdesktopsurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-mapdesktopsurface)
-   [**Idxgioutputduplizierung:: unmapdesktopsurface**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-unmapdesktopsurface)
-   [**Idxgioutputduplizierung:: releaseframe**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgioutputduplication-releaseframe)

Weitere Informationen zum Verwenden der Desktop Duplizierungs-API finden Sie unter [Desktop Duplizierung API](desktop-dup-api.md).

## <a name="improved-usage-of-shared-resources-and-synchronized-events"></a>Verbesserte Verwendung von freigegebenen Ressourcen und synchronisierten Ereignissen

In früheren Versionen von Windows verwenden apps kontinuierliches abrufen, um zu bestimmen, ob die Verarbeitung beliebiger Befehle von der Grafikverarbeitungseinheit (GPU) abgeschlossen ist. DXGI 1,2 ermöglicht einer APP, ein Ereignis an ein DXGI-Gerät in die Warteschlange zu stellen. Die APP kann dann warten, bis das DXGI-Gerät das Ereignis signalisiert, um zu ermitteln, ob die GPU alle renderingbefehle ausgeführt hat. DXGI 1,2 ermöglicht mehreren Geräten das Freigeben einer Ressource über ein NT-handle.

Sie können die folgende DXGI 1,2-API und die Direct3D 11,1-API verwenden, um Ressourcen freizugeben und Ereignisse zu synchronisieren.

-   [**IDXGIDevice2:: einqueuesetevent**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-enqueuesetevent)
-   [**IDXGIResource1:: kreatesharedhandle**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiresource1-createsharedhandle)
-   [**IDXGIFactory2:: getsharedresourceadapterluid**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgifactory2-getsharedresourceadapterluid)
-   [**ID3D11Device1::OpenSharedResource1**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresource1)
-   [**ID3D11Device1:: opensharedresourcebyname**](/windows/win32/api/d3d11_1/nf-d3d11_1-id3d11device1-opensharedresourcebyname)
-   [**D3D11 \_ \_ ressourcenmisc \_ Shared \_ nthandle**](/windows/win32/api/d3d11/ne-d3d11-d3d11_resource_misc_flag)

## <a name="offer-the-video-memory-of-resources"></a>Videospeicher für Ressourcen anbieten

DXGI 1,2 ermöglicht einer APP, den Videospeicher ihrer Ressourcen mit geringem Verwaltungsaufwand anzubieten. Durch die Bereitstellung des Video Speichers kann das Betriebssystem den Videospeicher freigeben.

Diese Funktion von DXGI 1,2 besteht aus den folgenden Methoden.

-   [**IDXGIDevice2:: offerresources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources)
-   [**IDXGIDevice2:: reclaimresources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources)

Sie können die [**ID3D11Debug:: setfeaturemask**](/windows/win32/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask) -Methode verwenden, um Merkmals Masken-Flags festzulegen, die das Verhalten der Methoden [**IDXGIDevice2:: offerresources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-offerresources) und [**IDXGIDevice2:: reclaimresources**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgidevice2-reclaimresources) in Ihrer APP Debuggen.

## <a name="gpu-preemption-at-finer-granularity-levels-for-wddm-12-driver-model"></a>GPU-vorzeitig Entfernung auf präzisere Granularitätsstufen für das WDDM 1,2-Treibermodell

Beginnend mit dem Windows Display Driver Model (WDDM) 1,2-Treibermodell kann der WDDM-Scheduler der GPU die Ausführung von Anwendungs Tasks auf präzisere Granularitätsebene voranstellen. Mit DXGI 1,2 können Sie die Granularitätsebene der GPU-voremption bestimmen.

Diese Funktion von DXGI 1,2 besteht aus der folgenden Methode.

-   [**IDXGIAdapter2::GetDesc2**](/windows/desktop/api/DXGI1_2/nf-dxgi1_2-idxgiadapter2-getdesc2)

## <a name="debugging-apis"></a>Debugging-APIs

Das Windows 8 SDK bietet zusätzliche Debuggingfunktionen. Sie können die folgenden DXGI-APIs aus Dxgidebug.dll verwenden, um Ihre APP zu Debuggen:

-   [**Dxgigetdebug-Schnittstelle**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)
-   [**Idxgidebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug)
-   [**Idxgiinfoqueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue)

Um auf [**dxgigetdebug Interface**](/windows/desktop/api/DXGIDebug/nf-dxgidebug-dxgigetdebuginterface)zuzugreifen, müssen Sie die [**GetModuleHandle**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulehandlea) -Funktion aufrufen, um Dxgidebug.dll und die [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion abzurufen, um die Adresse von **dxgigetdebug Interface** abzurufen. Sie können dann **dxgigetdebuginterface** aufrufen, um die [**idxgidebug**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgidebug) -oder [**idxgiinfoqueue**](/windows/desktop/api/DXGIDebug/nn-dxgidebug-idxgiinfoqueue) -Schnittstelle zu erhalten.

Informationen zum Remote Debuggen von DirectX-apps finden Sie unter [Remote Debuggen von DirectX-apps](../direct3dtools/debugging-directx-apps-remotely.md).

## <a name="related-topics"></a>Zugehörige Themen

[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)
