---
title: Ibackgroundcopyjob getnotifyflags-Methode (deliveryoptimization. h)
description: Ruft die ereignisbenachrichtigungsflags für den Auftrag ab.
ms.assetid: 95ADC97F-63DC-4EB6-B85C-7BCC79238C12
keywords:
- Getnotifyflags-Methode
- Getnotifyflags-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, getnotifyflags-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyFlags
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e104857725849dfeb899b449ea055bc3cdb046bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340677"
---
# <a name="ibackgroundcopyjobgetnotifyflags-method"></a><span data-ttu-id="503fc-106">Ibackgroundcopyjob:: getnotifyflags-Methode</span><span class="sxs-lookup"><span data-stu-id="503fc-106">IBackgroundCopyJob::GetNotifyFlags method</span></span>

<span data-ttu-id="503fc-107">Ruft die ereignisbenachrichtigungsflags für den Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="503fc-107">Retrieves the event notification flags for the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="503fc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="503fc-108">Syntax</span></span>


```C++
HRESULT GetNotifyFlags(
  [out] ULONG *pNotifyFlags
);
```



## <a name="parameters"></a><span data-ttu-id="503fc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="503fc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="503fc-110">*pnotifyflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="503fc-110">*pNotifyFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="503fc-111">Identifiziert die Ereignisse, die von der Anwendung empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="503fc-111">Identifies the events that your application receives.</span></span> <span data-ttu-id="503fc-112">In der folgenden Tabelle sind die Werte für das Ereignis Benachrichtigungs Kennzeichen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="503fc-112">The following table lists the event notification flag values.</span></span>



| <span data-ttu-id="503fc-113">Wert</span><span class="sxs-lookup"><span data-stu-id="503fc-113">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="503fc-114">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="503fc-114">Meaning</span></span>                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="BG_NOTIFY_JOB_TRANSFERRED"></span><span id="bg_notify_job_transferred"></span><dl> <span data-ttu-id="503fc-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span><span class="sxs-lookup"><span data-stu-id="503fc-115"><dt>**BG_NOTIFY_JOB_TRANSFERRED**</dt></span></span> </dl>    | <span data-ttu-id="503fc-116">Alle Dateien im Auftrag wurden übertragen.</span><span class="sxs-lookup"><span data-stu-id="503fc-116">All of the files in the job have been transferred.</span></span><br/>                  |
| <span id="BG_NOTIFY_JOB_ERROR"></span><span id="bg_notify_job_error"></span><dl> <span data-ttu-id="503fc-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span><span class="sxs-lookup"><span data-stu-id="503fc-117"><dt>**BG_NOTIFY_JOB_ERROR**</dt></span></span> </dl>                      | <span data-ttu-id="503fc-118">Es ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="503fc-118">An error has occurred.</span></span><br/>                                              |
| <span id="BG_NOTIFY_DISABLE"></span><span id="bg_notify_disable"></span><dl> <span data-ttu-id="503fc-119"><dt>**BG_NOTIFY_DISABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="503fc-119"><dt>**BG_NOTIFY_DISABLE**</dt></span></span> </dl>                             | <span data-ttu-id="503fc-120">Die Ereignis Benachrichtigung ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="503fc-120">Event notification is disabled.</span></span> <span data-ttu-id="503fc-121">Wenn festgelegt, werden die anderen Flags ignoriert.</span><span class="sxs-lookup"><span data-stu-id="503fc-121">If set, DO ignores the other flags.</span></span><br/> |
| <span id="BG_NOTIFY_JOB_MODIFICATION"></span><span id="bg_notify_job_modification"></span><dl> <span data-ttu-id="503fc-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span><span class="sxs-lookup"><span data-stu-id="503fc-122"><dt>**BG_NOTIFY_JOB_MODIFICATION**</dt></span></span> </dl> | <span data-ttu-id="503fc-123">Der Auftrag wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="503fc-123">The job has been modified.</span></span><br/>                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="503fc-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="503fc-124">Return value</span></span>

<span data-ttu-id="503fc-125">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="503fc-125">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="503fc-126">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="503fc-126">Return code</span></span>                                                                              | <span data-ttu-id="503fc-127">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="503fc-127">Description</span></span>                                                |
|------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="503fc-128"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="503fc-128"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="503fc-129">Die Flags für die Ereignis Benachrichtigung wurden erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="503fc-129">Event notify flags were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="503fc-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="503fc-130">Requirements</span></span>



| <span data-ttu-id="503fc-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="503fc-131">Requirement</span></span> | <span data-ttu-id="503fc-132">Wert</span><span class="sxs-lookup"><span data-stu-id="503fc-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="503fc-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="503fc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="503fc-134">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="503fc-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="503fc-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="503fc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="503fc-136">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="503fc-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="503fc-137">Header</span><span class="sxs-lookup"><span data-stu-id="503fc-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="503fc-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="503fc-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="503fc-139">IDL</span><span class="sxs-lookup"><span data-stu-id="503fc-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="503fc-140"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="503fc-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="503fc-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="503fc-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="503fc-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="503fc-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="503fc-143">DLL</span><span class="sxs-lookup"><span data-stu-id="503fc-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="503fc-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="503fc-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="503fc-145">IID</span><span class="sxs-lookup"><span data-stu-id="503fc-145">IID</span></span><br/>                      | <span data-ttu-id="503fc-146">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="503fc-146">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="503fc-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="503fc-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="503fc-148">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="503fc-148">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="503fc-149">**Ibackgroundcopycallback**</span><span class="sxs-lookup"><span data-stu-id="503fc-149">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="503fc-150">**Ibackgroundcopyjob:: getnotifyinterface**</span><span class="sxs-lookup"><span data-stu-id="503fc-150">**IBackgroundCopyJob::GetNotifyInterface**</span></span>](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[<span data-ttu-id="503fc-151">**Ibackgroundcopyjob:: setnotifyflags**</span><span class="sxs-lookup"><span data-stu-id="503fc-151">**IBackgroundCopyJob::SetNotifyFlags**</span></span>](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





