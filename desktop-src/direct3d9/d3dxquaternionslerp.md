---
description: Interpoliert zwischen zwei Quaternionen mit der Methode der sphärischen linearen Interpolation.
ms.assetid: 94a989c8-fa6b-4852-9aa3-e55ad814ffd7
title: D3DXQuaternionSlerp-Funktion (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f0f43e22ddc46007c6f589dfc5fd8b45aa885643
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354360"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="219d1-103">D3DXQuaternionSlerp-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="219d1-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="219d1-104">Interpoliert zwischen zwei Quaternionen mit der Methode der sphärischen linearen Interpolation.</span><span class="sxs-lookup"><span data-stu-id="219d1-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="219d1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="219d1-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="219d1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="219d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="219d1-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="219d1-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="219d1-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="219d1-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="219d1-109">Ein Zeiger auf die [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="219d1-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="219d1-110">*pQ1* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="219d1-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="219d1-111">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="219d1-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="219d1-112">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="219d1-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="219d1-113">*pQ2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="219d1-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="219d1-114">Typ: **Konstanten [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="219d1-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="219d1-115">Zeiger auf eine Quell- [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="219d1-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="219d1-116">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="219d1-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="219d1-117">Typ: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="219d1-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="219d1-118">-Parameter, der angibt, wie weit zwischen den Quaternionen interpolieren werden soll.</span><span class="sxs-lookup"><span data-stu-id="219d1-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="219d1-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="219d1-119">Return value</span></span>

<span data-ttu-id="219d1-120">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="219d1-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="219d1-121">Zeiger auf eine [**D3DXQUATERNION**](d3dxquaternion.md) -Struktur, die das Ergebnis der interpolung ist.</span><span class="sxs-lookup"><span data-stu-id="219d1-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="219d1-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="219d1-122">Remarks</span></span>

<span data-ttu-id="219d1-123">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="219d1-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="219d1-124">Auf diese Weise kann die **D3DXQuaternionSlerp** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="219d1-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="219d1-125">Verwenden Sie [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für eine beliebige Quaternion-Eingabe, die nicht bereits normalisiert ist.</span><span class="sxs-lookup"><span data-stu-id="219d1-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="219d1-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="219d1-126">Requirements</span></span>



| <span data-ttu-id="219d1-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="219d1-127">Requirement</span></span> | <span data-ttu-id="219d1-128">Wert</span><span class="sxs-lookup"><span data-stu-id="219d1-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="219d1-129">Header</span><span class="sxs-lookup"><span data-stu-id="219d1-129">Header</span></span><br/>  | <dl> <span data-ttu-id="219d1-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="219d1-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="219d1-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="219d1-131">Library</span></span><br/> | <dl> <span data-ttu-id="219d1-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="219d1-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="219d1-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="219d1-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="219d1-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="219d1-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
