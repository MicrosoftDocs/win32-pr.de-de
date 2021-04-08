---
title: Ibackgroundcopyjob GetState-Methode (deliveryoptimization. h)
description: Ruft den Status des Auftrags ab.
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- GetState-Methode
- GetState-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetState-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b195377a44cab8f336bae8090bacc5ca5624d7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741720"
---
# <a name="ibackgroundcopyjobgetstate-method"></a><span data-ttu-id="bc844-106">Ibackgroundcopyjob:: GetState-Methode</span><span class="sxs-lookup"><span data-stu-id="bc844-106">IBackgroundCopyJob::GetState method</span></span>

<span data-ttu-id="bc844-107">Ruft den Status des Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="bc844-107">Retrieves the state of the job.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc844-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc844-108">Syntax</span></span>


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a><span data-ttu-id="bc844-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bc844-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc844-110">*pjobstate* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bc844-110">*pJobState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bc844-111">Der Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="bc844-111">The state of the job.</span></span> <span data-ttu-id="bc844-112">Der Status gibt beispielsweise an, ob der Auftrag fehlerhaft ist, Daten überträgt oder angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="bc844-112">For example, the state reflects whether the job is in error, transferring data, or suspended.</span></span> <span data-ttu-id="bc844-113">Eine Liste der Auftrags Zustände finden Sie in der [**BG_JOB_STATE**](bg-job-state-.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="bc844-113">For a list of job states, see the [**BG_JOB_STATE**](bg-job-state-.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc844-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bc844-114">Return value</span></span>

<span data-ttu-id="bc844-115">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="bc844-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="bc844-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="bc844-116">Return code</span></span>                                                                              | <span data-ttu-id="bc844-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc844-117">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="bc844-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="bc844-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="bc844-119">Der Status des Auftrags wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="bc844-119">The state of the job was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bc844-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bc844-120">Remarks</span></span>

<span data-ttu-id="bc844-121">Wenn Sie wissen möchten, ob ein Auftrag fehlerhaft ist oder alle Dateien im Auftrag übertragen haben, können Sie diese Methode verwenden, um den Status des Auftrags abzurufen, oder Sie können sich registrieren, um eine Benachrichtigung zu erhalten, wenn Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="bc844-121">If you want to know when a job is in error or has transferred all the files in the job, you can use this method to poll for the state of the job or you can register to receive notification when events occur.</span></span> <span data-ttu-id="bc844-122">Ausführliche Informationen zum Registrieren von für den Empfang von Ereignis Benachrichtigungen finden Sie unter [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="bc844-122">For details on registering to receive event notification, see the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc844-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bc844-123">Requirements</span></span>



| <span data-ttu-id="bc844-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bc844-124">Requirement</span></span> | <span data-ttu-id="bc844-125">Wert</span><span class="sxs-lookup"><span data-stu-id="bc844-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc844-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bc844-126">Minimum supported client</span></span><br/> | <span data-ttu-id="bc844-127">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc844-127">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bc844-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bc844-128">Minimum supported server</span></span><br/> | <span data-ttu-id="bc844-129">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bc844-129">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="bc844-130">Header</span><span class="sxs-lookup"><span data-stu-id="bc844-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="bc844-131"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="bc844-131"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="bc844-132">IDL</span><span class="sxs-lookup"><span data-stu-id="bc844-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bc844-133"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bc844-133"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="bc844-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bc844-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="bc844-135"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bc844-135"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="bc844-136">DLL</span><span class="sxs-lookup"><span data-stu-id="bc844-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc844-137"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc844-137"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="bc844-138">IID</span><span class="sxs-lookup"><span data-stu-id="bc844-138">IID</span></span><br/>                      | <span data-ttu-id="bc844-139">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="bc844-139">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="bc844-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc844-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc844-141">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="bc844-141">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="bc844-142">**BG_JOB_STATE**</span><span class="sxs-lookup"><span data-stu-id="bc844-142">**BG_JOB_STATE**</span></span>](bg-job-state-.md)
</dt> <dt>

[<span data-ttu-id="bc844-143">**Ibackgroundcopycallback**</span><span class="sxs-lookup"><span data-stu-id="bc844-143">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> </dl>

 

 





