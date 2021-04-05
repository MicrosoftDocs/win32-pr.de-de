---
title: Anbau Effekt
description: Verwenden Sie den Anbau Effekt, um einen angegebenen Bereich eines Bilds auszugeben.
ms.assetid: DFB7DE20-F202-4E7F-AE63-94BF817B6E30
keywords:
- Anbau Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 653ceaf4cf8b5922fe05e151c1639269f3169b57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858874"
---
# <a name="crop-effect"></a><span data-ttu-id="b81e1-104">Anbau Effekt</span><span class="sxs-lookup"><span data-stu-id="b81e1-104">Crop effect</span></span>

<span data-ttu-id="b81e1-105">Verwenden Sie den Anbau Effekt, um einen angegebenen Bereich eines Bilds auszugeben.</span><span class="sxs-lookup"><span data-stu-id="b81e1-105">Use the crop effect to output a specified region of an image.</span></span>

<span data-ttu-id="b81e1-106">Die CLSID für diesen Effekt ist CLSID \_ D2D1Crop.</span><span class="sxs-lookup"><span data-stu-id="b81e1-106">The CLSID for this effect is CLSID\_D2D1Crop.</span></span>

-   [<span data-ttu-id="b81e1-107">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="b81e1-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="b81e1-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b81e1-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b81e1-109">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="b81e1-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="b81e1-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b81e1-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b81e1-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b81e1-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="b81e1-112">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="b81e1-112">Example image</span></span>



| <span data-ttu-id="b81e1-113">Vorher</span><span class="sxs-lookup"><span data-stu-id="b81e1-113">Before</span></span>                                                     |
|------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg) |
| <span data-ttu-id="b81e1-115">Nach</span><span class="sxs-lookup"><span data-stu-id="b81e1-115">After</span></span>                                                      |
| ![das Bild nach der Transformation.](images/8-crop.png)       |



 


```C++
ComPtr<ID2D1Effect> cropEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Crop, &cropEffect);

cropEffect->SetInput(0, bitmap);
cropEffect->SetValue(D2D1_CROP_PROP_RECT, D2D1::RectF(0.0f, 0.0f, 256.0f, 192.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(cropEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="b81e1-117">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b81e1-117">Effect properties</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b81e1-118">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="b81e1-118">Display name and index enumeration</span></span></th>
<th><span data-ttu-id="b81e1-119">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="b81e1-119">Type and default value</span></span></th>
<th><span data-ttu-id="b81e1-120">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b81e1-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b81e1-121">Rect</span><span class="sxs-lookup"><span data-stu-id="b81e1-121">Rect</span></span><br/></td>
<td><span data-ttu-id="b81e1-122">D2D1_VECTOR_4F</span><span class="sxs-lookup"><span data-stu-id="b81e1-122">D2D1_VECTOR_4F</span></span><br/></td>
<td><span data-ttu-id="b81e1-123">Der Bereich, der als Vektor im Formular (Links, oben, Breite, Höhe) festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b81e1-123">The region to be cropped specified as a vector in the form (left, top, width, height).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b81e1-124">D2D1_CROP_PROP_RECT</span><span class="sxs-lookup"><span data-stu-id="b81e1-124">D2D1_CROP_PROP_RECT</span></span><br/></td>
<td><span data-ttu-id="b81e1-125">{-FLT_MAX,-FLT_MAX, FLT_MAX, FLT_MAX}</span><span class="sxs-lookup"><span data-stu-id="b81e1-125">{-FLT_MAX, -FLT_MAX, FLT_MAX, FLT_MAX}</span></span><br/></td>
<td><span data-ttu-id="b81e1-126">Die Einheiten befinden sich in Dips.</span><span class="sxs-lookup"><span data-stu-id="b81e1-126">The units are in DIPs.</span></span> <br/>
<blockquote>
<p>[!Note]</p>
<p><span data-ttu-id="b81e1-127">Der Rect wird abgeschnitten, wenn die Randgrenzen des Eingabe Bilds überlappt werden.</span><span class="sxs-lookup"><span data-stu-id="b81e1-127">The Rect will be truncated if it overlaps the edge boundaries of the input image.</span></span><br/></p>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b81e1-128">D2D1_CROP_PROP_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="b81e1-128">D2D1_CROP_PROP_BORDER_MODE</span></span><br/></td>
<td><span data-ttu-id="b81e1-129">D2D1_BORDER_MODE</span><span class="sxs-lookup"><span data-stu-id="b81e1-129">D2D1_BORDER_MODE</span></span> <br/> <span data-ttu-id="b81e1-130">D2D1_BORDER_MODE_SOFT</span><span class="sxs-lookup"><span data-stu-id="b81e1-130">D2D1_BORDER_MODE_SOFT</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="b81e1-131">D2D1_BORDER_MODE_SOFT: Wenn das Zuweisungs Rechteck in Bruch Komma Koordinaten fällt, wendet der Effekt das Antialiasing an, das zu einem Soft Edge führt.</span><span class="sxs-lookup"><span data-stu-id="b81e1-131">D2D1_BORDER_MODE_SOFT : If the crop rectangle falls on fractional pixel coordinates, the effect applies antialiasing which results in a soft edge.</span></span></li>
<li><span data-ttu-id="b81e1-132">D2D1_BORDER_MODE_HARD: Wenn das Zuweisungs Rechteck auf Pixelkoordinaten mit Bruchteilen fällt, wird der Effekt durch einen festen Rand fest.</span><span class="sxs-lookup"><span data-stu-id="b81e1-132">D2D1_BORDER_MODE_HARD : If the crop rectangle falls on fractional pixel coordinates, the effect clamps which results in a hard edge.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="output-bitmap"></a><span data-ttu-id="b81e1-133">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="b81e1-133">Output bitmap</span></span>

<span data-ttu-id="b81e1-134">Die Ausgabe dieses Effekts ist die Größe der Rect-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b81e1-134">The output of this effect is the size of the Rect property.</span></span> <span data-ttu-id="b81e1-135">Länge und Breite sind Calc</span><span class="sxs-lookup"><span data-stu-id="b81e1-135">The length and width are calc</span></span>

<span data-ttu-id="b81e1-136">mithilfe der Gleichungen in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="b81e1-136">ulated using the equations here:</span></span> <dl> <span data-ttu-id="b81e1-137">Ausgabe Länge in Pixel = (Rect. Right-Rect. Left) \* (dpi/96 des Benutzers)</span><span class="sxs-lookup"><span data-stu-id="b81e1-137">Output length in Pixels=(Rect.Right-Rect.Left)\*(User's DPI/96)</span></span>  
<span data-ttu-id="b81e1-138">Ausgabe Höhe in Pixel = (Rect. Bottom-Rect.Top) \* (dpi/96 des Benutzers)</span><span class="sxs-lookup"><span data-stu-id="b81e1-138">Output height in pixels=(Rect.Bottom-Rect.Top)\*(User's DPI/96)</span></span>  
</dl>

## <a name="requirements"></a><span data-ttu-id="b81e1-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b81e1-139">Requirements</span></span>



| <span data-ttu-id="b81e1-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b81e1-140">Requirement</span></span> | <span data-ttu-id="b81e1-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b81e1-141">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b81e1-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b81e1-142">Minimum supported client</span></span> | <span data-ttu-id="b81e1-143">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b81e1-143">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b81e1-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b81e1-144">Minimum supported server</span></span> | <span data-ttu-id="b81e1-145">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b81e1-145">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b81e1-146">Header</span><span class="sxs-lookup"><span data-stu-id="b81e1-146">Header</span></span>                   | <span data-ttu-id="b81e1-147">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b81e1-147">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b81e1-148">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b81e1-148">Library</span></span>                  | <span data-ttu-id="b81e1-149">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b81e1-149">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b81e1-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b81e1-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b81e1-151">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b81e1-151">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

