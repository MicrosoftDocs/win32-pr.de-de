---
title: BG_JOB_STATE-Enumeration (deliveryoptimization. h)
description: Die BG_JOB_STATE-Enumeration definiert konstante Werte für die verschiedenen Zustände eines Auftrags.
ms.assetid: DB4806BD-08BC-4F0B-A7F4-BA0719112811
keywords:
- BG_JOB_STATE-Enumeration
- BG_JOB_STATE-Enumeration
topic_type:
- apiref
api_name:
- BG_JOB_STATE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 113e0b1ecc995a0a452f22835ad8717041b44d10
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339539"
---
# <a name="bg_job_state-enumeration"></a><span data-ttu-id="cda5d-105">BG_JOB_STATE-Enumeration</span><span class="sxs-lookup"><span data-stu-id="cda5d-105">BG_JOB_STATE enumeration</span></span>

<span data-ttu-id="cda5d-106">Die **BG_JOB_STATE** -Enumeration definiert konstante Werte für die verschiedenen Zustände eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="cda5d-106">The **BG_JOB_STATE** enumeration defines constant values for the different states of a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="cda5d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cda5d-107">Syntax</span></span>


```C++
typedef enum  { 
  BG_JOB_STATE_QUEUED,
  BG_JOB_STATE_CONNECTING,
  BG_JOB_STATE_TRANSFERRING,
  BG_JOB_STATE_SUSPENDED,
  BG_JOB_STATE_ERROR,
  BG_JOB_STATE_TRANSIENT_ERROR,
  BG_JOB_STATE_TRANSFERRED,
  BG_JOB_STATE_ACKNOWLEDGED,
  BG_JOB_STATE_CANCELLED
} BG_JOB_STATE;
```



## <a name="constants"></a><span data-ttu-id="cda5d-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="cda5d-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="cda5d-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span><span class="sxs-lookup"><span data-stu-id="cda5d-109"><span id="BG_JOB_STATE_QUEUED"></span><span id="bg_job_state_queued"></span>**BG_JOB_STATE_QUEUED**</span></span>
</dt> <dd>

<span data-ttu-id="cda5d-110">Gibt an, dass sich der Auftrag in der Warteschlange befindet und auf die Laufzeiten wartet.</span><span class="sxs-lookup"><span data-stu-id="cda5d-110">Specifies that the job is in the queue and waiting to run.</span></span> <span data-ttu-id="cda5d-111">Wenn ein Benutzer sich abmeldet, während der Auftrag übertragen wird, wechselt der Auftrag in den Zustand "in Warteschlange".</span><span class="sxs-lookup"><span data-stu-id="cda5d-111">If a user logs off while their job is transferring, the job transitions to the queued state.</span></span>

</dd> <dt>

<span data-ttu-id="cda5d-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span><span class="sxs-lookup"><span data-stu-id="cda5d-112"><span id="BG_JOB_STATE_CONNECTING"></span><span id="bg_job_state_connecting"></span>**BG_JOB_STATE_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="cda5d-113">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cda5d-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="cda5d-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span><span class="sxs-lookup"><span data-stu-id="cda5d-114"><span id="BG_JOB_STATE_TRANSFERRING"></span><span id="bg_job_state_transferring"></span>**BG_JOB_STATE_TRANSFERRING**</span></span>
</dt> <dd>

<span data-ttu-id="cda5d-115">Gibt an, dass Daten für den Auftrag übertragen.</span><span class="sxs-lookup"><span data-stu-id="cda5d-115">Specifies that DO is transferring data for the job.</span></span>

</dd> <dt>

<span data-ttu-id="cda5d-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="cda5d-116"><span id="BG_JOB_STATE_SUSPENDED"></span><span id="bg_job_state_suspended"></span>**BG_JOB_STATE_SUSPENDED**</span></span>
</dt> <dd>

<span data-ttu-id="cda5d-117">Gibt an, dass der Auftrag angehalten wurde (angehalten).</span><span class="sxs-lookup"><span data-stu-id="cda5d-117">Specifies that the job is suspended (paused).</span></span> <span data-ttu-id="cda5d-118">Zum Aussetzen eines Auftrags wird die [**ibackgroundcopyjob:: Suspend**](ibackgroundcopyjob-suspend.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="cda5d-118">To suspend a job, call the [**IBackgroundCopyJob::Suspend**](ibackgroundcopyjob-suspend.md) method.</span></span> <span data-ttu-id="cda5d-119">Der Auftrag bleibt angehalten, bis Sie die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md)-, [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md)-Methode oder die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="cda5d-119">The job remains suspended until you call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md), [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md), or [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="cda5d-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span><span class="sxs-lookup"><span data-stu-id="cda5d-120"><span id="BG_JOB_STATE_ERROR"></span><span id="bg_job_state_error"></span>**BG_JOB_STATE_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="cda5d-121">Gibt an, dass ein nicht BEHEB barer Fehler aufgetreten ist (der Dienst kann die Datei nicht übertragen).</span><span class="sxs-lookup"><span data-stu-id="cda5d-121">Specifies that a nonrecoverable error occurred (the service is unable to transfer the file).</span></span> <span data-ttu-id="cda5d-122">Wenn der Fehler, wie z. b. der Fehler "Zugriff verweigert", korrigiert werden kann, müssen Sie die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) -Methode aufrufen, nachdem der Fehler behoben wurde.</span><span class="sxs-lookup"><span data-stu-id="cda5d-122">If the error, such as an access-denied error, can be corrected, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method after the error is fixed.</span></span> <span data-ttu-id="cda5d-123">Wenn der Fehler jedoch nicht korrigiert werden kann, rufen Sie die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode auf, um den Auftrag abzubrechen, oder rufen Sie die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode auf, um den Teil eines Download Auftrags zu akzeptieren, der erfolgreich übertragen wurde.</span><span class="sxs-lookup"><span data-stu-id="cda5d-123">However, if the error cannot be corrected, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job, or call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to accept the portion of a download job that transferred successfully.</span></span>

</dd> <dt>

<span data-ttu-id="cda5d-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span><span class="sxs-lookup"><span data-stu-id="cda5d-124"><span id="BG_JOB_STATE_TRANSIENT_ERROR"></span><span id="bg_job_state_transient_error"></span>**BG_JOB_STATE_TRANSIENT_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="cda5d-125">Gibt an, dass ein BEHEB barer Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="cda5d-125">Specifies that a recoverable error occurred.</span></span> <span data-ttu-id="cda5d-126">Führt einen Wiederholungsversuch für Aufträge im vorübergehenden Fehlerstatus basierend auf der internen Wiederholungs Konfiguration aus.</span><span class="sxs-lookup"><span data-stu-id="cda5d-126">DO will retry jobs in the transient error state based on the internal retry configuration.</span></span> <span data-ttu-id="cda5d-127">Der Status des Auftrags ändert sich in **BG_JOB_STATE_ERROR** , wenn der Auftrag nicht fortgesetzt werden kann (siehe [**ibackgroundcopyjob:: setnoprogresstimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span><span class="sxs-lookup"><span data-stu-id="cda5d-127">The state of the job changes to **BG_JOB_STATE_ERROR** if the job fails to make progress (see [**IBackgroundCopyJob::SetNoProgressTimeout**](ibackgroundcopyjob-setnoprogresstimeout.md)).</span></span>

</dd> <dt>

<span data-ttu-id="cda5d-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span><span class="sxs-lookup"><span data-stu-id="cda5d-128"><span id="BG_JOB_STATE_TRANSFERRED"></span><span id="bg_job_state_transferred"></span>**BG_JOB_STATE_TRANSFERRED**</span></span>
</dt> <dd>

<span data-ttu-id="cda5d-129">Gibt an, dass der Auftrag erfolgreich verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="cda5d-129">Specifies that your job was successfully processed.</span></span> <span data-ttu-id="cda5d-130">Sie müssen die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode anrufen, um den Abschluss des Auftrags zu bestätigen und die Dateien für den Client verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="cda5d-130">You must call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge completion of the job and to make the files available to the client.</span></span>

</dd> <dt>

<span data-ttu-id="cda5d-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span><span class="sxs-lookup"><span data-stu-id="cda5d-131"><span id="BG_JOB_STATE_ACKNOWLEDGED"></span><span id="bg_job_state_acknowledged"></span>**BG_JOB_STATE_ACKNOWLEDGED**</span></span>
</dt> <dd>

<span data-ttu-id="cda5d-132">Gibt an, dass Sie die Methode [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) aufgerufen haben, um zu bestätigen, dass der Auftrag erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="cda5d-132">Specifies that you called the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that your job completed successfully.</span></span>

</dd> <dt>

<span data-ttu-id="cda5d-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="cda5d-133"><span id="BG_JOB_STATE_CANCELLED"></span><span id="bg_job_state_cancelled"></span>**BG_JOB_STATE_CANCELLED**</span></span>
</dt> <dd>

<span data-ttu-id="cda5d-134">Gibt an, dass Sie die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode aufgerufen haben, um den Auftrag abzubrechen (entfernen Sie den Auftrag aus der Übertragungs Warteschlange).</span><span class="sxs-lookup"><span data-stu-id="cda5d-134">Specifies that you called the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method to cancel the job (remove the job from the transfer queue).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cda5d-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cda5d-135">Requirements</span></span>



| <span data-ttu-id="cda5d-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cda5d-136">Requirement</span></span> | <span data-ttu-id="cda5d-137">Wert</span><span class="sxs-lookup"><span data-stu-id="cda5d-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cda5d-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cda5d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="cda5d-139">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cda5d-139">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cda5d-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cda5d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="cda5d-141">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cda5d-141">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="cda5d-142">Header</span><span class="sxs-lookup"><span data-stu-id="cda5d-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="cda5d-143"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="cda5d-143"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cda5d-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cda5d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cda5d-145">**Ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="cda5d-145">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





