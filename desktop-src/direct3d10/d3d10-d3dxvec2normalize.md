---
description: 'D3DXVec2Normalize-Funktion (D3DX10Math.h): Gibt die normalisierte Version eines 2D-Vektors zurück.'
ms.assetid: fac4f269-2778-4500-af9e-23a0112543b0
title: D3DXVec2Normalize-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec2Normalize
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: aaa7bde759b9023b69204d6cb39259f0905b9928
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108388"
---
# <a name="d3dxvec2normalize-function-d3dx10mathh"></a><span data-ttu-id="bd7d0-103">D3DXVec2Normalize-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="bd7d0-103">D3DXVec2Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="bd7d0-104">Gibt die normalisierte Version eines 2D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="bd7d0-104">Returns the normalized version of a 2D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd7d0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd7d0-105">Syntax</span></span>


```C++
D3DXVECTOR2* D3DXVec2Normalize(
  _Inout_       D3DXVECTOR2 *pOut,
  _In_    const D3DXVECTOR2 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="bd7d0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd7d0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd7d0-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="bd7d0-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="bd7d0-108">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd7d0-108">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bd7d0-109">Zeiger auf [**D3DXVECTOR2,**](d3d10-d3dxvector2.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="bd7d0-109">Pointer to the [**D3DXVECTOR2**](d3d10-d3dxvector2.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="bd7d0-110">*pV* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="bd7d0-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd7d0-111">Typ: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md) \***</span><span class="sxs-lookup"><span data-stu-id="bd7d0-111">Type: **const [**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bd7d0-112">Zeiger auf die D3DXVECTOR2-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="bd7d0-112">Pointer to the source D3DXVECTOR2 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd7d0-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd7d0-113">Return value</span></span>

<span data-ttu-id="bd7d0-114">Typ: **[ **D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span><span class="sxs-lookup"><span data-stu-id="bd7d0-114">Type: **[**D3DXVECTOR2**](../direct3d9/d3dxvector2.md)\***</span></span>

<span data-ttu-id="bd7d0-115">Zeiger auf eine D3DXVECTOR2-Struktur, die die normalisierte Version des Vektors ist.</span><span class="sxs-lookup"><span data-stu-id="bd7d0-115">Pointer to a D3DXVECTOR2 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="bd7d0-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd7d0-116">Remarks</span></span>

<span data-ttu-id="bd7d0-117">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bd7d0-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="bd7d0-118">Auf diese Weise kann die D3DXVec2Normalize-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bd7d0-118">In this way, the D3DXVec2Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd7d0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd7d0-119">Requirements</span></span>



| <span data-ttu-id="bd7d0-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bd7d0-120">Requirement</span></span> | <span data-ttu-id="bd7d0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bd7d0-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd7d0-122">Header</span><span class="sxs-lookup"><span data-stu-id="bd7d0-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bd7d0-123"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="bd7d0-123"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="bd7d0-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bd7d0-124">Library</span></span><br/> | <dl> <span data-ttu-id="bd7d0-125"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="bd7d0-125"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bd7d0-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bd7d0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd7d0-127">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="bd7d0-127">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
