---
description: Die folgende Funktionalität wurde in Microsoft DirectX Graphic Infrastructure (DXGI) 1.3 hinzugefügt, das ab Windows 8.1.
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: DXGI 1.3 Improvements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 709dc9e98ffe6ecd67f6bd91aa654b1e0bfe0375dabcd2a344f5b012c57dca2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984120"
---
# <a name="dxgi-13-improvements"></a>DXGI 1.3 Improvements

Die folgende Funktionalität wurde in Microsoft DirectX Graphic Infrastructure (DXGI) 1.3 hinzugefügt, das ab Windows 8.1.

## <a name="trim-dxgi-adapter-memory-usage"></a>Kürzen der Speicherauslastung des DXGI-Adapters

Ab version Windows 8.1 DXGI 1.3 die Funktion zum Leeren und Los freigaben nicht verwendeter Arbeitsspeicherressourcen, die vom DXGI-Adapter zugeordnet werden. Auf diese Weise können Apps temporären Speicher während des Aussetzens frei geben, was die Wahrscheinlichkeit verringert, dass die App beendet wird, um Ressourcen für andere Apps frei zu geben. Wenn die App fortgesetzt wird, erstellen Gerätetreiber, die Trim unterstützen, Ressourcen bei Bedarf neu. Ab Windows 8.1 müssen alle Direct3D-Geräte, die von einer App erstellt werden, [**IDXGIDevice3::Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) aufrufen, wenn sie angehalten werden, um den Speicherbedarf zu reduzieren und die Wahrscheinlichkeit zu verringern, dass die App beendet wird, um Systemressourcen wieder verfügbar zu machen.

## <a name="multi-plane-overlays"></a>Überlagerungen mit mehreren Ebenen

Ab Windows 8.1 unterstützt DXGI 1.3 Überlagerungen mit mehreren Ebenen. Sie können mithilfe von [**IDXGIOutput2::SupportsOverlays**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays)herausfinden, ob das Gerät Überlagerungen mit mehreren Ebenen in der Hardware unterstützt.

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>Überlappende Swapketten und Skalierung der Swapkette

Ab diesem Windows 8.1 DXGI 1.3 überlappende Swapketten. Überlappende Austauschketten werden verwendet, um 3D-Grafiken mit nicht nativen Auflösungen (mit Hardware-Upscaling) zu zeichnen, während die Benutzeroberfläche mit nativer Auflösung dargestellt wird. Auf diese Weise können Spiele höhere Füllraten für reaktionsschnelles Spiel nutzen, ohne die visuelle Qualität von Benutzeroberflächenelementen wie Spielerwertung und Dialogtext zu herabsetzen. Auf Geräten, die Überlagerungen mit mehreren Ebenen unterstützen, verwendet Direct3D Überlagerungen mit mehreren Ebenen für überlappende Austauschketten. Erstellen Sie eine Vordergrund-Swapkette, indem Sie beim Erstellen der Swapkette das [**DXGI \_ SWAP CHAIN FLAG FOREGROUND \_ \_ \_ \_ LAYER-Flag**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) angeben, und verwenden Sie [**IDXGISwapChain2::SetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) und [**IDXGISwapChain2::GetMatrixTransform,**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) um die für das Spiel verwendete Swapkette zu skalieren.

## <a name="select-backbuffer-subregion-for-swap-chain"></a>Auswählen des Unterbereichs "Backbuffer" für die Swapkette

Ab Windows 8.1 kann DXGI 1.3 verwendet werden, um einen Unterbereich des Backbuffers für die Verwendung mit der Swapkette auszuwählen, wodurch es möglich ist, in einen kleineren Hintergrundpuffer zu rendern, ohne die Swapkette neu zu schaffen. Siehe [**IDXGISwapChain2::SetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) und [**IDXGISwapChain2::GetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize).

## <a name="lower-latency-swap-chain-presentation"></a>Darstellung der Swapkette mit geringerer Latenz

Ab Windows 8.1 ermöglicht DXGI 1.3 die Reduzierung der Latenz, indem die Austauschkette die Präsentation des vorherigen Rahmens beendet, bevor das Gerät zum Zeichnen des nächsten Rahmens verwendet wird. Siehe [**IDXGISwapChain2::GetFrameLatencyWaitableObject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject), [**IDXGISwapChain2::GetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)und [**IDXGISwapChain2::SetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency).

## <a name="related-topics"></a>Zugehörige Themen

[Programmierhandbuch für DXGI](dx-graphics-dxgi-overviews.md)
