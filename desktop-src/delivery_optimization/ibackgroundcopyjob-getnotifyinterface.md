---
title: Ibackgroundcopyjob getnotifyinterface-Methode (deliveryoptimization. h)
description: Ruft den Schnittstellen Zeiger auf die Implementierung der ibackgroundcopycallback-Schnittstelle ab.
ms.assetid: 1AA50C03-AC84-4AA9-8EC3-3FBA865C70C0
keywords:
- Getnotifyinterface-Methode
- Getnotifyinterface-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, getnotifyinterface-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6586a90de5783ceb24e5a7677f699a9cf6dfa60c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346340"
---
# <a name="ibackgroundcopyjobgetnotifyinterface-method"></a><span data-ttu-id="0a184-106">Ibackgroundcopyjob:: getnotifyinterface-Methode</span><span class="sxs-lookup"><span data-stu-id="0a184-106">IBackgroundCopyJob::GetNotifyInterface method</span></span>

<span data-ttu-id="0a184-107">Ruft den Schnittstellen Zeiger auf die Implementierung der [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="0a184-107">Retrieves the interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a184-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a184-108">Syntax</span></span>


```C++
HRESULT GetNotifyInterface(
  [out] IUnknown **ppNotifyInterface
);
```



## <a name="parameters"></a><span data-ttu-id="0a184-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a184-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a184-110">*ppnotifyinterface* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0a184-110">*ppNotifyInterface* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a184-111">Ein Schnittstellen Zeiger auf Ihre Implementierung der [**ibackgroundcopycallback**](ibackgroundcopycallback.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="0a184-111">Interface pointer to your implementation of the [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) interface.</span></span> <span data-ttu-id="0a184-112">Wenn Sie dies erledigt haben, Release *ppnotifyinterface*.</span><span class="sxs-lookup"><span data-stu-id="0a184-112">When done, release *ppNotifyInterface*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a184-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0a184-113">Return value</span></span>

<span data-ttu-id="0a184-114">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="0a184-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="0a184-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0a184-115">Return code</span></span>                                                                              | <span data-ttu-id="0a184-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a184-116">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="0a184-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="0a184-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="0a184-118">Der Benachrichtigungs Schnittstellen Zeiger wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="0a184-118">Notification interface pointer was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0a184-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0a184-119">Requirements</span></span>



| <span data-ttu-id="0a184-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0a184-120">Requirement</span></span> | <span data-ttu-id="0a184-121">Wert</span><span class="sxs-lookup"><span data-stu-id="0a184-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0a184-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0a184-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0a184-123">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a184-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0a184-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0a184-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0a184-125">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0a184-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0a184-126">Header</span><span class="sxs-lookup"><span data-stu-id="0a184-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a184-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a184-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0a184-128">IDL</span><span class="sxs-lookup"><span data-stu-id="0a184-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0a184-129"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0a184-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0a184-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0a184-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="0a184-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0a184-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0a184-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0a184-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a184-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a184-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0a184-134">IID</span><span class="sxs-lookup"><span data-stu-id="0a184-134">IID</span></span><br/>                      | <span data-ttu-id="0a184-135">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="0a184-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="0a184-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a184-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a184-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="0a184-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="0a184-138">**Ibackgroundcopycallback**</span><span class="sxs-lookup"><span data-stu-id="0a184-138">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="0a184-139">**Ibackgroundcopyjob:: getnotifyflags**</span><span class="sxs-lookup"><span data-stu-id="0a184-139">**IBackgroundCopyJob::GetNotifyFlags**</span></span>](ibackgroundcopyjob-getnotifyflags.md)
</dt> <dt>

[<span data-ttu-id="0a184-140">**Ibackgroundcopyjob:: setnotifyinterface**</span><span class="sxs-lookup"><span data-stu-id="0a184-140">**IBackgroundCopyJob::SetNotifyInterface**</span></span>](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

 





