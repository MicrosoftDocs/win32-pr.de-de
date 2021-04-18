---
title: Ibackgroundcopyjob GetPriority-Methode (deliveryoptimization. h)
description: Ruft die Prioritätsstufe für den Auftrag ab. Die Prioritätsstufe bestimmt, wann der Auftrag in Bezug auf andere Aufträge in der Übertragungs Warteschlange verarbeitet wird.
ms.assetid: 2F778B35-8DBB-4540-88C2-A2E18EBB0D89
keywords:
- GetPriority-Methode
- GetPriority-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetPriority-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7ae9a865045ee1264a0598a3d3c1db8cc3c3b8bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106344473"
---
# <a name="ibackgroundcopyjobgetpriority-method"></a><span data-ttu-id="0fd3f-107">Ibackgroundcopyjob:: GetPriority-Methode</span><span class="sxs-lookup"><span data-stu-id="0fd3f-107">IBackgroundCopyJob::GetPriority method</span></span>

<span data-ttu-id="0fd3f-108">Ruft die Prioritätsstufe für den Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="0fd3f-108">Retrieves the priority level for the job.</span></span> <span data-ttu-id="0fd3f-109">Die Prioritätsstufe bestimmt, wann der Auftrag in Bezug auf andere Aufträge in der Übertragungs Warteschlange verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="0fd3f-109">The priority level determines when the job is processed relative to other jobs in the transfer queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="0fd3f-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0fd3f-110">Syntax</span></span>


```C++
HRESULT GetPriority(
  [out] BG_JOB_PRIORITY *pPriority
);
```



## <a name="parameters"></a><span data-ttu-id="0fd3f-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0fd3f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0fd3f-112">*ppriority* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0fd3f-112">*pPriority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0fd3f-113">Die Priorität des Auftrags in Bezug auf andere Aufträge in der Übertragungs Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="0fd3f-113">Priority of the job relative to other jobs in the transfer queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0fd3f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0fd3f-114">Return value</span></span>

<span data-ttu-id="0fd3f-115">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="0fd3f-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="0fd3f-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0fd3f-116">Return code</span></span>                                                                              | <span data-ttu-id="0fd3f-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0fd3f-117">Description</span></span>                                           |
|------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="0fd3f-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="0fd3f-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="0fd3f-119">Die Prioritätsstufe wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0fd3f-119">Priority level was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0fd3f-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0fd3f-120">Requirements</span></span>



| <span data-ttu-id="0fd3f-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0fd3f-121">Requirement</span></span> | <span data-ttu-id="0fd3f-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0fd3f-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0fd3f-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0fd3f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0fd3f-124">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fd3f-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0fd3f-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0fd3f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0fd3f-126">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0fd3f-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0fd3f-127">Header</span><span class="sxs-lookup"><span data-stu-id="0fd3f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0fd3f-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0fd3f-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0fd3f-129">IDL</span><span class="sxs-lookup"><span data-stu-id="0fd3f-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0fd3f-130"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0fd3f-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0fd3f-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0fd3f-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="0fd3f-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0fd3f-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0fd3f-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0fd3f-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0fd3f-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0fd3f-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0fd3f-135">IID</span><span class="sxs-lookup"><span data-stu-id="0fd3f-135">IID</span></span><br/>                      | <span data-ttu-id="0fd3f-136">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="0fd3f-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0fd3f-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0fd3f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0fd3f-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="0fd3f-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="0fd3f-139">**Ibackgroundcopyjob:: SetPriority**</span><span class="sxs-lookup"><span data-stu-id="0fd3f-139">**IBackgroundCopyJob::SetPriority**</span></span>](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





