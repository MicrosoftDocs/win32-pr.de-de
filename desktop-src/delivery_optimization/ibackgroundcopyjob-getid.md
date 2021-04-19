---
title: Ibackgroundcopyjob GetId-Methode (deliveryoptimization. h)
description: Ruft den Bezeichner ab, der zum Identifizieren des Auftrags in der Warteschlange verwendet wird.
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId-Methode
- GetId-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetId-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ade12d72d68b43df7d9ae3d1f33010bb95b7052a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339968"
---
# <a name="ibackgroundcopyjobgetid-method"></a><span data-ttu-id="967d9-106">Ibackgroundcopyjob:: GetId-Methode</span><span class="sxs-lookup"><span data-stu-id="967d9-106">IBackgroundCopyJob::GetId method</span></span>

<span data-ttu-id="967d9-107">Ruft den Bezeichner ab, der zum Identifizieren des Auftrags in der Warteschlange verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="967d9-107">Retrieves the identifier used to identify the job in the queue.</span></span>

## <a name="syntax"></a><span data-ttu-id="967d9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="967d9-108">Syntax</span></span>


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a><span data-ttu-id="967d9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="967d9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="967d9-110">*pjobid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="967d9-110">*pJobID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="967d9-111">GUID, die den Auftrag innerhalb der do-Warteschlange identifiziert.</span><span class="sxs-lookup"><span data-stu-id="967d9-111">GUID that identifies the job within the DO queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="967d9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="967d9-112">Return value</span></span>

<span data-ttu-id="967d9-113">Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="967d9-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="remarks"></a><span data-ttu-id="967d9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="967d9-114">Remarks</span></span>

<span data-ttu-id="967d9-115">Der Dienst generiert den Bezeichner, wenn Sie den Auftrag [Erstellen](ibackgroundcopymanager-createjob.md) .</span><span class="sxs-lookup"><span data-stu-id="967d9-115">The service generates the identifier when you [create](ibackgroundcopymanager-createjob.md) the job.</span></span> <span data-ttu-id="967d9-116">Um den Bezeichner zum Abrufen eines [**ibackgroundcopyjob**](ibackgroundcopyjob-.md) -Schnittstellen Zeigers für den Auftrag zu verwenden, rufen Sie die [**ibackgroundcopymanager:: GetJob**](ibackgroundcopymanager-getjob.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="967d9-116">To use the identifier to retrieve an [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) interface pointer for the job, call the [**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="967d9-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="967d9-117">Requirements</span></span>



| <span data-ttu-id="967d9-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="967d9-118">Requirement</span></span> | <span data-ttu-id="967d9-119">Wert</span><span class="sxs-lookup"><span data-stu-id="967d9-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="967d9-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="967d9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="967d9-121">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="967d9-121">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="967d9-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="967d9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="967d9-123">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="967d9-123">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="967d9-124">Header</span><span class="sxs-lookup"><span data-stu-id="967d9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="967d9-125"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="967d9-125"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="967d9-126">IDL</span><span class="sxs-lookup"><span data-stu-id="967d9-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="967d9-127"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="967d9-127"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="967d9-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="967d9-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="967d9-129"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="967d9-129"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="967d9-130">DLL</span><span class="sxs-lookup"><span data-stu-id="967d9-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="967d9-131"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="967d9-131"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="967d9-132">IID</span><span class="sxs-lookup"><span data-stu-id="967d9-132">IID</span></span><br/>                      | <span data-ttu-id="967d9-133">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="967d9-133">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="967d9-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="967d9-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="967d9-135">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="967d9-135">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="967d9-136">**Ibackgroundcopymanager:: kreatejob**</span><span class="sxs-lookup"><span data-stu-id="967d9-136">**IBackgroundCopyManager::CreateJob**</span></span>](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[<span data-ttu-id="967d9-137">**Ibackgroundcopymanager:: GetJob**</span><span class="sxs-lookup"><span data-stu-id="967d9-137">**IBackgroundCopyManager::GetJob**</span></span>](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





