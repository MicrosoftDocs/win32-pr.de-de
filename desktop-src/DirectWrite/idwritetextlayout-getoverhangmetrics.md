---
title: Idschreitetextlayout getverhangmetrics-Methode
description: Gibt die über schreibungen (in Dips) des Layouts und aller darin enthaltenen Objekte zurück, einschließlich Text Glyphen und Inline-Objekten.
ms.assetid: 4b23f6c5-cacc-41e2-8934-6f95208b999a
keywords:
- Getverhangmetrics-Methode direkt schreiben
- Getverhangmetrics-Methode Direct Write, idwrite tetextlayout-Schnittstelle
- Idwrite tetextlayout Interface Direct Write, getverhangmetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteTextLayout.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d8a015998f0a673a310319f93d8f4892dd4b1c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370091"
---
# <a name="idwritetextlayoutgetoverhangmetrics-method"></a><span data-ttu-id="c256e-106">Idwrite tetextlayout:: getverhangmetrics-Methode</span><span class="sxs-lookup"><span data-stu-id="c256e-106">IDWriteTextLayout::GetOverhangMetrics method</span></span>

<span data-ttu-id="c256e-107">Gibt die über schreibungen (in Dips) des Layouts und aller darin enthaltenen Objekte zurück, einschließlich Text Glyphen und Inline-Objekten.</span><span class="sxs-lookup"><span data-stu-id="c256e-107">Returns the overhangs (in DIPs) of the layout and all objects contained in it, including text glyphs and inline objects.</span></span>

## <a name="syntax"></a><span data-ttu-id="c256e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c256e-108">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="c256e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c256e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c256e-110">*überlastet* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c256e-110">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c256e-111">Typ: **[ **dwrite- \_ \_ overhängenmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="c256e-111">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="c256e-112">Über schießungen sichtbarer Blöcke (in Dips) außerhalb des Layouts.</span><span class="sxs-lookup"><span data-stu-id="c256e-112">Overshoots of visible extents (in DIPs) outside the layout.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c256e-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c256e-113">Return value</span></span>

<span data-ttu-id="c256e-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="c256e-114">Type: **HRESULT**</span></span>

<span data-ttu-id="c256e-115">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="c256e-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="c256e-116">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c256e-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="c256e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c256e-117">Remarks</span></span>

<span data-ttu-id="c256e-118">Unterstriche und strikete tragen nicht zur Bestimmung der Blackbox bei, da diese tatsächlich vom Renderer gezeichnet werden, der in einer Vielzahl von Stilen gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c256e-118">Underlines and strikethroughs do not contribute to the black box determination, since these are actually drawn by the renderer, which is allowed to draw them in any variety of styles.</span></span>

## <a name="requirements"></a><span data-ttu-id="c256e-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c256e-119">Requirements</span></span>



| <span data-ttu-id="c256e-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c256e-120">Requirement</span></span> | <span data-ttu-id="c256e-121">Wert</span><span class="sxs-lookup"><span data-stu-id="c256e-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c256e-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c256e-122">Library</span></span><br/> | <dl> <span data-ttu-id="c256e-123"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c256e-123"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="c256e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="c256e-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="c256e-125"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c256e-125"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c256e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c256e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c256e-127">**Idschreitetextlayout**</span><span class="sxs-lookup"><span data-stu-id="c256e-127">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[<span data-ttu-id="c256e-128">**Idschreitetextlayout**</span><span class="sxs-lookup"><span data-stu-id="c256e-128">**IDWriteTextLayout**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

