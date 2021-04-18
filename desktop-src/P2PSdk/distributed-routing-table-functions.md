---
description: Die DRT-API (verteilte Routing Tabelle) nutzt die folgenden Funktionen.
ms.assetid: 1ceff217-d410-47fa-99a2-8588f001859e
title: Tabellen Funktionen für verteilte Routing
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cd48c3a60f458285ce5f607f9ab6bcf7a557cd9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358904"
---
# <a name="distributed-routing-table-functions"></a><span data-ttu-id="06002-103">Tabellen Funktionen für verteilte Routing</span><span class="sxs-lookup"><span data-stu-id="06002-103">Distributed Routing Table Functions</span></span>

<span data-ttu-id="06002-104">Die DRT-API (verteilte Routing Tabelle) nutzt die folgenden Funktionen.</span><span class="sxs-lookup"><span data-stu-id="06002-104">The Distributed Routing Table (DRT) API utilizes the following functions.</span></span>

## <a name="lifetime-management-functions"></a><span data-ttu-id="06002-105">Lebensdauer Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="06002-105">Lifetime Management Functions</span></span>



| <span data-ttu-id="06002-106">Funktion</span><span class="sxs-lookup"><span data-stu-id="06002-106">Function</span></span>                                           | <span data-ttu-id="06002-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06002-107">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06002-108">**Drtopen**</span><span class="sxs-lookup"><span data-stu-id="06002-108">**DrtOpen**</span></span>](/windows/desktop/api/drt/nf-drt-drtopen)                         | <span data-ttu-id="06002-109">Erstellt eine lokale DRT-Instanz unter Verwendung der von der [**DRT- \_ Einstellungs**](/windows/desktop/api/drt/ns-drt-drt_settings) Struktur angegebenen Kriterien.</span><span class="sxs-lookup"><span data-stu-id="06002-109">Creates a local DRT instance using criteria specified by the [**DRT\_SETTINGS**](/windows/desktop/api/drt/ns-drt-drt_settings) structure.</span></span>  |
| [<span data-ttu-id="06002-110">**Drtclose**</span><span class="sxs-lookup"><span data-stu-id="06002-110">**DrtClose**</span></span>](/windows/desktop/api/drt/nf-drt-drtclose)                       | <span data-ttu-id="06002-111">Schließt die lokale Instanz der DRT und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="06002-111">Closes and removes the local instance of the DRT.</span></span>                                                              |
| [<span data-ttu-id="06002-112">**Drtgeteventdata**</span><span class="sxs-lookup"><span data-stu-id="06002-112">**DrtGetEventData**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdata)         | <span data-ttu-id="06002-113">Ruft die einem signalisierten Ereignis zugeordneten Ereignisdaten ab.</span><span class="sxs-lookup"><span data-stu-id="06002-113">Retrieves event data associated with a signaled event.</span></span>                                                         |
| [<span data-ttu-id="06002-114">**Drtgeteventdatasize**</span><span class="sxs-lookup"><span data-stu-id="06002-114">**DrtGetEventDataSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgeteventdatasize) | <span data-ttu-id="06002-115">Gibt die Größe der [**DRT- \_ Ereignis \_ Daten**](/windows/desktop/api/drt/ns-drt-drt_event_data) Struktur zurück, die einem signalisierten Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="06002-115">Returns the size of the [**DRT\_EVENT\_DATA**](/windows/desktop/api/drt/ns-drt-drt_event_data) structure associated with a signaled event.</span></span> |



 

## <a name="module-management-functions"></a><span data-ttu-id="06002-116">Modul Verwaltungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="06002-116">Module Management Functions</span></span>



| <span data-ttu-id="06002-117">Funktion</span><span class="sxs-lookup"><span data-stu-id="06002-117">Function</span></span>                                                                           | <span data-ttu-id="06002-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06002-118">Description</span></span>                                                                                                                           |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06002-119">**Drtkreatepnrpbootstrapresolver**</span><span class="sxs-lookup"><span data-stu-id="06002-119">**DrtCreatePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatepnrpbootstrapresolver)           | <span data-ttu-id="06002-120">Erstellt einen Bootstrap-Konflikt Löser basierend auf dem PNRP-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="06002-120">Creates a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="06002-121">**Drtdeletepnrpbootstrapresolver**</span><span class="sxs-lookup"><span data-stu-id="06002-121">**DrtDeletePnrpBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletepnrpbootstrapresolver)           | <span data-ttu-id="06002-122">Löscht einen Bootstrap-Konflikt Löser basierend auf dem PNRP-Protokoll.</span><span class="sxs-lookup"><span data-stu-id="06002-122">Deletes a bootstrap resolver based on the PNRP protocol.</span></span>                                                                              |
| [<span data-ttu-id="06002-123">**Drtkreatednsbootstrapresolver**</span><span class="sxs-lookup"><span data-stu-id="06002-123">**DrtCreateDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatednsbootstrapresolver)             | <span data-ttu-id="06002-124">Erstellt einen Bootstrap-Anbieter, der nach Namen einen bekannten Host kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="06002-124">Creates a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="06002-125">**Drtdeletednsbootstrapresolver**</span><span class="sxs-lookup"><span data-stu-id="06002-125">**DrtDeleteDnsBootstrapResolver**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletednsbootstrapresolver)             | <span data-ttu-id="06002-126">Löscht einen Bootstrap-Anbieter, der nach Namen einen bekannten Host kontaktiert.</span><span class="sxs-lookup"><span data-stu-id="06002-126">Deletes a bootstrap provider that will contact a well known host by name.</span></span>                                                             |
| [<span data-ttu-id="06002-127">**DrtCreateIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="06002-127">**DrtCreateIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreateipv6udptransport)                     | <span data-ttu-id="06002-128">Erstellt einen Transport auf der Grundlage des IPv6-UDP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="06002-128">Creates a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="06002-129">**DrtDeleteIpv6UdpTransport**</span><span class="sxs-lookup"><span data-stu-id="06002-129">**DrtDeleteIpv6UdpTransport**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeleteipv6udptransport)                     | <span data-ttu-id="06002-130">Löscht einen Transport auf der Grundlage des IPv6-UDP-Protokolls.</span><span class="sxs-lookup"><span data-stu-id="06002-130">Deletes a transport based on the IPv6 UDP protocol.</span></span>                                                                                   |
| [<span data-ttu-id="06002-131">**Drtkreatederivedkeysecurityprovider**</span><span class="sxs-lookup"><span data-stu-id="06002-131">**DrtCreateDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkeysecurityprovider) | <span data-ttu-id="06002-132">Erstellt einen abgeleiteten Schlüssel Sicherheitsanbieter für das DRT.</span><span class="sxs-lookup"><span data-stu-id="06002-132">Creates a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="06002-133">**Drtkreatederivedkey**</span><span class="sxs-lookup"><span data-stu-id="06002-133">**DrtCreateDerivedKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatederivedkey)                                 | <span data-ttu-id="06002-134">Erstellt einen Schlüssel, der von [**drtregisterkey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) verwendet werden kann, wenn der DRT einen abgeleiteten Schlüssel Sicherheitsanbieter verwendet.</span><span class="sxs-lookup"><span data-stu-id="06002-134">Creates a key that can be utilized by [**DrtRegisterKey**](/windows/desktop/api/drt/nf-drt-drtregisterkey) when the DRT is using a derived key security provider.</span></span> |
| [<span data-ttu-id="06002-135">**Drtdeletederivedkeysecurityprovider**</span><span class="sxs-lookup"><span data-stu-id="06002-135">**DrtDeleteDerivedKeySecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletederivedkeysecurityprovider) | <span data-ttu-id="06002-136">Löscht einen abgeleiteten Schlüssel Sicherheitsanbieter für das DRT.</span><span class="sxs-lookup"><span data-stu-id="06002-136">Deletes a derived key security provider for the DRT.</span></span>                                                                                  |
| [<span data-ttu-id="06002-137">**Drtkreatenullsecurityprovider**</span><span class="sxs-lookup"><span data-stu-id="06002-137">**DrtCreateNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtcreatenullsecurityprovider)             | <span data-ttu-id="06002-138">Erstellt einen NULL-Sicherheitsanbieter.</span><span class="sxs-lookup"><span data-stu-id="06002-138">Creates a null security provider.</span></span> <span data-ttu-id="06002-139">Dieser Sicherheitsanbieter erfordert keine Knoten zum Authentifizieren von Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="06002-139">This security provider does not require nodes to authenticate keys.</span></span>                                 |
| [<span data-ttu-id="06002-140">**Drtdeletenullsecurityprovider**</span><span class="sxs-lookup"><span data-stu-id="06002-140">**DrtDeleteNullSecurityProvider**</span></span>](/windows/desktop/api/drt/nf-drt-drtdeletenullsecurityprovider)             | <span data-ttu-id="06002-141">Löscht einen NULL-Sicherheitsanbieter.</span><span class="sxs-lookup"><span data-stu-id="06002-141">Deletes a null security provider.</span></span>                                                                                                     |



 

## <a name="registration-functions"></a><span data-ttu-id="06002-142">Registrierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="06002-142">Registration Functions</span></span>



| <span data-ttu-id="06002-143">Funktion</span><span class="sxs-lookup"><span data-stu-id="06002-143">Function</span></span>                                     | <span data-ttu-id="06002-144">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06002-144">Description</span></span>                                                    |
|----------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="06002-145">**Drtregisterkey**</span><span class="sxs-lookup"><span data-stu-id="06002-145">**DrtRegisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtregisterkey)     | <span data-ttu-id="06002-146">Registriert einen Schlüssel in der DRT.</span><span class="sxs-lookup"><span data-stu-id="06002-146">Registers a key in the DRT.</span></span>                                    |
| [<span data-ttu-id="06002-147">**Drtupdatekey**</span><span class="sxs-lookup"><span data-stu-id="06002-147">**DrtUpdateKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtupdatekey)         | <span data-ttu-id="06002-148">Aktualisiert die einem registrierten Schlüssel zugeordneten Anwendungsdaten.</span><span class="sxs-lookup"><span data-stu-id="06002-148">Updates the application data associated with a registered key.</span></span> |
| [<span data-ttu-id="06002-149">**Drtunregisterkey**</span><span class="sxs-lookup"><span data-stu-id="06002-149">**DrtUnregisterKey**</span></span>](/windows/desktop/api/drt/nf-drt-drtunregisterkey) | <span data-ttu-id="06002-150">Hebt die Registrierung eines Schlüssels aus dem DRT auf.</span><span class="sxs-lookup"><span data-stu-id="06002-150">Deregisters a key from the DRT.</span></span>                                |



 

## <a name="search-functions"></a><span data-ttu-id="06002-151">Suchfunktionen</span><span class="sxs-lookup"><span data-stu-id="06002-151">Search Functions</span></span>



| <span data-ttu-id="06002-152">Funktion</span><span class="sxs-lookup"><span data-stu-id="06002-152">Function</span></span>                                                 | <span data-ttu-id="06002-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06002-153">Description</span></span>                                                                                                                                                                                                             |
|----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="06002-154">**Drtstartsearch**</span><span class="sxs-lookup"><span data-stu-id="06002-154">**DrtStartSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtstartsearch)                 | <span data-ttu-id="06002-155">Durchsucht das DRT nach einem Schlüssel mithilfe der in der [**DRT- \_ Such \_ Informations**](/windows/desktop/api/drt/ns-drt-drt_search_info) Struktur angegebenen Kriterien.</span><span class="sxs-lookup"><span data-stu-id="06002-155">Searches the DRT for a key using criteria specified in the [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span>                                                                                                      |
| [<span data-ttu-id="06002-156">**Drtcontinuesearch**</span><span class="sxs-lookup"><span data-stu-id="06002-156">**DrtContinueSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtcontinuesearch)           | <span data-ttu-id="06002-157">Setzt die Suche nach einem DRT- \_ \_ \_ Suchpfad für einen Schlüssel in der DRT fort.</span><span class="sxs-lookup"><span data-stu-id="06002-157">Continues a DRT\_SEARCH\_RETURN\_PATH search for a key in the DRT.</span></span> <span data-ttu-id="06002-158">Diese Funktion wird nur verwendet, wenn das **-Flag in der** zugeordneten [**DRT- \_ Such \_ Informations**](/windows/desktop/api/drt/ns-drt-drt_search_info) Struktur auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="06002-158">This function is used only when the **fIterative** flag is set to **TRUE** in the associated [**DRT\_SEARCH\_INFO**](/windows/desktop/api/drt/ns-drt-drt_search_info) structure.</span></span> |
| [<span data-ttu-id="06002-159">**Drtgetsearchresult**</span><span class="sxs-lookup"><span data-stu-id="06002-159">**DrtGetSearchResult**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresult)         | <span data-ttu-id="06002-160">Ruft die Suchergebnisse ab.</span><span class="sxs-lookup"><span data-stu-id="06002-160">Retrieves the search result(s).</span></span>                                                                                                                                                                                         |
| [<span data-ttu-id="06002-161">**Drtgetsearchresultsize**</span><span class="sxs-lookup"><span data-stu-id="06002-161">**DrtGetSearchResultSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchresultsize) | <span data-ttu-id="06002-162">Gibt die Größe des nächsten verfügbaren Suchergebnisses zurück.</span><span class="sxs-lookup"><span data-stu-id="06002-162">Returns the size of the next available search result.</span></span>                                                                                                                                                                   |
| [<span data-ttu-id="06002-163">**Drtgetsearchpath**</span><span class="sxs-lookup"><span data-stu-id="06002-163">**DrtGetSearchPath**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpath)             | <span data-ttu-id="06002-164">Gibt eine Liste der Knoten zurück, die während des Such Vorgangs kontaktiert wurden.</span><span class="sxs-lookup"><span data-stu-id="06002-164">Returns a list of nodes contacted during the search operation.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="06002-165">**Drtgetsearchpathsize**</span><span class="sxs-lookup"><span data-stu-id="06002-165">**DrtGetSearchPathSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetsearchpathsize)     | <span data-ttu-id="06002-166">Gibt die Größe des Suchpfads zurück, der die Anzahl der im Suchvorgang verwendeten Knoten darstellt.</span><span class="sxs-lookup"><span data-stu-id="06002-166">Returns the size of the search path, which represents the number of nodes utilized in the search operation.</span></span>                                                                                                             |
| [<span data-ttu-id="06002-167">**Drtendsearch**</span><span class="sxs-lookup"><span data-stu-id="06002-167">**DrtEndSearch**</span></span>](/windows/desktop/api/drt/nf-drt-drtendsearch)                     | <span data-ttu-id="06002-168">Bricht eine Suche nach einem Schlüssel in einem DRT ab. Folglich wird die Rückgabe von Ergebnissen über das [**DRT- \_ Such \_ Ergebnis**](/windows/desktop/api/drt/ns-drt-drt_search_result) angehalten.</span><span class="sxs-lookup"><span data-stu-id="06002-168">Cancels a search for a key in a DRT, and as a result, the return of results via [**DRT\_SEARCH\_RESULT**](/windows/desktop/api/drt/ns-drt-drt_search_result) is stopped.</span></span> <span data-ttu-id="06002-169">Diese API kann zu einem beliebigen Zeitpunkt aufgerufen werden, nachdem eine Suche ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="06002-169">This API can be called at any point after a search is issued.</span></span>              |



 

## <a name="instance-name-functions"></a><span data-ttu-id="06002-170">Instanznamensfunktionen</span><span class="sxs-lookup"><span data-stu-id="06002-170">Instance Name Functions</span></span>



| <span data-ttu-id="06002-171">Funktion</span><span class="sxs-lookup"><span data-stu-id="06002-171">Function</span></span>                                                 | <span data-ttu-id="06002-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="06002-172">Description</span></span>                                                      |
|----------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="06002-173">**Drtgetinstancename**</span><span class="sxs-lookup"><span data-stu-id="06002-173">**DrtGetInstanceName**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancename)         | <span data-ttu-id="06002-174">Ruft den Namen ab, der einer DRT-Instanz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="06002-174">Gets the name associated with a DRT instance.</span></span>                    |
| [<span data-ttu-id="06002-175">**Drtgetinstancenamesize**</span><span class="sxs-lookup"><span data-stu-id="06002-175">**DrtGetInstanceNameSize**</span></span>](/windows/desktop/api/drt/nf-drt-drtgetinstancenamesize) | <span data-ttu-id="06002-176">Gibt die Größe des Tabellen Instanznamens der verteilten Routing Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="06002-176">Returns the size of the Distributed Routing Table instance name.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="06002-177">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="06002-177">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06002-178">Verteilte Routing Tabellen-Enumerationen</span><span class="sxs-lookup"><span data-stu-id="06002-178">Distributed Routing Table Enumerations</span></span>](distributed-routing-table-enumerations.md)
</dt> <dt>

[<span data-ttu-id="06002-179">Strukturen verteilter Routing Tabellen</span><span class="sxs-lookup"><span data-stu-id="06002-179">Distributed Routing Table Structures</span></span>](distributed-routing-table-structures.md)
</dt> <dt>

[<span data-ttu-id="06002-180">Tabellen-API Referenz zu verteiltem Routing</span><span class="sxs-lookup"><span data-stu-id="06002-180">Distributed Routing Table API Reference</span></span>](distributed-routing-table-api-reference.md)
</dt> </dl>

 

 



