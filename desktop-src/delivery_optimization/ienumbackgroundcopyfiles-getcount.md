---
title: Ienumbackgroundcopyfiles GetCount-Methode (deliveryoptimization. h)
description: Ruft die Anzahl der Dateien in der-Enumeration ab.
ms.assetid: EE27679D-3AC0-49DA-992F-8DEA10C21646
keywords:
- GetCount-Methode
- GetCount-Methode, ienumbackgroundcopyfiles-Schnittstelle
- Ienumbackgroundcopyfiles-Schnittstelle, GetCount-Methode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.GetCount
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 05e2672f0cda3c572024a0865b2fb534dddb6598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741472"
---
# <a name="ienumbackgroundcopyfilesgetcount-method"></a><span data-ttu-id="0d70e-106">Ienumbackgroundcopyfiles:: GetCount-Methode</span><span class="sxs-lookup"><span data-stu-id="0d70e-106">IEnumBackgroundCopyFiles::GetCount method</span></span>

<span data-ttu-id="0d70e-107">Ruft die Anzahl der Dateien in der-Enumeration ab.</span><span class="sxs-lookup"><span data-stu-id="0d70e-107">Retrieves a count of the number of files in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d70e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d70e-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pCount
);
```



## <a name="parameters"></a><span data-ttu-id="0d70e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d70e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d70e-110">*pcount* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0d70e-110">*pCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d70e-111">Anzahl der Dateien in der-Enumeration.</span><span class="sxs-lookup"><span data-stu-id="0d70e-111">Number of files in the enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d70e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d70e-112">Return value</span></span>

<span data-ttu-id="0d70e-113">Diese Methode gibt **S_OK** bei Erfolg oder einen der standardmäßigen com **HRESULT** -Werte bei einem Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="0d70e-113">This method returns **S_OK** on success or one of the standard COM **HRESULT** values on error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d70e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d70e-114">Requirements</span></span>



| <span data-ttu-id="0d70e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d70e-115">Requirement</span></span> | <span data-ttu-id="0d70e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0d70e-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d70e-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0d70e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0d70e-118">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d70e-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0d70e-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0d70e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0d70e-120">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0d70e-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="0d70e-121">Header</span><span class="sxs-lookup"><span data-stu-id="0d70e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d70e-122"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d70e-122"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="0d70e-123">IDL</span><span class="sxs-lookup"><span data-stu-id="0d70e-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0d70e-124"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0d70e-124"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="0d70e-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0d70e-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="0d70e-126"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d70e-126"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="0d70e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="0d70e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0d70e-128"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0d70e-128"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="0d70e-129">IID</span><span class="sxs-lookup"><span data-stu-id="0d70e-129">IID</span></span><br/>                      | <span data-ttu-id="0d70e-130">IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.</span><span class="sxs-lookup"><span data-stu-id="0d70e-130">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="0d70e-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d70e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d70e-132">**Ienumbackgroundcopyfiles**</span><span class="sxs-lookup"><span data-stu-id="0d70e-132">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





