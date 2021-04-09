---
title: Ibackgroundcopyjob Resume-Methode (deliveryoptimization. h)
description: Aktiviert einen neuen Auftrag oder startet einen Auftrag, der angehalten wurde, neu.
ms.assetid: B745BDA6-36B9-41FD-9737-61D14150A9E4
keywords:
- Resume-Methode
- Resume-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, Resume-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Resume
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f87f5b5347785810d84331ce56f240cd1f016383
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103242"
---
# <a name="ibackgroundcopyjobresume-method"></a><span data-ttu-id="500b9-106">Ibackgroundcopyjob:: Resume-Methode</span><span class="sxs-lookup"><span data-stu-id="500b9-106">IBackgroundCopyJob::Resume method</span></span>

<span data-ttu-id="500b9-107">Aktiviert einen neuen Auftrag oder startet einen Auftrag, der angehalten wurde, neu.</span><span class="sxs-lookup"><span data-stu-id="500b9-107">Activates a new job or restarts a job that has been suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="500b9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="500b9-108">Syntax</span></span>


```C++
HRESULT Resume();
```



## <a name="parameters"></a><span data-ttu-id="500b9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="500b9-109">Parameters</span></span>

<span data-ttu-id="500b9-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="500b9-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="500b9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="500b9-111">Return value</span></span>

<span data-ttu-id="500b9-112">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="500b9-112">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="500b9-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="500b9-113">Return code</span></span>                                                                                          | <span data-ttu-id="500b9-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="500b9-114">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="500b9-115"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="500b9-115"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="500b9-116">Der Auftrag wurde erfolgreich neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="500b9-116">Job was successfully restarted.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="500b9-117"><dt>**DO_E_EMPTY**</dt></span><span class="sxs-lookup"><span data-stu-id="500b9-117"><dt>**DO_E_EMPTY**</dt></span></span> </dl>          | <span data-ttu-id="500b9-118">Es sind keine zu übertragenden Dateien vorhanden.</span><span class="sxs-lookup"><span data-stu-id="500b9-118">There are no files to transfer.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="500b9-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="500b9-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="500b9-120">Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED sein.</span><span class="sxs-lookup"><span data-stu-id="500b9-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="500b9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="500b9-121">Remarks</span></span>

<span data-ttu-id="500b9-122">Wenn Sie einen Auftrag erstellen, wird der Auftrag anfänglich angehalten.</span><span class="sxs-lookup"><span data-stu-id="500b9-122">When you create a job, the job is initially suspended.</span></span> <span data-ttu-id="500b9-123">Durch Aufrufen von **Resume** wird der Auftrag in den Übertragungs Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="500b9-123">Calling **Resume** moves the job to the Transferring state.</span></span> <span data-ttu-id="500b9-124">Beachten Sie, dass der Auftrag vor dem Aufrufen dieser Methode eine oder mehrere Dateien enthalten muss.</span><span class="sxs-lookup"><span data-stu-id="500b9-124">Note that the job must contain one or more files before calling this method.</span></span>

<span data-ttu-id="500b9-125">Wenn ein Auftrag im Status BG_JOB_STATE_TRANSIENT_ERROR oder BG_JOB_STATE_ERROR ist, wird die **Resume** -Methode aufgerufen, um den Auftrag neu zu starten, nachdem Sie den Fehler behoben haben.</span><span class="sxs-lookup"><span data-stu-id="500b9-125">If a job that is in the BG_JOB_STATE_TRANSIENT_ERROR or BG_JOB_STATE_ERROR state, call the **Resume** method to restart the job after you fix the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="500b9-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="500b9-126">Requirements</span></span>



| <span data-ttu-id="500b9-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="500b9-127">Requirement</span></span> | <span data-ttu-id="500b9-128">Wert</span><span class="sxs-lookup"><span data-stu-id="500b9-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="500b9-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="500b9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="500b9-130">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="500b9-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="500b9-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="500b9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="500b9-132">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="500b9-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="500b9-133">Header</span><span class="sxs-lookup"><span data-stu-id="500b9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="500b9-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="500b9-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="500b9-135">IDL</span><span class="sxs-lookup"><span data-stu-id="500b9-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="500b9-136"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="500b9-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="500b9-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="500b9-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="500b9-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="500b9-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="500b9-139">DLL</span><span class="sxs-lookup"><span data-stu-id="500b9-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="500b9-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="500b9-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="500b9-141">IID</span><span class="sxs-lookup"><span data-stu-id="500b9-141">IID</span></span><br/>                      | <span data-ttu-id="500b9-142">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="500b9-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="500b9-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="500b9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="500b9-144">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="500b9-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="500b9-145">**Ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="500b9-145">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="500b9-146">**Ibackgroundcopyjob:: Suspend**</span><span class="sxs-lookup"><span data-stu-id="500b9-146">**IBackgroundCopyJob::Suspend**</span></span>](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





