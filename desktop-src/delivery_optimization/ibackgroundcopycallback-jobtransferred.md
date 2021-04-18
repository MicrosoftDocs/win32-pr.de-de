---
title: Ibackgroundcopycallback-jobtransfer-Methode (deliveryoptimization. h)
description: Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der jobübertragene Methode auf, wenn alle Dateien im Auftrag erfolgreich übertragen wurden.
ms.assetid: D3088279-2D26-4707-9BA2-19D2758EA1CC
keywords:
- Jobübertragene Methode
- Jobtransfer-Methode, ibackgroundcopycallback-Schnittstelle
- Ibackgroundcopycallback-Schnittstelle, jobtransfer-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobTransferred
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6c5c358978da1731152ca6f7de8c3f7a92a1da86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103514"
---
# <a name="ibackgroundcopycallbackjobtransferred-method"></a><span data-ttu-id="140de-106">Ibackgroundcopycallback:: jobtransfer-Methode</span><span class="sxs-lookup"><span data-stu-id="140de-106">IBackgroundCopyCallback::JobTransferred method</span></span>

<span data-ttu-id="140de-107">Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der **jobübertragene** Methode auf, wenn alle Dateien im Auftrag erfolgreich übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="140de-107">Delivery Optimization (DO) calls your implementation of the **JobTransferred** method when all of the files in the job have been successfully transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="140de-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="140de-108">Syntax</span></span>


```C++
HRESULT JobTransferred(
  [in] IBackgroundCopyJob *pJob
);
```



## <a name="parameters"></a><span data-ttu-id="140de-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="140de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="140de-110">*pjob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="140de-110">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="140de-111">Enthält auftragsbezogene Informationen, wie z. b. den Zeitpunkt, zu dem der Auftrag abgeschlossen wurde, die Anzahl der übertragenen Bytes und die Anzahl der übertragenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="140de-111">Contains job-related information, such as the time the job completed, the number of bytes transferred, and the number of files transferred.</span></span> <span data-ttu-id="140de-112">*Pjob* nicht freigeben; Gibt die-Schnittstelle frei, wenn die-Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="140de-112">Do not release *pJob*; DO releases the interface when the method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="140de-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="140de-113">Return value</span></span>

<span data-ttu-id="140de-114">Diese Methode sollte S_OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="140de-114">This method should return S_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="140de-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="140de-115">Remarks</span></span>

<span data-ttu-id="140de-116">In der Regel sollte Ihre Implementierung die [**ibackgroundcopyjob:: Complete**](ibackgroundcopyjob-complete.md) -Methode anrufen, um zu bestätigen, dass die Dateien erfolgreich übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="140de-116">Typically, your implementation should call the [**IBackgroundCopyJob::Complete**](ibackgroundcopyjob-complete.md) method to acknowledge that DO successfully transferred the files.</span></span> <span data-ttu-id="140de-117">Download Dateien und die Antwortdatei sind auf dem Client erst verfügbar, wenn Sie die **Complete** -Methode aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="140de-117">Download files and the reply file are not available on the client until you call the **Complete** method.</span></span>

<span data-ttu-id="140de-118">Wenn Sie die [**Complete**](ibackgroundcopyjob-complete.md) -Methode oder die [**ibackgroundcopyjob:: Cancel**](ibackgroundcopyjob-cancel.md) -Methode nicht aufzurufen, wird der Auftrag nach 30 Tagen abgebrochen, und die unvollständigen Dateien werden gelöscht.</span><span class="sxs-lookup"><span data-stu-id="140de-118">If you do not call the [**Complete**](ibackgroundcopyjob-complete.md) method or the [**IBackgroundCopyJob::Cancel**](ibackgroundcopyjob-cancel.md) method DO cancels the job after 30 days and deletes the incomplete files.</span></span>

## <a name="requirements"></a><span data-ttu-id="140de-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="140de-119">Requirements</span></span>



| <span data-ttu-id="140de-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="140de-120">Requirement</span></span> | <span data-ttu-id="140de-121">Wert</span><span class="sxs-lookup"><span data-stu-id="140de-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="140de-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="140de-122">Minimum supported client</span></span><br/> | <span data-ttu-id="140de-123">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="140de-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="140de-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="140de-124">Minimum supported server</span></span><br/> | <span data-ttu-id="140de-125">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="140de-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="140de-126">Header</span><span class="sxs-lookup"><span data-stu-id="140de-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="140de-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="140de-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="140de-128">IDL</span><span class="sxs-lookup"><span data-stu-id="140de-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="140de-129"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="140de-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="140de-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="140de-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="140de-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="140de-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="140de-132">DLL</span><span class="sxs-lookup"><span data-stu-id="140de-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="140de-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="140de-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="140de-134">IID</span><span class="sxs-lookup"><span data-stu-id="140de-134">IID</span></span><br/>                      | <span data-ttu-id="140de-135">IID_IBackgroundCopyCallback ist als 97ea99c7-0186-4ad4-8df9-c5b4e0ed6b22 definiert.</span><span class="sxs-lookup"><span data-stu-id="140de-135">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="140de-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="140de-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="140de-137">**Ibackgroundcopycallback**</span><span class="sxs-lookup"><span data-stu-id="140de-137">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="140de-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="140de-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="140de-139">**Ibackgroundcopyjob:: Complete**</span><span class="sxs-lookup"><span data-stu-id="140de-139">**IBackgroundCopyJob::Complete**</span></span>](ibackgroundcopyjob-complete.md)
</dt> <dt>

[<span data-ttu-id="140de-140">**Ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="140de-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> </dl>

 

 





