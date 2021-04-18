---
title: Inapsystemhealthagentbinding flushcache-Methode (napsystemhealthagent. h)
description: Wird von einem SHA aufgerufen, um den SoH-Cache zu leeren.
ms.assetid: a771ce03-1922-4e2d-9490-7ee9f693857c
keywords:
- Flushcache-Methode NAP
- Flushcache-Methode NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, flushcache-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.FlushCache
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ead6e496d220619439b80fdc5c7601675fdb7ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338316"
---
# <a name="inapsystemhealthagentbindingflushcache-method"></a><span data-ttu-id="e3d12-106">Inapsystemhealthagentbinding:: FLUSHCACHE-Methode</span><span class="sxs-lookup"><span data-stu-id="e3d12-106">INapSystemHealthAgentBinding::FlushCache method</span></span>

> [!Note]  
> <span data-ttu-id="e3d12-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e3d12-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="e3d12-108">Die **inapsystemhealthagentbinding:: FLUSHCACHE** -Methode wird von einem SHA aufgerufen, um den SoH-Cache zu leeren.</span><span class="sxs-lookup"><span data-stu-id="e3d12-108">The **INapSystemHealthAgentBinding::FlushCache** method is called by an SHA to flush its SoH cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3d12-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3d12-109">Syntax</span></span>


```C++
HRESULT FlushCache();
```



## <a name="parameters"></a><span data-ttu-id="e3d12-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3d12-110">Parameters</span></span>

<span data-ttu-id="e3d12-111">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e3d12-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3d12-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3d12-112">Return value</span></span>

<span data-ttu-id="e3d12-113">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e3d12-113">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="e3d12-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e3d12-114">Return code</span></span>                                                                                         | <span data-ttu-id="e3d12-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e3d12-115">Description</span></span>                                                                                                                    |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e3d12-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e3d12-116"><dt>**S\_OK** </dt></span></span> </dl>               | <span data-ttu-id="e3d12-117">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e3d12-117">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="e3d12-118"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="e3d12-118"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>     | <span data-ttu-id="e3d12-119">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="e3d12-119">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="e3d12-120"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="e3d12-120"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>      | <span data-ttu-id="e3d12-121">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e3d12-121">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="e3d12-122"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="e3d12-122"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl> | <span data-ttu-id="e3d12-123">Der NAPAgent wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="e3d12-123">The NapAgent has been stopped.</span></span> <span data-ttu-id="e3d12-124">Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.</span><span class="sxs-lookup"><span data-stu-id="e3d12-124">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e3d12-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3d12-125">Remarks</span></span>

<span data-ttu-id="e3d12-126">Der NAPAgent verwaltet einen Cache aktueller SoHs, die von verschiedenen SHAs bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="e3d12-126">The NapAgent maintains a cache of recent SoHs provided by different SHAs.</span></span> <span data-ttu-id="e3d12-127">Dieser Cache ist nützlich, um die Leistung der Start Zeit zu optimieren, wenn SHAs an das System gebunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="e3d12-127">This cache is useful to optimize boot-time performance, when SHAs may or may not be bound to the system.</span></span>

<span data-ttu-id="e3d12-128">Das SHA muss [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) aufrufen, bevor diese Methode oder eine andere Methode der [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="e3d12-128">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3d12-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3d12-129">Requirements</span></span>



| <span data-ttu-id="e3d12-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3d12-130">Requirement</span></span> | <span data-ttu-id="e3d12-131">Wert</span><span class="sxs-lookup"><span data-stu-id="e3d12-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3d12-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e3d12-132">Minimum supported client</span></span><br/> | <span data-ttu-id="e3d12-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3d12-133">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="e3d12-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e3d12-134">Minimum supported server</span></span><br/> | <span data-ttu-id="e3d12-135">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e3d12-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="e3d12-136">Header</span><span class="sxs-lookup"><span data-stu-id="e3d12-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="e3d12-137"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3d12-137"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="e3d12-138">IDL</span><span class="sxs-lookup"><span data-stu-id="e3d12-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e3d12-139"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e3d12-139"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="e3d12-140">DLL</span><span class="sxs-lookup"><span data-stu-id="e3d12-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3d12-141"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e3d12-141"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e3d12-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3d12-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3d12-143">**Inapsystemhealthagentbinding**</span><span class="sxs-lookup"><span data-stu-id="e3d12-143">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





