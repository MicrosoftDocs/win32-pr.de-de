---
title: Wiedergeben einer Befehlsliste
description: In diesem Thema wird gezeigt, wie eine Befehlsliste wiedergegeben wird.
ms.assetid: 4e6c0a98-85ff-45ca-963b-7d5c55f47195
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d04df73b481adea17e1f985e2c1851039fd016a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992799"
---
# <a name="how-to-play-back-a-command-list"></a><span data-ttu-id="12af5-103">Gewusst wie: Wiedergeben einer Befehlsliste</span><span class="sxs-lookup"><span data-stu-id="12af5-103">How to: Play Back a Command List</span></span>

<span data-ttu-id="12af5-104">Eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md) ist eine aufgezeichnete Liste von renderingbefehlen.</span><span class="sxs-lookup"><span data-stu-id="12af5-104">A [command list](overviews-direct3d-11-render-multi-thread-command-list.md) is a recorded list of rendering commands.</span></span> <span data-ttu-id="12af5-105">Verwenden Sie eine Befehlsliste, um Zeichnungs Befehle vorab aufzuzeichnen und Sie später wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="12af5-105">Use a command list to pre-record drawing commands and play them back later.</span></span> <span data-ttu-id="12af5-106">In diesem Thema wird gezeigt, wie eine [Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list.md)wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="12af5-106">This topic shows how to play back a [command list](overviews-direct3d-11-render-multi-thread-command-list.md).</span></span> <span data-ttu-id="12af5-107">Eine Befehlsliste kann verwendet werden, um renderingtasks zwischen Threads aufzuteilen.</span><span class="sxs-lookup"><span data-stu-id="12af5-107">A command list can be used to split rendering tasks between threads.</span></span>

<span data-ttu-id="12af5-108">In diesem Abschnitt wird beschrieben, wie eine Befehlsliste wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="12af5-108">This section describes how to play back a command list.</span></span> <span data-ttu-id="12af5-109">Informationen zum Aufzeichnen einer Befehlsliste finden [Sie unter Gewusst wie: Aufzeichnen einer Befehlsliste](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span><span class="sxs-lookup"><span data-stu-id="12af5-109">For recording a command list, see [How to: Record a Command List](overviews-direct3d-11-render-multi-thread-command-list-record.md).</span></span>

<span data-ttu-id="12af5-110">**Wiedergeben einer Befehlsliste**</span><span class="sxs-lookup"><span data-stu-id="12af5-110">**To play back a command list**</span></span>

-   <span data-ttu-id="12af5-111">Aufrufen von [**Verknüpfung id3d11devicecontext aus:: executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) und übergeben eines gültigen [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="12af5-111">Call [**ID3D11DeviceContext::ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) and pass a valid [**ID3D11CommandList**](/windows/desktop/api/D3D11/nn-d3d11-id3d11commandlist) object.</span></span>
    ```
    if(g_pd3dCommandList)
    {
        g_pImmediateContext->ExecuteCommandList(g_pd3dCommandList, TRUE);
    }
    ```

    

<span data-ttu-id="12af5-112">[**Executecommandlist**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) muss im [unmittelbaren Kontext](overviews-direct3d-11-devices-intro.md) ausgeführt werden, damit aufgezeichnete Befehle auf der Grafikverarbeitungseinheit (Graphics Processing Unit, GPU) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="12af5-112">[**ExecuteCommandList**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-executecommandlist) must be executed on the [immediate context](overviews-direct3d-11-devices-intro.md) for recorded commands to be run on the graphics processing unit (GPU).</span></span> <span data-ttu-id="12af5-113">Verwenden Sie den unmittelbaren Kontext zum Übertragen von Befehlen an die GPU zur Ausführung. verwenden Sie einen verzögerten Kontext zum Aufzeichnen von Befehlen für die Wiedergabe in einer anderen Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="12af5-113">Use the immediate context to feed commands to the GPU for execution, use a deferred context to record commands for playback onto another command list.</span></span> <span data-ttu-id="12af5-114">Wenn Sie **executecommandlist** in einem anderen verzögerten Kontext aufrufen, erstellen Sie eine verzögerte, verzögerte Befehlsliste.</span><span class="sxs-lookup"><span data-stu-id="12af5-114">When you call **ExecuteCommandList** onto another deferred context, you create a ‘merged’ deferred command list.</span></span> <span data-ttu-id="12af5-115">Wenn Sie die Befehle für die zusammengeführte verzögerte Befehlsliste ausführen möchten, müssen Sie diese im unmittelbaren Kontext ausführen.</span><span class="sxs-lookup"><span data-stu-id="12af5-115">To run the commands on the merged deferred command list, you need to execute them on the immediate context.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12af5-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="12af5-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12af5-117">Befehlsliste</span><span class="sxs-lookup"><span data-stu-id="12af5-117">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)
</dt> <dt>

[<span data-ttu-id="12af5-118">Verwendung von Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="12af5-118">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> </dl>

 

 




