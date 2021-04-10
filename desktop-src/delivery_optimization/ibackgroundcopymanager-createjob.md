---
title: IBackgroundCopyManager CreateJob-Methode (Deliveryoptimization.h)
description: Erstellt einen Auftrag.
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- Methode "kreatejob"
- Methode "kreatejob", ibackgroundcopymanager-Schnittstelle
- Ibackgroundcopymanager-Schnittstelle, Methode "kreatejob"
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/27/2021
ms.locfileid: "104050641"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a><span data-ttu-id="a425d-106">Ibackgroundcopymanager:: kreatejob-Methode</span><span class="sxs-lookup"><span data-stu-id="a425d-106">IBackgroundCopyManager::CreateJob method</span></span>

<span data-ttu-id="a425d-107">Erstellt einen Auftrag.</span><span class="sxs-lookup"><span data-stu-id="a425d-107">Creates a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="a425d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a425d-108">Syntax</span></span>


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a><span data-ttu-id="a425d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a425d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a425d-110">*pdisplayname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a425d-110">*pDisplayName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a425d-111">Eine auf NULL endenden Zeichenfolge, die einen anzeigen Amen für den Auftrag enthält.</span><span class="sxs-lookup"><span data-stu-id="a425d-111">Null-terminated string that contains a display name for the job.</span></span> <span data-ttu-id="a425d-112">In der Regel wird der Anzeige Name verwendet, um den Auftrag auf einer Benutzeroberfläche zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="a425d-112">Typically, the display name is used to identify the job in a user interface.</span></span> <span data-ttu-id="a425d-113">Beachten Sie, dass mehr als ein Auftrag denselben anzeigen Amen aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="a425d-113">Note that more than one job may have the same display name.</span></span> <span data-ttu-id="a425d-114">Darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="a425d-114">Must not be **NULL**.</span></span> <span data-ttu-id="a425d-115">Der Name ist auf 256 Zeichen beschränkt, ohne das NULL-Terminator.</span><span class="sxs-lookup"><span data-stu-id="a425d-115">The name is limited to 256 characters, not including the null terminator.</span></span>

</dd> <dt>

<span data-ttu-id="a425d-116">*Typ* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a425d-116">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a425d-117">Typ des Übertragungs Auftrags, z. b. BG_JOB_TYPE_DOWNLOAD.</span><span class="sxs-lookup"><span data-stu-id="a425d-117">Type of transfer job, such as BG_JOB_TYPE_DOWNLOAD.</span></span> <span data-ttu-id="a425d-118">Eine Liste der Übertragungs Typen finden Sie in der [**BG_JOB_TYPE**](bg-job-type.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="a425d-118">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="a425d-119">*pjobid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a425d-119">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a425d-120">Identifiziert den Auftrag in der Warteschlange eindeutig.</span><span class="sxs-lookup"><span data-stu-id="a425d-120">Uniquely identifies your job in the queue.</span></span> <span data-ttu-id="a425d-121">Verwenden Sie diesen Bezeichner, wenn Sie die [**ibackgroundcopymanager:: GetJob**](ibackgroundcopymanager-getjob.md) -Methode aufrufen, um einen Auftrag aus der Warteschlange abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a425d-121">Use this identifier when you call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method to get a job from the queue.</span></span>

</dd> <dt>

<span data-ttu-id="a425d-122">*ppjob* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a425d-122">*ppJob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a425d-123">Ein [**ibackgroundcopyjob**](ibackgroundcopyjob-.md) -Schnittstellen Zeiger, mit dem Sie die Eigenschaften des Auftrags ändern und die zu übertragenden Dateien angeben.</span><span class="sxs-lookup"><span data-stu-id="a425d-123">An [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer that you use to modify the job's properties and specify the files to be transferred.</span></span> <span data-ttu-id="a425d-124">Um den Auftrag in der Warteschlange zu aktivieren, müssen Sie die [**ibackgroundcopyjob:: Resume**](ibackgroundcopyjob-resume.md) -Methode abrufen.</span><span class="sxs-lookup"><span data-stu-id="a425d-124">To activate the job in the queue, call the [**IBackgroundCopyJob::Resume**](ibackgroundcopyjob-resume.md) method.</span></span> <span data-ttu-id="a425d-125">Release *ppjob* , wenn dies abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="a425d-125">Release *ppJob* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a425d-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a425d-126">Return value</span></span>

<span data-ttu-id="a425d-127">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="a425d-127">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="a425d-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a425d-128">Return code</span></span>                                                                              | <span data-ttu-id="a425d-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a425d-129">Description</span></span>                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="a425d-130"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a425d-130"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="a425d-131">Der neue Auftrag wurde erfolgreich generiert.</span><span class="sxs-lookup"><span data-stu-id="a425d-131">Successfully generated the new job.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a425d-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a425d-132">Remarks</span></span>

<span data-ttu-id="a425d-133">Nur der Benutzer, der den Auftrag erstellt, oder ein Benutzer mit Administratorrechten kann [dem Auftrag Dateien hinzufügen](https://www.bing.com/search?q=add+files+to+the+job) und [die Eigenschaften des Auftrags ändern](https://www.bing.com/search?q=change+the+job's+properties).</span><span class="sxs-lookup"><span data-stu-id="a425d-133">Only the user who creates the job or a user with administrator privileges can [add files to the job](https://www.bing.com/search?q=add+files+to+the+job) and [change the job's properties](https://www.bing.com/search?q=change+the+job's+properties).</span></span>

## <a name="requirements"></a><span data-ttu-id="a425d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a425d-134">Requirements</span></span>



| <span data-ttu-id="a425d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a425d-135">Requirement</span></span> | <span data-ttu-id="a425d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a425d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a425d-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a425d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a425d-138">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a425d-138">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a425d-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a425d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a425d-140">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a425d-140">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a425d-141">Header</span><span class="sxs-lookup"><span data-stu-id="a425d-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a425d-142"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a425d-142"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a425d-143">IDL</span><span class="sxs-lookup"><span data-stu-id="a425d-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a425d-144"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a425d-144"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a425d-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a425d-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="a425d-146"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a425d-146"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a425d-147">DLL</span><span class="sxs-lookup"><span data-stu-id="a425d-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a425d-148"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a425d-148"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a425d-149">IID</span><span class="sxs-lookup"><span data-stu-id="a425d-149">IID</span></span><br/>                      | <span data-ttu-id="a425d-150">IID_IBackgroundCopyManager ist als 5ce34c0d-0dc9-4c1f -897c-daa1b78cee7c definiert.</span><span class="sxs-lookup"><span data-stu-id="a425d-150">IID_IBackgroundCopyManager is defined as 5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="a425d-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a425d-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a425d-152">**Ibackgroundcopymanager**</span><span class="sxs-lookup"><span data-stu-id="a425d-152">**IBackgroundCopyManager**</span></span>](ibackgroundcopymanager.md)
</dt> <dt>

[<span data-ttu-id="a425d-153">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="a425d-153">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a425d-154">**Ibackgroundcopyjob:: Resume**</span><span class="sxs-lookup"><span data-stu-id="a425d-154">**IBackgroundCopyJob::Resume**</span></span>](ibackgroundcopyjob-resume.md)
</dt> </dl>
