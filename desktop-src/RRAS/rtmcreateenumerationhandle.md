---
title: Rtmkreateenumerationhandle-Funktion (RTM. h)
description: Die rtmkreateenumerationhandle-Funktion gibt ein Handle zurück, das mit rtmenumerategetnextroute verwendet werden kann, um alle Routen oder eine Teilmenge der Routen zu durchsuchen, die dem Routing Tabellen-Manager bekannt sind.
ms.assetid: 73e3ac7d-498a-4d89-a6b5-17aaf4b17ec2
keywords:
- Rtmkreateenumerationhandle-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmCreateEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14086639db299038139e0e7d02eb12bb892042bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103115"
---
# <a name="rtmcreateenumerationhandle-function"></a><span data-ttu-id="8f2ed-104">Rtmkreateenumerationhandle-Funktion</span><span class="sxs-lookup"><span data-stu-id="8f2ed-104">RtmCreateEnumerationHandle function</span></span>

<span data-ttu-id="8f2ed-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="8f2ed-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="8f2ed-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="8f2ed-107">Die **rtmkreateenumerationhandle** -Funktion gibt ein Handle zurück, das mit [**rtmenumerategetnextroute**](rtmenumerategetnextroute.md) verwendet werden kann, um alle Routen oder eine Teilmenge der Routen zu durchsuchen, die dem Routing Tabellen-Manager bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-107">The **RtmCreateEnumerationHandle** function returns a handle to use with [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md) to scan through all routes, or a subset of routes, known to the routing table manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f2ed-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f2ed-108">Syntax</span></span>


```C++
HANDLE RtmCreateEnumerationHandle(
  _In_ DWORD ProtocolFamily,
  _In_ DWORD EnumerationFlags,
  _In_ PVOID CriteriaRoute
);
```



## <a name="parameters"></a><span data-ttu-id="8f2ed-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f2ed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f2ed-110">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f2ed-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f2ed-111">Gibt die Protokollfamilie der aufzuzählenden Routen an.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-111">Specifies the protocol family of the routes to enumerate.</span></span>

</dd> <dt>

<span data-ttu-id="8f2ed-112">*Enumerationflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f2ed-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f2ed-113">Gibt an, welche Routen aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="8f2ed-114">Mit diesem Parameter wird der von der enumerationsapi zurückgegebene Satz von Routen auf eine Teilmenge beschränkt, die durch die folgenden Flags definiert ist, sowie auf die Werte in den entsprechenden Membern der Struktur, auf die durch den *Kriterium* -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-114">This parameter limits the set of routes returned by the enumeration API to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="8f2ed-115">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-115">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8f2ed-116">Enumerationflags</span><span class="sxs-lookup"><span data-stu-id="8f2ed-116">EnumerationFlags</span></span>                                                                                                                                                                              | <span data-ttu-id="8f2ed-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8f2ed-117">Meaning</span></span>                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RTM_ONLY_THIS_NETWORK"></span><span id="rtm_only_this_network"></span><dl> <span data-ttu-id="8f2ed-118"><dt>**\_nur \_ dieses \_ Netzwerk RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-118"><dt>**RTM\_ONLY\_THIS\_NETWORK**</dt></span></span> </dl>       | <span data-ttu-id="8f2ed-119">Listet nur die Routen auf, die die gleiche Netzwerk Nummer wie das RR- \_ netzwerkmember der Struktur aufweisen, auf die von Criteria verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-119">Enumerate only those routes that have the same network number as the RR\_Network member of the structure pointed to by CriteriaRoute.</span></span><br/>                        |
| <span id="RTM_ONLY_THIS_INTERFACE"></span><span id="rtm_only_this_interface"></span><dl> <span data-ttu-id="8f2ed-120"><dt>**\_nur \_ diese \_ Schnittstelle für RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-120"><dt>**RTM\_ONLY\_THIS\_INTERFACE**</dt></span></span> </dl> | <span data-ttu-id="8f2ed-121">Listet nur die Routen auf, die durch die Schnittstelle abgerufen wurden, die durch das RR- \_ interfakeid-Feld der Struktur abgerufen wurde, auf die von Criteria verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-121">Enumerate only those routes that were obtained through the interface specified by the RR\_InterfaceID field of the structure pointed to by CriteriaRoute.</span></span><br/>    |
| <span id="RTM_ONLY_THIS_PROTOCOL"></span><span id="rtm_only_this_protocol"></span><dl> <span data-ttu-id="8f2ed-122"><dt>**\_nur \_ dieses \_ Protokoll für RTM**</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-122"><dt>**RTM\_ONLY\_THIS\_PROTOCOL**</dt></span></span> </dl>    | <span data-ttu-id="8f2ed-123">Enumerieren Sie nur die Routen, die durch das Routing Protokoll hinzugefügt wurden, das durch das \_ Feld RR routingprotocol der Struktur, auf die durch Kriterienwerte verwiesen wird, angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-123">Enumerate only those routes that were added by the routing protocol specified by the RR\_RoutingProtocol field of the structure pointed to by CriteriaRoute.</span></span><br/> |
| <span id="RTM_ONLY_BEST_ROUTES"></span><span id="rtm_only_best_routes"></span><dl> <span data-ttu-id="8f2ed-124"><dt>**RTM hat \_ nur die \_ besten \_ Routen**</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-124"><dt>**RTM\_ONLY\_BEST\_ROUTES**</dt></span></span> </dl>          | <span data-ttu-id="8f2ed-125">Listet nur die optimalen Routen zu den einzelnen Netzwerken in der Gruppe auf.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-125">Enumerate only the best routes to each of the networks in the set.</span></span><br/>                                                                                           |



 

</dd> <dt>

<span data-ttu-id="8f2ed-126">*Kriterien* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8f2ed-126">*CriteriaRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f2ed-127">Zeiger auf eine Protokoll familienspezifische Routen Struktur ([**RTM \_ -IP- \_ Route**](rtm-ip-route.md) oder [**RTM \_ IPX- \_ Route**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="8f2ed-127">Pointer to a protocol-family-specific route structure ([**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="8f2ed-128">Die Element Werte in dieser Struktur entsprechen den Flags, die durch den *enumerationflags* -Parameter angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-128">The member values in this structure correspond to the flags specified by the *EnumerationFlags* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f2ed-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8f2ed-129">Return value</span></span>

<span data-ttu-id="8f2ed-130">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert ein **handle** , das bei nachfolgenden enumerationsaufrufen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-130">If the function succeeds, the return value is a **HANDLE** to use with subsequent enumeration calls.</span></span>

<span data-ttu-id="8f2ed-131">Wenn die Funktion fehlschlägt oder keine Routen mit den angegebenen Kriterien vorhanden sind, ist der Rückgabewert **null**.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-131">If the function fails, or no routes exist with the specified criteria, the return value is **NULL**.</span></span> <span data-ttu-id="8f2ed-132">Rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-132">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="8f2ed-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8f2ed-133">Value</span></span>                                                                                                       | <span data-ttu-id="8f2ed-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8f2ed-134">Description</span></span>                                                                                                                  |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8f2ed-135"><dt>**Fehler \_ ohne \_ Routen**</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-135"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="8f2ed-136">Es sind keine Routen vorhanden, die die angegebenen Kriterien aufweisen.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-136">There are no routes that have the specified criteria.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="8f2ed-137"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-137"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="8f2ed-138">Mindestens ein Eingabeparameter ist ungültig (z. b. unbekannte Protokollfamilie, ungültige Enumerationsflags).</span><span class="sxs-lookup"><span data-stu-id="8f2ed-138">One or more of the input parameters is invalid (for example, unknown protocol family, invalid enumeration flags).</span></span><br/> |
| <dl> <span data-ttu-id="8f2ed-139"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-139"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="8f2ed-140">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-140">There are insufficient resources to carry out the operation.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="8f2ed-141"><dt>**Fehler \_ nicht \_ genügend Arbeits \_ Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-141"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl>   | <span data-ttu-id="8f2ed-142">Es ist nicht genügend Arbeitsspeicher vorhanden, um das Handle zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="8f2ed-142">There is insufficient memory to allocate the handle.</span></span><br/>                                                              |



 

## <a name="requirements"></a><span data-ttu-id="8f2ed-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8f2ed-143">Requirements</span></span>



| <span data-ttu-id="8f2ed-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f2ed-144">Requirement</span></span> | <span data-ttu-id="8f2ed-145">Wert</span><span class="sxs-lookup"><span data-stu-id="8f2ed-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8f2ed-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8f2ed-146">Minimum supported client</span></span><br/> | <span data-ttu-id="8f2ed-147">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8f2ed-147">None supported</span></span><br/>                                                          |
| <span data-ttu-id="8f2ed-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8f2ed-148">Minimum supported server</span></span><br/> | <span data-ttu-id="8f2ed-149">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8f2ed-149">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8f2ed-150">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="8f2ed-150">End of server support</span></span><br/>    | <span data-ttu-id="8f2ed-151">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="8f2ed-151">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="8f2ed-152">Header</span><span class="sxs-lookup"><span data-stu-id="8f2ed-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="8f2ed-153"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-153"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="8f2ed-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8f2ed-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="8f2ed-155"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-155"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="8f2ed-156">DLL</span><span class="sxs-lookup"><span data-stu-id="8f2ed-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8f2ed-157"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8f2ed-157"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8f2ed-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f2ed-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f2ed-159">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="8f2ed-159">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="8f2ed-160">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="8f2ed-160">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="8f2ed-161">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="8f2ed-161">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="8f2ed-162">**RTM \_ -IP- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="8f2ed-162">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="8f2ed-163">**RTM- \_ IPX- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="8f2ed-163">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="8f2ed-164">**Rtmcloseenumerationhandle**</span><span class="sxs-lookup"><span data-stu-id="8f2ed-164">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="8f2ed-165">**Rtmenumschlag-ategetnextroute**</span><span class="sxs-lookup"><span data-stu-id="8f2ed-165">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

