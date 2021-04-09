---
title: Perspektivischer 3D-Transformationseffekt
description: Verwenden Sie den 3D-perspektivischen Transformations Effekt, um das Bild in drei Dimensionen so zu drehen, als ob es aus einer Entfernung
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- 3D--Perspektiven Transformations Effekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859321"
---
# <a name="3d-perspective-transform-effect"></a><span data-ttu-id="7b832-104">Perspektivischer 3D-Transformationseffekt</span><span class="sxs-lookup"><span data-stu-id="7b832-104">3D perspective transform effect</span></span>

<span data-ttu-id="7b832-105">Verwenden Sie den 3D-perspektivischen Transformations Effekt, um das Bild in drei Dimensionen so zu drehen, als ob es aus einer Entfernung</span><span class="sxs-lookup"><span data-stu-id="7b832-105">Use the 3D perspective transform effect to rotate the image in 3 dimensions as if viewed from a distance.</span></span>

<span data-ttu-id="7b832-106">Die 3D-perspektivische Transformation ist einfacher als der 3D-Transformations Effekt, macht aber nur eine Teilmenge der Funktionalität verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7b832-106">The 3D perspective transform is more convenient than the 3D transform effect, but only exposes a subset of the functionality.</span></span> <span data-ttu-id="7b832-107">Sie können eine vollständige 3D-Transformationsmatrix berechnen und mithilfe des [3D-](3d-transform.md) Transformations Effekts eine willkürlichere Transformationsmatrix auf ein Bild anwenden.</span><span class="sxs-lookup"><span data-stu-id="7b832-107">You can compute a full 3D transformation matrix and apply a more arbitrary transform matrix to an image using the [3D transform](3d-transform.md) effect.</span></span>

<span data-ttu-id="7b832-108">Die CLSID für diesen Effekt ist CLSID \_ D2D13DPerspectiveTransform.</span><span class="sxs-lookup"><span data-stu-id="7b832-108">The CLSID for this effect is CLSID\_D2D13DPerspectiveTransform.</span></span>

-   [<span data-ttu-id="7b832-109">Beispiel Bild</span><span class="sxs-lookup"><span data-stu-id="7b832-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="7b832-110">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b832-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="7b832-111">Interpolations Modi</span><span class="sxs-lookup"><span data-stu-id="7b832-111">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="7b832-112">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="7b832-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="7b832-113">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="7b832-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="7b832-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b832-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="7b832-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b832-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="7b832-116">Beispielbild</span><span class="sxs-lookup"><span data-stu-id="7b832-116">Example image</span></span>



| <span data-ttu-id="7b832-117">Vorher</span><span class="sxs-lookup"><span data-stu-id="7b832-117">Before</span></span>                                                               |
|----------------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)           |
| <span data-ttu-id="7b832-119">Nach</span><span class="sxs-lookup"><span data-stu-id="7b832-119">After</span></span>                                                                |
| ![das Bild nach dem Effekt.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="7b832-121">Effekt Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="7b832-121">Effect properties</span></span>



| <span data-ttu-id="7b832-122">Anzeige Name und indexenumeration</span><span class="sxs-lookup"><span data-stu-id="7b832-122">Display name and index enumeration</span></span>                                                              | <span data-ttu-id="7b832-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b832-123">Description</span></span>                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b832-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="7b832-124">InterpolationMode</span></span><br/> <span data-ttu-id="7b832-125">D2D1 \_ 3dperspectivetransform- \_ Prop- \_ Interpolations \_ Modus</span><span class="sxs-lookup"><span data-stu-id="7b832-125">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="7b832-126">Der Interpolations Modus, den der Effekt für das Bild verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b832-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="7b832-127">Es gibt fünf Skalierungs Modi, die die Qualität und Geschwindigkeit unterliegen.</span><span class="sxs-lookup"><span data-stu-id="7b832-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="7b832-128">Type ist der D2D1 \_ 3dperspectivetransform \_ Interpolations \_ Modus.</span><span class="sxs-lookup"><span data-stu-id="7b832-128">Type is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="7b832-129">Der Standardwert ist der D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus \_ linear.</span><span class="sxs-lookup"><span data-stu-id="7b832-129">Default value is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span><br/>              |
| <span data-ttu-id="7b832-130">Bordermode</span><span class="sxs-lookup"><span data-stu-id="7b832-130">BorderMode</span></span><br/> <span data-ttu-id="7b832-131">D2D1 \_ 3dperspectivetransform-Rahmen \_ \_ \_ Modus</span><span class="sxs-lookup"><span data-stu-id="7b832-131">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="7b832-132">Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart.</span><span class="sxs-lookup"><span data-stu-id="7b832-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="7b832-133">Weitere Informationen finden Sie unter [Border Modes](https://www.bing.com/search?q=Border+modes) .</span><span class="sxs-lookup"><span data-stu-id="7b832-133">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span><br/> <span data-ttu-id="7b832-134">Typ: D2D1 \_ Border \_ Mode</span><span class="sxs-lookup"><span data-stu-id="7b832-134">Type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="7b832-135">Der Standardwert ist D2D1 \_ Border \_ Mode \_ Soft.</span><span class="sxs-lookup"><span data-stu-id="7b832-135">Default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                              |
| <span data-ttu-id="7b832-136">Tiefe</span><span class="sxs-lookup"><span data-stu-id="7b832-136">Depth</span></span><br/> <span data-ttu-id="7b832-137">D2D1 \_ 3dperspectivetransform- \_ Prop- \_ Tiefe</span><span class="sxs-lookup"><span data-stu-id="7b832-137">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_DEPTH</span></span><br/>                           | <span data-ttu-id="7b832-138">Der Abstand zwischen *perspectiveorigin* und Projektionsebene.</span><span class="sxs-lookup"><span data-stu-id="7b832-138">The distance from the *PerspectiveOrigin* to the projection plane.</span></span> <span data-ttu-id="7b832-139">Der in Dips angegebene Wert muss größer als 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="7b832-139">The value specified in DIPs and must be greater than 0.</span></span><br/> <span data-ttu-id="7b832-140">Der Typ ist "float".</span><span class="sxs-lookup"><span data-stu-id="7b832-140">Type is FLOAT.</span></span><br/> <span data-ttu-id="7b832-141">Der Standardwert ist 1000.0 f.</span><span class="sxs-lookup"><span data-stu-id="7b832-141">Default value is 1000.0f.</span></span><br/>                                                                                               |
| <span data-ttu-id="7b832-142">Perspectiveorigin</span><span class="sxs-lookup"><span data-stu-id="7b832-142">PerspectiveOrigin</span></span><br/> <span data-ttu-id="7b832-143">D2D1 \_ 3dperspectivetransform \_ Prop \_ Perspective- \_ Ursprung</span><span class="sxs-lookup"><span data-stu-id="7b832-143">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_PERSPECTIVE\_ORIGIN</span></span><br/> | <span data-ttu-id="7b832-144">Der X-und Y-Speicherort des Viewers in der 3D-Szene.</span><span class="sxs-lookup"><span data-stu-id="7b832-144">The X and Y location of the viewer in the 3D scene.</span></span> <span data-ttu-id="7b832-145">Diese Eigenschaft ist ein D2D1 \_ Vector \_ 2F, definiert als: (Punkt X, Punkt Y).</span><span class="sxs-lookup"><span data-stu-id="7b832-145">This property is a D2D1\_VECTOR\_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="7b832-146">Die Einheiten befinden sich in Dips.</span><span class="sxs-lookup"><span data-stu-id="7b832-146">The units are in DIPs.</span></span><br/> <span data-ttu-id="7b832-147">Sie legen den Z-Wert mit der Eigenschaft *Tiefe* fest.</span><span class="sxs-lookup"><span data-stu-id="7b832-147">You set the Z value with the *Depth* property.</span></span><br/> <span data-ttu-id="7b832-148">Typ: D2D1 \_ Vector \_ 2F</span><span class="sxs-lookup"><span data-stu-id="7b832-148">Type is D2D1\_VECTOR\_2F.</span></span><br/> <span data-ttu-id="7b832-149">Der Standardwert ist {0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="7b832-149">Default value is {0.0f, 0.0f}.</span></span><br/> |
| <span data-ttu-id="7b832-150">Localoffset</span><span class="sxs-lookup"><span data-stu-id="7b832-150">LocalOffset</span></span><br/> <span data-ttu-id="7b832-151">D2D1 \_ 3dperspectivetransform- \_ Prop ( \_ lokaler \_ Offset)</span><span class="sxs-lookup"><span data-stu-id="7b832-151">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_LOCAL\_OFFSET</span></span><br/>             | <span data-ttu-id="7b832-152">Eine Übersetzung, die den Effekt ausführt, bevor die Projektionsebene gedreht wird.</span><span class="sxs-lookup"><span data-stu-id="7b832-152">A translation the effect performs before it rotates the projection plane.</span></span> <span data-ttu-id="7b832-153">Diese Eigenschaft ist ein D2D1 \_ Vector \_ 3F, definiert als: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="7b832-153">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="7b832-154">Die Einheiten befinden sich in Dips.</span><span class="sxs-lookup"><span data-stu-id="7b832-154">The units are in DIPs.</span></span><br/> <span data-ttu-id="7b832-155">Type ist D2D1 \_ Vector \_ 3f.</span><span class="sxs-lookup"><span data-stu-id="7b832-155">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="7b832-156">Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="7b832-156">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                        |
| <span data-ttu-id="7b832-157">Globaloffset</span><span class="sxs-lookup"><span data-stu-id="7b832-157">GlobalOffset</span></span><br/> <span data-ttu-id="7b832-158">D2D1 \_ 3dperspectivetransform \_ - \_ globaler \_ Offset</span><span class="sxs-lookup"><span data-stu-id="7b832-158">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_GLOBAL\_OFFSET</span></span><br/>           | <span data-ttu-id="7b832-159">Eine Übersetzung, die den Effekt nach dem Drehen der Projektionsebene ausführt.</span><span class="sxs-lookup"><span data-stu-id="7b832-159">A translation the effect performs after it rotates the projection plane.</span></span> <span data-ttu-id="7b832-160">Diese Eigenschaft ist ein D2D1 \_ Vector \_ 3F, definiert als: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="7b832-160">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="7b832-161">Die Einheiten befinden sich in Dips.</span><span class="sxs-lookup"><span data-stu-id="7b832-161">The units are in DIPs.</span></span><br/> <span data-ttu-id="7b832-162">Type ist D2D1 \_ Vector \_ 3f.</span><span class="sxs-lookup"><span data-stu-id="7b832-162">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="7b832-163">Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="7b832-163">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                         |
| <span data-ttu-id="7b832-164">Rotationorigin</span><span class="sxs-lookup"><span data-stu-id="7b832-164">RotationOrigin</span></span><br/> <span data-ttu-id="7b832-165">D2D1 \_ 3dperspectivetransform- \_ Prop- \_ Rotation- \_ Ursprung</span><span class="sxs-lookup"><span data-stu-id="7b832-165">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION\_ORIGIN</span></span><br/>       | <span data-ttu-id="7b832-166">Der Mittelpunkt der Drehung, die der Effekt ausführt.</span><span class="sxs-lookup"><span data-stu-id="7b832-166">The center point of the rotation the effect performs.</span></span> <span data-ttu-id="7b832-167">Diese Eigenschaft ist ein D2D1 \_ Vector \_ 3F, definiert als: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="7b832-167">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="7b832-168">Die Einheiten befinden sich in Dips.</span><span class="sxs-lookup"><span data-stu-id="7b832-168">The units are in DIPs.</span></span><br/> <span data-ttu-id="7b832-169">Type ist D2D1 \_ Vector \_ 3f.</span><span class="sxs-lookup"><span data-stu-id="7b832-169">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="7b832-170">Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="7b832-170">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                            |
| <span data-ttu-id="7b832-171">Drehung</span><span class="sxs-lookup"><span data-stu-id="7b832-171">Rotation</span></span><br/> <span data-ttu-id="7b832-172">D2D1 \_ 3dperspectivetransform- \_ Prop- \_ Drehung</span><span class="sxs-lookup"><span data-stu-id="7b832-172">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION</span></span><br/>                     | <span data-ttu-id="7b832-173">Die Winkel der Drehung für jede Achse.</span><span class="sxs-lookup"><span data-stu-id="7b832-173">The angles of rotation for each axis.</span></span> <span data-ttu-id="7b832-174">Diese Eigenschaft ist ein D2D1 \_ Vector \_ 3F, definiert als: (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="7b832-174">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="7b832-175">Die Einheiten liegen in Grad.</span><span class="sxs-lookup"><span data-stu-id="7b832-175">The units are in degrees.</span></span><br/> <span data-ttu-id="7b832-176">Type ist D2D1 \_ Vector \_ 3f.</span><span class="sxs-lookup"><span data-stu-id="7b832-176">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="7b832-177">Der Standardwert ist {0,0 f, 0,0 f, 0,0 f}.</span><span class="sxs-lookup"><span data-stu-id="7b832-177">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="7b832-178">Interpolations Modi</span><span class="sxs-lookup"><span data-stu-id="7b832-178">Interpolation modes</span></span>



| <span data-ttu-id="7b832-179">Enumeration</span><span class="sxs-lookup"><span data-stu-id="7b832-179">Enumeration</span></span>                                                              | <span data-ttu-id="7b832-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b832-180">Description</span></span>                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b832-181">D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus \_ Nächster \_ Nachbar</span><span class="sxs-lookup"><span data-stu-id="7b832-181">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="7b832-182">Verwendet den nächsten einzelnen Punkt und verwendet diesen.</span><span class="sxs-lookup"><span data-stu-id="7b832-182">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="7b832-183">Dieser Modus verwendet weniger Verarbeitungszeit, gibt jedoch das niedrigste Qualitätsbild aus.</span><span class="sxs-lookup"><span data-stu-id="7b832-183">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="7b832-184">D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus \_ linear</span><span class="sxs-lookup"><span data-stu-id="7b832-184">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="7b832-185">Verwendet ein vier-Punkt-Beispiel und eine lineare interpolung.</span><span class="sxs-lookup"><span data-stu-id="7b832-185">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="7b832-186">Dieser Modus verwendet mehr Verarbeitungszeit als der nächstgelegene Nachbar Modus, gibt aber ein Image mit höherer Qualität aus.</span><span class="sxs-lookup"><span data-stu-id="7b832-186">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="7b832-187">D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus ( \_ kubisch)</span><span class="sxs-lookup"><span data-stu-id="7b832-187">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="7b832-188">Verwendet einen 16-beispielkubischen Kernel für Interpolationen.</span><span class="sxs-lookup"><span data-stu-id="7b832-188">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="7b832-189">In diesem Modus wird die meiste Verarbeitungszeit verwendet, es wird jedoch ein Image mit höherer Qualität ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="7b832-189">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="7b832-190">D2D1 \_ 3dperspectivetransform \_ Interpolations \_ Modus \_ \_ Multisample \_ linear</span><span class="sxs-lookup"><span data-stu-id="7b832-190">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="7b832-191">Verwendet vier lineare Stichproben innerhalb eines einzelnen Pixels für eine gute Edge-Antialiasing.</span><span class="sxs-lookup"><span data-stu-id="7b832-191">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="7b832-192">Dieser Modus eignet sich gut zum horizontalen Herunterskalieren um kleine Beträge in Bildern mit wenigen Pixeln.</span><span class="sxs-lookup"><span data-stu-id="7b832-192">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="7b832-193">D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="7b832-193">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="7b832-194">Verwendet anisotrope Filterung, um ein Muster entsprechend der transformierten Form der Bitmap zu modellieren.</span><span class="sxs-lookup"><span data-stu-id="7b832-194">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="7b832-195">Wenn Sie keinen Modus auswählen, wird der Effekt standardmäßig auf den D2D1 \_ 3dperspectivetransform- \_ Interpolations \_ Modus linear festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="7b832-195">If you don't select a mode, the effect defaults to D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="7b832-196">Der anisotrope-Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für diesen Effekt eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.</span><span class="sxs-lookup"><span data-stu-id="7b832-196">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="7b832-197">Rahmen Modi</span><span class="sxs-lookup"><span data-stu-id="7b832-197">Border modes</span></span>



| <span data-ttu-id="7b832-198">Name</span><span class="sxs-lookup"><span data-stu-id="7b832-198">Name</span></span>                     | <span data-ttu-id="7b832-199">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7b832-199">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b832-200">D2D1 \_ Border \_ Mode \_ Soft</span><span class="sxs-lookup"><span data-stu-id="7b832-200">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="7b832-201">Der Effekt füllt das Bild mit transparenten schwarzen Pixeln, während es interpoliert, was zu einem weichen Rand führt.</span><span class="sxs-lookup"><span data-stu-id="7b832-201">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="7b832-202">D2D1 \_ Rahmen \_ Modus \_ hart</span><span class="sxs-lookup"><span data-stu-id="7b832-202">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="7b832-203">Der Effekt bindet die Ausgabe an die Größe des Eingabe Bilds.</span><span class="sxs-lookup"><span data-stu-id="7b832-203">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="output-bitmap"></a><span data-ttu-id="7b832-204">Ausgabe Bitmap</span><span class="sxs-lookup"><span data-stu-id="7b832-204">Output bitmap</span></span>

<span data-ttu-id="7b832-205">Die Größe der Ausgabe Bitmap hängt von der Transformationsmatrix ab, die auf das Bild angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b832-205">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="7b832-206">Der Effekt führt den Transformations Vorgang aus und wendet dann ein Begrenzungs Rahmen um das Ergebnis an.</span><span class="sxs-lookup"><span data-stu-id="7b832-206">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="7b832-207">Die Ausgabe Bitmap ist die Größe des umgebenden Felds.</span><span class="sxs-lookup"><span data-stu-id="7b832-207">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="7b832-208">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7b832-208">Requirements</span></span>



| <span data-ttu-id="7b832-209">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7b832-209">Requirement</span></span> | <span data-ttu-id="7b832-210">Wert</span><span class="sxs-lookup"><span data-stu-id="7b832-210">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7b832-211">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7b832-211">Minimum supported client</span></span> | <span data-ttu-id="7b832-212">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b832-212">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7b832-213">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7b832-213">Minimum supported server</span></span> | <span data-ttu-id="7b832-214">Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7b832-214">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="7b832-215">Header</span><span class="sxs-lookup"><span data-stu-id="7b832-215">Header</span></span>                   | <span data-ttu-id="7b832-216">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="7b832-216">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="7b832-217">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7b832-217">Library</span></span>                  | <span data-ttu-id="7b832-218">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="7b832-218">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="7b832-219">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7b832-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b832-220">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="7b832-220">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

