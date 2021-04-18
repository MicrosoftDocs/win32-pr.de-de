---
title: ID2D1RenderTarget pushaxisalignedclip-Methoden (D2d1 \_ 1. h)
description: Gibt ein Rechteck an, auf das alle nachfolgenden Zeichnungsvorgänge zugeschnitten werden.
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- Pushaxisalignedclip-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361063"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a><span data-ttu-id="31c3a-104">ID2D1RenderTarget::P ushaxisalignedclip-Methoden</span><span class="sxs-lookup"><span data-stu-id="31c3a-104">ID2D1RenderTarget::PushAxisAlignedClip methods</span></span>

<span data-ttu-id="31c3a-105">Gibt ein Rechteck an, auf das alle nachfolgenden Zeichnungsvorgänge zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="31c3a-105">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span>

### <a name="overload-list"></a><span data-ttu-id="31c3a-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="31c3a-106">Overload list</span></span>



| <span data-ttu-id="31c3a-107">Methode</span><span class="sxs-lookup"><span data-stu-id="31c3a-107">Method</span></span>                                                                                                                                         | <span data-ttu-id="31c3a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="31c3a-108">Description</span></span>                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| <span data-ttu-id="31c3a-109">[**Pushaxisalignedclip (D2D1 \_ Rect \_ F&, D2D1 \_ Antialias \_ Mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="31c3a-109">[**PushAxisAlignedClip(D2D1\_RECT\_F&,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span>  | <span data-ttu-id="31c3a-110">Gibt ein Rechteck an, auf das alle nachfolgenden Zeichnungsvorgänge zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="31c3a-110">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |
| <span data-ttu-id="31c3a-111">[**Pushaxisalignedclip (D2D1 \_ Rect \_ F \* , D2D1 \_ Antialias \_ Mode)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span><span class="sxs-lookup"><span data-stu-id="31c3a-111">[**PushAxisAlignedClip(D2D1\_RECT\_F\*,D2D1\_ANTIALIAS\_MODE)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))</span></span> | <span data-ttu-id="31c3a-112">Gibt ein Rechteck an, auf das alle nachfolgenden Zeichnungsvorgänge zugeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="31c3a-112">Specifies a rectangle to which all subsequent drawing operations are clipped.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="31c3a-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31c3a-113">Remarks</span></span>

<span data-ttu-id="31c3a-114">Ein [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) -und [**popaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) -Paar kann um oder innerhalb einer [**pushschicht**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) und [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)auftreten, sich aber nicht überlappen.</span><span class="sxs-lookup"><span data-stu-id="31c3a-114">A [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pair can occur around or within a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), but cannot overlap.</span></span> <span data-ttu-id="31c3a-115">Beispielsweise ist die Sequenz von **pushaxisalignedclip**, [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **poplayer** und **popaxisalignedclip** gültig, aber die Sequenz von **pushaxisalignedclip**, **pushlayer**, **popaxisalignedclip** und **poplayer** ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="31c3a-115">For example, the sequence of **PushAxisAlignedClip**, [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)), **PopLayer**, **PopAxisAlignedClip** is valid, but the sequence of **PushAxisAlignedClip**, **PushLayer**, **PopAxisAlignedClip**, **PopLayer** is invalid.</span></span>

<span data-ttu-id="31c3a-116">Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="31c3a-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="31c3a-117">Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **pushaxisalignedclip**) fehlgeschlagen ist, überprüfen Sie das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="31c3a-117">To determine whether a drawing operation (such as **PushAxisAlignedClip**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="31c3a-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31c3a-118">Examples</span></span>

<span data-ttu-id="31c3a-119">Ein Beispiel finden [Sie unter How to Clip with an Axis-Aligned Clip Rechteck](how-to-clip-with-axis-aligned-rects.md).</span><span class="sxs-lookup"><span data-stu-id="31c3a-119">For an example, see the [How to Clip with an Axis-Aligned Clip Rectangle](how-to-clip-with-axis-aligned-rects.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="31c3a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="31c3a-120">Requirements</span></span>



| <span data-ttu-id="31c3a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="31c3a-121">Requirement</span></span> | <span data-ttu-id="31c3a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="31c3a-122">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31c3a-123">Header</span><span class="sxs-lookup"><span data-stu-id="31c3a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="31c3a-124"><dt>D2d1 \_ 1. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="31c3a-124"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="31c3a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="31c3a-125">Library</span></span><br/> | <dl> <span data-ttu-id="31c3a-126"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="31c3a-126"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="31c3a-127">DLL</span><span class="sxs-lookup"><span data-stu-id="31c3a-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="31c3a-128"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="31c3a-128"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="31c3a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31c3a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="31c3a-130">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="31c3a-130">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

<span data-ttu-id="31c3a-131">�</span><span class="sxs-lookup"><span data-stu-id="31c3a-131">�</span></span>

<span data-ttu-id="31c3a-132">�</span><span class="sxs-lookup"><span data-stu-id="31c3a-132">�</span></span>
