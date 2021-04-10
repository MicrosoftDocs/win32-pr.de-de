---
title: Rtmde queueroutechangemess-Funktion (RTM. h)
description: Die rtmdequeueroutechangemess-Funktion gibt die nächste Weiterleitungs Änderungs Meldung in der Warteschlange zurück, die dem angegebenen Client zugeordnet ist.
ms.assetid: 44f2116a-3c8d-4ac6-896e-b12930b218a5
keywords:
- Rtmde queueroutechangemess-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmDequeueRouteChangeMessage
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 448df230742b03f82294de102bf14b50fefa035c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104390"
---
# <a name="rtmdequeueroutechangemessage-function"></a><span data-ttu-id="bdbac-104">Rtmde queueroutechangemess-Funktion</span><span class="sxs-lookup"><span data-stu-id="bdbac-104">RtmDequeueRouteChangeMessage function</span></span>

<span data-ttu-id="bdbac-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="bdbac-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="bdbac-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="bdbac-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="bdbac-107">Die **rtmdequeueroutechangemess** -Funktion gibt die nächste Weiterleitungs Änderungs Meldung in der Warteschlange zurück, die dem angegebenen Client zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="bdbac-107">The **RtmDequeueRouteChangeMessage** function returns the next route-change message in the queue associated with the specified client.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdbac-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bdbac-108">Syntax</span></span>


```C++
DWORD RtmDequeueRouteChangeMessage(
  _In_  HANDLE ClientHandle,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute,
  _Out_ PVOID  PrevBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="bdbac-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bdbac-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdbac-110">*Clienthandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bdbac-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbac-111">Handle, das den Client identifiziert, für den der Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bdbac-111">Handle that identifies the client for which the operation is performed.</span></span> <span data-ttu-id="bdbac-112">Rufen Sie dieses Handle durch Aufrufen von [**rtmregisterclient**](rtmregisterclient.md)ab.</span><span class="sxs-lookup"><span data-stu-id="bdbac-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="bdbac-113">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bdbac-113">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbac-114">Zeiger auf eine **DWORD** -Variable.</span><span class="sxs-lookup"><span data-stu-id="bdbac-114">Pointer to a **DWORD** variable.</span></span> <span data-ttu-id="bdbac-115">Der Wert dieser Variablen wird vom Routing Tabellen-Manager festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bdbac-115">The value of this variable is set by the routing table manager.</span></span> <span data-ttu-id="bdbac-116">Der-Wert gibt den Typ der Änderungs Meldung an und gibt an, welche Informationen in den bereitgestellten Puffern zurückgegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="bdbac-116">The value specifies the type of the change message, and what information was returned in the provided buffers.</span></span> <span data-ttu-id="bdbac-117">Bei diesem Parameter handelt es sich um einen der folgenden Parameter.</span><span class="sxs-lookup"><span data-stu-id="bdbac-117">This parameter is one of the following.</span></span>



| <span data-ttu-id="bdbac-118">Flags</span><span class="sxs-lookup"><span data-stu-id="bdbac-118">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="bdbac-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="bdbac-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                           |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ROUTE_ADDED"></span><span id="rtm_route_added"></span><dl> <span data-ttu-id="bdbac-120"><dt>**RTM- \_ Route \_ hinzugefügt**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-120"><dt>**RTM\_ROUTE\_ADDED**</dt></span></span> </dl>       | <span data-ttu-id="bdbac-121">Die erste Route wurde für ein bestimmtes Zielnetzwerk hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="bdbac-121">The first route was added for a particular destination network.</span></span> <span data-ttu-id="bdbac-122">Der Parameter " *currbestroute* " verweist auf die Informationen für die hinzugefügte Route.</span><span class="sxs-lookup"><span data-stu-id="bdbac-122">The *CurBestRoute* parameter points to the information for the added route.</span></span><br/>                                                                                                                                                            |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="bdbac-123"><dt>**RTM- \_ Route \_ gelöscht**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-123"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="bdbac-124">Die einzige Route, die für ein bestimmtes Zielnetzwerk verfügbar ist, wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bdbac-124">The only route available for a particular destination network was deleted.</span></span> <span data-ttu-id="bdbac-125">Der *prevbestroute* -Parameter verweist auf die Informationen für die gelöschte Route.</span><span class="sxs-lookup"><span data-stu-id="bdbac-125">The *PrevBestRoute* parameter points to the information for the deleted route.</span></span><br/>                                                                                                                                              |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="bdbac-126"><dt>**RTM- \_ Route \_ geändert**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-126"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="bdbac-127">Mindestens einer der wichtigen Parameter wurde für eine optimale Route zu einem bestimmten Zielnetzwerk geändert.</span><span class="sxs-lookup"><span data-stu-id="bdbac-127">At least one of the significant parameters was changed for a best route to a particular destination network.</span></span> <span data-ttu-id="bdbac-128">Die wichtigsten Parameter sind:</span><span class="sxs-lookup"><span data-stu-id="bdbac-128">The significant parameters are:</span></span> <br/> <span data-ttu-id="bdbac-129">Protokoll Bezeichner</span><span class="sxs-lookup"><span data-stu-id="bdbac-129">Protocol identifier</span></span><br/> <span data-ttu-id="bdbac-130">Schnittstellen Index</span><span class="sxs-lookup"><span data-stu-id="bdbac-130">Interface index</span></span><br/> <span data-ttu-id="bdbac-131">Adresse des nächsten Hops</span><span class="sxs-lookup"><span data-stu-id="bdbac-131">Next-hop address</span></span><br/> <span data-ttu-id="bdbac-132">Protokoll familienspezifische Daten (einschließlich Routingmetriken)</span><span class="sxs-lookup"><span data-stu-id="bdbac-132">Protocol-family-specific data (including route metrics)</span></span><br/> |



 

<span data-ttu-id="bdbac-133">Der *prevbestroute* -Parameter verweist auf die Routeninformationen wie vor der Änderung.</span><span class="sxs-lookup"><span data-stu-id="bdbac-133">The *PrevBestRoute* parameter points to the route information as it was before the change.</span></span> <span data-ttu-id="bdbac-134">Der Parameter " *currbestroute* " zeigt auf die aktuellen Routeninformationen (d. h. nach Änderung).</span><span class="sxs-lookup"><span data-stu-id="bdbac-134">The *CurBestRoute* parameter points to current (that is, after-change) route information.</span></span>

</dd> <dt>

<span data-ttu-id="bdbac-135">*Cursor Route* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bdbac-135">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbac-136">Ein Zeiger auf eine-Struktur, die die aktuellen Informationen zur optimalen Route (sofern vorhanden) empfängt.</span><span class="sxs-lookup"><span data-stu-id="bdbac-136">Pointer to a structure that receives the current best-route information (if any).</span></span> <span data-ttu-id="bdbac-137">Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.</span><span class="sxs-lookup"><span data-stu-id="bdbac-137">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="bdbac-138">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bdbac-138">This parameter is optional.</span></span> <span data-ttu-id="bdbac-139">Wenn der Aufrufer **null** für diesen Parameter angibt, werden die aktuellen Informationen zur optimalen Route nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bdbac-139">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> <dt>

<span data-ttu-id="bdbac-140">*Prevbestroute* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bdbac-140">*PrevBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdbac-141">Ein Zeiger auf eine-Struktur, die die vorherigen Informationen über die beste Route empfängt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="bdbac-141">Pointer to a structure that receives the previous best-route information, if any.</span></span> <span data-ttu-id="bdbac-142">Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.</span><span class="sxs-lookup"><span data-stu-id="bdbac-142">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="bdbac-143">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="bdbac-143">This parameter is optional.</span></span> <span data-ttu-id="bdbac-144">Wenn der Aufrufer **null** für diesen Parameter angibt, werden die vorherigen Informationen mit der besten Route nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bdbac-144">If the caller specifies **NULL** for this parameter, the previous best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdbac-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bdbac-145">Return value</span></span>

<span data-ttu-id="bdbac-146">Der Rückgabewert ist einer der folgenden Codes.</span><span class="sxs-lookup"><span data-stu-id="bdbac-146">The return value is one of the following codes.</span></span>



| <span data-ttu-id="bdbac-147">Wert</span><span class="sxs-lookup"><span data-stu-id="bdbac-147">Value</span></span>                                                                                                       | <span data-ttu-id="bdbac-148">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bdbac-148">Description</span></span>                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bdbac-149"><dt>**kein \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-149"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="bdbac-150">Diese Meldung war die letzte Meldung in der Warteschlange des Clients.</span><span class="sxs-lookup"><span data-stu-id="bdbac-150">This message was the last message in the client's queue.</span></span> <span data-ttu-id="bdbac-151">Das Ereignis Objekt wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="bdbac-151">The event object is reset.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="bdbac-152"><dt>**Fehler bei \_ ungültigem \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-152"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="bdbac-153">Der *Clienthandle* -Parameter ist kein gültiges Handle, oder der Client hat bei der Registrierung kein Ereignis Objekt für die Benachrichtigung von Änderungs Meldungen bereitgestellt (siehe [**rtmregisterclient**](rtmregisterclient.md)).</span><span class="sxs-lookup"><span data-stu-id="bdbac-153">The *ClientHandle* parameter is not a valid handle, or at registration the client did not provide an event object for change message notification (see [**RtmRegisterClient**](rtmregisterclient.md)).</span></span><br/>                           |
| <dl> <span data-ttu-id="bdbac-154"><dt>**\_Weitere Fehler \_ Meldungen**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-154"><dt>**ERROR\_MORE\_MESSAGES**</dt></span></span> </dl>        | <span data-ttu-id="bdbac-155">Die Warteschlange des Clients enthält zusätzliche Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="bdbac-155">The client's queue contains additional messages.</span></span> <span data-ttu-id="bdbac-156">Der Client sollte **rtmdequeueroutechangemessage** so bald wie möglich erneut abrufen, damit der Routing Tabellen-Manager die Ressourcen freigeben kann, die den ausstehenden Nachrichten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="bdbac-156">The client should call **RtmDequeueRouteChangeMessage** again as soon as possible to allow the routing table manager to free the resources associated with the pending messages.</span></span><br/> |
| <dl> <span data-ttu-id="bdbac-157"><dt>**Fehler \_ \_ Meldungen**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-157"><dt>**ERROR\_NO\_MESSAGES**</dt></span></span> </dl>          | <span data-ttu-id="bdbac-158">Die Warteschlange des Clients enthält keine Nachrichten. der-Befehl wurde nicht angefordert.</span><span class="sxs-lookup"><span data-stu-id="bdbac-158">The client's queue contains no messages; the call was unsolicited.</span></span> <span data-ttu-id="bdbac-159">Das Ereignis wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="bdbac-159">The event is reset.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="bdbac-160"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-160"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="bdbac-161">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bdbac-161">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="bdbac-162">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bdbac-162">Requirements</span></span>



| <span data-ttu-id="bdbac-163">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bdbac-163">Requirement</span></span> | <span data-ttu-id="bdbac-164">Wert</span><span class="sxs-lookup"><span data-stu-id="bdbac-164">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bdbac-165">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bdbac-165">Minimum supported client</span></span><br/> | <span data-ttu-id="bdbac-166">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="bdbac-166">None supported</span></span><br/>                                                          |
| <span data-ttu-id="bdbac-167">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bdbac-167">Minimum supported server</span></span><br/> | <span data-ttu-id="bdbac-168">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bdbac-168">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bdbac-169">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="bdbac-169">End of server support</span></span><br/>    | <span data-ttu-id="bdbac-170">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bdbac-170">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="bdbac-171">Header</span><span class="sxs-lookup"><span data-stu-id="bdbac-171">Header</span></span><br/>                   | <dl> <span data-ttu-id="bdbac-172"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-172"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="bdbac-173">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bdbac-173">Library</span></span><br/>                  | <dl> <span data-ttu-id="bdbac-174"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-174"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="bdbac-175">DLL</span><span class="sxs-lookup"><span data-stu-id="bdbac-175">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bdbac-176"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bdbac-176"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bdbac-177">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bdbac-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdbac-178">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="bdbac-178">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="bdbac-179">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="bdbac-179">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="bdbac-180">**Rtmregisterclient**</span><span class="sxs-lookup"><span data-stu-id="bdbac-180">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





