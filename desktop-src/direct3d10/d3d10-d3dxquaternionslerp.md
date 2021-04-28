---
description: 'D3DXQuaternionSlerp-Funktion (D3DX10Math.h): Interpoliert zwischen zwei Quaternionen mithilfe von sphärischer linearer Interpolation.'
ms.assetid: 487e1df1-bf20-49cb-ad14-61fcf1300904
title: D3DXQuaternionSlerp-Funktion (D3DX10Math.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXQuaternionSlerp
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 04cd3d82e4ca4e3f3357ab0114b57602f7e8a543
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103118"
---
# <a name="d3dxquaternionslerp-function-d3dx10mathh"></a><span data-ttu-id="6f95d-103">D3DXQuaternionSlerp-Funktion (D3DX10Math.h)</span><span class="sxs-lookup"><span data-stu-id="6f95d-103">D3DXQuaternionSlerp function (D3DX10Math.h)</span></span>

<span data-ttu-id="6f95d-104">Interpoliert zwischen zwei Quaternionen mit der Methode der sphärischen linearen Interpolation.</span><span class="sxs-lookup"><span data-stu-id="6f95d-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f95d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f95d-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="6f95d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f95d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f95d-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="6f95d-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f95d-108">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f95d-108">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6f95d-109">Zeiger auf [**D3DXQUATERNION,**](d3d10-d3dxquaternion.md) das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="6f95d-109">Pointer to the [**D3DXQUATERNION**](d3d10-d3dxquaternion.md) that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6f95d-110">*pQ1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6f95d-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f95d-111">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f95d-111">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6f95d-112">Zeiger auf eine D3DXQUATERNION-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="6f95d-112">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="6f95d-113">*pQ2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="6f95d-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f95d-114">Typ: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="6f95d-114">Type: **const [**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6f95d-115">Zeiger auf eine D3DXQUATERNION-Quellstruktur.</span><span class="sxs-lookup"><span data-stu-id="6f95d-115">Pointer to a source D3DXQUATERNION structure.</span></span>

</dd> <dt>

<span data-ttu-id="6f95d-116">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6f95d-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6f95d-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6f95d-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6f95d-118">Parameter, der angibt, wie weit zwischen den Quaternionen interpoliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f95d-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f95d-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f95d-119">Return value</span></span>

<span data-ttu-id="6f95d-120">Typ: **[ **D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="6f95d-120">Type: **[**D3DXQUATERNION**](../direct3d9/d3dxquaternion.md)\***</span></span>

<span data-ttu-id="6f95d-121">Zeiger auf eine D3DXQUATERNION-Struktur, die das Ergebnis der Interpolation ist.</span><span class="sxs-lookup"><span data-stu-id="6f95d-121">Pointer to a D3DXQUATERNION structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f95d-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f95d-122">Remarks</span></span>

<span data-ttu-id="6f95d-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im pOut-Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="6f95d-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6f95d-124">Auf diese Weise kann die D3DXQuaternionSlerp-Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6f95d-124">In this way, the D3DXQuaternionSlerp function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6f95d-125">Verwenden Sie [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) für alle Quaternioneingaben, die nicht bereits normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="6f95d-125">Use [**D3DXQuaternionNormalize**](d3d10-d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f95d-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f95d-126">Requirements</span></span>



| <span data-ttu-id="6f95d-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f95d-127">Requirement</span></span> | <span data-ttu-id="6f95d-128">Wert</span><span class="sxs-lookup"><span data-stu-id="6f95d-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f95d-129">Header</span><span class="sxs-lookup"><span data-stu-id="6f95d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6f95d-130"><dt>D3DX10Math.h</dt></span><span class="sxs-lookup"><span data-stu-id="6f95d-130"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6f95d-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6f95d-131">Library</span></span><br/> | <dl> <span data-ttu-id="6f95d-132"><dt>D3DX10.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6f95d-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6f95d-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="6f95d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f95d-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="6f95d-134">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
