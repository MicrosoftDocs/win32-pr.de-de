---
title: Ibackgroundcopycallback jobänderungs-Methode (deliveryoptimization. h)
description: Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der jobmodifizierungsmethode auf, wenn der Auftrag geändert wurde.
ms.assetid: 4AC2575F-57FB-45E6-B29C-12DF615237F3
keywords:
- Jobänderungs-Methode
- Jobmodifikations Methode, ibackgroundcopycallback-Schnittstelle
- Ibackgroundcopycallback-Schnittstelle, jobmodifizierungs Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback.JobModification
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ceeb390fc8592c1e8e1d03efdb432056bd131a6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337318"
---
# <a name="ibackgroundcopycallbackjobmodification-method"></a><span data-ttu-id="11b89-106">Ibackgroundcopycallback:: jobänderungs-Methode</span><span class="sxs-lookup"><span data-stu-id="11b89-106">IBackgroundCopyCallback::JobModification method</span></span>

<span data-ttu-id="11b89-107">Die Übermittlungs Optimierung (Do) ruft Ihre Implementierung der [**jobmodifizierungsmethode**](https://www.bing.com/search?q=**JobModification**) auf, wenn der Auftrag geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="11b89-107">Delivery Optimization (DO) calls your implementation of the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method when the job has been modified.</span></span> <span data-ttu-id="11b89-108">Der Dienst generiert dieses Ereignis, wenn Bytes übertragen werden, Dateien dem Auftrag hinzugefügt wurden, Eigenschaften geändert wurden oder sich der Status des Auftrags geändert hat.</span><span class="sxs-lookup"><span data-stu-id="11b89-108">The service generates this event when bytes are transferred, files have been added to the job, properties have been modified, or the state of the job has changed.</span></span>

## <a name="syntax"></a><span data-ttu-id="11b89-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="11b89-109">Syntax</span></span>


```C++
HRESULT JobModification(
  [in] IBackgroundCopyJob *pJob,
  [in] DWORD              dwReserved
);
```



## <a name="parameters"></a><span data-ttu-id="11b89-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="11b89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11b89-111">*pjob* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11b89-111">*pJob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11b89-112">Enthält die Methoden zum Zugreifen auf Eigenschafts-, Status-und Zustandsinformationen des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="11b89-112">Contains the methods for accessing property, progress, and state information of the job.</span></span> <span data-ttu-id="11b89-113">*Pjob* nicht freigeben; Gibt die-Schnittstelle frei, wenn die [**jobänderungs**](https://www.bing.com/search?q=**JobModification**) -Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="11b89-113">Do not release *pJob*; DO releases the interface when the [**JobModification**](https://www.bing.com/search?q=**JobModification**) method returns.</span></span>

</dd> <dt>

<span data-ttu-id="11b89-114">*dwReserved* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11b89-114">*dwReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11b89-115">Für die zukünftige Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="11b89-115">Reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11b89-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11b89-116">Return value</span></span>

<span data-ttu-id="11b89-117">Diese Methode sollte S_OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="11b89-117">This method should return S_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="11b89-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11b89-118">Requirements</span></span>



| <span data-ttu-id="11b89-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11b89-119">Requirement</span></span> | <span data-ttu-id="11b89-120">Wert</span><span class="sxs-lookup"><span data-stu-id="11b89-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11b89-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11b89-121">Minimum supported client</span></span><br/> | <span data-ttu-id="11b89-122">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11b89-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11b89-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11b89-123">Minimum supported server</span></span><br/> | <span data-ttu-id="11b89-124">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11b89-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="11b89-125">Header</span><span class="sxs-lookup"><span data-stu-id="11b89-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="11b89-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="11b89-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="11b89-127">IDL</span><span class="sxs-lookup"><span data-stu-id="11b89-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11b89-128"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11b89-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="11b89-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11b89-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="11b89-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11b89-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="11b89-131">DLL</span><span class="sxs-lookup"><span data-stu-id="11b89-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11b89-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11b89-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="11b89-133">IID</span><span class="sxs-lookup"><span data-stu-id="11b89-133">IID</span></span><br/>                      | <span data-ttu-id="11b89-134">IID_IBackgroundCopyCallback ist als 97ea99c7-0186-4ad4-8df9-c5b4e0ed6b22 definiert.</span><span class="sxs-lookup"><span data-stu-id="11b89-134">IID_IBackgroundCopyCallback is defined as 97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="11b89-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11b89-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11b89-136">**Ibackgroundcopycallback**</span><span class="sxs-lookup"><span data-stu-id="11b89-136">**IBackgroundCopyCallback**</span></span>](ibackgroundcopycallback.md)
</dt> <dt>

[<span data-ttu-id="11b89-137">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="11b89-137">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





