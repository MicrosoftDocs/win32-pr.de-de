---
title: Rtmgetnetworkcount-Funktion (RTM. h)
description: Die rtmgetnetworkcount-Funktion Ruft die Anzahl von Netzwerken ab, an die der Routing Tabellen-Manager Routen hat.
ms.assetid: d0c04b8d-a6c4-44bf-a3f2-de822d635131
keywords:
- Rtmgetnetworkcount-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmGetNetworkCount
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eab4babd1e9d98071b2fbe6ab30c9b92d4a23f0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741409"
---
# <a name="rtmgetnetworkcount-function"></a><span data-ttu-id="b86f2-104">Rtmgetnetworkcount-Funktion</span><span class="sxs-lookup"><span data-stu-id="b86f2-104">RtmGetNetworkCount function</span></span>

<span data-ttu-id="b86f2-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b86f2-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="b86f2-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="b86f2-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="b86f2-107">Die **rtmgetnetworkcount** -Funktion Ruft die Anzahl von Netzwerken ab, an die der Routing Tabellen-Manager Routen hat.</span><span class="sxs-lookup"><span data-stu-id="b86f2-107">The **RtmGetNetworkCount** function retrieves the number of networks to which the routing table manager has routes.</span></span>

## <a name="syntax"></a><span data-ttu-id="b86f2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b86f2-108">Syntax</span></span>


```C++
ULONG RtmGetNetworkCount(
  _In_ DWORD ProtocolFamily
);
```



## <a name="parameters"></a><span data-ttu-id="b86f2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b86f2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b86f2-110">*ProtocolFamily* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b86f2-110">*ProtocolFamily* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b86f2-111">Gibt an, für welchen Typ von Netzwerk Routeninformationen abgerufen werden sollen, z. b. IP oder IPX.</span><span class="sxs-lookup"><span data-stu-id="b86f2-111">Specifies for which type of network to obtain route information, for example, IP or IPX.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b86f2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b86f2-112">Return value</span></span>

<span data-ttu-id="b86f2-113">Wenn die Funktion erfolgreich ausgeführt wird, entspricht der Rückgabewert der Netzwerk Anzahl, der Anzahl von Netzwerken, die den Routing Protokollen der angegebenen Protokollfamilie bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="b86f2-113">If the function succeeds, the return value is the network count, the number of networks known to the routing protocols of the specified protocol family.</span></span>

<span data-ttu-id="b86f2-114">Wenn der Rückgabewert 0 (null) ist, sind entweder keine Routen verfügbar, oder der Vorgang ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="b86f2-114">If the return value is zero, either no routes are available, or the operation failed.</span></span> <span data-ttu-id="b86f2-115">Rufen Sie [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um weitere Informationen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="b86f2-115">Call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) to obtain more information.</span></span>



| <span data-ttu-id="b86f2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b86f2-116">Value</span></span>                                                                                                    | <span data-ttu-id="b86f2-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b86f2-117">Description</span></span>                                                                                                  |
|----------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b86f2-118"><dt>**kein \_ Fehler**</dt></span><span class="sxs-lookup"><span data-stu-id="b86f2-118"><dt>**NO\_ERROR**</dt></span></span> </dl>                 | <span data-ttu-id="b86f2-119">Der Vorgang war erfolgreich, aber es sind keine Routen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b86f2-119">The operation succeeded, but no routes are available.</span></span><br/>                                             |
| <dl> <span data-ttu-id="b86f2-120"><dt>**Fehler bei \_ ungültigem \_ Parameter**</dt></span><span class="sxs-lookup"><span data-stu-id="b86f2-120"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl> | <span data-ttu-id="b86f2-121">Der Wert des *ProtocolFamily* -Parameters entspricht keiner installierten Protokollfamilie.</span><span class="sxs-lookup"><span data-stu-id="b86f2-121">The value of the *ProtocolFamily* parameter does not correspond to any installed protocol family.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b86f2-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b86f2-122">Requirements</span></span>



| <span data-ttu-id="b86f2-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b86f2-123">Requirement</span></span> | <span data-ttu-id="b86f2-124">Wert</span><span class="sxs-lookup"><span data-stu-id="b86f2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b86f2-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b86f2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="b86f2-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b86f2-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="b86f2-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b86f2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="b86f2-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b86f2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b86f2-129">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="b86f2-129">End of server support</span></span><br/>    | <span data-ttu-id="b86f2-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b86f2-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="b86f2-131">Header</span><span class="sxs-lookup"><span data-stu-id="b86f2-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b86f2-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="b86f2-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="b86f2-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b86f2-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="b86f2-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b86f2-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="b86f2-135">DLL</span><span class="sxs-lookup"><span data-stu-id="b86f2-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b86f2-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b86f2-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b86f2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b86f2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b86f2-138">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="b86f2-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="b86f2-139">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="b86f2-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="b86f2-140">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="b86f2-140">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="b86f2-141">RTMv1-Protokoll Familien Bezeichner</span><span class="sxs-lookup"><span data-stu-id="b86f2-141">RTMv1 Protocol Family Identifiers</span></span>](routing-table-manager-version-1-protocol-family-identifiers.md)
</dt> </dl>

 

