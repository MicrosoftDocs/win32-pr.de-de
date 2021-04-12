---
title: INapSystemHealthAgentBinding2 getsystemisolationinfoex-Methode (napsystemhealthagent. h)
description: Wird von SHAs aufgerufen, um den systemisolations Status und den erweiterten Isolations Status zu bestimmen.
ms.assetid: 237e5539-889c-457d-8db0-bf3379f28b85
keywords:
- Getsystemisolationinfoex-Methode NAP
- Getsystemisolationinfoex-Methode NAP, INapSystemHealthAgentBinding2-Schnittstelle
- INapSystemHealthAgentBinding2 Interface NAP, getsystemisolationinfoex-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding2.GetSystemIsolationInfoEx
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2643d62afba1a35ebd96b8b39ea2fcf90397576
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517933"
---
# <a name="inapsystemhealthagentbinding2getsystemisolationinfoex-method"></a><span data-ttu-id="14126-106">INapSystemHealthAgentBinding2:: getsystemisolationinfoex-Methode</span><span class="sxs-lookup"><span data-stu-id="14126-106">INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx method</span></span>

> [!Note]  
> <span data-ttu-id="14126-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="14126-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="14126-108">Die **INapSystemHealthAgentBinding2:: getsystemsolationinfoex** -Methode wird von SHAs aufgerufen, um den systemisolations Status und den erweiterten Isolations Status zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="14126-108">The **INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx** method is called by SHAs to determine the system isolation state and extended isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="14126-109">Verwenden Sie [**inapsystemhealthagentbinding:: getsystemsolationinfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) , um nur den Isolations Status des Systems zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="14126-109">Use [**INapSystemHealthAgentBinding::GetSystemIsolationInfo**](inapsystemhealthagentbinding-getsystemisolationinfo-method.md) in order to only determine the isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="14126-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="14126-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfoEx(
  [out] IsolationInfoEx **isolationInfo,
  [out] BOOL            *unknownConnections
) const;
```



## <a name="parameters"></a><span data-ttu-id="14126-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="14126-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14126-112">*IsolationInfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="14126-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14126-113">Ein Zeiger auf einen Zeiger auf eine [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur, die den erweiterten Isolations Zustand des Systems für bekannte Verbindungen enthält.</span><span class="sxs-lookup"><span data-stu-id="14126-113">A pointer to a pointer to an [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure that contains the extended isolation state of the system for known connections.</span></span> <span data-ttu-id="14126-114">*IsolationInfo* gibt an, ob sich das System in einem Zustand mit eingeschränktem Zugriff, Bewährung oder uneingeschränktem Zugriff befindet, sowie [**extendedisolationstate**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) -Informationen.</span><span class="sxs-lookup"><span data-stu-id="14126-114">*isolationInfo* indicates if the system is in a state of restricted access, probation, or unrestricted access, as well as [**ExtendedIsolationState**](/windows/win32/api/naptypes/ne-naptypes-extendedisolationstate) information.</span></span>

</dd> <dt>

<span data-ttu-id="14126-115">*unknownconnections* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="14126-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14126-116">Ein Zeiger auf einen **booleschen** Wert, der **true** ist, wenn sich Verbindungen in einem unbekannten Zustand befinden, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="14126-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14126-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14126-117">Return value</span></span>

<span data-ttu-id="14126-118">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="14126-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="14126-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="14126-119">Return code</span></span>                                                                                             | <span data-ttu-id="14126-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14126-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="14126-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14126-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="14126-122">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="14126-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="14126-123"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="14126-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="14126-124">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="14126-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="14126-125"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="14126-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="14126-126">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="14126-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="14126-127"><dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="14126-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="14126-128">Das SHA wurde nicht bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="14126-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="14126-129"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="14126-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="14126-130">Der NAPAgent wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="14126-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="14126-131">Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.</span><span class="sxs-lookup"><span data-stu-id="14126-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14126-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14126-132">Remarks</span></span>

<span data-ttu-id="14126-133">Der SHA muss die [**isolationinfoex**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) -Struktur durch Aufrufen von [**freeisolationinfoex**](freeisolationinfoex.md)freigeben.</span><span class="sxs-lookup"><span data-stu-id="14126-133">The SHA must free the [**IsolationInfoEx**](/windows/win32/api/naptypes/ns-naptypes-isolationinfoex) structure by calling [**FreeIsolationInfoEx**](freeisolationinfoex.md).</span></span>

<span data-ttu-id="14126-134">Das SHA muss [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) aufrufen, bevor diese Methode oder eine andere Methode der [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="14126-134">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="14126-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14126-135">Requirements</span></span>



| <span data-ttu-id="14126-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14126-136">Requirement</span></span> | <span data-ttu-id="14126-137">Wert</span><span class="sxs-lookup"><span data-stu-id="14126-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14126-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="14126-138">Minimum supported client</span></span><br/> | <span data-ttu-id="14126-139">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14126-139">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="14126-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="14126-140">Minimum supported server</span></span><br/> | <span data-ttu-id="14126-141">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="14126-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="14126-142">Header</span><span class="sxs-lookup"><span data-stu-id="14126-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="14126-143"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="14126-143"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="14126-144">IDL</span><span class="sxs-lookup"><span data-stu-id="14126-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="14126-145"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="14126-145"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="14126-146">DLL</span><span class="sxs-lookup"><span data-stu-id="14126-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="14126-147"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="14126-147"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="14126-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14126-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14126-149">**INapSystemHealthAgentBinding2**</span><span class="sxs-lookup"><span data-stu-id="14126-149">**INapSystemHealthAgentBinding2**</span></span>](inapsystemhealthagentbinding2.md)
</dt> </dl>

 

 





