---
title: Sättigungseffekt
description: Verwenden Sie diesen Effekt, um die Sättigung eines Bilds zu ändern.
ms.assetid: 03A374D9-BED4-49ED-B90E-21193909C8AB
keywords:
- sättigungseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d6912e64c9297a3554b4785128e1282a3974d36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040482"
---
# <a name="saturation-effect"></a><span data-ttu-id="6de41-104">Sättigungseffekt</span><span class="sxs-lookup"><span data-stu-id="6de41-104">Saturation effect</span></span>

<span data-ttu-id="6de41-105">Verwenden Sie diesen Effekt, um die Sättigung eines Bilds zu ändern.</span><span class="sxs-lookup"><span data-stu-id="6de41-105">Use this effect to alter the saturation of an image.</span></span> <span data-ttu-id="6de41-106">Der sättigungseffekt ist eine Spezialisierung des [Farbmatrix](color-matrix.md) Effekts.</span><span class="sxs-lookup"><span data-stu-id="6de41-106">The saturation effect is a specialization of the [color matrix](color-matrix.md) effect.</span></span>

<span data-ttu-id="6de41-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1Saturation.</span><span class="sxs-lookup"><span data-stu-id="6de41-107">The CLSID for this effect is CLSID\_D2D1Saturation.</span></span>

-   [<span data-ttu-id="6de41-108">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="6de41-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="6de41-109">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6de41-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="6de41-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de41-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="6de41-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6de41-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="6de41-112">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="6de41-112">Example image</span></span>

<span data-ttu-id="6de41-113">Das Beispiel zeigt die Eingabe-und Ausgabe Bilder des Sättigungs Effekts mit einer Sättigung von 0%.</span><span class="sxs-lookup"><span data-stu-id="6de41-113">The example here shows the input and output images of the saturation effect with a saturation of 0%.</span></span>



| <span data-ttu-id="6de41-114">Vorher</span><span class="sxs-lookup"><span data-stu-id="6de41-114">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)  |
| <span data-ttu-id="6de41-116">Nach</span><span class="sxs-lookup"><span data-stu-id="6de41-116">After</span></span>                                                       |
| ![das Bild nach der Transformation.](images/16-saturation.png) |



 


```C++
ComPtr<ID2D1Effect> saturationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Saturation, &saturationEffect);

saturationEffect->SetInput(0, bitmap);

saturationEffect->SetValue(D2D1_SATURATION_PROP_SATURATION, 0.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(saturationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="6de41-118">Der Effekt berechnet eine Farbmatrix basierend auf dem Sättigungswert (*s* in der Gleichung hier), den Sie mit der Eigenschaft "D2D1 \_ Sättigung Prop-Sättigung" angeben \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="6de41-118">The effect calculates a color matrix based on the saturation value (*s* in the equation here) you specify with the D2D1\_SATURATION\_PROP\_SATURATION property.</span></span> <span data-ttu-id="6de41-119">Die Matrix Gleichung wird hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6de41-119">The matrix equation is shown here.</span></span>

![Formel zum Berechnen einer Sättigungs Matrix.](images/saturation-formula.png)

<span data-ttu-id="6de41-121">Die erstellte Matrix hängt nur vom Sättigungswert ab.</span><span class="sxs-lookup"><span data-stu-id="6de41-121">The matrix created depends only on the saturation value.</span></span> <span data-ttu-id="6de41-122">Sie können den [Farbmatrix](color-matrix.md) Effekt verwenden, wenn Sie eine bestimmte Matrix benötigen.</span><span class="sxs-lookup"><span data-stu-id="6de41-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

<span data-ttu-id="6de41-123">Diese Auswirkung verarbeitet und gibt vorab multiplizierte Alpha Bilder aus.</span><span class="sxs-lookup"><span data-stu-id="6de41-123">This effect consumes and outputs premultiplied alpha images.</span></span> <span data-ttu-id="6de41-124">Der Effekt funktioniert nicht bei geraden Alpha Bildern, es sei denn, Sie sind vollständig undurchsichtig.</span><span class="sxs-lookup"><span data-stu-id="6de41-124">The effect won't work on straight alpha images unless they are fully opaque.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="6de41-125">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="6de41-125">Effect properties</span></span>



| <span data-ttu-id="6de41-126">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="6de41-126">Display name and index enumeration</span></span>                                  | <span data-ttu-id="6de41-127">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="6de41-127">Type and default value</span></span>           | <span data-ttu-id="6de41-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6de41-128">Description</span></span>                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6de41-129">Sättigung</span><span class="sxs-lookup"><span data-stu-id="6de41-129">Saturation</span></span><br/> <span data-ttu-id="6de41-130">Sättigung der D2D1 \_ Sättigung \_ \_</span><span class="sxs-lookup"><span data-stu-id="6de41-130">D2D1\_SATURATION\_PROP\_SATURATION</span></span><br/> | <span data-ttu-id="6de41-131">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="6de41-131">FLOAT</span></span><br/> <span data-ttu-id="6de41-132">0,5 f</span><span class="sxs-lookup"><span data-stu-id="6de41-132">0.5f</span></span><br/> | <span data-ttu-id="6de41-133">Die Sättigung des Bilds.</span><span class="sxs-lookup"><span data-stu-id="6de41-133">The saturation of the image.</span></span> <span data-ttu-id="6de41-134">Sie können die Sättigung auf einen Wert zwischen 0 und 1 festlegen.</span><span class="sxs-lookup"><span data-stu-id="6de41-134">You can set the saturation to a value between 0 and 1.</span></span> <span data-ttu-id="6de41-135">Wenn Sie den Wert auf 1 festlegen, ist das Ausgabe Bild vollständig ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="6de41-135">If you set it to 1 the output image is fully saturated.</span></span> <span data-ttu-id="6de41-136">Wenn Sie den Wert auf 0 festlegen, ist das Ausgabe Bild Monochrome.</span><span class="sxs-lookup"><span data-stu-id="6de41-136">If you set it to 0 the output image is monochrome.</span></span> <span data-ttu-id="6de41-137">Der Sättigungswert ist unitless.</span><span class="sxs-lookup"><span data-stu-id="6de41-137">The saturation value is unitless.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="6de41-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6de41-138">Requirements</span></span>



| <span data-ttu-id="6de41-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6de41-139">Requirement</span></span> | <span data-ttu-id="6de41-140">Wert</span><span class="sxs-lookup"><span data-stu-id="6de41-140">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6de41-141">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6de41-141">Minimum supported client</span></span> | <span data-ttu-id="6de41-142">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6de41-142">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6de41-143">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6de41-143">Minimum supported server</span></span> | <span data-ttu-id="6de41-144">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6de41-144">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="6de41-145">Header</span><span class="sxs-lookup"><span data-stu-id="6de41-145">Header</span></span>                   | <span data-ttu-id="6de41-146">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="6de41-146">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="6de41-147">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6de41-147">Library</span></span>                  | <span data-ttu-id="6de41-148">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="6de41-148">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="6de41-149">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6de41-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6de41-150">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="6de41-150">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

