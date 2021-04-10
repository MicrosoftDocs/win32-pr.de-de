---
title: Ibackgroundcopyjob GetType-Methode (deliveryoptimization. h)
description: Ruft den Übertragungstyp ab, wie z. b. das herunterladen oder Hochladen von Dateien.
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType-Methode
- GetType-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetType-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040253"
---
# <a name="ibackgroundcopyjobgettype-method"></a><span data-ttu-id="a4ef6-106">Ibackgroundcopyjob:: GetType-Methode</span><span class="sxs-lookup"><span data-stu-id="a4ef6-106">IBackgroundCopyJob::GetType method</span></span>

<span data-ttu-id="a4ef6-107">Ruft den Übertragungstyp ab, wie z. b. das herunterladen oder Hochladen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-107">Retrieves the type of transfer being performed, such as a file download or upload.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4ef6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a4ef6-108">Syntax</span></span>


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a><span data-ttu-id="a4ef6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a4ef6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4ef6-110">*pjobtype* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a4ef6-110">*pJobType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a4ef6-111">Der Übertragungstyp, der ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-111">Type of transfer being performed.</span></span> <span data-ttu-id="a4ef6-112">Eine Liste der Übertragungs Typen finden Sie in der [**BG_JOB_TYPE**](bg-job-type.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-112">For a list of transfer types, see the [**BG_JOB_TYPE**](bg-job-type.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4ef6-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a4ef6-113">Return value</span></span>

<span data-ttu-id="a4ef6-114">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="a4ef6-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a4ef6-115">Return code</span></span>                                                                              | <span data-ttu-id="a4ef6-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a4ef6-116">Description</span></span>                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="a4ef6-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="a4ef6-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="a4ef6-118">Der Übertragungstyp wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-118">Transfer type was successfully retrieved.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a4ef6-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4ef6-119">Remarks</span></span>

<span data-ttu-id="a4ef6-120">Geben Sie den Übertragungstyp beim Erstellen des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-120">Specify the type of transfer when you create the job.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4ef6-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4ef6-121">Requirements</span></span>



| <span data-ttu-id="a4ef6-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4ef6-122">Requirement</span></span> | <span data-ttu-id="a4ef6-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a4ef6-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4ef6-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4ef6-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a4ef6-125">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4ef6-125">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a4ef6-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4ef6-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a4ef6-127">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4ef6-127">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="a4ef6-128">Header</span><span class="sxs-lookup"><span data-stu-id="a4ef6-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4ef6-129"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4ef6-129"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="a4ef6-130">IDL</span><span class="sxs-lookup"><span data-stu-id="a4ef6-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a4ef6-131"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a4ef6-131"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="a4ef6-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a4ef6-132">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4ef6-133"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a4ef6-133"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="a4ef6-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a4ef6-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a4ef6-135"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4ef6-135"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="a4ef6-136">IID</span><span class="sxs-lookup"><span data-stu-id="a4ef6-136">IID</span></span><br/>                      | <span data-ttu-id="a4ef6-137">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="a4ef6-137">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="a4ef6-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4ef6-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4ef6-139">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="a4ef6-139">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="a4ef6-140">**BG_JOB_TYPE**</span><span class="sxs-lookup"><span data-stu-id="a4ef6-140">**BG_JOB_TYPE**</span></span>](bg-job-type.md)
</dt> <dt>

[<span data-ttu-id="a4ef6-141">**Ibackgroundcopymanager:: kreatejob**</span><span class="sxs-lookup"><span data-stu-id="a4ef6-141">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





