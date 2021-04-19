---
description: Zusammenfassung des filterthreading
ms.assetid: b7e42101-75c9-428d-9dc7-e625242dbc1e
title: Zusammenfassung des filterthreading
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa0a7c4ce19c46a0f7b05db3cb4d82e8f2aa0beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362974"
---
# <a name="summary-of-filter-threading"></a><span data-ttu-id="ad866-103">Zusammenfassung des filterthreading</span><span class="sxs-lookup"><span data-stu-id="ad866-103">Summary of Filter Threading</span></span>

<span data-ttu-id="ad866-104">Die folgenden Methoden werden im streamingthread aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="ad866-104">The following methods are called on the streaming thread:</span></span>

-   [<span data-ttu-id="ad866-105">**IMemInputPin:: Receive**</span><span class="sxs-lookup"><span data-stu-id="ad866-105">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="ad866-106">**IMemInputPin:: receivemultiple**</span><span class="sxs-lookup"><span data-stu-id="ad866-106">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="ad866-107">**IPin:: EndOf Stream**</span><span class="sxs-lookup"><span data-stu-id="ad866-107">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="ad866-108">**IPin:: newsegment**</span><span class="sxs-lookup"><span data-stu-id="ad866-108">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)
-   [<span data-ttu-id="ad866-109">**Imemzuordcator:: GetBuffer**</span><span class="sxs-lookup"><span data-stu-id="ad866-109">**IMemAllocator::GetBuffer**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

<span data-ttu-id="ad866-110">Die folgenden Methoden werden im Anwendungs Thread aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="ad866-110">The following methods are called on the application thread:</span></span>

-   <span data-ttu-id="ad866-111">Statusänderungen: [**ibasefilter:: joinfiltergraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**imediafilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**imediafilter::**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop)End, [**iqualitycontrol:: setsink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).</span><span class="sxs-lookup"><span data-stu-id="ad866-111">State changes: [**IBaseFilter::JoinFilterGraph**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-joinfiltergraph), [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause), [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run), [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop), [**IQualityControl::SetSink**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-setsink).</span></span>
-   <span data-ttu-id="ad866-112">Referenzuhr: [**imediafilter:: getsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**imediafilter:: setsyncsource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).</span><span class="sxs-lookup"><span data-stu-id="ad866-112">Reference clock: [**IMediaFilter::GetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-getsyncsource), [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource).</span></span>
-   <span data-ttu-id="ad866-113">PIN-Vorgänge: [**ibasefilter:: findpin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin:: connectedto**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin:: connectionmediatype**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::D isconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin:: receiveconnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).</span><span class="sxs-lookup"><span data-stu-id="ad866-113">Pin operations: [**IBaseFilter::FindPin**](/windows/desktop/api/Strmif/nf-strmif-ibasefilter-findpin), [**IPin::Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect), [**IPin::ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto), [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype), [**IPin::Disconnect**](/windows/desktop/api/Strmif/nf-strmif-ipin-disconnect), [**IPin::ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection).</span></span>
-   <span data-ttu-id="ad866-114">Zuordnerfunktionen: [**IMemInputPin:: getallocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin:: notifyzuweisung**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).</span><span class="sxs-lookup"><span data-stu-id="ad866-114">Allocator functions: [**IMemInputPin::GetAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocator), [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator).</span></span>
-   <span data-ttu-id="ad866-115">Leeren: [**IPin:: beginflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span><span class="sxs-lookup"><span data-stu-id="ad866-115">Flushing: [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush), [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush).</span></span>

<span data-ttu-id="ad866-116">Diese Liste ist nicht vollständig.</span><span class="sxs-lookup"><span data-stu-id="ad866-116">This list is not exhaustive.</span></span> <span data-ttu-id="ad866-117">Wenn Sie einen Filter implementieren, müssen Sie in Erwägung ziehen, welche Methoden den Filter Zustand ändern und welche Methoden Streamingvorgänge durchführen.</span><span class="sxs-lookup"><span data-stu-id="ad866-117">When you implement a filter, you must consider which methods change the filter state, and which methods perform streaming operations.</span></span>

 

 



