---
title: Inapsystemhealthagentbinding notifysohchange-Methode (napsystemhealthagent. h)
description: Wird von SHAs verwendet, wenn sich Ihr SoH ändert.
ms.assetid: 3a653282-03b0-49d5-833f-966497f46faa
keywords:
- Notifysohchange-Methode NAP
- Notifysohchange-Methode NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, notifysohchange-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.NotifySoHChange
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b18c03be03c4bc5282e9ea62ec10d5356871cf5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518947"
---
# <a name="inapsystemhealthagentbindingnotifysohchange-method"></a><span data-ttu-id="5ba1d-106">Inapsystemhealthagentbinding:: notifysohchange-Methode</span><span class="sxs-lookup"><span data-stu-id="5ba1d-106">INapSystemHealthAgentBinding::NotifySoHChange method</span></span>

> [!Note]  
> <span data-ttu-id="5ba1d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="5ba1d-108">Die **inapsystemhealthagentbinding:: notifysohchange** -Methode wird von SHAs verwendet, wenn Ihr SoH geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-108">The **INapSystemHealthAgentBinding::NotifySoHChange** method is used by SHAs when their SoH changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ba1d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ba1d-109">Syntax</span></span>


```C++
HRESULT NotifySoHChange();
```



## <a name="parameters"></a><span data-ttu-id="5ba1d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ba1d-110">Parameters</span></span>

<span data-ttu-id="5ba1d-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5ba1d-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ba1d-112">Return value</span></span>

<span data-ttu-id="5ba1d-113">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="5ba1d-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5ba1d-114">Return code</span></span>                                                                                             | <span data-ttu-id="5ba1d-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ba1d-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ba1d-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba1d-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="5ba1d-117">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="5ba1d-118"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba1d-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="5ba1d-119">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="5ba1d-120"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba1d-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="5ba1d-121">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="5ba1d-122"><dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba1d-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="5ba1d-123">Das SHA wurde nicht bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="5ba1d-124"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="5ba1d-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="5ba1d-125">Der NAPAgent wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="5ba1d-126">Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ba1d-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ba1d-127">Remarks</span></span>

<span data-ttu-id="5ba1d-128">SHAs dürfen diese API nicht spekulativ aufrufen, da dies zu einem SoH-Austausch im Netzwerk führt.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-128">SHAs must not call this API speculatively since it results in an SoH exchange on the wire.</span></span> <span data-ttu-id="5ba1d-129">Aufrufe dieser API sollten nur bei Bedarf durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-129">Calls to this API should only be made when necessary.</span></span>

<span data-ttu-id="5ba1d-130">Der NAPAgent speichert diesen Thread nicht, um die SoH-Änderung zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-130">The NapAgent does not hold this thread to process the SoH change.</span></span> <span data-ttu-id="5ba1d-131">Stattdessen wird sofort zurückgegeben, und die Änderung wird asynchron verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-131">Instead, it returns immediately and processes the change asynchronously.</span></span>

<span data-ttu-id="5ba1d-132">Das SHA muss [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) aufrufen, bevor diese Methode oder eine andere Methode der [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5ba1d-132">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ba1d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ba1d-133">Requirements</span></span>



| <span data-ttu-id="5ba1d-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ba1d-134">Requirement</span></span> | <span data-ttu-id="5ba1d-135">Wert</span><span class="sxs-lookup"><span data-stu-id="5ba1d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ba1d-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ba1d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="5ba1d-137">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ba1d-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="5ba1d-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ba1d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="5ba1d-139">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ba1d-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="5ba1d-140">Header</span><span class="sxs-lookup"><span data-stu-id="5ba1d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ba1d-141"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="5ba1d-141"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="5ba1d-142">IDL</span><span class="sxs-lookup"><span data-stu-id="5ba1d-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5ba1d-143"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5ba1d-143"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="5ba1d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5ba1d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ba1d-145"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ba1d-145"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="5ba1d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ba1d-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ba1d-147">**Inapsystemhealthagentbinding**</span><span class="sxs-lookup"><span data-stu-id="5ba1d-147">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





