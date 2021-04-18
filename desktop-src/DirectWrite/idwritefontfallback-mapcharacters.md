---
title: Idwrite Test fontfallback-mapcharacter-Methode
description: Bestimmt eine entsprechende Schriftart, die zum Rendering des Anfangs Bereichs von Text verwendet werden soll.
ms.assetid: 9D3DBBF7-72D4-473D-A321-E64BC94493D5
keywords:
- Mapcharacters-Methode, direktes Schreiben
- Mapcharacters-Methode direkt schreiben, idwrite-fontfallback-Schnittstelle
- Idwrite-fontfallback-Schnittstelle Direct Write, mapcharacters-Methode
topic_type:
- apiref
api_name:
- IDWriteFontFallback.MapCharacters
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 428778afc12c668d284dffb5a8a6f734c03f0705
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340837"
---
# <a name="idwritefontfallbackmapcharacters-method"></a><span data-ttu-id="06dbb-106">Idschreitefontfallback:: mapcharacters-Methode</span><span class="sxs-lookup"><span data-stu-id="06dbb-106">IDWriteFontFallback::MapCharacters method</span></span>

<span data-ttu-id="06dbb-107">Bestimmt eine entsprechende Schriftart, die zum Rendering des Anfangs Bereichs von Text verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="06dbb-107">Determines an appropriate font to use to render the beginning range of text.</span></span>

## <a name="syntax"></a><span data-ttu-id="06dbb-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="06dbb-108">Syntax</span></span>


```C++
HRESULT MapCharacters(
                       IDWriteTextAnalysisSource *source,
                       UINT32                    textPosition,
                       UINT32                    textLength,
  [in, optional]       IDWriteFontCollection     *baseFontCollection,
  [in, optional] const wchar_t                   *baseFamilyName,
                       DWRITE_FONT_WEIGHT        baseWeight,
                       DWRITE_FONT_STYLE         baseStyle,
                       DWRITE_FONT_STRETCH       baseStretch,
  [out]                UINT32                    *mappedLength,
  [out]                IDWriteFont               **mappedFont,
  [out]                FLOAT                     *scale
);
```



## <a name="parameters"></a><span data-ttu-id="06dbb-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="06dbb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06dbb-110">*Quelle*</span><span class="sxs-lookup"><span data-stu-id="06dbb-110">*source*</span></span> 
</dt> <dd>

<span data-ttu-id="06dbb-111">Typ: \**[**idschreitetextanalysissource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) \** _</span><span class="sxs-lookup"><span data-stu-id="06dbb-111">Type: \**[**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource)\** _</span></span>

<span data-ttu-id="06dbb-112">Die Textquellen Implementierung enthält den Text und das Gebiets Schema.</span><span class="sxs-lookup"><span data-stu-id="06dbb-112">The text source implementation holds the text and locale.</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-113">_textPosition \*</span><span class="sxs-lookup"><span data-stu-id="06dbb-113">_textPosition\*</span></span> 
</dt> <dd>

<span data-ttu-id="06dbb-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06dbb-114">Type: **UINT32**</span></span>

<span data-ttu-id="06dbb-115">Startposition, die analysiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="06dbb-115">Starting position to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-116">*TextLength*</span><span class="sxs-lookup"><span data-stu-id="06dbb-116">*textLength*</span></span> 
</dt> <dd>

<span data-ttu-id="06dbb-117">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="06dbb-117">Type: **UINT32**</span></span>

<span data-ttu-id="06dbb-118">Die Länge des zu analysierenden Texts.</span><span class="sxs-lookup"><span data-stu-id="06dbb-118">Length of the text to analyze.</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-119">*basefontcollection* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="06dbb-119">*baseFontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06dbb-120">Typ: \**[**idschreitefontcollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) \** _</span><span class="sxs-lookup"><span data-stu-id="06dbb-120">Type: \**[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)\** _</span></span>

<span data-ttu-id="06dbb-121">Die zu verwendende Standard Schriftart Auflistung.</span><span class="sxs-lookup"><span data-stu-id="06dbb-121">Default font collection to use.</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-122">_baseFamilyName \* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="06dbb-122">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="06dbb-123">Typ: \* Konstante *WCHAR \_ t \** _</span><span class="sxs-lookup"><span data-stu-id="06dbb-123">Type: \**const wchar\_t\** _</span></span>

<span data-ttu-id="06dbb-124">Der Familienname der Basis Schriftart.</span><span class="sxs-lookup"><span data-stu-id="06dbb-124">Family name of the base font.</span></span> <span data-ttu-id="06dbb-125">Wenn Sie NULL übergeben, erfolgt keine Übereinstimmung mit der Familie.</span><span class="sxs-lookup"><span data-stu-id="06dbb-125">If you pass null, no matching will be done against the family.</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-126">_baseWeight \*</span><span class="sxs-lookup"><span data-stu-id="06dbb-126">_baseWeight\*</span></span> 
</dt> <dd>

<span data-ttu-id="06dbb-127">Type: **[ **dwrite \_ Schriftart \_ Weight**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span><span class="sxs-lookup"><span data-stu-id="06dbb-127">Type: **[**DWRITE\_FONT\_WEIGHT**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_weight)**</span></span>

<span data-ttu-id="06dbb-128">Die gewünschte Gewichtung.</span><span class="sxs-lookup"><span data-stu-id="06dbb-128">The desired weight.</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-129">*BaseStyle*</span><span class="sxs-lookup"><span data-stu-id="06dbb-129">*baseStyle*</span></span> 
</dt> <dd>

<span data-ttu-id="06dbb-130">Type: **[ **dwrite- \_ Schriftart \_ Stil**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span><span class="sxs-lookup"><span data-stu-id="06dbb-130">Type: **[**DWRITE\_FONT\_STYLE**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_style)**</span></span>

<span data-ttu-id="06dbb-131">Der gewünschte Stil.</span><span class="sxs-lookup"><span data-stu-id="06dbb-131">The desired style.</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-132">*basestretch*</span><span class="sxs-lookup"><span data-stu-id="06dbb-132">*baseStretch*</span></span> 
</dt> <dd>

<span data-ttu-id="06dbb-133">Typ: **[ **dwrite- \_ Schriftart \_ Streckung**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span><span class="sxs-lookup"><span data-stu-id="06dbb-133">Type: **[**DWRITE\_FONT\_STRETCH**](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_stretch)**</span></span>

<span data-ttu-id="06dbb-134">Die gewünschte Streckung.</span><span class="sxs-lookup"><span data-stu-id="06dbb-134">The desired stretch.</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-135">*mappedlength* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="06dbb-135">*mappedLength* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06dbb-136">Typ: \**UInt32 \** _</span><span class="sxs-lookup"><span data-stu-id="06dbb-136">Type: \**UINT32\** _</span></span>

<span data-ttu-id="06dbb-137">Länge des Texts, der der zugeordneten Schriftart zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="06dbb-137">Length of text mapped to the mapped font.</span></span> <span data-ttu-id="06dbb-138">Diese ist immer kleiner oder gleich der Textlänge und größer als 0 (wenn die Textlänge ungleich NULL ist), sodass der Aufrufer mindestens ein Zeichen verschiebt.</span><span class="sxs-lookup"><span data-stu-id="06dbb-138">This will always be less than or equal to the text length and greater than zero (if the text length is non-zero) so the caller advances at least one character.</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-139">_mappedFont \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="06dbb-139">_mappedFont\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06dbb-140">Typ: **[ **idschreiteschriftart**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span><span class="sxs-lookup"><span data-stu-id="06dbb-140">Type: **[**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont)\*\***</span></span>

<span data-ttu-id="06dbb-141">Die Schriftart, die verwendet werden soll, um die ersten *mappedlength* -Zeichen des Texts zu erzeugen.</span><span class="sxs-lookup"><span data-stu-id="06dbb-141">The font that should be used to render the first *mappedLength* characters of the text.</span></span> <span data-ttu-id="06dbb-142">Wenn NULL zurückgegeben wird, bedeutet dies, dass der Text von keiner Schriftart gerendert werden kann, und *mappedlength* die Anzahl der zu über springenden Zeichen (mit einem fehlenden Symbol gerendert).</span><span class="sxs-lookup"><span data-stu-id="06dbb-142">If it returns NULL, that means that no font can render the text, and *mappedLength* is the number of characters to skip (rendered with a missing glyph).</span></span>

</dd> <dt>

<span data-ttu-id="06dbb-143">*skalieren* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="06dbb-143">*scale* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06dbb-144">Typ: \**float \** _</span><span class="sxs-lookup"><span data-stu-id="06dbb-144">Type: \**FLOAT\** _</span></span>

<span data-ttu-id="06dbb-145">Skalierungsfaktor, um die Geviert Größe der zurückgegebenen Schriftart zu multiplizieren.</span><span class="sxs-lookup"><span data-stu-id="06dbb-145">Scale factor to multiply the em size of the returned font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06dbb-146">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06dbb-146">Return value</span></span>

<span data-ttu-id="06dbb-147">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="06dbb-147">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="06dbb-148">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="06dbb-148">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="06dbb-149">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="06dbb-149">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="06dbb-150">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06dbb-150">Requirements</span></span>



| <span data-ttu-id="06dbb-151">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06dbb-151">Requirement</span></span> | <span data-ttu-id="06dbb-152">Wert</span><span class="sxs-lookup"><span data-stu-id="06dbb-152">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06dbb-153">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="06dbb-153">Minimum supported client</span></span><br/> | <span data-ttu-id="06dbb-154">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="06dbb-154">Windows 8.1 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="06dbb-155">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="06dbb-155">Minimum supported server</span></span><br/> | <span data-ttu-id="06dbb-156">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="06dbb-156">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="06dbb-157">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="06dbb-157">Minimum supported phone</span></span><br/>  | <span data-ttu-id="06dbb-158">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="06dbb-158">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="06dbb-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06dbb-159">Library</span></span><br/>                  | <dl> <span data-ttu-id="06dbb-160"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06dbb-160"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="06dbb-161">DLL</span><span class="sxs-lookup"><span data-stu-id="06dbb-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06dbb-162"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06dbb-162"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06dbb-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06dbb-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06dbb-164">**Idschreitefontfallback**</span><span class="sxs-lookup"><span data-stu-id="06dbb-164">**IDWriteFontFallback**</span></span>](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback)
</dt> </dl>

 

