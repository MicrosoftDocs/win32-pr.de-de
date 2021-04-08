---
title: Ibackgroundcopyjob GetDisplayName-Methode (deliveryoptimization. h)
description: Ruft den anzeigen Amen für den Auftrag ab. In der Regel verwenden Sie den anzeigen Amen, um den Auftrag auf einer Benutzeroberfläche zu identifizieren.
ms.assetid: E3D906E1-5D58-4BA8-A3AB-24BCDCD487F5
keywords:
- GetDisplayName-Methode
- GetDisplayName-Methode, ibackgroundcopyjob-Schnittstelle
- Ibackgroundcopyjob-Schnittstelle, GetDisplayName-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetDisplayName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 981e4b60ea3c25d48a3b098237232e517e4ed1c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956948"
---
# <a name="ibackgroundcopyjobgetdisplayname-method"></a><span data-ttu-id="6ebec-107">Ibackgroundcopyjob:: GetDisplayName-Methode</span><span class="sxs-lookup"><span data-stu-id="6ebec-107">IBackgroundCopyJob::GetDisplayName method</span></span>

<span data-ttu-id="6ebec-108">Ruft den anzeigen Amen für den Auftrag ab.</span><span class="sxs-lookup"><span data-stu-id="6ebec-108">Retrieves the display name for the job.</span></span> <span data-ttu-id="6ebec-109">In der Regel verwenden Sie den anzeigen Amen, um den Auftrag auf einer Benutzeroberfläche zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="6ebec-109">Typically, you use the display name to identify the job in a user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ebec-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ebec-110">Syntax</span></span>


```C++
HRESULT GetDisplayName(
  [out] LPWSTR *ppDisplayName
);
```



## <a name="parameters"></a><span data-ttu-id="6ebec-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ebec-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ebec-112">*ppdisplayname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6ebec-112">*ppDisplayName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ebec-113">Eine auf NULL endenden Zeichenfolge, die den anzeigen Amen enthält, der den Auftrag identifiziert.</span><span class="sxs-lookup"><span data-stu-id="6ebec-113">Null-terminated string that contains the display name that identifies the job.</span></span> <span data-ttu-id="6ebec-114">Mehrere Aufträge können denselben anzeigen Amen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6ebec-114">More than one job can have the same display name.</span></span> <span data-ttu-id="6ebec-115">Aufrufen der Funktion " [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um " *ppdisplayname* " zu beenden</span><span class="sxs-lookup"><span data-stu-id="6ebec-115">Call the [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) function to free *ppDisplayName* when done.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ebec-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ebec-116">Return value</span></span>

<span data-ttu-id="6ebec-117">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="6ebec-117">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="6ebec-118">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="6ebec-118">Return code</span></span>                                                                                  | <span data-ttu-id="6ebec-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ebec-119">Description</span></span>                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| <dl> <span data-ttu-id="6ebec-120"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="6ebec-120"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl>     | <span data-ttu-id="6ebec-121">Der Anzeige Name wurde erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6ebec-121">Display name was successfully retrieved.</span></span><br/>          |
| <dl> <span data-ttu-id="6ebec-122"><dt>**E_INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="6ebec-122"><dt>**E_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="6ebec-123">Der *ppdisplayname* -Parameter darf nicht **null** sein.</span><span class="sxs-lookup"><span data-stu-id="6ebec-123">The *ppDisplayName* parameter cannot be **NULL**.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6ebec-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ebec-124">Requirements</span></span>



| <span data-ttu-id="6ebec-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ebec-125">Requirement</span></span> | <span data-ttu-id="6ebec-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6ebec-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ebec-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ebec-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6ebec-128">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ebec-128">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6ebec-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ebec-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6ebec-130">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ebec-130">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="6ebec-131">Header</span><span class="sxs-lookup"><span data-stu-id="6ebec-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ebec-132"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ebec-132"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="6ebec-133">IDL</span><span class="sxs-lookup"><span data-stu-id="6ebec-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6ebec-134"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6ebec-134"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="6ebec-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6ebec-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="6ebec-136"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6ebec-136"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="6ebec-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6ebec-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ebec-138"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ebec-138"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="6ebec-139">IID</span><span class="sxs-lookup"><span data-stu-id="6ebec-139">IID</span></span><br/>                      | <span data-ttu-id="6ebec-140">IID_IBackgroundCopyJob ist als 37668d37-507E-4160-9316-26306d150b12 definiert.</span><span class="sxs-lookup"><span data-stu-id="6ebec-140">IID_IBackgroundCopyJob is defined as 37668D37-507E-4160-9316-26306D150B12</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="6ebec-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ebec-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ebec-142">**IBackgroundCopyJob**</span><span class="sxs-lookup"><span data-stu-id="6ebec-142">**IBackgroundCopyJob**</span></span>](ibackgroundcopyjob-.md)
</dt> </dl>

 

