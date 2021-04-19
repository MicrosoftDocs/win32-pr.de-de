---
title: 'IDeliveryOptimizationFile2:: SetProperty-Methode'
description: 'Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück. | IDeliveryOptimizationFile2:: SetProperty-Methode'
keywords:
- SetProperty-Methode
- SetProperty-Methode, IDeliveryOptimizationFile2-Schnittstelle
- IDeliveryOptimizationFile2 Interface, SetProperty-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 74113fca944e79e9ecba8f822f73769775631821
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106361815"
---
# <a name="ideliveryoptimizationfile2setproperty-method"></a><span data-ttu-id="97a42-107">IDeliveryOptimizationFile2:: SetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="97a42-107">IDeliveryOptimizationFile2::SetProperty method</span></span>

<span data-ttu-id="97a42-108">Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="97a42-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="97a42-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="97a42-109">Syntax</span></span>

```C++
HRESULT SetProperty(
  [in]               DOFilePropertyId propId,
  [in, unique] const VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="97a42-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="97a42-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97a42-111">*PROPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97a42-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97a42-112">Die erforderliche Eigenschaften-ID, die vom Typ "dofilepropertyid" festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="97a42-112">The required property ID to set of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="97a42-113">*propvalue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97a42-113">*propValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97a42-114">Der festzulegende Eigenschafts Wert des Typs Variant.</span><span class="sxs-lookup"><span data-stu-id="97a42-114">The property value to set, of type VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97a42-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="97a42-115">Return value</span></span>

<span data-ttu-id="97a42-116">Diese Methode gibt die folgenden HRESULT-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="97a42-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="97a42-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="97a42-117">Return code</span></span>                  | <span data-ttu-id="97a42-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97a42-118">Description</span></span>                                                        |
|------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="97a42-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="97a42-119">**S_OK**</span></span>                     | <span data-ttu-id="97a42-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="97a42-120">Success</span></span>                                                            |
| <span data-ttu-id="97a42-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="97a42-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="97a42-122">Unbekannte eigen schafts-ID</span><span class="sxs-lookup"><span data-stu-id="97a42-122">Unknown property ID</span></span>                                                |
| <span data-ttu-id="97a42-123">**DO_E_INVALID_STATE**</span><span class="sxs-lookup"><span data-stu-id="97a42-123">**DO_E_INVALID_STATE**</span></span>       | <span data-ttu-id="97a42-124">Der Auftrag befindet sich derzeit nicht in einem Zustand, der eine Eigenschafts Einstellung zulässt.</span><span class="sxs-lookup"><span data-stu-id="97a42-124">The job is not currently in a state that allows a property setting</span></span> |

## <a name="requirements"></a><span data-ttu-id="97a42-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="97a42-125">Requirements</span></span>

| <span data-ttu-id="97a42-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="97a42-126">Requirement</span></span> | <span data-ttu-id="97a42-127">Wert</span><span class="sxs-lookup"><span data-stu-id="97a42-127">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="97a42-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="97a42-128">Minimum supported client</span></span>  | <span data-ttu-id="97a42-129">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97a42-129">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="97a42-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="97a42-130">Minimum supported server</span></span>  | <span data-ttu-id="97a42-131">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="97a42-131">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="97a42-132">Header</span><span class="sxs-lookup"><span data-stu-id="97a42-132">Header</span></span>                    | <span data-ttu-id="97a42-133">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="97a42-133">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="97a42-134">IDL</span><span class="sxs-lookup"><span data-stu-id="97a42-134">IDL</span></span>                       | <span data-ttu-id="97a42-135">Deliveryoptimization. idl</span><span class="sxs-lookup"><span data-stu-id="97a42-135">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="97a42-136">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="97a42-136">Library</span></span>                   | <span data-ttu-id="97a42-137">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="97a42-137">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="97a42-138">DLL</span><span class="sxs-lookup"><span data-stu-id="97a42-138">DLL</span></span>                       | <span data-ttu-id="97a42-139">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="97a42-139">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="97a42-140">IID</span><span class="sxs-lookup"><span data-stu-id="97a42-140">IID</span></span>                       | <span data-ttu-id="97a42-141">IID_IDeliveryOptimizationJob2 ist als 18995a26-BF 59-4abe-9B-d5092d5a2405 definiert.</span><span class="sxs-lookup"><span data-stu-id="97a42-141">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="97a42-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97a42-142">See also</span></span>

[<span data-ttu-id="97a42-143">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="97a42-143">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
