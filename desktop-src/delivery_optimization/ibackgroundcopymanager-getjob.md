---
title: Ibackgroundcopymanager GetJob-Methode (deliveryoptimization. h)
description: Ruft einen angegebenen Auftrag aus der Übertragungs Warteschlange ab. In der Regel speichert Ihre Anwendung die Auftrags Kennung, sodass Sie den Auftrag später aus der Warteschlange abrufen können.
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- GetJob-Methode
- GetJob-Methode, ibackgroundcopymanager-Schnittstelle
- Ibackgroundcopymanager-Schnittstelle, GetJob-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a59956e68b5b656e7182e62969b3212c2ef6732c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342017"
---
# <a name="ibackgroundcopymanagergetjob-method"></a><span data-ttu-id="12ec2-107">Ibackgroundcopymanager:: GetJob-Methode</span><span class="sxs-lookup"><span data-stu-id="12ec2-107">IBackgroundCopyManager::GetJob method</span></span>

<span data-ttu-id="12ec2-108">Ruft einen angegebenen Auftrag aus der Übertragungs Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="12ec2-108">Retrieves a specified job from the transfer queue.</span></span> <span data-ttu-id="12ec2-109">In der Regel speichert Ihre Anwendung die Auftrags Kennung, sodass Sie den Auftrag später aus der Warteschlange abrufen können.</span><span class="sxs-lookup"><span data-stu-id="12ec2-109">Typically, your application persists the job identifier, so you can later retrieve the job from the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="12ec2-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="12ec2-110">Syntax</span></span>


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="12ec2-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="12ec2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12ec2-112">*JobID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="12ec2-112">*JobID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="12ec2-113">Identifiziert den Auftrag, der aus der Übertragungs Warteschlange abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="12ec2-113">Identifies the job to retrieve from the transfer queue.</span></span> <span data-ttu-id="12ec2-114">Die Methode " [**kreatejob**](ibackgroundcopymanager-createjob.md) " gibt den Auftrags Bezeichner zurück.</span><span class="sxs-lookup"><span data-stu-id="12ec2-114">The [**CreateJob**](ibackgroundcopymanager-createjob.md) method returns the job identifier.</span></span>

</dd> <dt>

<span data-ttu-id="12ec2-115">*ppjob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="12ec2-115">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="12ec2-116">Ein [**ibackgroundcopyjob**](ibackgroundcopyjob-.md) -Schnittstellen Zeiger auf den von *JobID* angegebenen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="12ec2-116">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer to the job specified by *JobID*.</span></span> <span data-ttu-id="12ec2-117">Wenn Sie den Vorgang abgeschlossen haben, geben Sie *ppjob* frei</span><span class="sxs-lookup"><span data-stu-id="12ec2-117">When done, release *ppJob*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12ec2-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12ec2-118">Return value</span></span>

<span data-ttu-id="12ec2-119">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="12ec2-119">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="12ec2-120">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="12ec2-120">Return code</span></span>                                                                                      | <span data-ttu-id="12ec2-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="12ec2-121">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="12ec2-122"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="12ec2-122"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>         | <span data-ttu-id="12ec2-123">Der Auftrag wurde erfolgreich aus der Übertragungs Warteschlange abgerufen.</span><span class="sxs-lookup"><span data-stu-id="12ec2-123">Job was successfully retrieved from the transfer queue.</span></span><br/> |
| <dl> <span data-ttu-id="12ec2-124"><dt>**DO_E_NOT_FOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="12ec2-124"><dt>**DO_E_NOT_FOUND**</dt></span></span> </dl> | <span data-ttu-id="12ec2-125">Der Auftrag wurde nicht in der Warteschlange gefunden.</span><span class="sxs-lookup"><span data-stu-id="12ec2-125">The job was not found in the queue.</span></span><br/>                     |
| <dl> <span data-ttu-id="12ec2-126"><dt>**E_ACCESSDENIED**</dt></span><span class="sxs-lookup"><span data-stu-id="12ec2-126"><dt>**E_ACCESSDENIED**</dt></span></span> </dl>   | <span data-ttu-id="12ec2-127">Der Benutzer verfügt nicht über die Berechtigung zum Abrufen des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="12ec2-127">User does not have permission to retrieve the job.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="12ec2-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12ec2-128">Requirements</span></span>



| <span data-ttu-id="12ec2-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12ec2-129">Requirement</span></span> | <span data-ttu-id="12ec2-130">Wert</span><span class="sxs-lookup"><span data-stu-id="12ec2-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12ec2-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="12ec2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="12ec2-132">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12ec2-132">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="12ec2-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="12ec2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="12ec2-134">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="12ec2-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="12ec2-135">Header</span><span class="sxs-lookup"><span data-stu-id="12ec2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="12ec2-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="12ec2-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="12ec2-137">IDL</span><span class="sxs-lookup"><span data-stu-id="12ec2-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="12ec2-138"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="12ec2-138"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="12ec2-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="12ec2-139">Library</span></span><br/>                  | <dl> <span data-ttu-id="12ec2-140"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="12ec2-140"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="12ec2-141">DLL</span><span class="sxs-lookup"><span data-stu-id="12ec2-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="12ec2-142"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="12ec2-142"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="12ec2-143">IID</span><span class="sxs-lookup"><span data-stu-id="12ec2-143">IID</span></span><br/>                      | <span data-ttu-id="12ec2-144">IID_IBackgroundCopyManager ist als 5ce34c0d-0dc9-4c1f -897c-daa1b78cee7c definiert.</span><span class="sxs-lookup"><span data-stu-id="12ec2-144">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="12ec2-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12ec2-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12ec2-146">**Ibackgroundcopymanager**</span><span class="sxs-lookup"><span data-stu-id="12ec2-146">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="12ec2-147">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="12ec2-147">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="12ec2-148">**Ibackgroundcopyjob:: GetId**</span><span class="sxs-lookup"><span data-stu-id="12ec2-148">**IBackgroundCopyJob::GetId**</span></span>](ibackgroundcopyjob-getid.md)
</dt> <dt>

[<span data-ttu-id="12ec2-149">**Ibackgroundcopymanager:: kreatejob**</span><span class="sxs-lookup"><span data-stu-id="12ec2-149">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





