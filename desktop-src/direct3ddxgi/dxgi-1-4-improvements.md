---
description: Die folgende Funktionalität wurde in Microsoft DirectX Graphic Infrastructure (DXGI) 1.4 hinzugefügt oder geändert, hauptsächlich zur Unterstützung von Direct3D 12.
ms.assetid: DEA901EA-B0F9-41D9-802C-ED1D6A7888E0
title: DXGI 1.4-Verbesserungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aef5777f50a149da6ccb2893bcac8a8f509c86cdff40d94889155c2e5e1eb12c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118289554"
---
# <a name="dxgi-14-improvements"></a>DXGI 1.4-Verbesserungen

Die folgende Funktionalität wurde in Microsoft DirectX Graphic Infrastructure (DXGI) 1.4 hinzugefügt oder geändert, hauptsächlich zur Unterstützung von Direct3D 12.

## <a name="cheaper-adapter-enumeration"></a>Kostengünstigere Adapterenumeration

Für Direct3D 12 ist es nicht mehr möglich, eine Rückverfolgung von einem Gerät zum [**IDXGIAdapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) zu erstellen, der zum Erstellen verwendet wurde. Es ist auch nicht mehr möglich, D3D \_ DRIVER \_ TYPE \_ WARP in [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)bereitzustellen. Um die Entwicklung zu vereinfachen, können Sie [**IDXGIFactory4**](/windows/win32/api/DXGI1_4/nn-dxgi1_4-idxgifactory4) verwenden, um beides zu behandeln. [**IDXGIFactory4::EnumAdapterByLuid**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid) (für die Paarung mit [**ID3D12Device::GetAdapterLuid**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)konzipiert) ermöglicht einer App das Abrufen von Informationen über den Adapter, auf dem ein Direct3D 12-Gerät erstellt wurde. [**IDXGIFactory4::EnumWarpAdapter**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter) stellt einen Adapter bereit, der **für D3D12CreateDevice** bereitgestellt werden kann, um den WARP-Renderer zu verwenden.

## <a name="video-memory-budget-tracking"></a>Videospeicher-Budgetnachverfolgung

Anwendungsentwicklern wird empfohlen, ein Videospeicherreservierungssystem zu verwenden, um das Betriebssystem über die Menge des physischen Videospeichers zu informieren, auf den die App nicht verzichten kann.

Der für einen Prozess verfügbare physische Arbeitsspeicher wird als "Videospeicherbudget" bezeichnet. Das Budget kann merklich schwanken, wenn Hintergrundprozesse reaktivieren und in den Standbymodus versetzt werden. und schwanken erheblich, wenn der Benutzer zu einer anderen Anwendung wechselt. Die Anwendung kann benachrichtigt werden, wenn sich das Budget ändert und sowohl das aktuelle Budget als auch die aktuell verbrauchte Arbeitsspeichermenge abgefragt werden. Wenn eine Anwendung nicht innerhalb ihres Budgets bleibt, wird der Prozess zeitweilig eingefroren, damit andere Anwendungen ausgeführt werden können, und/oder die Erstellungs-APIs geben Fehler zurück. Die [**IDXGIAdapter3-Schnittstelle**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) stellt die Methoden für diese Funktionalität bereit, insbesondere [**QueryVideoMemoryInfo**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) und [**RegisterVideoMemoryBudgetChangeNotificationEvent.**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent)

Weitere Informationen finden Sie im Thema Direct3D 12 unter [Residency](../direct3d12/residency.md).

## <a name="direct3d-12-swapchain-changes"></a>Direct3D 12 Swapchain Changes

Einige der vorhandenen Direct3D 11-Austauschkettenfunktionen wurden als veraltet angesehen, um die Mehraufwandsreduzierungen in Direct3D 12 zu erzielen. Während andere Änderungen vorgenommen wurden, wurden entweder an Direct3D 12-Konzepten ausgerichtet oder bieten eine bessere Unterstützung für Direct3D 12-Features.

**Invariante Backbuffer-Identität**

In Direct3D 11 konnten Anwendungen [**GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer)aufrufen ( 0, ... ) nur einmal. Jeder Aufruf von [**Present**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-present) hat die Ressourcenidentität der zurückgegebenen Schnittstelle implizit geändert. Direct3D 12 unterstützt diese implizite Änderung der Ressourcenidentität aufgrund des erforderlichen CPU-Aufwands und des flexiblen Ressourcendeskriptorentwurfs nicht mehr. Daher muss die Anwendung **GetBuffer** für jeden Puffer, der mit der Swapchain erstellt wurde, manuell aufrufen. Die Anwendung muss nach dem Aufruf von **Present** manuell in den nächsten Puffer in der Sequenz gerendert werden. Anwendungen wird empfohlen, einen Cache von Deskriptoren für jeden Puffer zu erstellen, anstatt viele Objekte neu zu erstellen, die jeweils **vorhanden sind.**

**Unterstützung mehrerer Adapter**

Wenn eine Swapkette auf einem Multi-GPU-Adapter erstellt wird, werden alle Backbuffer auf Knoten 1 erstellt, und es wird nur eine einzige Befehlswarteschlange unterstützt. [**ResizeBuffers1**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1) ermöglicht Anwendungen das Erstellen von Backbuffern auf verschiedenen Knoten, sodass jeweils eine andere Befehlswarteschlange verwendet werden kann. Diese Funktionen ermöglichen die Verwendung von AFR-Techniken (Alternate Frame Rendering) mit der Swapchain. Weitere Informationen finden Sie unter Systeme mit [mehreren Adaptern.](../direct3d12/multi-engine.md)

**Verschiedenes**

-   Anstelle des Direct3D 12-Geräteobjekts muss ein Befehlswarteschlangenobjekt an [**CreateSwapChain-Methoden**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-createswapchain) übergeben werden.
-   Es werden nur die beiden folgenden Flip-Modellaustauscheffekte unterstützt: <dl> DXGI \_ SWAP EFFECT FLIP DISCARD sollte bevorzugt werden, wenn Anwendungen vor der Präsentation vollständig über den \_ \_ \_ Backbuffer gerendert werden oder an der einfachen Unterstützung von Szenarien mit mehreren Adaptern interessiert sind.  
    DXGI \_ SWAP EFFECT FLIP SEQUENTIAL sollte von Anwendungen verwendet \_ \_ \_ werden, die Teilpräsentationsoptimierungen verwenden oder regelmäßig aus zuvor präsentierten Backbuffern lesen.  
    </dl>
-   [**SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) no longer exclusively owns the display, so user-initiated operating system elements can seamlessly appear in front of application output. Volume settings is an example of this.

## <a name="related-topics"></a>Zugehörige Themen

[Direct3D 12-Hardwarefeatureebenen](../direct3d12/hardware-feature-levels.md)

[Programmierhandbuch für DXGI](dx-graphics-dxgi-overviews.md)
