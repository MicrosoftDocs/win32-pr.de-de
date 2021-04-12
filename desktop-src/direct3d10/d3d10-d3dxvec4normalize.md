---
description: Gibt die normalisierte Version eines 4D-Vektors zurück.
ms.assetid: ed3c48cf-4985-4ef3-b733-f8532e3ff6b5
title: D3DXVec4Normalize-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Normalize
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: ebedbdddbe558bfad71520b64aa0cf2ff4c2f451
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355296"
---
# <a name="d3dxvec4normalize-function-d3dx10mathh"></a><span data-ttu-id="d98a7-103">D3DXVec4Normalize-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="d98a7-103">D3DXVec4Normalize function (D3DX10Math.h)</span></span>

<span data-ttu-id="d98a7-104">Gibt die normalisierte Version eines 4D-Vektors zurück.</span><span class="sxs-lookup"><span data-stu-id="d98a7-104">Returns the normalized version of a 4D vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="d98a7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d98a7-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Normalize(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV
);
```



## <a name="parameters"></a><span data-ttu-id="d98a7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d98a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d98a7-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="d98a7-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="d98a7-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d98a7-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="d98a7-109">Zeiger auf das [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="d98a7-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="d98a7-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d98a7-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d98a7-111">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="d98a7-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="d98a7-112">Ein Zeiger auf die Quell-D3DXVECTOR4-Struktur.</span><span class="sxs-lookup"><span data-stu-id="d98a7-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d98a7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d98a7-113">Return value</span></span>

<span data-ttu-id="d98a7-114">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="d98a7-114">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="d98a7-115">Zeiger auf eine D3DXVECTOR4-Struktur, die die normalisierte Version des Vektors ist.</span><span class="sxs-lookup"><span data-stu-id="d98a7-115">Pointer to a D3DXVECTOR4 structure that is the normalized version of the vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="d98a7-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d98a7-116">Remarks</span></span>

<span data-ttu-id="d98a7-117">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d98a7-117">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="d98a7-118">Auf diese Weise kann die D3DXVec4Normalize-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d98a7-118">In this way, the D3DXVec4Normalize function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d98a7-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d98a7-119">Requirements</span></span>



| <span data-ttu-id="d98a7-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d98a7-120">Requirement</span></span> | <span data-ttu-id="d98a7-121">Wert</span><span class="sxs-lookup"><span data-stu-id="d98a7-121">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d98a7-122">Header</span><span class="sxs-lookup"><span data-stu-id="d98a7-122">Header</span></span><br/> | <dl> <span data-ttu-id="d98a7-123"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d98a7-123"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d98a7-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d98a7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d98a7-125">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="d98a7-125">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
