---
title: Austausch Ketten
description: Austausch Ketten steuern die Hintergrund Puffer Drehung und bilden die Grundlage der Grafik Animation.
ms.assetid: AABF5FDE-DB49-4B29-BC0E-032E0C7DF9EB
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbc7ec1b62ba620b42bc85c1c1f491ff7ba952d
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2021
ms.locfileid: "104548695"
---
# <a name="swap-chains"></a>Austausch Ketten

Austausch Ketten steuern die Hintergrund Puffer Drehung und bilden die Grundlage der Grafik Animation.

## <a name="overview"></a>Überblick

Das Programmiermodell für Swapketten in Direct3D 12 ist nicht identisch mit dem in früheren Versionen von D3D. Die Programmier Unterstützung, z. b. die Unterstützung automatischer Ressourcen Rotation, die in d3d10 und D3D11 vorhanden war, wird jetzt nicht unterstützt. Automatische Ressourcen Rotation aktivierte Apps zum Rendern desselben API-Objekts, während die tatsächliche Oberfläche gerendert wird, ändert jeden Frame. Das Verhalten von Swapketten wird mit Direct3D 12 geändert, damit andere Features von Direct3D 12 einen niedrigen CPU-Overhead haben. Automatischer Farbschlüssel und multisamplinggrad werden nicht unterstützt, obwohl das Strecken und drehen immer noch ist.

### <a name="buffer-lifetime"></a>Puffer Lebensdauer

Apps dürfen vorab erstellte Deskriptoren speichern, die auf die Puffer verweisen, die aktiviert werden, indem sichergestellt wird, dass sich der Satz von Puffern, die sich im Besitz einer Swapkette befinden, für die Lebensdauer der Swapkette nie ändert Der von [**idxgiswapchain:: GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) zurückgegebene Puffer Satz ändert sich erst, wenn bestimmte APIs aufgerufen werden:

-   [**Idxgiswapchain:: resizetarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget)
-   [**Idxgiswapchain:: resizebuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers)

Die Reihenfolge der von [**GetBuffer**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer) zurückgegebenen Puffer ändert sich nie.

[**IDXGISwapChain3:: getcurrentbackbufferindex**](/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex) gibt den Index des aktuellen Hintergrund Puffers an die APP zurück.

### <a name="swap-effects"></a>Auslagerungs Effekte

Die einzigen unterstützten Auslagerungs Effekte sind [**DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect) und [**DXGI_SWAP_EFFECT_FLIP_DISCARD**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_effect). Dies erfordert, dass die Puffer Anzahl größer als 1 ist.

### <a name="transitioning-between-windowed-and-full-screen-modes"></a>Übergang zwischen dem Fenstermodus und dem Vollbildmodus

Direct3D 12 unterstützt den Vollbildmodus exklusiv (FSE) nicht. Wenn ein Spiel die einzige sichtbare Anwendung auf dem Bildschirm ist, verwendet das Betriebssystem stattdessen eine Strategie namens Vollbild-Optimierungen (Full-Screen Optimierungen, FSO), um eine ähnliche Auswirkung auf FSE zu erzielen, ohne die Leistungs Nachteile zu erzielen. Weitere Informationen zu "f" finden Sie unter [Demystifying Fullscreen Optimierungen](https://devblogs.microsoft.com/directx/demystifying-full-screen-optimizations/).

Direct3D 12 behält die Einschränkung bei, dass Anwendungen [**resizebuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) nach dem Übergang zwischen den Fenster-und Vollbildmodi aufrufen müssen (D3D11 Flip-Model-Swapketten haben dieselben Einschränkungen).

Die [**idxgiswapchain:: setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) -Übergänge ändern nicht den Satz der für die APP sichtbaren Puffer in der SwapChain. Nur die [**resizebuffers**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers) und [**resizetarget**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget) -Aufrufe rufen App-sichtbare Puffer auf. Allerdings wechselt [**idxgiswapchain:: setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate) in Direct3D 12 nicht in den Vollbildmodus und ändert einfach Auflösungen und Aktualisierungs Raten, um voll Bild Optimierungen zu ermöglichen. Diese Änderungen können von einer APP ohne Verwendung dieser Methode vorgenommen werden.

Wenn oder [**idxgiswapchain::P Resent**](/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present) oder [**IDXGISwapChain1::P Resent**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1) aufgerufen wird, muss sich der zurück zugegende Hintergrund Puffer im Status " [**D3D12 \_ Resource \_ State \_ Present**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states) " befinden. Der vorhandene Fehler tritt mit einem **\_ \_ ungültigen \_ DXGI-Fehler** auf, wenn dies nicht der Fall ist.

Vollbild-Austausch Ketten verfügen weiterhin über die Einschränkung, dass [**setfullscreenstate**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate)(false, null) vor der endgültigen Freigabe der Swapkette aufgerufen werden muss. **Setfullscreenstate**(false) ist für Swapketten erfolgreich, die auf Direct3D 12-Geräten ausgeführt werden.

Aktuelle Vorgänge erfolgen in der 3D-Warteschlange, die bei der vorhandenes SwapChain-Erstellung bereitgestellt wird. Apps können gleichzeitig mehrere Swapketten präsentieren und Befehlslisten aufzeichnen und ausführen.

Wenn der letzte Teil der Grafik (z. b. Frame-Postprocessing) für eine computewarteschlange ausgeführt wird oder die Grafik Warteschlange des Geräts nicht umfasst, kann das Erstellen einer zweiten 3D-Warteschlange, die in vorhanden ist, von Vorteil sein und die Latenz der Präsentation verhindern, die den Beginn des nächsten Frames verzögert. 

### <a name="example"></a>Beispiel

Der folgende Beispielcode wäre in der Haupt-Renderingschleife enthalten:

```cpp
void Present()
{
    m_swapChain->Present(0, m_presentFlags);
    m_backBufferIndex = (m_backBufferIndex + 1) % m_backBufferCount;
}
```

### <a name="creating-swap-chains"></a>Erstellen von Austausch Ketten

Beachten Sie bei der Verwendung der Aufrufe " [**anateswapchadetailhwnd**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd)", " [**kreateswapchadetailcorewindow**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow)" oder " [**anateswapchadetailcomposition**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition) ", dass der *pdevice* -Parameter tatsächlich einen Zeiger auf eine direkte Befehls Warteschlange in Direct3D 12 und kein Gerät erfordert.

### <a name="presenting-on-windows-7"></a>Darstellung in Windows 7

Wenn Sie Direct3D 12 auf Windows 7 abzielen, sind die erforderlichen DXGI-Typen für Direct3D 12 nicht vorhanden. Daher müssen Sie die von D3D12On7 bereitgestellte **ID3D12CommandQueueDownLevel** (abgefragt von der direkten Befehls Warteschlange) verwenden, um zu präsentieren.

Sie stellen eine geöffnete Befehlsliste für die Windows 7-Methode bereit, die dann verwendet, geschlossen und automatisch an das Gerät gesendet wird. Sie müssen einen Hintergrund Puffer bereitstellen, der von der App erstellt werden muss, eine Zugesicherte Ressource sein muss, nur mit einem Sampling versehen werden muss und einem der folgenden Formate unterliegen muss.

* **DXGI_FORMAT_R16G16B16A16_FLOAT**
* **DXGI_FORMAT_R10G10B10A2_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM**
* **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB**
* **DXGI_FORMAT_B8G8R8X8_UNORM**
* **DXGI_FORMAT_R10G10B10_XR_BIAS_A2_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM**
* **DXGI_FORMAT_B8G8R8A8_UNORM_SRGB**

## <a name="related-topics"></a>Verwandte Themen

* [D3D12_HEAP_FLAGS](/windows/win32/api/d3d12/ne-d3d12-d3d12_heap_flags)
* [Video-Tutorials zu DirectX Advanced Learning: nicht gedrosselt Framerate](https://www.youtube.com/watch?v=wn02zCXa9IU)
* [Darstellung](rendering.md)
