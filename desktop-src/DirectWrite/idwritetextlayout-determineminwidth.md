---
title: Idschreitetextlayout determineminwidth-Methode
description: Bestimmt die minimal mögliche Breite, auf die das Layout festgelegt werden kann, ohne dass ein notfallumbruch zwischen den Zeichen der ganzen Wörter auftritt.
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- Determineminwidth-Methode direkt schreiben
- Determineminwidth-Methode direkt schreiben, idschreitetextlayout-Schnittstelle
- Idwrite tetextlayout Interface Direct Write, determineminwidth-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2525f770030b80f0e9c0d6df9e5ec88becbb394b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371218"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a><span data-ttu-id="7c3be-106">Idschreitetextlayout::D etermineminwidth-Methode</span><span class="sxs-lookup"><span data-stu-id="7c3be-106">IDWriteTextLayout::DetermineMinWidth method</span></span>

<span data-ttu-id="7c3be-107">Bestimmt die minimal mögliche Breite, auf die das Layout festgelegt werden kann, ohne dass ein notfallumbruch zwischen den Zeichen der ganzen Wörter auftritt.</span><span class="sxs-lookup"><span data-stu-id="7c3be-107">Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3be-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c3be-108">Syntax</span></span>


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="7c3be-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c3be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c3be-110">*MinWidth* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7c3be-110">*minWidth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c3be-111">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="7c3be-111">Type: **FLOAT\***</span></span>

<span data-ttu-id="7c3be-112">Minimale Breite.</span><span class="sxs-lookup"><span data-stu-id="7c3be-112">Minimum width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c3be-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7c3be-113">Return value</span></span>

<span data-ttu-id="7c3be-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7c3be-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7c3be-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="7c3be-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7c3be-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c3be-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7c3be-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7c3be-117">Requirements</span></span>



| <span data-ttu-id="7c3be-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7c3be-118">Requirement</span></span> | <span data-ttu-id="7c3be-119">Wert</span><span class="sxs-lookup"><span data-stu-id="7c3be-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c3be-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7c3be-120">Library</span></span><br/> | <dl> <span data-ttu-id="7c3be-121"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c3be-121"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="7c3be-122">DLL</span><span class="sxs-lookup"><span data-stu-id="7c3be-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="7c3be-123"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c3be-123"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c3be-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c3be-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c3be-125">**Idschreitetextlayout**</span><span class="sxs-lookup"><span data-stu-id="7c3be-125">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="7c3be-126">**Idschreitetextlayout**</span><span class="sxs-lookup"><span data-stu-id="7c3be-126">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

