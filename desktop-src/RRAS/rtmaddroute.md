---
title: Rtmaddroute-Funktion (RTM. h)
description: Die rtmaddroute-Funktion fügt einen Routen Eintrag hinzu oder aktualisiert einen vorhandenen Routen Eintrag.
ms.assetid: 09a9b57d-f10b-40b7-a3c1-2e0613f29431
keywords:
- Rtmaddroute-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmAddRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0c3ee68c9b026fc37457819777e69d2be7984e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339342"
---
# <a name="rtmaddroute-function"></a><span data-ttu-id="7c435-104">Rtmaddroute-Funktion</span><span class="sxs-lookup"><span data-stu-id="7c435-104">RtmAddRoute function</span></span>

<span data-ttu-id="7c435-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7c435-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="7c435-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="7c435-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="7c435-107">Die **rtmaddroute** -Funktion fügt einen Routen Eintrag hinzu oder aktualisiert einen vorhandenen Routen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="7c435-107">The **RtmAddRoute** function adds a route entry or updates an existing route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c435-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c435-108">Syntax</span></span>


```C++
DWORD RtmAddRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _In_  DWORD  TimeToLive,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="7c435-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c435-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c435-110">*Clienthandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c435-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c435-111">Handle, das den Client identifiziert, und damit das Routing Protokoll, das die Route hinzugefügt oder aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="7c435-111">Handle that identifies the client, and therefore the routing protocol, that added or updated the route.</span></span> <span data-ttu-id="7c435-112">Rufen Sie dieses Handle durch Aufrufen von [**rtmregisterclient**](rtmregisterclient.md)ab.</span><span class="sxs-lookup"><span data-stu-id="7c435-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="7c435-113">*Route* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c435-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c435-114">Zeiger auf eine Protokoll familienspezifische Struktur, die die neue oder aktualisierte Route angibt.</span><span class="sxs-lookup"><span data-stu-id="7c435-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="7c435-115">Die folgenden Felder werden vom Routing Tabellen-Manager verwendet, um die Routing Tabelle zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="7c435-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="7c435-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7c435-116">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="7c435-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7c435-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="7c435-118"><dt>**RR- \_ Netzwerk**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-118"><dt>**RR\_Network**</dt></span></span> </dl>                                                     | <span data-ttu-id="7c435-119">Gibt die Zielnetzwerk Nummer an.</span><span class="sxs-lookup"><span data-stu-id="7c435-119">Specifies the destination network number.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                      |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="7c435-120"><dt>**RR- \_ interfakeid**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>                                     | <span data-ttu-id="7c435-121">Gibt den Index der Schnittstelle an, über die die Route empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="7c435-121">Specifies the index of the interface through which the route was received.</span></span><br/>                                                                                                                                                                                                                                                                                                                     |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="7c435-122"><dt>**RR \_ NextHopAddress**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl>                         | <span data-ttu-id="7c435-123">Gibt die Adresse des Routers für den nächsten Hop an.</span><span class="sxs-lookup"><span data-stu-id="7c435-123">Specifies the address of the next-hop router.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                  |
| <span id="RR_FamilySpecificData"></span><span id="rr_familyspecificdata"></span><span id="RR_FAMILYSPECIFICDATA"></span><dl> <span data-ttu-id="7c435-124"><dt>**RR \_ familyspecificdata**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-124"><dt>**RR\_FamilySpecificData**</dt></span></span> </dl>         | <span data-ttu-id="7c435-125">Gibt Daten an, die für die Protokollfamilie spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="7c435-125">Specifies data that is specific to the protocol family.</span></span> <span data-ttu-id="7c435-126">Obwohl die Daten für den Routing Tabellen-Manager transparent sind, werden Sie beim Vergleichen von Routen zum ermitteln, ob sich die Routeninformationen geändert haben, berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="7c435-126">Although the data is transparent to the routing table manager, it is considered when comparing routes to determine if route information has changed.</span></span> <span data-ttu-id="7c435-127">Die Daten werden auch verwendet, um Metrikwerte festzulegen, die unabhängig vom Routing Protokoll sind.</span><span class="sxs-lookup"><span data-stu-id="7c435-127">The data is also used to set metric values that are independent of the routing protocol.</span></span> <span data-ttu-id="7c435-128">Folglich werden diese Daten verwendet, um die beste Route für das Zielnetzwerk zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="7c435-128">Consequently, this data is used to determine the best route for the destination network.</span></span><br/> |
| <span id="RR_ProtocolSpecificData"></span><span id="rr_protocolspecificdata"></span><span id="RR_PROTOCOLSPECIFICDATA"></span><dl> <span data-ttu-id="7c435-129"><dt>**RR \_ protocolspecificdata**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-129"><dt>**RR\_ProtocolSpecificData**</dt></span></span> </dl> | <span data-ttu-id="7c435-130">Gibt Daten an, die für das Routing Protokoll spezifisch sind, das die Route bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="7c435-130">Specifies data which is specific to the routing protocol that supplied the route.</span></span><br/>                                                                                                                                                                                                                                                                                                              |
| <span id="RR_TimeStamp"></span><span id="rr_timestamp"></span><span id="RR_TIMESTAMP"></span><dl> <span data-ttu-id="7c435-131"><dt>**RR- \_ Zeitstempel**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-131"><dt>**RR\_TimeStamp**</dt></span></span> </dl>                                             | <span data-ttu-id="7c435-132">Gibt die aktuelle Systemzeit an.</span><span class="sxs-lookup"><span data-stu-id="7c435-132">Specifies the current system time.</span></span> <span data-ttu-id="7c435-133">Dieses Feld wird vom Routing Tabellen-Manager festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c435-133">This field is set by the routing table manager.</span></span><br/>                                                                                                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="7c435-134">*Timeto-Live* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7c435-134">*TimeToLive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c435-135">Gibt die Anzahl der Sekunden an, die die angegebene Route in der Routing Tabelle aufbewahrt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c435-135">Specifies the number of seconds the specified route should be kept in the routing table.</span></span> <span data-ttu-id="7c435-136">Wenn dieser Parameter auf unendlich festgelegt ist, wird die Route so lange beibehalten, bis Sie explizit gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="7c435-136">If this parameter is set to INFINITE, the route is kept until it is explicitly deleted.</span></span> <span data-ttu-id="7c435-137">Das aktuelle Limit für *Timeto Live* beträgt 2147483 Sek. (24 + Tage).</span><span class="sxs-lookup"><span data-stu-id="7c435-137">The current limit for *TimeToLive* is 2147483 sec (24+ days).</span></span>

</dd> <dt>

<span data-ttu-id="7c435-138">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7c435-138">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c435-139">Zeiger auf eine **DWORD** -Variable.</span><span class="sxs-lookup"><span data-stu-id="7c435-139">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="7c435-140">Der Wert dieser Variablen wird vom Routing Tabellen-Manager festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c435-140">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="7c435-141">Der Wert gibt den Typ der Änderung an und welche Informationen in den bereitgestellten Puffern zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="7c435-141">The value indicates the type of the change, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="7c435-142">Bei diesem Parameter handelt es sich um einen der folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="7c435-142">This parameter is one of the following.</span></span>



| <span data-ttu-id="7c435-143">Flags</span><span class="sxs-lookup"><span data-stu-id="7c435-143">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="7c435-144">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="7c435-144">Meaning</span></span>                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="7c435-145"><dt>**RTM \_ keine \_ Änderung**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-145"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="7c435-146">Das Hinzufügen oder aktualisieren hat entweder keinen der wichtigen Routen Parameter geändert, oder der betroffene Routen Eintrag ist nicht die beste Route zwischen den Einträgen für das Zielnetzwerk.</span><span class="sxs-lookup"><span data-stu-id="7c435-146">The addition or update either did not change any of the significant route parameters, or the route entry affected is not the best route among the entries for the destination network.</span></span><br/>                                                                                                          |
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="7c435-147"><dt>**RTM- \_ Route \_ hinzugefügt**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-147"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="7c435-148">Die Route wurde für das Zielnetzwerk hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7c435-148">The route was added for the destination network.</span></span> <span data-ttu-id="7c435-149">Der Parameter " *currbestroute* " verweist auf die Informationen für die hinzugefügte Route.</span><span class="sxs-lookup"><span data-stu-id="7c435-149">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                                    |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="7c435-150"><dt>**RTM- \_ Route \_ geändert**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-150"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="7c435-151">Mindestens einer der wichtigen Parameter wurde geändert, um die beste Route zum Zielnetzwerk zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="7c435-151">At least one of the significant parameters was changed for the best route to the destination network.</span></span> <span data-ttu-id="7c435-152">Die wichtigsten Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="7c435-152">The significant parameters are:</span></span> <br/> <span data-ttu-id="7c435-153">Protokoll Bezeichner</span><span class="sxs-lookup"><span data-stu-id="7c435-153">Protocol identifier</span></span><br/> <span data-ttu-id="7c435-154">Schnittstellen Index</span><span class="sxs-lookup"><span data-stu-id="7c435-154">Interface index</span></span><br/> <span data-ttu-id="7c435-155">Adresse des nächsten Hops</span><span class="sxs-lookup"><span data-stu-id="7c435-155">Next-hop address</span></span><br/> <span data-ttu-id="7c435-156">Protokoll familienspezifische Daten (einschließlich Routingmetriken)</span><span class="sxs-lookup"><span data-stu-id="7c435-156">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="7c435-157">Der *prevbestroute* -Parameter verweist auf die Routeninformationen wie vor der Änderung.</span><span class="sxs-lookup"><span data-stu-id="7c435-157">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="7c435-158">Der Parameter " *currbestroute* " zeigt auf die aktuellen Routeninformationen (d. h. nach Änderung).</span><span class="sxs-lookup"><span data-stu-id="7c435-158">The *CurBestRoute* parameter points to the current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="7c435-159">*Cursor Route* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7c435-159">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c435-160">Ein Zeiger auf eine-Struktur, die die aktuellen Informationen über die beste Route empfängt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7c435-160">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="7c435-161">Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.</span><span class="sxs-lookup"><span data-stu-id="7c435-161">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="7c435-162">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7c435-162">This parameter is optional.</span></span> <span data-ttu-id="7c435-163">Wenn der Aufrufer **null** für diesen Parameter angibt, werden die aktuellen Informationen zur optimalen Route nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c435-163">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="7c435-164">*Prevbestroute* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7c435-164">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c435-165">Ein Zeiger auf eine-Struktur, die die vorherigen Informationen über die beste Route empfängt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7c435-165">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="7c435-166">Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.</span><span class="sxs-lookup"><span data-stu-id="7c435-166">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="7c435-167">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="7c435-167">This parameter is optional.</span></span> <span data-ttu-id="7c435-168">Wenn der Aufrufer für diesen Parameter **null** angibt, werden die vorherigen Informationen zur optimalen Route nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c435-168">If the caller specifies **NULL** for this parameter the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c435-169">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c435-169">Return value</span></span>

<span data-ttu-id="7c435-170">Der Rückgabewert ist einer der folgenden Codes.</span><span class="sxs-lookup"><span data-stu-id="7c435-170">The return value is one of the following codes.</span></span>



| <span data-ttu-id="7c435-171">Wert</span><span class="sxs-lookup"><span data-stu-id="7c435-171">Value</span></span>                                                                                                       | <span data-ttu-id="7c435-172">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c435-172">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7c435-173"><dt>**kein \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-173"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="7c435-174">Die Route wurde erfolgreich hinzugefügt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7c435-174">The route was added or updated successfully.</span></span><br/>                 |
| <dl> <span data-ttu-id="7c435-175"><dt>**Fehler bei \_ ungültigem \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-175"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="7c435-176">Der Clienthandle-Parameter ist kein gültiges Handle.</span><span class="sxs-lookup"><span data-stu-id="7c435-176">The client handle parameter is not a valid handle.</span></span><br/>           |
| <dl> <span data-ttu-id="7c435-177"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-177"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="7c435-178">Die Routen Struktur enthält einen ungültigen Parameter.</span><span class="sxs-lookup"><span data-stu-id="7c435-178">The route structure contains an invalid parameter.</span></span><br/>           |
| <dl> <span data-ttu-id="7c435-179"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-179"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="7c435-180">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="7c435-180">There are insufficient resources to carry out the operation.</span></span><br/> |
| <dl> <span data-ttu-id="7c435-181"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-181"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="7c435-182">Es ist nicht genügend Arbeitsspeicher zum Zuordnen des Routen Eintrags vorhanden.</span><span class="sxs-lookup"><span data-stu-id="7c435-182">There is insufficient memory to allocate the route entry.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="7c435-183">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c435-183">Remarks</span></span>

<span data-ttu-id="7c435-184">Die-Funktion generiert eine Weiterleitungs Änderungs Meldung, wenn sich die beste Route zu einem Zielnetzwerk aufgrund dieses Vorgangs geändert hat.</span><span class="sxs-lookup"><span data-stu-id="7c435-184">The function generates a route-change message if the best route to a destination network has changed as the result of this operation.</span></span> <span data-ttu-id="7c435-185">Die Weiterleitungs Änderungs Meldung wird jedoch nicht an den Client gesendet, von dem dieser aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="7c435-185">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="7c435-186">Stattdessen werden relevante Informationen von dieser Funktion direkt über die *Flags*, die Parameter " *currbestroute*" und " *prevbestroute* " an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c435-186">Instead, relevant information is returned by this function directly to that client through the *Flags*, *CurBestRoute*, and *PrevBestRoute* parameters.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c435-187">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c435-187">Requirements</span></span>



| <span data-ttu-id="7c435-188">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c435-188">Requirement</span></span> | <span data-ttu-id="7c435-189">Wert</span><span class="sxs-lookup"><span data-stu-id="7c435-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7c435-190">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7c435-190">Minimum supported client</span></span><br/> | <span data-ttu-id="7c435-191">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7c435-191">None supported</span></span><br/>                                                          |
| <span data-ttu-id="7c435-192">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7c435-192">Minimum supported server</span></span><br/> | <span data-ttu-id="7c435-193">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7c435-193">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="7c435-194">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="7c435-194">End of server support</span></span><br/>    | <span data-ttu-id="7c435-195">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="7c435-195">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="7c435-196">Header</span><span class="sxs-lookup"><span data-stu-id="7c435-196">Header</span></span><br/>                   | <dl> <span data-ttu-id="7c435-197"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-197"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c435-198">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c435-198">Library</span></span><br/>                  | <dl> <span data-ttu-id="7c435-199"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-199"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c435-200">DLL</span><span class="sxs-lookup"><span data-stu-id="7c435-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c435-201"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c435-201"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c435-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c435-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c435-203">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="7c435-203">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="7c435-204">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="7c435-204">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="7c435-205">**Rtmdeleteroute**</span><span class="sxs-lookup"><span data-stu-id="7c435-205">**RtmDeleteRoute**</span></span>](rtmdeleteroute.md)
</dt> <dt>

[<span data-ttu-id="7c435-206">**Rtmde queueroutechangemess**</span><span class="sxs-lookup"><span data-stu-id="7c435-206">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





