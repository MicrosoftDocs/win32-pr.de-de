---
description: Diagramm-Manager Filtern
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Diagramm-Manager Filtern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860003"
---
# <a name="filter-graph-manager"></a><span data-ttu-id="9e5ac-103">Diagramm-Manager Filtern</span><span class="sxs-lookup"><span data-stu-id="9e5ac-103">Filter Graph Manager</span></span>

<span data-ttu-id="9e5ac-104">Der Filter Graph-Manager erstellt und steuert Filter Diagramme.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-104">The Filter Graph Manager builds and controls filter graphs.</span></span> <span data-ttu-id="9e5ac-105">Dieses Objekt ist die zentrale Komponente in DirectShow.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-105">This object is the central component in DirectShow.</span></span> <span data-ttu-id="9e5ac-106">Anwendungen verwenden Sie, um Filter Diagramme zu erstellen und zu steuern.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-106">Applications use it to build and control filter graphs.</span></span> <span data-ttu-id="9e5ac-107">Der Filter Graph-Manager behandelt auch die Synchronisierung, Ereignis Benachrichtigung und andere Aspekte der Steuerung des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-107">The Filter Graph Manager also handles synchronization, event notification, and other aspects of the controlling the filter graph.</span></span> <span data-ttu-id="9e5ac-108">Erstellen Sie dieses Objekt durch Aufrufen von **CoCreateInstance**.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-108">Create this object by calling **CoCreateInstance**.</span></span>

### <a name="clsid"></a><span data-ttu-id="9e5ac-109">CLSID</span><span class="sxs-lookup"><span data-stu-id="9e5ac-109">CLSID</span></span>

<span data-ttu-id="9e5ac-110">Es gibt zwei CLSIDs zum Erstellen des Filter Graph-Managers:</span><span class="sxs-lookup"><span data-stu-id="9e5ac-110">There are two CLSIDs for creating the Filter Graph Manager:</span></span>



| <span data-ttu-id="9e5ac-111">CLSID</span><span class="sxs-lookup"><span data-stu-id="9e5ac-111">CLSID</span></span>                      | <span data-ttu-id="9e5ac-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9e5ac-112">Description</span></span>                                                 |
|----------------------------|-------------------------------------------------------------|
| <span data-ttu-id="9e5ac-113">CLSID- \_ Filtergraph</span><span class="sxs-lookup"><span data-stu-id="9e5ac-113">CLSID\_FilterGraph</span></span>         | <span data-ttu-id="9e5ac-114">Erstellt den Filter Graph-Manager in einem freigegebenen Arbeits Thread.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-114">Creates the Filter Graph Manager on a shared worker thread.</span></span> |
| <span data-ttu-id="9e5ac-115">CLSID- \_ filtergraphnothread</span><span class="sxs-lookup"><span data-stu-id="9e5ac-115">CLSID\_FilterGraphNoThread</span></span> | <span data-ttu-id="9e5ac-116">Erstellt den Filter Graph-Manager im Anwendungs Thread.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-116">Creates the Filter Graph Manager on the application thread.</span></span> |



 

<span data-ttu-id="9e5ac-117">Im Allgemeinen sollten Anwendungen CLSID \_ Filtergraph verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-117">Generally, applications should use CLSID\_FilterGraph.</span></span> <span data-ttu-id="9e5ac-118">Beide CLSIDs erstellen dasselbe Objekt, verwenden jedoch verschiedene Threading Modelle:</span><span class="sxs-lookup"><span data-stu-id="9e5ac-118">Both CLSIDs create the same object, but they use different threading models:</span></span>

-   <span data-ttu-id="9e5ac-119">CLSID \_ Filtergraph erstellt den Filter Graph-Manager in einem Arbeits Thread, der von allen CLSID- \_ Filtergraph-Instanzen innerhalb desselben Prozesses gemeinsam genutzt wird.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-119">CLSID\_FilterGraph creates the Filter Graph Manager on a worker thread, which is shared by all CLSID\_FilterGraph instances within the same process.</span></span> <span data-ttu-id="9e5ac-120">Der Thread sendet Nachrichten, die von Filtern gesendet werden, und steuert die Lebensdauer von Fenstern, die durch Filter erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-120">The thread dispatches messages sent by filters, and controls the lifetime of any windows created by filters.</span></span>
-   <span data-ttu-id="9e5ac-121">CLSID \_ filtergraphnothread erstellt den Filter Graph-Manager im Anwendungs Thread.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-121">CLSID\_FilterGraphNoThread creates the Filter Graph Manager on the application's thread.</span></span> <span data-ttu-id="9e5ac-122">Wenn Sie diese CLSID verwenden, muss der Thread, der **cokreateinstance** aufruft, eine Nachrichten Schleife aufweisen, die Nachrichten sendet. Andernfalls können Deadlocks auftreten.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-122">If you use this CLSID, the thread that calls **CoCreateInstance** must have a message loop that dispatches messages; otherwise, deadlocks can occur.</span></span> <span data-ttu-id="9e5ac-123">Bevor der Anwendungs Thread beendet wird, muss er außerdem den Filter Graph-Manager und alle Graph-Objekte (z. b. Filter, Pins, Referenzuhren usw.) freigeben.</span><span class="sxs-lookup"><span data-stu-id="9e5ac-123">Also, before the application thread exits, it must release the Filter Graph Manager and all graph objects (such as filters, pins, reference clocks, and so forth).</span></span>

### <a name="interfaces"></a><span data-ttu-id="9e5ac-124">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="9e5ac-124">Interfaces</span></span>

<span data-ttu-id="9e5ac-125">Der Filter Graph-Manager macht die folgenden Schnittstellen verfügbar:</span><span class="sxs-lookup"><span data-stu-id="9e5ac-125">The Filter Graph Manager exposes the following interfaces:</span></span>

-   [<span data-ttu-id="9e5ac-126">**Iamgraphstreams**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-126">**IAMGraphStreams**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [<span data-ttu-id="9e5ac-127">**Iamstats**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-127">**IAMStats**</span></span>](/windows/desktop/api/Control/nn-control-iamstats)
-   [<span data-ttu-id="9e5ac-128">**Ibasicaudiodatei**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-128">**IBasicAudio**</span></span>](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [<span data-ttu-id="9e5ac-129">**Ibasicvideo**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-129">**IBasicVideo**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [<span data-ttu-id="9e5ac-130">**IBasicVideo2**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-130">**IBasicVideo2**</span></span>](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [<span data-ttu-id="9e5ac-131">**Ifilterchain**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-131">**IFilterChain**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [<span data-ttu-id="9e5ac-132">**Ifiltergraph**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-132">**IFilterGraph**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [<span data-ttu-id="9e5ac-133">**IFilterGraph2**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-133">**IFilterGraph2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [<span data-ttu-id="9e5ac-134">**IFilterGraph3**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-134">**IFilterGraph3**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [<span data-ttu-id="9e5ac-135">**IFilterMapper2**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-135">**IFilterMapper2**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [<span data-ttu-id="9e5ac-136">**Igraphbuilder**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-136">**IGraphBuilder**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [<span data-ttu-id="9e5ac-137">**Igraphconfig**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-137">**IGraphConfig**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [<span data-ttu-id="9e5ac-138">**Igraphversion**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-138">**IGraphVersion**</span></span>](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [<span data-ttu-id="9e5ac-139">**IMediaControl**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-139">**IMediaControl**</span></span>](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [<span data-ttu-id="9e5ac-140">**Imediaevent**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-140">**IMediaEvent**</span></span>](/windows/desktop/api/Control/nn-control-imediaevent)
-   [<span data-ttu-id="9e5ac-141">**Imediaeventex**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-141">**IMediaEventEx**</span></span>](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [<span data-ttu-id="9e5ac-142">**Imediaeventsink**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-142">**IMediaEventSink**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [<span data-ttu-id="9e5ac-143">**Imediafilter**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-143">**IMediaFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [<span data-ttu-id="9e5ac-144">**Imediaposition**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-144">**IMediaPosition**</span></span>](/windows/desktop/api/Control/nn-control-imediaposition)
-   [<span data-ttu-id="9e5ac-145">**Imediaseeking**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-145">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [<span data-ttu-id="9e5ac-146">**Iqueuecommand**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-146">**IQueueCommand**</span></span>](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [<span data-ttu-id="9e5ac-147">**Iregisterserviceprovider**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-147">**IRegisterServiceProvider**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [<span data-ttu-id="9e5ac-148">**IResourceManager**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-148">**IResourceManager**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   <span data-ttu-id="9e5ac-149">**IServiceProvider**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-149">**IServiceProvider**</span></span>
-   [<span data-ttu-id="9e5ac-150">**Ivideoframestep**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-150">**IVideoFrameStep**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [<span data-ttu-id="9e5ac-151">**IVideoWindow**</span><span class="sxs-lookup"><span data-stu-id="9e5ac-151">**IVideoWindow**</span></span>](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a><span data-ttu-id="9e5ac-152">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="9e5ac-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e5ac-153">DirectShow-Objekte</span><span class="sxs-lookup"><span data-stu-id="9e5ac-153">DirectShow Objects</span></span>](directshow-objects.md)
</dt> </dl>

 

 



