---
title: ID2D1RenderTarget fillopacitymask-Methoden
description: Wendet die durch die angegebene Bitmap beschriebene Deck Kraft Maske auf einen Pinsel an und verwendet diesen Pinsel zum Zeichnen eines Bereichs des Renderziels.
ms.assetid: a5e56d8a-2929-4f7b-b1c4-fb358c202721
keywords:
- Fillopacitymask-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: e988994b849c193725dfdd75773f22a63fed6754
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368304"
---
# <a name="id2d1rendertargetfillopacitymask-methods"></a><span data-ttu-id="27749-104">ID2D1RenderTarget:: fillopacitymask-Methoden</span><span class="sxs-lookup"><span data-stu-id="27749-104">ID2D1RenderTarget::FillOpacityMask methods</span></span>

<span data-ttu-id="27749-105">Wendet die durch die angegebene Bitmap beschriebene Deck Kraft Maske auf einen Pinsel an und verwendet diesen Pinsel zum Zeichnen eines Bereichs des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="27749-105">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span>

### <a name="overload-list"></a><span data-ttu-id="27749-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="27749-106">Overload list</span></span>



| <span data-ttu-id="27749-107">Methode</span><span class="sxs-lookup"><span data-stu-id="27749-107">Method</span></span>                                                                                                                                                                                                                          | <span data-ttu-id="27749-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="27749-108">Description</span></span>                                                                                                                                   |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27749-109">[**Fillopacitymask (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 \_ Opacity \_ mask \_ Content, D2D \_ Rect \_ f&, D2D \_ Rect \_ f&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="27749-109">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F&,D2D\_RECT\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f__constd2d1_rect_f_))</span></span>       | <span data-ttu-id="27749-110">Wendet die durch die angegebene Bitmap beschriebene Deck Kraft Maske auf einen Pinsel an und verwendet diesen Pinsel zum Zeichnen eines Bereichs des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="27749-110">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |
| <span data-ttu-id="27749-111">[**Fillopacitymask (ID2D1Bitmap \* , ID2D1Brush \* , D2D1 \_ Opacity \_ mask \_ Content, D2D \_ Rect \_ f \* , D2D \_ Rect \_ f \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span><span class="sxs-lookup"><span data-stu-id="27749-111">[**FillOpacityMask(ID2D1Bitmap\*,ID2D1Brush\*,D2D1\_OPACITY\_MASK\_CONTENT,D2D\_RECT\_F\*,D2D\_RECT\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillopacitymask(id2d1bitmap_id2d1brush_d2d1_opacity_mask_content_constd2d1_rect_f_constd2d1_rect_f))</span></span> | <span data-ttu-id="27749-112">Wendet die durch die angegebene Bitmap beschriebene Deck Kraft Maske auf einen Pinsel an und verwendet diesen Pinsel zum Zeichnen eines Bereichs des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="27749-112">Applies the opacity mask described by the specified bitmap to a brush and uses that brush to paint a region of the render target.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="27749-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27749-113">Remarks</span></span>

<span data-ttu-id="27749-114">Damit diese Methode ordnungsgemäß funktioniert, muss das Renderziel den Antialiasing-Modus für den [**D2D1- \_ Antialias \_ Modus \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) verwenden.</span><span class="sxs-lookup"><span data-stu-id="27749-114">For this method to work properly, the render target must be using the [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) antialiasing mode.</span></span> <span data-ttu-id="27749-115">Sie können den Antialiasing Modus festlegen, indem Sie die [**ID2D1RenderTarget:: setantialiasmode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="27749-115">You can set the antialiasing mode by calling the [**ID2D1RenderTarget::SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) method.</span></span>

<span data-ttu-id="27749-116">Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="27749-116">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="27749-117">Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **fillopacitymask**) fehlgeschlagen ist, überprüfen Sie das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="27749-117">To determine whether a drawing operation (such as **FillOpacityMask**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="27749-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="27749-118">Requirements</span></span>



| <span data-ttu-id="27749-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="27749-119">Requirement</span></span> | <span data-ttu-id="27749-120">Wert</span><span class="sxs-lookup"><span data-stu-id="27749-120">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="27749-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="27749-121">Library</span></span><br/> | <dl> <span data-ttu-id="27749-122"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="27749-122"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="27749-123">DLL</span><span class="sxs-lookup"><span data-stu-id="27749-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="27749-124"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27749-124"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27749-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="27749-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27749-126">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="27749-126">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

