---
title: Ienumbackgroundcopyfiles Skip-Methode (deliveryoptimization. h)
description: Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz. Wenn in der Sequenz weniger Elemente als die angeforderte Anzahl der zu über springenden Elemente vorhanden sind, wird das letzte Element in der Sequenz übersprungen.
ms.assetid: B01D4292-6BA5-4171-928B-AB2C555E2C2A
keywords:
- Skip-Methode
- Skip-Methode, ienumbackgroundcopyfiles-Schnittstelle
- Ienumbackgroundcopyfiles-Schnittstelle, Skip-Methode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Skip
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5d88a7d971ab93b90c844fc8d9d92d7f154c0ebf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040252"
---
# <a name="ienumbackgroundcopyfilesskip-method"></a><span data-ttu-id="11397-107">Ienumbackgroundcopyfiles:: Skip-Methode</span><span class="sxs-lookup"><span data-stu-id="11397-107">IEnumBackgroundCopyFiles::Skip method</span></span>

<span data-ttu-id="11397-108">Überspringt die nächste angegebene Anzahl von Elementen in der enumerationssequenz.</span><span class="sxs-lookup"><span data-stu-id="11397-108">Skips the next specified number of elements in the enumeration sequence.</span></span> <span data-ttu-id="11397-109">Wenn in der Sequenz weniger Elemente als die angeforderte Anzahl der zu über springenden Elemente vorhanden sind, wird das letzte Element in der Sequenz übersprungen.</span><span class="sxs-lookup"><span data-stu-id="11397-109">If there are fewer elements left in the sequence than the requested number of elements to skip, it skips past the last element in the sequence.</span></span>

## <a name="syntax"></a><span data-ttu-id="11397-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="11397-110">Syntax</span></span>


```C++
HRESULT Skip(
  [in] ULONG celt
);
```



## <a name="parameters"></a><span data-ttu-id="11397-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="11397-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11397-112">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="11397-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11397-113">Anzahl der zu überspringenden Elemente.</span><span class="sxs-lookup"><span data-stu-id="11397-113">Number of elements to skip.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11397-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="11397-114">Return value</span></span>

<span data-ttu-id="11397-115">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="11397-115">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="11397-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="11397-116">Return code</span></span>                                                                              | <span data-ttu-id="11397-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11397-117">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="11397-118"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="11397-118"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="11397-119">Die Anzahl der angeforderten Elemente wurde erfolgreich übersprungen.</span><span class="sxs-lookup"><span data-stu-id="11397-119">Successfully skipped the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="11397-120"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="11397-120"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="11397-121">Wird kleiner als die Anzahl der angeforderten Elemente übersprungen.</span><span class="sxs-lookup"><span data-stu-id="11397-121">Skipped less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="11397-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="11397-122">Requirements</span></span>



| <span data-ttu-id="11397-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="11397-123">Requirement</span></span> | <span data-ttu-id="11397-124">Wert</span><span class="sxs-lookup"><span data-stu-id="11397-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="11397-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="11397-125">Minimum supported client</span></span><br/> | <span data-ttu-id="11397-126">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11397-126">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="11397-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="11397-127">Minimum supported server</span></span><br/> | <span data-ttu-id="11397-128">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="11397-128">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="11397-129">Header</span><span class="sxs-lookup"><span data-stu-id="11397-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="11397-130"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="11397-130"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="11397-131">IDL</span><span class="sxs-lookup"><span data-stu-id="11397-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="11397-132"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="11397-132"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="11397-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="11397-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="11397-134"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11397-134"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="11397-135">DLL</span><span class="sxs-lookup"><span data-stu-id="11397-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="11397-136"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="11397-136"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="11397-137">IID</span><span class="sxs-lookup"><span data-stu-id="11397-137">IID</span></span><br/>                      | <span data-ttu-id="11397-138">IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.</span><span class="sxs-lookup"><span data-stu-id="11397-138">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="11397-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="11397-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11397-140">**Ienumbackgroundcopyfiles**</span><span class="sxs-lookup"><span data-stu-id="11397-140">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





