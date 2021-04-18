---
title: Idwrite teinlineobject gedeverhangmetrics-Methode
description: Idwrite tetextlayout ruft diese Rückruffunktion auf, um die sichtbaren Blöcke (in Dips) des Inline Objekts abzurufen. Im Fall einer einfachen Bitmap ohne Auffüll-und nicht Überlastung werden alle Überhängen einfach als Nullen angezeigt.
ms.assetid: b3b3e9f0-ee35-4117-9a62-a975c03b5ca9
keywords:
- Getverhangmetrics-Methode direkt schreiben
- Getverhangmetrics-Methode Direct Write, idwrite teinlineobject-Schnittstelle
- Idwrite teinlineobject Interface Direct Write, gedeverhangmetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteInlineObject.GetOverhangMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0960f28394c5b55c3377136451a5c13748edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371416"
---
# <a name="idwriteinlineobjectgetoverhangmetrics-method"></a><span data-ttu-id="76a98-107">Idwrite teinlineobject:: gedeverhangmetrics-Methode</span><span class="sxs-lookup"><span data-stu-id="76a98-107">IDWriteInlineObject::GetOverhangMetrics method</span></span>

<span data-ttu-id="76a98-108">[**Idwrite tetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) ruft diese Rückruffunktion auf, um die sichtbaren Blöcke (in Dips) des Inline Objekts abzurufen.</span><span class="sxs-lookup"><span data-stu-id="76a98-108">[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) calls this callback function to get the visible extents (in DIPs) of the inline object.</span></span> <span data-ttu-id="76a98-109">Im Fall einer einfachen Bitmap ohne Auffüll-und nicht Überlastung werden alle Überhängen einfach als Nullen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76a98-109">In the case of a simple bitmap, with no padding and no overhang, all the overhangs will simply be zeroes.</span></span>

<span data-ttu-id="76a98-110">Die über schreibungen sollten relativ zur gemeldeten Größe des Objekts zurückgegeben werden (siehe [**dwrite- \_ Inline \_ \_ objektmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)) und sollten nicht an die Baseline angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="76a98-110">The overhangs should be returned relative to the reported size of the object (see [**DWRITE\_INLINE\_OBJECT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_inline_object_metrics)), and should not be baseline adjusted.</span></span>

## <a name="syntax"></a><span data-ttu-id="76a98-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="76a98-111">Syntax</span></span>


```C++
virtual HRESULT GetOverhangMetrics(
  [out] DWRITE_OVERHANG_METRICS *overhangs
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="76a98-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="76a98-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76a98-113">*überlastet* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="76a98-113">*overhangs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="76a98-114">Typ: **[ **dwrite- \_ \_ overhängenmetriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="76a98-114">Type: **[**DWRITE\_OVERHANG\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_overhang_metrics)\***</span></span>

<span data-ttu-id="76a98-115">Überschreibung der sichtbaren Blöcke (in Dips) außerhalb des Objekts.</span><span class="sxs-lookup"><span data-stu-id="76a98-115">Overshoot of visible extents (in DIPs) outside the object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76a98-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="76a98-116">Return value</span></span>

<span data-ttu-id="76a98-117">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="76a98-117">Type: **HRESULT**</span></span>

<span data-ttu-id="76a98-118">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="76a98-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="76a98-119">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="76a98-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="76a98-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76a98-120">Requirements</span></span>



| <span data-ttu-id="76a98-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76a98-121">Requirement</span></span> | <span data-ttu-id="76a98-122">Wert</span><span class="sxs-lookup"><span data-stu-id="76a98-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="76a98-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="76a98-123">Library</span></span><br/> | <dl> <span data-ttu-id="76a98-124"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="76a98-124"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="76a98-125">DLL</span><span class="sxs-lookup"><span data-stu-id="76a98-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="76a98-126"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="76a98-126"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76a98-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76a98-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76a98-128">**Idwrite teinlineobject**</span><span class="sxs-lookup"><span data-stu-id="76a98-128">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> <dt>

[<span data-ttu-id="76a98-129">**Idwrite teinlineobject**</span><span class="sxs-lookup"><span data-stu-id="76a98-129">**IDWriteInlineObject**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject)
</dt> </dl>

 

