---
description: Erweiterte Erfassungs Themen
ms.assetid: 407702b2-5f4f-424d-a3ec-b0473e1b0da3
title: Erweiterte Erfassungs Themen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4c4e5a077f6f8b17543250efa0f10091f0917e8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125066"
---
# <a name="advanced-capture-topics"></a><span data-ttu-id="e4476-103">Erweiterte Erfassungs Themen</span><span class="sxs-lookup"><span data-stu-id="e4476-103">Advanced Capture Topics</span></span>

<span data-ttu-id="e4476-104">In diesem Abschnitt werden einige erweiterte Aspekte der Video Erfassung in DirectShow beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e4476-104">This section describes some advanced aspects of video capture in DirectShow.</span></span> <span data-ttu-id="e4476-105">Die meisten der in diesem Abschnitt beschriebenen Probleme werden automatisch von der [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) -Schnittstelle behandelt.</span><span class="sxs-lookup"><span data-stu-id="e4476-105">Most of the issues described in this section are automatically handled by the [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface.</span></span> <span data-ttu-id="e4476-106">Die hier aufgeführten Informationen sind jedoch möglicherweise nützlich, wenn Sie Probleme mit einer Video Erfassungs Anwendung beheben müssen.</span><span class="sxs-lookup"><span data-stu-id="e4476-106">However, the information here may be useful if you need to troubleshoot a video capture application.</span></span> <span data-ttu-id="e4476-107">Sie sollten diesen Abschnitt auch lesen, wenn Ihre Anwendung ein benutzerdefiniertes Erfassungs Diagramm erstellt und Sie feststellen, dass ICaptureGraphBuilder2 nicht Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="e4476-107">You should also read this section if your application builds a custom capture graph of some kind and you find that ICaptureGraphBuilder2 does not suit your needs.</span></span> <span data-ttu-id="e4476-108">Zum Schluss enthält dieser Abschnitt einige Informationen zur Verwendung des VMR-Filters (Video Mischungs-Renderer) in einer Video Erfassungs Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e4476-108">Finally, this section contains some information about using the Video Mixing Renderer (VMR) filter in a video capture application.</span></span>

<span data-ttu-id="e4476-109">Es ist möglich, ein Video Erfassungs Diagramm vollständig mit [**igraphbuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) -Methoden zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e4476-109">It is possible to build a video capture graph entirely using [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) methods.</span></span> <span data-ttu-id="e4476-110">Sie können auch die beiden Schnittstellen kombinieren, indem Sie ICaptureGraphBuilder2 für einige Aufgaben und igraphbuilder für andere Benutzer verwenden.</span><span class="sxs-lookup"><span data-stu-id="e4476-110">You can also combine the two interfaces, using ICaptureGraphBuilder2 for some tasks and IGraphBuilder for others.</span></span>

<span data-ttu-id="e4476-111">Dieser Abschnitt enthält die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="e4476-111">This section contains the following topics:</span></span>

-   [<span data-ttu-id="e4476-112">Behandeln von Repaint-Ereignissen in der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="e4476-112">Handling Repaint Events in Video Capture</span></span>](handling-repaint-events-in-video-capture.md)
-   [<span data-ttu-id="e4476-113">Arbeiten mit PIN-Kategorien</span><span class="sxs-lookup"><span data-stu-id="e4476-113">Working with Pin Categories</span></span>](working-with-pin-categories.md)
-   [<span data-ttu-id="e4476-114">Verwenden des Smart Tee-Filters</span><span class="sxs-lookup"><span data-stu-id="e4476-114">Using the Smart Tee Filter</span></span>](using-the-smart-tee-filter.md)
-   [<span data-ttu-id="e4476-115">Verwenden des Overlay-Mischers bei der Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="e4476-115">Using the Overlay Mixer in Video Capture</span></span>](using-the-overlay-mixer-in-video-capture.md)
-   [<span data-ttu-id="e4476-116">VideoPort-Pins</span><span class="sxs-lookup"><span data-stu-id="e4476-116">Video Port Pins</span></span>](video-port-pins.md)
-   [<span data-ttu-id="e4476-117">VideoInfo2-Formattyp</span><span class="sxs-lookup"><span data-stu-id="e4476-117">VideoInfo2 Format Type</span></span>](videoinfo2-format-type.md)
-   [<span data-ttu-id="e4476-118">Erstellen von Kernel-Mode filtern</span><span class="sxs-lookup"><span data-stu-id="e4476-118">Creating Kernel-Mode Filters</span></span>](creating-kernel-mode-filters.md)
-   [<span data-ttu-id="e4476-119">WDM-Klassen Treiber Filter</span><span class="sxs-lookup"><span data-stu-id="e4476-119">WDM Class Driver Filters</span></span>](wdm-class-driver-filters.md)
-   [<span data-ttu-id="e4476-120">Verwenden der WDDM-Erfassung in DirectShow</span><span class="sxs-lookup"><span data-stu-id="e4476-120">Using WDDM Capture in DirectShow</span></span>](using-wddm-capture-in-directshow.md)

## <a name="related-topics"></a><span data-ttu-id="e4476-121">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e4476-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e4476-122">Video Erfassung</span><span class="sxs-lookup"><span data-stu-id="e4476-122">Video Capture</span></span>](video-capture.md)
</dt> </dl>

 

 



