---
title: Writer-netzwerksink-Objekt
description: Writer-netzwerksink-Objekt
ms.assetid: f7765b42-693a-4f48-b750-17579e860b6d
keywords:
- Windows Media-Format-SDK, Writer-netzwerksenkenobjekte
- Advanced Systems Format (ASF), Writer-netzwerksenkenobjekte
- ASF (Advanced Systems Format), Writer-netzwerksenkenobjekte
- Objekte, Writer-netzwerksenke-Objekte
- Writer-netzwerksink-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c85af356c1d326ddaaf3703ca87c3b7bdd1628b9
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "104101351"
---
# <a name="writer-network-sink-object"></a><span data-ttu-id="b986b-108">Writer-netzwerksink-Objekt</span><span class="sxs-lookup"><span data-stu-id="b986b-108">Writer Network Sink Object</span></span>

<span data-ttu-id="b986b-109">Das Writer-netzwerksink-Objekt wird verwendet, um digitale Medien in ein Netzwerk zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="b986b-109">The writer network sink object is used to write digital media to a network.</span></span>

<span data-ttu-id="b986b-110">Das Writer-netzwerksink-Objekt wird von der Funktion [**wmkreateschreiternetworksink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink)erstellt, mit der ein Zeiger auf eine **iwmschreiternetworksink** -Schnittstelle festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="b986b-110">The writer network sink object is created by the function [**WMCreateWriterNetworkSink**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriternetworksink), which sets a pointer to an **IWMWriterNetworkSink** interface.</span></span> <span data-ttu-id="b986b-111">Die anderen Schnittstellen des Writer-netzwerksink-Objekts können durch Aufrufen der **QueryInterface** -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b986b-111">The other interfaces of the writer network sink object can be obtained by calling the **QueryInterface** method.</span></span>



| <span data-ttu-id="b986b-112">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b986b-112">Interface</span></span>                                              | <span data-ttu-id="b986b-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b986b-113">Description</span></span>                                                                                                                                                                                                     |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b986b-114">**Iwmclientconnections**</span><span class="sxs-lookup"><span data-stu-id="b986b-114">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)   | <span data-ttu-id="b986b-115">Sammelt Informationen zu verbundenen Clients.</span><span class="sxs-lookup"><span data-stu-id="b986b-115">Collects information on connected clients.</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="b986b-116">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="b986b-116">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2) | <span data-ttu-id="b986b-117">Ruft erweiterte Client Informationen ab.</span><span class="sxs-lookup"><span data-stu-id="b986b-117">Retrieves advanced client information.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="b986b-118">**Iwmregistercallback**</span><span class="sxs-lookup"><span data-stu-id="b986b-118">**IWMRegisterCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)     | <span data-ttu-id="b986b-119">Ermöglicht es der Anwendung, Statusmeldungen aus dem-Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b986b-119">Enables the application to get status messages from the object.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="b986b-120">**Iwmschreiternetworksink**</span><span class="sxs-lookup"><span data-stu-id="b986b-120">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)   | <span data-ttu-id="b986b-121">Öffnet und schließt Ports, legt die maximale Anzahl von Clients fest und ruft Sie ab, die eine Verbindung mit dem sink-Objekt herstellen können, legt das vom Writer-Objekt zu verwendende Netzwerkprotokoll fest und führt andere erweiterte Funktionen aus.</span><span class="sxs-lookup"><span data-stu-id="b986b-121">Opens and closes ports, sets and retrieves the maximum number of clients that can connect to the sink object, sets the network protocol to be used by the writer object, and performs other advanced functions.</span></span> |
| [<span data-ttu-id="b986b-122">**Iwmschreibsink**</span><span class="sxs-lookup"><span data-stu-id="b986b-122">**IWMWriterSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink)                 | <span data-ttu-id="b986b-123">Weist Arbeitsspeicher zu, bestimmt, ob die Senke in Echtzeit ausgeführt wird, und verarbeitet mehrere Rückruf Funktionen.</span><span class="sxs-lookup"><span data-stu-id="b986b-123">Allocates memory, determines whether the sink is operating in real time, and handles several callback functions.</span></span>                                                                                                |



 

<span data-ttu-id="b986b-124">Die folgende Rückruf Schnittstelle kann von der Anwendung implementiert werden, um den Fortschritt eines Writer-netzwerksink-Objekts zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="b986b-124">The following callback interface can be implemented by the application to track the progress of a writer network sink object.</span></span>



| <span data-ttu-id="b986b-125">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b986b-125">Interface</span></span>                                      | <span data-ttu-id="b986b-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b986b-126">Description</span></span>                                                                    |
|------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="b986b-127">**Iwmstatus Callback**</span><span class="sxs-lookup"><span data-stu-id="b986b-127">**IWMStatusCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstatuscallback) | <span data-ttu-id="b986b-128">Erforderlich, wenn Statusinformationen an die Host Anwendung übermittelt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b986b-128">Required when status information must be communicated to the host application.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b986b-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b986b-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b986b-130">**Übertragungen von ASF-Daten**</span><span class="sxs-lookup"><span data-stu-id="b986b-130">**Broadcasting ASF Data**</span></span>](broadcasting-asf-data.md)
</dt> <dt>

[<span data-ttu-id="b986b-131">**Objekte**</span><span class="sxs-lookup"><span data-stu-id="b986b-131">**Objects**</span></span>](objects.md)
</dt> <dt>

[<span data-ttu-id="b986b-132">**Arbeiten mit Writer-senken**</span><span class="sxs-lookup"><span data-stu-id="b986b-132">**Working with Writer Sinks**</span></span>](working-with-writer-sinks.md)
</dt> </dl>

 

 




