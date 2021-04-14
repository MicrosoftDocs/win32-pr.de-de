---
title: Inapsystemhealthvalidationrequest getcorrelationid-Methode (napsystemhealthvalidator. h)
description: Wird von System Integritätsprüfungen (SHVs) verwendet, um die Korrelations-ID abzurufen. Der SHV muss diese Informationen dann protokollieren.
ms.assetid: 72603d24-219e-4bb0-9b2b-b58d42939da8
keywords:
- Getcorrelationid-Methode NAP
- Getcorrelationid-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, getcorrelationid-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1095a2c3eec90ff33613b6d37b43f31fdabd107
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476467"
---
# <a name="inapsystemhealthvalidationrequestgetcorrelationid-method"></a><span data-ttu-id="d8be9-107">Inapsystemhealthvalidationrequest:: getcorrelationid-Methode</span><span class="sxs-lookup"><span data-stu-id="d8be9-107">INapSystemHealthValidationRequest::GetCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="d8be9-108">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="d8be9-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="d8be9-109">Die **inapsystemhealthvalidationrequest:: getcorrelationid** -Methode wird von System Integritätsprüfungen (SHVs) verwendet, um die Korrelations-ID abzurufen.</span><span class="sxs-lookup"><span data-stu-id="d8be9-109">The **INapSystemHealthValidationRequest::GetCorrelationId** method is used by System Health Validators (SHVs) to retrieve the correlation ID.</span></span> <span data-ttu-id="d8be9-110">Der SHV muss diese Informationen dann protokollieren.</span><span class="sxs-lookup"><span data-stu-id="d8be9-110">The SHV must then log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8be9-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8be9-111">Syntax</span></span>


```C++
HRESULT GetCorrelationId(
  [out] CorrelationId *correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="d8be9-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8be9-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8be9-113">*correlationId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d8be9-113">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8be9-114">Ein Zeiger auf eine eindeutige [**correlationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) für den SoH-Austausch.</span><span class="sxs-lookup"><span data-stu-id="d8be9-114">A pointer to a unique [**CorrelationId**](/windows/win32/api/naptypes/ns-naptypes-correlationid) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8be9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8be9-115">Return value</span></span>

<span data-ttu-id="d8be9-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d8be9-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="d8be9-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d8be9-117">Return code</span></span>                                                                                     | <span data-ttu-id="d8be9-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8be9-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8be9-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d8be9-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="d8be9-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="d8be9-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="d8be9-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="d8be9-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="d8be9-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="d8be9-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="d8be9-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="d8be9-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="d8be9-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d8be9-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d8be9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8be9-125">Requirements</span></span>



| <span data-ttu-id="d8be9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8be9-126">Requirement</span></span> | <span data-ttu-id="d8be9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d8be9-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8be9-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8be9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d8be9-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d8be9-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="d8be9-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8be9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d8be9-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8be9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d8be9-132">Header</span><span class="sxs-lookup"><span data-stu-id="d8be9-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8be9-133"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8be9-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8be9-134">IDL</span><span class="sxs-lookup"><span data-stu-id="d8be9-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8be9-135"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8be9-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="d8be9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="d8be9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8be9-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8be9-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="d8be9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8be9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8be9-139">**Inapsystemhealthvalidationrequest**</span><span class="sxs-lookup"><span data-stu-id="d8be9-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





