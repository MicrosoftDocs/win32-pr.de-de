---
title: Idwrite-fontface getgdicompatiblemetrics-Methode
description: Ruft Entwurfs Einheiten und allgemeine Metriken für die Schriftart ab. Diese Metriken gelten für alle Symbole innerhalb eines fontface und werden von Anwendungen für Layoutberechnungen verwendet.
ms.assetid: 9e132ec0-64cb-4681-b079-02a0047badd5
keywords:
- Getgdicompatiblemetrics-Methode direkt schreiben
- Getgdicompatiblemetrics-Methode direkt schreiben, idschreitefontface-Schnittstelle
- Idwrite Test fontface Interface Direct Write, getgdicompatiblemetrics-Methode
topic_type:
- apiref
api_name:
- IDWriteFontFace.GetGdiCompatibleMetrics
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81b1c00c872352c984c87ee84f7eaed5baffafd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370001"
---
# <a name="idwritefontfacegetgdicompatiblemetrics-method"></a><span data-ttu-id="d7709-107">Idschreitefontface:: getgdicompatiblemetrics-Methode</span><span class="sxs-lookup"><span data-stu-id="d7709-107">IDWriteFontFace::GetGdiCompatibleMetrics method</span></span>

<span data-ttu-id="d7709-108">Ruft Entwurfs Einheiten und allgemeine Metriken für die Schriftart ab.</span><span class="sxs-lookup"><span data-stu-id="d7709-108">Obtains design units and common metrics for the font face.</span></span> <span data-ttu-id="d7709-109">Diese Metriken gelten für alle Symbole innerhalb eines fontface und werden von Anwendungen für Layoutberechnungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="d7709-109">These metrics are applicable to all the glyphs within a fontface and are used by applications for layout calculations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7709-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7709-110">Syntax</span></span>


```C++
virtual HRESULT GetGdiCompatibleMetrics(
                       FLOAT               emSize,
                       FLOAT               pixelsPerDip,
  [in, optional] const DWRITE_MATRIX       *transform,
  [out]                DWRITE_FONT_METRICS *fontFaceMetrics
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="d7709-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7709-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7709-112">*emSize*</span><span class="sxs-lookup"><span data-stu-id="d7709-112">*emSize*</span></span> 
</dt> <dd>

<span data-ttu-id="d7709-113">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d7709-113">Type: **FLOAT**</span></span>

<span data-ttu-id="d7709-114">Die logische Größe der Schriftart in DIP-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="d7709-114">The logical size of the font in DIP units.</span></span>

</dd> <dt>

<span data-ttu-id="d7709-115">*Pixel sperdip*</span><span class="sxs-lookup"><span data-stu-id="d7709-115">*pixelsPerDip*</span></span> 
</dt> <dd>

<span data-ttu-id="d7709-116">Typ: **float**</span><span class="sxs-lookup"><span data-stu-id="d7709-116">Type: **FLOAT**</span></span>

<span data-ttu-id="d7709-117">Die Anzahl der physischen Pixel pro DIP.</span><span class="sxs-lookup"><span data-stu-id="d7709-117">The number of physical pixels per DIP.</span></span>

</dd> <dt>

<span data-ttu-id="d7709-118">*Transformation* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="d7709-118">*transform* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d7709-119">Typ: Konstante **[**dwrite- \_ Matrix**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix) \***</span><span class="sxs-lookup"><span data-stu-id="d7709-119">Type: **const [**DWRITE\_MATRIX**](/windows/win32/api/dwrite/ns-dwrite-dwrite_matrix)\***</span></span>

<span data-ttu-id="d7709-120">Eine optionale Transformation, die auf die Symbole und deren Positionen angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="d7709-120">An optional transform applied to the glyphs and their positions.</span></span> <span data-ttu-id="d7709-121">Diese Transformation wird nach der durch Schriftart Größe und *pixelsperdip* angegebenen Skalierung angewendet.</span><span class="sxs-lookup"><span data-stu-id="d7709-121">This transform is applied after the scaling specified by the font size and *pixelsPerDip*.</span></span>

</dd> <dt>

<span data-ttu-id="d7709-122">*fontfacemetrics* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d7709-122">*fontFaceMetrics* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7709-123">Typ: **[ **dwrite- \_ Schriftart \_ Metriken**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span><span class="sxs-lookup"><span data-stu-id="d7709-123">Type: **[**DWRITE\_FONT\_METRICS**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)\***</span></span>

<span data-ttu-id="d7709-124">Ein Zeiger auf eine [**dwrite- \_ Schriftart \_ Metrik**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S-Struktur, die ausgefüllt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d7709-124">A pointer to a [**DWRITE\_FONT\_METRIC**](/windows/win32/api/dwrite/ns-dwrite-dwrite_font_metrics)S structure to fill in.</span></span> <span data-ttu-id="d7709-125">Die von dieser Funktion zurückgegebenen Metriken sind in Schriftart Entwurfs Einheiten.</span><span class="sxs-lookup"><span data-stu-id="d7709-125">The metrics returned by this function are in font design units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7709-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d7709-126">Return value</span></span>

<span data-ttu-id="d7709-127">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d7709-127">Type: **HRESULT**</span></span>

<span data-ttu-id="d7709-128">Standard-HRESULT-Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="d7709-128">Standard HRESULT error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7709-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7709-129">Requirements</span></span>



| <span data-ttu-id="d7709-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7709-130">Requirement</span></span> | <span data-ttu-id="d7709-131">Wert</span><span class="sxs-lookup"><span data-stu-id="d7709-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d7709-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d7709-132">Library</span></span><br/> | <dl> <span data-ttu-id="d7709-133"><dt>Dwrite. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7709-133"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7709-134">DLL</span><span class="sxs-lookup"><span data-stu-id="d7709-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="d7709-135"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7709-135"><dt>Dwrite.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7709-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7709-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7709-137">**Idschreitefontface**</span><span class="sxs-lookup"><span data-stu-id="d7709-137">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> <dt>

[<span data-ttu-id="d7709-138">**Idschreitefontface**</span><span class="sxs-lookup"><span data-stu-id="d7709-138">**IDWriteFontFace**</span></span>](/windows/win32/api/dwrite/nn-dwrite-idwritefontface)
</dt> </dl>

 

