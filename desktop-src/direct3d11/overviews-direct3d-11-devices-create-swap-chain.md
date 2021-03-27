---
title: Erstellen einer austauschkette
description: In diesem Thema wird gezeigt, wie eine SwapChain erstellt wird, die zwei oder mehr Puffer kapselt, die zum Rendern und Anzeigen verwendet werden.
ms.assetid: 0e290b37-0807-42c7-9e50-fd2db6affb14
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8355eafff6e233b89be82fd9e58ca53224248e84
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390650"
---
# <a name="how-to-create-a-swap-chain"></a>Gewusst wie: Erstellen einer SwapChain

In diesem Thema wird gezeigt, wie eine SwapChain erstellt wird, die zwei oder mehr Puffer kapselt, die zum Rendern und Anzeigen verwendet werden. Sie enthalten normalerweise einen Front-Puffer, der dem Anzeigegerät angezeigt wird, und einen Hintergrund Puffer, der als Renderziel fungiert. Nachdem der unmittelbare Kontext zum Rendern des hinterpuffers gerendert wurde, zeigt die Swapkette den Hintergrund Puffer durch Austauschen der beiden Puffer an.

Die SwapChain definiert mehrere Renderingeigenschaften, einschließlich:

-   Die Größe des Rendering-Bereichs.
-   Die Aktualisierungsrate der Anzeige.
-   Der Anzeigemodus.
-   Das Oberflächen Format.

Definieren Sie die Merkmale der Austausch Kette, indem Sie eine [**DXGI \_ - \_ SwapChain \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) -Struktur auffüllen und eine [**idxgiswapchain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) -Schnittstelle initialisieren. Initialisieren Sie eine Swapkette, indem Sie [**idxgifactory:: createswapchain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)aufrufen.

## <a name="create-a-device-and-a-swap-chain"></a>Erstellen Sie ein Gerät und eine SwapChain.

Um ein Gerät und eine SwapChain zu initialisieren, verwenden Sie eine der beiden folgenden Funktionen:

-   Verwenden Sie die [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) -Funktion, wenn Sie die SwapChain zur gleichen Zeit wie die Geräte Initialisierung initialisieren möchten. Dies ist normalerweise die einfachste Option.

-   Verwenden Sie die [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion, wenn Sie bereits eine [**SwapChain mit idxgifactory:: kreateswapchain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)erstellt haben.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Geräte](overviews-direct3d-11-devices.md)
</dt> <dt>

[Verwendung von Direct3D 11](how-to-use-direct3d-11.md)
</dt> </dl>

 

 