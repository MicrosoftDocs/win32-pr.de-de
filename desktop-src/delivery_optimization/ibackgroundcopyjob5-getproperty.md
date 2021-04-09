---
title: IBackgroundCopyJob5 GetProperty-Methode (deliveryoptimization. h)
description: Eine generische Methode zum erhalten von Auftrags Eigenschaften für die Übermittlungs Optimierung (Do).
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- GetProperty-Methode
- GetProperty-Methode, IBackgroundCopyJob5-Schnittstelle
- IBackgroundCopyJob5-Schnittstelle, GetProperty-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956557"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a><span data-ttu-id="4fed2-106">IBackgroundCopyJob5:: GetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="4fed2-106">IBackgroundCopyJob5::GetProperty method</span></span>

<span data-ttu-id="4fed2-107">Eine generische Methode zum erhalten von Auftrags Eigenschaften für die Übermittlungs Optimierung (Do).</span><span class="sxs-lookup"><span data-stu-id="4fed2-107">A generic method for getting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fed2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fed2-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="4fed2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fed2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fed2-110">*PropertyId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4fed2-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fed2-111">Die ID der Eigenschaft, die abgerufen wird, als [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) Enumerationswert.</span><span class="sxs-lookup"><span data-stu-id="4fed2-111">The ID of the property that is being obtained specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="4fed2-112">*ppropertyvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4fed2-112">*pPropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4fed2-113">Der Eigenschafts Wert, der als BITS_JOB_PROPERTY_VALUE Union zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4fed2-113">The property value returned as a BITS_JOB_PROPERTY_VALUE union.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4fed2-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4fed2-114">Return value</span></span>

<span data-ttu-id="4fed2-115">Die-Methode gibt die folgenden Rückgabewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="4fed2-115">The method returns the following return values.</span></span>



| <span data-ttu-id="4fed2-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="4fed2-116">Return code</span></span>                                                                          | <span data-ttu-id="4fed2-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fed2-117">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="4fed2-118"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="4fed2-118"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="4fed2-119">Erfolg</span><span class="sxs-lookup"><span data-stu-id="4fed2-119">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4fed2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4fed2-120">Requirements</span></span>



| <span data-ttu-id="4fed2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4fed2-121">Requirement</span></span> | <span data-ttu-id="4fed2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4fed2-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4fed2-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4fed2-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4fed2-124">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fed2-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4fed2-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4fed2-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4fed2-126">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4fed2-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="4fed2-127">Header</span><span class="sxs-lookup"><span data-stu-id="4fed2-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fed2-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="4fed2-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="4fed2-129">IDL</span><span class="sxs-lookup"><span data-stu-id="4fed2-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="4fed2-130"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="4fed2-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="4fed2-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4fed2-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="4fed2-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4fed2-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="4fed2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4fed2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4fed2-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4fed2-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="4fed2-135">IID</span><span class="sxs-lookup"><span data-stu-id="4fed2-135">IID</span></span><br/>                      | <span data-ttu-id="4fed2-136">IID_IBackgroundCopyJob5 ist als E847030C-bbba-4657-AF6D-484aa42bf1fe definiert.</span><span class="sxs-lookup"><span data-stu-id="4fed2-136">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="4fed2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4fed2-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4fed2-138">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="4fed2-138">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="4fed2-139">**IBackgroundCopyJob5:: SetProperty**</span><span class="sxs-lookup"><span data-stu-id="4fed2-139">**IBackgroundCopyJob5::SetProperty**</span></span>](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





