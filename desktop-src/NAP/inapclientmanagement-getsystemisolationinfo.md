---
title: Inapclientmanagement getsystemisolationinfo-Methode (napmanagement. h)
description: Ruft Informationen zum Isolations Status von napclient ab.
ms.assetid: e1f69e66-71ca-402e-9c94-8af159d00b21
keywords:
- Getsystemisolationinfo-Methode NAP
- Getsystemisolationinfo-Methode NAP, inapclientmanagement-Schnittstelle
- Inapclientmanagement Interface NAP, getsystemisolationinfo-Methode
topic_type:
- apiref
api_name:
- INapClientManagement.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73b3d446e0a8068353be6656c16f0e6796df8922
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392091"
---
# <a name="inapclientmanagementgetsystemisolationinfo-method"></a><span data-ttu-id="b1b6d-106">Inapclientmanagement:: getsystemisolationinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="b1b6d-106">INapClientManagement::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="b1b6d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="b1b6d-108">Die **getsystemisolationinfo** -Methode ruft Informationen zum Isolations Status von napclient ab.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-108">The **GetSystemIsolationInfo** method retrieves information about the isolation state of the NapClient.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1b6d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1b6d-109">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="b1b6d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1b6d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1b6d-111">*IsolationInfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b1b6d-111">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1b6d-112">Ein Zeiger auf einen Zeiger auf eine [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) -Struktur, die Isolations Zustandsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-112">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains isolation state information.</span></span>

</dd> <dt>

<span data-ttu-id="b1b6d-113">*unknownconnections* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b1b6d-113">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b1b6d-114">Ein Zeiger auf ein Flag, das angibt, ob sich eine der Verbindungen in einem unbekannten Zustand befindet.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-114">A pointer to a flag that indicates whether any of the connections are in an unknown state.</span></span> <span data-ttu-id="b1b6d-115">Wenn eine der beiden Werte ist, wird das-Flag auf **true** festgelegt. Andernfalls wird das-Flag auf **false** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-115">If any of them are, the flag is set to **TRUE**; otherwise the flag is set to **FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1b6d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b1b6d-116">Return value</span></span>

<span data-ttu-id="b1b6d-117">Die-Methode gibt einen HRESULT-Statuscode zurück, einschließlich, aber nicht beschränkt auf einen der folgenden.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-117">The method returns an HRESULT status code including but not limited to one of the following.</span></span>



| <span data-ttu-id="b1b6d-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b1b6d-118">Return code</span></span>                                                                                         | <span data-ttu-id="b1b6d-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1b6d-119">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="b1b6d-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6d-120"><dt>**S\_OK**</dt></span></span> </dl>                | <span data-ttu-id="b1b6d-121">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-121">Operation successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="b1b6d-122"><dt>**E \_ AccessDenied**</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6d-122"><dt>**E\_ACCESSDENIED**</dt></span></span> </dl>      | <span data-ttu-id="b1b6d-123">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-123">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="b1b6d-124"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6d-124"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>       | <span data-ttu-id="b1b6d-125">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-125">System resource limit, could not perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="b1b6d-126"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6d-126"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="b1b6d-127">Der NAPAgent wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-127">The NapAgent is not running.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="b1b6d-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b1b6d-128">Remarks</span></span>

<span data-ttu-id="b1b6d-129">Die abgerufenen Isolations Informationen spiegeln keine unbekannten Zustände wider.</span><span class="sxs-lookup"><span data-stu-id="b1b6d-129">The isolation information that is retrieved does not reflect unknown states.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1b6d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b1b6d-130">Requirements</span></span>



| <span data-ttu-id="b1b6d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b1b6d-131">Requirement</span></span> | <span data-ttu-id="b1b6d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b1b6d-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1b6d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b1b6d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b1b6d-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1b6d-134">Windows Vista \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="b1b6d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b1b6d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b1b6d-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b1b6d-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="b1b6d-137">Header</span><span class="sxs-lookup"><span data-stu-id="b1b6d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1b6d-138"><dt>Napmanagement. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6d-138"><dt>NapManagement.h</dt></span></span> </dl>   |
| <span data-ttu-id="b1b6d-139">IDL</span><span class="sxs-lookup"><span data-stu-id="b1b6d-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b1b6d-140"><dt>Napmanagement. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6d-140"><dt>NapManagement.idl</dt></span></span> </dl> |
| <span data-ttu-id="b1b6d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b1b6d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1b6d-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1b6d-142"><dt>Qagent.dll</dt></span></span> </dl>        |



## <a name="see-also"></a><span data-ttu-id="b1b6d-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1b6d-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1b6d-144">**Inapclientmanagement**</span><span class="sxs-lookup"><span data-stu-id="b1b6d-144">**INapClientManagement**</span></span>](inapclientmanagement.md)
</dt> </dl>

 

 





