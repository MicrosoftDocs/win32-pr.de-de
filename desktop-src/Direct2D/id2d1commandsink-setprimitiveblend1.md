---
title: ID2D1CommandSink1 SetPrimitiveBlend1-Methode
description: Legt einen neuen primitiven Blend-Modus fest.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- SetPrimitiveBlend1-Methode Direct2D
- SetPrimitiveBlend1-Methode Direct2D, ID2D1CommandSink1-Schnittstelle
- ID2D1CommandSink1 Interface Direct2D, SetPrimitiveBlend1-Methode
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103546"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a><span data-ttu-id="4bfdc-106">ID2D1CommandSink1:: SetPrimitiveBlend1-Methode</span><span class="sxs-lookup"><span data-stu-id="4bfdc-106">ID2D1CommandSink1::SetPrimitiveBlend1 method</span></span>

<span data-ttu-id="4bfdc-107">Legt einen neuen primitiven Blend-Modus fest.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-107">Sets a new primitive blend mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bfdc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bfdc-108">Syntax</span></span>


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a><span data-ttu-id="4bfdc-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bfdc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bfdc-110">*primitiveblend*</span><span class="sxs-lookup"><span data-stu-id="4bfdc-110">*primitiveBlend*</span></span> 
</dt> <dd>

<span data-ttu-id="4bfdc-111">Type: **[ **D2D1 \_ primitive \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span><span class="sxs-lookup"><span data-stu-id="4bfdc-111">Type: **[**D2D1\_PRIMITIVE\_BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**</span></span>

<span data-ttu-id="4bfdc-112">Die primitive Mischung, die auf nachfolgende primitive angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-112">The primitive blend that will apply to subsequent primitives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bfdc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bfdc-113">Return value</span></span>

<span data-ttu-id="4bfdc-114">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4bfdc-114">Type: **HRESULT**</span></span>

<span data-ttu-id="4bfdc-115">Wenn die Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-115">If the method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="4bfdc-116">Wenn ein Fehler auftritt, wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-116">If it fails, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bfdc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4bfdc-117">Remarks</span></span>

### <a name="blend-modes"></a><span data-ttu-id="4bfdc-118">Füllmethoden</span><span class="sxs-lookup"><span data-stu-id="4bfdc-118">Blend modes</span></span>

<span data-ttu-id="4bfdc-119">Für das Rendern von Aliasing (mit Ausnahme des Min-Modus) wird der Ausgabewert O durch die lineare Interpolation der Werte *Blend (S, D)* mit dem Ziel Pixel Wert berechnet. Dies basiert auf dem Betrag, um den der primitive das Zielpixel abdeckt.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-119">For aliased rendering (except for MIN mode), the output value O is computed by linearly interpolating the value *blend(S, D)* with the destination pixel value, based on the amount that the primitive covers the destination pixel.</span></span>

<span data-ttu-id="4bfdc-120">In der hier aufgeführten Tabelle werden die primitiven Blend-Modi für die Mischung aus Alias und Antialiasing angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-120">The table here shows the primitive blend modes for both aliased and antialiased blending.</span></span> <span data-ttu-id="4bfdc-121">Die in der Tabelle aufgeführten Gleichungen verwenden die folgenden Elemente:</span><span class="sxs-lookup"><span data-stu-id="4bfdc-121">The equations listed in the table use these elements:</span></span>

-   <span data-ttu-id="4bfdc-122">O = Ausgabe</span><span class="sxs-lookup"><span data-stu-id="4bfdc-122">O = Output</span></span>
-   <span data-ttu-id="4bfdc-123">S = Quelle</span><span class="sxs-lookup"><span data-stu-id="4bfdc-123">S = Source</span></span>
-   <span data-ttu-id="4bfdc-124">Sa = quellalpha</span><span class="sxs-lookup"><span data-stu-id="4bfdc-124">SA = Source Alpha</span></span>
-   <span data-ttu-id="4bfdc-125">D = Ziel</span><span class="sxs-lookup"><span data-stu-id="4bfdc-125">D = Destination</span></span>
-   <span data-ttu-id="4bfdc-126">Da = zielalpha</span><span class="sxs-lookup"><span data-stu-id="4bfdc-126">DA = Destination Alpha</span></span>
-   <span data-ttu-id="4bfdc-127">C = Pixel Abdeckung</span><span class="sxs-lookup"><span data-stu-id="4bfdc-127">C = Pixel coverage</span></span>



| <span data-ttu-id="4bfdc-128">Primitiver Blend-Modus</span><span class="sxs-lookup"><span data-stu-id="4bfdc-128">Primitive blend mode</span></span>                 | <span data-ttu-id="4bfdc-129">Vermischung mit Alias</span><span class="sxs-lookup"><span data-stu-id="4bfdc-129">Aliased blending</span></span>                            | <span data-ttu-id="4bfdc-130">Vermischung mit Antialiasing</span><span class="sxs-lookup"><span data-stu-id="4bfdc-130">Antialiased blending</span></span>            | <span data-ttu-id="4bfdc-131">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4bfdc-131">Description</span></span>                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfdc-132">D2D1 \_ primitive \_ Blend- \_ Quelle \_ über</span><span class="sxs-lookup"><span data-stu-id="4bfdc-132">D2D1\_PRIMITIVE\_BLEND\_SOURCE\_OVER</span></span> | <span data-ttu-id="4bfdc-133">O = (S + (1 SA) \* D) \* C + D \* (1 C)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-133">O = (S + (1   SA) \* D) \* C + D \* (1   C)</span></span> | <span data-ttu-id="4bfdc-134">O = S \* c + D \* (1 SA \* c)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-134">O = S \* C + D \*(1   SA \*C)</span></span>   | <span data-ttu-id="4bfdc-135">Der standardmäßige Quellen-über-Ziel-Blend-Modus.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-135">The standard source-over-destination blend mode.</span></span>                                                                         |
| <span data-ttu-id="4bfdc-136">D2D1 \_ primitive \_ Blend- \_ Kopie kopieren</span><span class="sxs-lookup"><span data-stu-id="4bfdc-136">D2D1\_PRIMITIVE\_BLEND\_COPY</span></span>         | <span data-ttu-id="4bfdc-137">O = S \* c + D \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-137">O = S \* C + D \* (1   C)</span></span>                   | <span data-ttu-id="4bfdc-138">O = S \* c + D \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-138">O = S \* C + D \* (1   C)</span></span>       | <span data-ttu-id="4bfdc-139">Die Quelle wird in das Ziel kopiert. die Ziel Pixel werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-139">The source is copied to the destination; the destination pixels are ignored.</span></span>                                             |
| <span data-ttu-id="4bfdc-140">D2D1 \_ primitive \_ Blend \_ Min.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-140">D2D1\_PRIMITIVE\_BLEND\_MIN</span></span>          | <span data-ttu-id="4bfdc-141">O = min (S + 1-SA, D)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-141">O = Min(S + 1-SA, D)</span></span>                        | <span data-ttu-id="4bfdc-142">O = min (S \* c + 1 SA \* , D)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-142">O = Min(S \* C + 1   SA \*C, D)</span></span> | <span data-ttu-id="4bfdc-143">Die resultierenden Pixelwerte verwenden den minimalen Wert der Quell-und Ziel Pixelwerte.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-143">The resulting pixel values use the minimum of the source and destination pixel values.</span></span> <span data-ttu-id="4bfdc-144">Verfügbar in Windows 8 und höher.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-144">Available in Windows 8 and later.</span></span> |
| <span data-ttu-id="4bfdc-145">D2D1 \_ primitive \_ Blend- \_ Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="4bfdc-145">D2D1\_PRIMITIVE\_BLEND\_ADD</span></span>          | <span data-ttu-id="4bfdc-146">O = (S + d) \* C + d \* (1 c)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-146">O = (S + D) \* C + D \* (1   C)</span></span>             | <span data-ttu-id="4bfdc-147">O = S \* C + D</span><span class="sxs-lookup"><span data-stu-id="4bfdc-147">O = S \* C + D</span></span>                  | <span data-ttu-id="4bfdc-148">Die resultierenden Pixelwerte sind die Summe der Quell-und Ziel Pixelwerte.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-148">The resulting pixel values are the sum of the source and destination pixel values.</span></span> <span data-ttu-id="4bfdc-149">Verfügbar in Windows 8 und höher.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-149">Available in Windows 8 and later.</span></span>     |



 

![eine Abbildung der primitiven Direct2D-Blend-Modi mit variierender Deckkraft und Hintergründen.](images/primblenddemo.png)

<span data-ttu-id="4bfdc-151">Eine Abbildung der primitiven Blend-Modi mit variierender Deckkraft und Hintergründen.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-151">An illustration of the primitive blend modes with varying opacity and backgrounds.</span></span>

<span data-ttu-id="4bfdc-152">Die primitive Mischung gilt für alle primitiven, die auf dem Kontext gezeichnet werden, es sei denn, dies wird mit dem *compositemode* -Parameter in der [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) -API überschrieben.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-152">The primitive blend will apply to all of the primitive drawn on the context, unless this is overridden with the *compositeMode* parameter on the [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) API.</span></span>

<span data-ttu-id="4bfdc-153">Die primitive Mischung bezieht sich auf das innere aller primitiven, die auf dem Kontext gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-153">The primitive blend applies to the interior of any primitives drawn on the context.</span></span> <span data-ttu-id="4bfdc-154">Im Fall von [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))wird dies durch das Bild Rechteck, den Offset und die globale Transformation impliziert.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-154">In the case of [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), this will be implied by the image rectangle, offset and world transform.</span></span>

<span data-ttu-id="4bfdc-155">Wenn die primitive Mischung nichts anderes als **D2D1 \_ primitiver \_ Blend \_** ist, wird das ClearType-Rendering deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-155">If the primitive blend is anything other than **D2D1\_PRIMITIVE\_BLEND\_OVER** then ClearType rendering will be turned off.</span></span> <span data-ttu-id="4bfdc-156">Wenn die Anwendung das ClearType-Rendering in diesen Modi explizit erzwingt, wird der Zeichnungs Kontext in einen Fehlerzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-156">If the application explicitly forces ClearType rendering in these modes, the drawing context will be placed in an error state.</span></span> <span data-ttu-id="4bfdc-157">D2DERR \_ falscher \_ Zustand wird von " [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) " oder " [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4bfdc-157">D2DERR\_WRONG\_STATE will be returned from either [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bfdc-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bfdc-158">Requirements</span></span>



| <span data-ttu-id="4bfdc-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bfdc-159">Requirement</span></span> | <span data-ttu-id="4bfdc-160">Wert</span><span class="sxs-lookup"><span data-stu-id="4bfdc-160">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bfdc-161">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-161">Minimum supported client</span></span><br/> | <span data-ttu-id="4bfdc-162">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4bfdc-162">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="4bfdc-163">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-163">Minimum supported server</span></span><br/> | <span data-ttu-id="4bfdc-164">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="4bfdc-164">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="4bfdc-165">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="4bfdc-165">Minimum supported phone</span></span><br/>  | <span data-ttu-id="4bfdc-166">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="4bfdc-166">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4bfdc-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bfdc-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bfdc-168">**ID2D1CommandSink1**</span><span class="sxs-lookup"><span data-stu-id="4bfdc-168">**ID2D1CommandSink1**</span></span>](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

