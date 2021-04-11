---
title: IBackgroundCopyFile5 SetProperty-Methode (deliveryoptimization. h)
description: Legt eine generische Eigenschaft einer Übermittlungs Optimierungs Datei-Übertragung (Do) fest.
ms.assetid: 63B6806E-47D6-49B0-9867-628C110540D0
keywords:
- SetProperty-Methode
- SetProperty-Methode, IBackgroundCopyFile5-Schnittstelle
- IBackgroundCopyFile5 Interface, SetProperty-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 7f519ee77af0ae6e0c3d1d036aeeb6a8ad712870
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949785"
---
# <a name="ibackgroundcopyfile5setproperty-method"></a><span data-ttu-id="1fdae-106">IBackgroundCopyFile5:: SetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="1fdae-106">IBackgroundCopyFile5::SetProperty method</span></span>

<span data-ttu-id="1fdae-107">Legt eine generische Eigenschaft einer Übermittlungs Optimierungs Datei-Übertragung (Do) fest.</span><span class="sxs-lookup"><span data-stu-id="1fdae-107">Sets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fdae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fdae-108">Syntax</span></span>


```C++
HRESULT SetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *ProertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="1fdae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fdae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fdae-110">*PropertyId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1fdae-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdae-111">Gibt die festzulegende Eigenschaft an.</span><span class="sxs-lookup"><span data-stu-id="1fdae-111">Specifies the property to be set.</span></span>

</dd> <dt>

<span data-ttu-id="1fdae-112">*Proertyvalue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1fdae-112">*ProertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fdae-113">Ein Zeiger auf eine Union, die den festzulegenden Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="1fdae-113">A pointer to a union that specifies the value to be set.</span></span> <span data-ttu-id="1fdae-114">Das für die eigen schafts-ID geeignete Unionmember wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="1fdae-114">The union member appropriate for the property ID is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fdae-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1fdae-115">Return value</span></span>

<span data-ttu-id="1fdae-116">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fdae-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="1fdae-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="1fdae-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fdae-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1fdae-118">Requirements</span></span>



| <span data-ttu-id="1fdae-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1fdae-119">Requirement</span></span> | <span data-ttu-id="1fdae-120">Wert</span><span class="sxs-lookup"><span data-stu-id="1fdae-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fdae-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1fdae-121">Minimum supported client</span></span><br/> | <span data-ttu-id="1fdae-122">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fdae-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1fdae-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1fdae-123">Minimum supported server</span></span><br/> | <span data-ttu-id="1fdae-124">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1fdae-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="1fdae-125">Header</span><span class="sxs-lookup"><span data-stu-id="1fdae-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fdae-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fdae-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fdae-127">IDL</span><span class="sxs-lookup"><span data-stu-id="1fdae-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1fdae-128"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1fdae-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="1fdae-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1fdae-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="1fdae-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fdae-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="1fdae-131">DLL</span><span class="sxs-lookup"><span data-stu-id="1fdae-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fdae-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fdae-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="1fdae-133">IID</span><span class="sxs-lookup"><span data-stu-id="1fdae-133">IID</span></span><br/>                      | <span data-ttu-id="1fdae-134">IID_IBackgroundCopyFile5 ist als "85c1657f-DAFC-40e8-8834-df18ea25717e" definiert.</span><span class="sxs-lookup"><span data-stu-id="1fdae-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="1fdae-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fdae-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fdae-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="1fdae-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="1fdae-137">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="1fdae-137">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> </dl>

 

 





