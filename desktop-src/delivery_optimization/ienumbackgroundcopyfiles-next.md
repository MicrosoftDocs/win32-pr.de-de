---
title: Ienumbackgroundcopyfiles Next-Methode (deliveryoptimization. h)
description: Ruft eine angegebene Anzahl von Elementen in der Enumerationsfolge ab. Wenn weniger als die angeforderte Anzahl von Elementen in der Sequenz vorhanden sind, werden die restlichen Elemente abgerufen.
ms.assetid: 31E603EC-2684-487D-AB37-4C6A6F661298
keywords:
- Nächste Methode
- Next-Methode, ienumbackgroundcopyfiles-Schnittstelle
- Ienumbackgroundcopyfiles-Schnittstelle, Next-Methode
topic_type:
- apiref
api_name:
- IEnumBackgroundCopyFiles.Next
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 504b9083f4bdb1651496b4ab2d3b937740596243
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956945"
---
# <a name="ienumbackgroundcopyfilesnext-method"></a><span data-ttu-id="13eac-107">Ienumbackgroundcopyfiles:: Next-Methode</span><span class="sxs-lookup"><span data-stu-id="13eac-107">IEnumBackgroundCopyFiles::Next method</span></span>

<span data-ttu-id="13eac-108">Ruft eine angegebene Anzahl von Elementen in der Enumerationsfolge ab.</span><span class="sxs-lookup"><span data-stu-id="13eac-108">Retrieves a specified number of items in the enumeration sequence.</span></span> <span data-ttu-id="13eac-109">Wenn weniger als die angeforderte Anzahl von Elementen in der Sequenz vorhanden sind, werden die restlichen Elemente abgerufen.</span><span class="sxs-lookup"><span data-stu-id="13eac-109">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="syntax"></a><span data-ttu-id="13eac-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="13eac-110">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG               celt,
  [out] IBackgroundCopyFile **rgelt,
  [out] ULONG               *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="13eac-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="13eac-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13eac-112">*celt* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13eac-112">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13eac-113">Anzahl der angeforderten Elemente.</span><span class="sxs-lookup"><span data-stu-id="13eac-113">Number of elements requested.</span></span>

</dd> <dt>

<span data-ttu-id="13eac-114">*rgelt* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13eac-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13eac-115">Array von [**ibackgroundcopyfile**](ibackgroundcopyfile.md) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="13eac-115">Array of [**IBackgroundCopyFile**](ibackgroundcopyfile.md) objects.</span></span> <span data-ttu-id="13eac-116">Sie müssen jedes Objekt in *rgelt* freigeben, wenn Sie dies erledigt haben.</span><span class="sxs-lookup"><span data-stu-id="13eac-116">You must release each object in *rgelt* when done.</span></span>

</dd> <dt>

<span data-ttu-id="13eac-117">*pceltfetch* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13eac-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13eac-118">Anzahl der Elemente, die in *rgelt* zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="13eac-118">Number of elements returned in *rgelt*.</span></span> <span data-ttu-id="13eac-119">Sie können *pceltfetch* auf **null** festlegen, wenn es sich um ein *celt* handelt.</span><span class="sxs-lookup"><span data-stu-id="13eac-119">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="13eac-120">Initialisieren Sie andernfalls den Wert von *pceltfetch* auf 0, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="13eac-120">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13eac-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13eac-121">Return value</span></span>

<span data-ttu-id="13eac-122">Diese Methode gibt sowohl die folgenden **HRESULT** -Werte als auch andere zurück.</span><span class="sxs-lookup"><span data-stu-id="13eac-122">This method returns the following **HRESULT** values, as well as others.</span></span>



| <span data-ttu-id="13eac-123">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="13eac-123">Return code</span></span>                                                                              | <span data-ttu-id="13eac-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="13eac-124">Description</span></span>                                                        |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="13eac-125"><dt>S_OK \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="13eac-125"><dt>\*\*\*\*S_OK\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="13eac-126">Die Anzahl der angeforderten Elemente wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13eac-126">Successfully returned the number of requested elements.</span></span><br/> |
| <dl> <span data-ttu-id="13eac-127"><dt>**S_FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="13eac-127"><dt>**S_FALSE**</dt></span></span> </dl>  | <span data-ttu-id="13eac-128">Wird kleiner als die Anzahl der angeforderten Elemente zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13eac-128">Returned less than the number of requested elements.</span></span><br/>    |



 

## <a name="requirements"></a><span data-ttu-id="13eac-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13eac-129">Requirements</span></span>



| <span data-ttu-id="13eac-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13eac-130">Requirement</span></span> | <span data-ttu-id="13eac-131">Wert</span><span class="sxs-lookup"><span data-stu-id="13eac-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13eac-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13eac-132">Minimum supported client</span></span><br/> | <span data-ttu-id="13eac-133">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13eac-133">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="13eac-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13eac-134">Minimum supported server</span></span><br/> | <span data-ttu-id="13eac-135">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="13eac-135">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="13eac-136">Header</span><span class="sxs-lookup"><span data-stu-id="13eac-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="13eac-137"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="13eac-137"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="13eac-138">IDL</span><span class="sxs-lookup"><span data-stu-id="13eac-138">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13eac-139"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="13eac-139"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="13eac-140">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13eac-140">Library</span></span><br/>                  | <dl> <span data-ttu-id="13eac-141"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="13eac-141"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="13eac-142">DLL</span><span class="sxs-lookup"><span data-stu-id="13eac-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13eac-143"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13eac-143"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="13eac-144">IID</span><span class="sxs-lookup"><span data-stu-id="13eac-144">IID</span></span><br/>                      | <span data-ttu-id="13eac-145">IID_IEnumBackgroundCopyFiles ist als CA51E165-C365-424C-8D41-24AAA4FF3C40 definiert.</span><span class="sxs-lookup"><span data-stu-id="13eac-145">IID_IEnumBackgroundCopyFiles is defined as CA51E165-C365-424C-8D41-24AAA4FF3C40</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="13eac-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13eac-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13eac-147">**Ienumbackgroundcopyfiles**</span><span class="sxs-lookup"><span data-stu-id="13eac-147">**IEnumBackgroundCopyFiles**</span></span>](ienumbackgroundcopyfiles-.md)
</dt> </dl>

 

 





