---
title: Ibackgroundcopyjob-EnumFiles-Methode (deliveryoptimization. h)
description: Ruft einen ienumbackgroundcopyfiles-Schnittstellen Zeiger ab, mit dem Sie die Dateien in einem Auftrag aufzählen.
ms.assetid: 94FA5D7B-08C1-497E-9813-571D35AE3BCF
keywords:
- EnumFiles-Methode
- EnumFiles-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, EnumFiles-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.EnumFiles
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a4b0315f98594357d67fd5dbfed3bf2561f41f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104073"
---
# <a name="ibackgroundcopyjobenumfiles-method"></a><span data-ttu-id="2a9a1-106">Ibackgroundcopyjob:: EnumFiles-Methode</span><span class="sxs-lookup"><span data-stu-id="2a9a1-106">IBackgroundCopyJob::EnumFiles method</span></span>

<span data-ttu-id="2a9a1-107">Ruft einen [**ienumbackgroundcopyfiles**](ienumbackgroundcopyfiles-.md) -Schnittstellen Zeiger ab, mit dem Sie die Dateien in einem Auftrag aufzählen.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-107">Retrieves an [**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in a job.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a9a1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a9a1-108">Syntax</span></span>


```C++
HRESULT EnumFiles(
  [out] IEnumBackgroundCopyFiles **ppEnumFiles
);
```



## <a name="parameters"></a><span data-ttu-id="2a9a1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a9a1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a9a1-110">" *ppumschlag files* \[ " vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2a9a1-110">*ppEnumFiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a9a1-111">[**Ienumbackgroundcopyfiles**](ienumbackgroundcopyfiles-.md) -Schnittstellen Zeiger, mit dem die Dateien im Auftrag aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-111">[**IEnumBackgroundCopyFiles**](ienumbackgroundcopyfiles-.md) interface pointer that you use to enumerate the files in the job.</span></span> <span data-ttu-id="2a9a1-112">Geben Sie nach Abschluss " *ppumschlag files* " frei.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-112">Release *ppEnumFiles* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a9a1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a9a1-113">Return value</span></span>

<span data-ttu-id="2a9a1-114">Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a9a1-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a9a1-115">Requirements</span></span>



| <span data-ttu-id="2a9a1-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a9a1-116">Requirement</span></span> | <span data-ttu-id="2a9a1-117">Wert</span><span class="sxs-lookup"><span data-stu-id="2a9a1-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a9a1-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a9a1-118">Minimum supported client</span></span><br/> | <span data-ttu-id="2a9a1-119">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a9a1-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2a9a1-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a9a1-120">Minimum supported server</span></span><br/> | <span data-ttu-id="2a9a1-121">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a9a1-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="2a9a1-122">Header</span><span class="sxs-lookup"><span data-stu-id="2a9a1-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a9a1-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="2a9a1-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="2a9a1-124">IDL</span><span class="sxs-lookup"><span data-stu-id="2a9a1-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2a9a1-125"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="2a9a1-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="2a9a1-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2a9a1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="2a9a1-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a9a1-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="2a9a1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="2a9a1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a9a1-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a9a1-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="2a9a1-130">IID</span><span class="sxs-lookup"><span data-stu-id="2a9a1-130">IID</span></span><br/>                      | <span data-ttu-id="2a9a1-131">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="2a9a1-131">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="2a9a1-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a9a1-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a9a1-133">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="2a9a1-133">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> <dt>

[<span data-ttu-id="2a9a1-134">**Ienumbackgroundcopyfiles**</span><span class="sxs-lookup"><span data-stu-id="2a9a1-134">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





