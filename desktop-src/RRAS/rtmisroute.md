---
title: Rtmisroute-Funktion (RTM. h)
description: Die rtmisroute-Funktion bestimmt, ob eine oder mehrere Routen zu einem angegebenen Zielnetzwerk vorhanden sind. Wenn dies der Fall ist, gibt die Funktion Informationen für die beste Route zu diesem Netzwerk zurück.
ms.assetid: f9939790-d0a6-487e-9674-a01d436dc962
keywords:
- Rtmisroute-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmIsRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64621732f2f7a35223421e5f0fc86a309d332c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478222"
---
# <a name="rtmisroute-function"></a><span data-ttu-id="a91ea-105">Rtmisroute-Funktion</span><span class="sxs-lookup"><span data-stu-id="a91ea-105">RtmIsRoute function</span></span>

<span data-ttu-id="a91ea-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a91ea-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="a91ea-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="a91ea-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="a91ea-108">Die **rtmisroute** -Funktion bestimmt, ob eine oder mehrere Routen zu einem angegebenen Zielnetzwerk vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="a91ea-108">The **RtmIsRoute** function determines if one or more routes to a specified destination network exist.</span></span> <span data-ttu-id="a91ea-109">Wenn dies der Fall ist, gibt die Funktion Informationen für die beste Route zu diesem Netzwerk zurück.</span><span class="sxs-lookup"><span data-stu-id="a91ea-109">If so, the function returns information for the best route to that network.</span></span>

## <a name="syntax"></a><span data-ttu-id="a91ea-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a91ea-110">Syntax</span></span>


```C++
BOOL RtmIsRoute(
  _In_  DWORD ProtocolFamily,
  _In_  PVOID Network,
  _Out_ PVOID BestRoute
);
```



## <a name="parameters"></a><span data-ttu-id="a91ea-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a91ea-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a91ea-112">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a91ea-112">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a91ea-113">Gibt den Typ der Datenstruktur an, auf die vom *Netzwerk* Parameter verwiesen wird, z. b. [**IP- \_ Netzwerk**](ip-network.md), [**IPX- \_ Netzwerk**](ipx-network.md).</span><span class="sxs-lookup"><span data-stu-id="a91ea-113">Specifies the type of data structure pointed to by the *Network* parameter, for example, [**IP\_NETWORK**](ip-network.md), [**IPX\_NETWORK**](ipx-network.md).</span></span>

</dd> <dt>

<span data-ttu-id="a91ea-114">*Netzwerk* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a91ea-114">*Network* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a91ea-115">Ein Zeiger auf eine-Struktur, die die Protokoll Familien spezifischen Netzwerk Nummern Daten angibt.</span><span class="sxs-lookup"><span data-stu-id="a91ea-115">Pointer to a structure that specifies protocol-family-specific network number data.</span></span> <span data-ttu-id="a91ea-116">Diese Daten identifizieren das Netzwerk, für das der Aufrufer Routeninformationen sucht.</span><span class="sxs-lookup"><span data-stu-id="a91ea-116">This data identifies the network for which the caller seeks route information.</span></span>

</dd> <dt>

<span data-ttu-id="a91ea-117">*Bestroute* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a91ea-117">*BestRoute* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a91ea-118">Ein Zeiger auf eine Protokoll familienspezifische Struktur, die die aktuellen besten Routeninformationen empfängt, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a91ea-118">Pointer to a protocol-family-specific structure that receives the current best route information, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a91ea-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a91ea-119">Return value</span></span>

<span data-ttu-id="a91ea-120">Der Rückgabewert ist einer der folgenden Codes.</span><span class="sxs-lookup"><span data-stu-id="a91ea-120">The return value is one of the following codes.</span></span>



| <span data-ttu-id="a91ea-121">Wert</span><span class="sxs-lookup"><span data-stu-id="a91ea-121">Value</span></span>                                                                                                       | <span data-ttu-id="a91ea-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a91ea-122">Description</span></span>                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a91ea-123"><dt>**Fall**</dt></span><span class="sxs-lookup"><span data-stu-id="a91ea-123"><dt>**TRUE**</dt></span></span> </dl>                         | <span data-ttu-id="a91ea-124">Es ist mindestens eine Route zum angegebenen Netzwerk vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a91ea-124">At least one route to the specified network exists.</span></span> <span data-ttu-id="a91ea-125">Die beste Route wird in der Struktur zurückgegeben, auf die der *bestroute* -Parameter verweist.</span><span class="sxs-lookup"><span data-stu-id="a91ea-125">The best route is returned in the structure pointed to by the *BestRoute* parameter.</span></span><br/>      |
| <dl> <span data-ttu-id="a91ea-126"><dt>**Alarm**</dt></span><span class="sxs-lookup"><span data-stu-id="a91ea-126"><dt>**FALSE**</dt></span></span> </dl>                        | <span data-ttu-id="a91ea-127">Es ist keine Route zum angegebenen Netzwerk vorhanden, oder der Vorgang ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="a91ea-127">There is no route to the specified network, or the operation failed.</span></span> <span data-ttu-id="a91ea-128">Rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um weitere Informationen zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="a91ea-128">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information:</span></span><br/> |
| <dl> <span data-ttu-id="a91ea-129"><dt>**kein \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="a91ea-129"><dt>**NO\_ERROR**</dt></span></span> </dl>                    | <span data-ttu-id="a91ea-130">Der Vorgang war erfolgreich, aber es ist keine Route zum angegebenen Netzwerk vorhanden.</span><span class="sxs-lookup"><span data-stu-id="a91ea-130">The operation succeeded, but there is no route to the specified network.</span></span><br/>                                                                      |
| <dl> <span data-ttu-id="a91ea-131"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="a91ea-131"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>    | <span data-ttu-id="a91ea-132">Der Wert des *ProtocolFamily* -Parameters entspricht keiner installierten Protokollfamilie.</span><span class="sxs-lookup"><span data-stu-id="a91ea-132">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/>                                             |
| <dl> <span data-ttu-id="a91ea-133"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="a91ea-133"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="a91ea-134">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a91ea-134">There are insufficient resources to carry out the operation.</span></span><br/>                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="a91ea-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a91ea-135">Requirements</span></span>



| <span data-ttu-id="a91ea-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a91ea-136">Requirement</span></span> | <span data-ttu-id="a91ea-137">Wert</span><span class="sxs-lookup"><span data-stu-id="a91ea-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a91ea-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a91ea-138">Minimum supported client</span></span><br/> | <span data-ttu-id="a91ea-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a91ea-139">None supported</span></span><br/>                                                          |
| <span data-ttu-id="a91ea-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a91ea-140">Minimum supported server</span></span><br/> | <span data-ttu-id="a91ea-141">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a91ea-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a91ea-142">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="a91ea-142">End of server support</span></span><br/>    | <span data-ttu-id="a91ea-143">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a91ea-143">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="a91ea-144">Header</span><span class="sxs-lookup"><span data-stu-id="a91ea-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="a91ea-145"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="a91ea-145"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="a91ea-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a91ea-146">Library</span></span><br/>                  | <dl> <span data-ttu-id="a91ea-147"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a91ea-147"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="a91ea-148">DLL</span><span class="sxs-lookup"><span data-stu-id="a91ea-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a91ea-149"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a91ea-149"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a91ea-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a91ea-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a91ea-151">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="a91ea-151">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="a91ea-152">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="a91ea-152">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="a91ea-153">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="a91ea-153">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="a91ea-154">**IP- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="a91ea-154">**IP\_NETWORK**</span></span>](ip-network.md)
</dt> <dt>

[<span data-ttu-id="a91ea-155">**IPX- \_ Netzwerk**</span><span class="sxs-lookup"><span data-stu-id="a91ea-155">**IPX\_NETWORK**</span></span>](ipx-network.md)
</dt> <dt>

[<span data-ttu-id="a91ea-156">RTMv1-Protokoll Familien Bezeichner</span><span class="sxs-lookup"><span data-stu-id="a91ea-156">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

