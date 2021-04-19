---
description: Die folgenden Strukturen unterstützen die DRT-API-Funktionen (verteilte Routing Tabelle).
ms.assetid: 3ff85b24-5ec0-4b26-b30e-1bf8030a575d
title: Strukturen verteilter Routing Tabellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d454d2c28008422da897dc91ca9a3dc29db374b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349230"
---
# <a name="distributed-routing-table-structures"></a><span data-ttu-id="aa034-103">Strukturen verteilter Routing Tabellen</span><span class="sxs-lookup"><span data-stu-id="aa034-103">Distributed Routing Table Structures</span></span>

<span data-ttu-id="aa034-104">Die folgenden Strukturen unterstützen die DRT-API-Funktionen (verteilte Routing Tabelle).</span><span class="sxs-lookup"><span data-stu-id="aa034-104">The following structures support the Distributed Routing Table (DRT) API functions.</span></span>



| <span data-ttu-id="aa034-105">Struktur</span><span class="sxs-lookup"><span data-stu-id="aa034-105">Structure</span></span>                                                  | <span data-ttu-id="aa034-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="aa034-106">Description</span></span>                                                                                                                                                                              |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa034-107">**DRT- \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="aa034-107">**DRT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_data)                              | <span data-ttu-id="aa034-108">Enthält ein Daten-BLOB.</span><span class="sxs-lookup"><span data-stu-id="aa034-108">Contains a data blob.</span></span> <span data-ttu-id="aa034-109">Diese Struktur wird von mehreren DRT-Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="aa034-109">This structure is used by several DRT functions.</span></span>                                                                                                                   |
| [<span data-ttu-id="aa034-110">**DRT- \_ Registrierung**</span><span class="sxs-lookup"><span data-stu-id="aa034-110">**DRT\_REGISTRATION**</span></span>](/windows/desktop/api/drt/ns-drt-drt_registration)              | <span data-ttu-id="aa034-111">Enthält die Schlüssel Registrierung.</span><span class="sxs-lookup"><span data-stu-id="aa034-111">Contains the key registration.</span></span> <span data-ttu-id="aa034-112">Dies ist ein Member der [**DRT- \_ Such \_ Ergebnis**](/windows/desktop/api/drt/ns-drt-drt_search_result) Struktur und ein Argument, das an [**drtregisterkey**](/windows/desktop/api/drt/nf-drt-drtregisterkey)übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="aa034-112">This is a member of the [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) structure and is an argument passed to [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey).</span></span> |
| [<span data-ttu-id="aa034-113">**DRT- \_ Adresse**</span><span class="sxs-lookup"><span data-stu-id="aa034-113">**DRT\_ADDRESS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address)                        | <span data-ttu-id="aa034-114">Enthält Endpunkt Informationen zu einem DRT-Knoten, der an einer Suche beteiligt war.</span><span class="sxs-lookup"><span data-stu-id="aa034-114">Contains endpoint information about a DRT node that participated in a search.</span></span> <span data-ttu-id="aa034-115">Diese Informationen sind zum Debuggen von Konnektivitätsproblemen gedacht.</span><span class="sxs-lookup"><span data-stu-id="aa034-115">This information is intended for use in debugging connectivity problems.</span></span>                                   |
| [<span data-ttu-id="aa034-116">**Liste der DRT- \_ Adressen \_**</span><span class="sxs-lookup"><span data-stu-id="aa034-116">**DRT\_ADDRESS\_LIST**</span></span>](/windows/desktop/api/drt/ns-drt-drt_address_list)             | <span data-ttu-id="aa034-117">Enthält einen Satz von [**DRT- \_ Adress**](/windows/desktop/api/drt/ns-drt-drt_address) Strukturen, die die während einer Suche nach einem Schlüssel verbundenen Knoten darstellen.</span><span class="sxs-lookup"><span data-stu-id="aa034-117">Contains a set of [**DRT\_ADDRESS**](/windows/desktop/api/drt/ns-drt-drt_address) structures representing the nodes contacted during a search for a key.</span></span>                                                             |
| [<span data-ttu-id="aa034-118">**DRT- \_ Sicherheits \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="aa034-118">**DRT\_SECURITY\_PROVIDER**</span></span>](/windows/desktop/api/Drt/ns-drt-drt_security_provider)   | <span data-ttu-id="aa034-119">Definiert die Schnittstelle, die von einem Sicherheitsanbieter implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="aa034-119">Defines the interface that must be implemented by a security provider.</span></span>                                                                                                                   |
| [<span data-ttu-id="aa034-120">**DRT- \_ Bootstrap- \_ Anbieter**</span><span class="sxs-lookup"><span data-stu-id="aa034-120">**DRT\_BOOTSTRAP\_PROVIDER**</span></span>](/windows/desktop/api/drt/ns-drt-drt_bootstrap_provider) | <span data-ttu-id="aa034-121">Definiert die Schnittstelle, die von einem Bootstrap-Anbieter implementiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="aa034-121">Defines the interface that must be implemented by a bootstrap provider.</span></span>                                                                                                                  |
| [<span data-ttu-id="aa034-122">**DRT- \_ Einstellungen**</span><span class="sxs-lookup"><span data-stu-id="aa034-122">**DRT\_SETTINGS**</span></span>](/windows/desktop/api/drt/ns-drt-drt_settings)                      | <span data-ttu-id="aa034-123">Definiert DRT-Einstellungen bei der Initialisierung.</span><span class="sxs-lookup"><span data-stu-id="aa034-123">Defines DRT settings at initialization.</span></span> <span data-ttu-id="aa034-124">Diese Struktur wird als Argument an [**drtopen**](/windows/desktop/api/drt/nf-drt-drtopen)übermittelt.</span><span class="sxs-lookup"><span data-stu-id="aa034-124">This structure is passed as an argument to [**DrtOpen**](/windows/desktop/api/drt/nf-drt-drtopen).</span></span>                                                                           |
| [<span data-ttu-id="aa034-125">**DRT- \_ Such \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="aa034-125">**DRT\_SEARCH\_INFO**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_info)               | <span data-ttu-id="aa034-126">Definiert eine Suchabfrage.</span><span class="sxs-lookup"><span data-stu-id="aa034-126">Defines a search query.</span></span> <span data-ttu-id="aa034-127">Diese Struktur wird als Argument an [**drtstartsearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch)übermittelt.</span><span class="sxs-lookup"><span data-stu-id="aa034-127">This structure is passed as an argument to [**DrtStartSearch**](/windows/desktop/api/drt/nf-drt-drtstartsearch).</span></span>                                                                             |
| [<span data-ttu-id="aa034-128">**DRT- \_ Such \_ Ergebnis**</span><span class="sxs-lookup"><span data-stu-id="aa034-128">**DRT\_SEARCH\_RESULT**</span></span>](/windows/desktop/api/drt/ns-drt-drt_search_result)           | <span data-ttu-id="aa034-129">Enthält ein Suchergebnis.</span><span class="sxs-lookup"><span data-stu-id="aa034-129">Contains a search result.</span></span> <span data-ttu-id="aa034-130">Diese Struktur wird von [**drtgetsearchresult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="aa034-130">This structure is returned by [**DrtGetSearchResult**](/windows/desktop/api/drt/nf-drt-drtgetsearchresult).</span></span>                                                                                |
| [<span data-ttu-id="aa034-131">**DRT- \_ Ereignis \_ Daten**</span><span class="sxs-lookup"><span data-stu-id="aa034-131">**DRT\_EVENT\_DATA**</span></span>](/windows/desktop/api/drt/ns-drt-drt_event_data)                 | <span data-ttu-id="aa034-132">Enthält die Ereignisdaten, die zurückgegeben werden, indem [**drtgeteventdata**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) aufgerufen wird, nachdem eine Anwendung ein Ereignis Signal empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="aa034-132">Contains the event data returned by calling [**DrtGetEventData**](/windows/desktop/api/drt/nf-drt-drtgeteventdata) after an application receives an event signal.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="aa034-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="aa034-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa034-134">Verteilte Routing Tabellen-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="aa034-134">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="aa034-135">Tabellen Funktionen für verteilte Routing</span><span class="sxs-lookup"><span data-stu-id="aa034-135">Distributed Routing Table Functions</span></span>](distributed-routing-table-functions.md)
</dt> <dt>

[<span data-ttu-id="aa034-136">Tabellen-API Referenz zu verteiltem Routing</span><span class="sxs-lookup"><span data-stu-id="aa034-136">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



