---
title: Übersicht über Netzwerkschnittstellen
description: Übersicht über Netzwerkschnittstellen
ms.assetid: 7aa7ff1b-9c81-4fee-afa9-2a9eed457360
keywords:
- Windows Media-Format-SDK, Netzwerkschnittstellen
- Windows Media-Format-SDK, Schnittstellen
- Advanced Systems Format (ASF), Netzwerkschnittstellen
- ASF (Advanced Systems Format), Netzwerkschnittstellen
- Advanced Systems Format (ASF), Schnittstellen Liste für Netzwerk Features
- ASF (Advanced Systems Format), Schnittstellen Liste für Netzwerk Features
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebd1c235e7e8b36964993bb24ce30977446d9af8
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2020
ms.locfileid: "103724131"
---
# <a name="overview-of-networking-interfaces"></a><span data-ttu-id="033ac-109">Übersicht über Netzwerkschnittstellen</span><span class="sxs-lookup"><span data-stu-id="033ac-109">Overview of Networking Interfaces</span></span>

<span data-ttu-id="033ac-110">Die Netzwerk Features dieses SDK werden mithilfe von Methoden der folgenden Schnittstellen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="033ac-110">The networking features of this SDK are supported through methods of the following interfaces.</span></span>



| <span data-ttu-id="033ac-111">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="033ac-111">Interface</span></span>                                                  | <span data-ttu-id="033ac-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="033ac-112">Description</span></span>                                                                                                                                           |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="033ac-113">**Iwmclientconnections**</span><span class="sxs-lookup"><span data-stu-id="033ac-113">**IWMClientConnections**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections)       | <span data-ttu-id="033ac-114">Ruft Informationen zu den Clients ab, die mit einer Netzwerk Senke verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="033ac-114">Gets information about the clients connected to a network sink.</span></span>                                                                                       |
| [<span data-ttu-id="033ac-115">**IWMClientConnections2**</span><span class="sxs-lookup"><span data-stu-id="033ac-115">**IWMClientConnections2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmclientconnections2)     | <span data-ttu-id="033ac-116">Bietet eine Methode zum erhalten von Informationen zu einem Client, der an eine Writer-netzwerksenke angefügt ist</span><span class="sxs-lookup"><span data-stu-id="033ac-116">Provides a method to get information about a client attached to a writer network sink.</span></span> <span data-ttu-id="033ac-117">Diese Schnittstelle erweitert die **iwmclientconnections** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="033ac-117">This interface extends the **IWMClientConnections** interface.</span></span> |
| [<span data-ttu-id="033ac-118">**Iwmkredentialcallback**</span><span class="sxs-lookup"><span data-stu-id="033ac-118">**IWMCredentialCallback**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmcredentialcallback)     | <span data-ttu-id="033ac-119">Stellt eine Rückruf Methode zum Abrufen von Benutzer Anmelde Informationen für den Zugriff auf eine Remote Website bereit.</span><span class="sxs-lookup"><span data-stu-id="033ac-119">Provides a callback method to acquire user credentials when accessing a remote site.</span></span>                                                                  |
| [<span data-ttu-id="033ac-120">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="033ac-120">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)           | <span data-ttu-id="033ac-121">Stellt erweiterte Methoden für das Reader-Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="033ac-121">Provides advanced methods on the reader object.</span></span>                                                                                                       |
| [<span data-ttu-id="033ac-122">**IWMReaderAdvanced3**</span><span class="sxs-lookup"><span data-stu-id="033ac-122">**IWMReaderAdvanced3**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced3)           | <span data-ttu-id="033ac-123">Erweitert die **IWMReaderAdvanced2** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="033ac-123">Extends the **IWMReaderAdvanced2** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="033ac-124">**IWMReaderAdvanced4**</span><span class="sxs-lookup"><span data-stu-id="033ac-124">**IWMReaderAdvanced4**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)           | <span data-ttu-id="033ac-125">Erweitert die **IWMReaderAdvanced3** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="033ac-125">Extends the **IWMReaderAdvanced3** interface.</span></span>                                                                                                         |
| [<span data-ttu-id="033ac-126">**Iwmreadernetworkconfig**</span><span class="sxs-lookup"><span data-stu-id="033ac-126">**IWMReaderNetworkConfig**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig)   | <span data-ttu-id="033ac-127">Konfiguriert die Netzwerkeinstellungen für das Reader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="033ac-127">Configures the network settings on the reader object.</span></span>                                                                                                 |
| [<span data-ttu-id="033ac-128">**IWMReaderNetworkConfig2**</span><span class="sxs-lookup"><span data-stu-id="033ac-128">**IWMReaderNetworkConfig2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadernetworkconfig2) | <span data-ttu-id="033ac-129">Konfiguriert zusätzliche Netzwerkeinstellungen für das Reader-Objekt.</span><span class="sxs-lookup"><span data-stu-id="033ac-129">Configures additional network settings on the reader object.</span></span> <span data-ttu-id="033ac-130">Diese Schnittstelle erweitert die **iwmreadernetworkconfig** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="033ac-130">This interface extends the **IWMReaderNetworkConfig** interface.</span></span>                         |
| [<span data-ttu-id="033ac-131">**Iwmschreiternetworksink**</span><span class="sxs-lookup"><span data-stu-id="033ac-131">**IWMWriterNetworkSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriternetworksink)       | <span data-ttu-id="033ac-132">Konfiguriert das netzwerksink-Objekt, das zum Schreiben digitaler Medien in ein Netzwerk verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="033ac-132">Configures the network sink object, which is used to write digital media to a network.</span></span>                                                                |
| [<span data-ttu-id="033ac-133">**Iwmschreibpushsink**</span><span class="sxs-lookup"><span data-stu-id="033ac-133">**IWMWriterPushSink**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriterpushsink)             | <span data-ttu-id="033ac-134">Konfiguriert das Push Sink-Objekt, das zum Verteilen digitaler Medien an Publishing Points verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="033ac-134">Configures the push sink object, which is used to distribute digital media to publishing points.</span></span>                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="033ac-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="033ac-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="033ac-136">**Implementieren von Netzwerkfunktionen**</span><span class="sxs-lookup"><span data-stu-id="033ac-136">**Implementing Network Functionality**</span></span>](implementing-network-functionality.md)
</dt> </dl>

 

 




