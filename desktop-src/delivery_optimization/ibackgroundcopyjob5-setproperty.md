---
title: IBackgroundCopyJob5 SetProperty-Methode (deliveryoptimization. h)
description: Eine generische Methode zum Festlegen von Auftrags Eigenschaften für die Übermittlungs Optimierung.
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty-Methode
- SetProperty-Methode, IBackgroundCopyJob5-Schnittstelle
- IBackgroundCopyJob5 Interface, SetProperty-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a3dbd1e7c66592ea959c9b1ff4f4864340c504d8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742857"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a><span data-ttu-id="18621-106">IBackgroundCopyJob5:: SetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="18621-106">IBackgroundCopyJob5::SetProperty method</span></span>

<span data-ttu-id="18621-107">Eine generische Methode zum Festlegen von Auftrags Eigenschaften für die Übermittlungs Optimierung.</span><span class="sxs-lookup"><span data-stu-id="18621-107">A generic method for setting Delivery Optimization (DO) job properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="18621-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="18621-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="18621-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="18621-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18621-110">*PropertyId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18621-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18621-111">Die ID der Eigenschaft, die festgelegt wird, als [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) Enumerationswert festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="18621-111">The ID of the property that is being set specified as a [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enum value.</span></span>

</dd> <dt>

<span data-ttu-id="18621-112">*PropertyValue* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18621-112">*PropertyValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18621-113">Der Wert der Eigenschaft, die festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="18621-113">The value of the property that is being set.</span></span> <span data-ttu-id="18621-114">Um einen Wert aufzunehmen, dessen Typ der-Eigenschaft entspricht, wird dieser Wert über die [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) Union angegeben, die aus allen bekannten Eigenschafts Typen besteht.</span><span class="sxs-lookup"><span data-stu-id="18621-114">In order to hold a value whose type is appropriate to the property, this value is specified via the [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) union that is composed of all the known property types.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18621-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="18621-115">Return value</span></span>

<span data-ttu-id="18621-116">Die-Methode gibt die folgenden Rückgabewerte zurück.</span><span class="sxs-lookup"><span data-stu-id="18621-116">The method returns the following return values.</span></span>



| <span data-ttu-id="18621-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="18621-117">Return code</span></span>                                                                          | <span data-ttu-id="18621-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="18621-118">Description</span></span>        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="18621-119"><dt>**S_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="18621-119"><dt>**S_OK**</dt></span></span> </dl> | <span data-ttu-id="18621-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="18621-120">Success</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="18621-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="18621-121">Requirements</span></span>



| <span data-ttu-id="18621-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="18621-122">Requirement</span></span> | <span data-ttu-id="18621-123">Wert</span><span class="sxs-lookup"><span data-stu-id="18621-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18621-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="18621-124">Minimum supported client</span></span><br/> | <span data-ttu-id="18621-125">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18621-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="18621-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="18621-126">Minimum supported server</span></span><br/> | <span data-ttu-id="18621-127">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="18621-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="18621-128">Header</span><span class="sxs-lookup"><span data-stu-id="18621-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="18621-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="18621-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="18621-130">IDL</span><span class="sxs-lookup"><span data-stu-id="18621-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="18621-131"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="18621-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="18621-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="18621-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="18621-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18621-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="18621-134">DLL</span><span class="sxs-lookup"><span data-stu-id="18621-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18621-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18621-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="18621-136">IID</span><span class="sxs-lookup"><span data-stu-id="18621-136">IID</span></span><br/>                      | <span data-ttu-id="18621-137">IID_IBackgroundCopyJob5 ist als E847030C-bbba-4657-AF6D-484aa42bf1fe definiert.</span><span class="sxs-lookup"><span data-stu-id="18621-137">IID_IBackgroundCopyJob5 is defined as E847030C-BBBA-4657-AF6D-484AA42BF1FE</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="18621-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18621-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18621-139">**IBackgroundCopyJob5**</span><span class="sxs-lookup"><span data-stu-id="18621-139">**IBackgroundCopyJob5**</span></span>](ibackgroundcopyjob5.md)
</dt> <dt>

[<span data-ttu-id="18621-140">**IBackgroundCopyJob5:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="18621-140">**IBackgroundCopyJob5::GetProperty**</span></span>](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





