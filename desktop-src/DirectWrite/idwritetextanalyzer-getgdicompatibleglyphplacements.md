---
title: Idwrite Test Textanalyzer getgdicompatibleglyphplacement-Methode
description: Platzieren Sie die Glyphen-Ausgabe der getglyphs-Methode gemäß der Schriftart und den Renderingregeln des Schreibsystems.
ms.assetid: 49312b03-9ee9-44ef-b3eb-a35631a6e693
keywords:
- Getgdicompatibleglyphplacement-Methode direkt Schreibvorgang
- Getgdicompatibleglyphplacement-Methode Direct Write, idwrite tetextanalyzer-Schnittstelle
- Idwrite tetextanalyzer-Schnittstelle Direct Write, getgdicompatibleglyphplacement-Methode
topic_type:
- apiref
api_name:
- IDWriteTextAnalyzer.GetGdiCompatibleGlyphPlacements
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f548e5fd20ce8814dc59657ff7bb422387c959fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364594"
---
# <a name="idwritetextanalyzergetgdicompatibleglyphplacements-method"></a><span data-ttu-id="71f06-106">Idwrite Test Textanalyzer:: getgdicompatibleglyphplacement-Methode</span><span class="sxs-lookup"><span data-stu-id="71f06-106">IDWriteTextAnalyzer::GetGdiCompatibleGlyphPlacements method</span></span>

<span data-ttu-id="71f06-107">Platzieren Sie die Glyphen-Ausgabe der [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) -Methode gemäß der Schriftart und den Renderingregeln des Schreibsystems.</span><span class="sxs-lookup"><span data-stu-id="71f06-107">Place glyphs output from the [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs) method according to the font and the writing system's rendering rules.</span></span>

## <a name="syntax"></a><span data-ttu-id="71f06-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="71f06-108">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleGlyphPlacements(
  [in]           const WCHAR                           *textString,
  [in]           const UINT16                          *clusterMap,
  [in]                 DWRITE_SHAPING_TEXT_PROPERTIES  *textProps,
                       UINT32                          textLength,
  [in]           const UINT16                          *glyphIndices,
  [in]           const DWRITE_SHAPING_GLYPH_PROPERTIES *glyphProps,
                       UINT32                          glyphCount,
  [in]                 IDWriteFontFace                 *fontFace,
                       FLOAT                           fontEmSize,
                       FLOAT                           pixelsPerDip,
  [in, optional] const DWRITE_MATRIX                   *transform,
                       BOOL                            useGdiNatural,
                       BOOL                             isSideways,
                       BOOL                             isRightToLeft,
  [in]           const DWRITE_SCRIPT_ANALYSIS          * scriptAnalysis,
  [in, optional] const WCHAR                           * localeName,
  [in, optional] const DWRITE_TYPOGRAPHIC_FEATURES     ** features,
  [in, optional] const UINT32                          * featureRangeLengths,
                       UINT32                           featureRanges,
  [out]                FLOAT                           * glyphAdvances,
  [out]                DWRITE_GLYPH_OFFSET             * glyphOffsets
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="71f06-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="71f06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71f06-110">*Textstring* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f06-110">*textString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-111">Typ: Konstante **WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="71f06-111">Type: **const WCHAR\***</span></span>

<span data-ttu-id="71f06-112">Ein Array von Zeichen, das die Original Zeichenfolge enthält, aus der die Symbole stammen.</span><span class="sxs-lookup"><span data-stu-id="71f06-112">An array of characters containing the original string from which the glyphs came.</span></span>

</dd> <dt>

<span data-ttu-id="71f06-113">*ClusterMap* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f06-113">*clusterMap* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-114">Typ: **Konstanten UInt16 \***</span><span class="sxs-lookup"><span data-stu-id="71f06-114">Type: **const UINT16\***</span></span>

<span data-ttu-id="71f06-115">Ein Zeiger auf die Zuordnung von Zeichen Bereichen zu Symbol Bereichen.</span><span class="sxs-lookup"><span data-stu-id="71f06-115">A pointer to the mapping from character ranges to glyph ranges.</span></span> <span data-ttu-id="71f06-116">Dies wird von " [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71f06-116">This is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="71f06-117">*Texteigenschaften* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f06-117">*textProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-118">Type: **[ **dwrite-Strukturierungs \_ Text- \_ \_ Eigenschaften**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span><span class="sxs-lookup"><span data-stu-id="71f06-118">Type: **[**DWRITE\_SHAPING\_TEXT\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_text_properties)\***</span></span>

<span data-ttu-id="71f06-119">Ein Zeiger auf ein Array von-Strukturen, das Strukturierungs Eigenschaften für jedes Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="71f06-119">A pointer to an array of structures that contains shaping properties for each character.</span></span> <span data-ttu-id="71f06-120">Diese Struktur wird von " [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71f06-120">This structure is returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="71f06-121">*TextLength*</span><span class="sxs-lookup"><span data-stu-id="71f06-121">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="71f06-122">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71f06-122">Type: **UINT32**</span></span>

<span data-ttu-id="71f06-123">Die Textlänge von *Textstring*.</span><span class="sxs-lookup"><span data-stu-id="71f06-123">The text length of *textString*.</span></span>

</dd> <dt>

<span data-ttu-id="71f06-124">*GlyphIndices* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f06-124">*glyphIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-125">Typ: **Konstanten UInt16 \***</span><span class="sxs-lookup"><span data-stu-id="71f06-125">Type: **const UINT16\***</span></span>

<span data-ttu-id="71f06-126">Ein Array von Glyphe-Indizes, die von [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="71f06-126">An array of glyph indices returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="71f06-127">*Glyph-* \[ Eigenschaften in\]</span><span class="sxs-lookup"><span data-stu-id="71f06-127">*glyphProps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-128">Typ: Konstante **[**dwrite- \_ Formen \_ Glyphe- \_ Eigenschaften**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties) \***</span><span class="sxs-lookup"><span data-stu-id="71f06-128">Type: **const [**DWRITE\_SHAPING\_GLYPH\_PROPERTIES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_shaping_glyph_properties)\***</span></span>

<span data-ttu-id="71f06-129">Ein Zeiger auf ein Array von-Strukturen, die für jedes Symbol, das von [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben wird, Strukturierungs Eigenschaften enthalten.</span><span class="sxs-lookup"><span data-stu-id="71f06-129">A pointer to an array of structures that contain shaping properties for each glyph returned by [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="71f06-130">*GlyphCount*</span><span class="sxs-lookup"><span data-stu-id="71f06-130">*glyphCount*</span></span> 
</dt> <dd>

<span data-ttu-id="71f06-131">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71f06-131">Type: **UINT32**</span></span>

<span data-ttu-id="71f06-132">Die Anzahl von Symbolen, die von [**getglyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs)zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="71f06-132">The number of glyphs returned from [**GetGlyphs**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-getglyphs).</span></span>

</dd> <dt>

<span data-ttu-id="71f06-133">*fontface* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f06-133">*fontFace* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-134">Typ: **[ **idschreitefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span><span class="sxs-lookup"><span data-stu-id="71f06-134">Type: **[**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)\***</span></span>

<span data-ttu-id="71f06-135">Ein Zeiger auf die Schriftart, bei der es sich um die Quelle für die Ausgabe Symbole handelt.</span><span class="sxs-lookup"><span data-stu-id="71f06-135">A pointer to the font face that is the source for the output glyphs.</span></span>

</dd> <dt>

<span data-ttu-id="71f06-136">*fontemsize*</span><span class="sxs-lookup"><span data-stu-id="71f06-136">*fontEmSize*</span></span> 
</dt> <dd>

<span data-ttu-id="71f06-137">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="71f06-137">Type: **FLOAT**</span></span>

<span data-ttu-id="71f06-138">Die logische Schriftgröße in Dips.</span><span class="sxs-lookup"><span data-stu-id="71f06-138">The logical font size in DIPs.</span></span>

</dd> <dt>

<span data-ttu-id="71f06-139">*Pixel sperdip*</span><span class="sxs-lookup"><span data-stu-id="71f06-139">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="71f06-140">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="71f06-140">Type: **FLOAT**</span></span>

<span data-ttu-id="71f06-141">Die Anzahl der physischen Pixel pro DIP.</span><span class="sxs-lookup"><span data-stu-id="71f06-141">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="71f06-142">*Transformation* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="71f06-142">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-143">Typ: Konstante **[**dwrite- \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="71f06-143">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="71f06-144">Eine optionale Transformation, die auf die Symbole und deren Positionen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="71f06-144">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="71f06-145">Diese Transformation wird nach der durch Schriftart Größe und *pixelsperdip* angegebenen Skalierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="71f06-145">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="71f06-146">*usegdinatural*</span><span class="sxs-lookup"><span data-stu-id="71f06-146">*useGdiNatural*</span></span> 
</dt> <dd>

<span data-ttu-id="71f06-147">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="71f06-147">Type: **BOOL**</span></span>

<span data-ttu-id="71f06-148">Wenn diese Einstellung auf " **false**" festgelegt ist, sind die Metriken mit den Metriken des GDI-Alias Texts identisch.</span><span class="sxs-lookup"><span data-stu-id="71f06-148">When set to **FALSE**, the metrics are the same as the metrics of GDI aliased text.</span></span> <span data-ttu-id="71f06-149">Wenn diese Eigenschaft auf " **true**" festgelegt ist, sind die Metriken identisch mit den Metriken von Text, der von GDI mithilfe einer mit **ClearType \_ Natural \_ Quality** erstellten Schriftart gemessen wird.</span><span class="sxs-lookup"><span data-stu-id="71f06-149">When set to **TRUE**, the metrics are the same as the metrics of text measured by GDI using a font created with **CLEARTYPE\_NATURAL\_QUALITY**.</span></span>

</dd> <dt>

 <span data-ttu-id="71f06-150">*issientways*</span><span class="sxs-lookup"><span data-stu-id="71f06-150">*isSideways*</span></span> 
</dt> <dd>

<span data-ttu-id="71f06-151">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="71f06-151">Type: **BOOL**</span></span>

<span data-ttu-id="71f06-152">Ein boolesches Flag, das auf **true** festgelegt ist, wenn der Text vertikal gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="71f06-152">A Boolean flag set to **TRUE** if the text is intended to be drawn vertically.</span></span>

</dd> <dt>

 <span data-ttu-id="71f06-153">*IsRightToLeft*</span><span class="sxs-lookup"><span data-stu-id="71f06-153">*isRightToLeft*</span></span> 
</dt> <dd>

<span data-ttu-id="71f06-154">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="71f06-154">Type: **BOOL**</span></span>

<span data-ttu-id="71f06-155">Ein boolesches Flag, das für Text von rechts nach links auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="71f06-155">A Boolean flag set to **TRUE** for right-to-left text.</span></span>

</dd> <dt>

 <span data-ttu-id="71f06-156">*scriptanalysis* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="71f06-156">*scriptAnalysis* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-157">Typ: Konstante **[**dwrite- \_ Skript \_ Analyse**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis) \***</span><span class="sxs-lookup"><span data-stu-id="71f06-157">Type: **const [**DWRITE\_SCRIPT\_ANALYSIS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_script_analysis)\***</span></span>

<span data-ttu-id="71f06-158">Ein Zeiger auf ein Skript Analyseergebnis eines [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) -Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="71f06-158">A pointer to a Script analysis result from an [**AnalyzeScript**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalyzer-analyzescript) call.</span></span>

</dd> <dt>

 <span data-ttu-id="71f06-159">*localename* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="71f06-159">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-160">Typ: Konstante **WCHAR \***</span><span class="sxs-lookup"><span data-stu-id="71f06-160">Type: **const WCHAR\***</span></span>

<span data-ttu-id="71f06-161">Ein Array von Zeichen, das das zu verwendende Gebiets Schema enthält, wenn Symbole ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="71f06-161">An array of characters containing the locale to use when selecting glyphs.</span></span> <span data-ttu-id="71f06-162">Beispielsweise kann das gleiche Zeichen anderen Symbolen für ja-JP und zh-CHS zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="71f06-162">For example, the same character may map to different glyphs for ja-jp versus zh-chs.</span></span> <span data-ttu-id="71f06-163">Wenn dieser Wert **null** ist, wird die auf dem Skript basierende Standard Zuordnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="71f06-163">If this is **NULL**, then the default mapping based on the script is used.</span></span>

</dd> <dt>

 <span data-ttu-id="71f06-164">*Features* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="71f06-164">*features* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-165">Typ: Konstante **[**dwrite- \_ Typografiefunktionen \_**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features) \* \***</span><span class="sxs-lookup"><span data-stu-id="71f06-165">Type: **const [**DWRITE\_TYPOGRAPHIC\_FEATURES**](/windows/win32/api/dwrite/ns-dwrite-dwrite_typographic_features)\*\***</span></span>

<span data-ttu-id="71f06-166">Ein Array von Zeigern auf die Sätze von typografischen Features, die in jedem Featurebereich verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="71f06-166">An array of pointers to the sets of typographic features to use in each feature range.</span></span>

</dd> <dt>

 <span data-ttu-id="71f06-167">*featurerangelengths* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="71f06-167">*featureRangeLengths* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-168">Typ: **Konstanten UInt32 \***</span><span class="sxs-lookup"><span data-stu-id="71f06-168">Type: **const UINT32\***</span></span>

<span data-ttu-id="71f06-169">Die Länge der einzelnen Funktionsbereiche in Zeichen.</span><span class="sxs-lookup"><span data-stu-id="71f06-169">The length of each feature range, in characters.</span></span> <span data-ttu-id="71f06-170">Die Summe aller Längen muss gleich " *TextLength*" sein.</span><span class="sxs-lookup"><span data-stu-id="71f06-170">The sum of all lengths should be equal to *textLength*.</span></span>

</dd> <dt>

 <span data-ttu-id="71f06-171">*featureranges*</span><span class="sxs-lookup"><span data-stu-id="71f06-171">*featureRanges*</span></span> 
</dt> <dd>

<span data-ttu-id="71f06-172">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="71f06-172">Type: **UINT32**</span></span>

<span data-ttu-id="71f06-173">Die Anzahl von Funktionsbereichen.</span><span class="sxs-lookup"><span data-stu-id="71f06-173">The number of feature ranges.</span></span>

</dd> <dt>

 <span data-ttu-id="71f06-174">*glyphadvanzen* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="71f06-174">*glyphAdvances* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-175">Typ: **float \***</span><span class="sxs-lookup"><span data-stu-id="71f06-175">Type: **FLOAT\***</span></span>

<span data-ttu-id="71f06-176">Wenn diese Methode zurückgegeben wird, enthält Sie die voraus Breite jedes Symbols.</span><span class="sxs-lookup"><span data-stu-id="71f06-176">When this method returns, contains the advance width of each glyph.</span></span>

</dd> <dt>

 <span data-ttu-id="71f06-177">*Glyphosat-ffsets* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="71f06-177">*glyphOffsets* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="71f06-178">Typ: **[ **dwrite- \_ Glyphe \_ Offset**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span><span class="sxs-lookup"><span data-stu-id="71f06-178">Type: **[**DWRITE\_GLYPH\_OFFSET**](/windows/win32/api/dwrite/ns-dwrite-dwrite_glyph_offset)\***</span></span>

<span data-ttu-id="71f06-179">Wenn diese Methode zurückgegeben wird, enthält Sie den Offset des Ursprungs der einzelnen Glyphe.</span><span class="sxs-lookup"><span data-stu-id="71f06-179">When this method returns, contains the offset of the origin of each glyph.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71f06-180">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="71f06-180">Return value</span></span>

<span data-ttu-id="71f06-181">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="71f06-181">Type: **HRESULT**</span></span>

<span data-ttu-id="71f06-182">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="71f06-182">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="71f06-183">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="71f06-183">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="71f06-184">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="71f06-184">Requirements</span></span>



| <span data-ttu-id="71f06-185">Anforderung</span><span class="sxs-lookup"><span data-stu-id="71f06-185">Requirement</span></span> | <span data-ttu-id="71f06-186">Wert</span><span class="sxs-lookup"><span data-stu-id="71f06-186">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="71f06-187">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="71f06-187">Library</span></span><br/> | <dl> <span data-ttu-id="71f06-188"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="71f06-188"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="71f06-189">DLL</span><span class="sxs-lookup"><span data-stu-id="71f06-189">DLL</span></span><br/>     | <dl> <span data-ttu-id="71f06-190"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71f06-190"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71f06-191">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="71f06-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71f06-192">**Idschreitetextanalyzer**</span><span class="sxs-lookup"><span data-stu-id="71f06-192">**IDWriteTextAnalyzer**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer)
</dt> </dl>

 

