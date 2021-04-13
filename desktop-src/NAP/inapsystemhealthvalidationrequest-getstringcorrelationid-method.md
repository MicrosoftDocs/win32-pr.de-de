---
title: Inapsystemhealthvalidationrequest getstringcorrelationid-Methode (napsystemhealthvalidator. h)
description: Wird von System Integritätsprüfungen (SHVs) verwendet, von denen diese Informationen protokolliert werden müssen.
ms.assetid: c3e45857-463b-4048-a178-ec26a318b63b
keywords:
- Getstringcorrelationid-Methode NAP
- Getstringcorrelationid-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, getstringcorrelationid-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetStringCorrelationId
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 554a5a31f0aa46f6bcbd7a750662d47ab2c78040
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519167"
---
# <a name="inapsystemhealthvalidationrequestgetstringcorrelationid-method"></a><span data-ttu-id="ea0dd-106">Inapsystemhealthvalidationrequest:: getstringcorrelationid-Methode</span><span class="sxs-lookup"><span data-stu-id="ea0dd-106">INapSystemHealthValidationRequest::GetStringCorrelationId method</span></span>

> [!Note]  
> <span data-ttu-id="ea0dd-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="ea0dd-108">Die **inapsystemhealthvalidationrequest:: getstringcorrelationid** -Methode wird von System Integritätsprüfungen (SHVs) verwendet, von denen diese Informationen protokolliert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-108">The **INapSystemHealthValidationRequest::GetStringCorrelationId** method is used by System Health Validators (SHVs) which must log this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea0dd-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea0dd-109">Syntax</span></span>


```C++
HRESULT GetStringCorrelationId(
  [out] StringCorrelationId **correlationId
);
```



## <a name="parameters"></a><span data-ttu-id="ea0dd-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea0dd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea0dd-111">*correlationId* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ea0dd-111">*correlationId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ea0dd-112">Ein Zeiger auf einen Zeiger auf eine eindeutige [**stringcorrelationid**](nap-type-constants.md) für den SoH-Austausch.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-112">A pointer to a pointer to a unique [**StringCorrelationId**](nap-type-constants.md) for the SoH exchange.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea0dd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea0dd-113">Return value</span></span>

<span data-ttu-id="ea0dd-114">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-114">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="ea0dd-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ea0dd-115">Return code</span></span>                                                                                     | <span data-ttu-id="ea0dd-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ea0dd-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="ea0dd-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ea0dd-117"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="ea0dd-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-118">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="ea0dd-119"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="ea0dd-119"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="ea0dd-120">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-120">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="ea0dd-121"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ea0dd-121"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="ea0dd-122">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ea0dd-122">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ea0dd-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea0dd-123">Requirements</span></span>



| <span data-ttu-id="ea0dd-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea0dd-124">Requirement</span></span> | <span data-ttu-id="ea0dd-125">Wert</span><span class="sxs-lookup"><span data-stu-id="ea0dd-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea0dd-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea0dd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="ea0dd-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ea0dd-127">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="ea0dd-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea0dd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="ea0dd-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ea0dd-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ea0dd-130">Header</span><span class="sxs-lookup"><span data-stu-id="ea0dd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea0dd-131"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea0dd-131"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea0dd-132">IDL</span><span class="sxs-lookup"><span data-stu-id="ea0dd-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ea0dd-133"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ea0dd-133"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="ea0dd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ea0dd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea0dd-135"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea0dd-135"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="ea0dd-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea0dd-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea0dd-137">**Inapsystemhealthvalidationrequest**</span><span class="sxs-lookup"><span data-stu-id="ea0dd-137">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





