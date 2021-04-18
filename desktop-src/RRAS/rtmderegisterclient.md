---
title: Rtmderegisterclient-Funktion (RTM. h)
description: Die Funktion rtmderegisterclient hebt die Registrierung des Clients auf und gibt die dem Client zugeordneten Ressourcen frei.
ms.assetid: 5d04f276-86a7-4e63-8266-e93f0d6e5241
keywords:
- Rtmderegisterclient-Funktion (RAS)
topic_type:
- apiref
api_name:
- RtmDeregisterClient
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab1f56d3d65e13c083d8952f500cfba4638ab83
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391901"
---
# <a name="rtmderegisterclient-function"></a><span data-ttu-id="94739-104">Rtmderegisterclient-Funktion</span><span class="sxs-lookup"><span data-stu-id="94739-104">RtmDeregisterClient function</span></span>

<span data-ttu-id="94739-105">\[Diese API wurde durch die API für [Routing Table Manager, Version 2](about-routing-table-manager-version-2.md) , ersetzt und ist nicht über Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="94739-105">\[This API has been superseded by the [Routing Table Manager Version 2](about-routing-table-manager-version-2.md) API and will not be available beyond Windows Server 2003.</span></span> <span data-ttu-id="94739-106">Anwendungen sollten die API für Routing Table Manager Version 2 verwenden.\]</span><span class="sxs-lookup"><span data-stu-id="94739-106">Applications should use the Routing Table Manager Version 2 API.\]</span></span>

<span data-ttu-id="94739-107">Die Funktion **rtmderegisterclient** hebt die Registrierung des Clients auf und gibt die dem Client zugeordneten Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="94739-107">The **RtmDeregisterClient** function deregisters the client, and frees resources associated with the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="94739-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="94739-108">Syntax</span></span>


```C++
DWORD RtmDeregisterClient(
  _In_ HANDLE ClientHandle
);
```



## <a name="parameters"></a><span data-ttu-id="94739-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="94739-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94739-110">*Clienthandle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94739-110">*ClientHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94739-111">Handle, das den Client identifiziert, dessen Registrierung aufgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="94739-111">Handle that identifies the client to deregister.</span></span> <span data-ttu-id="94739-112">Rufen Sie dieses Handle durch Aufrufen von [**rtmregisterclient**](rtmregisterclient.md)ab.</span><span class="sxs-lookup"><span data-stu-id="94739-112">Obtain this handle by calling [**RtmRegisterClient**](rtmregisterclient.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94739-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94739-113">Return value</span></span>

<span data-ttu-id="94739-114">Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert kein \_ Fehler.</span><span class="sxs-lookup"><span data-stu-id="94739-114">If the function succeeds, the return value is NO\_ERROR.</span></span>

<span data-ttu-id="94739-115">Wenn die Funktion fehlschlägt, ist der Rückgabewert einer der folgenden Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="94739-115">If the function fails, the return value is one of the following error codes.</span></span>



| <span data-ttu-id="94739-116">Wert</span><span class="sxs-lookup"><span data-stu-id="94739-116">Value</span></span>                                                                                                       | <span data-ttu-id="94739-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94739-117">Description</span></span>                                                    |
|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="94739-118"><dt>**Fehler bei \_ ungültigem \_ handle**</dt></span><span class="sxs-lookup"><span data-stu-id="94739-118"><dt>**ERROR\_INVALID\_HANDLE**</dt></span></span> </dl>       | <span data-ttu-id="94739-119">Der *Clienthandle* -Parameter ist kein gültiges Handle.</span><span class="sxs-lookup"><span data-stu-id="94739-119">The *ClientHandle* parameter is not a valid handle.</span></span><br/> |
| <dl> <span data-ttu-id="94739-120"><dt>**Fehler \_ keine \_ System \_ Ressourcen**</dt></span><span class="sxs-lookup"><span data-stu-id="94739-120"><dt>**ERROR\_NO\_SYSTEM\_RESOURCES**</dt></span></span> </dl> | <span data-ttu-id="94739-121">Nicht genügend Ressourcen, um den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="94739-121">Insufficient resources to carry out the operation.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="94739-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="94739-122">Remarks</span></span>

<span data-ttu-id="94739-123">Diese Funktion entfernt alle Routen, die vom Client hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="94739-123">This function removes all routes that were added by the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="94739-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94739-124">Requirements</span></span>



| <span data-ttu-id="94739-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94739-125">Requirement</span></span> | <span data-ttu-id="94739-126">Wert</span><span class="sxs-lookup"><span data-stu-id="94739-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94739-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94739-127">Minimum supported client</span></span><br/> | <span data-ttu-id="94739-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="94739-128">None supported</span></span><br/>                                                          |
| <span data-ttu-id="94739-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94739-129">Minimum supported server</span></span><br/> | <span data-ttu-id="94739-130">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94739-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="94739-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="94739-131">End of server support</span></span><br/>    | <span data-ttu-id="94739-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="94739-132">Windows Server 2003</span></span><br/>                                                     |
| <span data-ttu-id="94739-133">Header</span><span class="sxs-lookup"><span data-stu-id="94739-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="94739-134"><dt>RTM. h</dt></span><span class="sxs-lookup"><span data-stu-id="94739-134"><dt>Rtm.h</dt></span></span> </dl>   |
| <span data-ttu-id="94739-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94739-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="94739-136"><dt>RTM. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94739-136"><dt>Rtm.lib</dt></span></span> </dl> |
| <span data-ttu-id="94739-137">DLL</span><span class="sxs-lookup"><span data-stu-id="94739-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94739-138"><dt>Rtm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94739-138"><dt>Rtm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94739-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94739-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94739-140">Referenz für Routing Tabellen-Manager Version 1</span><span class="sxs-lookup"><span data-stu-id="94739-140">Routing Table Manager Version 1 Reference</span></span>](routing-table-manager-version-1-reference.md)
</dt> <dt>

[<span data-ttu-id="94739-141">Funktionen der Routing-Tabellen-Manager-Version 1</span><span class="sxs-lookup"><span data-stu-id="94739-141">Routing Table Manager Version 1 Functions</span></span>](routing-table-manager-version-1-functions.md)
</dt> <dt>

[<span data-ttu-id="94739-142">**Rtmregisterclient**</span><span class="sxs-lookup"><span data-stu-id="94739-142">**RtmRegisterClient**</span></span>](rtmregisterclient.md)
</dt> </dl>

 

 





