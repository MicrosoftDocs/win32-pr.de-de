---
title: Effekt der Hue-rotatung
description: Verwenden Sie den Effekt Hue Drehung, um den Farbton eines Bilds zu ändern, indem Sie eine Farbmatrix auf Grundlage des Drehwinkels anwenden.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- Effekt der Hue-rotatung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104551345"
---
# <a name="hue-rotatation-effect"></a><span data-ttu-id="94f28-104">Effekt der Hue-rotatung</span><span class="sxs-lookup"><span data-stu-id="94f28-104">Hue rotatation effect</span></span>

<span data-ttu-id="94f28-105">Verwenden Sie den Effekt Hue Drehung, um den Farbton eines Bilds zu ändern, indem Sie eine Farbmatrix auf Grundlage des Drehwinkels anwenden.</span><span class="sxs-lookup"><span data-stu-id="94f28-105">Use the hue rotate effect to alter the hue of an image by applying a color matrix based on the rotation angle.</span></span>

<span data-ttu-id="94f28-106">Die CLSID für diesen Effekt ist CLSID \_ D2D1HueRotation.</span><span class="sxs-lookup"><span data-stu-id="94f28-106">The CLSID for this effect is CLSID\_D2D1HueRotation.</span></span>

-   [<span data-ttu-id="94f28-107">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="94f28-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="94f28-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94f28-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="94f28-109">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="94f28-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="94f28-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94f28-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="94f28-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94f28-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="94f28-112">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="94f28-112">Example image</span></span>

<span data-ttu-id="94f28-113">Das Beispiel zeigt die Eingabe-und Ausgabe Bilder des Hue-Drehungs Effekts mit einem Drehungs Winkel von 270 Grad.</span><span class="sxs-lookup"><span data-stu-id="94f28-113">The example here shows the input and output images of the hue rotate effect with a rotation angle of 270 degrees.</span></span>



| <span data-ttu-id="94f28-114">Vorher</span><span class="sxs-lookup"><span data-stu-id="94f28-114">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)   |
| <span data-ttu-id="94f28-116">Nach</span><span class="sxs-lookup"><span data-stu-id="94f28-116">After</span></span>                                                        |
| ![das Bild nach der Transformation.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="94f28-118">Der Effekt berechnet eine Farbmatrix basierend auf dem Drehungs Winkel (*?*), den Sie mit der \_ \_ Prop Angle-Eigenschaft D2D1 huerotation angeben \_ .</span><span class="sxs-lookup"><span data-stu-id="94f28-118">The effect calculates a color matrix based on the rotation angle (*?*) you specify with the D2D1\_HUEROTATION\_PROP\_ANGLE property.</span></span> <span data-ttu-id="94f28-119">Im folgenden finden Sie die Matrix Gleichungen.</span><span class="sxs-lookup"><span data-stu-id="94f28-119">Here are the matrix equations.</span></span>

![Hue-Rotations Berechnungen](images/hue-formula.png)

<span data-ttu-id="94f28-121">Die erstellte Matrix hängt nur vom Drehungs Winkel ab.</span><span class="sxs-lookup"><span data-stu-id="94f28-121">The matrix created depends only on the rotation angle.</span></span> <span data-ttu-id="94f28-122">Sie können den [Farbmatrix](color-matrix.md) Effekt verwenden, wenn Sie eine bestimmte Matrix benötigen.</span><span class="sxs-lookup"><span data-stu-id="94f28-122">You can use the [color matrix](color-matrix.md) effect if you need a specific matrix.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="94f28-123">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="94f28-123">Effect properties</span></span>



| <span data-ttu-id="94f28-124">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="94f28-124">Display name and index enumeration</span></span>                         | <span data-ttu-id="94f28-125">Typ und Standardwert</span><span class="sxs-lookup"><span data-stu-id="94f28-125">Type and default value</span></span>           | <span data-ttu-id="94f28-126">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94f28-126">Description</span></span>                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| <span data-ttu-id="94f28-127">Angle</span><span class="sxs-lookup"><span data-stu-id="94f28-127">Angle</span></span><br/> <span data-ttu-id="94f28-128">D2D1 \_ huerotations- \_ Prop- \_ Winkel</span><span class="sxs-lookup"><span data-stu-id="94f28-128">D2D1\_HUEROTATION\_PROP\_ANGLE</span></span><br/> | <span data-ttu-id="94f28-129">GLEITKOMMAZAHL</span><span class="sxs-lookup"><span data-stu-id="94f28-129">FLOAT</span></span><br/> <span data-ttu-id="94f28-130">0,0 f</span><span class="sxs-lookup"><span data-stu-id="94f28-130">0.0f</span></span><br/> | <span data-ttu-id="94f28-131">Der Winkel, um den Farbton in Grad zu drehen.</span><span class="sxs-lookup"><span data-stu-id="94f28-131">The angle to rotate the hue, in degrees.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="94f28-132">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="94f28-132">Output bitmap</span></span>

<span data-ttu-id="94f28-133">Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.</span><span class="sxs-lookup"><span data-stu-id="94f28-133">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="94f28-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="94f28-134">Requirements</span></span>



| <span data-ttu-id="94f28-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="94f28-135">Requirement</span></span> | <span data-ttu-id="94f28-136">Wert</span><span class="sxs-lookup"><span data-stu-id="94f28-136">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94f28-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="94f28-137">Minimum supported client</span></span> | <span data-ttu-id="94f28-138">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94f28-138">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="94f28-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="94f28-139">Minimum supported server</span></span> | <span data-ttu-id="94f28-140">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="94f28-140">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="94f28-141">Header</span><span class="sxs-lookup"><span data-stu-id="94f28-141">Header</span></span>                   | <span data-ttu-id="94f28-142">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="94f28-142">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="94f28-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="94f28-143">Library</span></span>                  | <span data-ttu-id="94f28-144">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="94f28-144">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="94f28-145">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="94f28-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="94f28-146">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="94f28-146">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

