---
title: Ibackgroundcopyjob setnotifyflags-Methode (deliveryoptimization. h)
description: Gibt den Typ der Ereignis Benachrichtigung an, die Sie empfangen möchten, z. b. Ereignisse, die übertragen werden.
ms.assetid: 19E626A5-6B6E-44E0-BD6F-43F132F32890
keywords:
- Setnotifyflags-Methode
- Setnotifyflags-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, setnotifyflags-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ea754eeafca8f0efdcad5545cfc3a462c8b508cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517849"
---
# <a name="ibackgroundcopyjobsetnotifyflags-method"></a><span data-ttu-id="abee1-106">Ibackgroundcopyjob:: setnotifyflags-Methode</span><span class="sxs-lookup"><span data-stu-id="abee1-106">IBackgroundCopyJob::SetNotifyFlags method</span></span>

<span data-ttu-id="abee1-107">Gibt den Typ der Ereignis Benachrichtigung an, die Sie empfangen möchten, z. b. Ereignisse, die übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="abee1-107">Specifies the type of event notification you want to receive, such as job transferred events.</span></span>

## <a name="syntax"></a><span data-ttu-id="abee1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="abee1-108">Syntax</span></span>


```C++
HRESULT SetNotifyFlags(
  [in] ULONG NotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="abee1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="abee1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abee1-110">*Notifyflags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abee1-110">*NotifyFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abee1-111">Legen Sie mindestens eines der folgenden Flags fest, um die Ereignisse zu identifizieren, die Sie empfangen möchten.</span><span class="sxs-lookup"><span data-stu-id="abee1-111">Set one or more of the following flags to identify the events that you want to receive.</span></span>



| <span data-ttu-id="abee1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="abee1-112">Value</span></span>                                                                                                                                                                                                                                                                                    | <span data-ttu-id="abee1-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="abee1-113">Meaning</span></span>                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="abee1-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-114"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt> <dt>0x0001</dt></span></span> </dl>                          | <span data-ttu-id="abee1-115">Alle Dateien im Auftrag wurden übertragen.</span><span class="sxs-lookup"><span data-stu-id="abee1-115">All of the files in the job have been transferred.</span></span><br/>                                                                                                                                                          |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="abee1-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-116"><dt>**BG_NOTIFY_JOB_ERROR**</dt> <dt>0x0002</dt></span></span> </dl>                                            | <span data-ttu-id="abee1-117">Es ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="abee1-117">An error has occurred.</span></span><br/>                                                                                                                                                                                      |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="abee1-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-118"><dt>**BG_NOTIFY_DISABLE**</dt> <dt>0x0004</dt></span></span> </dl>                                                   | <span data-ttu-id="abee1-119">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abee1-119">Not supported.</span></span><br/>                                                                                                                                                                                              |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="abee1-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-120"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt> <dt>0x0008</dt></span></span> </dl>                       | <span data-ttu-id="abee1-121">Der Auftrag wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="abee1-121">The job has been modified.</span></span> <span data-ttu-id="abee1-122">Beispielsweise wird ein Eigenschafts Wert geändert, der Status des Auftrags geändert, oder der Fortschritt wird durch das übertragen der Dateien durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="abee1-122">For example, a property value changed, the state of the job changed, or progress is made transferring the files.</span></span> <span data-ttu-id="abee1-123">Dieses Flag wird ignoriert, wenn eine Befehlszeilen Benachrichtigung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="abee1-123">This flag is ignored if command line notification is specified.</span></span><br/> |
| <span id="BG_NOTIFY_FILE_TRANSFERRED"></span><span id="bg_notify_file_transferred"></span><dl> <span data-ttu-id="abee1-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-124"><dt>**BG_NOTIFY_FILE_TRANSFERRED**</dt> <dt>0x0010</dt></span></span> </dl>                       | <span data-ttu-id="abee1-125">Eine Datei im Auftrag wurde übertragen.</span><span class="sxs-lookup"><span data-stu-id="abee1-125">A file in the job has been transferred.</span></span> <span data-ttu-id="abee1-126">Dieses Flag wird ignoriert, wenn eine Befehlszeilen Benachrichtigung angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="abee1-126">This flag is ignored if command line notification is specified.</span></span><br/>                                                                                                     |
| <span id="BG_NOTIFY_FILE_RANGES_TRANSFERRED"></span><span id="bg_notify_file_ranges_transferred"></span><dl> <span data-ttu-id="abee1-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-127"><dt>**BG_NOTIFY_FILE_RANGES_TRANSFERRED**</dt> <dt>0x0020</dt></span></span> </dl> | <span data-ttu-id="abee1-128">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="abee1-128">Not supported.</span></span><br/>                                                                                                                                                                                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abee1-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abee1-129">Return value</span></span>

<span data-ttu-id="abee1-130">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="abee1-130">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="abee1-131">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="abee1-131">Return code</span></span>                                                                                          | <span data-ttu-id="abee1-132">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="abee1-132">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="abee1-133"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-133"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="abee1-134">Der Typ der Ereignis Benachrichtigung wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="abee1-134">Type of event notification was successfully set.</span></span><br/>                                          |
| <dl> <span data-ttu-id="abee1-135"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-135"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="abee1-136">Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED sein.</span><span class="sxs-lookup"><span data-stu-id="abee1-136">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="abee1-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abee1-137">Remarks</span></span>

<span data-ttu-id="abee1-138">Verwenden Sie die **setnotifyflags** -Methode in Verbindung mit der [**ibackgroundcopyjob:: setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md)-Methode.</span><span class="sxs-lookup"><span data-stu-id="abee1-138">Use the **SetNotifyFlags** method in conjunction with the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="abee1-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abee1-139">Requirements</span></span>



| <span data-ttu-id="abee1-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abee1-140">Requirement</span></span> | <span data-ttu-id="abee1-141">Wert</span><span class="sxs-lookup"><span data-stu-id="abee1-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="abee1-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abee1-142">Minimum supported client</span></span><br/> | <span data-ttu-id="abee1-143">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abee1-143">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="abee1-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abee1-144">Minimum supported server</span></span><br/> | <span data-ttu-id="abee1-145">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="abee1-145">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="abee1-146">Header</span><span class="sxs-lookup"><span data-stu-id="abee1-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="abee1-147"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-147"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="abee1-148">IDL</span><span class="sxs-lookup"><span data-stu-id="abee1-148">IDL</span></span><br/>                      | <dl> <span data-ttu-id="abee1-149"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-149"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="abee1-150">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="abee1-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="abee1-151"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-151"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="abee1-152">DLL</span><span class="sxs-lookup"><span data-stu-id="abee1-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abee1-153"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abee1-153"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="abee1-154">IID</span><span class="sxs-lookup"><span data-stu-id="abee1-154">IID</span></span><br/>                      | <span data-ttu-id="abee1-155">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="abee1-155">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="abee1-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abee1-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abee1-157">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="abee1-157">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="abee1-158">**Ibackgroundcopycallback**</span><span class="sxs-lookup"><span data-stu-id="abee1-158">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="abee1-159">**Ibackgroundcopyjob:: getnotifyflags**</span><span class="sxs-lookup"><span data-stu-id="abee1-159">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="abee1-160">**Ibackgroundcopyjob:: setnotifyinterface**</span><span class="sxs-lookup"><span data-stu-id="abee1-160">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





