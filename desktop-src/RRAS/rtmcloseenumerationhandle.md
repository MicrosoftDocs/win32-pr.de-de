---
title: Rtmcloseenumerationhandle-Funktion (RTM. h)
description: Das rtmcloseenumerationhandle beendet eine angegebene Enumeration und gibt die zugeordneten Ressourcen frei.
ms.assetid: 8daea42f-4304-4749-9894-d37f6ba733da
keywords:
- Rtmcloseenumerationhandle-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmCloseEnumerationHandle
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5adb47d40cb1300305c7ff6f9bb6f1c3c716f0f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040753"
---
# <a name="rtmcloseenumerationhandle-function"></a><span data-ttu-id="75f24-104">Rtmcloseenumerationhandle-Funktion</span><span class="sxs-lookup"><span data-stu-id="75f24-104">RtmCloseEnumerationHandle function</span></span>

<span data-ttu-id="75f24-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="75f24-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="75f24-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="75f24-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="75f24-107">Das **rtmcloseenumerationhandle** beendet eine angegebene Enumeration und gibt die zugeordneten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="75f24-107">The **RtmCloseEnumerationHandle** terminates a specified enumeration and frees the associated resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="75f24-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="75f24-108">Syntax</span></span>


```C++
DWORD RtmCloseEnumerationHandle(
  _In_ HANDLE EnumerationHandle
);
```



## <a name="parameters"></a><span data-ttu-id="75f24-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="75f24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75f24-110">*Enumerationhandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75f24-110">*EnumerationHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75f24-111">Handle für die zu beendende Enumeration.</span><span class="sxs-lookup"><span data-stu-id="75f24-111">Handle to the enumeration to terminate.</span></span> <span data-ttu-id="75f24-112">Rufen Sie dieses Handle durch Aufrufen von [**rtmcreateenumerationhandle**](rtmcreateenumerationhandle.md)ab.</span><span class="sxs-lookup"><span data-stu-id="75f24-112">Obtain this handle by calling [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75f24-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75f24-113">Return value</span></span>

<span data-ttu-id="75f24-114">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.</span><span class="sxs-lookup"><span data-stu-id="75f24-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="75f24-115">Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="75f24-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="75f24-116">Wert</span><span class="sxs-lookup"><span data-stu-id="75f24-116">Value</span></span>                                                                                                       | <span data-ttu-id="75f24-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="75f24-117">Description</span></span>                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <span data-ttu-id="75f24-118"><dt>**Fehler bei \_ ungültigem \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="75f24-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="75f24-119">Der Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="75f24-119">The parameter is not valid.</span></span><br/>                                  |
| <dl> <span data-ttu-id="75f24-120"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="75f24-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="75f24-121">Es sind nicht genügend Ressourcen vorhanden, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="75f24-121">There are insufficient resources to carry out the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="75f24-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75f24-122">Requirements</span></span>



| <span data-ttu-id="75f24-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75f24-123">Requirement</span></span> | <span data-ttu-id="75f24-124">Wert</span><span class="sxs-lookup"><span data-stu-id="75f24-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="75f24-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75f24-125">Minimum supported client</span></span><br/> | <span data-ttu-id="75f24-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="75f24-126">None supported</span></span><br/>                                                          |
| <span data-ttu-id="75f24-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75f24-127">Minimum supported server</span></span><br/> | <span data-ttu-id="75f24-128">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="75f24-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="75f24-129">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="75f24-129">End of server support</span></span><br/>    | <span data-ttu-id="75f24-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="75f24-130">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="75f24-131">Header</span><span class="sxs-lookup"><span data-stu-id="75f24-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="75f24-132"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="75f24-132"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="75f24-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="75f24-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="75f24-134"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="75f24-134"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="75f24-135">DLL</span><span class="sxs-lookup"><span data-stu-id="75f24-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75f24-136"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75f24-136"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75f24-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75f24-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75f24-138">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="75f24-138">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="75f24-139">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="75f24-139">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="75f24-140">**Rtmkreateenumerationhandle**</span><span class="sxs-lookup"><span data-stu-id="75f24-140">**RtmCreateEnumerationHandle**</span></span>](rtmcreateenumerationhandle.md)
</dt> <dt>

[<span data-ttu-id="75f24-141">**Rtmenumschlag-ategetnextroute**</span><span class="sxs-lookup"><span data-stu-id="75f24-141">**RtmEnumerateGetNextRoute**</span></span>](rtmenumerategetnextroute.md)
</dt> </dl>

 

 





