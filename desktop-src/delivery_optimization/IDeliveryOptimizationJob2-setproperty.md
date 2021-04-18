---
title: 'IDeliveryOptimizationJob2:: SetProperty-Methode'
description: Diese Methode wird nicht verwendet.
keywords:
- SetProperty-Methode
- SetProperty-Methode, IDeliveryOptimizationJob2-Schnittstelle
- IDeliveryOptimizationJob2 Interface, SetProperty-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 41375ac3949dd4bcbdd22944f1f1a11d461fc3ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391971"
---
# <a name="ideliveryoptimizationjob2setproperty-method"></a><span data-ttu-id="11c06-106">IDeliveryOptimizationJob2:: SetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="11c06-106">IDeliveryOptimizationJob2::SetProperty method</span></span>

<span data-ttu-id="11c06-107">Diese Methode wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="11c06-107">This method is unused.</span></span>

## <a name="syntax"></a><span data-ttu-id="11c06-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="11c06-108">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOJobPropertyId propId,
  [in, unique] const VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="11c06-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="11c06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11c06-110">*PROPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11c06-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c06-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="11c06-111">Unused.</span></span>

</dd> <dt>

<span data-ttu-id="11c06-112">*propvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11c06-112">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11c06-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="11c06-113">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11c06-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11c06-114">Return value</span></span>

<span data-ttu-id="11c06-115">Wenn PROPID **DOJobPropertyId_ExtendedErrorInfo** ist, wird der zurückgegebene Wert **DO_E_READ_ONLY_PROPERTY**. andernfalls gibt die Funktion **DO_E_UNKNOWN_PROPERTY_ID** zurück.</span><span class="sxs-lookup"><span data-stu-id="11c06-115">If propId is **DOJobPropertyId_ExtendedErrorInfo**, the returned value is **DO_E_READ_ONLY_PROPERTY**, otherwise the function returns **DO_E_UNKNOWN_PROPERTY_ID**.</span></span>

## <a name="requirements"></a><span data-ttu-id="11c06-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11c06-116">Requirements</span></span>

| <span data-ttu-id="11c06-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11c06-117">Requirement</span></span> | <span data-ttu-id="11c06-118">Wert</span><span class="sxs-lookup"><span data-stu-id="11c06-118">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="11c06-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11c06-119">Minimum supported client</span></span>  | <span data-ttu-id="11c06-120">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11c06-120">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="11c06-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11c06-121">Minimum supported server</span></span>  | <span data-ttu-id="11c06-122">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11c06-122">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="11c06-123">Header</span><span class="sxs-lookup"><span data-stu-id="11c06-123">Header</span></span>                    | <span data-ttu-id="11c06-124">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="11c06-124">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="11c06-125">IDL</span><span class="sxs-lookup"><span data-stu-id="11c06-125">IDL</span></span>                       | <span data-ttu-id="11c06-126">Deliveryoptimization. idl</span><span class="sxs-lookup"><span data-stu-id="11c06-126">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="11c06-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11c06-127">Library</span></span>                   | <span data-ttu-id="11c06-128">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="11c06-128">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="11c06-129">DLL</span><span class="sxs-lookup"><span data-stu-id="11c06-129">DLL</span></span>                       | <span data-ttu-id="11c06-130">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="11c06-130">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="11c06-131">IID</span><span class="sxs-lookup"><span data-stu-id="11c06-131">IID</span></span>                       | <span data-ttu-id="11c06-132">IID_IDeliveryOptimizationJob2 ist als 18995a26-BF 59-4abe-9B-d5092d5a2405 definiert.</span><span class="sxs-lookup"><span data-stu-id="11c06-132">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="11c06-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11c06-133">See also</span></span>

[<span data-ttu-id="11c06-134">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="11c06-134">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
