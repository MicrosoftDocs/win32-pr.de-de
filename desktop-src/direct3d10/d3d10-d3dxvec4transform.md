---
description: Transformiert einen 4D-Vektor durch eine angegebene Matrix.
ms.assetid: ccbf33bc-1f94-4cf8-b048-220d54516e00
title: D3DXVec4Transform-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec4Transform
api_type:
- HeaderDef
api_location:
- D3DX10Math.h
ms.openlocfilehash: 56fc6b3041d799cda3e98d459b2523d4b171df10
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "103870095"
---
# <a name="d3dxvec4transform-function-d3dx10mathh"></a><span data-ttu-id="0f959-103">D3DXVec4Transform-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="0f959-103">D3DXVec4Transform function (D3DX10Math.h)</span></span>

<span data-ttu-id="0f959-104">Transformiert einen 4D-Vektor durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="0f959-104">Transforms a 4D vector by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f959-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f959-105">Syntax</span></span>


```C++
D3DXVECTOR4* D3DXVec4Transform(
  _Inout_       D3DXVECTOR4 *pOut,
  _In_    const D3DXVECTOR4 *pV,
  _In_    const D3DXMATRIX  *pM
);
```



## <a name="parameters"></a><span data-ttu-id="0f959-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f959-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f959-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0f959-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f959-108">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f959-108">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="0f959-109">Zeiger auf das [**D3DXVECTOR4**](d3d10-d3dxvector4.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="0f959-109">Pointer to the [**D3DXVECTOR4**](d3d10-d3dxvector4.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0f959-110">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f959-110">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f959-111">Typ: **Konstanten [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md) \***</span><span class="sxs-lookup"><span data-stu-id="0f959-111">Type: **const [**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="0f959-112">Ein Zeiger auf die Quell-D3DXVECTOR4-Struktur.</span><span class="sxs-lookup"><span data-stu-id="0f959-112">Pointer to the source D3DXVECTOR4 structure.</span></span>

</dd> <dt>

<span data-ttu-id="0f959-113">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f959-113">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f959-114">Typ: **Konstanten [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="0f959-114">Type: **const [**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0f959-115">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3d10-d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="0f959-115">Pointer to the source [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f959-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f959-116">Return value</span></span>

<span data-ttu-id="0f959-117">Typ: **[ **D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f959-117">Type: **[**D3DXVECTOR4**](../direct3d9/d3dxvector4.md)\***</span></span>

<span data-ttu-id="0f959-118">Zeiger auf eine D3DXVECTOR4-Struktur, die der transformierte 4D-Vektor ist.</span><span class="sxs-lookup"><span data-stu-id="0f959-118">Pointer to a D3DXVECTOR4 structure that is the transformed 4D vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f959-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f959-119">Remarks</span></span>

<span data-ttu-id="0f959-120">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0f959-120">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="0f959-121">Auf diese Weise kann die D3DXVec4Transform-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f959-121">In this way, the D3DXVec4Transform function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f959-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f959-122">Requirements</span></span>



| <span data-ttu-id="0f959-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f959-123">Requirement</span></span> | <span data-ttu-id="0f959-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0f959-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f959-125">Header</span><span class="sxs-lookup"><span data-stu-id="0f959-125">Header</span></span><br/> | <dl> <span data-ttu-id="0f959-126"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f959-126"><dt>D3DX10Math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f959-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f959-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f959-128">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="0f959-128">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
