---
title: Ibackgroundcopyjob GetError-Methode (deliveryoptimization. h)
description: Ruft die Fehler Schnittstelle ab, nachdem ein Fehler aufgetreten ist.
ms.assetid: 66891557-C118-4C66-AEFC-D8FD70976B9A
keywords:
- GetError-Methode
- GetError-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetError-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1f2da994da83a786b89adb5ae63104dbaa6e2ef9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391912"
---
# <a name="ibackgroundcopyjobgeterror-method"></a><span data-ttu-id="1b25f-106">Ibackgroundcopyjob:: GetError-Methode</span><span class="sxs-lookup"><span data-stu-id="1b25f-106">IBackgroundCopyJob::GetError method</span></span>

<span data-ttu-id="1b25f-107">Ruft die Fehler Schnittstelle ab, nachdem ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1b25f-107">Retrieves the error interface after an error occurs.</span></span>

<span data-ttu-id="1b25f-108">Die Übermittlungs Optimierung (Do) generiert ein Fehler Objekt, wenn der Status des Auftrags BG_JOB_STATE_ERROR oder BG_JOB_STATE_TRANSIENT_ERROR ist.</span><span class="sxs-lookup"><span data-stu-id="1b25f-108">Delivery Optimization (DO) generates an error object when the state of the job is BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR.</span></span> <span data-ttu-id="1b25f-109">Der Dienst erstellt kein Fehler Objekt, wenn ein-Rückruf für eine **ibackgroundcopyxxxx** -Schnittstellen Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="1b25f-109">The service does not create an error object when a call to an **IBackgroundCopyXXXX** interface method fails.</span></span> <span data-ttu-id="1b25f-110">Das Error-Objekt ist verfügbar, bis die Daten übertragen werden (der Status des Auftrags ändert sich in BG_JOB_STATE_TRANSFERRING), oder bis die Anwendung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b25f-110">The error object is available until DO begins transferring data (the state of the job changes to BG_JOB_STATE_TRANSFERRING) for the job or until your application exits.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b25f-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b25f-111">Syntax</span></span>


```C++
HRESULT GetError(
  [out] IBackgroundCopyError **ppError
);
```



## <a name="parameters"></a><span data-ttu-id="1b25f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b25f-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b25f-113">*pperror* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b25f-113">*ppError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b25f-114">Fehler Schnittstelle, die den Fehlercode, eine Beschreibung des Fehlers und den Kontext bereitstellt, in dem der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1b25f-114">Error interface that provides the error code, a description of the error, and the context in which the error occurred.</span></span> <span data-ttu-id="1b25f-115">Dieser Parameter identifiziert außerdem die Datei, die zum Zeitpunkt des Auftretens des Fehlers übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="1b25f-115">This parameter also identifies the file being transferred at the time the error occurred.</span></span> <span data-ttu-id="1b25f-116">Release *pperror* , wenn dies erledigt ist.</span><span class="sxs-lookup"><span data-stu-id="1b25f-116">Release *ppError* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b25f-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b25f-117">Return value</span></span>

<span data-ttu-id="1b25f-118">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="1b25f-118">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="1b25f-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1b25f-119">Return code</span></span>                                                                                                           | <span data-ttu-id="1b25f-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b25f-120">Description</span></span>                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b25f-121"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="1b25f-121"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>                              | <span data-ttu-id="1b25f-122">Das Fehler Objekt wurde erfolgreich generiert.</span><span class="sxs-lookup"><span data-stu-id="1b25f-122">Successfully generated the error object.</span></span><br/>                                                                                                                                                       |
| <dl> <span data-ttu-id="1b25f-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span><span class="sxs-lookup"><span data-stu-id="1b25f-123"><dt>**DO_E_ERROR_INFORMATION_UNAVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="1b25f-124">Die Fehler Schnittstelle ist nur verfügbar, wenn ein Fehler auftritt (BG_JOB_STATE_ERROR oder BG_JOB_STATE_TRANSIENT_ERROR) und bevor mit dem Übertragen von Daten begonnen wird (BG_JOB_STATE_TRANSFERRING).</span><span class="sxs-lookup"><span data-stu-id="1b25f-124">The error interface is available only after an error occurs (BG_JOB_STATE_ERROR or BG_JOB_STATE_TRANSIENT_ERROR) and before DO begins transferring data (BG_JOB_STATE_TRANSFERRING).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1b25f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b25f-125">Remarks</span></span>

<span data-ttu-id="1b25f-126">Der Auftrag wird bei schwerwiegenden Fehlern in einen Fehlerzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="1b25f-126">The job is placed in an error state on fatal errors.</span></span> <span data-ttu-id="1b25f-127">Verwenden Sie eine der folgenden Optionen, um zu bestimmen, ob der Auftrag fehlerhaft ist:</span><span class="sxs-lookup"><span data-stu-id="1b25f-127">Use one of the following options to determine if the job is in error:</span></span>

-   <span data-ttu-id="1b25f-128">Rufen Sie die [**ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) -Methode auf, um den Status des Auftrags abzurufen.</span><span class="sxs-lookup"><span data-stu-id="1b25f-128">To poll for the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="1b25f-129">Der Auftrag ist fehlerhaft, wenn der Status BG_JOB_STATE_ERROR ist.</span><span class="sxs-lookup"><span data-stu-id="1b25f-129">The job is in error if the state is BG_JOB_STATE_ERROR.</span></span>
-   <span data-ttu-id="1b25f-130">Um Benachrichtigungen zu erhalten, wenn ein Fehler auftritt, implementieren Sie die [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle (insbesondere die [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode).</span><span class="sxs-lookup"><span data-stu-id="1b25f-130">To receive notification when an error occurs, implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface (specifically, the [**JobError**](https://www.bing.com/search?q=**JobError**) method).</span></span> <span data-ttu-id="1b25f-131">Rufen Sie dann die [**ibackgroundcopyjob:: setnotifyinterface**](ibackgroundcopyjob-setnotifyinterface.md) -Methode auf, um den Rückruf zu registrieren, und die [**ibackgroundcopyjob:: setnotifyflags**](ibackgroundcopyjob-setnotifyflags.md) -Methode, um das BG_NOTIFY_JOB_ERROR-Flag festzulegen.</span><span class="sxs-lookup"><span data-stu-id="1b25f-131">Then, call the [**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) method to register the callback and the [**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) method to set the BG_NOTIFY_JOB_ERROR flag.</span></span>

<span data-ttu-id="1b25f-132">Die [**ibackgroundcopyerror**](ibackgroundcopyerror.md) -Schnittstelle enthält Informationen, die Sie verwenden, um die Ursache des Fehlers zu ermitteln, und, wenn der Übertragungsprozess fortgesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1b25f-132">The [**IBackgroundCopyError**](ibackgroundcopyerror.md) interface contains information that you use to determine the cause of the error and if the transfer process can proceed.</span></span> <span data-ttu-id="1b25f-133">Nachdem Sie die Ursache des Fehlers bestimmt haben, führen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="1b25f-133">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="1b25f-134">Um den Auftrag abzubrechen, rufen Sie die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="1b25f-134">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="1b25f-135">Um die Dateien zu speichern, die vor dem Auftreten des Fehlers erfolgreich übertragen wurden, müssen Sie die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="1b25f-135">To save those files that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span>
-   <span data-ttu-id="1b25f-136">Beheben Sie das Problem, und führen Sie dann die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) -Methode aus, um die Verarbeitung des Auftrags abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="1b25f-136">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b25f-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b25f-137">Requirements</span></span>



| <span data-ttu-id="1b25f-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b25f-138">Requirement</span></span> | <span data-ttu-id="1b25f-139">Wert</span><span class="sxs-lookup"><span data-stu-id="1b25f-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b25f-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b25f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="1b25f-141">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b25f-141">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1b25f-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b25f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="1b25f-143">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b25f-143">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1b25f-144">Header</span><span class="sxs-lookup"><span data-stu-id="1b25f-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b25f-145"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b25f-145"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="1b25f-146">IDL</span><span class="sxs-lookup"><span data-stu-id="1b25f-146">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1b25f-147"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1b25f-147"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="1b25f-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b25f-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="1b25f-149"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b25f-149"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="1b25f-150">DLL</span><span class="sxs-lookup"><span data-stu-id="1b25f-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b25f-151"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b25f-151"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="1b25f-152">IID</span><span class="sxs-lookup"><span data-stu-id="1b25f-152">IID</span></span><br/>                      | <span data-ttu-id="1b25f-153">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="1b25f-153">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="1b25f-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b25f-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b25f-155">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="1b25f-155">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="1b25f-156">**Ibackgroundcopycallback:: joberror**</span><span class="sxs-lookup"><span data-stu-id="1b25f-156">**IBackgroundCopyCallback::JobError**</span></span>](ibackgroundcopycallback-joberror-method.md)
</dt> <dt>

[<span data-ttu-id="1b25f-157">**Ibackgroundcopyerror**</span><span class="sxs-lookup"><span data-stu-id="1b25f-157">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="1b25f-158">**Ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="1b25f-158">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





