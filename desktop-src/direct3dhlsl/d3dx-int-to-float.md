---
title: D3DX_INT_to_FLOAT-Funktion
description: Konvertiert einen int-Wert in float.
ms.assetid: bee2fb3e-ffde-4013-a321-275d6beb5f77
keywords:
- D3DX_INT_to_FLOAT-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_INT_to_FLOAT
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a4d588661b1b2f5ddc14c7564699c7d2b47b4e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982500"
---
# <a name="d3dx_int_to_float-function"></a><span data-ttu-id="1dfb2-104">D3DX \_ int \_ to \_ float-Funktion</span><span class="sxs-lookup"><span data-stu-id="1dfb2-104">D3DX\_INT\_to\_FLOAT function</span></span>

<span data-ttu-id="1dfb2-105">Konvertiert einen int-Wert in float.</span><span class="sxs-lookup"><span data-stu-id="1dfb2-105">Converts a INT value to FLOAT.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dfb2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dfb2-106">Syntax</span></span>

``` syntax
FLOAT D3DX_INT_to_FLOAT(
   INT _V,
   FLOAT _Scale
);
```

## <a name="parameters"></a><span data-ttu-id="1dfb2-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dfb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dfb2-108">*\_Ramelow*</span><span class="sxs-lookup"><span data-stu-id="1dfb2-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfb2-109">Der v-Wert.</span><span class="sxs-lookup"><span data-stu-id="1dfb2-109">The v value.</span></span>

</dd> <dt>

<span data-ttu-id="1dfb2-110">*\_Skalieren*</span><span class="sxs-lookup"><span data-stu-id="1dfb2-110">*\_Scale*</span></span> 
</dt> <dd>

<span data-ttu-id="1dfb2-111">Der Skalierungs Wert.</span><span class="sxs-lookup"><span data-stu-id="1dfb2-111">The scale value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dfb2-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1dfb2-112">Return value</span></span>

<span data-ttu-id="1dfb2-113">Der konvertierte int-Wert.</span><span class="sxs-lookup"><span data-stu-id="1dfb2-113">The converted int value.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dfb2-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="1dfb2-114">Requirements</span></span>



| <span data-ttu-id="1dfb2-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dfb2-115">Requirement</span></span> | <span data-ttu-id="1dfb2-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1dfb2-116">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1dfb2-117">Header</span><span class="sxs-lookup"><span data-stu-id="1dfb2-117">Header</span></span><br/> | <dl> <span data-ttu-id="1dfb2-118"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="1dfb2-118"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1dfb2-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dfb2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dfb2-120">Funktionen</span><span class="sxs-lookup"><span data-stu-id="1dfb2-120">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="1dfb2-121">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="1dfb2-121">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





