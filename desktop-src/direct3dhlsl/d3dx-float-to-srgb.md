---
title: D3DX_FLOAT_to_SRGB-Funktion
description: Konvertiert einen float-Wert in einen sRGB-Wert.
ms.assetid: 734a0837-98da-45ba-bb0b-1e930ba78a7d
keywords:
- D3DX_FLOAT_to_SRGB-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_SRGB
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a71afb0c4e601be70c1ec04bd7bcd5e76c6cc573
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996178"
---
# <a name="d3dx_float_to_srgb-function"></a><span data-ttu-id="ce1fa-104">D3DX \_ float \_ zu \_ sRGB-Funktion</span><span class="sxs-lookup"><span data-stu-id="ce1fa-104">D3DX\_FLOAT\_to\_SRGB function</span></span>

<span data-ttu-id="ce1fa-105">Konvertiert einen float-Wert in einen sRGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-105">Converts a FLOAT value to an SRGB.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce1fa-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce1fa-106">Syntax</span></span>

``` syntax
FLOAT D3DX_FLOAT_to_SRGB(
   FLOAT val
);
```

## <a name="parameters"></a><span data-ttu-id="ce1fa-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce1fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce1fa-108">*ster*</span><span class="sxs-lookup"><span data-stu-id="ce1fa-108">*val*</span></span> 
</dt> <dd>

<span data-ttu-id="ce1fa-109">Der zu konvertierende Gleit Komma Wert.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-109">FLOAT value to convert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce1fa-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce1fa-110">Return value</span></span>

<span data-ttu-id="ce1fa-111">Der konvertierte sRGB-Wert.</span><span class="sxs-lookup"><span data-stu-id="ce1fa-111">The converted SRGB value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce1fa-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ce1fa-112">Requirements</span></span>



| <span data-ttu-id="ce1fa-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce1fa-113">Requirement</span></span> | <span data-ttu-id="ce1fa-114">Wert</span><span class="sxs-lookup"><span data-stu-id="ce1fa-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce1fa-115">Header</span><span class="sxs-lookup"><span data-stu-id="ce1fa-115">Header</span></span><br/> | <dl> <span data-ttu-id="ce1fa-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="ce1fa-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce1fa-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce1fa-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce1fa-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="ce1fa-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="ce1fa-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="ce1fa-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





