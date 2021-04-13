---
title: IDWriteFactory2-Methode "comateglyphrunanalysis"
description: Erstellt ein Symbol zum Ausführen von Symbolen, das Informationen kapselt, die zum renderischen Ausführen von Symbolen verwendet werden.
ms.assetid: 13cecfbf-8bb6-88a2-c8b2-3243f6cb92fd
keywords:
- Methode "comateglyphrunanalysis" direkt schreiben
- Methode "IDWriteFactory2" der Methode "" der Methode ""
- IDWriteFactory2 Interface Direct Write, Methode "kreateglyphrunanalysis"
topic_type:
- apiref
api_name:
- IDWriteFactory2.CreateGlyphRunAnalysis
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abd944c45fc271a22a0942556038073ebcc591cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392046"
---
# <a name="idwritefactory2createglyphrunanalysis-method"></a><span data-ttu-id="787de-106">IDWriteFactory2:: kreateglyphrunanalysis-Methode</span><span class="sxs-lookup"><span data-stu-id="787de-106">IDWriteFactory2::CreateGlyphRunAnalysis method</span></span>

<span data-ttu-id="787de-107">Erstellt ein Symbol zum Ausführen von Symbolen, das Informationen kapselt, die zum renderischen Ausführen von Symbolen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="787de-107">Creates a glyph run analysis object, which encapsulates information used to render a glyph run.</span></span>

## <a name="syntax"></a><span data-ttu-id="787de-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="787de-108">Syntax</span></span>


```C++
virtual HRESULT CreateGlyphRunAnalysis(
  [in]           const DWRITE_GLYPH_RUN           *glyphRun,
  [in, optional] const DWRITE_MATRIX              *transform,
                       DWRITE_RENDERING_MODE      renderingMode,
                       DWRITE_MEASURING_MODE      measuringMode,
                       DWRITE_GRID_FIT_MODE       gridFitMode,
                       DWRITE_TEXT_ANTIALIAS_MODE antialiasMode,
                       FLOAT                      baselineOriginX,
                       FLOAT                      baselineOriginY,
  [out]                IDWriteGlyphRunAnalysis    **glyphRunAnalysis
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="787de-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="787de-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="787de-110">*GlyphRun* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="787de-110">*glyphRun* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="787de-111">Typ: \* Konstante *[**dwrite- \_ Glyphe \_ Ausführen**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run) \** _</span><span class="sxs-lookup"><span data-stu-id="787de-111">Type: \**const [**DWRITE\_GLYPH\_RUN**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_run)\** _</span></span>

<span data-ttu-id="787de-112">-Struktur, die die Eigenschaften der Symbol Führung angibt.</span><span class="sxs-lookup"><span data-stu-id="787de-112">Structure specifying the properties of the glyph run.</span></span>

</dd> <dt>

<span data-ttu-id="787de-113">_transform \* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="787de-113">_transform\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="787de-114">Typ: \* Konstante *[**dwrite- \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \** _</span><span class="sxs-lookup"><span data-stu-id="787de-114">Type: \**const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\** _</span></span>

<span data-ttu-id="787de-115">Optionale Transformation, die auf die Symbole und deren Positionen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="787de-115">Optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="787de-116">Diese Transformation wird nach der durch "emSize" und "pixelsperdip" angegebenen Skalierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="787de-116">This transform is applied after the scaling specified by the emSize and pixelsPerDip.</span></span>

</dd> <dt>

<span data-ttu-id="787de-117">_renderingMode \*</span><span class="sxs-lookup"><span data-stu-id="787de-117">_renderingMode\*</span></span> 
</dt> <dd>

<span data-ttu-id="787de-118">Typ: **dwrite- \_ Renderingmodus \_**</span><span class="sxs-lookup"><span data-stu-id="787de-118">Type: **DWRITE\_RENDERING\_MODE**</span></span>

<span data-ttu-id="787de-119">Gibt den Renderingmodus an, bei dem es sich um einen der Raster Renderingmodi handeln muss (d. h. nicht default und Not Umriss).</span><span class="sxs-lookup"><span data-stu-id="787de-119">Specifies the rendering mode, which must be one of the raster rendering modes (i.e., not default and not outline).</span></span>

</dd> <dt>

<span data-ttu-id="787de-120">*measuringmode*</span><span class="sxs-lookup"><span data-stu-id="787de-120">*measuringMode*</span></span> 
</dt> <dd>

<span data-ttu-id="787de-121">Typ: **[ **dwrite \_ - \_ Messmodus**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span><span class="sxs-lookup"><span data-stu-id="787de-121">Type: **[**DWRITE\_MEASURING\_MODE**](/windows/win32/api/dcommon/ne-dcommon-dwrite_measuring_mode)**</span></span>

<span data-ttu-id="787de-122">Gibt die Methode an, mit der Symbole gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="787de-122">Specifies the method to measure glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="787de-123">*gridfitmode*</span><span class="sxs-lookup"><span data-stu-id="787de-123">*gridFitMode*</span></span> 
</dt> <dd>

<span data-ttu-id="787de-124">Type: **[ **dwrite \_ Grid \_ fit \_ Mode**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span><span class="sxs-lookup"><span data-stu-id="787de-124">Type: **[**DWRITE\_GRID\_FIT\_MODE**](/windows/win32/api/dwrite_2/ne-dwrite_2-dwrite_grid_fit_mode)**</span></span>

<span data-ttu-id="787de-125">Gewusst wie: Symbole mit Rasteranpassung.</span><span class="sxs-lookup"><span data-stu-id="787de-125">How to grid-fit glyph outlines.</span></span> <span data-ttu-id="787de-126">Dies darf nicht der Standardwert sein.</span><span class="sxs-lookup"><span data-stu-id="787de-126">This must be non-default.</span></span>

</dd> <dt>

<span data-ttu-id="787de-127">*antialiasmode*</span><span class="sxs-lookup"><span data-stu-id="787de-127">*antialiasMode*</span></span> 
</dt> <dd>

<span data-ttu-id="787de-128">Type: **[ **dwrite \_ Text \_ Antialias \_ Mode**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span><span class="sxs-lookup"><span data-stu-id="787de-128">Type: **[**DWRITE\_TEXT\_ANTIALIAS\_MODE**](/windows/win32/api/Dwrite_1/ne-dwrite_1-dwrite_text_antialias_mode)**</span></span>

<span data-ttu-id="787de-129">Gibt den AntiAlias Modus an.</span><span class="sxs-lookup"><span data-stu-id="787de-129">Specifies the antialias mode.</span></span>

</dd> <dt>

<span data-ttu-id="787de-130">*baselineoriginx*</span><span class="sxs-lookup"><span data-stu-id="787de-130">*baselineOriginX*</span></span> 
</dt> <dd>

<span data-ttu-id="787de-131">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="787de-131">Type: **FLOAT**</span></span>

<span data-ttu-id="787de-132">Die horizontale Position des Basis Linien Ursprungs in Dips.</span><span class="sxs-lookup"><span data-stu-id="787de-132">Horizontal position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="787de-133">*baselineoriginy*</span><span class="sxs-lookup"><span data-stu-id="787de-133">*baselineOriginY*</span></span> 
</dt> <dd>

<span data-ttu-id="787de-134">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="787de-134">Type: **FLOAT**</span></span>

<span data-ttu-id="787de-135">Vertikale Position des Basis Linien Ursprungs in Dips.</span><span class="sxs-lookup"><span data-stu-id="787de-135">Vertical position of the baseline origin, in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="787de-136">*glyphrunanalysis* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="787de-136">*glyphRunAnalysis* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="787de-137">Typ: **[ **idschreiteglyphrunanalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span><span class="sxs-lookup"><span data-stu-id="787de-137">Type: **[**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis)\*\***</span></span>

<span data-ttu-id="787de-138">Empfängt einen Zeiger auf das neu erstellte-Objekt.</span><span class="sxs-lookup"><span data-stu-id="787de-138">Receives a pointer to the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="787de-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="787de-139">Return value</span></span>

<span data-ttu-id="787de-140">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="787de-140">Type: **HRESULT**</span></span>

<span data-ttu-id="787de-141">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="787de-141">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="787de-142">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="787de-142">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="787de-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="787de-143">Requirements</span></span>



| <span data-ttu-id="787de-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="787de-144">Requirement</span></span> | <span data-ttu-id="787de-145">Wert</span><span class="sxs-lookup"><span data-stu-id="787de-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="787de-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="787de-146">Minimum supported client</span></span><br/> | <span data-ttu-id="787de-147">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="787de-147">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="787de-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="787de-148">Minimum supported server</span></span><br/> | <span data-ttu-id="787de-149">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="787de-149">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="787de-150">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="787de-150">Minimum supported phone</span></span><br/>  | <span data-ttu-id="787de-151">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="787de-151">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="787de-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="787de-152">Library</span></span><br/>                  | <dl> <span data-ttu-id="787de-153"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="787de-153"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="787de-154">DLL</span><span class="sxs-lookup"><span data-stu-id="787de-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="787de-155"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="787de-155"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="787de-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="787de-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="787de-157">**IDWriteFactory2**</span><span class="sxs-lookup"><span data-stu-id="787de-157">**IDWriteFactory2**</span></span>](idwritefactory2.md)
</dt> </dl>

 

