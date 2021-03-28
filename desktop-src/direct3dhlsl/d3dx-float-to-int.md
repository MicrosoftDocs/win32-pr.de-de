---
title: D3DX_FLOAT_to_INT-Funktion
description: Konvertiert einen float-Wert in einen int-Wert.
ms.assetid: 69b67218-fe25-478f-9f7e-05f94d9f99d5
keywords:
- D3DX_FLOAT_to_INT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_FLOAT_to_INT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c127ef20cdd21cbc83e466f75844b4f80f47f948
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104531064"
---
# <a name="d3dx_float_to_int-function"></a><span data-ttu-id="5635a-104">D3DX \_ float \_ to \_ int-Funktion</span><span class="sxs-lookup"><span data-stu-id="5635a-104">D3DX\_FLOAT\_to\_INT function</span></span>

<span data-ttu-id="5635a-105">Konvertiert einen float-Wert in einen int-Wert.</span><span class="sxs-lookup"><span data-stu-id="5635a-105">Converts a FLOAT value to INT.</span></span>

## <a name="syntax"></a><span data-ttu-id="5635a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5635a-106">Syntax</span></span>

``` syntax
INT D3DX_FLOAT_to_INT(
   FLOAT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="5635a-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="5635a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5635a-108">*\_Ramelow*</span><span class="sxs-lookup"><span data-stu-id="5635a-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="5635a-109">Der v-Wert.</span><span class="sxs-lookup"><span data-stu-id="5635a-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="5635a-110">*\_Skalieren*</span><span class="sxs-lookup"><span data-stu-id="5635a-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="5635a-111">Der Skalierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="5635a-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5635a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5635a-112">Return value</span></span>

<span data-ttu-id="5635a-113">Der konvertierte float-Wert.</span><span class="sxs-lookup"><span data-stu-id="5635a-113">The converted FLOAT value</span></span>

## <a name="requirements"></a><span data-ttu-id="5635a-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="5635a-114">Requirements</span></span>



| <span data-ttu-id="5635a-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5635a-115">Requirement</span></span> | <span data-ttu-id="5635a-116">Wert</span><span class="sxs-lookup"><span data-stu-id="5635a-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5635a-117">Header</span><span class="sxs-lookup"><span data-stu-id="5635a-117">Header</span></span><br/> | <dl> <span data-ttu-id="5635a-118"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="5635a-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5635a-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5635a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5635a-120">Funktionen</span><span class="sxs-lookup"><span data-stu-id="5635a-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="5635a-121">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="5635a-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





