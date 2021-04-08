---
title: Ibackgroundcopyjob SetPriority-Methode (deliveryoptimization. h)
description: Gibt die Prioritätsstufe des Auftrags an. Die Prioritätsstufe bestimmt, wann der Auftrag in Bezug auf andere Aufträge in der Übertragungs Warteschlange verarbeitet wird.
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- SetPriority-Methode
- SetPriority-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, SetPriority-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6fb6407c5d693a2c6e75f8aaf8f7a0544d08cdec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741713"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a><span data-ttu-id="347ac-107">Ibackgroundcopyjob:: SetPriority-Methode</span><span class="sxs-lookup"><span data-stu-id="347ac-107">IBackgroundCopyJob::SetPriority method</span></span>

<span data-ttu-id="347ac-108">Gibt die Prioritätsstufe des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="347ac-108">Specifies the priority level of your job.</span></span> <span data-ttu-id="347ac-109">Die Prioritätsstufe bestimmt, wann der Auftrag in Bezug auf andere Aufträge in der Übertragungs Warteschlange verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="347ac-109">The priority level determines when your job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="347ac-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="347ac-110">Syntax</span></span>


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a><span data-ttu-id="347ac-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="347ac-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="347ac-112">*Priorität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="347ac-112">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="347ac-113">Gibt die Prioritätsstufe Ihres Auftrags in Relation zu anderen Aufträgen in der Übertragungs Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="347ac-113">Specifies the priority level of your job relative to other jobs in the transfer queue.</span></span> <span data-ttu-id="347ac-114">Der Standardwert ist BG_JOB_PRIORITY_NORMAL.</span><span class="sxs-lookup"><span data-stu-id="347ac-114">The default is BG_JOB_PRIORITY_NORMAL.</span></span> <span data-ttu-id="347ac-115">Eine Liste der Prioritätsstufen finden Sie in der [**BG_JOB_PRIORITY**](bg-job-priority-.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="347ac-115">For a list of priority levels, see the [**BG_JOB_PRIORITY**](bg-job-priority-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="347ac-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="347ac-116">Return value</span></span>

<span data-ttu-id="347ac-117">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="347ac-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="347ac-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="347ac-118">Return code</span></span>                                                                              | <span data-ttu-id="347ac-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="347ac-119">Description</span></span>                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="347ac-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="347ac-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="347ac-121">Die Auftrags Priorität wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="347ac-121">Job priority was successfully set.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="347ac-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="347ac-122">Requirements</span></span>



| <span data-ttu-id="347ac-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="347ac-123">Requirement</span></span> | <span data-ttu-id="347ac-124">Wert</span><span class="sxs-lookup"><span data-stu-id="347ac-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="347ac-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="347ac-125">Minimum supported client</span></span><br/> | <span data-ttu-id="347ac-126">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="347ac-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="347ac-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="347ac-127">Minimum supported server</span></span><br/> | <span data-ttu-id="347ac-128">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="347ac-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="347ac-129">Header</span><span class="sxs-lookup"><span data-stu-id="347ac-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="347ac-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="347ac-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="347ac-131">IDL</span><span class="sxs-lookup"><span data-stu-id="347ac-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="347ac-132"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="347ac-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="347ac-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="347ac-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="347ac-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="347ac-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="347ac-135">DLL</span><span class="sxs-lookup"><span data-stu-id="347ac-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="347ac-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="347ac-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="347ac-137">IID</span><span class="sxs-lookup"><span data-stu-id="347ac-137">IID</span></span><br/>                      | <span data-ttu-id="347ac-138">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="347ac-138">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="347ac-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="347ac-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="347ac-140">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="347ac-140">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="347ac-141">**BG_JOB_PRIORITY**</span><span class="sxs-lookup"><span data-stu-id="347ac-141">**BG_JOB_PRIORITY**</span></span>](bg-job-priority-.md)
</dt> <dt>

[<span data-ttu-id="347ac-142">**Ibackgroundcopyjob:: GetPriority**</span><span class="sxs-lookup"><span data-stu-id="347ac-142">**IBackgroundCopyJob::GetPriority**</span></span>](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





