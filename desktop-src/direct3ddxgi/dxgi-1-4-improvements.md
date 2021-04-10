---
description: Die folgende Funktionalität wurde in der Microsoft DirectX Graphics Infrastructure (DXGI) 1,4 hinzugefügt oder geändert, größtenteils zur Unterstützung von Direct3D 12.
ms.assetid: DEA901EA-B0F9-41D9-802C-ED1D6A7888E0
title: DXGI 1,4-Verbesserungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24e9a8a48dd026248afac7c1a7df23a99176adef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104041163"
---
# <a name="dxgi-14-improvements"></a>DXGI 1,4-Verbesserungen

Die folgende Funktionalität wurde in der Microsoft DirectX Graphics Infrastructure (DXGI) 1,4 hinzugefügt oder geändert, größtenteils zur Unterstützung von Direct3D 12.

## <a name="cheaper-adapter-enumeration"></a>Günstigere adapterenumeration

Bei Direct3D 12 ist es nicht mehr möglich, von einem Gerät auf den [**idxgiadapter**](/windows/win32/api/DXGI/nn-dxgi-idxgiadapter) zu verweisen, der zum Erstellen verwendet wurde. Es ist auch nicht mehr möglich, D3D \_ Driver \_ Type \_ Warp in [**D3D12CreateDevice**](/windows/win32/api/d3d12/nf-d3d12-d3d12createdevice)bereitzustellen. Um die Entwicklung zu vereinfachen, können Sie [**IDXGIFactory4**](/windows/win32/api/DXGI1_4/nn-dxgi1_4-idxgifactory4) verwenden, um beides zu bewältigen. [**IDXGIFactory4:: einumadapterbyluid**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumadapterbyluid) (in Kombination mit [**ID3D12Device:: getadapterluid**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getadapterluid)) ermöglicht einer APP das Abrufen von Informationen über den Adapter, auf dem ein Direct3D 12-Gerät erstellt wurde. [**IDXGIFactory4:: enumwarpadapter**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgifactory4-enumwarpadapter) stellt einen Adapter bereit, der für **D3D12CreateDevice** zur Verwendung des Warp-Renderers bereitgestellt werden kann.

## <a name="video-memory-budget-tracking"></a>Budgetüberwachung für Video Speicher

Anwendungsentwicklern wird empfohlen, ein Reservierungssystem für den Videospeicher zu verwenden, um das Betriebssystem über die Menge an physischem Videospeicher zu informieren, ohne dass die APP nicht mehr verwendet werden kann

Die Menge an physischem Arbeitsspeicher, der für einen Prozess verfügbar ist, wird als "Videospeicher Budget" bezeichnet. Das Budget kann merklich schwanken, wenn sich Hintergrundprozesse reaktivieren und im Standbymodus befinden. und schwanken erheblich, wenn der Benutzer zu einer anderen Anwendung wechselt. Die Anwendung kann benachrichtigt werden, wenn sich das Budget ändert, und sowohl das aktuelle Budget als auch den aktuell verbrauchten Arbeitsspeicher abrufen. Wenn eine Anwendung nicht innerhalb Ihres Budgets bleibt, wird der Prozess zeitweise eingefroren, damit andere Anwendungen ausgeführt werden können und/oder die Erstellungs-APIs einen Fehler zurückgeben. Die [**IDXGIAdapter3**](/windows/win32/api/dxgi1_4/nn-dxgi1_4-idxgiadapter3) -Schnittstelle stellt die Methoden bereit, die diese Funktionalität betreffen, insbesondere [**queryvideomemoryinfo**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-queryvideomemoryinfo) und [**registervideomemorybudgetchangenotificationevent**](/windows/win32/api/dxgi1_4/nf-dxgi1_4-idxgiadapter3-registervideomemorybudgetchangenotificationevent).

Weitere Informationen finden Sie im Thema zu Direct3D 12 unter [Residenz](../direct3d12/residency.md).

## <a name="direct3d-12-swapchain-changes"></a>Direct3D 12 SwapChain-Änderungen

Einige der vorhandenen Direct3D 11-vorhandenes SwapChain-Funktionen wurden als veraltet markiert, um die Verringerung des Aufwands in Direct3D 12 zu erzielen. Während andere Änderungen vorgenommen wurden, um entweder an Direct3D 12-Konzepten auszurichten oder eine bessere Unterstützung für Direct3D 12-Funktionen bereitzustellen.

**Invariante BackBuffer-Identität**

In Direct3D 11 können Anwendungen [**GetBuffer**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-getbuffer)(0,... ) nur einmal. Jeder-aufruter hat die Ressourcen Identität der zurückgegebenen Schnitt [**Stelle implizit geändert**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-present) . Direct3D 12 unterstützt diese implizite Ressourcen Identitäts Änderung aufgrund des erforderlichen CPU-Aufwands und des flexiblen Ressourcen deskriptorentwurfs nicht mehr. Folglich muss die Anwendung **GetBuffer** für jeden mit SwapChain erstellten Puffer manuell aufrufen. Die Anwendung muss nach dem Aufruf von " **Present**" manuell zum nächsten Puffer in der Sequenz Rendering werden. Anwendungen wird empfohlen, für jeden Puffer einen Cache von Deskriptoren zu erstellen, anstatt viele Objekte neu zu erstellen, die jeweils **vorhanden** sind.

**Unterstützung für mehrere Adapter**

Wenn eine vorhandenes SwapChain auf einem Multi-GPU-Adapter erstellt wird, werden alle backbuffers auf Knoten 1 erstellt, und nur eine einzige Befehls Warteschlange wird unterstützt. [**ResizeBuffers1**](/windows/win32/api/DXGI1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1) ermöglicht es Anwendungen, BackBuffer auf verschiedenen Knoten zu erstellen, sodass jeweils eine andere Befehls Warteschlange verwendet werden kann. Diese Funktionen ermöglichen das Verwenden alternativer Frame Rendering (AFR)-Techniken für die SwapChain. Weitere Informationen finden Sie unter [Systeme mit mehreren Adaptern](../direct3d12/multi-engine.md).

**Verschiedenes**

-   Ein Befehls Warteschlangen-Objekt muss an die Methoden " [**anateswapchain**](/windows/win32/api/DXGI/nf-dxgi-idxgifactory-createswapchain) " anstatt an das Direct3D 12-Geräte Objekt übergeben werden.
-   Nur die folgenden zwei Auslagerungs Effekte im Flip-Modell werden unterstützt: <dl> Der DXGI- \_ \_ swapffekt \_ kippen \_ sollte bevorzugt werden, wenn Anwendungen vor der Darstellung vollständig über den Swapkette werden oder wenn Sie daran interessiert sind, Szenarien mit mehreren Adaptern zu unterstützen.  
    Der DXGI- \_ \_ swapffekt \_ \_ , der aufeinander folgt, sollte von Anwendungen verwendet werden, die auf partiellen Präsentations Optimierungen basieren oder regelmäßig aus zuvor dargestellten backbuffers lesen.  
    </dl>
-   [**SetFullscreenState**](/windows/win32/api/DXGI/nf-dxgi-idxgiswapchain-setfullscreenstate) no longer exclusively owns the display, so user-initiated operating system elements can seamlessly appear in front of application output. Volume settings is an example of this.

## <a name="related-topics"></a>Zugehörige Themen

[Direct3D 12-Hardware Funktionsebenen](../direct3d12/hardware-feature-levels.md)

[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)
