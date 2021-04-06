---
title: Rtmgetrouteage-Funktion (RTM. h)
description: Die Funktion rtmgetrouteage gibt das Alter einer Route zurück. Das Alter ist die Zeit (in Sekunden), seit der es erstellt oder zuletzt aktualisiert wurde.
ms.assetid: 93052412-227f-4c9e-978b-3ec4bde4a256
keywords:
- Rtmgetrouteage-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmGetRouteAge
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a484bb5684fde974ce5fa704c0d0cca38c320851
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742184"
---
# <a name="rtmgetrouteage-function"></a><span data-ttu-id="e7903-105">Rtmgetrouteage-Funktion</span><span class="sxs-lookup"><span data-stu-id="e7903-105">RtmGetRouteAge function</span></span>

<span data-ttu-id="e7903-106">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e7903-106">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="e7903-107">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="e7903-107">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="e7903-108">Die Funktion **rtmgetrouteage** gibt das Alter einer Route zurück.</span><span class="sxs-lookup"><span data-stu-id="e7903-108">The **RtmGetRouteAge** function returns the age of a route.</span></span> <span data-ttu-id="e7903-109">Das Alter ist die Zeit (in Sekunden), seit der es erstellt oder zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e7903-109">The age is the time, in seconds, since it was created or last updated.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7903-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7903-110">Syntax</span></span>


```C++
ULONG RtmGetRouteAge(
  _In_ PVOID Route
);
```



## <a name="parameters"></a><span data-ttu-id="e7903-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="e7903-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7903-112">*Route* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e7903-112">*Route* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7903-113">Ein Zeiger auf eine Protokoll Familien spezifische Struktur, die Routendaten angibt, die vor kurzem vom Routing Tabellen-Manager abgerufen wurden.</span><span class="sxs-lookup"><span data-stu-id="e7903-113">Pointer to a protocol-family-specific structure that specifies route data recently obtained from the routing table manager.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7903-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e7903-114">Return value</span></span>

<span data-ttu-id="e7903-115">Der Rückgabewert ist einer der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="e7903-115">The return value is one of the following values.</span></span>



| <span data-ttu-id="e7903-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e7903-116">Value</span></span>                                                                                   | <span data-ttu-id="e7903-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e7903-117">Description</span></span>                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e7903-118"><dt>**Routeage**</dt></span><span class="sxs-lookup"><span data-stu-id="e7903-118"><dt>**RouteAge**</dt></span></span> </dl> | <span data-ttu-id="e7903-119">Die Zeit (in Sekunden), seit der eine Route erstellt oder zuletzt aktualisiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e7903-119">The time in seconds since a route was created or last updated.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="e7903-120"><dt>**Lichem**</dt></span><span class="sxs-lookup"><span data-stu-id="e7903-120"><dt>**INFINITE**</dt></span></span> </dl> | <span data-ttu-id="e7903-121">Der Inhalt der Routen Struktur ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e7903-121">The content of the route structure is invalid.</span></span> <span data-ttu-id="e7903-122">In diesem Fall gibt ein Aufrufen von " [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) " einen \_ ungültigen \_ Parameter zurück.</span><span class="sxs-lookup"><span data-stu-id="e7903-122">In this case, a call to [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns ERROR\_INVALID\_PARAMETER.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e7903-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7903-123">Remarks</span></span>

<span data-ttu-id="e7903-124">Das Routing Alter wird aus dem RR- \_ timestamp-Member der Struktur berechnet, auf die durch den *Routen* Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e7903-124">The route age is computed from the RR\_TimeStamp member of the structure that is pointed to by the *Route* parameter.</span></span> <span data-ttu-id="e7903-125">Der Routing Tabellen-Manager legt den Wert dieses Members fest, wenn eine Route hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="e7903-125">The routing table manager sets the value of this member when a route is added or updated.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7903-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7903-126">Requirements</span></span>



| <span data-ttu-id="e7903-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7903-127">Requirement</span></span> | <span data-ttu-id="e7903-128">Wert</span><span class="sxs-lookup"><span data-stu-id="e7903-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e7903-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e7903-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e7903-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e7903-130">None supported</span></span><br/>                                                          |
| <span data-ttu-id="e7903-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e7903-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e7903-132">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e7903-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e7903-133">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="e7903-133">End of server support</span></span><br/>    | <span data-ttu-id="e7903-134">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e7903-134">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="e7903-135">Header</span><span class="sxs-lookup"><span data-stu-id="e7903-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7903-136"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7903-136"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7903-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e7903-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7903-138"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7903-138"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="e7903-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e7903-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e7903-140"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e7903-140"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7903-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7903-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7903-142">Referenz für Routing Tabellen-Manager Version \_ 1</span><span class="sxs-lookup"><span data-stu-id="e7903-142">Routing Table Manager Version\_1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="e7903-143">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="e7903-143">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="e7903-144">**GetLastError**</span><span class="sxs-lookup"><span data-stu-id="e7903-144">**GetLastError**</span></span>](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[<span data-ttu-id="e7903-145">**RTM \_ -IP- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="e7903-145">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="e7903-146">**RTM- \_ IPX- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="e7903-146">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> </dl>

 

