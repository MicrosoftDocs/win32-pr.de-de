---
title: Auswirkung der dpi-Kompensation
description: Verwenden Sie den dpi-Kompensierungs Effekt, um eine Eingabe Bitmap automatisch an den dpi-Kontext des Kontexts anzupassen. Dies ist nützlich für Situationen, in denen eine Bitmap auf einem anderen dpi-Wert als der Bildschirm erstellt oder geladen wird.
ms.assetid: EA8AD89B-A710-468F-A6F3-474DA29586F1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a0477d2a57f39738fa9b1ce16c97995c60cf96
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859319"
---
# <a name="dpi-compensation-effect"></a><span data-ttu-id="28c9e-104">Auswirkung der dpi-Kompensation</span><span class="sxs-lookup"><span data-stu-id="28c9e-104">DPI compensation effect</span></span>

<span data-ttu-id="28c9e-105">Verwenden Sie den dpi-Kompensierungs Effekt, um eine Eingabe Bitmap automatisch an den dpi-Kontext des Kontexts anzupassen.</span><span class="sxs-lookup"><span data-stu-id="28c9e-105">Use the DPI compensation effect to automatically adjust an input bitmap to match the DPI of the context.</span></span> <span data-ttu-id="28c9e-106">Dies ist nützlich für Situationen, in denen eine Bitmap auf einem anderen dpi-Wert als der Bildschirm erstellt oder geladen wird.</span><span class="sxs-lookup"><span data-stu-id="28c9e-106">This is useful for situations where a bitmap is created or loaded at a different DPI than the screen.</span></span>

<span data-ttu-id="28c9e-107">Die CLSID für diesen Effekt ist CLSID \_ D2D1DpiCompensation.</span><span class="sxs-lookup"><span data-stu-id="28c9e-107">The CLSID for this effect is CLSID\_D2D1DpiCompensation.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="28c9e-108">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="28c9e-108">Effect properties</span></span>



| <span data-ttu-id="28c9e-109">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="28c9e-109">Display name and index enumeration</span></span>                                                       | <span data-ttu-id="28c9e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28c9e-110">Description</span></span>                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c9e-111">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="28c9e-111">InterpolationMode</span></span><br/> <span data-ttu-id="28c9e-112">D2D1 \_ dpicompensation- \_ Prop- \_ Interpolations \_ Modus</span><span class="sxs-lookup"><span data-stu-id="28c9e-112">D2D1\_DPICOMPENSATION\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="28c9e-113">Der Interpolations Modus, den der Effekt zum Skalieren des Bilds verwendet.</span><span class="sxs-lookup"><span data-stu-id="28c9e-113">The interpolation mode the effect uses to scale the image.</span></span><br/> <span data-ttu-id="28c9e-114">Der Typ ist der D2D1 \_ dpicompensation- \_ Interpolations \_ Modus.</span><span class="sxs-lookup"><span data-stu-id="28c9e-114">The type is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="28c9e-115">Der Standardwert ist D2D1 \_ dpicompensation \_ Interpolations \_ Mode \_ linear.</span><span class="sxs-lookup"><span data-stu-id="28c9e-115">The default value is D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR .</span></span><br/>                  |
| <span data-ttu-id="28c9e-116">Bordermode</span><span class="sxs-lookup"><span data-stu-id="28c9e-116">BorderMode</span></span><br/> <span data-ttu-id="28c9e-117">D2D1 \_ dpicompensation-Prop-Rahmen \_ \_ \_ Modus</span><span class="sxs-lookup"><span data-stu-id="28c9e-117">D2D1\_DPICOMPENSATION\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="28c9e-118">Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart.</span><span class="sxs-lookup"><span data-stu-id="28c9e-118">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="28c9e-119">Weitere Informationen finden Sie unter [Border Modes](https://www.bing.com/search?q=Border+modes) .</span><span class="sxs-lookup"><span data-stu-id="28c9e-119">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span> <br/> <span data-ttu-id="28c9e-120">Der Typ ist "D2D1 \_ Border \_ Mode".</span><span class="sxs-lookup"><span data-stu-id="28c9e-120">The type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="28c9e-121">Der Standardwert ist D2D1 \_ Border \_ Mode \_ Soft.</span><span class="sxs-lookup"><span data-stu-id="28c9e-121">The default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/> |
| <span data-ttu-id="28c9e-122">Inputdpi</span><span class="sxs-lookup"><span data-stu-id="28c9e-122">InputDpi</span></span><br/> <span data-ttu-id="28c9e-123">D2D1 \_ dpicompensation- \_ Prop- \_ Eingabe \_ dpi</span><span class="sxs-lookup"><span data-stu-id="28c9e-123">D2D1\_DPICOMPENSATION\_PROP\_INPUT\_DPI</span></span><br/>                   | <span data-ttu-id="28c9e-124">Der dpi-Eintrag des Eingabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="28c9e-124">The DPI of the input image.</span></span><br/> <span data-ttu-id="28c9e-125">Der Typ ist "float".</span><span class="sxs-lookup"><span data-stu-id="28c9e-125">The type is FLOAT.</span></span><br/> <span data-ttu-id="28c9e-126">Der Standardwert ist 96.0 f.</span><span class="sxs-lookup"><span data-stu-id="28c9e-126">The default value is 96.0f.</span></span><br/>                                                                                                                                    |



 

## <a name="interpolation-modes"></a><span data-ttu-id="28c9e-127">Interpolations Modi</span><span class="sxs-lookup"><span data-stu-id="28c9e-127">Interpolation modes</span></span>



| <span data-ttu-id="28c9e-128">Enumeration</span><span class="sxs-lookup"><span data-stu-id="28c9e-128">Enumeration</span></span>                                                       | <span data-ttu-id="28c9e-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28c9e-129">Description</span></span>                                                                                                                                                                                          |
|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c9e-130">D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ Nächster \_ Nachbar</span><span class="sxs-lookup"><span data-stu-id="28c9e-130">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="28c9e-131">Verwendet den nächsten einzelnen Punkt und verwendet diesen.</span><span class="sxs-lookup"><span data-stu-id="28c9e-131">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="28c9e-132">Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.</span><span class="sxs-lookup"><span data-stu-id="28c9e-132">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                                                           |
| <span data-ttu-id="28c9e-133">D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ linear</span><span class="sxs-lookup"><span data-stu-id="28c9e-133">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="28c9e-134">Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung.</span><span class="sxs-lookup"><span data-stu-id="28c9e-134">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="28c9e-135">Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus.</span><span class="sxs-lookup"><span data-stu-id="28c9e-135">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span>                                           |
| <span data-ttu-id="28c9e-136">D2D1 \_ dpicompensation \_ Interpolations \_ Modus ( \_ kubisch)</span><span class="sxs-lookup"><span data-stu-id="28c9e-136">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="28c9e-137">Verwendet einen 16-beispielkubischen Kernel für Interpolationen.</span><span class="sxs-lookup"><span data-stu-id="28c9e-137">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="28c9e-138">In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="28c9e-138">This mode uses the most processing time, but outputs a higher quality image.</span></span>                                                                        |
| <span data-ttu-id="28c9e-139">D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ \_ Multisample \_ linear</span><span class="sxs-lookup"><span data-stu-id="28c9e-139">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="28c9e-140">Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="28c9e-140">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="28c9e-141">Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="28c9e-141">This mode is good for scaling down by small amounts on images with few pixels.</span></span>                                              |
| <span data-ttu-id="28c9e-142">D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="28c9e-142">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="28c9e-143">Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="28c9e-143">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                                                                     |
| <span data-ttu-id="28c9e-144">D2D1 \_ dpicompensation \_ Interpolations \_ Modus \_ High \_ Quality \_ kubisch</span><span class="sxs-lookup"><span data-stu-id="28c9e-144">D2D1\_DPICOMPENSATION\_INTERPOLATION\_MODE\_HIGH\_QUALITY\_CUBIC</span></span>  | <span data-ttu-id="28c9e-145">Verwendet einen kubischen Kernel mit hoher Qualität für eine Variable Größe, um das Abbild vorab zu skalieren, wenn eine downstreamingmatrix an der Transformationsmatrix beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="28c9e-145">Uses a variable size high quality cubic kernel to perform a pre-downscale the image if downscaling is involved in the transform matrix.</span></span> <span data-ttu-id="28c9e-146">Verwendet dann den kubischen Interpolations Modus für die endgültige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="28c9e-146">Then uses the cubic interpolation mode for the final output.</span></span> |



 

> [!Note]  
> <span data-ttu-id="28c9e-147">Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ dpicompensstion \_ Interpolations \_ Modus linear festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="28c9e-147">If you don't select a mode, the effect defaults to D2D1\_DPICOMPENSTION\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="28c9e-148">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="28c9e-148">Border modes</span></span>



| <span data-ttu-id="28c9e-149">Name</span><span class="sxs-lookup"><span data-stu-id="28c9e-149">Name</span></span>                     | <span data-ttu-id="28c9e-150">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="28c9e-150">Description</span></span>                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="28c9e-151">D2D1 \_ Border \_ Mode \_ Soft</span><span class="sxs-lookup"><span data-stu-id="28c9e-151">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="28c9e-152">Pixel außerhalb der Eingabe Grenzen werden vom [Spiegelungs Rahmen Effekt](border.md)generiert.</span><span class="sxs-lookup"><span data-stu-id="28c9e-152">Pixels outside of the input boundaries are generated by the [mirror border effect](border.md).</span></span> <br/> |
| <span data-ttu-id="28c9e-153">D2D1 \_ Rahmen \_ Modus \_ hart</span><span class="sxs-lookup"><span data-stu-id="28c9e-153">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="28c9e-154">Pixel außerhalb der Eingabe Grenzen sind transparent schwarz.</span><span class="sxs-lookup"><span data-stu-id="28c9e-154">Pixels outside of the input boundaries are transparent black.</span></span><br/>                                    |



 

## <a name="requirements"></a><span data-ttu-id="28c9e-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="28c9e-155">Requirements</span></span>



| <span data-ttu-id="28c9e-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="28c9e-156">Requirement</span></span> | <span data-ttu-id="28c9e-157">Wert</span><span class="sxs-lookup"><span data-stu-id="28c9e-157">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="28c9e-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="28c9e-158">Minimum supported client</span></span> | <span data-ttu-id="28c9e-159">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28c9e-159">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="28c9e-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="28c9e-160">Minimum supported server</span></span> | <span data-ttu-id="28c9e-161">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="28c9e-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="28c9e-162">Header</span><span class="sxs-lookup"><span data-stu-id="28c9e-162">Header</span></span>                   | <span data-ttu-id="28c9e-163">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="28c9e-163">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="28c9e-164">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="28c9e-164">Library</span></span>                  | <span data-ttu-id="28c9e-165">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="28c9e-165">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="28c9e-166">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="28c9e-166">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="28c9e-167">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="28c9e-167">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

