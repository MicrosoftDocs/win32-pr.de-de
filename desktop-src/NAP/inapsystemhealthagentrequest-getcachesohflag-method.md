---
title: Inapsystemhealthagentrequest getcachesohflag-Methode (napsystemhealthagent. h)
description: Wird nur von NAPAgent verwendet.
ms.assetid: 97dd4e95-30c2-48e2-9359-b1019299581d
keywords:
- Getcachesohflag-Methode NAP
- Getcachesohflag-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, getcachesohflag-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCacheSoHFlag
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53d8b458e4a49b690fe1f0f53482a72dd253c7c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518419"
---
# <a name="inapsystemhealthagentrequestgetcachesohflag-method"></a><span data-ttu-id="41b42-106">Inapsystemhealthagentrequest:: getcachesohflag-Methode</span><span class="sxs-lookup"><span data-stu-id="41b42-106">INapSystemHealthAgentRequest::GetCacheSoHFlag method</span></span>

> [!Note]  
> <span data-ttu-id="41b42-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="41b42-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="41b42-108">Die **inapsystemhealthagentrequest:: getcachesohflag** -Methode wird nur von NAPAgent verwendet.</span><span class="sxs-lookup"><span data-stu-id="41b42-108">The **INapSystemHealthAgentRequest::GetCacheSoHFlag** method is used only by the NapAgent.</span></span>

## <a name="syntax"></a><span data-ttu-id="41b42-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="41b42-109">Syntax</span></span>


```C++
HRESULT GetCacheSoHFlag(
   BOOL *cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="41b42-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="41b42-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41b42-111">*cachesohforlateral use*</span><span class="sxs-lookup"><span data-stu-id="41b42-111">*cacheSohForLaterUse*</span></span> 
</dt> <dd>

<span data-ttu-id="41b42-112">Ein **boolescher** Wert, der **true** ist, wenn der NAPAgent das [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) zwischenspeichern soll, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="41b42-112">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41b42-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41b42-113">Return value</span></span>

<span data-ttu-id="41b42-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="41b42-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="41b42-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="41b42-115">Return code</span></span>                                                                                     | <span data-ttu-id="41b42-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="41b42-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="41b42-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="41b42-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="41b42-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="41b42-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="41b42-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="41b42-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="41b42-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="41b42-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="41b42-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="41b42-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="41b42-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="41b42-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="41b42-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41b42-123">Requirements</span></span>



| <span data-ttu-id="41b42-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41b42-124">Requirement</span></span> | <span data-ttu-id="41b42-125">Wert</span><span class="sxs-lookup"><span data-stu-id="41b42-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41b42-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41b42-126">Minimum supported client</span></span><br/> | <span data-ttu-id="41b42-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41b42-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="41b42-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41b42-128">Minimum supported server</span></span><br/> | <span data-ttu-id="41b42-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41b42-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="41b42-130">Header</span><span class="sxs-lookup"><span data-stu-id="41b42-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="41b42-131"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="41b42-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="41b42-132">IDL</span><span class="sxs-lookup"><span data-stu-id="41b42-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="41b42-133"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="41b42-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="41b42-134">DLL</span><span class="sxs-lookup"><span data-stu-id="41b42-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="41b42-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="41b42-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="41b42-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41b42-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41b42-137">**Inapsystemhealthagentrequest**</span><span class="sxs-lookup"><span data-stu-id="41b42-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





