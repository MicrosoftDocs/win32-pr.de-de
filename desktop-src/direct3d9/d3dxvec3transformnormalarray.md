---
description: Transformiert ein Array (x, y, z, 0) durch eine angegebene Matrix.
ms.assetid: c12fad52-d541-483f-a919-e6031aa4f761
title: D3DXVec3TransformNormalArray-Funktion (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXVec3TransformNormalArray
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7a70893cc38d2f2fa04b3b89432aa0f887c5a352
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2021
ms.locfileid: "106354402"
---
# <a name="d3dxvec3transformnormalarray-function-d3dx9mathh"></a><span data-ttu-id="1dd7e-103">D3DXVec3TransformNormalArray-Funktion (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="1dd7e-103">D3DXVec3TransformNormalArray function (D3dx9math.h)</span></span>

<span data-ttu-id="1dd7e-104">Transformiert ein Array (x, y, z, 0) durch eine angegebene Matrix.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-104">Transforms an array (x, y, z, 0) by a given matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="1dd7e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1dd7e-105">Syntax</span></span>


```C++
D3DXVECTOR3* D3DXVec3TransformNormalArray(
  _Inout_       D3DXVECTOR3 *pOut,
  _In_          UINT        OutStride,
  _In_    const D3DXVECTOR3 *pV,
  _In_          UINT        VStride,
  _In_    const D3DXMATRIX  *pM,
  _In_          UINT        n
);
```



## <a name="parameters"></a><span data-ttu-id="1dd7e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1dd7e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1dd7e-107">*Pout* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="1dd7e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd7e-108">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1dd7e-108">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1dd7e-109">Zeiger auf das [**D3DXVECTOR3**](d3dxvector3.md) -Array, das das Ergebnis des Vorgangs ist.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-109">Pointer to the [**D3DXVECTOR3**](d3dxvector3.md) array that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1dd7e-110">*Outstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dd7e-110">*OutStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd7e-111">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1dd7e-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1dd7e-112">Schritt zwischen Vektoren im Ausgabedatenstrom.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-112">Stride between vectors in the output data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1dd7e-113">*PV* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dd7e-113">*pV* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd7e-114">Typ: **Konstanten [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="1dd7e-114">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1dd7e-115">Zeiger auf das Quell- [**D3DXVECTOR3**](d3dxvector3.md) Array.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-115">Pointer to the source [**D3DXVECTOR3**](d3dxvector3.md) array.</span></span>

</dd> <dt>

<span data-ttu-id="1dd7e-116">*Vstride* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dd7e-116">*VStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd7e-117">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1dd7e-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1dd7e-118">Schritt zwischen Vektoren im Eingabedaten Strom.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-118">Stride between vectors in the input data stream.</span></span>

</dd> <dt>

<span data-ttu-id="1dd7e-119">*pm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dd7e-119">*pM* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd7e-120">Typ: **Konstanten [**D3DXMATRIX**](d3dxmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="1dd7e-120">Type: **const [**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="1dd7e-121">Ein Zeiger auf die Quell- [**D3DXMATRIX**](d3dxmatrix.md) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-121">Pointer to the source [**D3DXMATRIX**](d3dxmatrix.md) structure.</span></span>

</dd> <dt>

<span data-ttu-id="1dd7e-122">*n* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1dd7e-122">*n* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1dd7e-123">Typ: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1dd7e-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1dd7e-124">Anzahl der Elemente im Array.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-124">Number of elements in the array.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1dd7e-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1dd7e-125">Return value</span></span>

<span data-ttu-id="1dd7e-126">Typ: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="1dd7e-126">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="1dd7e-127">Zeiger auf ein [**D3DXVECTOR3**](d3dxvector3.md) -Array, das das transformierte Array ist.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-127">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) array that is the transformed array.</span></span>

## <a name="remarks"></a><span data-ttu-id="1dd7e-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1dd7e-128">Remarks</span></span>

<span data-ttu-id="1dd7e-129">Diese Funktion transformiert den Vektor (*PV*->x, *PV*->y, *PV*->z, 0) durch die Matrix, auf die von *pm* gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-129">This function transforms the vector (*pV*->x, *pV*->y, *pV*->z, 0) by the matrix pointed to by *pM*.</span></span>

<span data-ttu-id="1dd7e-130">Wenn Sie eine normale Transformation durchführen möchten, sollte die Matrix, die Sie an diese Funktion übergeben, die Umwandlung der Umkehrung der Matrix sein, die zum Transformieren eines Punkts verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-130">If you want to transform a normal, the matrix you pass to this function should be the transpose of the inverse of the matrix you would use to transform a point.</span></span>

<span data-ttu-id="1dd7e-131">Der Rückgabewert für diese Funktion ist derselbe Wert, der im *Pout* -Parameter zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-131">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="1dd7e-132">Auf diese Weise kann die **D3DXVec3TransformNormalArray** -Funktion als Parameter für eine andere Funktion verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1dd7e-132">In this way, the **D3DXVec3TransformNormalArray** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1dd7e-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1dd7e-133">Requirements</span></span>



| <span data-ttu-id="1dd7e-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1dd7e-134">Requirement</span></span> | <span data-ttu-id="1dd7e-135">Wert</span><span class="sxs-lookup"><span data-stu-id="1dd7e-135">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1dd7e-136">Header</span><span class="sxs-lookup"><span data-stu-id="1dd7e-136">Header</span></span><br/>  | <dl> <span data-ttu-id="1dd7e-137"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="1dd7e-137"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="1dd7e-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1dd7e-138">Library</span></span><br/> | <dl> <span data-ttu-id="1dd7e-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1dd7e-139"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="1dd7e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1dd7e-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1dd7e-141">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1dd7e-141">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
