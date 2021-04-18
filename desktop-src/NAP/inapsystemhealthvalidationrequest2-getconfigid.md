---
title: INapSystemHealthValidationRequest2 getconfigid-Methode (napsystemhealthvalidator. h)
description: Wird von den System Integritätsprüfungen (SHVs) verwendet, um die Konfigurations-ID in einer Validierungs Anforderung abzurufen.
ms.assetid: 6d5564e4-8386-444b-a859-f0c855e4ee30
keywords:
- Getconfigid-Methode NAP
- Getconfigid-Methode NAP, INapSystemHealthValidationRequest2-Schnittstelle
- INapSystemHealthValidationRequest2 Interface NAP, getconfigid-Methode
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2.GetConfigID
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3b41d2f08dc117fd28e704d607c628ec73e6ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340009"
---
# <a name="inapsystemhealthvalidationrequest2getconfigid-method"></a><span data-ttu-id="3f07d-106">INapSystemHealthValidationRequest2:: getconfigid-Methode</span><span class="sxs-lookup"><span data-stu-id="3f07d-106">INapSystemHealthValidationRequest2::GetConfigID method</span></span>

> [!Note]  
> <span data-ttu-id="3f07d-107">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="3f07d-107">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="3f07d-108">Die **INapSystemHealthValidationRequest2:: getconfigid** -Methode wird von den System Integritätsprüfungen (SHVs) verwendet, um die Konfigurations-ID in einer Validierungs Anforderung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3f07d-108">The **INapSystemHealthValidationRequest2::GetConfigId** method is used by the System Health Validators (SHVs) to retrieve the configuration ID in a validation request.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f07d-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f07d-109">Syntax</span></span>


```C++
HRESULT GetConfigID(
  [out] UINT32 *configID
) const;
```



## <a name="parameters"></a><span data-ttu-id="3f07d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f07d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f07d-111">*ConfigID* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3f07d-111">*configID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3f07d-112">Bei der Rückgabe ein Zeiger auf UInt32, der eine Konfigurations-ID des SHV enthält.</span><span class="sxs-lookup"><span data-stu-id="3f07d-112">On return, a pointer to UINT32 that contains a configuration ID of the SHV.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f07d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3f07d-113">Return value</span></span>

<span data-ttu-id="3f07d-114">Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.</span><span class="sxs-lookup"><span data-stu-id="3f07d-114">Returns one of the following error codes based on the result of this operation.</span></span>



| <span data-ttu-id="3f07d-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3f07d-115">Return code</span></span>                                                                                  | <span data-ttu-id="3f07d-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f07d-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="3f07d-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3f07d-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="3f07d-118">Vorgang erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3f07d-118">Operation successful.</span></span><br/>                |
| <dl> <span data-ttu-id="3f07d-119"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="3f07d-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="3f07d-120">Der ConfigID-Parameter war **null**.</span><span class="sxs-lookup"><span data-stu-id="3f07d-120">The configID parameter was **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="3f07d-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3f07d-121">Requirements</span></span>



| <span data-ttu-id="3f07d-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3f07d-122">Requirement</span></span> | <span data-ttu-id="3f07d-123">Wert</span><span class="sxs-lookup"><span data-stu-id="3f07d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f07d-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3f07d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3f07d-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3f07d-125">None supported</span></span><br/>                                                                               |
| <span data-ttu-id="3f07d-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3f07d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3f07d-127">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3f07d-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="3f07d-128">Header</span><span class="sxs-lookup"><span data-stu-id="3f07d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f07d-129"><dt>Napsystemhealthvalidator. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f07d-129"><dt>NapSystemHealthValidator.h</dt></span></span> </dl>   |
| <span data-ttu-id="3f07d-130">IDL</span><span class="sxs-lookup"><span data-stu-id="3f07d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3f07d-131"><dt>Napsystemhealthvalidator. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3f07d-131"><dt>NapSystemHealthValidator.idl</dt></span></span> </dl> |
| <span data-ttu-id="3f07d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="3f07d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3f07d-133"><dt>Qshvhost.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3f07d-133"><dt>Qshvhost.dll</dt></span></span> </dl>                 |



## <a name="see-also"></a><span data-ttu-id="3f07d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3f07d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f07d-135">**INapSystemHealthValidationRequest2**</span><span class="sxs-lookup"><span data-stu-id="3f07d-135">**INapSystemHealthValidationRequest2**</span></span>](inapsystemhealthvalidationrequest2.md)
</dt> </dl>

 

 





