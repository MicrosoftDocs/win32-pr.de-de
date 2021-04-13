---
title: 'IDeliveryOptimizationJob2:: GetProperty-Methode'
description: Gibt eine einzelne Eigenschaft des Do-Auftrags zurück.
keywords:
- GetProperty-Methode
- GetProperty-Methode, IDeliveryOptimizationJob2-Schnittstelle
- IDeliveryOptimizationJob2-Schnittstelle, GetProperty-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationJob2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 52e405685534c0dbae7c8c205dc5e114a3dbe68b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475933"
---
# <a name="ideliveryoptimizationjob2getproperty-method"></a><span data-ttu-id="3033d-106">IDeliveryOptimizationJob2:: GetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="3033d-106">IDeliveryOptimizationJob2::GetProperty method</span></span>

<span data-ttu-id="3033d-107">Diese Methode gibt eine einzelne Eigenschaft des Do-Auftrags zurück.</span><span class="sxs-lookup"><span data-stu-id="3033d-107">This method returns a single property of the DO job.</span></span>

## <a name="syntax"></a><span data-ttu-id="3033d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3033d-108">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOJobPropertyId propId,
  [out] VARIANT         *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="3033d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3033d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3033d-110">*PROPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="3033d-110">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3033d-111">Die erforderliche Eigenschafts-ID, die erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="3033d-111">The required property ID to get.</span></span> <span data-ttu-id="3033d-112">Nur **DOJobPropertyId_ExtendedErrorInfo** vom Typ VT_BSTR wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3033d-112">Only **DOJobPropertyId_ExtendedErrorInfo** of type VT_BSTR is supported.</span></span>

</dd> <dt>

<span data-ttu-id="3033d-113">*propvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3033d-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3033d-114">Der resultierende Eigenschafts Wert, der in einem Variant-Typ gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="3033d-114">The resultant property value, stored in a VARIANT type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3033d-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3033d-115">Return value</span></span>

<span data-ttu-id="3033d-116">Diese Methode gibt die folgenden HRESULT-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="3033d-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="3033d-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="3033d-117">Return code</span></span>                  | <span data-ttu-id="3033d-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3033d-118">Description</span></span>          |
|------------------------------|----------------------|
| <span data-ttu-id="3033d-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="3033d-119">**S_OK**</span></span>                     | <span data-ttu-id="3033d-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="3033d-120">Success</span></span>              |
| <span data-ttu-id="3033d-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="3033d-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="3033d-122">Unbekannte eigen schafts-ID.</span><span class="sxs-lookup"><span data-stu-id="3033d-122">Unknown property ID.</span></span> |

## <a name="requirements"></a><span data-ttu-id="3033d-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3033d-123">Requirements</span></span>

| <span data-ttu-id="3033d-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3033d-124">Requirement</span></span> | <span data-ttu-id="3033d-125">Wert</span><span class="sxs-lookup"><span data-stu-id="3033d-125">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3033d-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3033d-126">Minimum supported client</span></span>  | <span data-ttu-id="3033d-127">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3033d-127">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="3033d-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3033d-128">Minimum supported server</span></span>  | <span data-ttu-id="3033d-129">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3033d-129">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="3033d-130">Header</span><span class="sxs-lookup"><span data-stu-id="3033d-130">Header</span></span>                    | <span data-ttu-id="3033d-131">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="3033d-131">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="3033d-132">IDL</span><span class="sxs-lookup"><span data-stu-id="3033d-132">IDL</span></span>                       | <span data-ttu-id="3033d-133">Deliveryoptimization. idl</span><span class="sxs-lookup"><span data-stu-id="3033d-133">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="3033d-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3033d-134">Library</span></span>                   | <span data-ttu-id="3033d-135">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="3033d-135">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="3033d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="3033d-136">DLL</span></span>                       | <span data-ttu-id="3033d-137">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="3033d-137">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="3033d-138">IID</span><span class="sxs-lookup"><span data-stu-id="3033d-138">IID</span></span>                       | <span data-ttu-id="3033d-139">IID_IDeliveryOptimizationJob2 ist als 18995a26-BF 59-4abe-9B-d5092d5a2405 definiert.</span><span class="sxs-lookup"><span data-stu-id="3033d-139">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="3033d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3033d-140">See also</span></span>

[<span data-ttu-id="3033d-141">**IDeliveryOptimizationJob2**</span><span class="sxs-lookup"><span data-stu-id="3033d-141">**IDeliveryOptimizationJob2**</span></span>](ideliveryoptimizationjob2.md)
