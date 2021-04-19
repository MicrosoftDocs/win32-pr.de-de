---
title: Rtmenenerategetnextroute-Funktion (RTM. h)
description: Die rtmenumerategetnextroute-Funktion gibt den Eintrag für die nächste Route in der Enumeration zurück, die durch einen Aufruf von rtmkreateenumerationhandle gestartet wird.
ms.assetid: fff6fb58-8a37-49f0-abc5-354b5bc340f8
keywords:
- Rtmenumschlag-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmEnumerateGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e74cc5aa15c1014056075e876efca296556066d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339989"
---
# <a name="rtmenumerategetnextroute-function"></a><span data-ttu-id="5540f-104">Rtmenenerategetnextroute-Funktion</span><span class="sxs-lookup"><span data-stu-id="5540f-104">RtmEnumerateGetNextRoute function</span></span>

<span data-ttu-id="5540f-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5540f-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="5540f-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="5540f-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="5540f-107">Die **rtmenumerategetnextroute** -Funktion gibt den Eintrag für die nächste Route in der Enumeration zurück, die durch einen Aufruf von [**rtmkreateenumerationhandle**](rtmcreateenumerationhandle.md)gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5540f-107">The **RtmEnumerateGetNextRoute** function returns the next-route entry in the enumeration started by a call to [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="5540f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5540f-108">Syntax</span></span>


```C++
DWORD RtmEnumerateGetNextRoute(
  _In_  HANDLE EnumerationHandle,
  _Out_ PVOID  Route
);
```



## <a name="parameters"></a><span data-ttu-id="5540f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5540f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5540f-110">*Enumerationhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5540f-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5540f-111">Handle, das die Enumeration identifiziert und den Gültigkeitsbereich angibt.</span><span class="sxs-lookup"><span data-stu-id="5540f-111">Handle that identifies the enumeration and specifies its scope.</span></span> <span data-ttu-id="5540f-112">Rufen Sie dieses Handle durch Aufrufen von [**rtmcreateenumerationhandle**](rtmcreateenumerationhandle.md)ab.</span><span class="sxs-lookup"><span data-stu-id="5540f-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> <dt>

<span data-ttu-id="5540f-113">*Route* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5540f-113">*Route* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5540f-114">Zeiger auf eine Protokoll familienspezifische Routen Struktur ( [**RTM \_ -IP- \_ Route**](rtm-ip-route.md) oder [**RTM \_ IPX- \_ Route**](rtm-ipx-route.md)).</span><span class="sxs-lookup"><span data-stu-id="5540f-114">Pointer to a protocol-family-specific route structure ( [**RTM\_IP\_ROUTE**](rtm-ip-route.md) or [**RTM\_IPX\_ROUTE**](rtm-ipx-route.md)).</span></span> <span data-ttu-id="5540f-115">Diese Struktur empfängt die nächste Route in der-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="5540f-115">This structure will receive the next route in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5540f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5540f-116">Return value</span></span>

<span data-ttu-id="5540f-117">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.</span><span class="sxs-lookup"><span data-stu-id="5540f-117">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="5540f-118">Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="5540f-118">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="5540f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="5540f-119">Value</span></span>                                                                                                       | <span data-ttu-id="5540f-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5540f-120">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5540f-121"><dt>**Fehler bei \_ ungültigem \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="5540f-121"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="5540f-122">Der *enumerationhandle* -Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="5540f-122">The *EnumerationHandle* parameter is not valid.</span></span><br/>              |
| <dl> <span data-ttu-id="5540f-123"><dt>**Fehler \_ keine \_ weiteren \_ Routen**</dt></span><span class="sxs-lookup"><span data-stu-id="5540f-123"><dt>**ERROR\_NO\_MORE\_ROUTES**</dt></span></span> </dl>      | <span data-ttu-id="5540f-124">In der-Enumeration sind keine weiteren Routen vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5540f-124">There are no more routes in the enumeration.</span></span><br/>                 |
| <dl> <span data-ttu-id="5540f-125"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="5540f-125"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="5540f-126">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="5540f-126">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5540f-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5540f-127">Remarks</span></span>

<span data-ttu-id="5540f-128">Obwohl Routen nicht in einer bestimmten Reihenfolge zurückgegeben werden, wird jede Route in der Enumeration nur einmal zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5540f-128">Although routes are not returned in any particular order, each route in the enumeration is returned only once.</span></span>

## <a name="requirements"></a><span data-ttu-id="5540f-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5540f-129">Requirements</span></span>



| <span data-ttu-id="5540f-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5540f-130">Requirement</span></span> | <span data-ttu-id="5540f-131">Wert</span><span class="sxs-lookup"><span data-stu-id="5540f-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5540f-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5540f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="5540f-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="5540f-133">None supported</span></span><br/>                                                          |
| <span data-ttu-id="5540f-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5540f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="5540f-135">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5540f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="5540f-136">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="5540f-136">End of server support</span></span><br/>    | <span data-ttu-id="5540f-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="5540f-137">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="5540f-138">Header</span><span class="sxs-lookup"><span data-stu-id="5540f-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="5540f-139"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="5540f-139"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="5540f-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5540f-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="5540f-141"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5540f-141"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="5540f-142">DLL</span><span class="sxs-lookup"><span data-stu-id="5540f-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5540f-143"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5540f-143"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5540f-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5540f-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5540f-145">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="5540f-145">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="5540f-146">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="5540f-146">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="5540f-147">**RTM \_ -IP- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="5540f-147">**RTM\_IP\_ROUTE**</span></span>](rtm-ip-route.md)
</dt> <dt>

[<span data-ttu-id="5540f-148">**RTM- \_ IPX- \_ Route**</span><span class="sxs-lookup"><span data-stu-id="5540f-148">**RTM\_IPX\_ROUTE**</span></span>](rtm-ipx-route.md)
</dt> <dt>

[<span data-ttu-id="5540f-149">**Rtmcloseenumerationhandle**</span><span class="sxs-lookup"><span data-stu-id="5540f-149">**RtmCloseEnumerationHandle**</span></span>](rtmcloseenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="5540f-150">**Rtmkreateenumerationhandle**</span><span class="sxs-lookup"><span data-stu-id="5540f-150">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> </dl>

 

 





