---
title: Ibackgroundcopyfile GetProgress-Methode (deliveryoptimization. h)
description: Ruft Informationen zum Fortschritt der Dateiübertragung ab.
ms.assetid: 3D8AFD65-AF34-4000-A4A9-8A187427E85C
keywords:
- GetProgress-Methode
- GetProgress-Methode, ibackgroundcopyfile-Schnittstelle
- Ibackgroundcopyfile-Schnittstelle, GetProgress-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f0828105822700f9d34cd180c8877634bc3a6013
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476374"
---
# <a name="ibackgroundcopyfilegetprogress-method"></a><span data-ttu-id="eff47-106">Ibackgroundcopyfile:: GetProgress-Methode</span><span class="sxs-lookup"><span data-stu-id="eff47-106">IBackgroundCopyFile::GetProgress method</span></span>

<span data-ttu-id="eff47-107">Ruft Informationen zum Fortschritt der Dateiübertragung ab.</span><span class="sxs-lookup"><span data-stu-id="eff47-107">Retrieves information on the progress of the file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="eff47-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="eff47-108">Syntax</span></span>


```C++
HRESULT GetProgress(
  [out] BG_FILE_PROGRESS *pProgress
);
```



## <a name="parameters"></a><span data-ttu-id="eff47-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="eff47-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eff47-110">*pprogress* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="eff47-110">*pProgress* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eff47-111">-Struktur, deren Elemente den Fortschritt der Dateiübertragung angeben.</span><span class="sxs-lookup"><span data-stu-id="eff47-111">Structure whose members indicate the progress of the file transfer.</span></span> <span data-ttu-id="eff47-112">Ausführliche Informationen zu den verfügbaren Fortschrittsinformationen finden Sie in der [**BG_FILE_PROGRESS**](bg-file-progress.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="eff47-112">For details on the type of progress information available, see the [**BG_FILE_PROGRESS**](bg-file-progress.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eff47-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="eff47-113">Return value</span></span>

<span data-ttu-id="eff47-114">Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="eff47-114">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="eff47-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="eff47-115">Requirements</span></span>



| <span data-ttu-id="eff47-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="eff47-116">Requirement</span></span> | <span data-ttu-id="eff47-117">Wert</span><span class="sxs-lookup"><span data-stu-id="eff47-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eff47-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="eff47-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eff47-119">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eff47-119">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="eff47-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="eff47-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eff47-121">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="eff47-121">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="eff47-122">Header</span><span class="sxs-lookup"><span data-stu-id="eff47-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="eff47-123"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="eff47-123"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="eff47-124">IDL</span><span class="sxs-lookup"><span data-stu-id="eff47-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="eff47-125"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="eff47-125"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="eff47-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="eff47-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="eff47-127"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eff47-127"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="eff47-128">DLL</span><span class="sxs-lookup"><span data-stu-id="eff47-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="eff47-129"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="eff47-129"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="eff47-130">IID</span><span class="sxs-lookup"><span data-stu-id="eff47-130">IID</span></span><br/>                      | <span data-ttu-id="eff47-131">IID_IBackgroundCopyFile ist als 01b7bd23-B88-4a77-8490-5891d3e4653a definiert.</span><span class="sxs-lookup"><span data-stu-id="eff47-131">IID_IBackgroundCopyFile is defined as 01B7BD23-FB88-4A77-8490-5891D3E4653A</span></span><br/>              |



## <a name="see-also"></a><span data-ttu-id="eff47-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eff47-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eff47-133">**BG_FILE_PROGRESS**</span><span class="sxs-lookup"><span data-stu-id="eff47-133">**BG_FILE_PROGRESS**</span></span>](bg-file-progress.md)
</dt> <dt>

[<span data-ttu-id="eff47-134">**Ibackgroundcopyfile**</span><span class="sxs-lookup"><span data-stu-id="eff47-134">**IBackgroundCopyFile**</span></span>](ibackgroundcopyfile.md)
</dt> <dt>

[<span data-ttu-id="eff47-135">**Ibackgroundcopyjob:: GetProgress**</span><span class="sxs-lookup"><span data-stu-id="eff47-135">**IBackgroundCopyJob::GetProgress**</span></span>](ibackgroundcopyjob-getprogress.md)
</dt> </dl>

 

 





