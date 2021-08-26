---
title: Swapchains
description: Austauschketten steuern die Hintergrundpufferrotation und bilden die Grundlage der Grafikanimation.
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e98fc2baf63d7d80fefc190f2d01da33ea24d420e647b4f0c57df7ec4c501f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119850650"
---
# <a name="swap-chains"></a>Swapchains

Austauschketten steuern die Hintergrundpufferrotation und bilden die Grundlage der Grafikanimation.

## <a name="overview"></a>Übersicht

Das Programmiermodell für Austauschketten in Direct3D 12 ist nicht identisch mit dem in früheren Versionen von D3D. Die Programmierfreundlichkeit der Unterstützung der automatischen Ressourcenrotation, die in D3D10 und D3D11 vorhanden war, wird jetzt nicht mehr unterstützt. Die automatische Ressourcenrotation aktiviert Apps, um dasselbe API-Objekt zu rendern, während die tatsächliche Oberfläche, die gerendert wird, jeden Frame ändert. Das Verhalten von Austauschketten wird mit Direct3D 12 geändert, um anderen Features von Direct3D 12 einen geringen CPU-Mehraufwand zu ermöglichen. Automatische Farbtasten und Multisampling werden nicht unterstützt, insbesondere Stretching und Drehung sind dies jedoch weiterhin.

### <a name="buffer-lifetime"></a>Pufferlebensdauer

Apps dürfen vorab erstellte Deskriptoren speichern, die auf Rückpuffer verweisen. Dies wird aktiviert, indem sichergestellt wird, dass sich der Satz von Puffern, die sich im Besitz einer Austauschkette befinden, während der Lebensdauer der Swapkette nie ändert. Der Satz von Puffern, die von [**IDXGISwapChain::GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) zurückgegeben werden, ändert sich erst, wenn bestimmte APIs aufgerufen werden:

-   [**IDXGISwapChain::ResizeTarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**IDXGISwapChain::ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

Die Reihenfolge der von [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) zurückgegebenen Puffer ändert sich nie.

[**IDXGISwapChain3::GetCurrentBackBufferIndex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) gibt den Index des aktuellen Zurückpuffers an die App zurück.

### <a name="swap-effects"></a>Swap-Effekte

Die einzigen unterstützten Swapeffekte sind [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) und [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect), für die die Pufferanzahl größer als 1 sein muss.

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>Übergang zwischen Fenstermodus und Vollbildmodus

Direct3D 12 unterstützt den exklusiven Vollbildmodus (Full-Screen Exclusive Mode, FSE) nicht. Wenn ein Spiel die einzige sichtbare Anwendung auf dem Bildschirm ist, verwendet das Betriebssystem stattdessen eine Strategie namens Vollbild-Beeinträchtigungen (FSO), um einen ähnlichen Effekt wie FSE ohne die Leistungsnachteile zu erzielen. Weitere Informationen zum FSO finden Sie unter [Demystifying Fullscreen 2016 .](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/)

Direct3D 12 behält die Einschränkung bei, dass Anwendungen [**ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) nach dem Übergang zwischen Fenster- und Vollbildmodus aufrufen müssen (D3D11-Flip-Model-Austauschketten haben die gleichen Einschränkungen).

Die [**Übergänge IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) ändern nicht den Satz der für die App sichtbaren Puffer in der Swapkette. Nur die [**Aufrufe ResizeBuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) und [**ResizeTarget erstellen**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) oder zerstören für die App sichtbare Puffer. In Direct3D 12 [**wechselt IDXGISwapChain::SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) jedoch nicht in den exklusiven Vollbildmodus und ändert einfach auflösungs- und aktualisierungsraten, um Vollbild-Bildschirme zu ermöglichen. Diese Änderungen können von einer App ohne verwendung dieser Methode vorgenommen werden.

Wenn oder [**IDXGISwapChain::P resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) oder [**IDXGISwapChain1::P resent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) aufgerufen wird, muss der anzuzeigende Backpuffer den Zustand [**D3D12 \_ RESOURCE STATE \_ \_ PRESENT**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) haben. Bei vorhanden tritt ein **Fehler mit DXGI \_ ERROR INVALID CALL \_ \_ auf,** wenn dies nicht der Fall ist.

Für Vollbild-Swapketten gilt weiterhin die Einschränkung, dass [**SetFullscreenState**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(FALSE, NULL) vor der endgültigen Freigabe der Swapkette aufgerufen werden muss. **SetFullscreenState**(FALSE) ist bei Austauschketten erfolgreich, die auf Direct3D 12-Geräten ausgeführt werden.

Aktuelle Vorgänge treten in der 3D-Warteschlange auf, die bei der Erstellung der Swapchain bereitgestellt wird, und Apps können mehrere Swapketten gleichzeitig präsentieren und Befehlslisten aufzeichnen und ausführen.

Wenn der letzte Teil der Grafikarbeit (z. B. Frame-Nachverarbeitung) für eine Computewarteschlange durchgeführt wird oder die Grafikwarteschlange des Geräts nicht umfasst, kann das Erstellen einer zweiten 3D-Warteschlange, die auf angezeigt werden soll, von Vorteil sein und die Latenz der Präsentation verhindern, die den Start des nächsten Frames verzögert. 

### <a name="example"></a>Beispiel

Der folgende Beispielcode wäre in der Hauptrenderingschleife vorhanden:

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>Erstellen von Swapketten

Beachten Sie bei Verwendung der Aufrufe [**CreateSwapChainForHwnd,**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd) [**CreateSwapChainForCoreWindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)oder [**CreateSwapChainForComposition,**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) dass der *pDevice-Parameter* tatsächlich einen Zeiger auf eine direkte Befehlswarteschlange in Direct3D 12 und kein Gerät erfordert.

### <a name="presenting-on-windows-7"></a>Präsentation auf Windows 7

Wenn Direct3D 12 auf Windows 7 als Ziel verwendet wird, sind die erforderlichen DXGI-Typen für Direct3D 12 nicht vorhanden. Daher müssen Sie die von D3D12On7 bereitgestellte **ID3D12CommandQueueDownLevel** (abgefragt aus der direkten Befehlswarteschlange) verwenden, um dies zu präsentieren.

Sie stellen eine offene Befehlsliste für die Windows 7-Methode zur Verfügung, die dann verwendet, geschlossen und automatisch für Sie an das Gerät übermittelt wird. Sie müssen einen Backpuffer bereitstellen, der von der App erstellt werden muss, eine Ressource sein muss, für die ein Committed erstellt wurde, ein Einzelstichproben erstellt werden müssen und eines der folgenden Formate sein muss.

* **DXGI_FORMAT_R16G16B16A16_FLOAT**
* **DXGI_FORMAT_R10G10B10A2_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**
* **DXGI_FORMAT_B8G8R8X8_UNORM**
* **DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**

## <a name="related-topics"></a>Zugehörige Themen

* [D3D12_HEAP_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)
* [Videotutorials für erweitertes Lernen mit DirectX: Unthrottled Framerate](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [Rendering](rendering.md)
