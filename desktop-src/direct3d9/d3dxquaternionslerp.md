---
description: 'D3DXQuaternionSlerp-Funktion (D3dx9math.h): Interpoliert mithilfe der pherischen linearen Interpolation zwischen zwei Quaternionen.'
ms.assetid: 94a989c8-fa6b-4852-9aa3-e55ad814ffd7
title: D3DXQuaternionSlerp-Funktion (D3dx9math.h)
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
ms.openlocfilehash: fb9110da7fae4ebbf4609d361124dbbcdedfe59b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108093938"
---
# <a name="d3dxquaternionslerp-function-d3dx9mathh"></a><span data-ttu-id="082ff-103">D3DXQuaternionSlerp-Funktion (D3dx9math.h)</span><span class="sxs-lookup"><span data-stu-id="082ff-103">D3DXQuaternionSlerp function (D3dx9math.h)</span></span>

<span data-ttu-id="082ff-104">Interpoliert zwischen zwei Quaternionen mit der Methode der sphärischen linearen Interpolation.</span><span class="sxs-lookup"><span data-stu-id="082ff-104">Interpolates between two quaternions, using spherical linear interpolation.</span></span>

## <a name="syntax"></a><span data-ttu-id="082ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="082ff-105">Syntax</span></span>


```C++
D3DXQUATERNION* D3DXQuaternionSlerp(
  _Inout_       D3DXQUATERNION *pOut,
  _In_    const D3DXQUATERNION *pQ1,
  _In_    const D3DXQUATERNION *pQ2,
  _In_          FLOAT          t
);
```



## <a name="parameters"></a><span data-ttu-id="082ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="082ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="082ff-107">*pOut* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="082ff-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="082ff-108">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="082ff-108">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="082ff-109">Zeiger auf die [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="082ff-109">Pointer to the [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="082ff-110">*pQ1* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="082ff-110">*pQ1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="082ff-111">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="082ff-111">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="082ff-112">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="082ff-112">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="082ff-113">*pQ2* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="082ff-113">*pQ2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="082ff-114">Typ: **const [**D3DXQUATERNION**](d3dxquaternion.md) \***</span><span class="sxs-lookup"><span data-stu-id="082ff-114">Type: **const [**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="082ff-115">Zeiger auf eine [**D3DXQUATERNION-Quellstruktur.**](d3dxquaternion.md)</span><span class="sxs-lookup"><span data-stu-id="082ff-115">Pointer to a source [**D3DXQUATERNION**](d3dxquaternion.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="082ff-116">*t* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="082ff-116">*t* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="082ff-117">Typ: **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="082ff-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="082ff-118">Parameter, der angibt, wie weit zwischen den Quaternionen interpoliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="082ff-118">Parameter that indicates how far to interpolate between the quaternions.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="082ff-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="082ff-119">Return value</span></span>

<span data-ttu-id="082ff-120">Typ: **[ **D3DXQUATERNION**](d3dxquaternion.md)\***</span><span class="sxs-lookup"><span data-stu-id="082ff-120">Type: **[**D3DXQUATERNION**](d3dxquaternion.md)\***</span></span>

<span data-ttu-id="082ff-121">Zeiger auf eine [**D3DXQUATERNION-Struktur,**](d3dxquaternion.md) die das Ergebnis der Interpolation ist.</span><span class="sxs-lookup"><span data-stu-id="082ff-121">Pointer to a [**D3DXQUATERNION**](d3dxquaternion.md) structure that is the result of the interpolation.</span></span>

## <a name="remarks"></a><span data-ttu-id="082ff-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="082ff-122">Remarks</span></span>

<span data-ttu-id="082ff-123">Der Rückgabewert für diese Funktion ist der gleiche Wert, der im *pOut-Parameter zurückgegeben* wird.</span><span class="sxs-lookup"><span data-stu-id="082ff-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="082ff-124">Auf diese Weise kann die **D3DXQuaternionSlerp-Funktion** als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="082ff-124">In this way, the **D3DXQuaternionSlerp** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="082ff-125">Verwenden [**Sie D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) für alle Quaternioneingaben, die noch nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="082ff-125">Use [**D3DXQuaternionNormalize**](d3dxquaternionnormalize.md) for any quaternion input that is not already normalized.</span></span>

## <a name="requirements"></a><span data-ttu-id="082ff-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="082ff-126">Requirements</span></span>



| <span data-ttu-id="082ff-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="082ff-127">Requirement</span></span> | <span data-ttu-id="082ff-128">Wert</span><span class="sxs-lookup"><span data-stu-id="082ff-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="082ff-129">Header</span><span class="sxs-lookup"><span data-stu-id="082ff-129">Header</span></span><br/>  | <dl> <span data-ttu-id="082ff-130"><dt>D3dx9math.h</dt></span><span class="sxs-lookup"><span data-stu-id="082ff-130"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="082ff-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="082ff-131">Library</span></span><br/> | <dl> <span data-ttu-id="082ff-132"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="082ff-132"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="082ff-133">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="082ff-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="082ff-134">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="082ff-134">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
