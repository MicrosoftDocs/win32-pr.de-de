---
title: IDWriteTextFormat2 setlinespacingmethode
description: Zeilenabstand festlegen. | IDWriteTextFormat2 setlinespacingmethode
ms.assetid: 71d8c6c4-920f-a1b5-5a13-9985a7aca41e
keywords:
- Setlinespacingmethode direkt schreiben
- Setlinespacingmethod Direct Write, IDWriteTextFormat2-Schnittstelle
- IDWriteTextFormat2 Interface Direct Write, setlinespacingmethode
topic_type:
- apiref
api_name:
- IDWriteTextFormat2.SetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d3514c52c9b8a51666d36eec7ce893735635f3e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104219366"
---
# <a name="idwritetextformat2setlinespacing-method"></a><span data-ttu-id="764a8-107">IDWriteTextFormat2:: setlinespacingmethode</span><span class="sxs-lookup"><span data-stu-id="764a8-107">IDWriteTextFormat2::SetLineSpacing method</span></span>

<span data-ttu-id="764a8-108">Zeilenabstand festlegen.</span><span class="sxs-lookup"><span data-stu-id="764a8-108">Set line spacing.</span></span>

## <a name="syntax"></a><span data-ttu-id="764a8-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="764a8-109">Syntax</span></span>


```C++
HRESULT SetLineSpacing(
  [in] const DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="764a8-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="764a8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="764a8-111">*linespacingoptions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="764a8-111">*lineSpacingOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="764a8-112">Typ: konstanter **[**dwrite- \_ Zeilen \_ Abstand**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing) \***</span><span class="sxs-lookup"><span data-stu-id="764a8-112">Type: **const [**DWRITE\_LINE\_SPACING**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)\***</span></span>

<span data-ttu-id="764a8-113">So verwalten Sie den Leerraum zwischen Zeilen</span><span class="sxs-lookup"><span data-stu-id="764a8-113">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="764a8-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="764a8-114">Return value</span></span>

<span data-ttu-id="764a8-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="764a8-115">Type: **HRESULT**</span></span>

<span data-ttu-id="764a8-116">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="764a8-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="764a8-117">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="764a8-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="764a8-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="764a8-118">Requirements</span></span>



| <span data-ttu-id="764a8-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="764a8-119">Requirement</span></span> | <span data-ttu-id="764a8-120">Wert</span><span class="sxs-lookup"><span data-stu-id="764a8-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="764a8-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="764a8-121">Minimum supported client</span></span><br/> | <span data-ttu-id="764a8-122">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="764a8-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="764a8-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="764a8-123">Minimum supported server</span></span><br/> | <span data-ttu-id="764a8-124">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="764a8-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="764a8-125">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="764a8-125">Minimum supported phone</span></span><br/>  | <span data-ttu-id="764a8-126">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="764a8-126">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="764a8-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="764a8-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="764a8-128"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="764a8-128"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="764a8-129">DLL</span><span class="sxs-lookup"><span data-stu-id="764a8-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="764a8-130"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="764a8-130"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="764a8-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="764a8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="764a8-132">**IDWriteTextFormat2**</span><span class="sxs-lookup"><span data-stu-id="764a8-132">**IDWriteTextFormat2**</span></span>](idwritetextformat2.md)
</dt> </dl>

 

 





