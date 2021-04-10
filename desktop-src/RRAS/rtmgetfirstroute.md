---
title: Rtmgetfirstroute-Funktion (RTM. h)
description: Die rtmgetfirstroute-Funktion gibt die erste Route von der angegebenen Teilmenge der Routen in der Tabelle zurück.
ms.assetid: f2071b50-4b06-432f-8dbf-45696f8a5cb1
keywords:
- Rtmgetfirstroute-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmGetFirstRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e98a5deb0f925fbf3b27c21302060bbe4869b4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104385"
---
# <a name="rtmgetfirstroute-function"></a><span data-ttu-id="e3f2d-104">Rtmgetfirstroute-Funktion</span><span class="sxs-lookup"><span data-stu-id="e3f2d-104">RtmGetFirstRoute function</span></span>

<span data-ttu-id="e3f2d-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="e3f2d-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="e3f2d-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="e3f2d-107">Die **rtmgetfirstroute** -Funktion gibt die erste Route von der angegebenen Teilmenge der Routen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-107">The **RtmGetFirstRoute** function returns the first route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3f2d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3f2d-108">Syntax</span></span>


```C++
DWORD RtmGetFirstRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="e3f2d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3f2d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3f2d-110">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3f2d-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f2d-111">Gibt die Protokollfamilie der abzurufenden Routen an, z. b. IP oder IPX.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="e3f2d-112">*Enumerationflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e3f2d-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f2d-113">Gibt an, dass den Satz gelöschter Routen auf eine Teilmenge beschränkt, die durch diese Flags definiert ist, sowie die Werte in den entsprechenden Membern der Struktur, auf die durch den *Kriterienparameter* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-113">Specifies the limits the set of deleted routes to a subset defined by these flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="e3f2d-114">Die Flags sind identisch mit denen, die in [**rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-114">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="e3f2d-115">*Route* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e3f2d-115">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e3f2d-116">Bei der Eingabe verweist die *Route* auf eine Protokoll familienspezifische Struktur ( [**RTM- \_ IP- \_ Route**](rtm-ip-route.md) oder [**RTM \_ IPX- \_ Route**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="e3f2d-116">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="e3f2d-117">Die Aufruf Funktion stellt Element Werte für diese-Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-117">The calling function provides member values for this structure.</span></span> <span data-ttu-id="e3f2d-118">Diese Werte geben in Verbindung mit dem *enumerationflags* -Parameter den Satz an, aus dem Routen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-118">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="e3f2d-119">Ausgabe, *Route* verweist auf die erste Route, die mit den angegebenen Kriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-119">Out output, *Route* points to the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e3f2d-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3f2d-120">Return value</span></span>

<span data-ttu-id="e3f2d-121">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-121">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="e3f2d-122">Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-122">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="e3f2d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="e3f2d-123">Value</span></span>                                                                                                       | <span data-ttu-id="e3f2d-124">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3f2d-124">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3f2d-125"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="e3f2d-125"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="e3f2d-126">Einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-126">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="e3f2d-127"><dt>**Fehler \_ ohne \_ Routen**</dt></span><span class="sxs-lookup"><span data-stu-id="e3f2d-127"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="e3f2d-128">Es sind keine Routen vorhanden, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-128">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="e3f2d-129"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="e3f2d-129"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="e3f2d-130">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e3f2d-130">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3f2d-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3f2d-131">Remarks</span></span>

<span data-ttu-id="e3f2d-132">Die Routen werden in der folgenden Reihenfolge zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="e3f2d-132">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="e3f2d-133">Netzwerk Nummer</span><span class="sxs-lookup"><span data-stu-id="e3f2d-133">Network number</span></span>
2.  <span data-ttu-id="e3f2d-134">Routing Protokoll</span><span class="sxs-lookup"><span data-stu-id="e3f2d-134">Routing protocol</span></span>
3.  <span data-ttu-id="e3f2d-135">Schnittstellen-ID</span><span class="sxs-lookup"><span data-stu-id="e3f2d-135">Interface identifier</span></span>
4.  <span data-ttu-id="e3f2d-136">Adresse des nächsten Hops</span><span class="sxs-lookup"><span data-stu-id="e3f2d-136">Next-hop address</span></span>

<span data-ttu-id="e3f2d-137">Diese Funktion ist weniger effizient als die entsprechende [**enumerationshandle-Funktion rtmenumerategetnextroute**](rtmenumerategetnextroute.md).</span><span class="sxs-lookup"><span data-stu-id="e3f2d-137">This function is less efficient than the corresponding enumeration handle function, [**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e3f2d-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3f2d-138">Requirements</span></span>



| <span data-ttu-id="e3f2d-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3f2d-139">Requirement</span></span> | <span data-ttu-id="e3f2d-140">Wert</span><span class="sxs-lookup"><span data-stu-id="e3f2d-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e3f2d-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3f2d-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e3f2d-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e3f2d-142">None supported</span></span><br/>                                                          |
| <span data-ttu-id="e3f2d-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3f2d-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e3f2d-144">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3f2d-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e3f2d-145">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="e3f2d-145">End of server support</span></span><br/>    | <span data-ttu-id="e3f2d-146">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e3f2d-146">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="e3f2d-147">Header</span><span class="sxs-lookup"><span data-stu-id="e3f2d-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3f2d-148"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3f2d-148"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3f2d-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e3f2d-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="e3f2d-150"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e3f2d-150"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="e3f2d-151">DLL</span><span class="sxs-lookup"><span data-stu-id="e3f2d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3f2d-152"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3f2d-152"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3f2d-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3f2d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3f2d-154">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="e3f2d-154">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="e3f2d-155">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="e3f2d-155">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="e3f2d-156">**Rtmcloseenumerationhandle**</span><span class="sxs-lookup"><span data-stu-id="e3f2d-156">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="e3f2d-157">**Rtmkreateenumerationhandle**</span><span class="sxs-lookup"><span data-stu-id="e3f2d-157">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="e3f2d-158">**Rtmenumschlag-ategetnextroute**</span><span class="sxs-lookup"><span data-stu-id="e3f2d-158">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="e3f2d-159">**Rtmgetnextroute**</span><span class="sxs-lookup"><span data-stu-id="e3f2d-159">**RtmGetNextRoute**</span></span>](rtmgetnextroute.md)
</dt> </dl>

 

 





