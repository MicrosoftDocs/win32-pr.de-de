---
title: Inapsystemhealthagentbinding getsystemsolationinfo-Methode (napsystemhealthagent. h)
description: Wird von SHAs aufgerufen, um den systemisolations Status zu bestimmen.
ms.assetid: 0401a846-0da2-4975-87bc-3e9fe8b5b67d
keywords:
- Getsystemisolationinfo-Methode NAP
- Getsystemsolationinfo-Methode NAP, inapsystemhealthagentbinding-Schnittstelle
- Inapsystemhealthagentbinding-Schnittstelle NAP, getsystemsolationinfo-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentBinding.GetSystemIsolationInfo
api_location:
- qagent.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0323149be50cd8896a191ca57584cea0c015487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479047"
---
# <a name="inapsystemhealthagentbindinggetsystemisolationinfo-method"></a><span data-ttu-id="a7ab3-106">Inapsystemhealthagentbinding:: getsystemsolationinfo-Methode</span><span class="sxs-lookup"><span data-stu-id="a7ab3-106">INapSystemHealthAgentBinding::GetSystemIsolationInfo method</span></span>

> [!Note]  
> <span data-ttu-id="a7ab3-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="a7ab3-108">Die **inapsystemhealthagentbinding:: getsystemsolationinfo** -Methode wird von SHAs aufgerufen, um den systemisolations Status zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-108">The **INapSystemHealthAgentBinding::GetSystemIsolationInfo** method is called by SHAs to determine the system isolation state.</span></span>

> [!Note]  
> <span data-ttu-id="a7ab3-109">Verwenden Sie [**INapSystemHealthAgentBinding2:: getsystemsolationinfoex**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) , um den erweiterten Isolations Status des Systems zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-109">Use [**INapSystemHealthAgentBinding2::GetSystemIsolationInfoEx**](inapsystemhealthagentbinding2-getsystemisolationinfoex.md) in order to determine the extended isolation state of the system.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="a7ab3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7ab3-110">Syntax</span></span>


```C++
HRESULT GetSystemIsolationInfo(
  [out] IsolationInfo **isolationInfo,
  [out] BOOL          *unknownConnections
);
```



## <a name="parameters"></a><span data-ttu-id="a7ab3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7ab3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7ab3-112">*IsolationInfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7ab3-112">*isolationInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ab3-113">Ein Zeiger auf einen Zeiger auf eine [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) -Struktur, die den Isolations Zustand des Systems für bekannte Verbindungen enthält.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-113">A pointer to a pointer to an [**IsolationInfo**](/windows/win32/api/naptypes/ns-naptypes-isolationinfo) structure that contains the isolation state of the system for known connections.</span></span> <span data-ttu-id="a7ab3-114">*isolationinfoweist darauf hin* , dass sich das System im Zustand eingeschränkten Zugriffs, Bewährung oder uneingeschränkten Zugriffs befindet.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-114">*isolationInfoindicates* if the system is in a state of restricted access, probation, or unrestricted access.</span></span>

</dd> <dt>

<span data-ttu-id="a7ab3-115">*unknownconnections* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a7ab3-115">*unknownConnections* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7ab3-116">Ein Zeiger auf einen **booleschen** Wert, der **true** ist, wenn sich Verbindungen in einem unbekannten Zustand befinden, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="a7ab3-116">A pointer to a **BOOL** that is **TRUE** if any connections are in an unknown state and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7ab3-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a7ab3-117">Return value</span></span>

<span data-ttu-id="a7ab3-118">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-118">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="a7ab3-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a7ab3-119">Return code</span></span>                                                                                             | <span data-ttu-id="a7ab3-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7ab3-120">Description</span></span>                                                                                                                    |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a7ab3-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a7ab3-121"><dt>**S\_OK** </dt></span></span> </dl>                   | <span data-ttu-id="a7ab3-122">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-122">Operation succeeded.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="a7ab3-123"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="a7ab3-123"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl>         | <span data-ttu-id="a7ab3-124">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-124">Permissions error, access denied.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="a7ab3-125"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="a7ab3-125"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>          | <span data-ttu-id="a7ab3-126">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-126">System resource limit, could not perform the operation.</span></span><br/>                                                             |
| <dl> <span data-ttu-id="a7ab3-127"><dt>**NAP \_ E \_ nicht \_ Initialisiert**</dt></span><span class="sxs-lookup"><span data-stu-id="a7ab3-127"><dt>**NAP\_E\_NOT\_INITIALIZED**</dt></span></span> </dl> | <span data-ttu-id="a7ab3-128">Das SHA wurde nicht bereits initialisiert.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-128">The SHA has not been previously initialized.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="a7ab3-129"><dt>**RPC- \_ E \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="a7ab3-129"><dt>**RPC\_E\_DISCONNECTED**</dt></span></span> </dl>     | <span data-ttu-id="a7ab3-130">Der NAPAgent wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-130">The NapAgent has been stopped.</span></span> <span data-ttu-id="a7ab3-131">Dieses Objekt wird nach dem Neustart automatisch wieder hergestellt und an den NAPAgent gebunden.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-131">This object will recover automatically and rebind to the NapAgent, once it restarts.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a7ab3-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7ab3-132">Remarks</span></span>

<span data-ttu-id="a7ab3-133">Das SHA muss [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) aufrufen, bevor diese Methode oder eine andere Methode der [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) -Schnittstelle aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="a7ab3-133">The SHA must call [**Initialize**](inapsystemhealthagentbinding-initialize-method.md) before calling this method or any other method of the [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7ab3-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a7ab3-134">Requirements</span></span>



| <span data-ttu-id="a7ab3-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a7ab3-135">Requirement</span></span> | <span data-ttu-id="a7ab3-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a7ab3-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ab3-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a7ab3-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a7ab3-138">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7ab3-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a7ab3-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a7ab3-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a7ab3-140">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a7ab3-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a7ab3-141">Header</span><span class="sxs-lookup"><span data-stu-id="a7ab3-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7ab3-142"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7ab3-142"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="a7ab3-143">IDL</span><span class="sxs-lookup"><span data-stu-id="a7ab3-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a7ab3-144"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a7ab3-144"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="a7ab3-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a7ab3-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7ab3-146"><dt>Qagent.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7ab3-146"><dt>Qagent.dll</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="a7ab3-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7ab3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7ab3-148">**Inapsystemhealthagentbinding**</span><span class="sxs-lookup"><span data-stu-id="a7ab3-148">**INapSystemHealthAgentBinding**</span></span>](inapsystemhealthagentbinding.md)
</dt> </dl>

 

 





