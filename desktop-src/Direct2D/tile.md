---
title: Kachel Effekt
description: Verwenden Sie den Kachel Effekt, um den angegebenen Bereich des Bilds zu wiederholen.
ms.assetid: C7505DBF-5F79-4407-84C4-634EA7EC06B7
keywords:
- Kachel Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c5def48ab30cadb28673179f6eec5d7ffa7e19e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040688"
---
# <a name="tile-effect"></a><span data-ttu-id="71129-104">Kachel Effekt</span><span class="sxs-lookup"><span data-stu-id="71129-104">Tile effect</span></span>

<span data-ttu-id="71129-105">Verwenden Sie den Kachel Effekt, um den angegebenen Bereich des Bilds zu wiederholen.</span><span class="sxs-lookup"><span data-stu-id="71129-105">Use the tile effect to repeat the specified region of the image.</span></span>

<span data-ttu-id="71129-106">Die CLSID für diesen Effekt ist CLSID \_ D2D1Tile.</span><span class="sxs-lookup"><span data-stu-id="71129-106">The CLSID for this effect is CLSID\_D2D1Tile.</span></span>

## <a name="example-image"></a><span data-ttu-id="71129-107">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="71129-107">Example image</span></span>



| <span data-ttu-id="71129-108">Vorher</span><span class="sxs-lookup"><span data-stu-id="71129-108">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| <span data-ttu-id="71129-110">Nach</span><span class="sxs-lookup"><span data-stu-id="71129-110">After</span></span>                                                      |
| ![das Bild nach der Transformation.](images/9-tile.png)       |



 


```C++
ComPtr<ID2D1Effect> tileEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Tile, &tileEffect);

tileEffect->SetInput(0, bitmap);

tileEffect->SetValue(D2D1_TILE_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(tileEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="71129-112">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="71129-112">Effect properties</span></span>



| <span data-ttu-id="71129-113">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="71129-113">Display name and index enumeration</span></span>                | <span data-ttu-id="71129-114">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="71129-114">Type and default value</span></span>                                              | <span data-ttu-id="71129-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="71129-115">Description</span></span>                                                                                                                                        |
|---------------------------------------------------|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71129-116">Rect</span><span class="sxs-lookup"><span data-stu-id="71129-116">Rect</span></span><br/> <span data-ttu-id="71129-117">D2D1- \_ Kachel- \_ Prop- \_ Rect</span><span class="sxs-lookup"><span data-stu-id="71129-117">D2D1\_TILE\_PROP\_RECT</span></span><br/> | <span data-ttu-id="71129-118">D2D1 \_ Vector \_ 4f</span><span class="sxs-lookup"><span data-stu-id="71129-118">D2D1\_VECTOR\_4F</span></span><br/> <span data-ttu-id="71129-119">{0,0 f, 0,0 f, 100,0 f, 100,0 f}</span><span class="sxs-lookup"><span data-stu-id="71129-119">{0.0f, 0.0f, 100.0f, 100.0f}</span></span><br/> | <span data-ttu-id="71129-120">Der Bereich des Bilds, das gekachelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="71129-120">The region of the image to be tiled.</span></span> <span data-ttu-id="71129-121">Diese Eigenschaft ist ein D2D1 \_ Vector \_ 4f, definiert als: (Links, oben, rechts, unten).</span><span class="sxs-lookup"><span data-stu-id="71129-121">This property is a D2D1\_VECTOR\_4F defined as: (left, top, right, bottom).</span></span> <span data-ttu-id="71129-122">Die Einheiten befinden sich in Dips.</span><span class="sxs-lookup"><span data-stu-id="71129-122">The units are in DIPs.</span></span><br/> |



 

## <a name="output-bitmap"></a><span data-ttu-id="71129-123">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="71129-123">Output bitmap</span></span>

<span data-ttu-id="71129-124">Dieser Effekt generiert eine Bitmap mit logischer unbegrenzter groß.</span><span class="sxs-lookup"><span data-stu-id="71129-124">This effect generates a logically infinite sized bitmap.</span></span>

<span data-ttu-id="71129-125">Sie können ein Bildkacheln und eine bestimmte Größe ohne zusätzliche Effekte ausgeben, indem Sie die Größe beim Abrufen von [**ID2D1DeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))festlegen.</span><span class="sxs-lookup"><span data-stu-id="71129-125">You can tile an image and output a certain size without any additional effects by setting the size when you call [**ID2D1DeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)).</span></span>

## <a name="requirements"></a><span data-ttu-id="71129-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71129-126">Requirements</span></span>



| <span data-ttu-id="71129-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71129-127">Requirement</span></span> | <span data-ttu-id="71129-128">Wert</span><span class="sxs-lookup"><span data-stu-id="71129-128">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71129-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="71129-129">Minimum supported client</span></span> | <span data-ttu-id="71129-130">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71129-130">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="71129-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="71129-131">Minimum supported server</span></span> | <span data-ttu-id="71129-132">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="71129-132">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="71129-133">Header</span><span class="sxs-lookup"><span data-stu-id="71129-133">Header</span></span>                   | <span data-ttu-id="71129-134">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="71129-134">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="71129-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71129-135">Library</span></span>                  | <span data-ttu-id="71129-136">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="71129-136">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="71129-137">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="71129-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71129-138">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="71129-138">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

