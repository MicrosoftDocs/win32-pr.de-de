---
title: Ibackgroundcopyjob gettimes-Methode (deliveryoptimization. h)
description: Ruft auftragsbezogene Zeitstempel ab, z. b. den Zeitpunkt, zu dem der Auftrag erstellt oder zuletzt geändert wurde.
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- Gettimes-Methode
- Gettimes-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, gettimes-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 04e779b59e0976e77b287bc575f3b08f8d39340a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104477031"
---
# <a name="ibackgroundcopyjobgettimes-method"></a><span data-ttu-id="5e77f-106">Ibackgroundcopyjob:: gettimes-Methode</span><span class="sxs-lookup"><span data-stu-id="5e77f-106">IBackgroundCopyJob::GetTimes method</span></span>

<span data-ttu-id="5e77f-107">Ruft auftragsbezogene Zeitstempel ab, z. b. den Zeitpunkt, zu dem der Auftrag erstellt oder zuletzt geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="5e77f-107">Retrieves job-related time stamps, such as the time that the job was created or last modified.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e77f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e77f-108">Syntax</span></span>


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a><span data-ttu-id="5e77f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e77f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e77f-110">*ptimes* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5e77f-110">*pTimes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5e77f-111">Enthält auftragsbezogene Zeitstempel.</span><span class="sxs-lookup"><span data-stu-id="5e77f-111">Contains job-related time stamps.</span></span> <span data-ttu-id="5e77f-112">Informationen zu verfügbaren Zeitstempeln finden Sie in der [**BG_JOB_TIMES**](bg-job-times.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="5e77f-112">For available time stamps, see the [**BG_JOB_TIMES**](bg-job-times.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e77f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e77f-113">Return value</span></span>

<span data-ttu-id="5e77f-114">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="5e77f-114">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="5e77f-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5e77f-115">Return code</span></span>                                                                              | <span data-ttu-id="5e77f-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e77f-116">Description</span></span>                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="5e77f-117"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="5e77f-117"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="5e77f-118">Die Zeitstempel konnten erfolgreich abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5e77f-118">Time stamps were successfully retrieved.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5e77f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e77f-119">Requirements</span></span>



| <span data-ttu-id="5e77f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e77f-120">Requirement</span></span> | <span data-ttu-id="5e77f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5e77f-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e77f-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e77f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5e77f-123">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e77f-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5e77f-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e77f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5e77f-125">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e77f-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="5e77f-126">Header</span><span class="sxs-lookup"><span data-stu-id="5e77f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e77f-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5e77f-127"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="5e77f-128">IDL</span><span class="sxs-lookup"><span data-stu-id="5e77f-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5e77f-129"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="5e77f-129"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="5e77f-130">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e77f-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="5e77f-131"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5e77f-131"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="5e77f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="5e77f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5e77f-133"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5e77f-133"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="5e77f-134">IID</span><span class="sxs-lookup"><span data-stu-id="5e77f-134">IID</span></span><br/>                      | <span data-ttu-id="5e77f-135">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="5e77f-135">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5e77f-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e77f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e77f-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="5e77f-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="5e77f-138">**BG_JOB_TIMES**</span><span class="sxs-lookup"><span data-stu-id="5e77f-138">**BG_JOB_TIMES**</span></span>](bg-job-times.md)
</dt> </dl>

 

 





