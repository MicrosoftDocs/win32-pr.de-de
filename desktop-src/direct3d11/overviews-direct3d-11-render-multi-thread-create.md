---
title: Objekt Erstellung mit Multithreading
description: Verwenden Sie die ID3D11Device-Schnittstelle zum Erstellen von Ressourcen und Objekten, und verwenden Sie Verknüpfung id3d11devicecontext aus zum Rendern.
ms.assetid: e1765192-865c-4a62-9be7-6e95280ee8ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28cbfbe73efc96b301216deb5ccbf623354ddbb7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947739"
---
# <a name="object-creation-with-multithreading"></a><span data-ttu-id="e6e49-103">Objekt Erstellung mit Multithreading</span><span class="sxs-lookup"><span data-stu-id="e6e49-103">Object Creation with Multithreading</span></span>

<span data-ttu-id="e6e49-104">Verwenden Sie die [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) -Schnittstelle zum Erstellen von Ressourcen und Objekten, und verwenden Sie [**Verknüpfung id3d11devicecontext aus**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) zum [Rendern](overviews-direct3d-11-render-multi-thread-render.md).</span><span class="sxs-lookup"><span data-stu-id="e6e49-104">Use the [**ID3D11Device**](/windows/desktop/api/D3D11/nn-d3d11-id3d11device) interface to create resources and objects, use the [**ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) for [rendering](overviews-direct3d-11-render-multi-thread-render.md).</span></span>

<span data-ttu-id="e6e49-105">Im folgenden finden Sie einige Beispiele für das Erstellen von Ressourcen:</span><span class="sxs-lookup"><span data-stu-id="e6e49-105">Here are some examples of how to create resources:</span></span>

-   [<span data-ttu-id="e6e49-106">Vorgehensweise: Erstellen eines Scheitelpunkt Puffers</span><span class="sxs-lookup"><span data-stu-id="e6e49-106">How to: Create a Vertex Buffer</span></span>](overviews-direct3d-11-resources-buffers-vertex-how-to.md)
-   [<span data-ttu-id="e6e49-107">Vorgehensweise: Erstellen eines Index Puffers</span><span class="sxs-lookup"><span data-stu-id="e6e49-107">How to: Create an Index Buffer</span></span>](overviews-direct3d-11-resources-buffers-index-how-to.md)
-   [<span data-ttu-id="e6e49-108">Vorgehensweise: Erstellen eines konstanten Puffers</span><span class="sxs-lookup"><span data-stu-id="e6e49-108">How to: Create a Constant Buffer</span></span>](overviews-direct3d-11-resources-buffers-constant-how-to.md)
-   [<span data-ttu-id="e6e49-109">Gewusst wie: Initialisieren einer Textur aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="e6e49-109">How to: Initialize a Texture From a File</span></span>](overviews-direct3d-11-resources-textures-how-to.md)

## <a name="multithreading-considerations"></a><span data-ttu-id="e6e49-110">Überlegungen zum Multithreading</span><span class="sxs-lookup"><span data-stu-id="e6e49-110">Multithreading Considerations</span></span>

<span data-ttu-id="e6e49-111">Der Umfang der Parallelität beim Erstellen und Rendern von Ressourcen, die Ihre Anwendung erreichen kann, hängt von der durch den Treiber implementierten Multithreadunterstützung ab.</span><span class="sxs-lookup"><span data-stu-id="e6e49-111">The amount of concurrency of resource creation and rendering that your application can achieve depends on the level of multithreading support that the driver implements.</span></span> <span data-ttu-id="e6e49-112">Wenn der Treiber gleichzeitige Erstellung unterstützt, sollte die Anwendung weitaus weniger Parallelitäts Probleme aufweisen.</span><span class="sxs-lookup"><span data-stu-id="e6e49-112">If the driver supports concurrent creates, then the application should have much less concurrency concerns.</span></span> <span data-ttu-id="e6e49-113">Wenn der Treiber die gleichzeitige Objekt Erstellung jedoch nicht unterstützt, ist der Umfang der Parallelität äußerst eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="e6e49-113">However, if the driver does not support concurrent object creation, the amount of concurrency is extremely limited.</span></span> <span data-ttu-id="e6e49-114">Um zu verstehen, wie viele Unterstützung in einem Treiber verfügbar ist, Fragen Sie den Treiber nach dem Wert des **driverconcurrenterstellungsmembers** der [**D3D11 \_ Feature \_ Data \_ Threading**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) -Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="e6e49-114">To understand the amount of support available in a driver, query the driver for the value of the **DriverConcurrentCreates** member of the [**D3D11\_FEATURE\_DATA\_THREADING**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_threading) structure.</span></span> <span data-ttu-id="e6e49-115">Weitere Informationen zum Überprüfen der Treiberunterstützung für Multithreading finden Sie unter Gewusst [wie: Überprüfen der Treiberunterstützung](overviews-direct3d-11-render-multi-thread-support.md).</span><span class="sxs-lookup"><span data-stu-id="e6e49-115">For more information about checking for driver support of multithreading, see [How To: Check for Driver Support](overviews-direct3d-11-render-multi-thread-support.md).</span></span>

<span data-ttu-id="e6e49-116">Gleichzeitige Vorgänge führen nicht zwangsläufig zu einer besseren Leistung.</span><span class="sxs-lookup"><span data-stu-id="e6e49-116">Concurrent operations do not necessarily lead to better performance.</span></span> <span data-ttu-id="e6e49-117">Beispielsweise wird das Erstellen und Laden einer Textur in der Regel durch die Speicherbandbreite begrenzt.</span><span class="sxs-lookup"><span data-stu-id="e6e49-117">For example, creating and loading a texture is typically limited by memory bandwidth.</span></span> <span data-ttu-id="e6e49-118">Der Versuch, mehrere Texturen zu erstellen und zu laden, ist möglicherweise nicht schneller als eine Textur gleichzeitig, auch wenn dadurch mehrere CPU-Kerne im Leerlauf bleiben.</span><span class="sxs-lookup"><span data-stu-id="e6e49-118">Attempting to create and load multiple textures might be no faster than doing one texture at a time, even if this leaves multiple CPU cores idle.</span></span> <span data-ttu-id="e6e49-119">Wenn Sie jedoch mehrere Shader mithilfe mehrerer Threads erstellen, kann dies die Leistung erhöhen, da dieser Vorgang weniger von Systemressourcen wie z. b. der Speicherbandbreite abhängt.</span><span class="sxs-lookup"><span data-stu-id="e6e49-119">However, creating multiple shaders using multiple threads can increase performance as this operation is less dependent on system resources such as memory bandwidth.</span></span>

<span data-ttu-id="e6e49-120">Wenn die Treiber-und Grafikhardware Multithreading unterstützt, können Sie die neu erstellten Ressourcen in der Regel effizienter initialisieren, indem Sie einen Zeiger auf die Anfangsdaten im *pinitialdata* -Parameter übergeben (z. b. in einem Aufrufen der [**ID3D11Device:: CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) -Methode).</span><span class="sxs-lookup"><span data-stu-id="e6e49-120">When the driver and graphics hardware support multithreading, you can typically initialize newly created resources more efficiently by passing a pointer to initial data in the *pInitialData* parameter (for example, in a call to the [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) method).</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6e49-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e6e49-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6e49-122">MultiThreading</span><span class="sxs-lookup"><span data-stu-id="e6e49-122">MultiThreading</span></span>](overviews-direct3d-11-render-multi-thread.md)
</dt> </dl>

 

 




