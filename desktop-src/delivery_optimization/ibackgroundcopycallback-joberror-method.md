---
title: Ibackgroundcopycallback-joberror-Methode (deliveryoptimization. h)
description: Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der joberror-Methode auf, wenn sich der Status des Auftrags in "BG_JOB_STATE_ERROR" ändert.
ms.assetid: 121712A5-98EB-4B2F-A004-A3BDF9C1332B
keywords:
- Joberror-Methode
- Joberror-Methode, ibackgroundcopycallback-Schnittstelle
- Ibackgroundcopycallback-Schnittstelle, joberror-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobError
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0122f5777303506be5fd81d0966b00f828bf2073
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391841"
---
# <a name="ibackgroundcopycallbackjoberror-method"></a><span data-ttu-id="09a71-106">Ibackgroundcopycallback:: joberror-Methode</span><span class="sxs-lookup"><span data-stu-id="09a71-106">IBackgroundCopyCallback::JobError method</span></span>

<span data-ttu-id="09a71-107">Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode auf, wenn sich der Status des Auftrags in "BG_JOB_STATE_ERROR" ändert.</span><span class="sxs-lookup"><span data-stu-id="09a71-107">Delivery Optimization (DO) calls your implementation of the [**JobError**](https://www.bing.com/search?q=**JobError**) method when the state of the job changes to BG_JOB_STATE_ERROR.</span></span>

## <a name="syntax"></a><span data-ttu-id="09a71-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="09a71-108">Syntax</span></span>


```C++
HRESULT JobError(
  [in] IBackgroundCopyJob   *pJob,
  [in] IBackgroundCopyError *pError
);
```



## <a name="parameters"></a><span data-ttu-id="09a71-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="09a71-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09a71-110">*pjob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09a71-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a71-111">Enthält auftragsbezogene Informationen, wie z. b. die Anzahl von Bytes und Dateien, die vor dem Auftreten des Fehlers übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="09a71-111">Contains job-related information, such as the number of bytes and files transferred before the error occurred.</span></span> <span data-ttu-id="09a71-112">Außerdem enthält es die Methoden zum fortsetzen und Abbrechen des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="09a71-112">It also contains the methods to resume and cancel the job.</span></span> <span data-ttu-id="09a71-113">*Pjob* nicht freigeben; Gibt die-Schnittstelle frei, wenn die [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="09a71-113">Do not release *pJob*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="09a71-114">*perror* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="09a71-114">*pError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="09a71-115">Enthält Fehlerinformationen, wie z. b. die Datei, die zu dem Zeitpunkt, zu dem ein schwerwiegender Fehler aufgetreten ist, und eine Beschreibung des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="09a71-115">Contains error information, such as the file being processed at the time the fatal error occurred and a description of the error.</span></span> <span data-ttu-id="09a71-116">Kein Release von *perror*; Gibt die-Schnittstelle frei, wenn die [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="09a71-116">Do not release *pError*; DO releases the interface when the [**JobError**](https://www.bing.com/search?q=**JobError**) method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09a71-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="09a71-117">Return value</span></span>

<span data-ttu-id="09a71-118">Diese Methode sollte **S_OK** zurückgeben. Andernfalls wird diese Methode weiterhin aufgerufen, bis **S_OK** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="09a71-118">This method should return **S_OK**; otherwise, DO continues to call this method until **S_OK** is returned.</span></span> <span data-ttu-id="09a71-119">Aus Leistungsgründen sollten Sie begrenzen, wie oft ein anderer Wert als **S_OK** zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="09a71-119">For performance reasons, you should limit the number of times you return a value other than **S_OK** to a few times.</span></span> <span data-ttu-id="09a71-120">Als Alternative zum Zurückgeben eines Fehlercodes sollten Sie die Rückgabe von **S_OK** und die interne Behandlung des Fehlers in Erwägung gezogen.</span><span class="sxs-lookup"><span data-stu-id="09a71-120">As an alternative to returning an error code, consider always returning **S_OK** and handling the error internally.</span></span> <span data-ttu-id="09a71-121">Das Intervall, in dem diese Methode aufgerufen wird, ist willkürlich.</span><span class="sxs-lookup"><span data-stu-id="09a71-121">The interval at which this method is called is arbitrary.</span></span>

## <a name="remarks"></a><span data-ttu-id="09a71-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09a71-122">Remarks</span></span>

<span data-ttu-id="09a71-123">Nachdem Sie die Ursache des Fehlers bestimmt haben, führen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="09a71-123">After you determine the cause of the error, perform one of the following options:</span></span>

-   <span data-ttu-id="09a71-124">Um den Auftrag abzubrechen, rufen Sie die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="09a71-124">To cancel the job, call the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method.</span></span>
-   <span data-ttu-id="09a71-125">Um den Teil des Auftrags zu akzeptieren, der vor dem Auftreten des Fehlers erfolgreich übertragen wurde, können Sie die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="09a71-125">To accept the portion of the job that transferred successfully before the error occurred, call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method.</span></span> <span data-ttu-id="09a71-126">Diese Option gilt nicht für Aufträge zum hochladen. ein Teil eines uploadauftrags kann nicht ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="09a71-126">This option does not apply to upload jobs; you cannot complete a portion of an upload job.</span></span>
-   <span data-ttu-id="09a71-127">Beheben Sie das Problem, und führen Sie dann die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) -Methode aus, um die Verarbeitung des Auftrags abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="09a71-127">To finish processing the job, fix the problem, and then call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span>

<span data-ttu-id="09a71-128">Vorübergehende Fehler generieren keine Aufrufe der [**joberror**](https://www.bing.com/search?q=**JobError**) -Methode.</span><span class="sxs-lookup"><span data-stu-id="09a71-128">Transient errors do not generate calls to the [**JobError**](https://www.bing.com/search?q=**JobError**) method.</span></span>

<span data-ttu-id="09a71-129">Gibt BG_ERROR_CONTEXT_REMOTE_FILE zurück, wenn der Auftrag einen HTTP 403-Fehler ausgelöst hat, andernfalls BG_ERROR_CONTEXT_NONE.</span><span class="sxs-lookup"><span data-stu-id="09a71-129">DO returns BG_ERROR_CONTEXT_REMOTE_FILE if the job hit a HTTP 403 error, BG_ERROR_CONTEXT_NONE otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="09a71-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="09a71-130">Requirements</span></span>



| <span data-ttu-id="09a71-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="09a71-131">Requirement</span></span> | <span data-ttu-id="09a71-132">Wert</span><span class="sxs-lookup"><span data-stu-id="09a71-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09a71-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="09a71-133">Minimum supported client</span></span><br/> | <span data-ttu-id="09a71-134">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09a71-134">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="09a71-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="09a71-135">Minimum supported server</span></span><br/> | <span data-ttu-id="09a71-136">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="09a71-136">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="09a71-137">Header</span><span class="sxs-lookup"><span data-stu-id="09a71-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="09a71-138"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="09a71-138"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="09a71-139">IDL</span><span class="sxs-lookup"><span data-stu-id="09a71-139">IDL</span></span><br/>                      | <dl> <span data-ttu-id="09a71-140"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="09a71-140"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="09a71-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="09a71-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="09a71-142"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="09a71-142"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="09a71-143">DLL</span><span class="sxs-lookup"><span data-stu-id="09a71-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09a71-144"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09a71-144"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="09a71-145">IID</span><span class="sxs-lookup"><span data-stu-id="09a71-145">IID</span></span><br/>                      | <span data-ttu-id="09a71-146">IID_IBackgroundCopyCallback ist als 97ea99c7-0186-4ad4-8df9-c5b4e0ed6b22 definiert.</span><span class="sxs-lookup"><span data-stu-id="09a71-146">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="09a71-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09a71-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09a71-148">**Ibackgroundcopycallback**</span><span class="sxs-lookup"><span data-stu-id="09a71-148">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="09a71-149">**Ibackgroundcopyerror**</span><span class="sxs-lookup"><span data-stu-id="09a71-149">**IBackgroundCopyError**</span></span>](ibackgroundcopyerror.md)
</dt> <dt>

[<span data-ttu-id="09a71-150">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="09a71-150">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="09a71-151">**Ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="09a71-151">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="09a71-152">**Ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="09a71-152">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





