---
description: Die folgende Funktionalität wurde in der Microsoft DirectX Graphics Infrastructure (DXGI) 1,3 hinzugefügt, die in Windows 8.1 enthalten ist.
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: DXGI 1,3-Verbesserungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c863bc30ffdf27705492b56a5348040c8e12f4fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860130"
---
# <a name="dxgi-13-improvements"></a>DXGI 1,3-Verbesserungen

Die folgende Funktionalität wurde in der Microsoft DirectX Graphics Infrastructure (DXGI) 1,3 hinzugefügt, die in Windows 8.1 enthalten ist.

## <a name="trim-dxgi-adapter-memory-usage"></a>Speicherauslastung für DXGI-Adapter kürzen

Ab Windows 8.1 fügt DXGI 1,3 die Möglichkeit hinzu, nicht verwendete Speicherressourcen, die vom DXGI-Adapter zugeordnet werden, zu leeren und freizugeben. Dadurch können apps temporären Arbeitsspeicher freigeben, während angehalten wird. Dadurch wird die Wahrscheinlichkeit verringert, dass die APP beendet wird, um Ressourcen für andere apps freizugeben. Wenn die APP fortgesetzt wird, werden Gerätetreiber, die Trim unterstützen, Ressourcen nach Bedarf neu erstellen. Ab Windows 8.1 müssen alle Direct3D-Geräte, die von einer App erstellt werden, beim Anhalten [**"idxgidevice3:: Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) aufgerufen werden, um den Speicherbedarf zu verringern und die Wahrscheinlichkeit zu verringern, dass die APP beendet wird, um Systemressourcen freizugeben.

## <a name="multi-plane-overlays"></a>Überlagerungen mit mehreren Ebenen

Ab Windows 8.1 unterstützt DXGI 1,3 Überlagerungen mit mehreren Ebenen. Sie können herausfinden, ob das Gerät Überlagerungen mit mehreren Ebenen in der Hardware unterstützt, indem Sie [**IDXGIOutput2:: supportsoverlay**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays)verwenden.

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>Überlappende Austausch Ketten und die Skalierungs Ketten Skalierung

Ab Windows 8.1 unterstützt DXGI 1,3 überlappende Austausch Ketten. Überlappende Austausch Ketten werden verwendet, um 3D-Grafiken in nicht systemeigenen Auflösungen (mit Hardware-upskalierung) zu zeichnen, während die Benutzeroberfläche bei der systemeigenen Auflösung Dadurch können Spiele höhere Füll Raten für reaktionsfähiges Spiel nutzen, ohne die visuelle Qualität von UI-Elementen zu beeinträchtigen, wie z. b. Player Bewertung und Dialog Text. Auf Geräten, die Überlagerungen mit mehreren Ebenen unterstützen, verwendet Direct3D multiebenenüberlagerungen für überlappende Austausch Ketten. Erstellen Sie eine vorlagerungs Kette, indem Sie beim Erstellen der SwapChain das Flag der [**\_ \_ \_ \_ Vorder \_ Grundschicht der DXGI-SwapChain-Flag**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) angeben, und verwenden Sie [**IDXGISwapChain2:: setmatrixtransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) und [**IDXGISwapChain2:: getmatrixtransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) , um die für das Spiel verwendete SwapChain

## <a name="select-backbuffer-subregion-for-swap-chain"></a>Swapkette-Unterregion für SwapChain auswählen

Ab Windows 8.1 kann DXGI 1,3 verwendet werden, um einen Unterbereich des backpuffers für die Verwendung mit der SwapChain auszuwählen, sodass es möglich ist, in einen kleineren Hintergrund Puffer zu gerenden, ohne die Swapkette neu zu erstellen. Weitere Informationen finden Sie unter [**IDXGISwapChain2:: setsourcesize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) und [**IDXGISwapChain2:: getsourcesize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize).

## <a name="lower-latency-swap-chain-presentation"></a>Darstellung der Swap-Kette mit niedrigerer Latenzzeit

Beginnend mit der Windows 8.1 ermöglicht DXGI 1,3 das Reduzieren der Latenzzeit, indem es der SwapChain ermöglicht, den vorherigen Frame vorzufinden, bevor die Verwendung des Geräts zum Zeichnen des nächsten Frames gestartet wird. Weitere Informationen finden Sie unter [**IDXGISwapChain2:: getframelatencywaitableobject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject), [**IDXGISwapChain2:: getmaximumframelatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)und [**IDXGISwapChain2:: setmaximumframelatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency).

## <a name="related-topics"></a>Zugehörige Themen

[Programmier Handbuch für DXGI](dx-graphics-dxgi-overviews.md)
