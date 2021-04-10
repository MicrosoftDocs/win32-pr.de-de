---
title: IDWriteTextLayout3 getlinespacingmethode
description: Ruft Informationen zum Zeilenabstand ab.
ms.assetid: 6b93a3ec-c8ea-2e64-45b5-51565d6de173
keywords:
- Getlinespacung-Methode direkt schreiben
- Getlinespaceing-Methode Direct Write, IDWriteTextLayout3-Schnittstelle
- IDWriteTextLayout3 Interface Direct Write, getlinespacingmethode
topic_type:
- apiref
api_name:
- IDWriteTextLayout3.GetLineSpacing
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303030a5674f39c160804ae2dad5b91050d82f37
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956702"
---
# <a name="idwritetextlayout3getlinespacing-method"></a><span data-ttu-id="d7ade-106">IDWriteTextLayout3:: GetLineSpacing-Methode</span><span class="sxs-lookup"><span data-stu-id="d7ade-106">IDWriteTextLayout3::GetLineSpacing method</span></span>

<span data-ttu-id="d7ade-107">Ruft Informationen zum Zeilenabstand ab.</span><span class="sxs-lookup"><span data-stu-id="d7ade-107">Gets line spacing information.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7ade-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7ade-108">Syntax</span></span>


```C++
HRESULT GetLineSpacing(
  [out] DWRITE_LINE_SPACING *lineSpacingOptions
);
```



## <a name="parameters"></a><span data-ttu-id="d7ade-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7ade-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7ade-110">*linespacingoptions* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d7ade-110">*lineSpacingOptions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7ade-111">So verwalten Sie den Leerraum zwischen Zeilen</span><span class="sxs-lookup"><span data-stu-id="d7ade-111">How to manage space between lines.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7ade-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7ade-112">Return value</span></span>

<span data-ttu-id="d7ade-113">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d7ade-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7ade-114">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7ade-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7ade-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7ade-115">Requirements</span></span>



| <span data-ttu-id="d7ade-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7ade-116">Requirement</span></span> | <span data-ttu-id="d7ade-117">Wert</span><span class="sxs-lookup"><span data-stu-id="d7ade-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7ade-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7ade-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d7ade-119">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="d7ade-119">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d7ade-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7ade-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d7ade-121">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7ade-121">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d7ade-122">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="d7ade-122">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d7ade-123">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="d7ade-123">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="d7ade-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7ade-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7ade-125"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7ade-125"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d7ade-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d7ade-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7ade-127"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7ade-127"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7ade-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7ade-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7ade-129">**IDWriteTextLayout3**</span><span class="sxs-lookup"><span data-stu-id="d7ade-129">**IDWriteTextLayout3**</span></span>](idwritetextlayout3.md)
</dt> </dl>

 

 





