---
title: IBackgroundCopyFile5 GetProperty-Methode (deliveryoptimization. h)
description: Ruft eine generische Eigenschaft einer Dateiübertragung für die Übermittlungs Optimierung (Do) ab.
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- GetProperty-Methode
- GetProperty-Methode, IBackgroundCopyFile5-Schnittstelle
- IBackgroundCopyFile5-Schnittstelle, GetProperty-Methode
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103507"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a><span data-ttu-id="879e4-106">IBackgroundCopyFile5:: GetProperty-Methode</span><span class="sxs-lookup"><span data-stu-id="879e4-106">IBackgroundCopyFile5::GetProperty method</span></span>

<span data-ttu-id="879e4-107">Ruft eine generische Eigenschaft einer Dateiübertragung für die Übermittlungs Optimierung (Do) ab.</span><span class="sxs-lookup"><span data-stu-id="879e4-107">Gets a generic property of a Delivery Optimization (DO) file transfer.</span></span>

## <a name="syntax"></a><span data-ttu-id="879e4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="879e4-108">Syntax</span></span>


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a><span data-ttu-id="879e4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="879e4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="879e4-110">*PropertyId* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="879e4-110">*PropertyId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="879e4-111">Gibt die Datei Eigenschaft an, deren Wert abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="879e4-111">Specifies the file property whose value is to be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="879e4-112">*PropertyValue* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="879e4-112">*PropertyValue* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="879e4-113">Der Eigenschafts Wert, der als Zeiger auf einen BITS_FILE_PROPERTY_VALUE Union zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="879e4-113">The property value, returned as a pointer to a BITS_FILE_PROPERTY_VALUE union.</span></span> <span data-ttu-id="879e4-114">Verwenden Sie das Union-Feld, das für den Wert der Eigenschaft ID geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="879e4-114">Use the union field appropriate for the property ID value passed in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="879e4-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="879e4-115">Return value</span></span>

<span data-ttu-id="879e4-116">Wenn diese Methode erfolgreich ausgeführt wird, wird **S_OK** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="879e4-116">If this method succeeds, it returns **S_OK**.</span></span> <span data-ttu-id="879e4-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="879e4-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="879e4-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="879e4-118">Requirements</span></span>



| <span data-ttu-id="879e4-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="879e4-119">Requirement</span></span> | <span data-ttu-id="879e4-120">Wert</span><span class="sxs-lookup"><span data-stu-id="879e4-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="879e4-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="879e4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="879e4-122">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="879e4-122">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="879e4-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="879e4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="879e4-124">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="879e4-124">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="879e4-125">Header</span><span class="sxs-lookup"><span data-stu-id="879e4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="879e4-126"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="879e4-126"><dt>Deliveryoptimization.h</dt></span></span> </dl>   |
| <span data-ttu-id="879e4-127">IDL</span><span class="sxs-lookup"><span data-stu-id="879e4-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="879e4-128"><dt>Deliveryoptimization. idl</dt></span><span class="sxs-lookup"><span data-stu-id="879e4-128"><dt>DeliveryOptimization.idl</dt></span></span> </dl> |
| <span data-ttu-id="879e4-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="879e4-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="879e4-130"><dt>Dosvc. lib</dt></span><span class="sxs-lookup"><span data-stu-id="879e4-130"><dt>Dosvc.lib</dt></span></span> </dl>                |
| <span data-ttu-id="879e4-131">DLL</span><span class="sxs-lookup"><span data-stu-id="879e4-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="879e4-132"><dt>Dosvc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="879e4-132"><dt>Dosvc.dll</dt></span></span> </dl>                |
| <span data-ttu-id="879e4-133">IID</span><span class="sxs-lookup"><span data-stu-id="879e4-133">IID</span></span><br/>                      | <span data-ttu-id="879e4-134">IID_IBackgroundCopyFile5 ist als "85c1657f-DAFC-40e8-8834-df18ea25717e" definiert.</span><span class="sxs-lookup"><span data-stu-id="879e4-134">IID_IBackgroundCopyFile5 is defined as 85C1657F-DAFC-40E8-8834-DF18EA25717E</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="879e4-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="879e4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="879e4-136">**IBackgroundCopyFile5**</span><span class="sxs-lookup"><span data-stu-id="879e4-136">**IBackgroundCopyFile5**</span></span>](ibackgroundcopyfile5.md)
</dt> <dt>

[<span data-ttu-id="879e4-137">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="879e4-137">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





