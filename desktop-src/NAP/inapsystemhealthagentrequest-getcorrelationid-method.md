---
title: Inapsystemhealthagentrequest getcorrelationid-Methode (napsystemhealthagent. h)
description: Wird von Systemintegritäts-Agents verwendet, um SoH-und SoH-Antworten zu korrelieren.
ms.assetid: 220db71a-31d7-45a7-a8e7-ddb4955d546e
keywords:
- Getcorrelationid-Methode NAP
- Getcorrelationid-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, getcorrelationid-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7af5b182df738ec22c75f2afffd1adb3591007be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519271"
---
# <a name="inapsystemhealthagentrequestgetcorrelationid-method"></a><span data-ttu-id="c2a7b-106">Inapsystemhealthagentrequest:: getcorrelationid-Methode</span><span class="sxs-lookup"><span data-stu-id="c2a7b-106">INapSystemHealthAgentRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="c2a7b-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c2a7b-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="c2a7b-108">Die **inapsystemhealthagentrequest:: getcorrelationid** -Methode wird von Systemintegritäts-Agents verwendet, um SoH-und SoH-Antworten zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="c2a7b-108">The **INapSystemHealthAgentRequest::GetCorrelationId** method is used by system health agents to correlate SoH's and SoH-Responses.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a7b-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2a7b-109">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="c2a7b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2a7b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2a7b-111">*correlationId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c2a7b-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2a7b-112">Ein Zeiger auf eine eindeutige [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) für den SoH-Austausch.</span><span class="sxs-lookup"><span data-stu-id="c2a7b-112">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2a7b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2a7b-113">Return value</span></span>

<span data-ttu-id="c2a7b-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c2a7b-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="c2a7b-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c2a7b-115">Return code</span></span>                                                                                     | <span data-ttu-id="c2a7b-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2a7b-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2a7b-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a7b-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="c2a7b-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c2a7b-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="c2a7b-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a7b-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="c2a7b-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="c2a7b-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="c2a7b-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c2a7b-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="c2a7b-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="c2a7b-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c2a7b-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2a7b-123">Requirements</span></span>



| <span data-ttu-id="c2a7b-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2a7b-124">Requirement</span></span> | <span data-ttu-id="c2a7b-125">Wert</span><span class="sxs-lookup"><span data-stu-id="c2a7b-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2a7b-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2a7b-126">Minimum supported client</span></span><br/> | <span data-ttu-id="c2a7b-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2a7b-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="c2a7b-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2a7b-128">Minimum supported server</span></span><br/> | <span data-ttu-id="c2a7b-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2a7b-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="c2a7b-130">Header</span><span class="sxs-lookup"><span data-stu-id="c2a7b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2a7b-131"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2a7b-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2a7b-132">IDL</span><span class="sxs-lookup"><span data-stu-id="c2a7b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2a7b-133"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2a7b-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="c2a7b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c2a7b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2a7b-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2a7b-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="c2a7b-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2a7b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2a7b-137">**Inapsystemhealthagentrequest**</span><span class="sxs-lookup"><span data-stu-id="c2a7b-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





