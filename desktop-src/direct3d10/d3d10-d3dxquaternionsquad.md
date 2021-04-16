---
description: Interpoliert zwischen Quaternionen mithilfe der sphärischen Quadranten-Interpolation.
ms.assetid: ba953731-4372-4b32-942b-23abfe479704
title: D3DXQuaternionSquad-Funktion (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSquad
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: af2bb582909cf09a4044b293f3f298a5da2335a5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530998"
---
# <a name="d3dxquaternionsquad-function-d3dx10mathh"></a><span data-ttu-id="f7246-103">D3DXQuaternionSquad-Funktion (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="f7246-103">D3DXQuaternionSquad function (D3DX10Math.h)</span></span>

<span data-ttu-id="f7246-104">Interpoliert zwischen Quaternionen mithilfe der sphärischen Quadranten-Interpolation.</span><span class="sxs-lookup"><span data-stu-id="f7246-104">Interpolates between quaternions, using spherical quadrangle interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7246-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7246-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSquad(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pA,
  _In_    const D3DXQUATERNION *pB,
  _In_    const D3DXQUATERNION *pC,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="f7246-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7246-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7246-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="f7246-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f7246-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7246-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f7246-109">Zeiger auf das [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) , das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="f7246-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="f7246-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7246-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7246-111">Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7246-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f7246-112">Zeiger auf eine Quell-D3DXQUATERNION-Struktur.</span><span class="sxs-lookup"><span data-stu-id="f7246-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="f7246-113">*PA* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7246-113">*pA* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7246-114">Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7246-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f7246-115">Zeiger auf eine Quell-D3DXQUATERNION-Struktur.</span><span class="sxs-lookup"><span data-stu-id="f7246-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="f7246-116">*PB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7246-116">*pB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7246-117">Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7246-117">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f7246-118">Zeiger auf eine Quell-D3DXQUATERNION-Struktur.</span><span class="sxs-lookup"><span data-stu-id="f7246-118">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="f7246-119">*PC* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7246-119">*pC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7246-120">Typ: **Konstanten [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="f7246-120">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f7246-121">Zeiger auf eine Quell-D3DXQUATERNION-Struktur.</span><span class="sxs-lookup"><span data-stu-id="f7246-121">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="f7246-122">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f7246-122">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7246-123">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f7246-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f7246-124">-Parameter, der angibt, wie weit zwischen den Quaternionen interpolieren werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7246-124">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7246-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f7246-125">Return value</span></span>

<span data-ttu-id="f7246-126">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="f7246-126">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="f7246-127">Zeiger auf eine D3DXQUATERNION-Struktur, die das Ergebnis der sphärischen Quadrangle-interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="f7246-127">Pointer to a D3DXQUATERNION structure that is the result of the spherical quadrangle interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7246-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f7246-128">Remarks</span></span>

<span data-ttu-id="f7246-129">Diese Funktion verwendet die folgende Sequenz von sphärischen linearen Interpolations Vorgängen:</span><span class="sxs-lookup"><span data-stu-id="f7246-129">This function uses the following sequence of spherical linear interpolation operations:</span></span>


```
Slerp(Slerp(pQ1, pC, t), Slerp(pA, pB, t), 2t(1 - t))
```



<span data-ttu-id="f7246-130">Der Rückgabewert für diese Funktion ist derselbe Wert, der im Pout-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f7246-130">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="f7246-131">Auf diese Weise kann die D3DXQuaternionSquad-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7246-131">In this way, the D3DXQuaternionSquad function can be used as a parameter for another function.</span></span>

<span data-ttu-id="f7246-132">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="f7246-132">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="f7246-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f7246-133">Requirements</span></span>



| <span data-ttu-id="f7246-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f7246-134">Requirement</span></span> | <span data-ttu-id="f7246-135">Wert</span><span class="sxs-lookup"><span data-stu-id="f7246-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7246-136">Header</span><span class="sxs-lookup"><span data-stu-id="f7246-136">Header</span></span><br/>  | <dl> <span data-ttu-id="f7246-137"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f7246-137"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="f7246-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f7246-138">Library</span></span><br/> | <dl> <span data-ttu-id="f7246-139"><dt>D3dx10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f7246-139"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f7246-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7246-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7246-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="f7246-141">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
