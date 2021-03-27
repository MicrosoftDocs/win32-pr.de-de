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
# <a name="how-to-create-a-swap-chain"></a><span data-ttu-id="1e8ac-103">Gewusst wie: Erstellen einer SwapChain</span><span class="sxs-lookup"><span data-stu-id="1e8ac-103">How To: Create a Swap Chain</span></span>

<span data-ttu-id="1e8ac-104">In diesem Thema wird gezeigt, wie eine SwapChain erstellt wird, die zwei oder mehr Puffer kapselt, die zum Rendern und Anzeigen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-104">This topic show how to create a swap chain that encapsulates two or more buffers that are used for rendering and display.</span></span> <span data-ttu-id="1e8ac-105">Sie enthalten normalerweise einen Front-Puffer, der dem Anzeigegerät angezeigt wird, und einen Hintergrund Puffer, der als Renderziel fungiert.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-105">They usually contain a front buffer that is presented to the display device and a back buffer that serves as the render target.</span></span> <span data-ttu-id="1e8ac-106">Nachdem der unmittelbare Kontext zum Rendern des hinterpuffers gerendert wurde, zeigt die Swapkette den Hintergrund Puffer durch Austauschen der beiden Puffer an.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-106">After the immediate context is done rendering to the back buffer, the swap chain presents the back buffer by swapping the two buffers.</span></span>

<span data-ttu-id="1e8ac-107">Die SwapChain definiert mehrere Renderingeigenschaften, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="1e8ac-107">The swap chain defines several rendering characteristics including:</span></span>

-   <span data-ttu-id="1e8ac-108">Die Größe des Rendering-Bereichs.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-108">The size of the render area.</span></span>
-   <span data-ttu-id="1e8ac-109">Die Aktualisierungsrate der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-109">The display refresh rate.</span></span>
-   <span data-ttu-id="1e8ac-110">Der Anzeigemodus.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-110">The display mode.</span></span>
-   <span data-ttu-id="1e8ac-111">Das Oberflächen Format.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-111">The surface format.</span></span>

<span data-ttu-id="1e8ac-112">Definieren Sie die Merkmale der Austausch Kette, indem Sie eine [**DXGI \_ - \_ SwapChain \_**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) -Struktur auffüllen und eine [**idxgiswapchain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) -Schnittstelle initialisieren.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-112">Define the characteristics of the swap chain by filling in a [**DXGI\_SWAP\_CHAIN\_DESC**](/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc) structure and initializing an [**IDXGISwapChain**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain) interface.</span></span> <span data-ttu-id="1e8ac-113">Initialisieren Sie eine Swapkette, indem Sie [**idxgifactory:: createswapchain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) oder [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain)aufrufen.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-113">Initialize a swap chain by calling [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) or [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain).</span></span>

## <a name="create-a-device-and-a-swap-chain"></a><span data-ttu-id="1e8ac-114">Erstellen Sie ein Gerät und eine SwapChain.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-114">Create a device and a swap chain</span></span>

<span data-ttu-id="1e8ac-115">Um ein Gerät und eine SwapChain zu initialisieren, verwenden Sie eine der beiden folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="1e8ac-115">To initialize a device and swap chain, use one of the following two functions:</span></span>

-   <span data-ttu-id="1e8ac-116">Verwenden Sie die [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) -Funktion, wenn Sie die SwapChain zur gleichen Zeit wie die Geräte Initialisierung initialisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-116">Use the [**D3D11CreateDeviceAndSwapChain**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdeviceandswapchain) function when you want to initialize the swap chain at the same time as device initialization.</span></span> <span data-ttu-id="1e8ac-117">Dies ist normalerweise die einfachste Option.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-117">This usually is the easiest option.</span></span>

-   <span data-ttu-id="1e8ac-118">Verwenden Sie die [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) -Funktion, wenn Sie bereits eine [**SwapChain mit idxgifactory:: kreateswapchain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain)erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="1e8ac-118">Use the [**D3D11CreateDevice**](/windows/desktop/api/D3D11/nf-d3d11-d3d11createdevice) function when you have already created a swap chain using [**IDXGIFactory::CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e8ac-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1e8ac-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e8ac-120">Geräte</span><span class="sxs-lookup"><span data-stu-id="1e8ac-120">Devices</span></span>](overviews-direct3d-11-devices.md)
</dt> <dt>

[<span data-ttu-id="1e8ac-121">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1e8ac-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 