---
title: D3DX_IsNan-Funktion
description: Bestimmt, ob der Wert ein NaN (not a Number) ist.
ms.assetid: 862d1d34-36ab-471e-b3ce-ce71896441e5
keywords:
- D3DX_IsNan-Funktion HLSL
topic_type:
- apiref
api_name:
- D3DX_IsNan
api_location:
- D3DX_DXGIFormatConvert.inl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 60aac82ebfb145bc11aac8d4ab509a4260767a74
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103961734"
---
# <a name="d3dx_isnan-function"></a><span data-ttu-id="cd7eb-104">D3DX \_ isNaN-Funktion</span><span class="sxs-lookup"><span data-stu-id="cd7eb-104">D3DX\_IsNan function</span></span>

<span data-ttu-id="cd7eb-105">Bestimmt, ob der Wert ein NaN (not a Number) ist.</span><span class="sxs-lookup"><span data-stu-id="cd7eb-105">Determines if the value is a NaN (Not a Number).</span></span>

## <a name="syntax"></a><span data-ttu-id="cd7eb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cd7eb-106">Syntax</span></span>

``` syntax
bool D3DX_IsNan(
   FLOAT _V
);
```

## <a name="parameters"></a><span data-ttu-id="cd7eb-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="cd7eb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd7eb-108">*\_Ramelow*</span><span class="sxs-lookup"><span data-stu-id="cd7eb-108">*\_V*</span></span> 
</dt> <dd>

<span data-ttu-id="cd7eb-109">Der angegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="cd7eb-109">The specified value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd7eb-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cd7eb-110">Return value</span></span>

<span data-ttu-id="cd7eb-111">true, wenn ein NaN; andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="cd7eb-111">true if a NaN; otherwise false.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd7eb-112">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="cd7eb-112">Requirements</span></span>



| <span data-ttu-id="cd7eb-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cd7eb-113">Requirement</span></span> | <span data-ttu-id="cd7eb-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cd7eb-114">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd7eb-115">Header</span><span class="sxs-lookup"><span data-stu-id="cd7eb-115">Header</span></span><br/> | <dl> <span data-ttu-id="cd7eb-116"><dt>D3DX \_ dxgiformatconvert. INL</dt></span><span class="sxs-lookup"><span data-stu-id="cd7eb-116"><dt>D3DX\_DXGIFormatConvert.inl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd7eb-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd7eb-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd7eb-118">Funktionen</span><span class="sxs-lookup"><span data-stu-id="cd7eb-118">Functions</span></span>](format-conversion-functions.md)
</dt> <dt>

[<span data-ttu-id="cd7eb-119">Entpacken und Verpacken des DXGI- \_ Formats für In-Place Bildbearbeitung</span><span class="sxs-lookup"><span data-stu-id="cd7eb-119">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>](dx-graphics-hlsl-unpacking-packing-dxgi-format.md)
</dt> </dl>

 

 





