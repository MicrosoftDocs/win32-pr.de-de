---
title: Rtmgetnextroute-Funktion (RTM. h)
description: Die rtmgetnextroute-Funktion gibt die nächste Route von der angegebenen Teilmenge der Routen in der Tabelle zurück.
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- Rtmgetnextroute-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518089"
---
# <a name="rtmgetnextroute-function"></a><span data-ttu-id="b86a8-104">Rtmgetnextroute-Funktion</span><span class="sxs-lookup"><span data-stu-id="b86a8-104">RtmGetNextRoute function</span></span>

<span data-ttu-id="b86a8-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b86a8-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="b86a8-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="b86a8-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="b86a8-107">Die **rtmgetnextroute** -Funktion gibt die nächste Route von der angegebenen Teilmenge der Routen in der Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="b86a8-107">The **RtmGetNextRoute** function returns the next route from the specified subset of routes in the table.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86a8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b86a8-108">Syntax</span></span>


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="b86a8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b86a8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86a8-110">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b86a8-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86a8-111">Gibt die Protokollfamilie der abzurufenden Routen an, z. b. IP oder IPX.</span><span class="sxs-lookup"><span data-stu-id="b86a8-111">Specifies the protocol family of routes to retrieve, for example, IP or IPX.</span></span>

</dd> <dt>

<span data-ttu-id="b86a8-112">*Enumerationflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b86a8-112">*EnumerationFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86a8-113">Gibt an, welche Routen aufgelistet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b86a8-113">Specifies which routes should be enumerated.</span></span> <span data-ttu-id="b86a8-114">Mit diesem Parameter wird der Satz gelöschter Routen auf eine Teilmenge beschränkt, die durch die folgenden Flags definiert ist, sowie auf die Werte in den entsprechenden Membern der Struktur, auf die durch den *Kriterienparameter* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b86a8-114">This parameter limits the set of deleted routes to a subset defined by the following flags and the values in the corresponding members of the structure pointed to by the *CriteriaRoute* parameter.</span></span> <span data-ttu-id="b86a8-115">Die Flags sind identisch mit denen, die in [**rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md)verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b86a8-115">The flags are the same as those used in [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="b86a8-116">*Route* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="b86a8-116">*Route* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b86a8-117">Bei der Eingabe verweist die *Route* auf eine Protokoll familienspezifische Struktur ( [**RTM- \_ IP- \_ Route**](rtm-ip-route.md) oder [**RTM \_ IPX- \_ Route**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="b86a8-117">On input, *Route* points to a protocol-family-specific structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span>

<span data-ttu-id="b86a8-118">Die Aufruf Funktion stellt Element Werte für diese-Struktur bereit.</span><span class="sxs-lookup"><span data-stu-id="b86a8-118">The calling function provides member values for this structure.</span></span> <span data-ttu-id="b86a8-119">Diese Werte geben in Verbindung mit dem *enumerationflags* -Parameter den Satz an, aus dem Routen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b86a8-119">These values, in conjunction with the *EnumerationFlags* parameter, specify the set from which to return routes.</span></span>

<span data-ttu-id="b86a8-120">Bei der Ausgabe verweist die *Route* auf eine Struktur, die die erste Route empfängt, die mit den angegebenen Kriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="b86a8-120">On output, *Route* points to a structure that receives the first route that matched the specified criteria.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86a8-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b86a8-121">Return value</span></span>

<span data-ttu-id="b86a8-122">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert **kein \_ Fehler**.</span><span class="sxs-lookup"><span data-stu-id="b86a8-122">If the function succeeds, the return value is **NO\_ERROR**.</span></span>

<span data-ttu-id="b86a8-123">Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="b86a8-123">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="b86a8-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b86a8-124">Value</span></span>                                                                                                       | <span data-ttu-id="b86a8-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b86a8-125">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b86a8-126"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="b86a8-126"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="b86a8-127">Einer der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b86a8-127">One of the parameters is invalid.</span></span><br/>                            |
| <dl> <span data-ttu-id="b86a8-128"><dt>**Fehler \_ ohne \_ Routen**</dt></span><span class="sxs-lookup"><span data-stu-id="b86a8-128"><dt>**ERROR\_NO\_ROUTES**</dt></span></span> </dl>            | <span data-ttu-id="b86a8-129">Es sind keine Routen vorhanden, die den angegebenen Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b86a8-129">There are no routes that match the specified criteria.</span></span><br/>       |
| <dl> <span data-ttu-id="b86a8-130"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="b86a8-130"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="b86a8-131">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="b86a8-131">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b86a8-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b86a8-132">Remarks</span></span>

<span data-ttu-id="b86a8-133">Die Routen werden in der folgenden Reihenfolge zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="b86a8-133">The routes are returned in the following order:</span></span>

1.  <span data-ttu-id="b86a8-134">Netzwerk Nummer</span><span class="sxs-lookup"><span data-stu-id="b86a8-134">Network number</span></span>
2.  <span data-ttu-id="b86a8-135">Routing Protokoll</span><span class="sxs-lookup"><span data-stu-id="b86a8-135">Routing protocol</span></span>
3.  <span data-ttu-id="b86a8-136">Schnittstellen-ID</span><span class="sxs-lookup"><span data-stu-id="b86a8-136">Interface identifier</span></span>
4.  <span data-ttu-id="b86a8-137">Adresse des nächsten Hops</span><span class="sxs-lookup"><span data-stu-id="b86a8-137">Next-hop address</span></span>

<span data-ttu-id="b86a8-138">Diese Funktion ist weniger effizient als die entsprechenden Funktionen des enumerationshandles.</span><span class="sxs-lookup"><span data-stu-id="b86a8-138">This function is less efficient than the corresponding enumeration handle functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="b86a8-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b86a8-139">Requirements</span></span>



| <span data-ttu-id="b86a8-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b86a8-140">Requirement</span></span> | <span data-ttu-id="b86a8-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b86a8-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b86a8-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b86a8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b86a8-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b86a8-143">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b86a8-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b86a8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b86a8-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b86a8-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b86a8-146">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b86a8-146">End of server support</span></span><br/>    | <span data-ttu-id="b86a8-147">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b86a8-147">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="b86a8-148">Header</span><span class="sxs-lookup"><span data-stu-id="b86a8-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="b86a8-149"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b86a8-149"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="b86a8-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b86a8-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="b86a8-151"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b86a8-151"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="b86a8-152">DLL</span><span class="sxs-lookup"><span data-stu-id="b86a8-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b86a8-153"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b86a8-153"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b86a8-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b86a8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86a8-155">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="b86a8-155">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="b86a8-156">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="b86a8-156">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="b86a8-157">**Rtmcloseenumerationhandle**</span><span class="sxs-lookup"><span data-stu-id="b86a8-157">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="b86a8-158">**Rtmkreateenumerationhandle**</span><span class="sxs-lookup"><span data-stu-id="b86a8-158">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="b86a8-159">**Rtmenumschlag-ategetnextroute**</span><span class="sxs-lookup"><span data-stu-id="b86a8-159">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> <dt>

[<span data-ttu-id="b86a8-160">**Rtmgetfirstroute**</span><span class="sxs-lookup"><span data-stu-id="b86a8-160">**RtmGetFirstRoute**</span></span>](rtmgetfirstroute.md)
</dt> </dl>

 

 





