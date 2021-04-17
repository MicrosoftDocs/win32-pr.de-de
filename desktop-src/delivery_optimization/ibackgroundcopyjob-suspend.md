---
title: Ibackgroundcopyjob Suspend-Methode (deliveryoptimization. h)
description: Hält einen Auftrag an. Neue Aufträge, Aufträge mit Fehlern und Aufträge, die die Übertragung von Dateien abgeschlossen haben, werden automatisch angehalten.
ms.assetid: 23EED354-A3AC-4865-8C06-ADA097851F96
keywords:
- Suspend-Methode
- Suspend-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, Suspend-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Suspend
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: dd4464a04f87a7759e9b51974eef2188ba1d0c2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391910"
---
# <a name="ibackgroundcopyjobsuspend-method"></a><span data-ttu-id="9a7f6-107">Ibackgroundcopyjob:: Suspend-Methode</span><span class="sxs-lookup"><span data-stu-id="9a7f6-107">IBackgroundCopyJob::Suspend method</span></span>

<span data-ttu-id="9a7f6-108">Hält einen Auftrag an.</span><span class="sxs-lookup"><span data-stu-id="9a7f6-108">Suspends a job.</span></span> <span data-ttu-id="9a7f6-109">Neue Aufträge, Aufträge mit Fehlern und Aufträge, die die Übertragung von Dateien abgeschlossen haben, werden automatisch angehalten.</span><span class="sxs-lookup"><span data-stu-id="9a7f6-109">New jobs, jobs that are in error, and jobs that have finished transferring files are automatically suspended.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a7f6-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a7f6-110">Syntax</span></span>


```C++
HRESULT Suspend();
```



## <a name="parameters"></a><span data-ttu-id="9a7f6-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a7f6-111">Parameters</span></span>

<span data-ttu-id="9a7f6-112">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9a7f6-112">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a7f6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a7f6-113">Return value</span></span>

<span data-ttu-id="9a7f6-114">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="9a7f6-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="9a7f6-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9a7f6-115">Return code</span></span>                                                                                          | <span data-ttu-id="9a7f6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a7f6-116">Description</span></span>                                                                                          |
|------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9a7f6-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="9a7f6-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>             | <span data-ttu-id="9a7f6-118">Der Auftrag wurde erfolgreich angehalten.</span><span class="sxs-lookup"><span data-stu-id="9a7f6-118">Successfully suspended the job.</span></span><br/>                                                           |
| <dl> <span data-ttu-id="9a7f6-119"><dt>**DO_E_INVALID_STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="9a7f6-119"><dt>**DO_E_INVALID_STATE**</dt></span></span> </dl> | <span data-ttu-id="9a7f6-120">Der Status des Auftrags kann nicht BG_JOB_STATE_CANCELLED oder BG_JOB_STATE_ACKNOWLEDGED sein.</span><span class="sxs-lookup"><span data-stu-id="9a7f6-120">The state of the job cannot be BG_JOB_STATE_CANCELLED or BG_JOB_STATE_ACKNOWLEDGED.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="9a7f6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a7f6-121">Requirements</span></span>



| <span data-ttu-id="9a7f6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a7f6-122">Requirement</span></span> | <span data-ttu-id="9a7f6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="9a7f6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a7f6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9a7f6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="9a7f6-125">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a7f6-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="9a7f6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9a7f6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="9a7f6-127">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9a7f6-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="9a7f6-128">Header</span><span class="sxs-lookup"><span data-stu-id="9a7f6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="9a7f6-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="9a7f6-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="9a7f6-130">IDL</span><span class="sxs-lookup"><span data-stu-id="9a7f6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9a7f6-131"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9a7f6-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="9a7f6-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a7f6-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="9a7f6-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9a7f6-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="9a7f6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9a7f6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9a7f6-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9a7f6-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="9a7f6-136">IID</span><span class="sxs-lookup"><span data-stu-id="9a7f6-136">IID</span></span><br/>                      | <span data-ttu-id="9a7f6-137">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="9a7f6-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="9a7f6-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a7f6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a7f6-139">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="9a7f6-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="9a7f6-140">**Ibackgroundcopyjob:: Cancel**</span><span class="sxs-lookup"><span data-stu-id="9a7f6-140">**IBackgroundCopyJob::Cancel**</span></span>](ibackgroundcopyjob-cancel.md)
</dt> <dt>

[<span data-ttu-id="9a7f6-141">**Ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="9a7f6-141">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>

 

 





