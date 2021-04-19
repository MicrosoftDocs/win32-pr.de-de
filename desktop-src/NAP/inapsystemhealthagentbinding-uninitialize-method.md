---
title: Inapsystemhealthagentbinding-Methode zur uninitialisierung (napsystemhealthagent. h)
description: Bewirkt, dass der NAPAgent alle Verweise auf com-Zeiger für den Systemintegritäts-Agent freigibt.
ms.assetid: 8b9fabc9-7453-41fe-a1e7-2ec5fa275a3a
keywords:
- Methode "NAP initialisieren"
- Uninitialize-Methode, NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, Uninitialize-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.Uninitialize
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a863e9d742610ab764a3b7a00966e8e112278317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339974"
---
# <a name="inapsystemhealthagentbindinguninitialize-method"></a><span data-ttu-id="6c239-106">Inapsystemhealthagentbinding:: Uninitialize-Methode</span><span class="sxs-lookup"><span data-stu-id="6c239-106">INapSystemHealthAgentBinding::Uninitialize method</span></span>

> [!Note]  
> <span data-ttu-id="6c239-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="6c239-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="6c239-108">Die **inapsystemhealthagentbinding:: Uninitialize** -Methode bewirkt, dass der NAPAgent alle Verweise auf com-Zeiger für den Systemintegritäts-Agent freigibt.</span><span class="sxs-lookup"><span data-stu-id="6c239-108">The **INapSystemHealthAgentBinding::Uninitialize** method causes the NapAgent to release all its references to system health agent COM pointers.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c239-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c239-109">Syntax</span></span>


```C++
HRESULT Uninitialize();
```



## <a name="parameters"></a><span data-ttu-id="6c239-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c239-110">Parameters</span></span>

<span data-ttu-id="6c239-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6c239-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6c239-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c239-112">Return value</span></span>

<span data-ttu-id="6c239-113">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="6c239-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="6c239-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6c239-114">Return code</span></span>                                                                                             | <span data-ttu-id="6c239-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6c239-115">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6c239-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6c239-116"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="6c239-117">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6c239-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="6c239-118"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="6c239-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="6c239-119">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="6c239-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="6c239-120"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="6c239-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="6c239-121">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6c239-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="6c239-122"><dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="6c239-122"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="6c239-123">Das SHA wurde nicht bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="6c239-123">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="6c239-124"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="6c239-124"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="6c239-125">Der NAPAgent wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="6c239-125">The NapAgent has been stopped.</span></span> <span data-ttu-id="6c239-126">Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.</span><span class="sxs-lookup"><span data-stu-id="6c239-126">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6c239-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c239-127">Remarks</span></span>

<span data-ttu-id="6c239-128">Der NAPAgent blockiert die Ausführung dieses Methoden Aufrufs, bis alle vorhandenen Aufrufe an die Bindungs-und Rückruf Schnittstellen vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="6c239-128">The NapAgent blocks execution of this method call until all existing calls on the Binding and Callback interfaces complete.</span></span>

<span data-ttu-id="6c239-129">Das SHA muss [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) aufrufen, bevor diese Methode oder eine andere Methode der [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6c239-129">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c239-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c239-130">Requirements</span></span>



| <span data-ttu-id="6c239-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c239-131">Requirement</span></span> | <span data-ttu-id="6c239-132">Wert</span><span class="sxs-lookup"><span data-stu-id="6c239-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c239-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c239-133">Minimum supported client</span></span><br/> | <span data-ttu-id="6c239-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c239-134">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6c239-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c239-135">Minimum supported server</span></span><br/> | <span data-ttu-id="6c239-136">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c239-136">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6c239-137">Header</span><span class="sxs-lookup"><span data-stu-id="6c239-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c239-138"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c239-138"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c239-139">IDL</span><span class="sxs-lookup"><span data-stu-id="6c239-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6c239-140"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c239-140"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="6c239-141">DLL</span><span class="sxs-lookup"><span data-stu-id="6c239-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c239-142"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c239-142"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="6c239-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c239-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c239-144">**Inapsystemhealthagentbinding**</span><span class="sxs-lookup"><span data-stu-id="6c239-144">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





