---
description: Addiert zwei Farbwerte, um einen neuen Farbwert zu erstellen.
ms.assetid: 7743392d-4676-4408-93e9-f92d4bf02411
title: D3DXColorAdd-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXColorAdd
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f326c9bec4802a9a94accc76b825cd1c6ea28fd5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106353742"
---
# <a name="d3dxcoloradd-function"></a><span data-ttu-id="4268d-103">D3DXColorAdd-Funktion</span><span class="sxs-lookup"><span data-stu-id="4268d-103">D3DXColorAdd function</span></span>

<span data-ttu-id="4268d-104">Addiert zwei Farbwerte, um einen neuen Farbwert zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4268d-104">Adds two color values together to create a new color value.</span></span>

## <a name="syntax"></a><span data-ttu-id="4268d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4268d-105">Syntax</span></span>


```C++
D3DXCOLOR* D3DXColorAdd(
  _Inout_       D3DXCOLOR *pOut,
  _In_    const D3DXCOLOR *pC1,
  _In_    const D3DXCOLOR *pC2
);
```



## <a name="parameters"></a><span data-ttu-id="4268d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4268d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4268d-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="4268d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4268d-108">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="4268d-108">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="4268d-109">Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="4268d-109">Pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="4268d-110">*pC1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4268d-110">*pC1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4268d-111">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="4268d-111">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="4268d-112">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4268d-112">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4268d-113">*pC2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4268d-113">*pC2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4268d-114">Typ: **Konstanten [**D3DXCOLOR**](d3dxcolor.md) \***</span><span class="sxs-lookup"><span data-stu-id="4268d-114">Type: **const [**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="4268d-115">Zeiger auf eine Quell- [**D3DXCOLOR**](d3dxcolor.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="4268d-115">Pointer to a source [**D3DXCOLOR**](d3dxcolor.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4268d-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4268d-116">Return value</span></span>

<span data-ttu-id="4268d-117">Typ: **[ **D3DXCOLOR**](d3dxcolor.md)\***</span><span class="sxs-lookup"><span data-stu-id="4268d-117">Type: **[**D3DXCOLOR**](d3dxcolor.md)\***</span></span>

<span data-ttu-id="4268d-118">Diese Funktion gibt einen Zeiger auf eine [**D3DXCOLOR**](d3dxcolor.md) -Struktur zurück, die die Summe von zwei Farbwerten ist.</span><span class="sxs-lookup"><span data-stu-id="4268d-118">This function returns a pointer to a [**D3DXCOLOR**](d3dxcolor.md) structure that is the sum of two color values.</span></span>

## <a name="remarks"></a><span data-ttu-id="4268d-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4268d-119">Remarks</span></span>

<span data-ttu-id="4268d-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der in "Pout" zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="4268d-120">The return value for this function is the same value returned in pOut.</span></span> <span data-ttu-id="4268d-121">Auf diese Weise kann die **D3DXColorAdd** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4268d-121">In this way, the **D3DXColorAdd** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="4268d-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4268d-122">Requirements</span></span>



| <span data-ttu-id="4268d-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4268d-123">Requirement</span></span> | <span data-ttu-id="4268d-124">Wert</span><span class="sxs-lookup"><span data-stu-id="4268d-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="4268d-125">Header</span><span class="sxs-lookup"><span data-stu-id="4268d-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4268d-126"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="4268d-126"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="4268d-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4268d-127">Library</span></span><br/> | <dl> <span data-ttu-id="4268d-128"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4268d-128"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4268d-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4268d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4268d-130">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4268d-130">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="4268d-131">**D3DXColorModulate**</span><span class="sxs-lookup"><span data-stu-id="4268d-131">**D3DXColorModulate**</span></span>](d3dxcolormodulate.md)
</dt> <dt>

[<span data-ttu-id="4268d-132">**D3DXColorSubtract**</span><span class="sxs-lookup"><span data-stu-id="4268d-132">**D3DXColorSubtract**</span></span>](d3dxcolorsubtract.md)
</dt> </dl>

 

 




