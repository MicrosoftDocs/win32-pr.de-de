---
title: Farbmatrix Effekt
description: Verwenden Sie den Farbmatrix Effekt, um die RGBA-Werte einer Bitmap zu ändern.
ms.assetid: 093EEEF1-8C38-414E-8261-58A6C3DD930D
keywords:
- Farbmatrix Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1078b1858bc68396546e1036c717e01acb1069c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040484"
---
# <a name="color-matrix-effect"></a><span data-ttu-id="8e187-104">Farbmatrix Effekt</span><span class="sxs-lookup"><span data-stu-id="8e187-104">Color matrix effect</span></span>

<span data-ttu-id="8e187-105">Verwenden Sie den Farbmatrix Effekt, um die RGBA-Werte einer Bitmap zu ändern.</span><span class="sxs-lookup"><span data-stu-id="8e187-105">Use the color matrix effect to alter the RGBA values of a bitmap.</span></span>

<span data-ttu-id="8e187-106">Sie können diesen Effekt für Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="8e187-106">You can use this effect to:</span></span>

-   <span data-ttu-id="8e187-107">Entfernen eines Farbkanals aus einem Bild.</span><span class="sxs-lookup"><span data-stu-id="8e187-107">Remove a color channel from an image.</span></span>
-   <span data-ttu-id="8e187-108">Reduzieren Sie die Farbe in einem Bild.</span><span class="sxs-lookup"><span data-stu-id="8e187-108">Reduce the color in an image.</span></span>
-   <span data-ttu-id="8e187-109">Farbkanäle austauschen.</span><span class="sxs-lookup"><span data-stu-id="8e187-109">Swap color channels.</span></span>
-   <span data-ttu-id="8e187-110">Farbkanäle kombinieren.</span><span class="sxs-lookup"><span data-stu-id="8e187-110">Combine color channels.</span></span>

<span data-ttu-id="8e187-111">Viele integrierte Effekte sind Spezialisierungs Farben von Farb Matrizen, die für die beabsichtigte Verwendung der Effekte optimiert sind.</span><span class="sxs-lookup"><span data-stu-id="8e187-111">Many built-in effects are specializations of color matrix that are optimized for the intended use of the effects.</span></span> <span data-ttu-id="8e187-112">Beispiele hierfür sind [Sättigung](saturation.md), [Farbton Drehung](hue-rotate.md),- [Pia](sepia-effect.md)und [Temperatur und Tönungs](temperature-and-tint-effect.md).</span><span class="sxs-lookup"><span data-stu-id="8e187-112">Examples include [saturation](saturation.md), [hue rotate](hue-rotate.md), [sepia](sepia-effect.md), and [temperature and tint](temperature-and-tint-effect.md).</span></span>

<span data-ttu-id="8e187-113">Die CLSID für diesen Effekt ist CLSID \_ D2D1ColorMatrix.</span><span class="sxs-lookup"><span data-stu-id="8e187-113">The CLSID for this effect is CLSID\_D2D1ColorMatrix.</span></span>

-   [<span data-ttu-id="8e187-114">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="8e187-114">Example image</span></span>](#example-image)
-   [<span data-ttu-id="8e187-115">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e187-115">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="8e187-116">Alpha-Modi</span><span class="sxs-lookup"><span data-stu-id="8e187-116">Alpha modes</span></span>](#alpha-modes)
-   [<span data-ttu-id="8e187-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e187-117">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="8e187-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e187-118">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="8e187-119">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="8e187-119">Example image</span></span>

<span data-ttu-id="8e187-120">Das Beispiel zeigt die Eingabe-und Ausgabe Bilder des Farbmatrix Effekts, der die roten und blauen Kanäle vertauscht.</span><span class="sxs-lookup"><span data-stu-id="8e187-120">The example here shows the input and output images of the color matrix effect that swaps the red and blue channels.</span></span>



| <span data-ttu-id="8e187-121">Vorher</span><span class="sxs-lookup"><span data-stu-id="8e187-121">Before</span></span>                                                       |
|--------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)   |
| <span data-ttu-id="8e187-123">Nach</span><span class="sxs-lookup"><span data-stu-id="8e187-123">After</span></span>                                                        |
| ![das Bild nach der Transformation.](images/15-colormatrix.png) |



 


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect);

colorMatrixEffect->SetInput(0, bitmap);
D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="8e187-125">Dieser Effekt multipliziert die RGBA-Werte des Bilds mit einer 5 x 4-Spalten hauptmatrix, wie in dieser Gleichung gezeigt.</span><span class="sxs-lookup"><span data-stu-id="8e187-125">This effect multiplies the RGBA values of the image by a 5x4, column major matrix as shown in this equation.</span></span>

![eine Beispiel Matrix Definition.](images/color-matrix-formula.png)

<span data-ttu-id="8e187-127">Dieser Effekt kann bei geraden und vorab multiplizierten Alpha Bildern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8e187-127">This effect works on straight and premultiplied alpha images.</span></span>

## <a name="effect-properties"></a><span data-ttu-id="8e187-128">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="8e187-128">Effect properties</span></span>



| <span data-ttu-id="8e187-129">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="8e187-129">Display name and index enumeration</span></span>                                       | <span data-ttu-id="8e187-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e187-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e187-131">ColorMatrix</span><span class="sxs-lookup"><span data-stu-id="8e187-131">ColorMatrix</span></span><br/> <span data-ttu-id="8e187-132">D2D1 \_ ColorMatrix \_ - \_ Farb \_ Matrix</span><span class="sxs-lookup"><span data-stu-id="8e187-132">D2D1\_COLORMATRIX\_PROP\_COLOR\_MATRIX</span></span><br/> | <span data-ttu-id="8e187-133">Eine 5X4-Matrix von float-Werten.</span><span class="sxs-lookup"><span data-stu-id="8e187-133">A 5x4 matrix of float values.</span></span> <span data-ttu-id="8e187-134">Die Elemente in der Matrix sind nicht gebunden und sind unitless.</span><span class="sxs-lookup"><span data-stu-id="8e187-134">The elements in the matrix are not bounded and are unitless.</span></span><br/> <span data-ttu-id="8e187-135">Der Standardwert ist die Identitätsmatrix.</span><span class="sxs-lookup"><span data-stu-id="8e187-135">The default is the identity matrix.</span></span><br/> <span data-ttu-id="8e187-136">Der Typ ist D2D1 \_ Matrix \_ 5X4 \_ F.</span><span class="sxs-lookup"><span data-stu-id="8e187-136">The type is D2D1\_MATRIX\_5X4\_F.</span></span><br/> <span data-ttu-id="8e187-137">Der Standardwert ist Matrix5x4F (1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 0, 0, 0, 0, 0).</span><span class="sxs-lookup"><span data-stu-id="8e187-137">The default value is Matrix5x4F(1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0, 1, 0, 0, 0, 0).</span></span> <br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="8e187-138">Alpha AMODE</span><span class="sxs-lookup"><span data-stu-id="8e187-138">AlphaMode</span></span><br/> <span data-ttu-id="8e187-139">D2D1 \_ ColorMatrix- \_ Prop- \_ alpha- \_ Modus</span><span class="sxs-lookup"><span data-stu-id="8e187-139">D2D1\_COLORMATRIX\_PROP\_ALPHA\_MODE</span></span><br/>     | <span data-ttu-id="8e187-140">Der Alpha-Modus der Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="8e187-140">The alpha mode of the output.</span></span> <span data-ttu-id="8e187-141">Weitere Informationen finden Sie unter [Alpha-Modi](#alpha-modes) .</span><span class="sxs-lookup"><span data-stu-id="8e187-141">See [Alpha modes](#alpha-modes) for more info.</span></span> <br/> <span data-ttu-id="8e187-142">Der Typ ist der D2D1 \_ ColorMatrix \_ alpha- \_ Modus.</span><span class="sxs-lookup"><span data-stu-id="8e187-142">The type is D2D1\_COLORMATRIX\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="8e187-143">Der Standardwert ist "D2D1 \_ ColorMatrix \_ Alpha Mode" ( \_ \_ vorab multipliziert).</span><span class="sxs-lookup"><span data-stu-id="8e187-143">The default value is D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/>                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="8e187-144">Klamme Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8e187-144">ClampOutput</span></span><br/> <span data-ttu-id="8e187-145">D2D1 \_ ColorMatrix- \_ Prop- \_ Klemm \_ Ausgabe</span><span class="sxs-lookup"><span data-stu-id="8e187-145">D2D1\_COLORMATRIX\_PROP\_CLAMP\_OUTPUT</span></span><br/> | <span data-ttu-id="8e187-146">Gibt an, ob der Effekt Farbwerte auf zwischen 0 und 1 zeigt, bevor der Effekt die Werte an den nächsten Effekt im Diagramm übergibt.</span><span class="sxs-lookup"><span data-stu-id="8e187-146">Whether the effect clamps color values to between 0 and 1 before the effect passes the values to the next effect in the graph.</span></span> <span data-ttu-id="8e187-147">Der Effekt bindet die Werte, bevor die Alpha-angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="8e187-147">The effect clamps the values before it premultiplies the alpha .</span></span><br/> <span data-ttu-id="8e187-148">Wenn Sie diese Einstellung auf "true" festlegen, werden die Werte durch die Auswirkung fixiert.</span><span class="sxs-lookup"><span data-stu-id="8e187-148">If you set this to TRUE the effect will clamp the values.</span></span> <span data-ttu-id="8e187-149">Wenn Sie diese Einstellung auf "false" festlegen, werden die Farbwerte durch die Auswirkung nicht fixiert, aber andere Effekte und die Ausgabe Oberfläche können die Werte einspannen, wenn Sie nicht über eine hohe Genauigkeit verfügen.</span><span class="sxs-lookup"><span data-stu-id="8e187-149">If you set this to FALSE, the effect will not clamp the color values, but other effects and the output surface may clamp the values if they are not of high enough precision.</span></span><br/> <span data-ttu-id="8e187-150">Der Typ ist "bool".</span><span class="sxs-lookup"><span data-stu-id="8e187-150">The type is BOOL.</span></span><br/> <span data-ttu-id="8e187-151">Der Standardwert ist FALSE.</span><span class="sxs-lookup"><span data-stu-id="8e187-151">The default value is FALSE.</span></span><br/> |



 

## <a name="alpha-modes"></a><span data-ttu-id="8e187-152">Alpha-Modi</span><span class="sxs-lookup"><span data-stu-id="8e187-152">Alpha modes</span></span>



| <span data-ttu-id="8e187-153">Name</span><span class="sxs-lookup"><span data-stu-id="8e187-153">Name</span></span>                                          | <span data-ttu-id="8e187-154">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e187-154">Description</span></span>                                                                                               |
|-----------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e187-155">D2D1 \_ ColorMatrix- \_ alpha \_ Modus ist \_ vorab multipliziert</span><span class="sxs-lookup"><span data-stu-id="8e187-155">D2D1\_COLORMATRIX\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="8e187-156">Der Effekt bewirkt, dass die Eingabe nicht vorab multipliziert wird, wendet die Farbmatrix an und führt die Ausgabe vorab aus.</span><span class="sxs-lookup"><span data-stu-id="8e187-156">The effect un-premultiplies the input, applies the color matrix, and premultiplies the output.</span></span><br/> |
| <span data-ttu-id="8e187-157">D2D1 \_ ColorMatrix- \_ alpha \_ Modus \_ direkt</span><span class="sxs-lookup"><span data-stu-id="8e187-157">D2D1\_COLORMATRIX\_ALPHA\_MODE\_STRAIGHT</span></span>      | <span data-ttu-id="8e187-158">Der Effekt wendet die Farbmatrix direkt auf die Eingabe an und führt keine vorab Multiplikation der Ausgabe aus.</span><span class="sxs-lookup"><span data-stu-id="8e187-158">The effect applies the color matrix directly to the input, and doesn't premultiply the output.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="8e187-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e187-159">Requirements</span></span>



| <span data-ttu-id="8e187-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e187-160">Requirement</span></span> | <span data-ttu-id="8e187-161">Wert</span><span class="sxs-lookup"><span data-stu-id="8e187-161">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e187-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e187-162">Minimum supported client</span></span> | <span data-ttu-id="8e187-163">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e187-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8e187-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e187-164">Minimum supported server</span></span> | <span data-ttu-id="8e187-165">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e187-165">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="8e187-166">Header</span><span class="sxs-lookup"><span data-stu-id="8e187-166">Header</span></span>                   | <span data-ttu-id="8e187-167">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="8e187-167">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="8e187-168">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8e187-168">Library</span></span>                  | <span data-ttu-id="8e187-169">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="8e187-169">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="8e187-170">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8e187-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8e187-171">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="8e187-171">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

