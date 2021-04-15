---
title: IBackgroundCopyFile2 getfileranges-Methode (deliveryoptimization. h)
description: Ruft die Bereiche ab, die Sie aus der Remote Datei herunterladen möchten.
ms.assetid: 19B7B4FC-371F-482B-B997-C240B5483F4D
keywords:
- Getfileranges-Methode
- Getfileranges-Methode, IBackgroundCopyFile2-Schnittstelle
- IBackgroundCopyFile2 Interface, getfileranges-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.GetFileRanges
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 37352176ca460587343bed0a154ee992c12c2fff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391839"
---
# <a name="ibackgroundcopyfile2getfileranges-method"></a><span data-ttu-id="d8615-106">IBackgroundCopyFile2:: getfileranges-Methode</span><span class="sxs-lookup"><span data-stu-id="d8615-106">IBackgroundCopyFile2::GetFileRanges method</span></span>

<span data-ttu-id="d8615-107">Ruft die Bereiche ab, die Sie aus der Remote Datei herunterladen möchten.</span><span class="sxs-lookup"><span data-stu-id="d8615-107">Retrieves the ranges that you want to download from the remote file.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8615-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8615-108">Syntax</span></span>


```C++
HRESULT GetFileRanges(
  [in, out] DWORD         *RangeCount,
  [out]     BG_FILE_RANGE **Ranges
);
```



## <a name="parameters"></a><span data-ttu-id="d8615-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8615-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8615-110">*Rangecount* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d8615-110">*RangeCount* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8615-111">Anzahl der Elemente in *Bereichen*.</span><span class="sxs-lookup"><span data-stu-id="d8615-111">Number of elements in *Ranges*.</span></span>

</dd> <dt>

<span data-ttu-id="d8615-112">*Bereiche* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d8615-112">*Ranges* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d8615-113">Array von [**BG_FILE_RANGE**](bg-file-range.md) Strukturen, die die Bereiche angeben, die heruntergeladen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d8615-113">Array of [**BG_FILE_RANGE**](bg-file-range.md) structures that specify the ranges to download.</span></span> <span data-ttu-id="d8615-114">Wenn Sie den Vorgang abgeschlossen haben *, können Sie* die Funktion " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen</span><span class="sxs-lookup"><span data-stu-id="d8615-114">When done, call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *Ranges*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8615-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8615-115">Return value</span></span>

<span data-ttu-id="d8615-116">Diese Methode gibt sowohl die folgenden Rückgabewerte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="d8615-116">This method returns the following return values, as well as others.</span></span>



| <span data-ttu-id="d8615-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d8615-117">Return code</span></span>                                                                              | <span data-ttu-id="d8615-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d8615-118">Description</span></span>                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d8615-119"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="d8615-119"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="d8615-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="d8615-120">Success</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="d8615-121"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="d8615-121"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="d8615-122">Es wurden keine Bereiche angegeben, oder es handelt sich um einen Upload-oder Upload-Reply-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="d8615-122">No ranges were specified or the job is an upload or upload-reply job.</span></span> <span data-ttu-id="d8615-123">*Rangecount* ist auf 0 (null) und *Bereiche* auf **null** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d8615-123">*RangeCount* is set to zero and *Ranges* is set to **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d8615-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d8615-124">Requirements</span></span>



| <span data-ttu-id="d8615-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d8615-125">Requirement</span></span> | <span data-ttu-id="d8615-126">Wert</span><span class="sxs-lookup"><span data-stu-id="d8615-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8615-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d8615-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d8615-128">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8615-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d8615-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d8615-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d8615-130">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d8615-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d8615-131">Header</span><span class="sxs-lookup"><span data-stu-id="d8615-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d8615-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="d8615-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="d8615-133">IDL</span><span class="sxs-lookup"><span data-stu-id="d8615-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d8615-134"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d8615-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="d8615-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d8615-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="d8615-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d8615-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="d8615-137">DLL</span><span class="sxs-lookup"><span data-stu-id="d8615-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8615-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8615-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="d8615-139">IID</span><span class="sxs-lookup"><span data-stu-id="d8615-139">IID</span></span><br/>                      | <span data-ttu-id="d8615-140">IID_IBackgroundCopyFile2 ist als 83e81b93-0873-474d-8a8c-f 2018b1a939c definiert.</span><span class="sxs-lookup"><span data-stu-id="d8615-140">IID_IBackgroundCopyFile2 is defined as 83e81b93-0873-474d-8a8c-f2018b1a939c</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d8615-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8615-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8615-142">**BG_FILE_RANGE**</span><span class="sxs-lookup"><span data-stu-id="d8615-142">**BG_FILE_RANGE**</span></span>](bg-file-range.md)
</dt> <dt>

[<span data-ttu-id="d8615-143">**IBackgroundCopyFile2**</span><span class="sxs-lookup"><span data-stu-id="d8615-143">**IBackgroundCopyFile2**</span></span>](ibackgroundcopyfile2.md)
</dt> </dl>

 

