---
title: IDWriteFactory2-Methode für die Methode "samatecustomrenderingpara"
description: Erstellt ein Renderparameter-Objekt mit den angegebenen Eigenschaften.
ms.assetid: 947d50fd-888c-2f0b-25c2-b19b0e6fad58
keywords:
- Methode der Methode "kreatecustomrenderingparser" direkt schreiben
- Methode "samatecustomrenderingparser" Direct Write, IDWriteFactory2 Interface
- IDWriteFactory2 Interface Direct Write, Methode "kreatecustomrenderingparameams"
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateCustomRenderingParams
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36bd69cde6858061b69b8143dcdd0560342e65f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392047"
---
# <a name="idwritefactory2createcustomrenderingparams-method"></a><span data-ttu-id="bb619-106">IDWriteFactory2:: kreatecustomrenderingparameams-Methode</span><span class="sxs-lookup"><span data-stu-id="bb619-106">IDWriteFactory2::CreateCustomRenderingParams method</span></span>

<span data-ttu-id="bb619-107">Erstellt ein Renderparameter-Objekt mit den angegebenen Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="bb619-107">Creates a rendering parameters object with the specified properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb619-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb619-108">Syntax</span></span>


```C++
virtual HRESULT CreateCustomRenderingParams(
        FLOAT                   gamma,
        FLOAT                   enhancedContrast,
        FLOAT                   grayscaleEnhancedContrast,
        FLOAT                   clearTypeLevel,
        DWRITE_PIXEL_GEOMETRY   pixelGeometry,
        DWRITE_RENDERING_MODE   renderingMode,
        DWRITE_GRID_FIT_MODE    gridFitMode,
  [out] IDWriteRenderingParams2 **renderingParams
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="bb619-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb619-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb619-110">*GAM*</span><span class="sxs-lookup"><span data-stu-id="bb619-110">*gamma*</span></span> 
</dt> <dd>

<span data-ttu-id="bb619-111">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bb619-111">Type: **FLOAT**</span></span>

<span data-ttu-id="bb619-112">Der für die Gammakorrektur verwendete Gamma Wert, der größer als 0 (null) sein muss und 256 nicht überschreiten darf.</span><span class="sxs-lookup"><span data-stu-id="bb619-112">The gamma value used for gamma correction, which must be greater than zero and cannot exceed 256.</span></span>

</dd> <dt>

<span data-ttu-id="bb619-113">*enhancedcontrast*</span><span class="sxs-lookup"><span data-stu-id="bb619-113">*enhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="bb619-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bb619-114">Type: **FLOAT**</span></span>

<span data-ttu-id="bb619-115">Die Menge der Kontrastverbesserung, 0 (null) oder größer.</span><span class="sxs-lookup"><span data-stu-id="bb619-115">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="bb619-116">*grayscaleenhancedcontrast*</span><span class="sxs-lookup"><span data-stu-id="bb619-116">*grayscaleEnhancedContrast*</span></span> 
</dt> <dd>

<span data-ttu-id="bb619-117">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bb619-117">Type: **FLOAT**</span></span>

<span data-ttu-id="bb619-118">Die Menge der Kontrastverbesserung, 0 (null) oder größer.</span><span class="sxs-lookup"><span data-stu-id="bb619-118">The amount of contrast enhancement, zero or greater.</span></span>

</dd> <dt>

<span data-ttu-id="bb619-119">*ClearTypeLevel*</span><span class="sxs-lookup"><span data-stu-id="bb619-119">*clearTypeLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="bb619-120">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="bb619-120">Type: **FLOAT**</span></span>

<span data-ttu-id="bb619-121">Der Grad der ClearType-Ebene von 0,0 f (kein ClearType) bis 1.0 f (Full ClearType).</span><span class="sxs-lookup"><span data-stu-id="bb619-121">The degree of ClearType level, from 0.0f (no ClearType) to 1.0f (full ClearType).</span></span>

</dd> <dt>

<span data-ttu-id="bb619-122">*Pixel Geometry*</span><span class="sxs-lookup"><span data-stu-id="bb619-122">*pixelGeometry*</span></span> 
</dt> <dd>

<span data-ttu-id="bb619-123">Type: **[ **dwrite \_ Pixel \_ Geometry**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span><span class="sxs-lookup"><span data-stu-id="bb619-123">Type: **[**DWRITE\_PIXEL\_GEOMETRY**](/windows/win32/api/dwrite/ne-dwrite-dwrite_pixel_geometry)**</span></span>

<span data-ttu-id="bb619-124">Die Geometrie eines Geräte Pixels.</span><span class="sxs-lookup"><span data-stu-id="bb619-124">The geometry of a device pixel.</span></span>

</dd> <dt>

<span data-ttu-id="bb619-125">*renderingmode*</span><span class="sxs-lookup"><span data-stu-id="bb619-125">*renderingMode*</span></span> 
</dt> <dd>

<span data-ttu-id="bb619-126">Typ: **[ **dwrite \_ - \_ Renderingmodus**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span><span class="sxs-lookup"><span data-stu-id="bb619-126">Type: **[**DWRITE\_RENDERING\_MODE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_rendering_mode)**</span></span>

<span data-ttu-id="bb619-127">Methode zum Rendern von Symbolen.</span><span class="sxs-lookup"><span data-stu-id="bb619-127">Method of rendering glyphs.</span></span> <span data-ttu-id="bb619-128">In den meisten Fällen sollte dies der dwrite- \_ Renderingmodus sein, damit \_ \_ automatisch ein entsprechender Modus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="bb619-128">In most cases, this should be DWRITE\_RENDERING\_MODE\_DEFAULT to automatically use an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="bb619-129">*gridfitmode*</span><span class="sxs-lookup"><span data-stu-id="bb619-129">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="bb619-130">Type: **[ **dwrite \_ Grid \_ fit \_ Mode**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="bb619-130">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="bb619-131">Gewusst wie: Raster an Symbole anpassen.</span><span class="sxs-lookup"><span data-stu-id="bb619-131">How to grid fit glyph outlines.</span></span> <span data-ttu-id="bb619-132">In den meisten Fällen sollte dies der Standardwert \_ für die Einstellung "dwrite Grid" lauten \_ \_ , um automatisch einen geeigneten Modus auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="bb619-132">In most cases, this should be DWRITE\_GRID\_FIT\_DEFAULT to automatically choose an appropriate mode.</span></span>

</dd> <dt>

<span data-ttu-id="bb619-133">*renderingparametriams* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bb619-133">*renderingParams* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bb619-134">Typ: **[ **IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span><span class="sxs-lookup"><span data-stu-id="bb619-134">Type: **[**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2)\*\***</span></span>

<span data-ttu-id="bb619-135">Enthält das neu erstellte Renderparameter-Objekt oder NULL bei einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="bb619-135">Holds the newly created rendering parameters object, or NULL in case of failure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb619-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb619-136">Return value</span></span>

<span data-ttu-id="bb619-137">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bb619-137">Type: **HRESULT**</span></span>

<span data-ttu-id="bb619-138">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bb619-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bb619-139">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bb619-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb619-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb619-140">Requirements</span></span>



| <span data-ttu-id="bb619-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb619-141">Requirement</span></span> | <span data-ttu-id="bb619-142">Wert</span><span class="sxs-lookup"><span data-stu-id="bb619-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb619-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb619-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bb619-144">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb619-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="bb619-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb619-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bb619-146">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="bb619-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="bb619-147">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="bb619-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="bb619-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="bb619-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="bb619-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bb619-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="bb619-150"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb619-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="bb619-151">DLL</span><span class="sxs-lookup"><span data-stu-id="bb619-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb619-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb619-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb619-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb619-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb619-154">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="bb619-154">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

