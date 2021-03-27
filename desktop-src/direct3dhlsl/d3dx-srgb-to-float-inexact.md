---
title: D3DX_SRGB_to_FLOAT_inexact-Funktion
description: Konvertiert einen sRGB-Wert in float. | D3DX_SRGB_to_FLOAT_inexact-Funktion
ms.assetid: 6eadda6d-ff99-4a8e-9e30-ae455732438e
keywords:
- D3DX_SRGB_to_FLOAT_inexact-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT_inexact
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44804ad73ab49ce4f62274c870d8487501c44361
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982209"
---
# <a name="d3dx_srgb_to_float_inexact-function"></a><span data-ttu-id="be7c1-105">D3DX \_ sRGB \_ in \_ \_ ungenau-Funktion</span><span class="sxs-lookup"><span data-stu-id="be7c1-105">D3DX\_SRGB\_to\_FLOAT\_inexact function</span></span>

<span data-ttu-id="be7c1-106">Konvertiert einen sRGB-Wert in float.</span><span class="sxs-lookup"><span data-stu-id="be7c1-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="be7c1-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="be7c1-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT_inexact(
   hlsl_precise FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="be7c1-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="be7c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="be7c1-109">*ster*</span><span class="sxs-lookup"><span data-stu-id="be7c1-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="be7c1-110">Der zu konvertierende sRGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="be7c1-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="be7c1-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be7c1-111">Return value</span></span>

<span data-ttu-id="be7c1-112">Der konvertierte sRGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="be7c1-112">The converted SRGB value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be7c1-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be7c1-113">Remarks</span></span>

<span data-ttu-id="be7c1-114">Diese Funktion hat keine hohe Genauigkeit, um die genaue Antwort zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="be7c1-114">This function doesn't have a high enough precision to give the exact answer.</span></span> <span data-ttu-id="be7c1-115">Die Alternative Funktion [**D3DX \_ sRGB \_ to \_ float**](d3dx-srgb-to-float.md) verwendet eine Nachschlage Tabelle, um eine exakte sRGB-Konvertierung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="be7c1-115">The alternative function [**D3DX\_SRGB\_to\_FLOAT**](d3dx-srgb-to-float.md) uses a lookup table to give an exact SRGB to float conversion.</span></span>

## <a name="requirements"></a><span data-ttu-id="be7c1-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="be7c1-116">Requirements</span></span>



| <span data-ttu-id="be7c1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be7c1-117">Requirement</span></span> | <span data-ttu-id="be7c1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="be7c1-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be7c1-119">Header</span><span class="sxs-lookup"><span data-stu-id="be7c1-119">Header</span></span><br/> | <dl> <span data-ttu-id="be7c1-120"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="be7c1-120"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be7c1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be7c1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be7c1-122">Funktionen</span><span class="sxs-lookup"><span data-stu-id="be7c1-122">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="be7c1-123">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="be7c1-123">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





