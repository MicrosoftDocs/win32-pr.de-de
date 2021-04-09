---
title: Ibackgroundcopyjob Cancel-Methode (deliveryoptimization. h)
description: Löscht den Auftrag aus der Übertragungs Warteschlange und entfernt zugehörige temporäre Dateien vom Client (Downloads) und Server (Uploads).
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Cancel-Methode
- Cancel-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, Cancel-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858836"
---
# <a name="ibackgroundcopyjobcancel-method"></a><span data-ttu-id="2a3c2-106">Ibackgroundcopyjob:: Cancel-Methode</span><span class="sxs-lookup"><span data-stu-id="2a3c2-106">IBackgroundCopyJob::Cancel method</span></span>

<span data-ttu-id="2a3c2-107">Löscht den Auftrag aus der Übertragungs Warteschlange und entfernt zugehörige temporäre Dateien vom Client (Downloads) und Server (Uploads).</span><span class="sxs-lookup"><span data-stu-id="2a3c2-107">Deletes the job from the transfer queue and removes related temporary files from the client (downloads) and server (uploads).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a3c2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a3c2-108">Syntax</span></span>


```C++
HRESULT Cancel();
```



## <a name="parameters"></a><span data-ttu-id="2a3c2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a3c2-109">Parameters</span></span>

<span data-ttu-id="2a3c2-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2a3c2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a3c2-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a3c2-111">Return value</span></span>

<span data-ttu-id="2a3c2-112">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="2a3c2-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="2a3c2-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="2a3c2-113">Return code</span></span>                                                                                          | <span data-ttu-id="2a3c2-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a3c2-114">Description</span></span>                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="2a3c2-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c2-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="2a3c2-116">Der Auftrag wurde erfolgreich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="2a3c2-116">Job was successfully canceled.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="2a3c2-117"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c2-117"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="2a3c2-118">Ein Auftrag, dessen Status BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED ist, kann nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="2a3c2-118">Cannot cancel a job whose state is BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2a3c2-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a3c2-119">Remarks</span></span>

<span data-ttu-id="2a3c2-120">Sie können einen Auftrag jederzeit abbrechen. der Auftrag kann jedoch nicht wieder hergestellt werden, nachdem er abgebrochen wurde.</span><span class="sxs-lookup"><span data-stu-id="2a3c2-120">You can cancel a job at any time; however, the job cannot be recovered after it is canceled.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a3c2-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a3c2-121">Requirements</span></span>



| <span data-ttu-id="2a3c2-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a3c2-122">Requirement</span></span> | <span data-ttu-id="2a3c2-123">Wert</span><span class="sxs-lookup"><span data-stu-id="2a3c2-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a3c2-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a3c2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2a3c2-125">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a3c2-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2a3c2-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a3c2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2a3c2-127">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a3c2-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2a3c2-128">Header</span><span class="sxs-lookup"><span data-stu-id="2a3c2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a3c2-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c2-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a3c2-130">IDL</span><span class="sxs-lookup"><span data-stu-id="2a3c2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a3c2-131"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c2-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2a3c2-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2a3c2-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a3c2-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c2-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2a3c2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="2a3c2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a3c2-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a3c2-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2a3c2-136">IID</span><span class="sxs-lookup"><span data-stu-id="2a3c2-136">IID</span></span><br/>                      | <span data-ttu-id="2a3c2-137">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="2a3c2-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2a3c2-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a3c2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a3c2-139">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="2a3c2-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="2a3c2-140">**Ibackgroundcopyjob:: Complete**</span><span class="sxs-lookup"><span data-stu-id="2a3c2-140">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="2a3c2-141">**Ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="2a3c2-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> <dt>

[<span data-ttu-id="2a3c2-142">**Ibackgroundcopyjob:: Suspend**</span><span class="sxs-lookup"><span data-stu-id="2a3c2-142">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





