---
title: Ibackgroundcopyjob GetProgress-Methode (deliveryoptimization. h)
description: Ruft auftragsbezogene Statusinformationen ab, wie z. b. die Anzahl der Bytes und übertragenen Dateien.
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- GetProgress-Methode
- GetProgress-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetProgress-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d49a040bb5656ae6ef6d926a45b31808623e399b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103953"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a><span data-ttu-id="579b9-106">Ibackgroundcopyjob:: GetProgress-Methode</span><span class="sxs-lookup"><span data-stu-id="579b9-106">IBackgroundCopyJob::GetProgress method</span></span>

<span data-ttu-id="579b9-107">Ruft auftragsbezogene Statusinformationen ab, wie z. b. die Anzahl der Bytes und übertragenen Dateien.</span><span class="sxs-lookup"><span data-stu-id="579b9-107">Retrieves job-related progress information, such as the number of bytes and files transferred.</span></span>

## <a name="syntax"></a><span data-ttu-id="579b9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="579b9-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="579b9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="579b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="579b9-110">*pprogress* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="579b9-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="579b9-111">Enthält Daten, die Sie verwenden können, um den Prozentsatz des abgeschlossenen Auftrags zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="579b9-111">Contains data that you can use to calculate the percentage of the job that is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="579b9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="579b9-112">Return value</span></span>

<span data-ttu-id="579b9-113">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="579b9-113">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="579b9-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="579b9-114">Return code</span></span>                                                                              | <span data-ttu-id="579b9-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="579b9-115">Description</span></span>                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="579b9-116"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="579b9-116"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="579b9-117">Die Fortschrittsinformationen wurden erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="579b9-117">Progress information was successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="579b9-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="579b9-118">Requirements</span></span>



| <span data-ttu-id="579b9-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="579b9-119">Requirement</span></span> | <span data-ttu-id="579b9-120">Wert</span><span class="sxs-lookup"><span data-stu-id="579b9-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="579b9-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="579b9-121">Minimum supported client</span></span><br/> | <span data-ttu-id="579b9-122">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="579b9-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="579b9-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="579b9-123">Minimum supported server</span></span><br/> | <span data-ttu-id="579b9-124">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="579b9-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="579b9-125">Header</span><span class="sxs-lookup"><span data-stu-id="579b9-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="579b9-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="579b9-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="579b9-127">IDL</span><span class="sxs-lookup"><span data-stu-id="579b9-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="579b9-128"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="579b9-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="579b9-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="579b9-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="579b9-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="579b9-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="579b9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="579b9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="579b9-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="579b9-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="579b9-133">IID</span><span class="sxs-lookup"><span data-stu-id="579b9-133">IID</span></span><br/>                      | <span data-ttu-id="579b9-134">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="579b9-134">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="579b9-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="579b9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="579b9-136">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="579b9-136">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





