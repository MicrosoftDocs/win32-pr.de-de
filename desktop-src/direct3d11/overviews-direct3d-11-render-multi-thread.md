---
title: MultiThreading
description: Direct3D 11 implementiert die Unterstützung für das Erstellen und Rendering von Objekten mithilfe mehrerer Threads.
ms.assetid: 1bf50927-268b-4471-b059-819adf2189a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4de7ca3e7e00ffba0c728aef334f21efc18899
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104207078"
---
# <a name="multithreading"></a><span data-ttu-id="ddc66-103">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="ddc66-103">MultiThreading</span></span>

<span data-ttu-id="ddc66-104">Direct3D 11 implementiert die Unterstützung für das Erstellen und Rendering von Objekten mithilfe mehrerer Threads.</span><span class="sxs-lookup"><span data-stu-id="ddc66-104">Direct3D 11 implements support for object creation and rendering using multiple threads.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ddc66-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ddc66-105">In this section</span></span>



| <span data-ttu-id="ddc66-106">Thema</span><span class="sxs-lookup"><span data-stu-id="ddc66-106">Topic</span></span>                                                                                                                   | <span data-ttu-id="ddc66-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ddc66-107">Description</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ddc66-108">Einführung in das Multithreading in Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="ddc66-108">Introduction to Multithreading in Direct3D 11</span></span>](overviews-direct3d-11-render-multi-thread-intro.md)<br/>         | <span data-ttu-id="ddc66-109">Multithreading ist darauf ausgelegt, die Leistung zu verbessern, indem Sie die Arbeit mit einem oder mehreren Threads gleichzeitig ausführen.</span><span class="sxs-lookup"><span data-stu-id="ddc66-109">Multithreading is designed to improve performance by performing work using one or more threads at the same time.</span></span> <br/>                                                                                                         |
| [<span data-ttu-id="ddc66-110">Objekt Erstellung mit Multithreading</span><span class="sxs-lookup"><span data-stu-id="ddc66-110">Object Creation with Multithreading</span></span>](overviews-direct3d-11-render-multi-thread-create.md)<br/>                  | <span data-ttu-id="ddc66-111">Verwenden Sie die [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstelle zum Erstellen von Ressourcen und Objekten, und verwenden Sie [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) zum [Rendern](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="ddc66-111">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span><br/> |
| [<span data-ttu-id="ddc66-112">Sofortiges und verzögertes Rendering</span><span class="sxs-lookup"><span data-stu-id="ddc66-112">Immediate and Deferred Rendering</span></span>](overviews-direct3d-11-render-multi-thread-render.md)<br/>                     | <span data-ttu-id="ddc66-113">Direct3D 11 unterstützt zwei renderingtypen: direkt und verzögert.</span><span class="sxs-lookup"><span data-stu-id="ddc66-113">Direct3D 11 supports two types of rendering: immediate and deferred.</span></span> <span data-ttu-id="ddc66-114">Beide werden mithilfe der [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) -Schnittstelle implementiert.</span><span class="sxs-lookup"><span data-stu-id="ddc66-114">Both are implemented by using the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) interface.</span></span><br/>                                                      |
| [<span data-ttu-id="ddc66-115">Befehlsliste</span><span class="sxs-lookup"><span data-stu-id="ddc66-115">Command List</span></span>](overviews-direct3d-11-render-multi-thread-command-list.md)<br/>                                   | <span data-ttu-id="ddc66-116">Eine Befehlsliste ist eine Sequenz von GPU-Befehlen, die aufgezeichnet und wiedergegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="ddc66-116">A command list is a sequence of GPU commands that can be recorded and played back.</span></span> <span data-ttu-id="ddc66-117">Eine Befehlsliste kann die Leistung verbessern, indem der von der Laufzeit generierte Verwaltungsaufwand verringert wird.</span><span class="sxs-lookup"><span data-stu-id="ddc66-117">A command list may improve performance by reducing the amount of overhead generated by the runtime.</span></span><br/>                                    |
| [<span data-ttu-id="ddc66-118">Threading Unterschiede zwischen Direct3D-Versionen</span><span class="sxs-lookup"><span data-stu-id="ddc66-118">Threading Differences between Direct3D Versions</span></span>](overviews-direct3d-11-render-multi-thread-differences.md)<br/> | <span data-ttu-id="ddc66-119">Viele multithreadprogrammierungs-Modelle verwenden Synchronisierungs primitive (z. b. Mutexen), um kritische Abschnitte zu erstellen und zu verhindern, dass der Zugriff auf Code von mehreren Threads gleichzeitig erfolgt.</span><span class="sxs-lookup"><span data-stu-id="ddc66-119">Many multi-threaded programming models make use of synchronization primitives (such as mutexes) to create critical sections and prevent code from being accessed by more than one thread at a time.</span></span><br/>                       |



 

## <a name="related-topics"></a><span data-ttu-id="ddc66-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ddc66-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ddc66-121">Vorgehensweise: Überprüfen der Treiberunterstützung</span><span class="sxs-lookup"><span data-stu-id="ddc66-121">How To: Check for Driver Support</span></span>](overviews-direct3d-11-render-multi-thread-support.md)
</dt> <dt>

[<span data-ttu-id="ddc66-122">Darstellung</span><span class="sxs-lookup"><span data-stu-id="ddc66-122">Rendering</span></span>](overviews-direct3d-11-render.md)
</dt> </dl>

 

 





