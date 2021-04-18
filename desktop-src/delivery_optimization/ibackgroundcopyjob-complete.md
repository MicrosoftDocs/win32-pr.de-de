---
title: Methode "ibackgroundcopyjob Complete" (deliveryoptimization. h)
description: Beendet den Auftrag und speichert die übertragenen Dateien auf dem Client.
ms.assetid: A3706DBA-C44E-4F7A-A787-62FB436706FC
keywords:
- Complete-Methode
- Complete-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, Complete-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Complete
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72383bb235d31043f781998324891b6df134e6ec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103658"
---
# <a name="ibackgroundcopyjobcomplete-method"></a><span data-ttu-id="c2af8-106">Ibackgroundcopyjob:: Complete-Methode</span><span class="sxs-lookup"><span data-stu-id="c2af8-106">IBackgroundCopyJob::Complete method</span></span>

<span data-ttu-id="c2af8-107">Beendet den Auftrag und speichert die übertragenen Dateien auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="c2af8-107">Ends the job and saves the transferred files on the client.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2af8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2af8-108">Syntax</span></span>


```C++
HRESULT Complete();
```



## <a name="parameters"></a><span data-ttu-id="c2af8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2af8-109">Parameters</span></span>

<span data-ttu-id="c2af8-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c2af8-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c2af8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2af8-111">Return value</span></span>

<span data-ttu-id="c2af8-112">Diese Methode gibt die folgenden **HRESULT** -Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c2af8-112">This method returns the following **HRESULT** values.</span></span> <span data-ttu-id="c2af8-113">Die-Methode kann auch Fehler im Zusammenhang mit dem Umbenennen der temporären Kopien der übertragenen Dateien in Ihre angegebenen Namen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c2af8-113">The method can also return errors related to renaming the temporary copies of the transferred files to their given names.</span></span>



| <span data-ttu-id="c2af8-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c2af8-114">Return code</span></span>                                                                                          | <span data-ttu-id="c2af8-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2af8-115">Description</span></span>                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="c2af8-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="c2af8-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="c2af8-117">Alle Dateien wurden erfolgreich übertragen.</span><span class="sxs-lookup"><span data-stu-id="c2af8-117">All files transferred successfully.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="c2af8-118"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="c2af8-118"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="c2af8-119">Für Downloads kann der Status des Auftrags nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED sein.</span><span class="sxs-lookup"><span data-stu-id="c2af8-119">For downloads, the state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span> <br/> <span data-ttu-id="c2af8-120">Für Uploads muss der Status des Auftrags BG_JOB_STATE_TRANSFERRED sein.</span><span class="sxs-lookup"><span data-stu-id="c2af8-120">For uploads, the state of the job must be BG_JOB_STATE_TRANSFERRED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2af8-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2af8-121">Remarks</span></span>

<span data-ttu-id="c2af8-122">Alle Dateien wurden erfolgreich übertragen, wenn der Status des Auftrags **BG_JOB_STATE_TRANSFERRED** ist.</span><span class="sxs-lookup"><span data-stu-id="c2af8-122">All of the files have been successfully transferred if the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span> <span data-ttu-id="c2af8-123">Um den Status des Auftrags zu überprüfen, müssen Sie die [**ibackgroundcopyjob:: GetState**](ibackgroundcopyjob-getstate.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="c2af8-123">To check the state of the job, call the [**IBackgroundCopyJob::GetState**](ibackgroundcopyjob-getstate.md) method.</span></span> <span data-ttu-id="c2af8-124">Sie können auch die [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle implementieren, um eine Benachrichtigung zu erhalten, wenn alle Dateien an den Client übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="c2af8-124">You can also implement the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface to receive notification when all of the files have been transferred to the client.</span></span>

<span data-ttu-id="c2af8-125">Behält Aufträge bei, die weniger als 30 Tage sind.</span><span class="sxs-lookup"><span data-stu-id="c2af8-125">DO retains jobs that are less than 30 days only.</span></span> <span data-ttu-id="c2af8-126">Alle älteren Aufträge werden entfernt.</span><span class="sxs-lookup"><span data-stu-id="c2af8-126">All older jobs will be removed.</span></span> <span data-ttu-id="c2af8-127">Die Gruppenrichtlinie " [jobinactivitytimeout](https://www.bing.com/search?q=JobInactivityTimeout) " wird von nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2af8-127">DO does not support the [JobInactivityTimeout](https://www.bing.com/search?q=JobInactivityTimeout) Group Policy.</span></span>

<span data-ttu-id="c2af8-128">Für Download Aufträge können Sie während des Übertragungs Vorgangs jederzeit die **Complete** -Methode abrufen. Allerdings werden nur Dateien gespeichert, die vor dem Aufruf dieser Methode erfolgreich an den Client übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="c2af8-128">For download jobs, you can call the **Complete** method at anytime during the transfer process; however, only files that were successfully transferred to the client before calling this method are saved.</span></span> <span data-ttu-id="c2af8-129">Wenn Sie z. b. die **Complete** -Methode aufzurufen, während die dritte von fünf Dateien verarbeitet, werden nur die ersten beiden Dateien gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c2af8-129">For example, if you call the **Complete** method while DO is processing the third of five files, only the first two files are saved.</span></span> <span data-ttu-id="c2af8-130">Um zu ermitteln, welche Dateien übertragen wurden, müssen Sie die [**ibackgroundcopyfile:: GetProgress**](ibackgroundcopyfile-getprogress-method.md) -Methode aufrufen und den **bytesTransferred** -Member mit dem **bytesTotal** -Member der [**BG_FILE_PROGRESS**](bg-file-progress.md) Struktur vergleichen.</span><span class="sxs-lookup"><span data-stu-id="c2af8-130">To determine which files have been transferred, call the [**IBackgroundCopyFile::GetProgress**](ibackgroundcopyfile-getprogress-method.md) method and compare the **BytesTransferred** member to the **BytesTotal** member of the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

<span data-ttu-id="c2af8-131">Bei Uploadaufträgen können Sie die **Complete** -Methode nur dann aufzurufen, wenn der Status des Auftrags **BG_JOB_STATE_TRANSFERRED** ist.</span><span class="sxs-lookup"><span data-stu-id="c2af8-131">For upload jobs, you can call the **Complete** method only when the job's state is **BG_JOB_STATE_TRANSFERRED**.</span></span>

<span data-ttu-id="c2af8-132">Der Besitzer der Datei ist der Benutzer, der den-Befehl durchgeführt hat.</span><span class="sxs-lookup"><span data-stu-id="c2af8-132">The owner of the file is the user who made the call.</span></span> <span data-ttu-id="c2af8-133">Wenn ein Administrator beispielsweise den Auftrag eines anderen Benutzers abschließt, ist der Administrator nicht der Besitzer des Auftrags, der die Datei besitzt.</span><span class="sxs-lookup"><span data-stu-id="c2af8-133">For example, if an administrator completes someone else's job, the administrator not the owner of the job owns the file.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2af8-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2af8-134">Requirements</span></span>



| <span data-ttu-id="c2af8-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2af8-135">Requirement</span></span> | <span data-ttu-id="c2af8-136">Wert</span><span class="sxs-lookup"><span data-stu-id="c2af8-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2af8-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c2af8-137">Minimum supported client</span></span><br/> | <span data-ttu-id="c2af8-138">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2af8-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c2af8-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c2af8-139">Minimum supported server</span></span><br/> | <span data-ttu-id="c2af8-140">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c2af8-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="c2af8-141">Header</span><span class="sxs-lookup"><span data-stu-id="c2af8-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="c2af8-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2af8-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2af8-143">IDL</span><span class="sxs-lookup"><span data-stu-id="c2af8-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c2af8-144"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c2af8-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="c2af8-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2af8-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="c2af8-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2af8-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="c2af8-147">DLL</span><span class="sxs-lookup"><span data-stu-id="c2af8-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c2af8-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c2af8-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="c2af8-149">IID</span><span class="sxs-lookup"><span data-stu-id="c2af8-149">IID</span></span><br/>                      | <span data-ttu-id="c2af8-150">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="c2af8-150">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="c2af8-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2af8-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2af8-152">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="c2af8-152">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="c2af8-153">**Ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="c2af8-153">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="c2af8-154">**Ibackgroundcopyjob:: GetState**</span><span class="sxs-lookup"><span data-stu-id="c2af8-154">**IBackgroundCopyJob::GetState**</span></span>](ibackgroundcopyjob-getstate.md)
</dt> </dl>

 

 





