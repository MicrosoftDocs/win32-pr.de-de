---
title: Inapsystemhealthagentrequest-setsohrequest-Methode (napsystemhealthagent. h)
description: Wird von Integritäts-Agents zum Schreiben der SoH-Anforderung verwendet, die sich aus dem Aufrufen von "inapsystemhealthagentcallback getsohrequest" ergibt.
ms.assetid: 76471cf2-e5df-4e07-b872-ccac0fd45998
keywords:
- Setsohrequest-Methode NAP
- Setsohrequest-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, setsohrequest-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.SetSoHRequest
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be0fd1dcccad2a402d8455bcdf4f66052d41160b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337312"
---
# <a name="inapsystemhealthagentrequestsetsohrequest-method"></a><span data-ttu-id="9431b-106">Inapsystemhealthagentrequest:: setsohrequest-Methode</span><span class="sxs-lookup"><span data-stu-id="9431b-106">INapSystemHealthAgentRequest::SetSoHRequest method</span></span>

> [!Note]  
> <span data-ttu-id="9431b-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9431b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="9431b-108">Die **inapsystemhealthagentrequest:: setsohrequest** -Methode wird von Health-Agents verwendet, um Ihre SoH-Anforderung zu schreiben, die sich aus dem Aufrufen von [**inapsystemhealthagentcallback:: getsohrequest**](inapsystemhealthagentcallback-getsohrequest-method.md)ergibt.</span><span class="sxs-lookup"><span data-stu-id="9431b-108">The **INapSystemHealthAgentRequest::SetSoHRequest** method is used by health agents to write their SoH request resulting from the call to [**INapSystemHealthAgentCallback::GetSoHRequest**](inapsystemhealthagentcallback-getsohrequest-method.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9431b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9431b-109">Syntax</span></span>


```C++
HRESULT SetSoHRequest(
  [in] const SoHRequest *sohRequest,
  [in]       BOOL       cacheSohForLaterUse
);
```



## <a name="parameters"></a><span data-ttu-id="9431b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9431b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9431b-111">*sohrequest* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9431b-111">*sohRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9431b-112">Ein Zeiger auf ein [**sohrequest**](/windows/win32/api/naptypes/ns-naptypes-soh) -Paket.</span><span class="sxs-lookup"><span data-stu-id="9431b-112">A pointer to a [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) packet.</span></span>

</dd> <dt>

<span data-ttu-id="9431b-113">*cachesohforlateral use* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9431b-113">*cacheSohForLaterUse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9431b-114">Ein **boolescher** Wert, der **true** ist, wenn der NAPAgent das [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) zwischenspeichern soll, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9431b-114">A **BOOL** that is **TRUE** if the NapAgent should cache the [**SoH**](/windows/win32/api/naptypes/ns-naptypes-soh) and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9431b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9431b-115">Return value</span></span>

<span data-ttu-id="9431b-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9431b-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="9431b-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9431b-117">Return code</span></span>                                                                                     | <span data-ttu-id="9431b-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9431b-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9431b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9431b-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="9431b-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="9431b-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="9431b-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="9431b-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="9431b-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="9431b-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="9431b-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="9431b-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="9431b-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="9431b-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9431b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9431b-125">Requirements</span></span>



| <span data-ttu-id="9431b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9431b-126">Requirement</span></span> | <span data-ttu-id="9431b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9431b-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9431b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9431b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9431b-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9431b-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9431b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9431b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9431b-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9431b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9431b-132">Header</span><span class="sxs-lookup"><span data-stu-id="9431b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9431b-133"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="9431b-133"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="9431b-134">IDL</span><span class="sxs-lookup"><span data-stu-id="9431b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9431b-135"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9431b-135"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="9431b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="9431b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9431b-137"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9431b-137"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="9431b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9431b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9431b-139">**Inapsystemhealthagentrequest**</span><span class="sxs-lookup"><span data-stu-id="9431b-139">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





