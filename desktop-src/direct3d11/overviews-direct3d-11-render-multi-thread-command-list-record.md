---
title: Aufzeichnen einer Befehlsliste
description: In diesem Thema wird gezeigt, wie eine Befehlsliste erstellt und aufgezeichnet wird.
ms.assetid: f5b90dfb-0b07-432e-813b-1541efbe3de5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712f48386e0625c58a1f11c122d105064477ca8c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711544"
---
# <a name="how-to-record-a-command-list"></a><span data-ttu-id="1360b-103">Gewusst wie: Aufzeichnen einer Befehlsliste</span><span class="sxs-lookup"><span data-stu-id="1360b-103">How to: Record a Command List</span></span>

<span data-ttu-id="1360b-104">Eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md) ist eine aufgezeichnete Liste von renderingbefehlen.</span><span class="sxs-lookup"><span data-stu-id="1360b-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="1360b-105">In diesem Thema wird gezeigt, wie eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)erstellt und aufgezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1360b-105">This topic shows how to create and record a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="1360b-106">Verwenden Sie eine Befehlsliste, um Rendering-Befehle aufzuzeichnen und Sie später wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="1360b-106">Use a command list to record render commands and play them back later.</span></span> <span data-ttu-id="1360b-107">Eine Befehlsliste ist praktisch für das Aufteilen von renderingtasks zwischen Threads.</span><span class="sxs-lookup"><span data-stu-id="1360b-107">A command list is convenient for splitting rendering tasks between threads.</span></span>

<span data-ttu-id="1360b-108">**So zeichnen Sie eine Befehlsliste auf**</span><span class="sxs-lookup"><span data-stu-id="1360b-108">**To record a command list**</span></span>

1.  <span data-ttu-id="1360b-109">Eine Befehlsliste muss aus einem verzögerten Kontext erstellt werden, der Geräte Zustands-und renderingaktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="1360b-109">A command list must be created from a deferred context, which contains device state and rendering actions.</span></span> <span data-ttu-id="1360b-110">Wenn Sie ein Gerät haben, erstellen Sie einen verzögerten Kontext durch Aufrufen von [**ID3D11Device:: createdeferredcontext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span><span class="sxs-lookup"><span data-stu-id="1360b-110">Given a device, create a deferred context by calling [**ID3D11Device::CreateDeferredContext**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdeferredcontext).</span></span>

    ```
    HRESULT hr;
    ID3D11DeviceContext* pDeferredContext = NULL;

    hr = g_pd3dDevice->CreateDeferredContext(0, &pDeferredContext);
    ```

    

2.  <span data-ttu-id="1360b-111">Verwenden Sie den verzögerten Kontext zum Rendering.</span><span class="sxs-lookup"><span data-stu-id="1360b-111">Use the deferred context to render.</span></span>

    ```
    float ClearColor[4] = { 0.0f, 0.125f, 0.3f, 1.0f };
    pDeferredContext->ClearRenderTargetView( g_pRenderTargetView, ClearColor );
        
    // Add additional rendering commands
    ...
    ```

    

    <span data-ttu-id="1360b-112">In diesem einfachen Beispiel wird ein Renderziel gelöscht, aber Sie können zusätzliche renderbefehle hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1360b-112">This simple example clears a render target, but you could add additional render commands.</span></span>

3.  <span data-ttu-id="1360b-113">Erstellen Sie eine Befehlsliste, und zeichnen Sie Sie auf, indem Sie [**Verknüpfung id3d11devicecontext aus:: finishcommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) aufrufen und einen Zeiger auf eine nicht initialisierte [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) -Schnittstelle übergeben.</span><span class="sxs-lookup"><span data-stu-id="1360b-113">Create/record a command list by calling [**ID3D11DeviceContext::FinishCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-finishcommandlist) and passing a pointer to an uninitialized [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) interface.</span></span>

    ```
    ID3D11CommandList* pd3dCommandList = NULL;
    HRESULT hr;
    hr = pDeferredContext->FinishCommandList(FALSE, &pd3dCommandList);
    ```

    

    <span data-ttu-id="1360b-114">Wenn die-Methode zurückgibt, wird eine Befehlsliste erstellt, die alle Rendering-Befehle enthält, und eine Schnittstelle wird an die Anwendung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1360b-114">When the method returns, a command list is created containing all the render commands and an interface is returned to the application.</span></span>

    <span data-ttu-id="1360b-115">Der boolesche Parameter teilt der Laufzeit mit, was mit dem Pipeline Zustand im verzögerten Kontext zu tun ist.</span><span class="sxs-lookup"><span data-stu-id="1360b-115">The boolean parameter tells the runtime what to do with the pipeline state in the deferred context.</span></span> <span data-ttu-id="1360b-116">" **True** " bedeutet, dass der Zustand des Geräte Kontexts in der vorbefehls Listen Bedingung wieder hergestellt wird, wenn die Aufzeichnung abgeschlossen ist. " **false** " bedeutet, dass der Status nach der Aufzeichnung nicht geändert</span><span class="sxs-lookup"><span data-stu-id="1360b-116">**TRUE** means restore the state of the device context to its pre-command list condition when recording is completed, **FALSE** means do not change the state after recording.</span></span> <span data-ttu-id="1360b-117">Dies bedeutet, dass der Gerätekontext die in der Befehlsliste enthaltenen Zustandsänderungen widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="1360b-117">This means that the device context will reflect the state changes contained in the command list.</span></span>

<span data-ttu-id="1360b-118">Ein Beispiel für die Wiedergabe einer Befehlsliste finden Sie unter Gewusst [wie: Wiedergeben einer Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span><span class="sxs-lookup"><span data-stu-id="1360b-118">To see an example for playing back a command list, see [How to: Play Back a Command List](overviews-direct3d-11-render-multi-thread-command-list-play.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1360b-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="1360b-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1360b-120">Befehlsliste</span><span class="sxs-lookup"><span data-stu-id="1360b-120">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="1360b-121">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="1360b-121">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




