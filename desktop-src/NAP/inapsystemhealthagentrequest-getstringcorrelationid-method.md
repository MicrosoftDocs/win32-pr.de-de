---
title: Inapsystemhealthagentrequest getstringcorrelationid-Methode (napsystemhealthagent. h)
description: Wird von Systemintegritäts-Agents zum Protokollieren der Korrelations-ID verwendet.
ms.assetid: 5d6f2392-2ada-474a-b150-31e0583c2ea7
keywords:
- Getstringcorrelationid-Methode NAP
- Getstringcorrelationid-Methode NAP, inapsystemhealthagentrequest-Schnittstelle
- Inapsystemhealthagentrequest-Schnittstelle NAP, getstringcorrelationid-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthAgentRequest.GetStringCorrelationId
api_location:
- qagentrt.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f33e98ae4b0fd76d97e85fb3588bcd1f2d33fd2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740905"
---
# <a name="inapsystemhealthagentrequestgetstringcorrelationid-method"></a><span data-ttu-id="80efa-106">Inapsystemhealthagentrequest:: getstringcorrelationid-Methode</span><span class="sxs-lookup"><span data-stu-id="80efa-106">INapSystemHealthAgentRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="80efa-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="80efa-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="80efa-108">Die **inapsystemhealthagentrequest:: getstringcorrelationid** -Methode wird von Systemintegritäts-Agents verwendet, um die Korrelations-ID zu protokollieren.</span><span class="sxs-lookup"><span data-stu-id="80efa-108">The **INapSystemHealthAgentRequest::GetStringCorrelationId** method is used by system health agents to log the correlation ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="80efa-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="80efa-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="80efa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="80efa-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80efa-111">*correlationId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="80efa-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="80efa-112">Ein Zeiger auf einen Zeiger auf eine eindeutige [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) für diesen SoH-Austausch.</span><span class="sxs-lookup"><span data-stu-id="80efa-112">A pointer to a pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for this SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80efa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80efa-113">Return value</span></span>

<span data-ttu-id="80efa-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="80efa-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="80efa-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="80efa-115">Return code</span></span>                                                                                     | <span data-ttu-id="80efa-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80efa-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="80efa-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="80efa-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="80efa-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="80efa-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="80efa-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="80efa-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="80efa-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="80efa-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="80efa-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="80efa-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="80efa-123">Requirements</span></span>



| <span data-ttu-id="80efa-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="80efa-124">Requirement</span></span> | <span data-ttu-id="80efa-125">Wert</span><span class="sxs-lookup"><span data-stu-id="80efa-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="80efa-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="80efa-126">Minimum supported client</span></span><br/> | <span data-ttu-id="80efa-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80efa-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="80efa-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="80efa-128">Minimum supported server</span></span><br/> | <span data-ttu-id="80efa-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="80efa-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="80efa-130">Header</span><span class="sxs-lookup"><span data-stu-id="80efa-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="80efa-131"><dt>Napsystemhealthagent. h</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-131"><dt>NapSystemHealthAgent.h</dt></span></span> </dl>   |
| <span data-ttu-id="80efa-132">IDL</span><span class="sxs-lookup"><span data-stu-id="80efa-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80efa-133"><dt>Napsystemhealthagent. idl</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-133"><dt>NapSystemHealthAgent.idl</dt></span></span> </dl> |
| <span data-ttu-id="80efa-134">DLL</span><span class="sxs-lookup"><span data-stu-id="80efa-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80efa-135"><dt>Qagentrt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80efa-135"><dt>Qagentrt.dll</dt></span></span> </dl>             |



## <a name="see-also"></a><span data-ttu-id="80efa-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80efa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80efa-137">**Inapsystemhealthagentrequest**</span><span class="sxs-lookup"><span data-stu-id="80efa-137">**INapSystemHealthAgentRequest**</span></span>](inapsystemhealthagentrequest.md)
</dt> </dl>

 

 





