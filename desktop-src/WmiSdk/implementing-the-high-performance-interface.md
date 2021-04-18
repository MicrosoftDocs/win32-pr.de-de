---
description: Da WMI einen hochleistungsfähigen Anbieter in eine WMI-oder Client Anwendung lädt, müssen Sie den Hochleistungs Anbieter als Prozess interner Server entwerfen.
ms.assetid: c37e3652-8c76-4125-ba62-ae860858797e
ms.tgt_platform: multiple
title: Implementieren der High-Performance-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea6e7f75e1031caacbb7379fba025baceb7b1a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347703"
---
# <a name="implementing-the-high-performance-interface"></a><span data-ttu-id="081c1-103">Implementieren der High-Performance-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="081c1-103">Implementing the High-Performance Interface</span></span>

<span data-ttu-id="081c1-104">Da WMI einen hochleistungsfähigen Anbieter in eine WMI-oder Client Anwendung lädt, müssen Sie den Hochleistungs Anbieter als Prozess interner Server entwerfen.</span><span class="sxs-lookup"><span data-stu-id="081c1-104">Because WMI loads a high-performance provider in-process to either WMI or a client application, you must design your high-performance provider as an in-process server.</span></span> <span data-ttu-id="081c1-105">Außerdem müssen Sie die Hochleistungs Anbieter Methoden in den Schnittstellen [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) und [**iwbemaktusher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) implementieren.</span><span class="sxs-lookup"><span data-stu-id="081c1-105">In addition, you must implement the high-performance provider methods in the [**IWbemHiPerfProvider**](/windows/desktop/api/Wbemprov/nn-wbemprov-iwbemhiperfprovider) and [**IWbemRefresher**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemrefresher) interfaces.</span></span>

<span data-ttu-id="081c1-106">Implementieren Sie einen Hochleistungs Anbieter als in-Process-Server.</span><span class="sxs-lookup"><span data-stu-id="081c1-106">You should implement a high-performance provider as an in-process server.</span></span> <span data-ttu-id="081c1-107">Eine Funktion, die Sie bei der Implementierung der Sicherheit eines in-Process-Servers berücksichtigen sollten, ist die Art und Weise, in der der Anbieter seinen eigenen Speicherort identifiziert.</span><span class="sxs-lookup"><span data-stu-id="081c1-107">One feature you should be aware of when implementing the security of an in-process server is how the provider identifies its own location.</span></span> <span data-ttu-id="081c1-108">Beim Laden von "in-Process" in WMI instanziiert WMI den Anbieter mithilfe einer CLSID.</span><span class="sxs-lookup"><span data-stu-id="081c1-108">When loaded in-process to WMI, WMI instantiates the provider using a CLSID.</span></span> <span data-ttu-id="081c1-109">Wenn die Client Anwendung im Prozess in eine Client Anwendung geladen wird, instanziiert Sie den Anbieter mit der **clientloadableclsid** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="081c1-109">When loaded in process to a client application, the client application instantiates the provider with the **ClientLoadableCLSID** property.</span></span> <span data-ttu-id="081c1-110">Wenn Sie einer CLSID und **clientloadableclsid** unterschiedliche Werte geben, können Sie den Anbieter ermitteln, ob er in-Process in WMI oder in eine Client Anwendung geladen wird.</span><span class="sxs-lookup"><span data-stu-id="081c1-110">By giving different values to a CLSID and **ClientLoadableCLSID**, you allow the provider to determine if it is loaded in-process to WMI or to a client application.</span></span> <span data-ttu-id="081c1-111">Wenn Sie sich in einem WMI-Prozess befinden, sollte der Anbieter alle notwendigen Client Identitätswechsel mithilfe von **clientloadableclsid** durchführen.</span><span class="sxs-lookup"><span data-stu-id="081c1-111">If located in a WMI process, the provider should do any necessary client impersonation by using **ClientLoadableCLSID**.</span></span> <span data-ttu-id="081c1-112">Wenn Sie sich in einem Client Prozess befinden, erbt der Anbieter das Zugriffs Token des Threads, für den er aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="081c1-112">If located in a client process, the provider inherits the access token of the thread it is called on.</span></span> <span data-ttu-id="081c1-113">Weitere Informationen zum Implementieren eines in-Process-Servers finden Sie im [Abschnitt zu com](https://msdn.microsoft.com/library/aa139695.aspx) in MSDN.</span><span class="sxs-lookup"><span data-stu-id="081c1-113">For more information about implementing an in-process server, see the [COM section](https://msdn.microsoft.com/library/aa139695.aspx) of MSDN.</span></span>

<span data-ttu-id="081c1-114">Als Prozess interner Server verwendet ein Hochleistungs Anbieter ein Aktualisierungs Objekt, um Daten für den Remote Client aktuell zu halten.</span><span class="sxs-lookup"><span data-stu-id="081c1-114">As an in-process server, a high-performance provider uses a refresher object to keep data current for the remote client.</span></span> <span data-ttu-id="081c1-115">In der folgenden Tabelle sind die Methoden aufgeführt, die Sie für einen Hochleistungs Anbieter implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="081c1-115">The following table lists methods that you must implement for a high-performance provider.</span></span>



| <span data-ttu-id="081c1-116">Methode</span><span class="sxs-lookup"><span data-stu-id="081c1-116">Method</span></span>                                                                                              | <span data-ttu-id="081c1-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="081c1-117">Feature</span></span>                                           |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="081c1-118">**IWbemHiPerfProvider:: queryinstance**</span><span class="sxs-lookup"><span data-stu-id="081c1-118">**IWbemHiPerfProvider::QueryInstances**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-queryinstances)                   | <span data-ttu-id="081c1-119">Abfragen</span><span class="sxs-lookup"><span data-stu-id="081c1-119">Queries</span></span>                                           |
| [<span data-ttu-id="081c1-120">**IWbemHiPerfProvider:: GetObjects**</span><span class="sxs-lookup"><span data-stu-id="081c1-120">**IWbemHiPerfProvider::GetObjects**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-getobjects)                           | <span data-ttu-id="081c1-121">Objekt Abruf</span><span class="sxs-lookup"><span data-stu-id="081c1-121">Object retrieval</span></span>                                  |
| [<span data-ttu-id="081c1-122">**IWbemHiPerfProvider:: "kreaterefresher"**</span><span class="sxs-lookup"><span data-stu-id="081c1-122">**IWbemHiPerfProvider::CreateRefresher**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefresher)                 | <span data-ttu-id="081c1-123">Erstellt ein Aktualisierungs Programm</span><span class="sxs-lookup"><span data-stu-id="081c1-123">Creates a refresher</span></span>                               |
| [<span data-ttu-id="081c1-124">**IWbemHiPerfProvider:: kreaterefreshableobject**</span><span class="sxs-lookup"><span data-stu-id="081c1-124">**IWbemHiPerfProvider::CreateRefreshableObject**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableobject) | <span data-ttu-id="081c1-125">Erstellt ein Aktualisier bares Instanzobjekt.</span><span class="sxs-lookup"><span data-stu-id="081c1-125">Creates a refreshable instance object</span></span>             |
| [<span data-ttu-id="081c1-126">**IWbemHiPerfProvider:: Aufzählung**</span><span class="sxs-lookup"><span data-stu-id="081c1-126">**IWbemHiPerfProvider::CreateRefreshableEnum**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum)     | <span data-ttu-id="081c1-127">Erstellt einen aktualisierbaren Enumerator.</span><span class="sxs-lookup"><span data-stu-id="081c1-127">Creates a refreshable enumerator</span></span>                  |
| [<span data-ttu-id="081c1-128">**IWbemHiPerfProvider:: stopaktualisieren**</span><span class="sxs-lookup"><span data-stu-id="081c1-128">**IWbemHiPerfProvider::StopRefreshing**</span></span>](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemhiperfprovider-stoprefreshing)                   | <span data-ttu-id="081c1-129">Beendet das Aktualisieren eines Enumerators oder Instanzobjekts.</span><span class="sxs-lookup"><span data-stu-id="081c1-129">Stops refreshing an enumerator or instance object</span></span> |
| [<span data-ttu-id="081c1-130">**Iwbemrefresh Sher:: Refresh**</span><span class="sxs-lookup"><span data-stu-id="081c1-130">**IWbemRefresher::Refresh**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemrefresher-refresh)                                           | <span data-ttu-id="081c1-131">Erstellt ein Aktualisierungs Programm</span><span class="sxs-lookup"><span data-stu-id="081c1-131">Creates a refresher</span></span>                               |



 

## <a name="related-topics"></a><span data-ttu-id="081c1-132">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="081c1-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="081c1-133">Erstellen eines Instanzanbieters in einen High-Performance-Anbieter</span><span class="sxs-lookup"><span data-stu-id="081c1-133">Making an Instance Provider into a High-Performance Provider</span></span>](making-an-instance-provider-into-a-high-performance-provider.md)
</dt> </dl>

 

 



