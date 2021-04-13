---
title: Idwrite-fontfallbackbuilder-AddMapping-Methode
description: Fügt eine einzelne Zuordnung an die Liste an. Dies wird einmal für jede weitere Zuordnung aufgerufen.
ms.assetid: FCA3CD9C-9FB3-49BD-B4D1-53AEAAAAEE8A
keywords:
- Direkte Schreibweise von AddMapping-Methode
- AddMapping-Methode Direct Write, idwrite Test fontfallbackbuilder-Schnittstelle
- Idwrite-fontfallbackbuilder-Schnittstelle Direct Write, AddMapping-Methode
topic_type:
- apiref
api_name:
- IDWriteFontFallbackBuilder.AddMapping
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a084aa2a9df0e34741c8bf5f39ae00933d49cfe7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392043"
---
# <a name="idwritefontfallbackbuilderaddmapping-method"></a><span data-ttu-id="d7f05-107">Idschreitefontfallbackbuilder:: AddMapping-Methode</span><span class="sxs-lookup"><span data-stu-id="d7f05-107">IDWriteFontFallbackBuilder::AddMapping method</span></span>

<span data-ttu-id="d7f05-108">Fügt eine einzelne Zuordnung an die Liste an.</span><span class="sxs-lookup"><span data-stu-id="d7f05-108">Appends a single mapping to the list.</span></span> <span data-ttu-id="d7f05-109">Dies wird einmal für jede weitere Zuordnung aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="d7f05-109">Call this once for each additional mapping.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f05-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7f05-110">Syntax</span></span>


```C++
HRESULT AddMapping(
                       DWRITE_UNICODE_RANGE  *ranges,
                       UINT32                rangesCount,
  [in]           const WCHAR                 **targetFamilyNames,
                       UINT32                targetFamilyNamesCount,
  [in, optional]       IDWriteFontCollection fontCollection = nullptr,
  [in, optional] const WCHAR                 *localeName = nullptr,
  [in, optional] const WCHAR                 *baseFamilyName = nullptr,
                       FLOAT                 scale = 1
);
```



## <a name="parameters"></a><span data-ttu-id="d7f05-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7f05-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f05-112">*Ketten*</span><span class="sxs-lookup"><span data-stu-id="d7f05-112">*ranges*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f05-113">Typ: \**[**dwrite- \_ Unicode- \_ Bereich**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range) \** _</span><span class="sxs-lookup"><span data-stu-id="d7f05-113">Type: \**[**DWRITE\_UNICODE\_RANGE**](/windows/win32/api/Dwrite_1/ns-dwrite_1-dwrite_unicode_range)\** _</span></span>

<span data-ttu-id="d7f05-114">Unicode-Bereiche, die für diese Zuordnung gelten.</span><span class="sxs-lookup"><span data-stu-id="d7f05-114">Unicode ranges that apply to this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="d7f05-115">_rangesCount \*</span><span class="sxs-lookup"><span data-stu-id="d7f05-115">_rangesCount\*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f05-116">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d7f05-116">Type: **UINT32**</span></span>

<span data-ttu-id="d7f05-117">Anzahl von Unicode-Bereichen.</span><span class="sxs-lookup"><span data-stu-id="d7f05-117">Number of Unicode ranges.</span></span>

</dd> <dt>

<span data-ttu-id="d7f05-118">*targetfamilynames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d7f05-118">*targetFamilyNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f05-119">Typ: Konstante **WCHAR \* \***</span><span class="sxs-lookup"><span data-stu-id="d7f05-119">Type: **const WCHAR\*\***</span></span>

<span data-ttu-id="d7f05-120">Liste der Ziel Familiennamen-Zeichen folgen.</span><span class="sxs-lookup"><span data-stu-id="d7f05-120">List of target family name strings.</span></span>

</dd> <dt>

<span data-ttu-id="d7f05-121">*targetfamilynamescount*</span><span class="sxs-lookup"><span data-stu-id="d7f05-121">*targetFamilyNamesCount*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f05-122">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="d7f05-122">Type: **UINT32**</span></span>

<span data-ttu-id="d7f05-123">Anzahl der Ziel Familiennamen.</span><span class="sxs-lookup"><span data-stu-id="d7f05-123">Number of target family names.</span></span>

</dd> <dt>

<span data-ttu-id="d7f05-124">*FontCollection* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d7f05-124">*fontCollection* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f05-125">Typ: **[ **idschreitefontcollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span><span class="sxs-lookup"><span data-stu-id="d7f05-125">Type: **[**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection)**</span></span>

<span data-ttu-id="d7f05-126">Optionale explizite Schriftart Auflistung für diese Zuordnung.</span><span class="sxs-lookup"><span data-stu-id="d7f05-126">Optional explicit font collection for this mapping.</span></span>

</dd> <dt>

<span data-ttu-id="d7f05-127">*localename* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d7f05-127">*localeName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f05-128">Typ: \* Konstante *WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d7f05-128">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="d7f05-129">Das Gebiets Schema des Kontexts.</span><span class="sxs-lookup"><span data-stu-id="d7f05-129">Locale of the context.</span></span>

</dd> <dt>

<span data-ttu-id="d7f05-130">_baseFamilyName \* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d7f05-130">_baseFamilyName\* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f05-131">Typ: \* Konstante *WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="d7f05-131">Type: \**const WCHAR\** _</span></span>

<span data-ttu-id="d7f05-132">Der Basis Familienname für den Abgleich, falls zutreffend.</span><span class="sxs-lookup"><span data-stu-id="d7f05-132">Base family name to match against, if applicable.</span></span>

</dd> <dt>

<span data-ttu-id="d7f05-133">_scale \*</span><span class="sxs-lookup"><span data-stu-id="d7f05-133">_scale\*</span></span> 
</dt> <dd>

<span data-ttu-id="d7f05-134">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d7f05-134">Type: **FLOAT**</span></span>

<span data-ttu-id="d7f05-135">Der Skalierungsfaktor zum Multiplizieren der Ergebnisziel Schriftart.</span><span class="sxs-lookup"><span data-stu-id="d7f05-135">Scale factor to multiply the result target font by.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f05-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7f05-136">Return value</span></span>

<span data-ttu-id="d7f05-137">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d7f05-137">Type: **HRESULT**</span></span>

<span data-ttu-id="d7f05-138">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d7f05-138">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d7f05-139">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d7f05-139">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f05-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7f05-140">Requirements</span></span>



| <span data-ttu-id="d7f05-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7f05-141">Requirement</span></span> | <span data-ttu-id="d7f05-142">Wert</span><span class="sxs-lookup"><span data-stu-id="d7f05-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f05-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7f05-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f05-144">Windows 8.1 \[ Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f05-144">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="d7f05-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7f05-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f05-146">Windows Server 2012 R2 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f05-146">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                          |
| <span data-ttu-id="d7f05-147">Unterstützte Mindestversion (Telefon)</span><span class="sxs-lookup"><span data-stu-id="d7f05-147">Minimum supported phone</span></span><br/>  | <span data-ttu-id="d7f05-148">Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]</span><span class="sxs-lookup"><span data-stu-id="d7f05-148">Windows Phone 8.1 \[Windows Phone Silverlight 8.1 and Windows Runtime apps\]</span></span><br/> |
| <span data-ttu-id="d7f05-149">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7f05-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7f05-150"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7f05-150"><dt>Dwrite.lib</dt></span></span> </dl>   |
| <span data-ttu-id="d7f05-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d7f05-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7f05-152"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7f05-152"><dt>Dwrite.dll</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d7f05-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7f05-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f05-154">**Idschreitefontfallbackbuilder**</span><span class="sxs-lookup"><span data-stu-id="d7f05-154">**IDWriteFontFallbackBuilder**</span></span>](idwritefontfallbackbuilder.md)
</dt> </dl>

 

