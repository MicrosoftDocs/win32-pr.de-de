---
title: Idwrite-fontface getgdicompatibleglyphmetrics-Methode
description: Ruft Symbol Metriken in Schriftart Entwurfs Einheiten mit den Rückgabe Werten ab, die mit den GDI-Werten kompatibel sind.
ms.assetid: 7bda3916-6db3-4f56-b18c-288506c0b646
keywords:
- Getgdicompatibleglyphmetrics-Methode direkt Schreibvorgang
- Getgdicompatibleglyphmetrics-Methode direkt schreiben, idschreitefontface-Schnittstelle
- Idwrite-fontface Interface Direct Write, getgdicompatibleglyphmetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleGlyphMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a949edbdad2f25d748e5af64ebe408c79c7372b9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371636"
---
# <a name="idwritefontfacegetgdicompatibleglyphmetrics-method"></a><span data-ttu-id="8ef96-106">Idschreitefontface:: getgdicompatibleglyphmetrics-Methode</span><span class="sxs-lookup"><span data-stu-id="8ef96-106">IDWriteFontFace::GetGdiCompatibleGlyphMetrics method</span></span>

<span data-ttu-id="8ef96-107">Ruft Symbol Metriken in Schriftart Entwurfs Einheiten mit den Rückgabe Werten ab, die mit den GDI-Werten kompatibel sind.</span><span class="sxs-lookup"><span data-stu-id="8ef96-107">Obtains glyph metrics in font design units with the return values compatible with what GDI would produce.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ef96-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ef96-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphMetrics(
                       FLOAT                emSize,
                       FLOAT                pixelsPerDip,
  [in, optional] const DWRITE_MATRIX        *transform,
                       BOOL                 useGdiNatural,
  [in]           const UINT16               *glyphIndices,
                       UINT32               glyphCount,
  [out]                DWRITE_GLYPH_METRICS *glyphMetrics,
                       BOOL                 isSideways = FALSE
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="8ef96-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ef96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ef96-110">*emSize*</span><span class="sxs-lookup"><span data-stu-id="8ef96-110">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef96-111">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="8ef96-111">Type: **FLOAT**</span></span>

<span data-ttu-id="8ef96-112">Die ogische Größe der Schriftart in DIP-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="8ef96-112">The ogical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="8ef96-113">*Pixel sperdip*</span><span class="sxs-lookup"><span data-stu-id="8ef96-113">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef96-114">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="8ef96-114">Type: **FLOAT**</span></span>

<span data-ttu-id="8ef96-115">Die Anzahl der physischen Pixel pro DIP.</span><span class="sxs-lookup"><span data-stu-id="8ef96-115">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="8ef96-116">*Transformation* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="8ef96-116">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8ef96-117">Typ: Konstante **[**dwrite- \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="8ef96-117">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="8ef96-118">Eine optionale Transformation, die auf die Symbole und deren Positionen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="8ef96-118">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="8ef96-119">Diese Transformation wird nach der durch Schriftart Größe und *pixelsperdip* angegebenen Skalierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="8ef96-119">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="8ef96-120">*usegdinatural*</span><span class="sxs-lookup"><span data-stu-id="8ef96-120">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef96-121">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="8ef96-121">Type: **BOOL**</span></span>

<span data-ttu-id="8ef96-122">Wenn diese Einstellung auf " **false**" festgelegt ist, sind die Metriken mit den Metriken des GDI-Alias Texts identisch.</span><span class="sxs-lookup"><span data-stu-id="8ef96-122">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="8ef96-123">Wenn diese Eigenschaft auf " **true**" festgelegt ist, sind die Metriken identisch mit den Metriken von Text, der von GDI mithilfe einer mit **ClearType \_ Natural \_ Quality** erstellten Schriftart gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="8ef96-123">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

<span data-ttu-id="8ef96-124">*GlyphIndices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8ef96-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ef96-125">Typ: **Konstanten UInt16 \***</span><span class="sxs-lookup"><span data-stu-id="8ef96-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="8ef96-126">Ein Array von Symbol Indizes, für das die Metriken berechnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8ef96-126">An array of glyph indices for which to compute the metrics.</span></span>

</dd> <dt>

<span data-ttu-id="8ef96-127">*GlyphCount*</span><span class="sxs-lookup"><span data-stu-id="8ef96-127">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef96-128">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="8ef96-128">Type: **UINT32**</span></span>

<span data-ttu-id="8ef96-129">Die Anzahl der Elemente im *GlyphIndices* -Array.</span><span class="sxs-lookup"><span data-stu-id="8ef96-129">The number of elements in the *glyphIndices* array.</span></span>

</dd> <dt>

<span data-ttu-id="8ef96-130">*GlyphMetrics* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8ef96-130">*glyphMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8ef96-131">Typ: **[ **dwrite- \_ Glyphe- \_ Metriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="8ef96-131">Type: **[**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics)\***</span></span>

<span data-ttu-id="8ef96-132">Ein Array von [**dwrite- \_ Glyphe- \_ Metriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) , die von dieser Funktion ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="8ef96-132">An array of [**DWRITE\_GLYPH\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_metrics) structures filled by this function.</span></span> <span data-ttu-id="8ef96-133">Die Metriken sind in Schriftart Entwurfs Einheiten.</span><span class="sxs-lookup"><span data-stu-id="8ef96-133">The metrics are in font design units.</span></span>

</dd> <dt>

<span data-ttu-id="8ef96-134">*issientways*</span><span class="sxs-lookup"><span data-stu-id="8ef96-134">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="8ef96-135">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="8ef96-135">Type: **BOOL**</span></span>

<span data-ttu-id="8ef96-136">Ein boolescher Wert, der angibt, ob die Schriftart in einer seitwärts lauflauf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8ef96-136">A BOOL value that indicates whether the font is being used in a sideways run.</span></span> <span data-ttu-id="8ef96-137">Dies kann sich auf die Glyphe-Metriken auswirken, wenn die Schriftart über eine schräge Simulation verfügt, da sich die seitwärts schräge Simulation von der nicht-seitwärts schrägen</span><span class="sxs-lookup"><span data-stu-id="8ef96-137">This can affect the glyph metrics if the font has oblique simulation because sideways oblique simulation differs from non-sideways oblique simulation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ef96-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ef96-138">Return value</span></span>

<span data-ttu-id="8ef96-139">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8ef96-139">Type: **HRESULT**</span></span>

<span data-ttu-id="8ef96-140">Standard- **HRESULT** -Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="8ef96-140">Standard **HRESULT** error code.</span></span> <span data-ttu-id="8ef96-141">Wenn eine der Eingabe Symbol Indizes außerhalb des gültigen Symbol Index Bereichs für die aktuelle Schriftart liegt, wird **E \_ invalidArg** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8ef96-141">If any of the input glyph indices are outside of the valid glyph index range for the current font face, **E\_INVALIDARG** will be returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ef96-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ef96-142">Requirements</span></span>



| <span data-ttu-id="8ef96-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ef96-143">Requirement</span></span> | <span data-ttu-id="8ef96-144">Wert</span><span class="sxs-lookup"><span data-stu-id="8ef96-144">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8ef96-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ef96-145">Library</span></span><br/> | <dl> <span data-ttu-id="8ef96-146"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8ef96-146"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="8ef96-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8ef96-147">DLL</span></span><br/>     | <dl> <span data-ttu-id="8ef96-148"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ef96-148"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ef96-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ef96-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ef96-150">**Idschreitefontface**</span><span class="sxs-lookup"><span data-stu-id="8ef96-150">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="8ef96-151">**Idschreitefontface**</span><span class="sxs-lookup"><span data-stu-id="8ef96-151">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

