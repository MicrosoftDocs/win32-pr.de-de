---
title: Ibackgroundcopyjob setnoprogresstimeout-Methode (deliveryoptimization. h)
description: Legt die Zeitspanne fest, die die Übermittlungs Optimierung (Do) versucht, die Datei zu übertragen, nachdem ein vorübergehender Fehler aufgetreten ist. Bei einem Fortschritt wird der Timer zurückgesetzt.
ms.assetid: DC86F74F-8429-4D78-B425-CAF19867B05E
keywords:
- Setnoprogresstimeout-Methode
- Setnoprogresstimeout-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, setnoprogresstimeout-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 276c8c44d2b2b034543aae25361c5f5c94046f5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040674"
---
# <a name="ibackgroundcopyjobsetnoprogresstimeout-method"></a><span data-ttu-id="b9415-107">Ibackgroundcopyjob:: setnoprogresstimeout-Methode</span><span class="sxs-lookup"><span data-stu-id="b9415-107">IBackgroundCopyJob::SetNoProgressTimeout method</span></span>

<span data-ttu-id="b9415-108">Legt die Zeitspanne fest, die die Übermittlungs Optimierung (Do) versucht, die Datei zu übertragen, nachdem ein vorübergehender Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b9415-108">Sets the length of time that Delivery Optimization (DO) tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="b9415-109">Bei einem Fortschritt wird der Timer zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="b9415-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9415-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9415-110">Syntax</span></span>


```C++
HRESULT SetNoProgressTimeout(
  [in] ULONG RetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="b9415-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="b9415-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9415-112">*RetryPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b9415-112">*RetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b9415-113">Die Zeitspanne in Sekunden, die versucht, die Datei zu übertragen, nachdem kein Fortschritt unternommen wurde.</span><span class="sxs-lookup"><span data-stu-id="b9415-113">Length of time, in seconds, that DO tries to transfer the file after there has been no progress made.</span></span> <span data-ttu-id="b9415-114">Der standardmäßige Wiederholungs Zeitraum für einen Auftrag mit hoher Priorität beträgt 3600 Sekunden (1 Stunde), und für einen Auftrag mit niedriger Priorität beträgt der Wert 86400 Sekunden (24 Stunden).</span><span class="sxs-lookup"><span data-stu-id="b9415-114">The default retry period for high priority job is 3600 seconds (1 hour) and for low priority job is 86400 seconds (24 hours).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b9415-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b9415-115">Return value</span></span>

<span data-ttu-id="b9415-116">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="b9415-116">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="b9415-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b9415-117">Return code</span></span>                                                                                          | <span data-ttu-id="b9415-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b9415-118">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b9415-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="b9415-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="b9415-120">Der Wiederholungs Zeitraum wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b9415-120">Retry period successfully set.</span></span><br/>                                                            |
| <dl> <span data-ttu-id="b9415-121"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="b9415-121"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="b9415-122">Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED sein.</span><span class="sxs-lookup"><span data-stu-id="b9415-122">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b9415-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9415-123">Remarks</span></span>

<span data-ttu-id="b9415-124">Wenn der Vorgang während des Wiederholungs Zeitraums nicht fortgesetzt wird, wird der Status des Auftrags von BG_JOB_STATE_TRANSIENT_ERROR in BG_JOB_STATE_ERROR verschoben.</span><span class="sxs-lookup"><span data-stu-id="b9415-124">If DO does not make progress during the retry period, it moves the state of the job from BG_JOB_STATE_TRANSIENT_ERROR to BG_JOB_STATE_ERROR.</span></span> <span data-ttu-id="b9415-125">Wenn Sie eine Fehler Benachrichtigung anfordern, wird Ihr [**joberror**](https://www.bing.com/search?q=**JobError**) -Rückruf aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="b9415-125">If you request error notification, DO then calls your [**JobError**](https://www.bing.com/search?q=**JobError**) callback.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9415-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9415-126">Requirements</span></span>



| <span data-ttu-id="b9415-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9415-127">Requirement</span></span> | <span data-ttu-id="b9415-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b9415-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b9415-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9415-129">Minimum supported client</span></span><br/> | <span data-ttu-id="b9415-130">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9415-130">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b9415-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9415-131">Minimum supported server</span></span><br/> | <span data-ttu-id="b9415-132">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9415-132">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b9415-133">Header</span><span class="sxs-lookup"><span data-stu-id="b9415-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9415-134"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9415-134"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="b9415-135">IDL</span><span class="sxs-lookup"><span data-stu-id="b9415-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b9415-136"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b9415-136"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="b9415-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b9415-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="b9415-138"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b9415-138"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="b9415-139">DLL</span><span class="sxs-lookup"><span data-stu-id="b9415-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9415-140"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9415-140"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="b9415-141">IID</span><span class="sxs-lookup"><span data-stu-id="b9415-141">IID</span></span><br/>                      | <span data-ttu-id="b9415-142">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="b9415-142">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b9415-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9415-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9415-144">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="b9415-144">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="b9415-145">**Ibackgroundcopyjob:: getnoprogresstimeout**</span><span class="sxs-lookup"><span data-stu-id="b9415-145">**IBackgroundCopyJob::GetNoProgressTimeout**</span></span>](ibackgroundcopyjob-getnoprogresstimeout.md)
</dt> </dl>

 

 





