---
title: Ibackgroundcopyjob getnoprogresstimeout-Methode (deliveryoptimization. h)
description: Ruft die Zeitspanne ab, die der Dienst versucht, die Datei zu übertragen, nachdem ein vorübergehender Fehler aufgetreten ist. Bei einem Fortschritt wird der Timer zurückgesetzt.
ms.assetid: 3C31A15B-62EF-4807-8EC3-78BAEA3E23AE
keywords:
- Getnoprogresstimeout-Methode
- Getnoprogresstimeout-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, getnoprogresstimeout-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetNoProgressTimeout
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3ccd236c17612aa03a28e07a08d087454f8db6f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477034"
---
# <a name="ibackgroundcopyjobgetnoprogresstimeout-method"></a><span data-ttu-id="94237-107">Ibackgroundcopyjob:: getnoprogresstimeout-Methode</span><span class="sxs-lookup"><span data-stu-id="94237-107">IBackgroundCopyJob::GetNoProgressTimeout method</span></span>

<span data-ttu-id="94237-108">Ruft die Zeitspanne ab, die der Dienst versucht, die Datei zu übertragen, nachdem ein vorübergehender Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="94237-108">Retrieves the length of time that the service tries to transfer the file after a transient error condition occurs.</span></span> <span data-ttu-id="94237-109">Bei einem Fortschritt wird der Timer zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="94237-109">If there is progress, the timer is reset.</span></span>

## <a name="syntax"></a><span data-ttu-id="94237-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="94237-110">Syntax</span></span>


```C++
HRESULT GetNoProgressTimeout(
  [in] ULONG *pRetryPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="94237-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="94237-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94237-112">*pretryperiod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="94237-112">*pRetryPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94237-113">Zeitspanne (in Sekunden), die der Dienst versucht, die Datei zu übertragen, nachdem ein vorübergehender Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="94237-113">Length of time, in seconds, that the service tries to transfer the file after a transient error occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94237-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="94237-114">Return value</span></span>

<span data-ttu-id="94237-115">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="94237-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="94237-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="94237-116">Return code</span></span>                                                                              | <span data-ttu-id="94237-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="94237-117">Description</span></span>                                     |
|------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="94237-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="94237-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="94237-119">Das Timeout wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="94237-119">Time-out was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="94237-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94237-120">Requirements</span></span>



| <span data-ttu-id="94237-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94237-121">Requirement</span></span> | <span data-ttu-id="94237-122">Wert</span><span class="sxs-lookup"><span data-stu-id="94237-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94237-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94237-123">Minimum supported client</span></span><br/> | <span data-ttu-id="94237-124">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94237-124">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="94237-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94237-125">Minimum supported server</span></span><br/> | <span data-ttu-id="94237-126">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94237-126">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="94237-127">Header</span><span class="sxs-lookup"><span data-stu-id="94237-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="94237-128"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="94237-128"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="94237-129">IDL</span><span class="sxs-lookup"><span data-stu-id="94237-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="94237-130"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="94237-130"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="94237-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94237-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="94237-132"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94237-132"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="94237-133">DLL</span><span class="sxs-lookup"><span data-stu-id="94237-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="94237-134"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94237-134"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="94237-135">IID</span><span class="sxs-lookup"><span data-stu-id="94237-135">IID</span></span><br/>                      | <span data-ttu-id="94237-136">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="94237-136">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="94237-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="94237-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94237-138">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="94237-138">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="94237-139">**Ibackgroundcopyjob:: setnoprogresstimeout**</span><span class="sxs-lookup"><span data-stu-id="94237-139">**IBackgroundCopyJob::SetNoProgressTimeout**</span></span>](ibackgroundcopyjob-setnoprogresstimeout.md)
</dt> </dl>

 

 





