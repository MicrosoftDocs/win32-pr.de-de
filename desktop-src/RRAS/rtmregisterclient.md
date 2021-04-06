---
title: Rtmregisterclient-Funktion (RTM. h)
description: Die Funktion rtmregisterclient registriert einen Client als Handler für das angegebene Protokoll. Er richtet einen Weiterleitungs Änderungs Benachrichtigungs Mechanismus für den Client ein und legt Protokoll Optionen fest.
ms.assetid: 70426601-695d-47ed-b71a-1df3fb8ddf10
keywords:
- Rtmregisterclient-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmRegisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 564f47e68fd6cdce3d5437fe184bac1ed74d8322
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743112"
---
# <a name="rtmregisterclient-function"></a><span data-ttu-id="38f98-105">Rtmregisterclient-Funktion</span><span class="sxs-lookup"><span data-stu-id="38f98-105">RtmRegisterClient function</span></span>

<span data-ttu-id="38f98-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="38f98-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="38f98-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="38f98-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="38f98-108">Die Funktion **rtmregisterclient** registriert einen Client als Handler für das angegebene Protokoll.</span><span class="sxs-lookup"><span data-stu-id="38f98-108">The **RtmRegisterClient** function registers a client as a handler of the specified protocol.</span></span> <span data-ttu-id="38f98-109">Er richtet einen Weiterleitungs Änderungs Benachrichtigungs Mechanismus für den Client ein und legt Protokoll Optionen fest.</span><span class="sxs-lookup"><span data-stu-id="38f98-109">It establishes a route change notification mechanism for the client, and sets protocol options.</span></span>

## <a name="syntax"></a><span data-ttu-id="38f98-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="38f98-110">Syntax</span></span>


```C++
HANDLE RtmRegisterClient(
  _In_ DWORD  ProtocolFamily,
  _In_ DWORD  RoutingProtocol,
  _In_ HANDLE ChangeEvent,
  _In_ DWORD  Flags
);
```



## <a name="parameters"></a><span data-ttu-id="38f98-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="38f98-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38f98-112">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38f98-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f98-113">Gibt die Protokollfamilie des zu registrierenden Routing Protokolls an.</span><span class="sxs-lookup"><span data-stu-id="38f98-113">Specifies the protocol family of the routing protocol to register.</span></span>

</dd> <dt>

<span data-ttu-id="38f98-114">*Routingprotocol* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38f98-114">*RoutingProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f98-115">Gibt die Routing Protokoll-ID an, die mit der übereinstimmen, die bei der Registrierung beim routermanager verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="38f98-115">Specifies the routing protocol identifier, the same as that used when registering with the router manager.</span></span> <span data-ttu-id="38f98-116">Siehe [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span><span class="sxs-lookup"><span data-stu-id="38f98-116">See [**RegisterProtocol**](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol).</span></span>

</dd> <dt>

<span data-ttu-id="38f98-117">*ChangeEvent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="38f98-117">*ChangeEvent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f98-118">Gibt an, dass sich die beste Route zu einem Netzwerk in der Tabelle geändert hat.</span><span class="sxs-lookup"><span data-stu-id="38f98-118">Specifies that a best route to a network in the table has changed.</span></span> <span data-ttu-id="38f98-119">Der Routing Tabellen-Manager signalisiert dieses Ereignis nach einer Änderung an der optimalen Route zu einem beliebigen Netzwerk in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="38f98-119">The routing table manager signals this event after a change to the best route to any network in the table.</span></span> <span data-ttu-id="38f98-120">Weitere Informationen zur Weiterleitung von Änderungs Benachrichtigungen finden Sie unter [**rtmdequeueroutechangemess**](rtmdequeueroutechangemessage.md) .</span><span class="sxs-lookup"><span data-stu-id="38f98-120">See [**RtmDequeueRouteChangeMessage**](rtmdequeueroutechangemessage.md) for more information about route-change notification.</span></span>

<span data-ttu-id="38f98-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="38f98-121">This parameter is optional.</span></span> <span data-ttu-id="38f98-122">Wenn der Aufrufer **null** für diesen Parameter angibt, benachrichtigt der Routing Tabellen-Manager den Client über Änderungen am besten Routen Status.</span><span class="sxs-lookup"><span data-stu-id="38f98-122">If the caller specifies **NULL** for this parameter, the routing table manager does not notify the client of changes in best route status.</span></span>

</dd> <dt>

<span data-ttu-id="38f98-123">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="38f98-123">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38f98-124">Gibt verschiedene Optionen für die spezielle Behandlung des Routing Protokolls an.</span><span class="sxs-lookup"><span data-stu-id="38f98-124">Specifies miscellaneous options for special handling of the routing protocol.</span></span> <span data-ttu-id="38f98-125">Der folgende Wert wird derzeit unterstützt.</span><span class="sxs-lookup"><span data-stu-id="38f98-125">The following value is currently supported.</span></span>



| <span data-ttu-id="38f98-126">Flags</span><span class="sxs-lookup"><span data-stu-id="38f98-126">Flags</span></span>                                                                                                                                                                                               | <span data-ttu-id="38f98-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="38f98-127">Meaning</span></span>                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_PROTOCOL_SINGLE_ROUTE"></span><span id="rtm_protocol_single_route"></span><dl> <span data-ttu-id="38f98-128"><dt>**RTM- \_ Protokoll- \_ einzelne \_ Route**</dt></span><span class="sxs-lookup"><span data-stu-id="38f98-128"><dt>**RTM\_PROTOCOL\_SINGLE\_ROUTE**</dt></span></span> </dl> | <span data-ttu-id="38f98-129">Der Routing Tabellen-Manager behält nur eine Route pro Zielnetzwerk für das Routing Protokoll bei.</span><span class="sxs-lookup"><span data-stu-id="38f98-129">The routing table manager keeps only one route per destination network for the routing protocol.</span></span> <span data-ttu-id="38f98-130">Mit anderen Worten: der Routing Tabellen-Manager ersetzt Routen Einträge, die dieselben Zielnetzwerk Nummern aufweisen, anstatt neue hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="38f98-130">In other words, the routing table manager replaces route entries that have the same destination network numbers instead of adding new ones.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38f98-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="38f98-131">Return value</span></span>

<span data-ttu-id="38f98-132">Bei erfolgreicher Rückgabe ein **handle** -Wert, der den Client in nachfolgenden Aufrufen des Routing Tabellen-Managers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="38f98-132">On successful return, a **HANDLE** value that identifies the client in subsequent calls to the routing table manager.</span></span>

<span data-ttu-id="38f98-133">Ein **null** -handle gibt an, dass der Routing Tabellen-Manager den Client nicht registrieren konnte.</span><span class="sxs-lookup"><span data-stu-id="38f98-133">A **NULL** handle indicates that the routing table manager was unable to register the client.</span></span> <span data-ttu-id="38f98-134">Rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um den Grund für den Fehler zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="38f98-134">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain the reason for the failure.</span></span>



| <span data-ttu-id="38f98-135">Wert</span><span class="sxs-lookup"><span data-stu-id="38f98-135">Value</span></span>                                                                                                         | <span data-ttu-id="38f98-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="38f98-136">Description</span></span>                                                                                     |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="38f98-137"><dt>**der Fehler \_ Client ist \_ bereits \_ vorhanden.**</dt></span><span class="sxs-lookup"><span data-stu-id="38f98-137"><dt>**ERROR\_CLIENT\_ALREADY\_EXISTS**</dt></span></span> </dl> | <span data-ttu-id="38f98-138">Ein anderer Client hat sich bereits für die Verarbeitung des angegebenen Protokolls registriert.</span><span class="sxs-lookup"><span data-stu-id="38f98-138">Another client has already registered to handle the specified protocol.</span></span><br/>              |
| <dl> <span data-ttu-id="38f98-139"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="38f98-139"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>      | <span data-ttu-id="38f98-140">Die angegebene Protokollfamilie wird nicht unterstützt, oder der *Flags* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="38f98-140">The specified protocol family is not supported, or the *Flags* parameter is invalid.</span></span><br/> |
| <dl> <span data-ttu-id="38f98-141"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="38f98-141"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl>   | <span data-ttu-id="38f98-142">Nicht genügend Ressourcen, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="38f98-142">Insufficient resources to carry out the operation.</span></span><br/>                                   |
| <dl> <span data-ttu-id="38f98-143"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="38f98-143"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>     | <span data-ttu-id="38f98-144">Nicht genügend Arbeitsspeicher zum Zuordnen von Datenstrukturen für den Client.</span><span class="sxs-lookup"><span data-stu-id="38f98-144">Insufficient memory to allocate data structures for the client.</span></span><br/>                      |



 

## <a name="requirements"></a><span data-ttu-id="38f98-145">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="38f98-145">Requirements</span></span>



| <span data-ttu-id="38f98-146">Anforderung</span><span class="sxs-lookup"><span data-stu-id="38f98-146">Requirement</span></span> | <span data-ttu-id="38f98-147">Wert</span><span class="sxs-lookup"><span data-stu-id="38f98-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="38f98-148">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="38f98-148">Minimum supported client</span></span><br/> | <span data-ttu-id="38f98-149">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="38f98-149">None supported</span></span><br/>                                                          |
| <span data-ttu-id="38f98-150">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="38f98-150">Minimum supported server</span></span><br/> | <span data-ttu-id="38f98-151">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="38f98-151">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="38f98-152">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="38f98-152">End of server support</span></span><br/>    | <span data-ttu-id="38f98-153">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="38f98-153">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="38f98-154">Header</span><span class="sxs-lookup"><span data-stu-id="38f98-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="38f98-155"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="38f98-155"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="38f98-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="38f98-156">Library</span></span><br/>                  | <dl> <span data-ttu-id="38f98-157"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="38f98-157"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="38f98-158">DLL</span><span class="sxs-lookup"><span data-stu-id="38f98-158">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38f98-159"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38f98-159"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38f98-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="38f98-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38f98-161">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="38f98-161">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="38f98-162">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="38f98-162">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="38f98-163">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="38f98-163">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="38f98-164">**Register Protocol**</span><span class="sxs-lookup"><span data-stu-id="38f98-164">**RegisterProtocol**</span></span>](/windows/desktop/api/Routprot/nc-routprot-pregister_protocol)
</dt> <dt>

[<span data-ttu-id="38f98-165">RTMv1-Protokoll Familien Bezeichner</span><span class="sxs-lookup"><span data-stu-id="38f98-165">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> <dt>

[<span data-ttu-id="38f98-166">**Rtmde queueroutechangemess**</span><span class="sxs-lookup"><span data-stu-id="38f98-166">**RtmDequeueRouteChangeMessage**</span></span>](rtmdequeueroutechangemessage.md)
</dt> <dt>

[<span data-ttu-id="38f98-167">**Rtmderegisterclient**</span><span class="sxs-lookup"><span data-stu-id="38f98-167">**RtmDeregisterClient**</span></span>](rtmderegisterclient.md)
</dt> </dl>

 

