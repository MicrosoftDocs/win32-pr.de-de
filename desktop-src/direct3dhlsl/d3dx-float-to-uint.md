---
title: D3DX_FLOAT_to_UINT-Funktion
description: Konvertiert einen float-Wert in uint.
ms.assetid: 05c5de72-8915-4541-a82d-242e46bfa883
keywords:
- D3DX_FLOAT_to_UINT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_UINT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e729ba805d63068844192a134236722288fe8a9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354296"
---
# <a name="d3dx_float_to_uint-function"></a><span data-ttu-id="cca82-104">D3DX \_ float \_ in \_ uint-Funktion</span><span class="sxs-lookup"><span data-stu-id="cca82-104">D3DX\_FLOAT\_to\_UINT function</span></span>

<span data-ttu-id="cca82-105">Konvertiert einen float-Wert in uint.</span><span class="sxs-lookup"><span data-stu-id="cca82-105">Converts a FLOAT value to UINT.</span></span>

## <a name="syntax"></a><span data-ttu-id="cca82-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cca82-106">Syntax</span></span>

``` syntax
UINT D3DX_FLOAT_to_UINT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="cca82-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cca82-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cca82-108">*\_Ramelow*</span><span class="sxs-lookup"><span data-stu-id="cca82-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="cca82-109">Der v-Vektor.</span><span class="sxs-lookup"><span data-stu-id="cca82-109">The v vector.</span></span>

</dd> <dt>

<span data-ttu-id="cca82-110">*\_Skalieren*</span><span class="sxs-lookup"><span data-stu-id="cca82-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="cca82-111">Der Skalierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="cca82-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cca82-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cca82-112">Return value</span></span>

<span data-ttu-id="cca82-113">Der konvertierte float-Wert.</span><span class="sxs-lookup"><span data-stu-id="cca82-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="cca82-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cca82-114">Requirements</span></span>



| <span data-ttu-id="cca82-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cca82-115">Requirement</span></span> | <span data-ttu-id="cca82-116">Wert</span><span class="sxs-lookup"><span data-stu-id="cca82-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cca82-117">Header</span><span class="sxs-lookup"><span data-stu-id="cca82-117">Header</span></span><br/> | <dl> <span data-ttu-id="cca82-118"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="cca82-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cca82-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cca82-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cca82-120">Funktionen</span><span class="sxs-lookup"><span data-stu-id="cca82-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="cca82-121">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="cca82-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





