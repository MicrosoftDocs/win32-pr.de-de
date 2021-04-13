---
title: 'IDeliveryOptimizationFile2:: GetProperty-Methode'
description: 'Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück. | IDeliveryOptimizationFile2:: GetProperty-Methode'
keywords:
- GetProperty-Methode
- GetProperty-Methode, IDeliveryOptimizationFile2-Schnittstelle
- IDeliveryOptimizationFile2-Schnittstelle, GetProperty-Methode
topic_type:
- apiref
api_name:
- IDeliveryOptimizationFile2.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 01/18/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c53167287cf821ceca26782dab9b8011d40a1785
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353728"
---
# <a name="ideliveryoptimizationfile2getproperty-method"></a><span data-ttu-id="6f4e8-107">IDeliveryOptimizationFile2:: GetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="6f4e8-107">IDeliveryOptimizationFile2::GetProperty method</span></span>

<span data-ttu-id="6f4e8-108">Diese Methode gibt eine einzelne Eigenschaft der do-Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="6f4e8-108">This method returns a single property of the DO file.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f4e8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f4e8-109">Syntax</span></span>

```C++
HRESULT GetProperty(
  [in]  DOFilePropertyId propId,
  [out] VARIANT          *propValue
);
```

## <a name="parameters"></a><span data-ttu-id="6f4e8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f4e8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f4e8-111">*PROPID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f4e8-111">*propId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4e8-112">Die erforderliche Eigenschaften-ID, die vom Typ "dofilepropertyid" erhalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f4e8-112">The required property ID to get of type DOFilePropertyId.</span></span>

</dd> <dt>

<span data-ttu-id="6f4e8-113">*propvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f4e8-113">*propValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f4e8-114">Der in einer Variante gespeicherte Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="6f4e8-114">The property value stored in a VARIANT.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f4e8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f4e8-115">Return value</span></span>

<span data-ttu-id="6f4e8-116">Diese Methode gibt die folgenden HRESULT-Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6f4e8-116">This method returns the following HRESULT values.</span></span>

| <span data-ttu-id="6f4e8-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6f4e8-117">Return code</span></span>                  | <span data-ttu-id="6f4e8-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f4e8-118">Description</span></span>                                         |
|------------------------------|-----------------------------------------------------|
| <span data-ttu-id="6f4e8-119">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="6f4e8-119">**S_OK**</span></span>                     | <span data-ttu-id="6f4e8-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="6f4e8-120">Success</span></span>                                             |
| <span data-ttu-id="6f4e8-121">**DO_E_UNKNOWN_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="6f4e8-121">**DO_E_UNKNOWN_PROPERTY_ID**</span></span> | <span data-ttu-id="6f4e8-122">Unbekannte eigen schafts-ID.</span><span class="sxs-lookup"><span data-stu-id="6f4e8-122">Unknown property ID.</span></span>                                |
| <span data-ttu-id="6f4e8-123">**DO_E_WRITE_ONLY_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="6f4e8-123">**DO_E_WRITE_ONLY_PROPERTY**</span></span> | <span data-ttu-id="6f4e8-124">Die Eigenschaft ist schreibgeschützt und kann nicht gelesen werden.</span><span class="sxs-lookup"><span data-stu-id="6f4e8-124">The property is Write only and cannot be read.</span></span>      |
| <span data-ttu-id="6f4e8-125">**E_NOT_SET**</span><span class="sxs-lookup"><span data-stu-id="6f4e8-125">**E_NOT_SET**</span></span>                | <span data-ttu-id="6f4e8-126">Mit der SetProperty-Methode wurde keine Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6f4e8-126">No property was set through the SetProperty method.</span></span> |
| <span data-ttu-id="6f4e8-127">**E_OUTOFMEMORY**</span><span class="sxs-lookup"><span data-stu-id="6f4e8-127">**E_OUTOFMEMORY**</span></span>            |  <span data-ttu-id="6f4e8-128">Fehler bei der Speicher Belegung</span><span class="sxs-lookup"><span data-stu-id="6f4e8-128">Memory allocation failure</span></span>                          |

## <a name="requirements"></a><span data-ttu-id="6f4e8-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f4e8-129">Requirements</span></span>

| <span data-ttu-id="6f4e8-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f4e8-130">Requirement</span></span> | <span data-ttu-id="6f4e8-131">Wert</span><span class="sxs-lookup"><span data-stu-id="6f4e8-131">Value</span></span> |
|---------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6f4e8-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f4e8-132">Minimum supported client</span></span>  | <span data-ttu-id="6f4e8-133">Windows 10, Version 1803, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f4e8-133">Windows 10, version 1803 \[desktop apps only\]</span></span>                                   |
| <span data-ttu-id="6f4e8-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f4e8-134">Minimum supported server</span></span>  | <span data-ttu-id="6f4e8-135">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f4e8-135">Windows Server, version 1709 \[desktop apps only\]</span></span>                               |
| <span data-ttu-id="6f4e8-136">Header</span><span class="sxs-lookup"><span data-stu-id="6f4e8-136">Header</span></span>                    | <span data-ttu-id="6f4e8-137">Deliveryoptimization. h</span><span class="sxs-lookup"><span data-stu-id="6f4e8-137">Deliveryoptimization.h</span></span>                                                           |
| <span data-ttu-id="6f4e8-138">IDL</span><span class="sxs-lookup"><span data-stu-id="6f4e8-138">IDL</span></span>                       | <span data-ttu-id="6f4e8-139">Deliveryoptimization. idl</span><span class="sxs-lookup"><span data-stu-id="6f4e8-139">DeliveryOptimization.idl</span></span>                                                         |
| <span data-ttu-id="6f4e8-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f4e8-140">Library</span></span>                   | <span data-ttu-id="6f4e8-141">Dosvc. lib</span><span class="sxs-lookup"><span data-stu-id="6f4e8-141">Dosvc.lib</span></span>                                                                        |
| <span data-ttu-id="6f4e8-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6f4e8-142">DLL</span></span>                       | <span data-ttu-id="6f4e8-143">Dosvc.dll</span><span class="sxs-lookup"><span data-stu-id="6f4e8-143">Dosvc.dll</span></span>                                                                        |
| <span data-ttu-id="6f4e8-144">IID</span><span class="sxs-lookup"><span data-stu-id="6f4e8-144">IID</span></span>                       | <span data-ttu-id="6f4e8-145">IID_IDeliveryOptimizationJob2 ist als 18995a26-BF 59-4abe-9B-d5092d5a2405 definiert.</span><span class="sxs-lookup"><span data-stu-id="6f4e8-145">IID_IDeliveryOptimizationJob2 is defined as 18995A26-BF59-4ABE-9F8B-D5092D5A2405</span></span> |

## <a name="see-also"></a><span data-ttu-id="6f4e8-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f4e8-146">See also</span></span>

[<span data-ttu-id="6f4e8-147">**IDeliveryOptimizationFile2**</span><span class="sxs-lookup"><span data-stu-id="6f4e8-147">**IDeliveryOptimizationFile2**</span></span>](ideliveryoptimizationfile2.md)
