---
title: Rtmdeleteroute-Funktion (RTM. h)
description: Die rtmdeleteroute-Funktion löscht einen Routen Eintrag.
ms.assetid: a98026e9-40f5-42e9-943c-dfc561feef6d
keywords:
- Rtmdeleteroute-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmDeleteRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 310364bdb6e6ba7daf285316fcaaf16884e53929
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956694"
---
# <a name="rtmdeleteroute-function"></a><span data-ttu-id="92e09-104">Rtmdeleteroute-Funktion</span><span class="sxs-lookup"><span data-stu-id="92e09-104">RtmDeleteRoute function</span></span>

<span data-ttu-id="92e09-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="92e09-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="92e09-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="92e09-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="92e09-107">Die **rtmdeleteroute** -Funktion löscht einen Routen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="92e09-107">The **RtmDeleteRoute** function deletes a route entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="92e09-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="92e09-108">Syntax</span></span>


```C++
DWORD RtmDeleteRoute(
  _In_  HANDLE ClientHandle,
  _In_  PVOID  Route,
  _Out_ DWORD  Flags,
  _Out_ PVOID  CurBestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="92e09-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="92e09-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92e09-110">*Clienthandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92e09-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92e09-111">Handle, das den Client und somit das Routing Protokoll der hinzugefügten oder aktualisierten Route identifiziert.</span><span class="sxs-lookup"><span data-stu-id="92e09-111">Handle that identifies the client and therefore the routing protocol of the added or updated route.</span></span> <span data-ttu-id="92e09-112">Rufen Sie dieses Handle durch Aufrufen von [**rtmregisterclient**](rtmregisterclient.md)ab.</span><span class="sxs-lookup"><span data-stu-id="92e09-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> <dt>

<span data-ttu-id="92e09-113">*Route* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="92e09-113">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92e09-114">Zeiger auf eine Protokoll familienspezifische Struktur, die die neue oder aktualisierte Route angibt.</span><span class="sxs-lookup"><span data-stu-id="92e09-114">Pointer to a protocol-family-specific structure that specifies the new or updated route.</span></span> <span data-ttu-id="92e09-115">Die folgenden Felder werden vom Routing Tabellen-Manager verwendet, um die Routing Tabelle zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="92e09-115">The following fields are used by the routing table manager to update the routing table:</span></span>



| <span data-ttu-id="92e09-116">Wert</span><span class="sxs-lookup"><span data-stu-id="92e09-116">Value</span></span>                                                                                                                                                                                                         | <span data-ttu-id="92e09-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="92e09-117">Meaning</span></span>                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="RR_Network"></span><span id="rr_network"></span><span id="RR_NETWORK"></span><dl> <span data-ttu-id="92e09-118"><dt>**RR- \_ Netzwerk**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-118"><dt>**RR\_Network**</dt></span></span> </dl>                             | <span data-ttu-id="92e09-119">Gibt die Zielnetzwerk Nummer an.</span><span class="sxs-lookup"><span data-stu-id="92e09-119">Specifies the destination network number.</span></span> <br/>                                 |
| <span id="RR_InterfaceID"></span><span id="rr_interfaceid"></span><span id="RR_INTERFACEID"></span><dl> <span data-ttu-id="92e09-120"><dt>**RR- \_ interfakeid**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-120"><dt>**RR\_InterfaceID**</dt></span></span> </dl>             | <span data-ttu-id="92e09-121">Gibt den Index der Schnittstelle an, über die die Route empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="92e09-121">Specifies the index of the interface through which the route was received.</span></span><br/> |
| <span id="RR_NextHopAddress"></span><span id="rr_nexthopaddress"></span><span id="RR_NEXTHOPADDRESS"></span><dl> <span data-ttu-id="92e09-122"><dt>**RR \_ NextHopAddress**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-122"><dt>**RR\_NextHopAddress**</dt></span></span> </dl> | <span data-ttu-id="92e09-123">Gibt die Netzwerkadresse des Routers für den nächsten Hop an.</span><span class="sxs-lookup"><span data-stu-id="92e09-123">Specifies the network address of the next-hop router.</span></span><br/>                      |



 

</dd> <dt>

<span data-ttu-id="92e09-124">*Flags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="92e09-124">*Flags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92e09-125">Ein Zeiger auf einen Satz von Flags, die den Typ der Änderungs Meldung angeben, und die Informationen, die in den bereitgestellten Puffern abgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="92e09-125">Pointer to a set of flags that indicate the type of the change message, and what information was placed in the provided buffers.</span></span> <span data-ttu-id="92e09-126">Dieser Parameter ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="92e09-126">This parameter is one of the following values.</span></span>



| <span data-ttu-id="92e09-127">Flags</span><span class="sxs-lookup"><span data-stu-id="92e09-127">Flags</span></span>                                                                                                                                                                      | <span data-ttu-id="92e09-128">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="92e09-128">Meaning</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_NO_CHANGE"></span><span id="rtm_no_change"></span><dl> <span data-ttu-id="92e09-129"><dt>**RTM \_ keine \_ Änderung**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-129"><dt>**RTM\_NO\_CHANGE**</dt></span></span> </dl>             | <span data-ttu-id="92e09-130">Das Löschen der Route hat keine Auswirkung auf die beste Route zu einem Zielnetzwerk.</span><span class="sxs-lookup"><span data-stu-id="92e09-130">Deleting the route did not affect the best route to any destination network.</span></span> <span data-ttu-id="92e09-131">Anders ausgedrückt: ein anderer Eintrag stellt eine Route zum gleichen Zielnetzwerk dar und verfügt über eine niedrigere Metrik.</span><span class="sxs-lookup"><span data-stu-id="92e09-131">In other words, another entry represents a route to the same destination network and has a lower metric.</span></span><br/> |
| <span id="RTM_ROUTE_DELETED"></span><span id="rtm_route_deleted"></span><dl> <span data-ttu-id="92e09-132"><dt>**RTM- \_ Route \_ gelöscht**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-132"><dt>**RTM\_ROUTE\_DELETED**</dt></span></span> </dl> | <span data-ttu-id="92e09-133">Die gelöschte Route war die einzige Route, die für ein bestimmtes Zielnetzwerk verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="92e09-133">The route deleted was the only route available for a particular destination network.</span></span><br/>                                                                                                  |
| <span id="RTM_ROUTE_CHANGED"></span><span id="rtm_route_changed"></span><dl> <span data-ttu-id="92e09-134"><dt>**RTM- \_ Route \_ geändert**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-134"><dt>**RTM\_ROUTE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="92e09-135">Nachdem diese Route gelöscht wurde, wurde eine andere Route zu einem bestimmten Zielnetzwerk.</span><span class="sxs-lookup"><span data-stu-id="92e09-135">After this route was deleted, another route became the best route to a particular destination network.</span></span> <span data-ttu-id="92e09-136">" *Currbestroute* " zeigt auf die Informationen für die neue beste Route.</span><span class="sxs-lookup"><span data-stu-id="92e09-136">*CurBestRoute* points to the information for the new best route.</span></span><br/>               |



 

</dd> <dt>

<span data-ttu-id="92e09-137">*Cursor Route* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="92e09-137">*CurBestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92e09-138">Ein Zeiger auf eine-Struktur, die die aktuellen Informationen über die beste Route empfängt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="92e09-138">Pointer to a structure that receives the current best-route information, if any.</span></span> <span data-ttu-id="92e09-139">Der Typ der Struktur ist spezifisch für die Protokollfamilie, z. b. IP oder IPX.</span><span class="sxs-lookup"><span data-stu-id="92e09-139">The type of the structure is specific to the protocol family, for example, IP or IPX.</span></span>

<span data-ttu-id="92e09-140">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="92e09-140">This parameter is optional.</span></span> <span data-ttu-id="92e09-141">Wenn der Aufrufer **null** für diesen Parameter angibt, werden die aktuellen Informationen zur optimalen Route nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="92e09-141">If the caller specifies **NULL** for this parameter, the current best-route information is not returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92e09-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92e09-142">Return value</span></span>

<span data-ttu-id="92e09-143">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **kein \_ Fehler**.</span><span class="sxs-lookup"><span data-stu-id="92e09-143">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="92e09-144">Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="92e09-144">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="92e09-145">Wert</span><span class="sxs-lookup"><span data-stu-id="92e09-145">Value</span></span>                                                                                                       | <span data-ttu-id="92e09-146">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="92e09-146">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92e09-147"><dt>**Fehler bei \_ ungültigem \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-147"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="92e09-148">Der Clienthandle-Parameter ist kein gültiges Handle.</span><span class="sxs-lookup"><span data-stu-id="92e09-148">The client handle parameter is not a valid handle.</span></span><br/>                                          |
| <dl> <span data-ttu-id="92e09-149"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-149"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="92e09-150">Die Routen Struktur, auf die durch den *Routen* Parameter verwiesen wird, enthält einen Elementwert.</span><span class="sxs-lookup"><span data-stu-id="92e09-150">The route structure pointed to by the *Route* parameter contains a member value.</span></span><br/>            |
| <dl> <span data-ttu-id="92e09-151"><dt>**Fehler " \_ keine \_ solche \_ Route"**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-151"><dt>**ERROR\_NO\_SUCH\_ROUTE**</dt></span></span> </dl>       | <span data-ttu-id="92e09-152">Es sind keine Einträge in der Routing Tabelle vorhanden, die den Parametern der angegebenen Route entsprechen.</span><span class="sxs-lookup"><span data-stu-id="92e09-152">There are no entries in the routing table that match the parameters of the specified route.</span></span><br/> |
| <dl> <span data-ttu-id="92e09-153"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-153"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="92e09-154">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="92e09-154">There are insufficient resources to perform the operation.</span></span> <br/>                                 |



 

## <a name="remarks"></a><span data-ttu-id="92e09-155">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92e09-155">Remarks</span></span>

<span data-ttu-id="92e09-156">Die Funktion generiert eine Weiterleitungs Änderungs Meldung, wenn sich die beste Route zu einem Zielnetzwerk aufgrund des Löschvorgangs geändert hat.</span><span class="sxs-lookup"><span data-stu-id="92e09-156">The function generates a route-change message if the best route to a destination network has changed as the result of the deletion.</span></span> <span data-ttu-id="92e09-157">Die Weiterleitungs Änderungs Meldung wird jedoch nicht an den Client gesendet, von dem dieser aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="92e09-157">However, the route-change message is not sent to the client that makes this call.</span></span> <span data-ttu-id="92e09-158">Stattdessen werden relevante Informationen von dieser Funktion direkt an den Client zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="92e09-158">Instead, relevant information is returned by this function directly to that client.</span></span>

## <a name="requirements"></a><span data-ttu-id="92e09-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92e09-159">Requirements</span></span>



| <span data-ttu-id="92e09-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92e09-160">Requirement</span></span> | <span data-ttu-id="92e09-161">Wert</span><span class="sxs-lookup"><span data-stu-id="92e09-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92e09-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92e09-162">Minimum supported client</span></span><br/> | <span data-ttu-id="92e09-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="92e09-163">None supported</span></span><br/>                                                          |
| <span data-ttu-id="92e09-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92e09-164">Minimum supported server</span></span><br/> | <span data-ttu-id="92e09-165">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92e09-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92e09-166">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="92e09-166">End of server support</span></span><br/>    | <span data-ttu-id="92e09-167">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="92e09-167">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="92e09-168">Header</span><span class="sxs-lookup"><span data-stu-id="92e09-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="92e09-169"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-169"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="92e09-170">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="92e09-170">Library</span></span><br/>                  | <dl> <span data-ttu-id="92e09-171"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-171"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="92e09-172">DLL</span><span class="sxs-lookup"><span data-stu-id="92e09-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="92e09-173"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92e09-173"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92e09-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92e09-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92e09-175">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="92e09-175">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="92e09-176">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="92e09-176">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="92e09-177">**Rtmaddroute**</span><span class="sxs-lookup"><span data-stu-id="92e09-177">**RtmAddRoute**</span></span>](rtmaddroute.md)
</dt> <dt>

[<span data-ttu-id="92e09-178">**Rtmde queueroutechangemess**</span><span class="sxs-lookup"><span data-stu-id="92e09-178">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> </dl>

 

 





