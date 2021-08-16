---
title: Erstellen einer Austauschkette
description: In diesem Thema wird gezeigt, wie Sie eine Austauschkette erstellen, die zwei oder mehr Puffer kapselt, die zum Rendern und Anzeigen verwendet werden.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ef97b261d9831c451c8a81bfc1f4d9d13b1cd423ac28f38de4b90c1d4ae100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118530572"
---
# <a name="how-to-create-a-swap-chain"></a>How To: Create a Swap Chain

In diesem Thema wird gezeigt, wie Sie eine Austauschkette erstellen, die zwei oder mehr Puffer kapselt, die zum Rendern und Anzeigen verwendet werden. Sie enthalten in der Regel einen Frontpuffer, der dem Anzeigegerät angezeigt wird, und einen Hintergrundpuffer, der als Renderziel dient. Nachdem der unmittelbare Kontext in den Hintergrundpuffer gerendert wurde, stellt die Swapkette den Hintergrundpuffer durch Austauschen der beiden Puffer vor.

Die Austauschkette definiert mehrere Renderingmerkmale, einschließlich:

-   Die Größe des Renderbereichs.
-   Die Anzeigeaktualisierungsrate.
-   Der Anzeigemodus.
-   Das Oberflächenformat.

Definieren Sie die Merkmale der Swapkette, indem Sie eine [**DXGI \_ SWAP CHAIN \_ \_ DESC-Struktur**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) ausfüllen und eine [**IDXGISwapChain-Schnittstelle**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) initialisieren. Initialisieren Sie eine Austauschkette, indem Sie [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) oder [**D3D11CreateDeviceAndSwapChain aufrufen.**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)

## <a name="create-a-device-and-a-swap-chain"></a>Erstellen eines Geräts und einer Austauschkette

Verwenden Sie eine der beiden folgenden Funktionen, um ein Gerät und eine Austauschkette zu initialisieren:

-   Verwenden Sie [**die Funktion D3D11CreateDeviceAndSwapChain,**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) wenn Sie die Auslagerungskette gleichzeitig mit der Geräteinitialisierung initialisieren möchten. Dies ist in der Regel die einfachste Option.

-   Verwenden Sie [**die D3D11CreateDevice-Funktion,**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) wenn Sie bereits eine Swapkette mithilfe von [**IDXGIFactory::CreateSwapChain erstellt haben.**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> <dt>

[Verwenden von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 