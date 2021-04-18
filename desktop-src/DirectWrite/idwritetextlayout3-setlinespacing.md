---
title: IDWriteTextLayout3 setlinespacingmethode
description: Zeilenabstand festlegen. | IDWriteTextLayout3 setlinespacingmethode
ms.assetid: 1bfca257-189c-4d18-628c-aff8217d2775
keywords:
- Setlinespacingmethode direkt schreiben
- Setlinespacingmethod Direct Write, IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3 Interface Direct Write, setlinespacingmethode
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 794df5b0dc993688c8bab15c927ae2c03bc18d69
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106371848"
---
# <a name="idwritetextlayout3setlinespacing-method"></a><span data-ttu-id="10d45-107">IDWriteTextLayout3:: setlinespacingmethode</span><span class="sxs-lookup"><span data-stu-id="10d45-107">IDWriteTextLayout3::SetLineSpacing method</span></span>

<span data-ttu-id="10d45-108">Zeilenabstand festlegen.</span><span class="sxs-lookup"><span data-stu-id="10d45-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="10d45-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="10d45-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="10d45-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="10d45-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10d45-111">*linespacingoptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="10d45-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10d45-112">So verwalten Sie den Leerraum zwischen Zeilen</span><span class="sxs-lookup"><span data-stu-id="10d45-112">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10d45-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="10d45-113">Return value</span></span>

<span data-ttu-id="10d45-114">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="10d45-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="10d45-115">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="10d45-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="10d45-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="10d45-116">Requirements</span></span>



| <span data-ttu-id="10d45-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="10d45-117">Requirement</span></span> | <span data-ttu-id="10d45-118">Wert</span><span class="sxs-lookup"><span data-stu-id="10d45-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10d45-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="10d45-119">Minimum supported client</span></span><br/> | <span data-ttu-id="10d45-120">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="10d45-120">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="10d45-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="10d45-121">Minimum supported server</span></span><br/> | <span data-ttu-id="10d45-122">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="10d45-122">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="10d45-123">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="10d45-123">Minimum supported phone</span></span><br/>  | <span data-ttu-id="10d45-124">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="10d45-124">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="10d45-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="10d45-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="10d45-126"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="10d45-126"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="10d45-127">DLL</span><span class="sxs-lookup"><span data-stu-id="10d45-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10d45-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10d45-128"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="10d45-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10d45-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10d45-130">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="10d45-130">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





