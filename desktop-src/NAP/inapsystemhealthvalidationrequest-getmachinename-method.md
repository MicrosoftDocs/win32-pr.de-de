---
title: Inapsystemhealthvalidationrequest GetMachineName-Methode (napsystemhealthvalidator. h)
description: Wird von System Integritätsprüfungen (SHVs) verwendet, um den Computernamen des NAP-Clients abzurufen. Der SHV protokolliert diese Informationen dann.
ms.assetid: 2ea6a65d-1579-4a05-b5bc-aebf6421e46a
keywords:
- GetMachineName-Methode NAP
- GetMachineName-Methode NAP, inapsystemhealthvalidationrequest-Schnittstelle
- Inapsystemhealthvalidationrequest-Schnittstelle NAP, GetMachineName-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetMachineName
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be1c3e264d7d2d6e4d93e3ad71d7f3adc92ff8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106508"
---
# <a name="inapsystemhealthvalidationrequestgetmachinename-method"></a><span data-ttu-id="2ac6b-107">Inapsystemhealthvalidationrequest:: GetMachineName-Methode</span><span class="sxs-lookup"><span data-stu-id="2ac6b-107">INapSystemHealthValidationRequest::GetMachineName method</span></span>

> [!Note]  
> <span data-ttu-id="2ac6b-108">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="2ac6b-108">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="2ac6b-109">Die **inapsystemhealthvalidationrequest:: GetMachineName** -Methode wird von System Integritätsprüfungen (SHVs) verwendet, um den Computernamen des NAP-Clients abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2ac6b-109">The **INapSystemHealthValidationRequest::GetMachineName** method is used by System Health Validators (SHVs) to retrieve the machine name of the NAP client.</span></span> <span data-ttu-id="2ac6b-110">Der SHV protokolliert diese Informationen dann.</span><span class="sxs-lookup"><span data-stu-id="2ac6b-110">The SHV then logs this information.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ac6b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="2ac6b-111">Syntax</span></span>


```C++
HRESULT GetMachineName(
  [out] CountedString **machineName
);
```



## <a name="parameters"></a><span data-ttu-id="2ac6b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2ac6b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ac6b-113">*MachineName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2ac6b-113">*machineName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ac6b-114">Ein Zeiger auf einen Zeiger auf eine [**zählstring**](/windows/win32/api/naptypes/ns-naptypes-countedstring) -Struktur, die den Computernamen des NAP-Clients enthält.</span><span class="sxs-lookup"><span data-stu-id="2ac6b-114">A pointer to a pointer to a [**CountedString**](/windows/win32/api/naptypes/ns-naptypes-countedstring) structure that contains the machine name of the NAP client.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ac6b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2ac6b-115">Return value</span></span>

<span data-ttu-id="2ac6b-116">Es können auch andere com-spezifische Fehlercodes zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2ac6b-116">Other COM-specific error codes also may be returned.</span></span>



| <span data-ttu-id="2ac6b-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2ac6b-117">Return code</span></span>                                                                                     | <span data-ttu-id="2ac6b-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2ac6b-118">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="2ac6b-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac6b-119"><dt>**S\_OK** </dt></span></span> </dl>           | <span data-ttu-id="2ac6b-120">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="2ac6b-120">Operation succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="2ac6b-121"><dt>**E \_ Access verweigert**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac6b-121"><dt>**E\_ACCESSDENIED** </dt></span></span> </dl> | <span data-ttu-id="2ac6b-122">Berechtigungs Fehler, Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="2ac6b-122">Permissions error, access denied.</span></span><br/>                       |
| <dl> <span data-ttu-id="2ac6b-123"><dt>**E \_ Outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="2ac6b-123"><dt>**E\_OUTOFMEMORY** </dt></span></span> </dl>  | <span data-ttu-id="2ac6b-124">System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2ac6b-124">System resource limit, could not perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2ac6b-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2ac6b-125">Requirements</span></span>



| <span data-ttu-id="2ac6b-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2ac6b-126">Requirement</span></span> | <span data-ttu-id="2ac6b-127">Wert</span><span class="sxs-lookup"><span data-stu-id="2ac6b-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ac6b-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2ac6b-128">Minimum supported client</span></span><br/> | <span data-ttu-id="2ac6b-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="2ac6b-129">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="2ac6b-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2ac6b-130">Minimum supported server</span></span><br/> | <span data-ttu-id="2ac6b-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2ac6b-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2ac6b-132">Header</span><span class="sxs-lookup"><span data-stu-id="2ac6b-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ac6b-133"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ac6b-133"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="2ac6b-134">IDL</span><span class="sxs-lookup"><span data-stu-id="2ac6b-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2ac6b-135"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2ac6b-135"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="2ac6b-136">DLL</span><span class="sxs-lookup"><span data-stu-id="2ac6b-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ac6b-137"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ac6b-137"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="2ac6b-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2ac6b-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ac6b-139">**Inapsystemhealthvalidationrequest**</span><span class="sxs-lookup"><span data-stu-id="2ac6b-139">**INapSystemHealthValidationRequest**</span></span>](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





