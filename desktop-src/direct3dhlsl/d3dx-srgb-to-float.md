---
title: D3DX_SRGB_to_FLOAT-Funktion
description: Konvertiert einen sRGB-Wert in float. | D3DX_SRGB_to_FLOAT-Funktion
ms.assetid: 03e2ea09-3dd7-48cb-81b3-e11f7a9cf0ee
keywords:
- D3DX_SRGB_to_FLOAT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_SRGB_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32e1b5dc6224a06881e227b82e74436c4820aaf3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961635"
---
# <a name="d3dx_srgb_to_float-function"></a><span data-ttu-id="cc732-105">D3DX \_ sRGB \_ to \_ float-Funktion</span><span class="sxs-lookup"><span data-stu-id="cc732-105">D3DX\_SRGB\_to\_FLOAT function</span></span>

<span data-ttu-id="cc732-106">Konvertiert einen sRGB-Wert in float.</span><span class="sxs-lookup"><span data-stu-id="cc732-106">Converts an SRGB value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc732-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc732-107">Syntax</span></span>

``` syntax
FLOAT D3DX_SRGB_to_FLOAT(
   UINT val
);
```

## <a name="parameters"></a><span data-ttu-id="cc732-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc732-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc732-109">*ster*</span><span class="sxs-lookup"><span data-stu-id="cc732-109">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="cc732-110">Der zu konvertierende sRGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="cc732-110">SRGB value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc732-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc732-111">Return value</span></span>

<span data-ttu-id="cc732-112">Der konvertierte sRGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="cc732-112">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc732-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cc732-113">Requirements</span></span>



| <span data-ttu-id="cc732-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc732-114">Requirement</span></span> | <span data-ttu-id="cc732-115">Wert</span><span class="sxs-lookup"><span data-stu-id="cc732-115">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc732-116">Header</span><span class="sxs-lookup"><span data-stu-id="cc732-116">Header</span></span><br/> | <dl> <span data-ttu-id="cc732-117"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="cc732-117"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc732-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc732-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc732-119">Funktionen</span><span class="sxs-lookup"><span data-stu-id="cc732-119">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="cc732-120">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="cc732-120">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





