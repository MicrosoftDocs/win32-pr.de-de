---
title: Idwrite-colorglyphrunenumerator-Methode von "muvenext"
description: Wechselt zum nächsten Symbol, das im Enumerator ausgeführt wird.
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- Methode "direkte Schreibvorgänge" in der Methode "
- Comvenext-Methode Direct Write, idwrite tecolorglyphrunenumerator-Schnittstelle
- Idwrite-colorglyphrunenumerator-Schnittstelle Direct Write, "ivenext"-Methode
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518113"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a><span data-ttu-id="40f50-106">Idwrite-colorglyphrunenumerator:: ivenext-Methode</span><span class="sxs-lookup"><span data-stu-id="40f50-106">IDWriteColorGlyphRunEnumerator::MoveNext method</span></span>

<span data-ttu-id="40f50-107">Wechselt zum nächsten Symbol, das im Enumerator ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40f50-107">Move to the next glyph run in the enumerator.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f50-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="40f50-108">Syntax</span></span>


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a><span data-ttu-id="40f50-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="40f50-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40f50-110">*haverun* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="40f50-110">*haveRun* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="40f50-111">Typ: \**bool \** _</span><span class="sxs-lookup"><span data-stu-id="40f50-111">Type: \**BOOL\** _</span></span>

<span data-ttu-id="40f50-112">Gibt _ *true*\* zurück, wenn ein nächstes Symbol ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="40f50-112">Returns _ *TRUE*\* if there is a next glyph run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40f50-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="40f50-113">Return value</span></span>

<span data-ttu-id="40f50-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="40f50-114">Type: **HRESULT**</span></span>

<span data-ttu-id="40f50-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="40f50-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="40f50-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="40f50-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="40f50-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="40f50-117">Requirements</span></span>



| <span data-ttu-id="40f50-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="40f50-118">Requirement</span></span> | <span data-ttu-id="40f50-119">Wert</span><span class="sxs-lookup"><span data-stu-id="40f50-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="40f50-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="40f50-120">Minimum supported client</span></span><br/> | <span data-ttu-id="40f50-121">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="40f50-121">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="40f50-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="40f50-122">Minimum supported server</span></span><br/> | <span data-ttu-id="40f50-123">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="40f50-123">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="40f50-124">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="40f50-124">Minimum supported phone</span></span><br/>  | <span data-ttu-id="40f50-125">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="40f50-125">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="40f50-126">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="40f50-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="40f50-127"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="40f50-127"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="40f50-128">DLL</span><span class="sxs-lookup"><span data-stu-id="40f50-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="40f50-129"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="40f50-129"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="40f50-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40f50-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f50-131">**Idschreitecolorglyphrunenumerator**</span><span class="sxs-lookup"><span data-stu-id="40f50-131">**IDWriteColorGlyphRunEnumerator**</span></span>](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





